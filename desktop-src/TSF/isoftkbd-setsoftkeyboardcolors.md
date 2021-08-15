---
title: ISoftKbd SetSoftKeyboardColors-Methode (Softkbdc.h)
description: Die ISoftKbd-Methode SetSoftKeyboardColors legt die Bildschirmtastaturfarbe für den angegebenen Farbtyp fest.
ms.assetid: 1abbff35-a5ef-4119-9367-60b6e0961c59
keywords:
- SetSoftKeyboardColors-Textdienstframework
- SetSoftKeyboardColors-Methode Textdienstframework , ISoftKbd-Schnittstelle
- ISoftKbd-Schnittstelle Textdienstframework , SetSoftKeyboardColors-Methode
topic_type:
- apiref
api_name:
- ISoftKbd.SetSoftKeyboardColors
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b572d62895a4f5df503df3ed78bfcf931af331ded25596267f0dd5b4286a4c4b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118877371"
---
# <a name="isoftkbdsetsoftkeyboardcolors-method"></a>ISoftKbd::SetSoftKeyboardColors-Methode

Die **ISoftKbd::SetSoftKeyboardColors-Methode** legt die Bildschirmtastaturfarbe für den angegebenen Farbtyp fest.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetSoftKeyboardColors(
  [in] COLORTYPE colorType,
  [in] COLORREF  Color
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*colorType* \[ In\]
</dt> <dd>

Ein -Wert, der den Farbtyp für die Softtastatur an gibt. Mögliche Werte werden für die [**COLORTYPE-Enumeration**](/windows/win32/api/icm/ne-icm-colortype) definiert.

</dd> <dt>

*Farbe* \[ In\]
</dt> <dd>

Ein [**32-Bit-COLORREF-Wert,**](/windows/desktop/gdi/colorref) der eine RGB-Farbe an gibt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Wert                                                                                        | BESCHREIBUNG                                  |
|----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | Die Methode war erfolgreich.<br/>        |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Einer der Parameter ist ungültig.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                             |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                   |
| Verteilbare Komponente<br/>          | TSF 1.0 auf Windows 2000 Professional<br/>                                        |
| Header<br/>                   | <dl> <dt>Softkbdc.h</dt> </dl>  |
| Idl<br/>                      | <dl> <dt>Softkbd.idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Softkbd.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**ISoftKbd**](isoftkbd.md)
</dt> <dt>

[**ISoftKbd::GetSoftKeyboardColors**](isoftkbd-getsoftkeyboardcolors.md)
</dt> <dt>

[**Farbtyp**](/windows/win32/api/icm/ne-icm-colortype)
</dt> <dt>

[**COLORREF**](/windows/desktop/gdi/colorref)
</dt> </dl>

 

