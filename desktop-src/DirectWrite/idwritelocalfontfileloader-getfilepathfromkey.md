---
title: Idwrite telocalfontfileloader getfilepathfromkey-Methode
description: Ruft den absoluten Schriftart Datei Pfad aus dem Verweis Schlüssel der Schriftart Datei ab.
ms.assetid: a61cfe80-100d-4813-b04f-a39f626893dd
keywords:
- Getfilepathfromkey-Methode direkt schreiben
- Getfilepathfromkey-Methode Direct Write, idwrite telocalfontfileloader-Schnittstelle
- Idwrite telocalfontfileloader-Schnittstelle Direct Write, getfilepathfromkey-Methode
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
ms.openlocfilehash: 14fb3070ddc2f0d82554c86f005343faa3c087fe
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361966"
---
# <a name="idwritelocalfontfileloadergetfilepathfromkey-method"></a>Idwrite telocalfontfileloader:: getfilepathfromkey-Methode

Ruft den absoluten Schriftart Datei Pfad aus dem Verweis Schlüssel der Schriftart Datei ab.

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

*fontfilereferencekey* \[ in\]
</dt> <dd>

Typ: Konstante **void \***

Der Verweis Schlüssel der Schriftart Datei, der die lokale Schriftart Datei innerhalb des Gültigkeits Bereichs des verwendeten Schriftart Lade Moduls eindeutig identifiziert.

</dd> <dt>

*fontfilereferencekeysize* 
</dt> <dd>

Typ: **UInt32**

Die Größe des Verweis Schlüssels der Schriftart Datei in Bytes.

</dd> <dt>

*FilePath* \[ vorgenommen\]
</dt> <dd>

Typ: **WCHAR \***

Das Zeichen Array, das den lokalen Dateipfad empfängt.

</dd> <dt>

*filepathsize* 
</dt> <dd>

Typ: **UInt32**

Die Länge des Dateipfad-Zeichen Arrays.

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

 

 





