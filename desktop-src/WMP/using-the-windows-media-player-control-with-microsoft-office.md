---
title: Verwenden des Windows Media Player-Steuerelements mit Microsoft Office
description: Verwenden des Windows Media Player-Steuerelements mit Microsoft Office
ms.assetid: bc7b2623-8e6d-4af6-b4d0-8087c0159273
keywords:
- Windows Media Player,einbetten ActiveX Steuerelement
- Windows Media Player Objektmodell, Einbetten ActiveX Steuerelements
- Objektmodell,Einbetten ActiveX Steuerelement
- Windows Media Player Mobil,einbetten ActiveX Steuerelement
- Windows Media Player ActiveX,Einbetten
- Windows Media Player Mobile ActiveX-Steuerelement,Einbetten
- ActiveX,Einbetten
- Windows Media Player,Office
- Windows Media Player-Objektmodell,Office
- Objektmodell,Office
- Windows Media Player Mobil,Office
- Windows Media Player ActiveX,Office
- Windows Media Player Mobile ActiveX-Steuerelement,Office
- ActiveX,Office
- Office des Einbettens von Dokumenten
- Einbetten, Office Dokumente
- Windows Media Player ActiveX,Excel
- Windows Media Player Mobile ActiveX-Steuerelement,Excel
- ActiveX,Excel
- Einbetten, Excel Tabellenkalkulationen
- Excel einbetten von Tabellenkalkulationen
- Windows Media Player ActiveX,PowerPoint
- Windows Media Player Mobile ActiveX-Steuerelement,PowerPoint
- ActiveX,PowerPoint
- Embedding,PowerPoint slide shows
- PowerPoint einbetten
- Windows Media Player ActiveX,Word
- Windows Media Player Mobile ActiveX-Steuerelement, Word
- ActiveX,Word
- Einbetten von Word-Dokumenten
- Einbetten, Word-Dokumente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 418c082cad2793e3ebd676c4d648339f9e637f46c7519efc1b426a44b69ee05c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120001400"
---
# <a name="using-the-windows-media-player-control-with-microsoft-office"></a>Verwenden des Windows Media Player-Steuerelements mit Microsoft Office

In diesem Abschnitt wird beschrieben, wie Sie das Windows Media Player 9-Serie-Steuerelement oder höher in ActiveX Dokumente einbetten, die mithilfe von Microsoft Office XP erstellt wurden.

In Microsoft Word, Excel und PowerPoint® betten Sie das Steuerelement ein, indem Sie im  Menü Einfügen die Option  Objekt und dann Windows Media Player in der Liste der verfügbaren Objekttypen auswählen.  Das Windows Media Player-Steuerelement wird im Dokument an der aktuellen Position angezeigt. Sie können dann im Kontextmenü des Steuerelements die Option Formatsteuerelement **(Objekt** **in** Excel formatieren) auswählen, um das Layout, den Textumbruchstil und andere Formatoptionen anzupassen. In Word und Excel müssen Sie sich dazu im Entwurfsmodus befinden.

Nachdem Sie das Steuerelement positioniert und formatiert haben,  können Sie es mithilfe des Dialogfelds Eigenschaften konfigurieren, auf das über die **Steuerelement-Toolbox** oder über das Kontextmenü im Entwurfsmodus für Word und Excel. Hier können Sie grundlegende Player-Steuerelementeigenschaften angeben, z. B. den Steuerelementnamen, die URL einer digitalen Mediendatei und den Benutzeroberflächenmodus. Wenn Sie die **uiMode-Eigenschaft** auf "none" festlegen, wird alles im Steuerelement außer dem Video- oder Visualisierungsfenster ausblendet, sodass Sie eigene Schaltflächen hinzufügen und Skriptcode mithilfe von Visual Basic for Applications (VBA) schreiben können, um die Klicks auf die Schaltflächen und Player-Steuerelementereignisse zu verarbeiten.

Im Dialogfeld  Grundlegende Eigenschaften können Sie auch auf das anspruchsvollere Dialogfeld **Windows Media Player-Steuerelementeigenschaften** zugreifen, indem Sie auf die Zeile "(Benutzerdefiniert)" doppelklicken oder auf die Schaltfläche mit den Auslassungstasten ("...") klicken, nachdem Sie diese Zeile ausgewählt haben. In diesem Dialogfeld können Sie alle verfügbaren Eigenschaften des Player-Steuerelements ändern.

> [!Note]  
> Sie müssen darauf achten, keine Aktionen in Ereignishandlern des Player-Steuerelements durchzuführen, die dazu führen, dass das Steuerelement zerstört wird. Wenn Sie z. B. das Windows Media Player-Steuerelement auf einer Folie in eine PowerPoint-Präsentation einbetten, rufen Sie die PowerPoint **Next-Methode** nicht aus dem Player **openStateChange-Ereignis** oder einem anderen Ereignis auf.

 

> [!Note]  
> Darüber hinaus sollten Sie die **Player.URL-Eigenschaft** nicht aus einem Ereignishandler des Player-Steuerelements festlegen.

 

Fügen Sie in FrontPage das Windows Media Player einer Webseite hinzu, indem Sie im Menü **Einfügen** die Option **Webkomponente** auswählen. Wählen Sie im **Dialogfeld Webkomponente** einfügen  in der Liste Komponententyp die Option Erweiterte Steuerelemente und dann ActiveX Steuerelement **aus** der Liste der Steuerelementoptionen aus.  Wählen Sie im nächsten Fenster des Dialogfelds die Option **Windows Media Player.** Wenn sie nicht aufgeführt ist, klicken Sie auf **Anpassen,** und aktivieren Sie **Windows Media Player** Kontrollkästchen in der **Liste Steuerelement.**

Nachdem das Windows Media Player-Steuerelement eingebettet wurde, können Sie es positionieren und seine  Größe ändern und seine Eigenschaften ändern, indem Sie ActiveX Steuerelementeigenschaften im Kontextmenü für das Steuerelement auswählen. In der HTML-Ansicht werden die von Ihnen angegebenen Eigenschaftswerte im OBJECT-Element angezeigt, das das Windows Media Player darstellt. Der Objektname wird als ID-Attribut angezeigt, und die Steuerelementeigenschaften werden als PARAM-Tags angezeigt. Mit dem Objektnamen erhalten Sie Zugriff auf das Windows Media Player-Steuerelementobjektmodell, das Sie mit microsoft JScript. Weitere Informationen finden Sie unter [Verwenden des Windows Media Player-Steuerelements in einer Webseite.](using-the-windows-media-player-control-in-a-web-page.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Leitfaden zum Player-Steuerelement**](player-control-guide.md)
</dt> </dl>

 

 




