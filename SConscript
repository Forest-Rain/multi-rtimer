Import('RTT_ROOT')
Import('rtconfig')
from building import *

cwd     = GetCurrentDir()
src     = Split('''multi_rtimer.c
				hw_rtc_stm32l.c''') 

if GetDepend(['PKG_USING_MULTI_RTIMER_EXAMPLE']):
    src += Glob('multi_rtimer_example.c')

CPPPATH = [cwd]

group = DefineGroup('multi_rtimer', src, depend = ['PKG_USING_MULTI_RTIMER'], CPPPATH = CPPPATH)

Return('group')