---
description: Die getframerecognizedata-Funktion gibt eine Tabelle mit erkenzedata-Strukturen zurück. Jede dieser Strukturen enthält einen Protokoll Bezeichner und einen Offset, der auf den Anfang des angegebenen Protokolls in den Daten zeigt.
ms.assetid: 3bf809ff-8d87-4746-95ee-fb68c5e51d42
title: Getframerecognizedata-Funktion (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetFrameRecognizeData
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 627ba046b3adead0291239f5d94f4e56958e6a80
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958715"
---
# <a name="getframerecognizedata-function"></a>Getframerecognizedata-Funktion

Die **getframerecognizedata** -Funktion gibt eine Tabelle mit **erkenzedata** -Strukturen zurück. Jede dieser Strukturen enthält einen Protokoll Bezeichner und einen Offset, der auf den Anfang des angegebenen Protokolls in den Daten zeigt.

## <a name="syntax"></a>Syntax


```C++
LPRECOGNIZEDATATABLE WINAPI GetFrameRecognizeData(
  _In_ HFRAME hFrame
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hframe* \[ in\]
</dt> <dd>

Handle für einen Frame.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist, ist der Rückgabewert ein Zeiger auf eine **erkenzedatabel** -Struktur.

Wenn die Funktion nicht erfolgreich ist, ist der Rückgabewert 0 (null).

## <a name="remarks"></a>Bemerkungen

[*Experten*](e.md) und [*Parser*](p.md) können die **getframerecognizedata** -Funktion aufrufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                           |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                 |
| Header<br/>                   | <dl> <dt>Netmon. h</dt> </dl>  |
| Bibliothek<br/>                  | <dl> <dt>Nmapi. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




