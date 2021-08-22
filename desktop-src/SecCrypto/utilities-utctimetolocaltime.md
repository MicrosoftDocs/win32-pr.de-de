---
description: Konvertiert koordinierte Weltzeit (Greenwich Mean Time) in die Lokale Zeit des Computers.
ms.assetid: 4085d7cb-d346-477d-a043-e96fb951c35a
title: Utilities.UTCTimeToLocalTime-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Utilities.UTCTimeToLocalTime
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: c1ad7236564fff2f9a3814beda9bedacbf96fbc9ca2678546304ee108891bea1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119005148"
---
# <a name="utilitiesutctimetolocaltime-method"></a>Utilities.UTCTimeToLocalTime-Methode

\[Die **UTCTimeToLocalTime-Methode** ist für die Verwendung in den im Abschnitt Anforderungen angegebenen Betriebssystemen verfügbar.\]

Die **UTCTimeToLocalTime-Methode** konvertiert koordinierte Weltzeit (Greenwich Mean Time) in die Ortszeit des Computers.

## <a name="syntax"></a>Syntax


```VB
Utilities.UTCTimeToLocalTime( _
  ByVal UTCTime _
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*UTCTime* \[ In\]
</dt> <dd>

Die koordinierte Weltzeit, die in die Lokale Zeit des Computers konvertiert werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die Lokale Zeit, die dem angegebenen Wert koordinierte Weltzeit.

## <a name="remarks"></a>Hinweise

Während das System koordinierte Weltzeit verwendet, zeigen Anwendungen in der Regel die lokale Uhrzeit an. Dies ist das Datum und die Uhrzeit für die lokale Zeitzone des Computers.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------|----------------------------------------------------------------------------------------|
| Verteilbare Komponente<br/> | CAPICOM 2.0 oder höher auf Windows Server 2003 und Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Hilfsprogramme**](utilities.md)
</dt> </dl>

 

 




