---
title: EM_SELECTIONTYPE Meldung (RichEdit. h)
description: Bestimmt den Auswahltyp für ein Rich-Edit-Steuerelement.
ms.assetid: a4200e32-1056-47bd-be47-5fabaf99c058
keywords:
- Windows-Steuerelemente für EM_SELECTIONTYPE Meldung
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
ms.openlocfilehash: d0deb62ac3bf774c72bb076f6fce9aa8c77b423f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518683"
---
# <a name="em_selectiontype-message"></a>EM \_ SelectionType-Meldung

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

Wenn die Auswahl leer ist, ist SEL Empty der Rückgabewert \_ .

Wenn die Auswahl nicht leer ist, ist der Rückgabewert ein Satz von Flags, der einen oder mehrere der folgenden Werte enthält.



| Rückgabecode                                                                                     | Beschreibung                                 |
|-------------------------------------------------------------------------------------------------|---------------------------------------------|
| <dl> <dt>**SEL- \_ Text**</dt> </dl>        | Text.<br/>                            |
| <dl> <dt>**SEL- \_ Objekt**</dt> </dl>      | Mindestens ein COM-Objekt.<br/>         |
| <dl> <dt>**SEL \_ multichar**</dt> </dl>   | Mehr als ein Textzeichen.<br/> |
| <dl> <dt>**SEL- \_ Multiobject**</dt> </dl> | Mehr als ein COM-Objekt.<br/>        |



 

## <a name="remarks"></a>Bemerkungen

Diese Meldung ist während der Verarbeitung der [**WM- \_ Größe**](/windows/desktop/winmsg/wm-size) für das übergeordnete Element eines untersten Rich-Edit-Steuer Elements nützlich.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**WM- \_ Größe**](/windows/desktop/winmsg/wm-size)
</dt> </dl>

 

