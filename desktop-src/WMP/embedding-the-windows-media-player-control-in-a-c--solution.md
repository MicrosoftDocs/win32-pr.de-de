---
title: Einbetten des Windows Media Player-Steuerelements in eine C-Projektmappe
description: Einbetten des Windows Media Player-Steuerelements in eine C\-Projektmappe
ms.assetid: 0889cfd8-ed1f-4d0c-aff8-bff2f55ffccb
keywords:
- Windows Media Player,einbetten ActiveX Steuerelement
- Windows Media Player Objektmodell, Einbetten ActiveX Steuerelements
- Objektmodell,Einbetten ActiveX Steuerelement
- Windows Media Player Mobil,einbetten ActiveX Steuerelement
- Windows Media Player ActiveX,Einbetten
- Windows Media Player Mobile ActiveX-Steuerelement,Einbetten
- ActiveX,Einbetten
- Windows Media Player,C
- Windows Media Player Objektmodell,C
- Objektmodell, C
- Windows Media Player Mobil,C
- Windows Media Player ActiveX,C
- Windows Media Player Mobile ActiveX-Steuerelement,C
- ActiveX,C
- Einbetten, C-Programme
- Einbetten von C-Programmen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a067a407fccdd78d71d9e60bc00d1eae6950e3fdaf204f886c5e96edf372eb07
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119901980"
---
# <a name="embedding-the-windows-media-player-control-in-a-c-solution"></a>Einbetten des Windows Media Player-Steuerelements in eine C#-Projektmappe

Um die Funktionalität von Windows Media Player in einer C#-Anwendung zu verwenden, fügen Sie zunächst die Komponente einem Formular hinzu, wie unter Verwenden des Windows Media Player-Steuerelements [mit Microsoft Visual Studio](using-the-windows-media-player-control-with-microsoft-visual-studio.md)

In den folgenden Abschnitten wird beschrieben, wie Sie eine Anwendung erstellen, die Video abspielt und benutzerdefinierte Wiedergabe- und Stoppschaltflächen verwendet.

## <a name="add-the-video-window"></a>Hinzufügen des Videofensters

Fügen Sie das Windows Media Player ActiveX einem Formular hinzu. Ändern Sie die Größe des Steuerelements, und platzieren Sie es an der Stelle, an der das Videofenster angezeigt werden soll.

Wählen Sie das Windows Media Player aus, und ändern Sie dann die **uiMode-Eigenschaft** in "none". Diese Einstellung blendet die Ui-Steuerelemente aus. Wenn der Benutzer ein Video abspielt, wird es im Fenster angezeigt. Für nur audiobasierte Inhalte wird eine Visualisierung angezeigt.

## <a name="add-two-buttons-and-adjust-the-form"></a>Hinzufügen von zwei Schaltflächen und Anpassen des Formulars

Fügen Sie dem Formular nun zwei Schaltflächen hinzu. Wählen Sie die erste Schaltfläche aus, und ändern Sie die **Text-Eigenschaft** in "Play". Wählen Sie die zweite Schaltfläche aus, und ändern Sie die **Text-Eigenschaft** in "Stop".

## <a name="add-the-play-code"></a>Hinzufügen des Wiedergabecodes

Doppelklicken Sie auf die **Schaltfläche Wiedergabe,** um das Codefenster anzuzeigen. In C# wird der folgende Code angezeigt:


```CSharp
private void button1_Click(object sender, System.EventArgs e)
{

}

```



Fügen Sie diese Zeile zwischen den beiden geschweiften Klammern hinzu:


```CSharp
axWindowsMediaPlayer1.URL = @"c:\mediafile.wmv";

```



Im obigen Codebeispiel ist "axWindowsMediaPlayer1" der Standardname des Windows Media Player-Steuerelements, und "c: mediafile.wmv" ist ein Platzhalter für den Namen des Medienelements, das Sie wieder geben \\ möchten. Es kann ein beliebiger gültiger Dateipfad verwendet werden. Das @-Symbol weist den Compiler an, schräge Schrägstriche nicht als Escapezeichen zu interpretieren.

Wenn Sie die digitalen Medieninhalte aus dem Windows Media Player SDK der Bibliothek in Windows Media Player hinzugefügt haben, können Sie stattdessen den folgenden Code verwenden:


```CSharp
axWindowsMediaPlayer1.currentPlaylist = axWindowsMediaPlayer1.mediaCollection.getByName("mediafile");

```



Da die **autoStart-Eigenschaft** standardmäßig true ist, Windows Media Player die Wiedergabe gestartet, wenn Sie die **currentPlaylist-** oder **URL-Eigenschaft** festlegen.

## <a name="add-the-stop-code"></a>Hinzufügen des Stoppcodes

Doppelklicken Sie auf die **Schaltfläche Beenden,** um das Fenster Code anzuzeigen. In C# wird der folgende Code angezeigt:


```CSharp
private void button2_Click(object sender, System.EventArgs e)
{

}

```



Fügen Sie diese Zeile zwischen den beiden geschweiften Klammern hinzu:


```CSharp
axWindowsMediaPlayer1.Ctlcontrols.stop();

```



> [!Note]  
> Der Wrapper für verwalteten Code für das Windows Media Player-Steuerelement macht das **Controls-Objekt** als **Ctlcontrols** verfügbar, um einen Zusammenstoß mit der von System.Windows geerbten **Controls-Eigenschaft** **zu vermeiden. Forms.Control**.

 

## <a name="add-error-handling"></a>Hinzufügen der Fehlerbehandlung

Das Windows Media Player-Steuerelement gibt keine Ausnahme aus, wenn ein Fehler auftritt, z. B. eine ungültige URL. Stattdessen signalisiert sie ein Ereignis. Ihre Anwendung sollte vom Player gesendete Fehlerereignisse verarbeiten.

Um einen Ereignishandler zu erstellen, öffnen Sie zuerst die Eigenschaftenfenster für das Windows Media Player Steuerelement. Doppelklicken Sie in der Liste der Ereignisse auf **MediaError.** Der folgende Code wird angezeigt:


```CSharp
private void Player_MediaError(object sender, _WMPOCXEvents_MediaErrorEvent e)
{
}

```



Der folgende Code könnte in die -Methode eingefügt werden, um eine minimale Fehlerbehandlungsfunktion zu bieten. Beachten Sie, dass Informationen zum Fehler aus dem **\_ WMPOCXEvents \_ MediaErrorEvent-Argument abgerufen werden** können.


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

[**Einbetten des Windows Media Player-Steuerelements in eine .NET Framework Projektmappe**](using-the-windows-media-player-control-in-a--net-framework-solution.md)
</dt> </dl>

 

 




