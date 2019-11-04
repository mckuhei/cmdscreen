# cmdscreen
Allow you change cmd screen color
# Explames
    import cmdscreen
    import os
    for i in range(30):
        cmdscreen.MoveCursor(i,0)
        print('                                                                                                                       ')
    cmdscreen.printcolors('Hello!This color code:',0xfc,'\n',False)
    os.system('color /?')
    cmdscreen.printcolors('Explames:If i need foreground(Text color) is 7,and i need background is 0,so i need type 0x07 in color,Like:cmdscreen.printcolors(\u0027Hello!This color code:\u0027,0x07,\u0027\\n\u0027,False)')
    
