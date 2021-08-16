---
title: EM_SETEDITSTYLEEX Nachricht (Richedit.h)
description: Legt die aktuellen erweiterten Bearbeitungsformatflags fest.
ms.assetid: C5CECC7C-6418-4A72-9F0B-6F55BE89E302
keywords:
- EM_SETEDITSTYLEEX Windows-Steuerelemente für Nachrichten
topic_type:
- apiref
api_name:
- EM_SETEDITSTYLEEX
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b96a353b62dc3a31affd9e827ee803c481bcd806eaad9f8a5d0e9dd35388cf5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117831221"
---
# <a name="em_seteditstyleex-message"></a>EM \_ SETEDITSTYLEEX-Nachricht

Legt die aktuellen erweiterten Bearbeitungsformatflags fest.


```C++
#define EM_SETEDITSTYLEEX       (WM_USER + 275)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Gibt ein oder mehrere erweiterte Bearbeitungsformatflags an. Eine Liste der möglichen Werte finden Sie unter [**EM \_ GETEDITSTYLEEX**](/windows/desktop/Controls/em-geteditstyleex).

</dd> <dt>

*lParam* 
</dt> <dd>

Eine Maske, die aus einem oder mehreren *wParam-Werten* besteht. Nur die in dieser Maske angegebenen Werte werden festgelegt oder gelöscht. Dadurch kann ein einzelnes Flag festgelegt oder gelöscht werden, ohne die aktuellen Flagzustände zu lesen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert ist der Status der erweiterten Bearbeitungsformatflags, nachdem rich edit versucht hat, Änderungen am Bearbeitungsstil zu implementieren. Die Bearbeitungsformatflags sind eine Gruppe von Flags, die den aktuellen Bearbeitungsstil angeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8 Nur Desktop-Apps\]<br/>                                            |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2012 Nur Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**EM \_ GETEDITSTYLEEX**](em-geteditstyleex.md)
</dt> </dl>

 

