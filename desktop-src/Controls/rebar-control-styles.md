---
title: Grund leisten-Steuerelement Stile (kommstrg. h)
description: Grund leisten-Steuerelemente unterstützen zusätzlich zu Standardfenster Stilen eine Reihe von Steuerelement Stilen.
ms.assetid: 9690a4bd-51bd-4df9-8988-7da3ece7899f
topic_type:
- apiref
api_name:
- RBS_AUTOSIZE
- RBS_BANDBORDERS
- RBS_DBLCLKTOGGLE
- RBS_FIXEDORDER
- RBS_REGISTERDROP
- RBS_TOOLTIPS
- RBS_VARHEIGHT
- RBS_VERTICALGRIPPER
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 67b9f447df2cbf1bb2b956a7ec300d1f29280eef
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358386"
---
# <a name="rebar-control-styles"></a>Grund leisten-Steuerelement Stile

Grund leisten-Steuerelemente unterstützen zusätzlich zu Standardfenster Stilen eine Reihe von Steuerelement Stilen.



| Konstante                                                                                                                                                                        | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                 |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RBS_AUTOSIZE"></span><span id="rbs_autosize"></span><dl> <dt>**RSB \_ AutoSize**</dt> </dl>                      | [Version 4,71](common-control-versions.md). Das Grund leisten-Steuerelement ändert automatisch das Layout der Bänder, wenn sich die Größe oder Position des Steuer Elements ändert. Wenn dieses Problem auftritt, wird eine [ \_ Automatische RBN](rbn-autosize.md) -Benachrichtigung gesendet.<br/>                                                                                              |
| <span id="RBS_BANDBORDERS"></span><span id="rbs_bandborders"></span><dl> <dt>**RSB- \_ Band Rahmen**</dt> </dl>             | [Version 4,71](common-control-versions.md). Das Grund leisten-Steuerelement zeigt schmale Linien an, um angrenzende Bänder voneinander zu trennen.<br/>                                                                                                                                                                                                                                 |
| <span id="RBS_DBLCLKTOGGLE"></span><span id="rbs_dblclktoggle"></span><dl> <dt>**RSB \_ dblclktoggle**</dt> </dl>          | [Version 4,71](common-control-versions.md). Der Bereich der Info Leiste schaltet seinen maximierten oder minimierten Zustand um, wenn der Benutzer auf das Band doppelklickt. Ohne diesen Stil wird der maximierte oder minimierte Status ein-und ausgeschaltet, wenn der Benutzer auf das Band klickt.<br/>                                                                                          |
| <span id="RBS_FIXEDORDER"></span><span id="rbs_fixedorder"></span><dl> <dt>**RSB- \_ fixedorder**</dt> </dl>                | [Version 4,70](common-control-versions.md). Das Grund leisten-Steuerelement zeigt immer Bänder in derselben Reihenfolge an. Sie können Bänder in verschiedene Zeilen verschieben, aber die Reihenfolge der Bänder ist statisch.<br/>                                                                                                                                                                      |
| <span id="RBS_REGISTERDROP"></span><span id="rbs_registerdrop"></span><dl> <dt>**RSB- \_ Register Drop**</dt> </dl>          | [Version 4,71](common-control-versions.md). Das Grund leisten-Steuerelement generiert [RBN- \_ GetObject](rbn-getobject.md) -Benachrichtigungs Codes, wenn ein Objekt über ein Band im-Steuerelement gezogen wird. Um die RBN- \_ GetObject-Benachrichtigungen zu empfangen, initialisieren Sie OLE mit einem Aufrufen von [**OleInitialize**](/windows/desktop/api/ole2/nf-ole2-oleinitialize) oder [**CoInitialize**](/windows/desktop/api/objbase/nf-objbase-coinitialize).<br/> |
| <span id="RBS_TOOLTIPS"></span><span id="rbs_tooltips"></span><dl> <dt>**RSB-Quick Infos \_**</dt> </dl>                      | [Version 4,71](common-control-versions.md). Noch nicht unterstützt.<br/>                                                                                                                                                                                                                                                                                  |
| <span id="RBS_VARHEIGHT"></span><span id="rbs_varheight"></span><dl> <dt>**RSB \_ varHeight**</dt> </dl>                   | [Version 4,71](common-control-versions.md). Das Grund leisten-Steuerelement zeigt nach Möglichkeit Bänder mit der minimal erforderlichen Höhe an. Ohne diesen Stil zeigt das Grund leisten-Steuerelement alle Bänder in derselben Höhe an und verwendet dabei die Höhe des höchsten sichtbaren Bands, um die Höhe anderer Bänder zu ermitteln.<br/>                                                   |
| <span id="RBS_VERTICALGRIPPER"></span><span id="rbs_verticalgripper"></span><dl> <dt>**RSB \_ verticalgripperdatei**</dt> </dl> | [Version 4,71](common-control-versions.md). Der Größen Zieh Punkt wird vertikal anstatt horizontal in einem vertikalen Grund leisten-Steuerelement angezeigt. Dieser Stil wird für Grund leisten-Steuerelemente ignoriert, die nicht den CCS-Stil " [**\_ Vert**](common-control-styles.md) " aufweisen.<br/>                                                                            |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Kommstrg. h</dt> </dl> |



 

