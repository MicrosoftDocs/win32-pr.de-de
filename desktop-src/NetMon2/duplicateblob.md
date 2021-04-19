---
description: Die duplicateblob-Funktion kopiert ein bestimmtes Blob.
ms.assetid: d2478f53-328c-4799-890c-7849ce1f22e9
title: Duplicateblob-Funktion (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DuplicateBlob
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: df0fc00f0bd51e89da432e6f3b0143ce6092cedb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106359415"
---
# <a name="duplicateblob-function"></a>Duplicateblob-Funktion

Die **duplicateblob** -Funktion kopiert ein bestimmtes Blob.

## <a name="syntax"></a>Syntax


```C++
DWORD DuplicateBlob(
  _In_  HBLOB hSrcBlob,
  _Out_ HBLOB *hBlobThatWillBeCreated
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hsrcblob* \[ in\]
</dt> <dd>

Handle für das BLOB, das kopiert wird.

</dd> <dt>

*hblobthatwillbecreated* \[ vorgenommen\]
</dt> <dd>

Handle für das doppelte BLOB.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist, ist der Rückgabewert nmerr \_ Success.

Wenn die Funktion nicht erfolgreich ist, ist der Rückgabewert ein nmerr-Wert, der den Fehler beschreibt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                              |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                    |
| Header<br/>                   | <dl> <dt>Netmon. h</dt> </dl>     |
| Bibliothek<br/>                  | <dl> <dt>Npptools. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Npptools.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[CreateBlob](createblob.md)
</dt> <dt>

[Destroyblob](destroyblob.md)
</dt> </dl>

 

 




