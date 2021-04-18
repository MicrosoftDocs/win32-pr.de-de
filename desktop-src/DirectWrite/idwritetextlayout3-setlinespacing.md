---
title: IDWriteTextLayout3 setlinespacingmethode
description: Zeilenabstand festlegen. | IDWriteTextLayout3 setlinespacingmethode
ms.assetid: 1bfca257-189c-4d18-628c-aff8217d2775
keywords:
- Setlinespacingmethode direkt schreiben
- Setlinespacingmethod Direct Write, IDWriteTextLayout3-Schnittstelle
- IDWriteTextLayout3 Interface Direct Write, setlinespacingmethode
topic_type:
- apiref
api_name:
- IDWriteTextLayout3.SetLineSpacing
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 794df5b0dc993688c8bab15c927ae2c03bc18d69
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "106371848"
---
# <a name="idwritetextlayout3setlinespacing-method"></a>IDWriteTextLayout3:: setlinespacingmethode

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

So verwalten Sie den Leerraum zwischen Zeilen

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

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

[**IDWriteTextLayout3**](idwritetextlayout3.md)
</dt> </dl>

 

 





