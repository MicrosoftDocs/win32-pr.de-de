---
description: Tritt ein, wenn der Benutzer eine Taste drückt und freilässt, während das InkEdit-Steuerelement den Fokus besitzt.
ms.assetid: 8284ab41-dfac-4da2-b101-6968a43b15d7
title: InkEdit.KeyPress-Ereignis (Inked.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 713100edeae3ce6b950433afb73d13f40aefb291047e98984cbd6908dde3ce2b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119935099"
---
# <a name="inkeditkeypress-event"></a>InkEdit.KeyPress-Ereignis

Tritt ein, wenn der Benutzer eine Taste drückt und freilässt, während das [InkEdit-Steuerelement](inkedit-control-reference.md) den Fokus besitzt.

## <a name="syntax"></a>Syntax


```C++
HRESULT KeyPress(
   Long *Char
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Char* 
</dt> <dd>

Eine ganze Zahl, die einen standardmäßigen numerischen ANSI-Schlüsselcode zurückgibt. Der *Char-Parameter* wird als Verweis übergeben. Wenn sie geändert wird, wird ein anderes Zeichen an das -Steuerelement übermittelt. Wenn Sie den *Char-Parameter* in 0 ändern, wird das Ereignis abgebrochen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn dieses Ereignis erfolgreich ist, wird **S \_ OK zurückgegeben.** Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="remarks"></a>Hinweise

Diese Ereignismethode wird in der **\_ IInkEditEvents-Schnittstelle** definiert. Die **\_ IInkEditEvents-Schnittstelle** implementiert die [**IDispatch-Schnittstelle**](/windows/win32/api/oaidl/nn-oaidl-idispatch) mit dem Bezeichner DISPID \_ IeeKeyPress.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur Desktop-Apps der XP Tablet PC Edition \[\]<br/>                                                 |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                     |
| Header<br/>                   | <dl> <dt>Inked.h (erfordert auch inked \_ i.c)</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>InkEd.dll</dt> </dl>                          |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Inkedit](inkedit-control-reference.md)
</dt> <dt>

[**KeyDown-Ereignis \[ inkEdit-Steuerelement\]**](inkedit-keydown.md)
</dt> <dt>

[**KeyUp-Ereignis \[ inkEdit-Steuerelement\]**](inkedit-keyup.md)
</dt> </dl>

 

