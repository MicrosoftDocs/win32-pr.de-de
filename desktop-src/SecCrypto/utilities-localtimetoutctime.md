---
description: Konvertiert die lokale Zeit des Computers in eine koordinierte Weltzeit (Greenwich Mean Time).
ms.assetid: ff5d40ba-7d94-4f11-9c18-e41752d1d7b9
title: Utilities. localtimetoutctime-Methode
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
ms.openlocfilehash: 2691e3306a84ce4eff3d73df4b070ba4b65671f9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106355857"
---
# <a name="utilitieslocaltimetoutctime-method"></a>Utilities. localtimetoutctime-Methode

\[Die **localtimetoutctime** -Methode ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.\]

Die **localtimetoutctime** -Methode konvertiert die lokale Zeit des Computers in eine koordinierte Weltzeit (Greenwich Mean Time).

## <a name="syntax"></a>Syntax


```VB
Utilities.LocalTimeToUTCTime( _
  ByVal LocalTime _
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Localtime* \[ in\]
</dt> <dd>

Die Ortszeit, die in die koordinierte Weltzeit konvertiert werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die koordinierte Weltzeit, die der angegebenen Ortszeit entspricht.

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

 

 




