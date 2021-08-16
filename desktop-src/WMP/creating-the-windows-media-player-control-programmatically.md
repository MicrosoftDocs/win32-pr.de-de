---
title: Programmgesteuertes Erstellen Windows Media Player-Steuerelements
description: Programmgesteuertes Erstellen Windows Media Player-Steuerelements
ms.assetid: 9a4856ce-6a44-47fb-b863-59ce4deb0597
keywords:
- Windows Media Player,Programmgesteuertes Erstellen ActiveX Steuerelements
- Windows Media Player Objektmodell, programmgesteuertes erstellen ActiveX Steuerelement
- Objektmodell, programmgesteuertes Erstellen ActiveX Steuerelements
- Windows Media Player Mobil, programmgesteuertes erstellen ActiveX-Steuerelement
- Windows Media Player ActiveX,programmgesteuert erstellen
- Windows Media Player Mobile ActiveX-Steuerelement,programmgesteuert erstellen
- ActiveX,programmgesteuert erstellen
- Programmgesteuertes ActiveX-Steuerelements
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f57b3f4ba9d8c297aee9feb14fc05a35306e1a85d8a718aef6721b92475e19c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118340963"
---
# <a name="creating-the-windows-media-player-control-programmatically"></a>Programmgesteuertes Erstellen Windows Media Player-Steuerelements

Wenn Sie das Windows Media Player einem Formular aus der Toolbox hinzufügen, wird ein Objekt der Klasse **AxWMPLib.AxWindowsMediaPlayer** erstellt. Diese Wrapperklasse bietet dem Player alle Funktionen eines ActiveX-Steuerelements, einschließlich des Zugriffs auf Benutzeroberflächeneigenschaften wie **Location** und **Size.**

Wenn Sie die von **AxWindowsMediaPlayer** verfügbar gemachten Eigenschaften nicht benötigen oder ihre Anwendung keine grafische Benutzeroberfläche besitzt, können Sie ein Player-Steuerelement programmgesteuert erstellen. In diesem Fall erstellen Sie ein Objekt der **WMPLib.WindowsMediaPlayer-Klasse.**

> [!Note]  
> Da das **WindowsMediaPlayer-Objekt** nicht als ActiveX-Steuerelement umschlossen ist, verfügt es nicht über Eigenschaften, die von **System.Windows. Forms.Control**. Daher wird die **Controls-Eigenschaft** nicht wie in **AxWindowsMediaPlayer** in **CtlControls** umbenannt.

 

Um das Windows Media Player programmgesteuert zu erstellen, müssen Sie zunächst einen Verweis auf wmp.dll hinzufügen, der sich im Ordner Windows \\ \\ system32 befindet. Durch das Hinzufügen dieses Verweises WMPLib.dll projektordner erstellt, und ein Verweis auf WMPLib wird in Projektmappen-Explorer.

Der folgende Beispielcode, der Teil einer Form1-Klasse ist, zeigt, wie sie ein **Player-Objekt** erstellen und eine Datei wieder geben. Wenn die Wiedergabe endet oder die Datei nicht abgespielt werden kann, wird das Formular geschlossen.


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

[**Einbetten des Windows Media Player-Steuerelements in eine .NET Framework Projektmappe**](using-the-windows-media-player-control-in-a--net-framework-solution.md)
</dt> </dl>

 

 




