---
title: Trackbar-Steuerelementstile (CommCtrl.h)
description: Dieser Abschnitt enthält Informationen zu den Stilen, die mit Trackbar-Steuerelementen verwendet werden.
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
ms.openlocfilehash: 9165325c2d78ac6e4dc1ae69e410d293100de24cb8d38868475e99e49c0faaa8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120046020"
---
# <a name="trackbar-control-styles"></a>Trackbar-Steuerelementstile

Dieser Abschnitt enthält Informationen zu den Stilen, die mit Trackbar-Steuerelementen verwendet werden.



| Konstante                                                                                                                                                                           | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                           |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TBS_AUTOTICKS"></span><span id="tbs_autoticks"></span><dl> <dt>**AUTOMATISCHE \_ TBS-TICKS**</dt> </dl>                      | Das Trackbar-Steuerelement verfügt über eine Teilstrichmarkierung für jedes Inkrement in seinem Wertebereich. <br/>                                                                                                                                                                                                                                                                           |
| <span id="TBS_VERT"></span><span id="tbs_vert"></span><dl> <dt>**\_TBS-VERT**</dt> </dl>                                     | Das Trackbar-Steuerelement ist vertikal ausgerichtet.<br/>                                                                                                                                                                                                                                                                                                               |
| <span id="TBS_HORZ"></span><span id="tbs_horz"></span><dl> <dt>**TBS \_ HORZ**</dt> </dl>                                     | Das Trackbar-Steuerelement ist horizontal ausgerichtet. Dies ist die Standardausrichtung. <br/>                                                                                                                                                                                                                                                                           |
| <span id="TBS_TOP"></span><span id="tbs_top"></span><dl> <dt>**TBS \_ TOP**</dt> </dl>                                        | Das Trackbar-Steuerelement zeigt Teilstriche über dem Steuerelement an. Dieser Stil ist nur bei TBS \_ HORZ gültig. <br/>                                                                                                                                                                                                                                                      |
| <span id="TBS_BOTTOM"></span><span id="tbs_bottom"></span><dl> <dt>**TBS \_ BOTTOM**</dt> </dl>                               | Das Trackbar-Steuerelement zeigt Teilstriche unterhalb des Steuerelements an. Dieser Stil ist nur bei TBS \_ HORZ gültig. <br/>                                                                                                                                                                                                                                                      |
| <span id="TBS_LEFT"></span><span id="tbs_left"></span><dl> <dt>**TBS \_ LEFT**</dt> </dl>                                     | Das Trackbar-Steuerelement zeigt Teilstriche links vom Steuerelement an. Dieser Stil ist nur mit TBS \_ VERT gültig. <br/>                                                                                                                                                                                                                                             |
| <span id="TBS_RIGHT"></span><span id="tbs_right"></span><dl> <dt>**TBS \_ RIGHT**</dt> </dl>                                  | Das Trackbar-Steuerelement zeigt Teilstriche rechts neben dem Steuerelement an. Dieser Stil ist nur mit TBS \_ VERT gültig. <br/>                                                                                                                                                                                                                                            |
| <span id="TBS_BOTH"></span><span id="tbs_both"></span><dl> <dt>**TBS \_ BEIDE**</dt> </dl>                                     | Das Trackbar-Steuerelement zeigt Teilstriche auf beiden Seiten des Steuerelements an. Dies ist sowohl oben als auch unten, wenn sie mit TBS HORZ verwendet \_ wird, oder sowohl links als auch rechts, wenn sie mit TBS VERT verwendet \_ werden. <br/>                                                                                                                                                                           |
| <span id="TBS_NOTICKS"></span><span id="tbs_noticks"></span><dl> <dt>**TBS \_ NOTICKS**</dt> </dl>                            | Das Trackbar-Steuerelement zeigt keine Teilstriche an. <br/>                                                                                                                                                                                                                                                                                                     |
| <span id="TBS_ENABLESELRANGE"></span><span id="tbs_enableselrange"></span><dl> <dt>**TBS \_ ENABLESELRANGE**</dt> </dl>       | Das Trackbar-Steuerelement zeigt nur einen Auswahlbereich an. Die Teilstriche an der Anfangs- und Endposition eines Auswahlbereichs werden als Dreiecke (anstelle vertikaler Bindestriche) angezeigt, und der Auswahlbereich wird hervorgehoben. <br/>                                                                                                                           |
| <span id="TBS_FIXEDLENGTH"></span><span id="tbs_fixedlength"></span><dl> <dt>**TBS \_ FIXEDLENGTH**</dt> </dl>                | Mit dem Trackbar-Steuerelement kann die Größe des Schiebereglers mit der [**TBM \_ SETTHUMBLENGTH-Nachricht**](tbm-setthumblength.md) geändert werden. <br/>                                                                                                                                                                                                                      |
| <span id="TBS_NOTHUMB"></span><span id="tbs_nothumb"></span><dl> <dt>**TBS \_ NOTHUMB**</dt> </dl>                            | Das Trackbar-Steuerelement zeigt keinen Schieberegler an. <br/>                                                                                                                                                                                                                                                                                                           |
| <span id="TBS_TOOLTIPS"></span><span id="tbs_tooltips"></span><dl> <dt>**\_TBS-QUICKINFOS**</dt> </dl>                         | [Version 4.70.](common-control-versions.md) Das Trackbar-Steuerelement unterstützt QuickInfos. Wenn ein Trackbar-Steuerelement mit diesem Stil erstellt wird, wird automatisch ein Standard-QuickInfo-Steuerelement erstellt, das die aktuelle Position des Schiebereglers anzeigt. Sie können ändern, wo die QuickInfos angezeigt werden, indem Sie die [**TBM \_ SETTIPSIDE-Meldung**](tbm-settipside.md) verwenden. <br/> |
| <span id="TBS_REVERSED"></span><span id="tbs_reversed"></span><dl> <dt>**TBS \_ UMGEKEHRT**</dt> </dl>                         | [Version 5.80.](common-control-versions.md) Dieses Stilbit wird für "umgekehrte" Trackbars verwendet, wobei eine kleinere Zahl auf "höher" und eine größere Zahl auf "niedriger" hinweist. Sie hat keine Auswirkungen auf das Steuerelement. Es handelt sich lediglich um eine Bezeichnung, die überprüft werden kann, um zu bestimmen, ob eine Trackbar normal oder umgekehrt ist.<br/>                                             |
| <span id="TBS_DOWNISLEFT"></span><span id="tbs_downisleft"></span><dl> <dt>**TBS \_ DOWNISLEFT**</dt> </dl>                   | Standardmäßig verwendet das Trackbar-Steuerelement nach unten gleich rechts und nach oben gleich links. Verwenden Sie den \_ TBS-DOWNISLEFT-Stil, um den Standardwert umzukehren, sodass nach unten links und nach oben gleich rechts wird. <br/>                                                                                                                                                                          |
| <span id="TBS_NOTIFYBEFOREMOVE"></span><span id="tbs_notifybeforemove"></span><dl> <dt>**TBS \_ NOTIFYBEFOREMOVE**</dt> </dl> | [Version 6.00](common-control-versions.md) und **Windows Vista.** Die Nachverfolgungsleiste sollte das übergeordnete Element benachrichtigen, bevor der Schieberegler aufgrund einer Benutzeraktion neu positioniert wird (aktiviert Snapping). <br/>                                                                                                                                                                                   |
| <span id="TBS_TRANSPARENTBKGND"></span><span id="tbs_transparentbkgnd"></span><dl> <dt>**TBS \_ TRANSPARENTBKGND**</dt> </dl> | [Version 6.00](common-control-versions.md) und **Windows Vista.** Der Hintergrund wird vom übergeordneten Element über die WM \_ PRINTCLIENT-Nachricht gezeichnet. <br/>                                                                                                                                                                                                                   |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>CommCtrl.h</dt> </dl> |



 

 





