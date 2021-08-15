---
description: Legt den Blobmuster-Übereinstimmungsfilter fest.
ms.assetid: 44e7c67a-f430-4d68-bc7f-f6bbd5b9e5a9
title: SetNPPPatternFilterInBlob-Funktion (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetNPPPatternFilterInBlob
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: a920d6ffc135855826719e31613119a27671e334d5a75ce7dba29c2b140816fc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118363751"
---
# <a name="setnpppatternfilterinblob-function"></a>SetNPPPatternFilterInBlob-Funktion

Die **SetNPPPatternFilterInBlob-Funktion legt** den Blobmuster-Übereinstimmungsfilter fest.

## <a name="syntax"></a>Syntax


```C++
DWORD SetNPPPatternFilterInBlob(
  _In_  HBLOB        hBlob,
  _In_  LPEXPRESSION pExpression,
  _Out_ HBLOB        hErrorBlob
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hBlob* \[ In\]
</dt> <dd>

Das Handle für das BLOB.

</dd> <dt>

*pExpression* \[ In\]
</dt> <dd>

Ein Zeiger auf eine [EXPRESSION-Struktur,](expression.md) die den festgelegten Filterausdruck definiert.

</dd> <dt>

*hErrorBlob* \[ out\]
</dt> <dd>

Das Handle für ein Fehlerblob, das angibt, wo im ursprünglichen BLOB der Fehler aufgetreten ist (sofern ein Fehler aufgetreten ist).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die **SetNPPPatternFilterInBlob-Funktion** erfolgreich ist, ist der Rückgabewert NMERR \_ SUCCESS.

Wenn die Funktion nicht erfolgreich ist, ist der Rückgabewert ein NMERR-Wert, der den Fehler angibt.

## <a name="remarks"></a>Hinweise

Die In der **Config-Kategorie** des BLOB gespeicherten Muster-Matchfilterdaten.

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

[GetNPPAddressFilterFromBlob](getnppaddressfilterfromblob.md)
</dt> <dt>

[SetBoolInBlob](setboolinblob.md)
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

[SetNPPTriggerInBlob](setnpptriggerinblob.md)
</dt> <dt>

[SetStringInBlob](setstringinblob.md)
</dt> </dl>

 

 




