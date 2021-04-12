---
description: Enthält Informationen zu einem Tablet-System Ereignis.
ms.assetid: 725f4b43-0bcb-4452-a87f-b24a85de0049
title: SYSTEM_EVENT_DATA Struktur
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
ms.openlocfilehash: 5d77c78a78a6cecae0368e8d9192a0dc0efc10e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218573"
---
# <a name="system_event_data-structure"></a>System \_ Ereignis- \_ Datenstruktur

Enthält Informationen zu einem Tablet-System Ereignis.

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

**bmodifizierer**
</dt> <dd>

Bitwerte für die Modifizierer. Weitere Informationen finden Sie im Abschnitt "Hinweise".

</dd> <dt>

**wkey**
</dt> <dd>

Scannen Sie den Code nach dem Tastatur Zeichen.

</dd> <dt>

**XPos**
</dt> <dd>

X-Position des Ereignisses.

</dd> <dt>

**YPos**
</dt> <dd>

Y-Position des Ereignisses.

</dd> <dt>

**bcurrsormode**
</dt> <dd>

Der Cursortyp, der das Ereignis verursacht hat. Weitere Informationen finden Sie im Abschnitt "Hinweise".

</dd> <dt>

**dwbuttonstate**
</dt> <dd>

Der Zustand der Schaltflächen zum Zeitpunkt des System Ereignisses.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die folgenden Systemereignisse werden für die Verwendung im **bmodifier** -Member definiert.



| Wert               | BESCHREIBUNG                  |
|---------------------|------------------------------|
| SE- \_ Modifizierer \_ STRG  | Die Steuerelement Taste wurde gedrückt. |
| SE- \_ Modifizierer \_ alt   | Die Alt-Taste wurde gedrückt.     |
| SE- \_ \_ modifiziererschicht | Die UMSCHALTTASTE wurde gedrückt.   |



 

Die folgenden Systemereignisse sind für die Verwendung im **bcurrsormode** -Member definiert.



| Wert              | BESCHREIBUNG               |
|--------------------|---------------------------|
| \_normaler \_ Cursor SE | Gibt den Stift Tipp an.    |
| SE- \_ \_ radierercursor | Gibt den Stift Radierer an. |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]<br/> |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Istylusplugin:: systemevent-Methode**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-systemevent)
</dt> <dt>

[**Itableteventsink:: systemevent-Methode**](itableteventsink-systemevent.md)
</dt> </dl>

 

 




