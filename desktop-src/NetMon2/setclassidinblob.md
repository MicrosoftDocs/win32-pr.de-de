---
description: Die SetClassIDInBlob-Funktion legt den Bezeichnerwert der benannten Klasse eines BLOB fest.
ms.assetid: d17dd48b-2e35-4c57-ba33-688180910b63
title: SetClassIDInBlob-Funktion (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetClassIDInBlob
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: 70e68d3a0d9d105b765ee6cd0ae1a6422f48e3dd6776cf144b302c9e1c5ff951
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118364159"
---
# <a name="setclassidinblob-function"></a>SetClassIDInBlob-Funktion

Die **SetClassIDInBlob-Funktion** legt den Bezeichnerwert der benannten Klasse eines BLOB fest.

## <a name="syntax"></a>Syntax


```C++
DWORD SetClassIDInBlob(
  _In_       HBLOB hBlob,
  _In_ const char  *pOwnerName,
  _In_ const char  *pCategoryName,
  _In_ const char  *pTagName,
  _In_ const CLSID *pClsID
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hBlob* \[ In\]
</dt> <dd>

Handle für ein BLOB.

</dd> <dt>

*pOwnerName* \[ In\]
</dt> <dd>

Zeiger auf den **Blobbesitzernamen,** der festgelegt ist.

</dd> <dt>

*pCategoryName* \[ In\]
</dt> <dd>

Zeiger auf den **Blobkategorienamen,** der festgelegt ist.

</dd> <dt>

*pTagName* \[ In\]
</dt> <dd>

Zeiger auf den **blob-Tagnamen,** der festgelegt ist.

</dd> <dt>

*pClsID* \[ In\]
</dt> <dd>

Zeiger auf den Klassenbezeichner des BLOB, das festgelegt ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist, lautet der Rückgabewert NMERR \_ SUCCESS.

Wenn die Funktion nicht erfolgreich ist, ist der Rückgabewert ein NMERR-Wert, der den Fehler angibt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                              |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                    |
| Header<br/>                   | <dl> <dt>Netmon.h</dt> </dl>     |
| Bibliothek<br/>                  | <dl> <dt>Npptools.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Npptools.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[GetClassIDFromBlob](getclassidfromblob.md)
</dt> <dt>

[SetBoolInBlob](setboolinblob.md)
</dt> <dt>

[SetDwordInBlob](setdwordinblob.md)
</dt> <dt>

[SetMacAddressInBlob](setmacaddressinblob.md)
</dt> <dt>

[SetNetworkInfoInBlob](setnetworkinfoinblob.md)
</dt> <dt>

[SetNPPAddressFilterInBlob](setnppaddressfilterinblob.md)
</dt> <dt>

[SetNPPPatternFilterInBlob](setnpppatternfilterinblob.md)
</dt> <dt>

[SetNPPTriggerInBlob](setnpptriggerinblob.md)
</dt> <dt>

[SetStringInBlob](setstringinblob.md)
</dt> </dl>

 

 




