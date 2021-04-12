---
title: IDWriteTextFormat2 setlinespacingmethode
description: Zeilenabstand festlegen. | IDWriteTextFormat2 setlinespacingmethode
ms.assetid: 71d8c6c4-920f-a1b5-5a13-9985a7aca41e
keywords:
- Setlinespacingmethode direkt schreiben
- Setlinespacingmethod Direct Write, IDWriteTextFormat2-Schnittstelle
- IDWriteTextFormat2 Interface Direct Write, setlinespacingmethode
topic_type:
- apiref
api_name:
- IDWriteTextFormat2.SetLineSpacing
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4d3514c52c9b8a51666d36eec7ce893735635f3e
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104219366"
---
# <a name="idwritetextformat2setlinespacing-method"></a>IDWriteTextFormat2:: setlinespacingmethode

Zeilenabstand festlegen.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetLineSpacing(
  [in] const DWRITE_LINE_SPACING *lineSpacingOptions
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*linespacingoptions* \[ in\]
</dt> <dd>

Typ: konstanter **[**dwrite- \_ Zeilen \_ Abstand**](/windows/win32/api/Dwrite_3/ns-dwrite_3-dwrite_line_spacing) \***

So verwalten Sie den Leerraum zwischen Zeilen

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Nur Desktop-Apps Windows 8.1\]<br/>                                            |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2012 R2 \[ -Desktop-Apps\]<br/>                                 |
| Unterstützte Mindestversion (Telefon)<br/>  | Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 und Windows-Runtime apps\]<br/> |
| Bibliothek<br/>                  | <dl> <dt>Dwrite. lib</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>Dwrite.dll</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IDWriteTextFormat2**](idwritetextformat2.md)
</dt> </dl>

 

 





