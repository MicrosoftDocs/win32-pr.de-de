---
description: Die RegCreateBlobKey-Funktion speichert ein BLOB am angegebenen Registrierungsschlüssel.
ms.assetid: 14f3763e-aa04-4d51-b388-81ebf0d3952c
title: RegCreateBlobKey-Funktion (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RegCreateBlobKey
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: 3267fd0ba5e6fe56b99b5d465f69718fe5509a7ead58acf1d8dafb642397af5e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119889650"
---
# <a name="regcreateblobkey-function"></a>RegCreateBlobKey-Funktion

Die **RegCreateBlobKey-Funktion** speichert ein BLOB am angegebenen Registrierungsschlüssel.

## <a name="syntax"></a>Syntax


```C++
DWORD RegCreateBlobKey(
  _Out_       HKEY  hkey,
  _In_  const char  *szBlobName,
  _In_        HBLOB hBlob
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hkey* \[ out\]
</dt> <dd>

Handle für den Registrierungsschlüssel, in dem das BLOB gespeichert wird.

</dd> <dt>

*szBlobName* \[ In\]
</dt> <dd>

Name (anwendungsdefiniert), der das BLOB in der Registrierung darstellt.

</dd> <dt>

*hBlob* \[ In\]
</dt> <dd>

Handle für das blob, das gespeichert wird.

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



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[RegOpenBlobKey](regopenblobkey.md)
</dt> </dl>

 

 




