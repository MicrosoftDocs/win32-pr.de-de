---
title: Einbetten des Windows Media Player-Steuer Elements in eine C-Lösung
description: Einbetten des Windows Media Player-Steuer Elements in eine C \-Lösung
ms.assetid: 0889cfd8-ed1f-4d0c-aff8-bff2f55ffccb
keywords:
- Windows Media Player, Einbetten des ActiveX-Steuer Elements
- Windows Media Player Objektmodell, Einbetten des ActiveX-Steuer Elements
- Objektmodell, Einbetten des ActiveX-Steuer Elements
- Windows Media Player Mobile, Einbetten des ActiveX-Steuer Elements
- Windows Media Player ActiveX-Steuerelement, einbetten
- Windows Media Player Mobile ActiveX-Steuerelement, einbetten
- ActiveX-Steuerelement, einbetten
- Windows Media Player, C
- Windows Media Player-Objektmodell, C
- Objektmodell, C
- Windows Media Player Mobile, C
- Windows Media Player ActiveX-Steuerelement, C
- Windows Media Player Mobile ActiveX-Steuerelement, C
- ActiveX-Steuerelement, C
- einbetten, C-Programme
- C-Programm Einbettung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c950bed9812cea0aa6ce28995fd6998bb8417ac
ms.sourcegitcommit: e22adfb0dd3bb989e59455baedb4d905a877a240
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/21/2019
ms.locfileid: "106337190"
---
# <a name="embedding-the-windows-media-player-control-in-a-c-solution"></a>Einbetten des Windows Media Player-Steuer Elements in eine c#-Lösung

Um die Funktionalität von Windows Media Player in einer c#-Anwendung zu verwenden, fügen Sie die Komponente zunächst einem Formular hinzu, wie unter [Verwenden des Windows Media Player-Steuer Elements mit Microsoft Visual Studio](using-the-windows-media-player-control-with-microsoft-visual-studio.md)

In den folgenden Abschnitten wird beschrieben, wie Sie eine Anwendung erstellen, die Video abgespielt und benutzerdefinierte Wiedergabe-und Schaltflächen verwendet.

## <a name="add-the-video-window"></a>Hinzufügen des Video Fensters

Fügen Sie das Windows Media Player ActiveX-Steuerelement zu einem Formular hinzu. Ändern Sie die Größe des Steuer Elements, und platzieren Sie es an der Stelle, an der das Videofenster angezeigt werden soll.

Wählen Sie das Windows Media Player-Steuerelement aus, und ändern Sie dann die **uiMode** -Eigenschaft in "None". Diese Einstellung blendet die UI-Steuerelemente aus. Wenn der Benutzer ein Video wieder gibt, wird es im Fenster angezeigt. Bei reinen Audioinhalten wird eine Visualisierung angezeigt.

## <a name="add-two-buttons-and-adjust-the-form"></a>Zwei Schaltflächen hinzufügen und das Formular anpassen

Fügen Sie dem Formular nun zwei Schaltflächen hinzu. Wählen Sie die erste Schaltfläche aus, und ändern Sie die **Text** -Eigenschaft in "Play". Wählen Sie die zweite Schaltfläche aus, und ändern Sie die **Text** -Eigenschaft in "Ende".

## <a name="add-the-play-code"></a>Hinzufügen des Wiedergabe Codes

Doppelklicken Sie auf die **Wiedergabe** Schaltfläche, um das Code Fenster anzuzeigen. In c# wird folgender Code angezeigt:


```CSharp
private void button1_Click(object sender, System.EventArgs e)
{

}

```



Fügen Sie diese Zeile zwischen den beiden geschweiften Klammern ein:


```CSharp
axWindowsMediaPlayer1.URL = @"c:\mediafile.wmv";

```



Im vorangehenden Codebeispiel ist "axWindowsMediaPlayer1" der Standardname des Windows Media Player-Steuer Elements, und "c: \\ mediafile. wmv" ist ein Platzhalter für den Namen des Medien Elements, das Sie wiedergeben möchten. Es kann ein beliebiger gültiger Dateipfad verwendet werden. Das @-Symbol weist den Compiler an, keine umgekehrten Schrägstriche als Escapezeichen zu interpretieren.

Wenn Sie den Inhalt digitaler Medien aus dem Windows Media Player SDK der Bibliothek in Windows Media Player hinzugefügt haben, können Sie stattdessen den folgenden Code verwenden:


```CSharp
axWindowsMediaPlayer1.currentPlaylist = axWindowsMediaPlayer1.mediaCollection.getByName("mediafile");

```



Da die **Autostart** -Eigenschaft standardmäßig auf true festgelegt ist, wird die Wiedergabe von Windows Media Player gestartet, wenn Sie die Eigenschaft **currentwiedergabe** oder **URL** festlegen.

## <a name="add-the-stop-code"></a>Hinzufügen des endcodes

Doppelklicken Sie auf die Schaltfläche " **Abbrechen** ", um das Code Fenster anzuzeigen. In c# wird folgender Code angezeigt:


```CSharp
private void button2_Click(object sender, System.EventArgs e)
{

}

```



Fügen Sie diese Zeile zwischen den beiden geschweiften Klammern ein:


```CSharp
axWindowsMediaPlayer1.Ctlcontrols.stop();

```



> [!Note]  
> Der Wrapper für verwalteten Code für das Windows Media Player-Steuerelement macht das Steuer **Element Objekt als** **ctlcontrols** verfügbar, um einen Konflikt **mit der** Steuerelement Eigenschaft zu vermeiden, die von **System. Windows. Forms. Control** geerbt wird.

 

## <a name="add-error-handling"></a>Fehlerbehandlung hinzufügen

Das Windows Media Player-Steuerelement gibt keine Ausnahme aus, wenn ein Fehler auftritt, z. b. eine ungültige URL. Stattdessen wird ein Ereignis signalisiert. Die Anwendung sollte vom Player gesendete Fehlerereignisse verarbeiten.

Um einen Ereignishandler zu erstellen, öffnen Sie zunächst die Eigenschaftenfenster für das Windows Media Player-Steuerelement. Doppelklicken Sie in der Liste der Ereignisse auf **MediaError**. Der folgende Code wird angezeigt:


```CSharp
private void Player_MediaError(object sender, _WMPOCXEvents_MediaErrorEvent e)
{
}

```



Der folgende Code kann in die-Methode eingefügt werden, um eine minimale Fehler Behandlungs Funktion bereitzustellen. Beachten Sie, dass Informationen über den Fehler vom **\_ wmpocxevents \_ mediaerrorevent** -Argument abgerufen werden können.


```CSharp
try
// If the Player encounters a corrupt or missing file, 
// show the hexadecimal error code and URL.
{
    IWMPMedia2 errSource = e.pMediaObject as IWMPMedia2;
    IWMPErrorItem errorItem = errSource.Error;
    MessageBox.Show("Error " + errorItem.errorCode.ToString("X") 
                    + " in " + errSource.sourceURL);
}
catch(InvalidCastException)
// In case pMediaObject is not an IWMPMedia item.
{
    MessageBox.Show("Error.");
} 

```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Einbetten des Windows Media Player-Steuer Elements in eine .NET Framework Lösung**](using-the-windows-media-player-control-in-a--net-framework-solution.md)
</dt> </dl>

 

 




