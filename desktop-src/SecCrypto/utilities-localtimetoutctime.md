---
description: Konvertiert die Ortszeit des Computers in koordinierte Weltzeit (Greenwich Mean Time).
ms.assetid: ff5d40ba-7d94-4f11-9c18-e41752d1d7b9
title: Utilities.LocalTimeToUTCTime-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Utilities.LocalTimeToUTCTime
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 03efb6cdfbea712f2fbca194073b89bcee66975481c1a7c0fdc2d7bd385eb652
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117971021"
---
# <a name="utilitieslocaltimetoutctime-method"></a>Utilities.LocalTimeToUTCTime-Methode

\[Die **LocalTimeToUTCTime-Methode** ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt Anforderungen angegeben sind.\]

Die **LocalTimeToUTCTime-Methode** konvertiert die lokale Zeit des Computers in koordinierte Weltzeit (Greenwich Mean Time).

## <a name="syntax"></a>Syntax


```VB
Utilities.LocalTimeToUTCTime( _
  ByVal LocalTime _
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*LocalTime* \[ In\]
</dt> <dd>

Die ortslokale Zeit, die in koordinierte Weltzeit konvertiert werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die koordinierte Weltzeit, die der angegebenen Ortszeit entspricht.

## <a name="remarks"></a>Hinweise

Während das System intern koordinierte Weltzeit verwendet, zeigen Anwendungen in der Regel die Ortszeit an, d. h. datums- und tageszeit für die lokale Zeitzone des Computers.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------|----------------------------------------------------------------------------------------|
| Verteilbare Komponente<br/> | CAPICOM 2.0 oder höher auf Windows Server 2003 und Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Hilfsprogramme**](utilities.md)
</dt> </dl>

 

 




