---
description: Die regopenblobkey-Funktion Ruft ein BLOB ab, das am angegebenen Registrierungsschlüssel gespeichert ist.
ms.assetid: f6b16c07-c705-47f1-a21c-6155368551c7
title: Regopenblobkey-Funktion (Netmon. h)
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
ms.openlocfilehash: 24d788c8c4b69525d6c0be374845b44f804982bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362764"
---
# <a name="regopenblobkey-function"></a>Regopenblobkey-Funktion

Die **regopenblobkey** -Funktion Ruft ein BLOB ab, das am angegebenen Registrierungsschlüssel gespeichert ist.

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

*HKEY* \[ in\]
</dt> <dd>

Handle für den Registrierungsschlüssel, der das BLOB enthält.

</dd> <dt>

*szblobname* \[ in\]
</dt> <dd>

Der Name, der das angegebene BLOB in der Registrierung identifiziert.

</dd> <dt>

*phblob* \[ vorgenommen\]
</dt> <dd>

Zeiger auf das BLOB, das abgerufen wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist, ist der Rückgabewert nmerr \_ Success.

Wenn die Funktion nicht erfolgreich ist, ist der Rückgabewert ein nmerr-Wert, der den Fehler angibt.

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

[Regkreateblobkey](regcreateblobkey.md)
</dt> </dl>

 

 




