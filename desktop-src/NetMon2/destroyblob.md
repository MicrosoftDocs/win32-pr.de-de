---
description: Die destroyblob-Funktion gibt den gesamten Arbeitsspeicher frei, der dem BLOB zugeordnet ist, und zerstört dann das BLOB.
ms.assetid: 46cde0b7-1b59-426e-b19b-3c73af3d461a
title: Destroyblob-Funktion (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DestroyBlob
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: e90630981c16f38d601d4e06d04f9326174ef721
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362931"
---
# <a name="destroyblob-function"></a>Destroyblob-Funktion

Die **destroyblob** -Funktion gibt den gesamten Arbeitsspeicher frei, der dem BLOB zugeordnet ist, und zerstört dann das BLOB.

## <a name="syntax"></a>Syntax


```C++
DWORD DestroyBlob(
  _In_ HBLOB hBlob
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hblob* \[ in\]
</dt> <dd>

Handle für das-BLOB, das zerstört wird.

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
</dt> </dl>

 

 




