---
title: Einbetten des Windows Media Player-Steuer Elements in eine Visual Basic .net-Lösung
description: Einbetten des Windows Media Player-Steuer Elements in eine Visual Basic .net-Lösung
ms.assetid: e6428b42-5d8b-48ef-9f7a-c90a4625b745
keywords:
- Windows Media Player, Einbetten des ActiveX-Steuer Elements
- Windows Media Player Objektmodell, Einbetten des ActiveX-Steuer Elements
- Objektmodell, Einbetten des ActiveX-Steuer Elements
- Windows Media Player Mobile, Einbetten des ActiveX-Steuer Elements
- Windows Media Player ActiveX-Steuerelement, einbetten
- Windows Media Player Mobile ActiveX-Steuerelement, einbetten
- ActiveX-Steuerelement, einbetten
- Windows Media Player, Visual Basic .net
- Windows Media Player-Objektmodell, Visual Basic .net
- Objektmodell, Visual Basic .net
- Windows Media Player Mobile, Visual Basic .net
- Windows Media Player ActiveX-Steuerelement, Visual Basic .net
- Windows Media Player Mobile ActiveX-Steuerelement, Visual Basic .net
- ActiveX-Steuerelement, Visual Basic .net
- einbetten, Visual Basic .net-Programme
- Visual Basic .NET-Programm Einbettung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d578b456a5064f1846ead7f074f178753dbc7c97
ms.sourcegitcommit: e22adfb0dd3bb989e59455baedb4d905a877a240
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/21/2019
ms.locfileid: "104311688"
---
# <a name="embedding-the-windows-media-player-control-in-a-visual-basic-net-solution"></a>Einbetten des Windows Media Player-Steuer Elements in eine Visual Basic .net-Lösung

Um die Funktionen von Windows Media Player 9 oder höher in einer Visual Basic .NET-Anwendung zu verwenden, fügen Sie die Komponente zunächst einem Formular hinzu, wie unter [Verwenden des Windows Media Player-Steuer Elements mit beschrieben Microsoft Visual Studio](using-the-windows-media-player-control-with-microsoft-visual-studio.md)

In diesem Abschnitt wird beschrieben, wie Sie eine Anwendung erstellen, die Videos wieder gibt und über benutzerdefinierte Wiedergabe-und Schaltflächen verfügt.

## <a name="add-the-video-window"></a>Hinzufügen des Video Fensters

Fügen Sie das Windows Media Player-Steuerelement einem Formular hinzu. Ändern Sie die Größe des Steuer Elements, und platzieren Sie es an der Stelle, an der das Videofenster angezeigt werden soll.

Wählen Sie das Windows Media Player-Steuerelement aus, und ändern Sie dann die **uiMode** -Eigenschaft in "None". Diese Einstellung blendet die UI-Steuerelemente aus. Wenn der Benutzer ein Video wieder gibt, wird es im Fenster angezeigt. Bei reinen Audioinhalten wird eine Visualisierung angezeigt.

## <a name="add-two-buttons-and-adjust-the-form"></a>Zwei Schaltflächen hinzufügen und das Formular anpassen

Fügen Sie dem Formular nun zwei Schaltflächen hinzu. Wählen Sie die erste Schaltfläche aus, und ändern Sie die **Text** -Eigenschaft in "Play". Wählen Sie die zweite Schaltfläche aus, und ändern Sie die **Text** -Eigenschaft in "Ende".

## <a name="add-the-play-code"></a>Hinzufügen des Wiedergabe Codes

Doppelklicken Sie auf die **Wiedergabe** Schaltfläche, um das Code Fenster anzuzeigen. Der folgende Code wird angezeigt:


```VB
Private Sub Button1_Click(ByVal sender As System.Object, _
        ByVal e As System.EventArgs) Handles Button1.Click

End Sub
```



Fügen Sie die folgende Zeile zur Unterroutine hinzu:


```VB
AxWindowsMediaPlayer1.URL = "c:\mediafile.wmv"
```



Im vorangehenden Codebeispiel ist "axWindowsMediaPlayer1" der Standardname des Windows Media Player-Steuer Elements und "c: \\ mediafile. wmv" ein Platzhalter für den Namen des Mediums, das Sie wiedergeben möchten.

Wenn Sie den Inhalt digitaler Medien aus dem Windows Media Player SDK der Bibliothek in Windows Media Player hinzugefügt haben, können Sie stattdessen den folgenden Code verwenden:


```VB
axWindowsMediaPlayer1.currentPlaylist = _
    axWindowsMediaPlayer1.mediaCollection.getByName("mediafile")

```



Da die **Autostart** -Eigenschaft standardmäßig auf true festgelegt ist, wird die Wiedergabe von Windows Media Player gestartet, wenn Sie die Eigenschaft **currentwiedergabe** oder **URL** festlegen.

## <a name="add-the-stop-code"></a>Hinzufügen des endcodes

Doppelklicken Sie auf die Schaltfläche " **Abbrechen** ", um das Code Fenster anzuzeigen. Der folgende Code wird angezeigt:


```VB
Private Sub Button2_Click(ByVal sender As System.Object, _
        ByVal e As System.EventArgs) Handles Button1.Click

End Sub

```



Fügen Sie die folgende Zeile zur Unterroutine hinzu:


```VB
AxWindowsMediaPlayer1.Ctlcontrols.stop()

```



> [!Note]  
> Der Wrapper für verwalteten Code für das Windows Media Player-Steuerelement macht das Steuer **Element Objekt als** **ctlcontrols** verfügbar, um einen Konflikt **mit der** Steuerelement Eigenschaft zu vermeiden, die von **System. Windows. Forms. Control** geerbt wird.

 

## <a name="add-error-handling"></a>Fehlerbehandlung hinzufügen

Das Windows Media Player-Steuerelement gibt keine Ausnahme aus, wenn ein Fehler auftritt, z. b. eine ungültige URL. Stattdessen signalisiert das Steuerelement ein Ereignis. Die Anwendung sollte vom Player gesendete Fehlerereignisse verarbeiten.

Um einen Ereignishandler zu erstellen, öffnen Sie das Code Fenster für die Formular Klasse. Wählen Sie in der Dropdown Liste am oberen Rand des Fensters das Windows Media Player-Steuerelement aus. In der Dropdown Liste auf der rechten Seite wird eine Liste der Ereignisse angezeigt. Wählen Sie in dieser Liste die Option [**MediaError**](axwmplib-axwindowsmediaplayer-mediaerror.md)aus. Der folgende Code wird angezeigt:


```VB
Private Sub AxWindowsMediaPlayer1_MediaError(ByVal sender As Object, _
    ByVal e As _WMPOCXEvents_MediaErrorEvent) Handles AxWindowsMediaPlayer1.MediaError

End Sub

```



Der folgende Code kann in die Unterroutine eingefügt werden, um eine minimale Fehler Behandlungs Funktion bereitzustellen. Beachten Sie, dass Informationen über den Fehler vom **\_ wmpocxevents \_ mediaerrorevent** -Argument abgerufen werden können.


```VB
Try
    ' If the file is corrupt or missing, show the 
    ' hexadecimal error code and URL.
    Dim errSource As WMPLib.IWMPMedia2 = e.pMediaObject
    Dim errorItem As WMPLib.IWMPErrorItem = errSource.Error
    MessageBox.Show("Media error " + errorItem.errorCode.ToString("X") _
                    + " in " + errSource.sourceURL)
Catch ex As InvalidCastException
    ' In case pMediaObject is not an IWMPMedia item.
    MessageBox.Show("Player error.")
End Try

```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Einbetten des Windows Media Player-Steuer Elements in eine .NET Framework Lösung**](using-the-windows-media-player-control-in-a--net-framework-solution.md)
</dt> </dl>

 

 




