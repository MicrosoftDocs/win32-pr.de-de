---
description: Die SetDwordInBlob-Funktion legt den benannten DWORD-Wert eines BLOB fest.
ms.assetid: 9174cd5c-4442-4fbe-8dc7-f8a74e1cc85d
title: SetDwordInBlob-Funktion (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetDwordInBlob
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: a0fdc05052542c8606bf72d7250e29086a59b6cc69761229df4800abdc781027
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118364048"
---
# <a name="setdwordinblob-function"></a>SetDwordInBlob-Funktion

Die **SetDwordInBlob-Funktion** legt den benannten **DWORD-Wert** eines BLOB fest.

## <a name="syntax"></a>Syntax


```C++
DWORD SetDwordInBlob(
  _In_       HBLOB hBlob,
  _In_ const char  *pOwnerName,
  _In_ const char  *pCategoryName,
  _In_ const char  *pTagName,
  _In_       DWORD Dword
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hBlob* \[ In\]
</dt> <dd>

Handle für ein BLOB, das festgelegt wird.

</dd> <dt>

*pOwnerName* \[ In\]
</dt> <dd>

Zeiger auf den **BLOB-Besitzernamen,** der festgelegt wird.

</dd> <dt>

*pCategoryName* \[ In\]
</dt> <dd>

Zeiger auf den namen der **BLOB-Kategorie,** der festgelegt wird.

</dd> <dt>

*pTagName* \[ In\]
</dt> <dd>

Zeiger auf den **BLOB-Tagnamen,** der festgelegt wird.

</dd> <dt>

*Dword* \[ In\]
</dt> <dd>

**DWORD-Wert** des festgelegten BLOBs.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist, ist der Rückgabewert NMERR \_ SUCCESS.

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

[GetDwordFromBlob](getdwordfromblob.md)
</dt> <dt>

[SetBoolInBlob](setboolinblob.md)
</dt> <dt>

[SetClassIDInBlob](setclassidinblob.md)
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

 

 




