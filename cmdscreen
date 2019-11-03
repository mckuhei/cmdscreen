#-*- coding:utf-8 -*-#

import ctypes,sys
 
STD_INPUT_HANDLE = -10
STD_OUTPUT_HANDLE = -11
STD_ERROR_HANDLE = -12

std_out_handle = ctypes.windll.kernel32.GetStdHandle(STD_OUTPUT_HANDLE)

class COORD(ctypes.Structure): 
     _fields_ = [("X", ctypes.c_short), ("Y", ctypes.c_short)] 
     def __init__(self,x,y):
         self.X = x
         self.Y = y


def MoveCursor(x,y,handle=std_out_handle):
    pos = COORD(x,y)
    Bool = ctypes.windll.kernel32.SetConsoleCursorPosition(handle,pos)
    return Bool


def printcolors(mess,bg=0x00,end='\n',reset=True):
    set_cmd_text_color(bg)
    sys.stdout.write(mess + end)
    if reset:
        resetColor()

 
def set_cmd_text_color(color, handle=std_out_handle):
    Bool = ctypes.windll.kernel32.SetConsoleTextAttribute(handle, color)
    return Bool
 

def resetColor():
    set_cmd_text_color(0x07)
