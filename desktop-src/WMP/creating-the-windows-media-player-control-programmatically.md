---
title: Programm gesteuertes Erstellen des Windows Media Player-Steuer Elements
description: Programm gesteuertes Erstellen des Windows Media Player-Steuer Elements
ms.assetid: 9a4856ce-6a44-47fb-b863-59ce4deb0597
keywords:
- Windows Media Player, Programm gesteuertes Erstellen eines ActiveX-Steuer Elements
- Windows Media Player-Objektmodell, Programm gesteuertes Erstellen eines ActiveX-Steuer Elements
- Objektmodell, Programm gesteuertes Erstellen eines ActiveX-Steuer Elements
- Windows Media Player Mobile, Programm gesteuertes Erstellen eines ActiveX-Steuer Elements
- Windows Media Player ActiveX-Steuerelement, Programm gesteuertes erstellen
- Windows Media Player Mobile ActiveX-Steuerelement, erstellen Programm gesteuert
- ActiveX-Steuerelement, Programm gesteuertes erstellen
- programmgesteuerte Erstellung des ActiveX-Steuer Elements
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 222c207b33dcc13a5392f79dad267d6ee82a677c
ms.sourcegitcommit: e22adfb0dd3bb989e59455baedb4d905a877a240
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/21/2019
ms.locfileid: "104311682"
---
# <a name="creating-the-windows-media-player-control-programmatically"></a>Programm gesteuertes Erstellen des Windows Media Player-Steuer Elements

Wenn Sie das Windows Media Player-Steuerelement einem Formular aus der Toolbox hinzufügen, wird ein Objekt der Klasse " **AxWMPLib. AxWindowsMediaPlayer** " erstellt. Diese Wrapper Klasse gibt dem Player die gesamte Funktionalität eines ActiveX-Steuer Elements, einschließlich des Zugriffs auf Benutzeroberflächen Eigenschaften, z. b. **Speicherort** und **Größe**.

Wenn Sie die von **AxWindowsMediaPlayer** verfügbar gemachten Eigenschaften nicht benötigen oder wenn die Anwendung nicht über eine grafische Benutzeroberfläche verfügt, können Sie ein Player-Steuerelement Programm gesteuert erstellen. In diesem Fall erstellen Sie ein Objekt der **WMPLib. windowsmediaplayer** -Klasse.

> [!Note]  
> Da das **windowsmediaplayer** -Objekt nicht als ActiveX-Steuerelement umschließt ist, verfügt es nicht über Eigenschaften, die von **System. Windows. Forms. Control** geerbt werden. Folglich wird die Steuerelement **Eigenschaft nicht** in **ctlcontrols** umbenannt, wie Sie in **AxWindowsMediaPlayer** der Fall ist.

 

Um das Windows Media Player-Steuerelement Programm gesteuert zu erstellen, müssen Sie zunächst einen Verweis auf wmp.dll hinzufügen, der im \\ Ordner Windows System32 zu finden ist \\ . Wenn Sie diesen Verweis hinzufügen, wird WMPLib.dll im Projektordner erstellt, und in Projektmappen-Explorer wird ein Verweis auf WMPLib angezeigt.

Der folgende Beispielcode, Teil einer Form1-Klasse, zeigt, wie ein **Player** -Objekt erstellt und eine Datei wiedergegeben wird. Wenn die Wiedergabe beendet wird, oder wenn die Datei nicht wiedergegeben werden kann, wird das Formular geschlossen.


```VB
Dim WithEvents Player As WMPLib.WindowsMediaPlayer

Private Sub PlayFile(ByVal url As String)
    Player = New WMPLib.WindowsMediaPlayer
    Player.URL = url
    Player.controls.play()
End Sub

Private Sub Form1_Load(ByVal sender As Object, ByVal e As System.EventArgs) _
                       Handles MyBase.Load
    ' TODO  Insert a valid path in the line below.
    PlayFile("c:\media\myaudio.wma")
End Sub

Private Sub Player_MediaError(ByVal pMediaObject As Object) _
                              Handles Player.MediaError
    MessageBox.Show("Cannot play media file.")
    Me.Close()
End Sub

Private Sub Player_PlayStateChange(ByVal NewState As Integer) _
                                   Handles Player.PlayStateChange
    If NewState = WMPLib.WMPPlayState.wmppsStopped Then
        Me.Close()
    End If
End Sub

```




```CSharp
WMPLib.WindowsMediaPlayer Player;

private void PlayFile(String url)
{
    Player = new WMPLib.WindowsMediaPlayer();
    Player.PlayStateChange += 
        new WMPLib._WMPOCXEvents_PlayStateChangeEventHandler(Player_PlayStateChange);
    Player.MediaError += 
        new WMPLib._WMPOCXEvents_MediaErrorEventHandler(Player_MediaError);
    Player.URL = url;
    Player.controls.play();
}

private void Form1_Load(object sender, System.EventArgs e)
{
    // TODO  Insert a valid path in the line below.
    PlayFile(@"c:\myaudio.wma");
}

private void Player_PlayStateChange(int NewState)
{
    if ((WMPLib.WMPPlayState)NewState == WMPLib.WMPPlayState.wmppsStopped)
    {
        this.Close();
    }
}

private void Player_MediaError(object pMediaObject)
{
    MessageBox.Show("Cannot play media file.");
    this.Close();
}


```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Einbetten des Windows Media Player-Steuer Elements in eine .NET Framework Lösung**](using-the-windows-media-player-control-in-a--net-framework-solution.md)
</dt> </dl>

 

 




