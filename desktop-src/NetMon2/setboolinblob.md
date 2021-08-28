---
description: Die SetBoolInBlob-Funktion legt einen booleschen Wert an einer bestimmten Position in einem BLOB fest.
ms.assetid: 354d22be-b8c4-4068-8356-19b30ac188d0
title: SetBoolInBlob-Funktion (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetBoolInBlob
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: 95785714919ad99026c8e179c11f992a79efc4d99d0de4caab20fd00f63cbffc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120128820"
---
# <a name="setboolinblob-function"></a>SetBoolInBlob-Funktion

Die **SetBoolInBlob-Funktion** legt einen booleschen Wert an einer bestimmten Position in einem BLOB fest.

## <a name="syntax"></a>Syntax


```C++
DWORD SetBoolInBlob(
  _In_       HBLOB hBlob,
  _In_ const char  *pOwnerName,
  _In_ const char  *pCategoryName,
  _In_ const char  *pTagName,
  _In_       BOOL  Bool
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

Zeiger auf den Namen des **BLOB-Besitzers.**

</dd> <dt>

*pCategoryName* \[ In\]
</dt> <dd>

Zeiger auf den Namen der **BLOB-Kategorie.**

</dd> <dt>

*pTagName* \[ In\]
</dt> <dd>

Zeiger auf den Namen des **BLOB-Tags.**

</dd> <dt>

*Bool* \[ In\]
</dt> <dd>

Boolescher Wert, der an der angegebenen Position festgelegt wird.

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



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[GetBoolFromBlob](getboolfromblob.md)
</dt> <dt>

[SetClassIDInBlob](setclassidinblob.md)
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

 

 




