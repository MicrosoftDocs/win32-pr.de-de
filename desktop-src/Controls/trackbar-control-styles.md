---
title: TrackBar-Steuerelement Stile (kommctrl. h)
description: Dieser Abschnitt enthält Informationen zu den Stilen, die mit TrackBar-Steuerelementen verwendet werden.
ms.assetid: ac2f59c6-85a2-4f41-aace-4132971d3559
topic_type:
- apiref
api_name:
- TBS_AUTOTICKS
- TBS_VERT
- TBS_HORZ
- TBS_TOP
- TBS_BOTTOM
- TBS_LEFT
- TBS_RIGHT
- TBS_BOTH
- TBS_NOTICKS
- TBS_ENABLESELRANGE
- TBS_FIXEDLENGTH
- TBS_NOTHUMB
- TBS_TOOLTIPS
- TBS_REVERSED
- TBS_DOWNISLEFT
- TBS_NOTIFYBEFOREMOVE
- TBS_TRANSPARENTBKGND
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 42966f98db18257c9a6a9ca463d5bd88028a02f7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364658"
---
# <a name="trackbar-control-styles"></a>TrackBar-Steuerelement Stile

Dieser Abschnitt enthält Informationen zu den Stilen, die mit TrackBar-Steuerelementen verwendet werden.



| Konstante                                                                                                                                                                           | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                           |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TBS_AUTOTICKS"></span><span id="tbs_autoticks"></span><dl> <dt>**TSB- \_ autoticks**</dt> </dl>                      | Das TrackBar-Steuerelement verfügt über einen Teil Strich für jedes Inkrement in seinem Wertebereich. <br/>                                                                                                                                                                                                                                                                           |
| <span id="TBS_VERT"></span><span id="tbs_vert"></span><dl> <dt>**TSB- \_ ververt**</dt> </dl>                                     | Das TrackBar-Steuerelement ist vertikal ausgerichtet.<br/>                                                                                                                                                                                                                                                                                                               |
| <span id="TBS_HORZ"></span><span id="tbs_horz"></span><dl> <dt>**TSB \_ Horz**</dt> </dl>                                     | Das TrackBar-Steuerelement ist horizontal ausgerichtet. Dies ist die Standardausrichtung. <br/>                                                                                                                                                                                                                                                                           |
| <span id="TBS_TOP"></span><span id="tbs_top"></span><dl> <dt>**TSB- \_ Top**</dt> </dl>                                        | Das TrackBar-Steuerelement zeigt Teil Striche oberhalb des Steuer Elements an. Dieser Stil ist nur mit TSB \_ Horz gültig. <br/>                                                                                                                                                                                                                                                      |
| <span id="TBS_BOTTOM"></span><span id="tbs_bottom"></span><dl> <dt>**TSB \_ unten**</dt> </dl>                               | Das TrackBar-Steuerelement zeigt unter dem Steuerelement Teil Striche an. Dieser Stil ist nur mit TSB \_ Horz gültig. <br/>                                                                                                                                                                                                                                                      |
| <span id="TBS_LEFT"></span><span id="tbs_left"></span><dl> <dt>**Linker TSB \_**</dt> </dl>                                     | Das TrackBar-Steuerelement zeigt die Teil Striche links neben dem Steuerelement an. Dieser Stil ist nur mit TSB \_ Vert gültig. <br/>                                                                                                                                                                                                                                             |
| <span id="TBS_RIGHT"></span><span id="tbs_right"></span><dl> <dt>**TSB- \_ Rechte**</dt> </dl>                                  | Das TrackBar-Steuerelement zeigt die Teil Striche rechts neben dem Steuerelement an. Dieser Stil ist nur mit TSB \_ Vert gültig. <br/>                                                                                                                                                                                                                                            |
| <span id="TBS_BOTH"></span><span id="tbs_both"></span><dl> <dt>**Beide TSB \_**</dt> </dl>                                     | Das TrackBar-Steuerelement zeigt Teil Striche auf beiden Seiten des Steuer Elements an. Dies ist sowohl bei der Verwendung mit TSB Horz als auch bei Verwendung von \_ left und right bei Verwendung mit TSB Vert von oben nach unten \_ . <br/>                                                                                                                                                                           |
| <span id="TBS_NOTICKS"></span><span id="tbs_noticks"></span><dl> <dt>**TSB- \_ Benachrichtigungen**</dt> </dl>                            | Das TrackBar-Steuerelement zeigt keine Teil Striche an. <br/>                                                                                                                                                                                                                                                                                                     |
| <span id="TBS_ENABLESELRANGE"></span><span id="tbs_enableselrange"></span><dl> <dt>**TSB- \_ enableselrange**</dt> </dl>       | Das TrackBar-Steuerelement zeigt nur einen Auswahlbereich an. Die Teil Striche an den Anfangs-und Endpositionen eines Auswahl Bereichs werden als Dreiecke (anstelle von vertikalen Bindestrichen) angezeigt, und der Auswahlbereich wird hervorgehoben. <br/>                                                                                                                           |
| <span id="TBS_FIXEDLENGTH"></span><span id="tbs_fixedlength"></span><dl> <dt>**TSB \_ FixedLength**</dt> </dl>                | Mit dem TrackBar-Steuerelement kann die Größe des Schiebereglers mit der [**TBM \_ setthumblength**](tbm-setthumblength.md) -Meldung geändert werden. <br/>                                                                                                                                                                                                                      |
| <span id="TBS_NOTHUMB"></span><span id="tbs_nothumb"></span><dl> <dt>**TSB- \_ Nothumb**</dt> </dl>                            | Das TrackBar-Steuerelement zeigt keinen Schieberegler an. <br/>                                                                                                                                                                                                                                                                                                           |
| <span id="TBS_TOOLTIPS"></span><span id="tbs_tooltips"></span><dl> <dt>**TSB- \_ Tooltips**</dt> </dl>                         | [Version 4,70](common-control-versions.md). Das TrackBar-Steuerelement unterstützt Quick Infos. Wenn ein TrackBar-Steuerelement mithilfe dieses Stils erstellt wird, wird automatisch ein Standardmäßiges QuickInfo-Steuerelement erstellt, das die aktuelle Position des Schiebereglers anzeigt. Sie können die Anzeige der Quick Infos ändern, indem Sie die [**TBM \_ -Datei "TBM**](tbm-settipside.md) " verwenden. <br/> |
| <span id="TBS_REVERSED"></span><span id="tbs_reversed"></span><dl> <dt>**umgekehrte TSB \_**</dt> </dl>                         | [Version 5,80.](common-control-versions.md) Dieses Stilbit wird für "umgekehrte" trackbars verwendet, bei denen eine geringere Zahl "höher" angibt und eine größere Zahl "Lower" angibt. Dies hat keine Auswirkung auf das Steuerelement. Es ist einfach eine Bezeichnung, die geprüft werden kann, um zu bestimmen, ob eine TrackBar normal oder umgekehrt ist.<br/>                                             |
| <span id="TBS_DOWNISLEFT"></span><span id="tbs_downisleft"></span><dl> <dt>**TSB- \_ Fenster Links**</dt> </dl>                   | Standardmäßig verwendet das TrackBar-Steuerelement nach unten rechts und nach oben gleich links. Verwenden Sie den TSB \_ -Fenster linken Stil, um die Standardeinstellung umzukehren, sodass Sie gleich links und nach oben rechtsbündig ist. <br/>                                                                                                                                                                          |
| <span id="TBS_NOTIFYBEFOREMOVE"></span><span id="tbs_notifybeforemove"></span><dl> <dt>**TSB \_ notifybeforemove**</dt> </dl> | [Version 6,00](common-control-versions.md) und **Windows Vista.** TrackBar sollte das übergeordnete Element Benachrichtigen, bevor der Schieberegler aufgrund der Benutzeraktion (aktiviert das ausrichten) neu positioniert wird. <br/>                                                                                                                                                                                   |
| <span id="TBS_TRANSPARENTBKGND"></span><span id="tbs_transparentbkgnd"></span><dl> <dt>**TSB- \_ transparentbkgnd**</dt> </dl> | [Version 6,00](common-control-versions.md) und **Windows Vista.** Der Hintergrund wird durch das übergeordnete Element über die WM- \_ printclient-Nachricht gezeichnet. <br/>                                                                                                                                                                                                                   |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Kommstrg. h</dt> </dl> |



 

 





