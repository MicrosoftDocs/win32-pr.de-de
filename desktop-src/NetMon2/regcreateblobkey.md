---
description: Die regkreateblobkey-Funktion speichert ein BLOB mit dem angegebenen Registrierungsschlüssel.
ms.assetid: 14f3763e-aa04-4d51-b388-81ebf0d3952c
title: Regkreateblobkey-Funktion (Netmon. h)
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
ms.openlocfilehash: fc46b38919b37dc004c1065b0cc8d5f80e65984c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106355448"
---
# <a name="regcreateblobkey-function"></a>Regkreateblobkey-Funktion

Die **regkreateblobkey** -Funktion speichert ein BLOB mit dem angegebenen Registrierungsschlüssel.

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

*HKEY* \[ vorgenommen\]
</dt> <dd>

Handle für den Registrierungsschlüssel, in dem das BLOB gespeichert wird.

</dd> <dt>

*szblobname* \[ in\]
</dt> <dd>

Name (Anwendung definiert), der das BLOB in der Registrierung darstellt.

</dd> <dt>

*hblob* \[ in\]
</dt> <dd>

Handle für das BLOB, das gespeichert wird.

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

[Regopenblobkey](regopenblobkey.md)
</dt> </dl>

 

 




