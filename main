import wx, time
username, password = 'GGT','GGT'
text = ''

class MyApp(wx.App):
    def __init__(self):
        super().__init__(clearSigInt = True)
        self.InitFrame()

    def InitFrame(self):
        frame = MyFrame(parent = None, title = 'window',pos = (100,100))
        frame.Show()

class MyFrame(wx.Frame):
    def __init__(self,parent,title, pos = (100,100)):
        super().__init__(parent = parent,title = title, pos = pos)
        self.OnInit()

    def OnInit(self):
        panel = MyPanel(parent = self)

class MyPanel(wx.Panel):
    def __init__(self,parent):
        super().__init__(parent = parent)
        welcome_Text = wx.StaticText(self, id = wx.ID_ANY, label='Hello And Welcome To GGT', pos=(130, 20))

        self._dont_show = False
        T1 = wx.StaticText(self, id = wx.ID_ANY, label = 'Name:',pos = (130,60))
        self._textbox_1 = wx.TextCtrl(parent = self,pos = (170,56))
        T2 = wx.StaticText(self, id=wx.ID_ANY, label='Password:', pos=(130, 90))
        self._textbox_2 = wx.TextCtrl(parent=self, pos=(190, 84),style=wx.TE_PASSWORD|wx.TE_PROCESS_ENTER)

        def Log_in(event):
            global username, password,text
            if self._textbox_1.GetValue() != username or self._textbox_2.GetValue() != password:
                self.T3 = wx.StaticText(self, id=wx.ID_ANY, label='Sorry, incorrect name or password', pos=(130, 170))
            else:
                quit(1)

        self._button = wx.Button(parent = self,label = 'Submit',pos = (160,130))
        self._button.Bind(wx.EVT_BUTTON,Log_in)

if __name__ == "__main__":
    app = MyApp()
    app.MainLoop()
