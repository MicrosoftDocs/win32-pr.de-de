---
title: EM_SELECTIONTYPE (Richedit.h)
description: Bestimmt den Auswahltyp für ein Rich-Edit-Steuerelement.
ms.assetid: a4200e32-1056-47bd-be47-5fabaf99c058
keywords:
- EM_SELECTIONTYPE von Windows-Steuerelementen
topic_type:
- apiref
api_name:
- EM_SELECTIONTYPE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1b79cb36759c857cea280b1c4beb5a476fa27a794f1f9985e1d259c345a9dc4b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119437840"
---
# <a name="em_selectiontype-message"></a>EM \_ SELECTIONTYPE-Meldung

Bestimmt den Auswahltyp für ein Rich-Edit-Steuerelement.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Nicht verwendet; muss 0 (null) sein.

</dd> <dt>

*lParam* 
</dt> <dd>

Nicht verwendet; muss 0 (null) sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Auswahl leer ist, ist der Rückgabewert SEL \_ EMPTY.

Wenn die Auswahl nicht leer ist, ist der Rückgabewert ein Satz von Flags, die einen oder mehrere der folgenden Werte enthalten.



| Rückgabecode                                                                                     | Beschreibung                                 |
|-------------------------------------------------------------------------------------------------|---------------------------------------------|
| <dl> <dt>**SEL \_ TEXT**</dt> </dl>        | Text.<br/>                            |
| <dl> <dt>**SEL \_ OBJECT**</dt> </dl>      | Mindestens ein COM-Objekt.<br/>         |
| <dl> <dt>**SEL \_ MULTICHAR**</dt> </dl>   | Mehr als ein Textzeichen.<br/> |
| <dl> <dt>**SEL \_ MULTIOBJECT**</dt> </dl> | Mehrere COM-Objekte.<br/>        |



 

## <a name="remarks"></a>Hinweise

Diese Meldung ist während der [**WM \_ SIZE-Verarbeitung**](/windows/desktop/winmsg/wm-size) für das übergeordnete Element eines bottomless Rich Edit-Steuerelements nützlich.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**WM \_ SIZE**](/windows/desktop/winmsg/wm-size)
</dt> </dl>

 

