---
description: Enthält Informationen zu einem Tablet-Systemereignis.
ms.assetid: 725f4b43-0bcb-4452-a87f-b24a85de0049
title: SYSTEM_EVENT_DATA-Struktur
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SYSTEM_EVENT_DATA
api_type:
- NA
api_location: ''
ms.openlocfilehash: 58e153da2695990f74d1268aa3e861bb9011b108ebdd1ea2d5128ff6f8e40a20
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119708210"
---
# <a name="system_event_data-structure"></a>SYSTEM \_ EVENT \_ DATA-Struktur

Enthält Informationen zu einem Tablet-Systemereignis.

## <a name="syntax"></a>Syntax


```C++
typedef struct tagSYSTEM_EVENT_DATA {
  BYTE  bModifier;
  WCHAR wKey;
  LONG  xPos;
  LONG  yPos;
  BYTE  bCursorMode;
  DWORD dwButtonState;
} SYSTEM_EVENT_DATA;
```



## <a name="members"></a>Member

<dl> <dt>

**bModifier**
</dt> <dd>

Bitwerte für die Modifizierer. Weitere Informationen finden Sie im Abschnitt "Hinweise".

</dd> <dt>

**wKey**
</dt> <dd>

Scancode für das Tastaturzeichen.

</dd> <dt>

**xPos**
</dt> <dd>

X Position des Ereignisses.

</dd> <dt>

**yPos**
</dt> <dd>

Y-Position des Ereignisses.

</dd> <dt>

**bCursorMode**
</dt> <dd>

Der Cursortyp, der das Ereignis verursacht hat. Weitere Informationen finden Sie im Abschnitt "Hinweise".

</dd> <dt>

**dwButtonState**
</dt> <dd>

Status der Schaltflächen zum Zeitpunkt des Systemereignisses.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die folgenden Systemereignisse werden für die Verwendung im **bModifier-Member** definiert.



| Wert               | Beschreibung                  |
|---------------------|------------------------------|
| \_SE MODIFIZIERER \_ STRG  | Die Steuertaste wurde gedrückt. |
| \_SE MODIFIZIERER \_ ALT   | Die ALT-TASTE wurde gedrückt.     |
| \_SE \_MODIFIZIERERVERSCHIEBUNG | Die UMSCHALTTASTE wurde gedrückt.   |



 

Die folgenden Systemereignisse werden für die Verwendung im **bCursorMode-Member** definiert.



| Wert              | Beschreibung               |
|--------------------|---------------------------|
| \_SE NORMAL \_ CURSOR | Gibt die Stiftspitze an.    |
| \_SE \_RADIERERCURSOR | Gibt den Stiftradierer an. |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur Desktop-Apps der XP Tablet PC Edition \[\]<br/> |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                     |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IStylusPlugin::SystemEvent-Methode**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-systemevent)
</dt> <dt>

[**ITabletEventSink::SystemEvent-Methode**](itableteventsink-systemevent.md)
</dt> </dl>

 

 




