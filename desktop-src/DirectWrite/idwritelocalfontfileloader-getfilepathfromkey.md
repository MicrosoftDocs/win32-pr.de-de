---
title: IDWriteLocalFontFileLoader GetFilePathFromKey-Methode
description: Erhält den absoluten Schriftartdateipfad aus dem Schriftartdateiverweisschlüssel.
ms.assetid: a61cfe80-100d-4813-b04f-a39f626893dd
keywords:
- 'GetFilePathFromKey-Methode : Direct Write'
- GetFilePathFromKey-Methode Direct Write, IDWriteLocalFontFileLoader-Schnittstelle
- IDWriteLocalFontFileLoader-Schnittstelle Direct Write , GetFilePathFromKey-Methode
topic_type:
- apiref
api_name:
- IDWriteLocalFontFileLoader.GetFilePathFromKey
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7739cfa4a03abb3506bd63a84e0c747021110198f7d0ffefa69116656cbfa616
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119928030"
---
# <a name="idwritelocalfontfileloadergetfilepathfromkey-method"></a>IDWriteLocalFontFileLoader::GetFilePathFromKey-Methode

Erhält den absoluten Schriftartdateipfad aus dem Schriftartdateiverweisschlüssel.

## <a name="syntax"></a>Syntax


```C++
virtual HRESULT GetFilePathFromKey(
  [in]  const void   *fontFileReferenceKey,
              UINT32 fontFileReferenceKeySize,
  [out]       WCHAR  *filePath,
              UINT32 filePathSize
) = 0;
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*fontFileReferenceKey* \[ In\]
</dt> <dd>

Typ: **const \* void**

Der Verweisschlüssel der Schriftartdatei, der die lokale Schriftartdatei innerhalb des Bereichs des verwendeten Schriftartladeers eindeutig identifiziert.

</dd> <dt>

*fontFileReferenceKeySize* 
</dt> <dd>

Typ: **UINT32**

Die Größe des Schriftartdateiverweisschlüssels in Bytes.

</dd> <dt>

*filePath* \[ out\]
</dt> <dd>

Typ: **WCHAR \***

Das Zeichenarray, das den lokalen Dateipfad empfängt.

</dd> <dt>

*filePathSize* 
</dt> <dd>

Typ: **UINT32**

Die Länge des Dateipfadzeichenarrays.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

Wenn diese Methode erfolgreich ist, wird **S \_ OK zurückgegeben.** Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------|
| Bibliothek<br/> | <dl> <dt>Dwrite.lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>Dwrite.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IDWriteLocalFontFileLoader**](idwritelocalfontfileloader.md)
</dt> </dl>

 

 





