---
title: QuickInfo-Stile (CommCtrl.h)
description: In diesem Abschnitt werden die mit QuickInfo-Steuerelementen verwendeten Steuerelementstile aufgelistet.
ms.assetid: a6aeac71-6a69-4903-af78-0bfe1f83e632
topic_type:
- apiref
api_name:
- TTS_ALWAYSTIP
- TTS_BALLOON
- TTS_CLOSE
- TTS_NOANIMATE
- TTS_NOFADE
- TTS_NOPREFIX
- TTS_USEVISUALSTYLE
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2dddd890f8bf3aad35d20ec2eabcbe34f89b3ef262fbe30586f9a0a893f85e3b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119751022"
---
# <a name="tooltip-styles"></a>QuickInfo-Stile

In diesem Abschnitt werden die mit QuickInfo-Steuerelementen verwendeten Steuerelementstile aufgelistet.



| Konstante                                                                                                                                                                     | Beschreibung                                                                                                                                                                                                                                                                                                                                                       |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TTS_ALWAYSTIP"></span><span id="tts_alwaystip"></span><dl> <dt>**TTS \_ ALWAYSTIP**</dt> </dl>                | Gibt an, dass das QuickInfo-Steuerelement angezeigt wird, wenn sich der Cursor in einem Tool befindet, auch wenn das Besitzerfenster des QuickInfo-Steuerelements inaktiv ist. Ohne diesen Stil wird die QuickInfo nur angezeigt, wenn das Besitzerfenster des Tools aktiv ist.<br/>                                                                                                                                  |
| <span id="TTS_BALLOON"></span><span id="tts_balloon"></span><dl> <dt>**TTS \_ BALLOON**</dt> </dl>                      | [Version 5.80.](common-control-versions.md) Gibt an, dass das QuickInfo-Steuerelement das Aussehen eines Sprechblasens mit abgerundeten Ecken und einem Stamm hat, der auf das Element zeigt. <br/>                                                                                                                                                                      |
| <span id="TTS_CLOSE"></span><span id="tts_close"></span><dl> <dt>**TTS \_ CLOSE**</dt> </dl>                            | Zeigt eine Schaltfläche **Schließen** in der QuickInfo an. Nur gültig, wenn die QuickInfo über den TTS \_ BALLOON-Stil und einen Titel verfügt. Weitere Informationen finden Sie unter [**TTM \_ SETTITLE.**](ttm-settitle.md)<br/>                                                                                                                                                                                             |
| <span id="TTS_NOANIMATE"></span><span id="tts_noanimate"></span><dl> <dt>**TTS \_ NOANIMATE**</dt> </dl>                | [Version 5.80.](common-control-versions.md) Deaktiviert gleitende QuickInfo-Animationen auf Windows 98- und Windows 2000-Systemen. Dieser Stil wird auf früheren Systemen ignoriert.<br/>                                                                                                                                                                                      |
| <span id="TTS_NOFADE"></span><span id="tts_nofade"></span><dl> <dt>**TTS \_ NOFADE**</dt> </dl>                         | [Version 5.80.](common-control-versions.md) Deaktiviert die verblassende QuickInfo-Animation. <br/>                                                                                                                                                                                                                                                                       |
| <span id="TTS_NOPREFIX"></span><span id="tts_noprefix"></span><dl> <dt>**TTS \_ NOPREFIX**</dt> </dl>                   | Verhindert, dass das System ampersand-Zeichen aus einer Zeichenfolge entfernt oder eine Zeichenfolge an einem Tabstoppzeichen beendet. Ohne diesen Stil entfernt das System automatisch Ampersandzeichen und beendet eine Zeichenfolge beim ersten Tabstoppzeichen. Dadurch kann eine Anwendung dieselbe Zeichenfolge sowohl als Menüelement als auch als Text in einem QuickInfo-Steuerelement verwenden.<br/> |
| <span id="TTS_USEVISUALSTYLE"></span><span id="tts_usevisualstyle"></span><dl> <dt>**TTS \_ USEVISUALSTYLE**</dt> </dl> | Verwendet Themenlinks. Das Design definiert die Stile für alle Links in der QuickInfo. Für diesen Stil muss immer TTF \_ PARSELINKS festgelegt werden. <br/>                                                                                                                                                                                                          |



## <a name="remarks"></a>Hinweise

Ein QuickInfo-Steuerelement verfügt immer über die \_ Fensterstile WS POPUP und WS \_ EX \_ TOOLWINDOW, unabhängig davon, ob Sie sie beim Erstellen des Steuerelements angeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>CommCtrl.h</dt> </dl> |



 

 





