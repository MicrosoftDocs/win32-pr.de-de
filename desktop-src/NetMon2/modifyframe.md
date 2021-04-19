---
description: Die Funktion "modifyframe" ändert einen vorhandenen Frame mit neuen Daten.
ms.assetid: ebd248e4-b248-4f4a-8b94-a6d1c331d12a
title: Modifyframe-Funktion (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ModifyFrame
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: af3ef6c2c5ccae2b6410ac8fc81c815f790b17a6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345754"
---
# <a name="modifyframe-function"></a>Modifyframe-Funktion

Die Funktion " **modifyframe** " ändert einen vorhandenen Frame mit neuen Daten.

## <a name="syntax"></a>Syntax


```C++
HFRAME WINAPI ModifyFrame(
  _In_  HCAPTURE hCapture,
  _In_  DWORD    FrameNumber,
  _In_  LPBYTE   FrameData,
  _In_  DWORD    FrameLength,
  _Out_ __int64  TimeStamp
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hcapture* \[ in\]
</dt> <dd>

Handle für die Erfassung. Weitere Informationen zum Abrufen des Aufzeichnungs Handles finden Sie im Abschnitt "Hinweise" in diesem Thema zu **modifyframe** .

</dd> <dt>

*Framengegen ber* \[ in\]
</dt> <dd>

Die Rahmen Indexnummer.

</dd> <dt>

*FrameData* \[ in\]
</dt> <dd>

Zeiger auf ein Bytearray, das die neuen Frame Daten enthält.

</dd> <dt>

*Framelength* \[ in\]
</dt> <dd>

Länge der neuen Daten in Bytes.

</dd> <dt>

*Zeitstempel* \[ vorgenommen\]
</dt> <dd>

Zeitstempel, der angibt, wann der Rahmen geändert wurde.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist, ist der Rückgabewert ein Handle für einen neuen Frame.

Wenn die Funktion nicht erfolgreich ist, ist der Rückgabewert **null**.

## <a name="remarks"></a>Bemerkungen

Wenn der-Befehl erfolgreich ausgeführt wurde, zerstört die **modifyframe** -Funktion den ursprünglichen Frame.

[*Experten*](e.md) und [*Parser*](p.md) können die Funktion " **modifyframe** " aufzurufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                           |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                 |
| Header<br/>                   | <dl> <dt>Netmon. h</dt> </dl>  |
| Bibliothek<br/>                  | <dl> <dt>Nmapi. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




