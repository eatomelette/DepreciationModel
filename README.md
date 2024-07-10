关于永续期折旧和资本性支出匹配的


假设:  
  1. 年初折现
  2. 设备年初开始提折旧
  3. 年折旧额A相等
  4. 折现率 $r$;  
  5. 折旧年限$t_d$;  
  6. 经济寿命$t_e$;


为了表示方便，令    $R = \dfrac{1}{1+r}$  ；

按照预测年度者旧额相等均为A，折旧的现值：
  $$\sum_{年折旧额相同} = PV(r,\infty,-A)  \\
    = \sum_{i=0}^\infty AR^{i}  \\
    = \dfrac{A}{1-R}
  $$

按照设备经济寿命为周期进行更新设备，即每到设备经济寿命开始更新设备，更新后按照每年A在设备折旧期内提折旧：

$$
 \sum_{按照经济寿命更新设备}=PV(\dfrac{1}{R^{t_e}}-1,\infty,-PV(r,t_d,-A))    \\

   =PV(\dfrac{1}{R^{t_e}}-1,\infty,-\dfrac{A(1-R^{t_d})}{1-R})\\
   =\dfrac{\dfrac{A(1-R^{t_d})}{1-R}}{1-R^{t_e}}
$$

那么，
$$ \dfrac{\sum_{年折旧额相同} }{\sum_{按照经济寿命更新设备}} = \dfrac{1-R^{t_d}}{1-R^{t_e}}
$$

$$
\sum_{按照经济寿命更新设备} = \dfrac{1-R^{t_e}}{1-R^{t_d}}*PV(r,\infty,-A)
$$


这个式子的意义在于可以方便的在EXCEL中计算出按照设备经济寿命进行更新的模式下，预测的永续期折旧。


若假设设备残值为0，相应的资本性支出 
$$
  \sum_{资本性支出}= PV(r,\infty,-A*t_d)
$$
