---
title: IDWriteLocalFontFileLoader GetLastWriteTimeFromKey-Methode
description: Erhält den Zeitpunkt des letzten Schreibzugriffs der Datei aus dem Verweisschlüssel der Schriftartdatei.
ms.assetid: ce7f5321-8ad8-4412-a54c-7102790e99c0
keywords:
- GetLastWriteTimeFromKey-Methode Direct Write
- GetLastWriteTimeFromKey-Methode Direct Write, IDWriteLocalFontFileLoader-Schnittstelle
- IDWriteLocalFontFileLoader-Schnittstelle Direct Write , GetLastWriteTimeFromKey-Methode
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
ms.openlocfilehash: a2fb3d79475a943c3a635b347cfd6dbe41e8b3a8903022bae9089e1d6a9847c8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117816314"
---
# <a name="idwritelocalfontfileloadergetlastwritetimefromkey-method"></a>IDWriteLocalFontFileLoader::GetLastWriteTimeFromKey-Methode

Erhält den Zeitpunkt des letzten Schreibzugriffs der Datei aus dem Verweisschlüssel der Schriftartdatei.

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

*lastWriteTime* \[ out\]
</dt> <dd>

Typ: **FILETIME \***

Der Zeitpunkt der letzten Änderung der Schriftartdatei.

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

 

 





