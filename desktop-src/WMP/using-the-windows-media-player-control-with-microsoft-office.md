---
title: Verwenden des Windows Media Player-Steuer Elements mit Microsoft Office
description: Verwenden des Windows Media Player-Steuer Elements mit Microsoft Office
ms.assetid: bc7b2623-8e6d-4af6-b4d0-8087c0159273
keywords:
- Windows Media Player, Einbetten des ActiveX-Steuer Elements
- Windows Media Player Objektmodell, Einbetten des ActiveX-Steuer Elements
- Objektmodell, Einbetten des ActiveX-Steuer Elements
- Windows Media Player Mobile, Einbetten des ActiveX-Steuer Elements
- Windows Media Player ActiveX-Steuerelement, einbetten
- Windows Media Player Mobile ActiveX-Steuerelement, einbetten
- ActiveX-Steuerelement, einbetten
- Windows Media Player, Office
- Windows Media Player-Objektmodell, Office
- Objektmodell, Office
- Windows Media Player Mobile, Office
- Windows Media Player ActiveX-Steuerelement, Office
- Windows Media Player Mobile ActiveX-Steuerelement, Office
- ActiveX-Steuerelement, Office
- Office-Dokument Einbettung
- einbetten, Office-Dokumente
- Windows Media Player ActiveX-Steuerelement, Excel
- Windows Media Player Mobile ActiveX-Steuerelement, Excel
- ActiveX-Steuerelement, Excel
- einbetten, Excel-Kalkulations Tabellen
- Einbettung von Excel-Tabellen
- Windows Media Player ActiveX-Steuerelement, PowerPoint
- Windows Media Player Mobile ActiveX-Steuerelement, PowerPoint
- ActiveX-Steuerelement, PowerPoint
- einbetten, PowerPoint-Folien anzeigen
- PowerPoint-Folien Anzeige Einbettung
- Windows Media Player ActiveX-Steuerelement, Word
- Windows Media Player Mobile ActiveX-Steuerelement, Word
- ActiveX-Steuerelement, Word
- Wort Papier Einbettung
- einbetten, Word-Dokumente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2504b46b4fb409dede108c41b43014c3aaeae5ec
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947776"
---
# <a name="using-the-windows-media-player-control-with-microsoft-office"></a>Verwenden des Windows Media Player-Steuer Elements mit Microsoft Office

In diesem Abschnitt wird beschrieben, wie Sie das ActiveX-Steuerelement Windows Media Player 9 oder höher in verschiedene Dokumente einbetten, die mit Microsoft Office XP erstellt wurden.

In den® von Microsoft Word, Excel und PowerPoint Betten Sie das Steuerelement ein, indem Sie im Menü **Einfügen** die Option **Objekt** auswählen und dann **Windows Media Player** aus der Liste der verfügbaren Objekttypen auswählen. Das Windows Media Player-Steuerelement wird im Dokument am aktuellen Speicherort angezeigt. Anschließend können Sie im Kontextmenü des-Steuer Elements **Format Control** ( **Format Objekt** in Excel) auswählen, um Layout, Text Wrapping Stil und andere Format Optionen anzupassen. In Word und Excel müssen Sie zu diesem Zweck den Entwurfs Modus verwenden.

Nachdem Sie das Steuerelement positioniert und formatiert haben, können Sie es mithilfe des Dialog Felds **Eigenschaften** konfigurieren, das über die **Steuer** Element-Toolbox oder über das Kontextmenü im Entwurfs Modus für Word und Excel zugänglich ist. Hier können Sie grundlegende Player-Steuerelement Eigenschaften angeben, z. b. den Namen des Steuer Elements, die URL einer digitalen Mediendatei und den Benutzeroberflächen Modus. Wenn die **uiMode** -Eigenschaft auf "None" festgelegt wird, werden alle Elemente im Steuerelement mit Ausnahme des Videos oder Visualisierungs Fensters ausgeblendet, sodass Sie eigene Schaltflächen hinzufügen und Skriptcode mithilfe Visual Basic for Applications (VBA) schreiben können, um die Schaltflächen Klicks und Player-Steuerelement Ereignisse zu verarbeiten

Im Dialogfeld "grundlegende **Eigenschaften** " können Sie auch auf das Dialogfeld "anspruchsvollere **Eigenschaften von Windows Media Player-Steuer** Element" zugreifen, indem Sie auf die Zeile "(Benutzer definiert)" doppelklicken oder nach dem Auswählen der Zeile auf die Schaltfläche mit den Auslassungs Punkten ("...") klicken In diesem Dialogfeld können Sie alle verfügbaren Player-Steuerelement Eigenschaften ändern.

> [!Note]  
> Sie müssen darauf achten, keine Aktionen in Ereignis Handlern für Player-Steuerelemente auszuführen, die dazu führen, dass das Steuerelement zerstört wird. Wenn Sie z. b. das Windows Media Player-Steuerelement auf einer Folie in einer PowerPoint-Präsentation einbetten, sollten Sie die PowerPoint-Methode " **Next** " nicht aus dem **OpenStateChange** -Ereignis des Players oder einem anderen Ereignis abrufen

 

> [!Note]  
> Außerdem sollten Sie die Eigenschaft " **Player. URL** " nicht von einem Ereignishandler für Player-Steuerelemente festlegen.

 

Fügen Sie in FrontPage der Webseite das Windows Media Player-Steuerelement hinzu, indem Sie im Menü **Einfügen** die Option **Webkomponente** auswählen. Wählen Sie im Dialogfeld **Webkomponente einfügen** in der Liste **Komponententyp** die Option **Erweiterte Steuerelemente** aus, und wählen Sie dann in der Liste der Steuerelement Optionen **ActiveX-Steuer** Element aus. Wählen Sie im nächsten Fenster des Dialog Felds die Option **Windows Media Player** aus. Wenn Sie nicht aufgeführt ist, klicken Sie auf **Anpassen** , und aktivieren Sie das Kontrollkästchen **Windows Media Player** in der **Steuer** Elementliste.

Nachdem das Windows Media Player-Steuerelement eingebettet ist, können Sie es positionieren und seine Größe ändern und seine Eigenschaften ändern, indem Sie im Kontextmenü für das Steuerelement **ActiveX-Steuerelement Eigenschaften** auswählen. In der HTML-Ansicht werden die von Ihnen angegebenen Eigenschaftswerte im Object-Element angezeigt, das das Windows Media Player-Steuerelement darstellt. Der Objektname wird als ID-Attribut angezeigt, und die Steuerelement Eigenschaften werden als param-Tags angezeigt. Der Objektname ermöglicht Ihnen den Zugriff auf das Windows-Media Player Steuerelement-Objektmodell, das Sie mit Microsoft JScript programmieren können. Weitere Informationen finden Sie unter [Verwenden des Windows Media Player-Steuer Elements in einer Webseite](using-the-windows-media-player-control-in-a-web-page.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Player-Steuerelement Handbuch**](player-control-guide.md)
</dt> </dl>

 

 




