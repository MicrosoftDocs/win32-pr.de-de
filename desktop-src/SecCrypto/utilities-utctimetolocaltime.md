---
description: Konvertiert die koordinierte Weltzeit (Greenwich Mean Time) in die Ortszeit des Computers.
ms.assetid: 4085d7cb-d346-477d-a043-e96fb951c35a
title: Utilities. utctimetolocaltime-Methode
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
ms.openlocfilehash: fe41cf8d9ec92c0c71be5130aded0b7db539b9b1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361265"
---
# <a name="utilitiesutctimetolocaltime-method"></a>Utilities. utctimetolocaltime-Methode

\[Die **utctimetolocaltime** -Methode ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.\]

Die **utctimetolocaltime** -Methode konvertiert die koordinierte Weltzeit (Greenwich Mean Time) in die Ortszeit des Computers.

## <a name="syntax"></a>Syntax


```VB
Utilities.UTCTimeToLocalTime( _
  ByVal UTCTime _
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*UtcTime* \[ in\]
</dt> <dd>

Die koordinierte Weltzeit, die in die lokale Zeit des Computers konvertiert werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die Ortszeit, die der angegebenen koordinierten Weltzeit entspricht.

## <a name="remarks"></a>Bemerkungen

Während das System eine koordinierte Weltzeit intern verwendet, zeigen Anwendungen in der Regel die Ortszeit an, die das Datum und die Uhrzeit für die lokale Zeitzone des Computers ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------|----------------------------------------------------------------------------------------|
| Verteilbare Komponente<br/> | CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Versorgungsunternehmen**](utilities.md)
</dt> </dl>

 

 




