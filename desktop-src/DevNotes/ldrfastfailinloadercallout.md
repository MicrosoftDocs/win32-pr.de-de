---
description: Diese Funktion beendet das aufrufende Programm, wenn es innerhalb eines Ladeprogrammaufrufs aufgerufen wird. Andernfalls hat sie keine Auswirkungen.
ms.assetid: 5C10BF04-B7C7-4481-A184-FDD418FE5F52
title: LdrFastFailInLoaderCallout-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LdrFastFailInLoaderCallout
api_type:
- DllExport
api_location:
- NTDll.dll
ms.openlocfilehash: f944de64f26d814af799d1f8d2419c2dd9ade04970774e2581f446c0bd32c0fc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120001330"
---
# <a name="ldrfastfailinloadercallout-function"></a>LdrFastFailInLoaderCallout-Funktion

\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können. Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]

Diese Funktion beendet das aufrufende Programm, wenn es innerhalb eines Ladeprogrammaufrufs aufgerufen wird. Andernfalls hat sie keine Auswirkungen.

## <a name="syntax"></a>Syntax


```C++
VOID NTAPI LdrFastFailInLoaderCallout(void);
```



## <a name="parameters"></a>Parameter

Diese Funktion besitzt keine Parameter.

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Diese Routine fängt nicht alle potenziellen Deadlockfälle ab. Es ist möglich, dass ein Thread innerhalb eines Ladeprogrammaufrufs eine Sperre abruft, während ein Thread außerhalb einer Ladeprogramm-Callout die gleiche Sperre aufnimmt und einen Aufruf an das Ladeprogramm vornimmt. Anders ausgedrückt: Zwischen der Ladeprogrammsperre und einer Clientsperre kann eine Inversion der Sperrreihenfolge vorhanden sein.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------|
| Bibliothek<br/> | <dl> <dt>NTDll.lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>NTDll.dll</dt> </dl> |



 

 




