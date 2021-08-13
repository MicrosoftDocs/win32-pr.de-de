---
description: Die \_ LINETSPIOPTION-Konstanten beschreiben, dass die Bestelldienstanbieter aufgerufen werden sollen.
ms.assetid: af91f466-d87e-4767-a2c6-d882b9108f21
title: LINETSPIOPTION_ Konstanten (Tspi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a5d4a57edd80a83ab442313706fd40a2fbd79f545a0b3e9485e5d8c88b8c2f8e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119404856"
---
# <a name="linetspioption_-constants"></a>LINETSPIOPTION-Konstanten \_

Die **\_ LINETSPIOPTION-Konstanten** beschreiben, dass die Bestelldienstanbieter aufgerufen werden sollen.

<dl> <dt>

<span id="LINETSPIOPTION_NONREENTRANT"></span><span id="linetspioption_nonreentrant"></span>**LINETSPIOPTION \_ NONREENTRANT**
</dt> <dd> <dl> <dt>



TAPI sollte Funktionen in diesem Dienstanbieter nach und nach aufrufen. Es sollte von jeder Funktion auf die Rückgabe (aber nicht auf den Abschluss asynchroner Funktionen) warten, bevor die gleiche oder eine andere Funktion aufgerufen wird, entweder auf demselben oder einem anderen Thread, auf demselben oder einem anderen Prozessor.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|-----------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 2.0 oder höher<br/>                                             |
| Header<br/>       | <dl> <dt>Tspi.h</dt> </dl> |



 

 




