---
description: Die linetspioption- \_ Konstanten beschreiben, welche Bestell Dienstanbieter aufgerufen werden müssen.
ms.assetid: af91f466-d87e-4767-a2c6-d882b9108f21
title: LINETSPIOPTION_ Konstanten (TSPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 45e8fa13047dcbad60472fac371b255f7533809c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365415"
---
# <a name="linetspioption_-constants"></a>Linetspioption- \_ Konstanten

Die **linetspioption- \_ Konstanten** beschreiben, welche Bestell Dienstanbieter aufgerufen werden müssen.

<dl> <dt>

<span id="LINETSPIOPTION_NONREENTRANT"></span><span id="linetspioption_nonreentrant"></span>**linetspioption \_ nicht Wiedereinstiegs fähig**
</dt> <dd> <dl> <dt>



TAPI sollte Funktionen in diesem Dienstanbieter nacheinander aufzurufen. vor dem Aufrufen der gleichen oder einer anderen Funktion, entweder auf demselben oder einem anderen Thread, auf demselben oder einem anderen Prozessor, sollte von jeder Funktion auf die Rückgabe gewartet werden (aber nicht für asynchrone Funktionen).


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|-----------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 2,0 oder höher<br/>                                             |
| Header<br/>       | <dl> <dt>TSPI. h</dt> </dl> |



 

 




