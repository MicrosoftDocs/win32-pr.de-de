---
title: IDWriteTextLayout3 SetLineSpacing-Methode
description: Legen Sie den Zeilenabstand fest. | IDWriteTextLayout3 SetLineSpacing-Methode
ms.assetid: 1bfca257-189c-4d18-628c-aff8217d2775
keywords:
- SetLineSpacing-Methode Direct Write
- SetLineSpacing-Methode Direct Write , IDWriteTextLayout3-Schnittstelle
- IDWriteTextLayout3-Schnittstelle Direct Write , SetLineSpacing-Methode
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
ms.openlocfilehash: 4d1c054fd63beb85303a7d163a16b55f07613b687085be53e22d814b0003c63c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118649378"
---
# <a name="idwritetextlayout3setlinespacing-method"></a>IDWriteTextLayout3::SetLineSpacing-Methode

Legen Sie den Zeilenabstand fest.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetLineSpacing(
  [in] const DWRITE_LINE_SPACING *lineSpacingOptions
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lineSpacingOptions* \[ In\]
</dt> <dd>

Verwalten des Speicherplatzes zwischen Linien.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ist, wird **S \_ OK** zurückgegeben. Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8.1 Nur Desktop-Apps\]<br/>                                            |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012 Nur \[ R2-Desktop-Apps\]<br/>                                 |
| Unterstützte Mindestversion (Telefon)<br/>  | Windows Phone 8.1 \[ Windows Phone Silverlight 8.1- und Windows Runtime-Apps\]<br/> |
| Bibliothek<br/>                  | <dl> <dt>Dwrite.lib</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>Dwrite.dll</dt> </dl>   |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IDWriteTextLayout3**](idwritetextlayout3.md)
</dt> </dl>

 

 





