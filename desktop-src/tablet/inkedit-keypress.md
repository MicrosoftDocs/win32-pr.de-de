---
description: Tritt ein, wenn der Benutzer eine Taste drückt und freigibt, während das InkEdit-Steuerelement den Fokus besitzt.
ms.assetid: 8284ab41-dfac-4da2-b101-6968a43b15d7
title: InkEdit. KeyPress-Ereignis (Inked. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e49264f82b2cfe3c6998666339f08340a540791
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106358549"
---
# <a name="inkeditkeypress-event"></a>InkEdit. KeyPress-Ereignis

Tritt ein, wenn der Benutzer eine Taste drückt und freigibt, während das [InkEdit](inkedit-control-reference.md) -Steuerelement den Fokus besitzt.

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

Eine ganze Zahl, die einen numerischen Standard-ANSI-Keycode zurückgibt. Der *char* -Parameter wird als Verweis übergeben. durch das ändern wird ein anderes Zeichen an das Steuerelement gesendet. Wenn der *char* -Parameter in 0 geändert wird, wird das Ereignis abgebrochen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn dieses Ereignis erfolgreich ist, gibt es " **S \_ OK**" zurück. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="remarks"></a>Bemerkungen

Diese Ereignismethode wird in der **\_ iinkeditevents** -Schnittstelle definiert. Die **\_ iinkeditevents** -Schnittstelle implementiert die [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) -Schnittstelle mit dem Bezeichner DISPID \_ ieekeypress.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]<br/>                                                 |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                     |
| Header<br/>                   | <dl> <dt>In "-. h" (auch als "gezeichneten \_ i. c" erforderlich)</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>InkEd.dll</dt> </dl>                          |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[InkEdit](inkedit-control-reference.md)
</dt> <dt>

[**KeyDown-Ereignis, \[ InkEdit-Steuerelement\]**](inkedit-keydown.md)
</dt> <dt>

[**KeyUp-Ereignis \[ InkEdit-Steuerelement\]**](inkedit-keyup.md)
</dt> </dl>

 

