---
title: Programmgesteuertes Erstellen des Windows Media Player-Steuerelements
description: Programmgesteuertes Erstellen des Windows Media Player-Steuerelements
ms.assetid: 9a4856ce-6a44-47fb-b863-59ce4deb0597
keywords:
- Windows Media Player,programmgesteuertes Erstellen ActiveX Steuerelements
- Windows Media Player Objektmodell, programmgesteuertes Erstellen ActiveX Steuerelements
- Objektmodell, programmgesteuertes Erstellen ActiveX Steuerelements
- Windows Media Player Mobil, programmgesteuertes Erstellen ActiveX-Steuerelements
- Windows Media Player ActiveX-Steuerelement,programmgesteuertes Erstellen
- Windows Media Player Mobile ActiveX-Steuerelement, programmgesteuert erstellen
- ActiveX Steuerelement, programmgesteuertes Erstellen
- Programmgesteuertes Erstellen ActiveX Steuerelements
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f57b3f4ba9d8c297aee9feb14fc05a35306e1a85d8a718aef6721b92475e19c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118340963"
---
# <a name="creating-the-windows-media-player-control-programmatically"></a>Programmgesteuertes Erstellen des Windows Media Player-Steuerelements

Wenn Sie einem Formular aus der Toolbox das Windows Media Player-Steuerelement hinzufügen, wird ein Objekt der **AxWMPLib.AxWindowsMediaPlayer-Klasse** erstellt. Diese Wrapperklasse bietet dem Player alle Funktionen eines ActiveX-Steuerelements, einschließlich des Zugriffs auf Benutzeroberflächeneigenschaften wie **Standort** und **Größe.**

Wenn Sie die von **AxWindowsMediaPlayer** verfügbar gemachten Eigenschaften nicht benötigen oder ihre Anwendung keine grafische Benutzeroberfläche hat, können Sie programmgesteuert ein Player-Steuerelement erstellen. In diesem Fall erstellen Sie ein Objekt der **WMPLib.WindowsMediaPlayer-Klasse.**

> [!Note]  
> Da das **WindowsMediaPlayer-Objekt** nicht als ActiveX-Steuerelement umschlossen ist, verfügt es nicht über Eigenschaften, die von System.Windows geerbt **wurden. Forms.Control**. Daher wird die **Controls-Eigenschaft** nicht wie in **AxWindowsMediaPlayer** in **CtlControls** umbenannt.

 

Um das Windows Media Player-Steuerelement programmgesteuert zu erstellen, müssen Sie zunächst einen Verweis auf wmp.dll hinzufügen, der sich im \\ Ordner Windows \\ system32 befindet. Durch Hinzufügen dieses Verweises wird WMPLib.dll in Ihrem Projektordner erstellt, und ein Verweis auf WMPLib wird in Projektmappen-Explorer angezeigt.

Der folgende Beispielcode, der Teil einer Form1-Klasse ist, zeigt, wie Sie ein **Player-Objekt** erstellen und eine Datei wiedergeben. Wenn die Wiedergabe endet oder die Datei nicht wiedergegeben werden kann, wird das Formular geschlossen.


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

[**Einbetten des Windows Media Player-Steuerelements in eine .NET Framework-Projektmappe**](using-the-windows-media-player-control-in-a--net-framework-solution.md)
</dt> </dl>

 

 




