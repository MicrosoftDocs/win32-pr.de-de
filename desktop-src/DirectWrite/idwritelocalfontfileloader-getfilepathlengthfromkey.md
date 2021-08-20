---
title: IDWriteLocalFontFileLoader GetFilePathLengthFromKey-Methode
description: Ruft die Länge des absoluten Dateipfads aus dem Referenzschlüssel der Schriftartdatei ab.
ms.assetid: bdd84d75-5a7a-448a-a52c-0f5997ab07b9
keywords:
- GetFilePathLengthFromKey-Methode Direct Write
- GetFilePathLengthFromKey-Methode Direct Write , IDWriteLocalFontFileLoader-Schnittstelle
- IDWriteLocalFontFileLoader-Schnittstelle Direct Write , GetFilePathLengthFromKey-Methode
topic_type:
- apiref
api_name:
- IDWriteLocalFontFileLoader.GetFilePathLengthFromKey
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 587f432f006493097ec8262fcc2201e2c3b67abe7115c395332671ec35efeba9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117816351"
---
# <a name="idwritelocalfontfileloadergetfilepathlengthfromkey-method"></a>IDWriteLocalFontFileLoader::GetFilePathLengthFromKey-Methode

Ruft die Länge des absoluten Dateipfads aus dem Referenzschlüssel der Schriftartdatei ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetFilePathLengthFromKey(
  [in]  const void   *fontFileReferenceKey,
              UINT32 fontFileReferenceKeySize,
  [out]       UINT32 *filePathLength
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*fontFileReferenceKey* \[ In\]
</dt> <dd>

Typ: **const \* void**

Verweisschlüssel für Schriftartdateien, der die lokale Schriftartdatei innerhalb des Bereichs des verwendeten Schriftartladeprogramm eindeutig identifiziert.

</dd> <dt>

*fontFileReferenceKeySize* 
</dt> <dd>

Typ: **UINT32**

Größe des Schriftartdatei-Referenzschlüssels in Bytes.

</dd> <dt>

*filePathLength* \[ out\]
</dt> <dd>

Typ: **UINT32 \***

Länge der Dateipfadzeichenfolge ohne das beendete **NULL-Zeichen.**

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

Wenn diese Methode erfolgreich ist, wird **S \_ OK** zurückgegeben. Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------|
| Bibliothek<br/> | <dl> <dt>Dwrite.lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>Dwrite.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IDWriteLocalFontFileLoader**](idwritelocalfontfileloader.md)
</dt> </dl>

 

 





