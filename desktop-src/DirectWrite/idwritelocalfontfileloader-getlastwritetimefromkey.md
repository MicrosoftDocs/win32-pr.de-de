---
title: Idwrite telocalfontfileloader getlastschreitetimefromkey-Methode
description: Ruft den Zeitpunkt des letzten Schreibzugriffs auf die Datei aus dem Verweis Schlüssel der Schriftart Datei ab.
ms.assetid: ce7f5321-8ad8-4412-a54c-7102790e99c0
keywords:
- Getlastwrite tetimefromkey-Methode direkt schreiben
- Getlastwrite tetimefromkey-Methode Direct Write, idwrite telocalfontfileloader-Schnittstelle
- Idwrite telocalfontfileloader-Schnittstelle Direct Write, getlastschreitetimefromkey-Methode
topic_type:
- apiref
api_name:
- IDWriteLocalFontFileLoader.GetLastWriteTimeFromKey
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ea9817917a59761278a961a6fcafcdeaea5fda32
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365678"
---
# <a name="idwritelocalfontfileloadergetlastwritetimefromkey-method"></a>Idwrite telocalfontfileloader:: getlastschreitetimefromkey-Methode

Ruft den Zeitpunkt des letzten Schreibzugriffs auf die Datei aus dem Verweis Schlüssel der Schriftart Datei ab.

## <a name="syntax"></a>Syntax


```C++
virtual HRESULT GetLastWriteTimeFromKey(
  [in]  const void     *fontFileReferenceKey,
              UINT32   fontFileReferenceKeySize,
  [out]       FILETIME *lastWriteTime
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

*lastschreibzeit* \[ vorgenommen\]
</dt> <dd>

Typ: **FILETIME \***

Der Zeitpunkt der letzten Änderung der Schriftart Datei.

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

 

 





