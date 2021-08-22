---
title: MM_JOY2BUTTONUP Meldung (Mmsystem.h)
description: Die \_ MM-NACHRICHT "MMMAKER2BUTTONUP" benachrichtigt das Fenster, das das Fenster erfasst hat, dass eine Schaltfläche losgelassen wurde.
ms.assetid: da024466-7cd3-42ec-90a7-1468eb42841e
keywords:
- MM_JOY2BUTTONUP Nachricht Windows Multimedia
topic_type:
- apiref
api_name:
- MM_JOY2BUTTONUP
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8f94a1761686bd2e3ac7c470268427a213d54cdb4b8a58d54fdd6961427c2377
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119557310"
---
# <a name="mm_joy2buttonup-message"></a>\_MM–NACHRICHT VOM 2.BUTTONUP

Die **\_ MM-NACHRICHT "MMMAKER2BUTTONUP"** benachrichtigt das Fenster, das das Fenster erfasst hat, dass eine Schaltfläche losgelassen wurde.


```C++
MM_JOY2BUTTONUP 
fwButton = wParam; 
xPos = LOWORD(lParam); 
yPos = HIWORD(lParam); 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

**fwButtons** 
</dt> <dd>

Identifiziert die Schaltfläche, deren Zustand geändert wurde, und die gedrückten Schaltflächen. Folgende Werte sind möglich:



| Wert                                                                                                                                                            | Bedeutung                                              |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| <span id="JOY_BUTTON1CHG"></span><span id="joy_button1chg"></span><dl> <dt>**JOY \_ BUTTON1CHG**</dt> </dl> | Der Zustand der ersten Schaltfläche wurde geändert.<br/>  |
| <span id="JOY_BUTTON2CHG"></span><span id="joy_button2chg"></span><dl> <dt>**JOY \_ BUTTON2CHG**</dt> </dl> | Der Zustand der zweiten Schaltfläche hat sich geändert.<br/> |
| <span id="JOY_BUTTON3CHG"></span><span id="joy_button3chg"></span><dl> <dt>**BUTTON \_ BUTTON3CHG**</dt> </dl> | Die dritte Schaltfläche "button" hat den Zustand geändert.<br/>  |
| <span id="JOY_BUTTON4CHG"></span><span id="joy_button4chg"></span><dl> <dt>**JOY \_ BUTTON4CHG**</dt> </dl> | Der Zustand der vierten Schaltfläche hat sich geändert.<br/> |



 

und mindestens eine der folgenden Angaben:



| Wert                                                                                                                                                   | Bedeutung                                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| <span id="JOY_BUTTON1"></span><span id="joy_button1"></span><dl> <dt>**JOY \_ BUTTON1**</dt> </dl> | Die erste Schaltfläche wird gedrückt.<br/>  |
| <span id="JOY_BUTTON2"></span><span id="joy_button2"></span><dl> <dt>**JOY \_ BUTTON2**</dt> </dl> | Die zweite Schaltfläche wird gedrückt.<br/> |
| <span id="JOY_BUTTON3"></span><span id="joy_button3"></span><dl> <dt>**JOY \_ BUTTON3**</dt> </dl> | Die dritte Schaltfläche wird gedrückt.<br/>  |
| <span id="JOY_BUTTON4"></span><span id="joy_button4"></span><dl> <dt>**JOY \_ BUTTON4**</dt> </dl> | Die vierte Schaltfläche wird gedrückt.<br/> |



 

</dd> <dt>

**xPos** 
</dt> <dd>

Die x-Koordinaten des Bereichs relativ zur oberen linken Ecke des Clientbereichs.

</dd> <dt>

**yPos** 
</dt> <dd>

Die y-Koordinate des Bereichs relativ zur oberen linken Ecke des Clientbereichs.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>Mmsystem.h (include Windows.h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Joysticks](joysticks.md)
</dt> <dt>

[Multimedia-Meldungen](multimedia-joystick-messages.md)
</dt> </dl>

 

 





