---
title: Idwrite telocalfontfileloader getfilepathlängen fromkey-Methode
description: Ruft die Länge des absoluten Dateipfads aus dem Verweis Schlüssel der Schriftart Datei ab.
ms.assetid: bdd84d75-5a7a-448a-a52c-0f5997ab07b9
keywords:
- Getfilepathlängen fromkey-Methode direkt schreiben
- Getfilepathlängen fromkey-Methode Direct Write, idwrite telocalfontfileloader-Schnittstelle
- Idwrite telocalfontfileloader-Schnittstelle Direct Write, getfilepathlängen fromkey-Methode
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
ms.openlocfilehash: 091c3cd5f1e13c40d364a3db005793f1dd0bf5f1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365523"
---
# <a name="idwritelocalfontfileloadergetfilepathlengthfromkey-method"></a>Idwrite telocalfontfileloader:: getfilepathlängen fromkey-Methode

Ruft die Länge des absoluten Dateipfads aus dem Verweis Schlüssel der Schriftart Datei ab.

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

*fontfilereferencekey* \[ in\]
</dt> <dd>

Typ: Konstante **void \***

Verweis Schlüssel der Schriftart Datei, der die lokale Schriftart Datei innerhalb des Gültigkeits Bereichs des verwendeten Schriftart Lade Moduls eindeutig identifiziert.

</dd> <dt>

*fontfilereferencekeysize* 
</dt> <dd>

Typ: **UInt32**

Größe des Verweis Schlüssels der Schriftart Datei in Bytes.

</dd> <dt>

*filepathlength* \[ vorgenommen\]
</dt> <dd>

Typ: **UInt32 \***

Länge der Dateipfad-Zeichenfolge ohne das beendete **null** Zeichen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------|
| Bibliothek<br/> | <dl> <dt>Dwrite. lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>Dwrite.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Idschreitelocalfontfileloader**](idwritelocalfontfileloader.md)
</dt> </dl>

 

 





