---
description: Die getprotocolstartoffsettthandle-Funktion gibt den Frame Offset eines bestimmten Protokolls zurück.
ms.assetid: b1e3a03b-f211-4c2c-8810-9e220c40136b
title: Getprotocolstarttfflthandle-Funktion (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetProtocolStartOffsetHandle
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: bac8a10e2a0d8be667f1448c523f208c0c3e1512
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106344402"
---
# <a name="getprotocolstartoffsethandle-function"></a>Getprotocolstarthfflthandle-Funktion

Die **getprotocolstartoffsettthandle** -Funktion gibt den Frame Offset eines bestimmten Protokolls zurück.

## <a name="syntax"></a>Syntax


```C++
DWORD WINAPI GetProtocolStartOffsetHandle(
  _In_ HFRAME    hFrame,
  _In_ HPROTOCOL hProtocol
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hframe* \[ in\]
</dt> <dd>

Handle für einen Frame.

</dd> <dt>

*hprotocol* \[ in\]
</dt> <dd>

Handle für ein Protokoll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist, ist der Rückgabewert der Offset des Frames, gemessen in Bytes.

Wenn die Funktion nicht erfolgreich ist, ist der Rückgabewert eins (1).

## <a name="remarks"></a>Bemerkungen

[*Experten*](e.md) und [*Parser*](p.md) können die **getprotocolstarto ffabthandle** -Funktion aufrufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                           |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                 |
| Header<br/>                   | <dl> <dt>Netmon. h</dt> </dl>  |
| Bibliothek<br/>                  | <dl> <dt>Nmapi. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




