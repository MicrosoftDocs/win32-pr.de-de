---
title: EM_SETEDITSTYLEEX Meldung (RichEdit. h)
description: Legt die aktuellen Flags für erweiterte Bearbeitungs Stile fest.
ms.assetid: C5CECC7C-6418-4A72-9F0B-6F55BE89E302
keywords:
- Windows-Steuerelemente für EM_SETEDITSTYLEEX Meldung
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
ms.openlocfilehash: 72fe7a1ff420048f620d69196360678e9718a510
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103957003"
---
# <a name="em_seteditstyleex-message"></a>EM- \_ Nachricht

Legt die aktuellen Flags für erweiterte Bearbeitungs Stile fest.


```C++
#define EM_SETEDITSTYLEEX       (WM_USER + 275)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Gibt ein oder mehrere erweiterte Bearbeitungs Stil-Flags an. Eine Liste möglicher Werte finden Sie unter [**EM \_ geteditstyleex**](/windows/desktop/Controls/em-geteditstyleex).

</dd> <dt>

*lParam* 
</dt> <dd>

Eine Maske, die aus einem oder mehreren der *wParam* -Werte besteht. Nur die in dieser Maske angegebenen Werte werden festgelegt oder gelöscht. Dadurch kann ein einzelnes Flag festgelegt oder gelöscht werden, ohne die aktuellen flagzustände zu lesen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert ist der Zustand der erweiterten Flags für die Bearbeitungs Formatierung, nachdem Rich Edit versucht hat, ihre Bearbeitungs Stiländerungen zu implementieren. Die formatierungsflags zum Bearbeiten sind ein Satz von Flags, die den aktuellen Bearbeitungs Stil angeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 8 \[ -Desktop-Apps\]<br/>                                            |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2012 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**EM \_ geteditstyleex**](em-geteditstyleex.md)
</dt> </dl>

 

