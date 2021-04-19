---
description: Diese Funktion beendet das aufrufende Programm, wenn es in einer Lade Programm Legende aufgerufen wird. Andernfalls hat Sie keine Auswirkung.
ms.assetid: 5C10BF04-B7C7-4481-A184-FDD418FE5F52
title: Ldrfastfailinloadercallout-Funktion
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
ms.openlocfilehash: f74b9cdc0aec666242a8267fab8d6255c75dc94b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106373603"
---
# <a name="ldrfastfailinloadercallout-function"></a>Ldrfastfailinloadercallout-Funktion

\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können. Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]

Diese Funktion beendet das aufrufende Programm, wenn es in einer Lade Programm Legende aufgerufen wird. Andernfalls hat Sie keine Auswirkung.

## <a name="syntax"></a>Syntax


```C++
VOID NTAPI LdrFastFailInLoaderCallout(void);
```



## <a name="parameters"></a>Parameter

Diese Funktion besitzt keine Parameter.

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Diese Routine fängt nicht alle potenziellen deadlockfälle ab. Es ist möglich, dass ein Thread innerhalb eines Lade Programmen eine Sperre erhält, während ein Thread außerhalb einer Lade Modul Legende die gleiche Sperre besitzt und einen Aufruf an das Lade Modul durchführt. Anders ausgedrückt: zwischen der Loadersperre und einer Client Sperre kann eine Sperr Reihenfolge-Inversion vorhanden sein.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------|
| Bibliothek<br/> | <dl> <dt>Ntdll. lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>NTDll.dll</dt> </dl> |



 

 




