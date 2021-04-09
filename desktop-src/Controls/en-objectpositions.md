---
title: EN_OBJECTPOSITIONS Benachrichtigungs Code (RichEdit. h)
description: Benachrichtigt das übergeordnete Fenster eines Rich-Edit-Steuer Elements, wenn das-Steuerelement Objekte einliest. Ein Rich Edit-Steuerelement sendet diesen Benachrichtigungs Code in Form einer WM-Benachrichtigungs \_ Meldung.
ms.assetid: 1965185f-8a13-4989-8574-af8b9b30f6b0
keywords:
- Windows-Steuerelemente für EN_OBJECTPOSITIONS Benachrichtigungs
topic_type:
- apiref
api_name:
- EN_OBJECTPOSITIONS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 35681f6734457eb6b6ebcac1bcb67227cbd3b9e9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103858947"
---
# <a name="en_objectpositions-notification-code"></a>EN \_ objectpositions-Benachrichtigungs Code

Benachrichtigt das übergeordnete Fenster eines Rich-Edit-Steuer Elements, wenn das-Steuerelement Objekte einliest. Ein Rich Edit-Steuerelement sendet diesen Benachrichtigungs Code in Form einer WM-Benachrichtigungs Meldung. [**\_**](wm-notify.md)


```C++
EN_OBJECTPOSITIONS

    pOjectPositions = (OBJECTPOSITIONS *) lParam; 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Eine [**objectpositions**](/windows/desktop/api/Richedit/ns-richedit-objectpositions) -Struktur.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt NULL zurück, um den **Lese** Vorgang fortzusetzen.

Gibt einen Wert ungleich 0 (null) zurück, um den **Lese** Vorgang anzuhalten.

## <a name="remarks"></a>Bemerkungen

Um einen en \_ objectpositions-Benachrichtigungs Code zu erhalten, geben Sie das [**ENM \_ objectpositions**](rich-edit-control-event-mask-flags.md) -Flag in der mit der [**EM \_ SetEventMask**](em-seteventmask.md) -Nachricht gesendeten Maske an.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Verweis**
</dt> <dt>

[**EM-- \_ einventmask**](em-seteventmask.md)
</dt> <dt>

[**Objectpositions**](/windows/desktop/api/Richedit/ns-richedit-objectpositions)
</dt> <dt>

[**WM- \_ Benachrichtigung**](wm-notify.md)
</dt> <dt>

**Andere Ressourcen**
</dt> <dt>

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))
</dt> <dt>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))
</dt> </dl>

 

