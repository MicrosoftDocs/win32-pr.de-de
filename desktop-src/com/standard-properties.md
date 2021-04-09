---
title: Standardeigenschaften
description: Standardeigenschaften
ms.assetid: 08b7c388-a362-4d71-ac24-93675984881f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78ab30dd644231c5c11a9f1e4d7ccf9c861ae2fa
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "104039643"
---
# <a name="standard-properties"></a>Standardeigenschaften

OLE definiert einen Satz von Standard-DISPIDs für alle drei Arten von Eigenschaften: Steuerelement, Ambient und erweitert. In den folgenden Tabellen sind diese Standards für Steuerelement Eigenschaften, Ambient-Eigenschaften und erweiterte Eigenschaften aufgeführt.



| Control-Eigenschaft                                                                               | type                             | BESCHREIBUNG                                                                                                                                                                                                                              |
|------------------------------------------------------------------------------------------------|----------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| BackColor, ForeColor, FillColor, BorderColor<br/>                                        | **OLE- \_ Farbe**<br/>        | Das Farbschema des Steuer Elements.<br/>                                                                                                                                                                                                    |
| BackStyle, FillStyle, BorderStyle, BorderWidth, bordervisible, DrawStyle, DrawWidth<br/> | **kurz** oder **lang**<br/> | Bits, die das visuelle Verhalten eines Steuer Elements definieren, wie z. b. Solid oder transparent, mit Thick oder Thin Rahmen, Linienstilen usw.<br/>                                                                                    |
| Schriftart<br/>                                                                                | **IDispatch \***<br/>      | Die im Steuerelement verwendete Schriftart, bei der es sich um einen **IDispatch** -Zeiger auf ein Standard schriftobjekt handelt. Weitere Informationen finden Sie unter [Standard Schriftart Objekt](standard-font-object.md) .<br/>                                                         |
| Beschriftung, Text<br/>                                                                       | **BSTR**<br/>              | Zeichen folgen, die die Bezeichnung des Steuer Elements (die Beschriftung) oder Ihren Text Inhalt (den Text) enthalten. Beachten Sie, dass die Beschriftung das Steuerelement nicht unbedingt im Container benennen muss. Siehe die erweiterte Name-Eigenschaft in der folgenden Tabelle.<br/> |
| Aktiviert<br/>                                                                             | **BOOL**<br/>              | Bestimmt, ob das Steuerelement aktiviert oder deaktiviert ist. Wenn diese Option deaktiviert ist, ist das Steuerelement wahrscheinlich ausgegraut.<br/>                                                                                                                           |
| Fenster<br/>                                                                              | **HWND**<br/>              | Das Fenster Handle des Steuer Elements, wenn es über ein Element verfügt.<br/>                                                                                                                                                                              |
| TabStop<br/>                                                                             | **BOOL**<br/>              | Bestimmt, ob dieses Steuerelement ein Tabstopp ist.<br/>                                                                                                                                                                                |



 



| Ambient-Eigenschaft                         | type                        | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                            |
|------------------------------------------|-----------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| BackColor, ForeColor<br/>          | **OLE- \_ Farbe**<br/>   | Stellt Steuerelemente mit den Standard Hintergrund-und Vorder Grundfarben bereit. Die Verwendung durch ein-Steuerelement ist optional.<br/>                                                                                                                                                                                                                                                                                          |
| Schriftart<br/>                          | **IDispatch \***<br/> | Ein Zeiger auf ein Standard schriftobjekt, das die Standard Schriftart für das Formular definiert. Die Verwendung durch ein-Steuerelement ist optional. Weitere Informationen finden Sie unter [Standard Schriftart Objekt](standard-font-object.md) .<br/>                                                                                                                                                                                                    |
| LocaleID<br/>                      | **LCID**<br/>         | Die im Container verwendete Sprache. Die Verwendung durch ein-Steuerelement wird empfohlen.<br/>                                                                                                                                                                                                                                                                                                                        |
| UserMode<br/>                      | **BOOL**<br/>         | Beschreibt, ob sich der Container in einem Entwurfs Modus (**false**) oder im Lauf Modus (**true**) befindet, der von einem Steuerelement verwendet werden soll, um die verfügbaren Funktionen nach Bedarf zu ändern.<br/>                                                                                                                                                                                                                      |
| Uidead<br/>                        | **BOOL**<br/>         | Beschreibt, ob der Container in einem Modus ist, in dem Steuerelemente Benutzereingaben ignorieren sollten. Dies gilt unabhängig vom Usermode. In einem Container kann uidead im Entwurfs Modus immer auf **true** festgelegt werden, und er kann auf **true** festgelegt werden, wenn er einen Haltepunkt oder einen solchen während des Lauf Zeit Modus erreichen hat. Ein Steuerelement muss auf diese Eigenschaft achten.<br/>                                                                |
| MessageReflect<br/>                | **BOOL**<br/>         | Gibt an, ob der Container Windows-Meldungen wie z. b \_ . WM CtlColor, WM \_ DrawItem, WM \_ -Parser und so weiter als Ereignisse empfangen möchte.<br/>                                                                                                                                                                                                                                           |
| Supportsmnetmonics<br/>             | **BOOL**<br/>         | Beschreibt, ob der Container mnetmonics verarbeitet. Ein Steuerelement kann mit diesen Informationen alle gewünschten Aktionen ausführen, z. b. nicht Unterstreichung von Zeichen, die normalerweise als mnetmonisch verwendet werden.<br/>                                                                                                                                                                                                 |
| ShowGrabHandles, shoching<br/> | **BOOL**<br/>         | Beschreibt, ob ein Steuerelement einen schraffurrahmen oder Zieh Punkte (im schraffurrahmen) anzeigen soll, wenn es direkt aktiv ist. Steuerelemente müssen diese Eigenschaften einhalten, sodass der Container die eigentliche Kontrolle darüber gibt, wer diese Bits von Benutzeroberflächen tatsächlich zeichnet. Ein Steuerelement Container kann seinen eigenen zeichnen, anstatt sich auf jedes Steuerelement zu verlassen. in diesem Fall werden diese ambivalente immer **false** sein.<br/> |
| DisplayAsDefault<br/>              | **BOOL**<br/>         | Der Container macht eine **true** für diese Eigenschaft über jede Site verfügbar, die als Standard Schaltfläche markiert ist, wenn das Schaltflächen-Steuerelement mit einem dickeren Standardrahmen gezeichnet werden soll.<br/>                                                                                                                                                                                         |



 



| Erweiterte Eigenschaft          | type                        | BESCHREIBUNG                                                           |
|----------------------------|-----------------------------|-----------------------------------------------------------------------|
| Name<br/>            | **BSTR**<br/>         | Der Name des Containers für das Steuerelement.<br/>                      |
| Sichtbar<br/>         | **BOOL**<br/>         | Die Sichtbarkeit des Steuer Elements.<br/>                                  |
| Parent<br/>          | **IDispatch \***<br/> | Die dispinterface des Formulars, das das Steuerelement enthält.<br/>      |
| Standard, Abbrechen<br/> | **BOOL**<br/>         | Gibt an, ob dieses Steuerelement die Standard-oder Abbruch Schaltfläche ist<br/> |



 

Alle diese Standardeigenschaften haben negative DISPID-Werte, die ihren Standardstatus angeben.

Beachten Sie Folgendes: um Konflikte in den programmatischen Symbolen für diese DispIds zu vermeiden, erhalten alle Ambient-Eigenschaften Symbole in der Form DISPID \_ Ambient \_ *Property* as in DISPID \_ Ambient \_ ForeColor. Alle anderen Symbole verwenden die DISPID- \_ *Eigenschaft* wie üblich.

Einige Ambient-Eigenschaften, und Steuerelement Eigenschaften, beinhalten Farben. Der in den vorherigen Tabellen erwähnte **OLE- \_ Farbtyp** kann auf einen standardmäßigen **COLORREF** -Typ, einen Index für eine Palette, einen palettenrelativen Index oder einen System Farb Index verweisen, der mit der [**GetSysColor**](/windows/desktop/api/winuser/nf-winuser-getsyscolor) -Funktion verwendet wird. Die [**oletranslatecolor**](/windows/desktop/api/OleCtl/nf-olectl-oletranslatecolor) -Funktion konvertiert einen **OLE- \_ Farbtyp** in einen **COLORREF** -Typ, wenn eine Palette angegeben wird.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Steuerelement Eigenschaften](control-properties.md)
</dt> </dl>

 

