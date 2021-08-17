---
title: IDWriteTextLayout3 GetLineSpacing-Methode
description: Ruft Zeilenabstandsinformationen ab.
ms.assetid: 6b93a3ec-c8ea-2e64-45b5-51565d6de173
keywords:
- GetLineSpacing-Methode "Direct Write"
- GetLineSpacing-Methode Direct Write , IDWriteTextLayout3-Schnittstelle
- IDWriteTextLayout3-Schnittstelle Direct Write , GetLineSpacing-Methode
topic_type:
- apiref
api_name:
- IDWriteTextLayout3.GetLineSpacing
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 96444f0e50cbb79074c6fc6d8b041d91c0751616ec5afe7024704709a2240947
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119964010"
---
# <a name="idwritetextlayout3getlinespacing-method"></a>IDWriteTextLayout3::GetLineSpacing-Methode

Ruft Zeilenabstandsinformationen ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetLineSpacing(
  [out] DWRITE_LINE_SPACING *lineSpacingOptions
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lineSpacingOptions* \[ out\]
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

 

 





