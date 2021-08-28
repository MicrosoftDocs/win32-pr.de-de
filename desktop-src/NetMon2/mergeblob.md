---
description: Die MergeBlob-Funktion kopiert alle Einträge aus dem Quell-BLOB in ein Ziel-BLOB.
ms.assetid: 7521ce0c-fd02-4002-bdae-0d74a2e4a646
title: MergeBlob-Funktion (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MergeBlob
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: 5c0ce93235a0c46286b9bfbef0773a5584f3db774aa52991b4e0eaa9dd38352f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119677190"
---
# <a name="mergeblob-function"></a>MergeBlob-Funktion

Die **MergeBlob-Funktion** kopiert alle Einträge aus dem Quell-BLOB in ein Ziel-BLOB.

## <a name="syntax"></a>Syntax


```C++
DWORD MergeBlob(
  _Inout_ HBLOB hDstBlob,
  _In_    HBLOB hSrcBlob
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hDstBlob* \[ in, out\]
</dt> <dd>

Handle für das Ziel-BLOB. Bei der Eingabe enthält dieses BLOB seine ursprünglichen Informationen. Bei der Ausgabe enthält dieses BLOB seine ursprünglichen Informationen sowie alle Informationen des Quell-BLOB.

</dd> <dt>

*hSrcBlob* \[ In\]
</dt> <dd>

Handle für das Quellblob.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist, lautet der Rückgabewert NMERR \_ SUCCESS.

Wenn die Funktion nicht erfolgreich ist, ist der Rückgabewert ein NMERR-Wert, der den Fehler angibt.

## <a name="remarks"></a>Hinweise

Einträge, die für Quell- und Zieldateien gelten, werden mit Daten aus dem Quell-BLOB überschrieben.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                              |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                    |
| Header<br/>                   | <dl> <dt>Netmon.h</dt> </dl>     |
| Bibliothek<br/>                  | <dl> <dt>Npptools.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Npptools.dll</dt> </dl> |



 

 




