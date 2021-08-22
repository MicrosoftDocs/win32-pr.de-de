---
title: Rebar-Steuerelementstile (CommCtrl.h)
description: Neuleistensteuerelemente unterstützen neben Standardfensterstilen eine Vielzahl von Steuerelementstilen.
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
ms.openlocfilehash: 09e40a2f93820391d0c2b928c67784157c1f58d7995d42c51df5373d642bd796
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119078524"
---
# <a name="rebar-control-styles"></a>Formatvorlagen für DasBar-Steuerelement

Neuleistensteuerelemente unterstützen neben Standardfensterstilen eine Vielzahl von Steuerelementstilen.



| Konstante                                                                                                                                                                        | Beschreibung                                                                                                                                                                                                                                                                                                                                                 |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RBS_AUTOSIZE"></span><span id="rbs_autosize"></span><dl> <dt>**RBS \_ AUTOIZE**</dt> </dl>                      | [Version 4.71.](common-control-versions.md) Das Steuerelement für die Neuleiste ändert automatisch das Layout der Bänder, wenn sich die Größe oder Position des Steuerelements ändert. In diesem Fall wird eine [RBN-AUTOIZE-Benachrichtigung \_ ](rbn-autosize.md) gesendet.<br/>                                                                                              |
| <span id="RBS_BANDBORDERS"></span><span id="rbs_bandborders"></span><dl> <dt>**RBS \_ BANDBORDERS**</dt> </dl>             | [Version 4.71.](common-control-versions.md) Das Rebar-Steuerelement zeigt schmale Linien an, um angrenzende Bänder zu trennen.<br/>                                                                                                                                                                                                                                 |
| <span id="RBS_DBLCLKTOGGLE"></span><span id="rbs_dblclktoggle"></span><dl> <dt>**RBS \_ DBLCLKTOGGLE**</dt> </dl>          | [Version 4.71.](common-control-versions.md) Das Leistenband schaltet seinen maximierten oder minimierten Zustand um, wenn der Benutzer auf das Band doppelklickt. Ohne diesen Stil wird der maximierte oder minimierte Zustand umgeschaltet, wenn der Benutzer auf das Band klickt.<br/>                                                                                          |
| <span id="RBS_FIXEDORDER"></span><span id="rbs_fixedorder"></span><dl> <dt>**RBS \_ FIXEDORDER**</dt> </dl>                | [Version 4.70.](common-control-versions.md) Das Rebar-Steuerelement zeigt Bänder immer in der gleichen Reihenfolge an. Sie können Bänder in verschiedene Zeilen verschieben, aber die Bandreihenfolge ist statisch.<br/>                                                                                                                                                                      |
| <span id="RBS_REGISTERDROP"></span><span id="rbs_registerdrop"></span><dl> <dt>**RBS \_ REGISTERDROP**</dt> </dl>          | [Version 4.71.](common-control-versions.md) Das Rebar-Steuerelement generiert [RBN GETOBJECT-Benachrichtigungscodes, \_ ](rbn-getobject.md) wenn ein Objekt über ein Band im Steuerelement gezogen wird. Um die \_ RBN-GETOBJECT-Benachrichtigungen zu empfangen, initialisieren Sie OLE mit einem Aufruf von [**OleInitialize**](/windows/desktop/api/ole2/nf-ole2-oleinitialize) oder [**CoInitialize**](/windows/desktop/api/objbase/nf-objbase-coinitialize).<br/> |
| <span id="RBS_TOOLTIPS"></span><span id="rbs_tooltips"></span><dl> <dt>**\_RBS-QUICKINFOS**</dt> </dl>                      | [Version 4.71.](common-control-versions.md) Noch nicht unterstützt.<br/>                                                                                                                                                                                                                                                                                  |
| <span id="RBS_VARHEIGHT"></span><span id="rbs_varheight"></span><dl> <dt>**RBS \_ VARHEIGHT**</dt> </dl>                   | [Version 4.71.](common-control-versions.md) Das Rebar-Steuerelement zeigt nach Möglichkeit Bänder mit der minimal erforderlichen Höhe an. Ohne diesen Stil zeigt das Rebar-Steuerelement alle Bänder mit der gleichen Höhe an, wobei die Höhe des höchsten sichtbaren Bands verwendet wird, um die Höhe anderer Bänder zu bestimmen.<br/>                                                   |
| <span id="RBS_VERTICALGRIPPER"></span><span id="rbs_verticalgripper"></span><dl> <dt>**RBS \_ VERTICALGTROP**</dt> </dl> | [Version 4.71.](common-control-versions.md) Der Größen-Klammer wird vertikal statt horizontal in einem vertikalen Rebar-Steuerelement angezeigt. Dieser Stil wird für Steuerelemente der Neuleiste ignoriert, die nicht über den [**\_ CCS-VERT-Stil**](common-control-styles.md) verfügen.<br/>                                                                            |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>CommCtrl.h</dt> </dl> |



 

