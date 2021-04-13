---
title: Idwrite-colorglyphrunenumerator-Methode von "muvenext"
description: Wechselt zum nächsten Symbol, das im Enumerator ausgeführt wird.
ms.assetid: E6336C0E-F880-485C-9111-A102298257C1
keywords:
- Methode "direkte Schreibvorgänge" in der Methode "
- Comvenext-Methode Direct Write, idwrite tecolorglyphrunenumerator-Schnittstelle
- Idwrite-colorglyphrunenumerator-Schnittstelle Direct Write, "ivenext"-Methode
topic_type:
- apiref
api_name:
- IDWriteColorGlyphRunEnumerator.MoveNext
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 15c9963916c07f1df8cf3cfedb49b9e3fd66d0df
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518113"
---
# <a name="idwritecolorglyphrunenumeratormovenext-method"></a>Idwrite-colorglyphrunenumerator:: ivenext-Methode

Wechselt zum nächsten Symbol, das im Enumerator ausgeführt wird.

## <a name="syntax"></a>Syntax


```C++
HRESULT MoveNext(
  [out] BOOL *haveRun
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*haverun* \[ vorgenommen\]
</dt> <dd>

Typ: **bool \** _

Gibt _ *true** zurück, wenn ein nächstes Symbol ausgeführt wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8.1 \[ Desktop-Apps \| UWP-apps\]<br/>                                     |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012 R2 \[ -Desktop-Apps \| UWP-apps\]<br/>                          |
| Unterstützte Mindestversion (Telefon)<br/>  | Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 und Windows-Runtime apps\]<br/> |
| Bibliothek<br/>                  | <dl> <dt>Dwrite. lib</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>Dwrite.dll</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Idschreitecolorglyphrunenumerator**](idwritecolorglyphrunenumerator.md)
</dt> </dl>

 

 





