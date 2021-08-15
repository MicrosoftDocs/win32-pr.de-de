---
description: Die RegOpenBlobKey-Funktion ruft ein BLOB ab, das am angegebenen Registrierungsschlüssel gespeichert ist.
ms.assetid: f6b16c07-c705-47f1-a21c-6155368551c7
title: RegOpenBlobKey-Funktion (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RegOpenBlobKey
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: 5d372d6cc69c4e80691f96075aaa0d9030c90d06fc8256f85a7ed2dc894f3fc1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118364149"
---
# <a name="regopenblobkey-function"></a>RegOpenBlobKey-Funktion

Die **RegOpenBlobKey-Funktion** ruft ein BLOB ab, das am angegebenen Registrierungsschlüssel gespeichert ist.

## <a name="syntax"></a>Syntax


```C++
DWORD RegOpenBlobKey(
  _In_        HKEY  hkey,
  _In_  const char  *szBlobName,
  _Out_       HBLOB *phBlob
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hkey* \[ In\]
</dt> <dd>

Handle für den Registrierungsschlüssel, der das BLOB enthält.

</dd> <dt>

*szBlobName* \[ In\]
</dt> <dd>

Name, der das angegebene BLOB in der Registrierung identifiziert.

</dd> <dt>

*phBlob* \[ out\]
</dt> <dd>

Zeiger auf das abgerufene BLOB.

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

[RegCreateBlobKey](regcreateblobkey.md)
</dt> </dl>

 

 




