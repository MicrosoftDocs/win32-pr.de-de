---
description: Die GetFrameRecognizeData-Funktion gibt eine Tabelle mit RECOGNIZEDATA-Strukturen zurück. Jede dieser Strukturen enthält einen Protokollbezeichner und einen Offset, der auf den Anfang des angegebenen Protokolls in den Daten zeigt.
ms.assetid: 3bf809ff-8d87-4746-95ee-fb68c5e51d42
title: GetFrameRecognizeData-Funktion (Netmon.h)
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
ms.openlocfilehash: 2b04472e0fee0238677a6592cace0d1c7fbe078635ac85b92ff8922c68da3c1d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118366498"
---
# <a name="getframerecognizedata-function"></a>GetFrameRecognizeData-Funktion

Die **GetFrameRecognizeData-Funktion** gibt eine Tabelle mit **RECOGNIZEDATA-Strukturen** zurück. Jede dieser Strukturen enthält einen Protokollbezeichner und einen Offset, der auf den Anfang des angegebenen Protokolls in den Daten zeigt.

## <a name="syntax"></a>Syntax


```C++
LPRECOGNIZEDATATABLE WINAPI GetFrameRecognizeData(
  _In_ HFRAME hFrame
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hFrame* \[ In\]
</dt> <dd>

Handle für einen Frame.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist, ist der Rückgabewert ein Zeiger auf eine **RECOGNIZEDATATABLE-Struktur.**

Wenn die Funktion nicht erfolgreich ist, ist der Rückgabewert 0 (null).

## <a name="remarks"></a>Hinweise

[*Experten*](e.md) und [*Parser*](p.md) können die **GetFrameRecognizeData-Funktion** aufrufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                           |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                 |
| Header<br/>                   | <dl> <dt>Netmon.h</dt> </dl>  |
| Bibliothek<br/>                  | <dl> <dt>Nmapi.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




