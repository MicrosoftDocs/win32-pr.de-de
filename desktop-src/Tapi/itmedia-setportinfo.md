---
description: Die SetPortInfo-Methode legt den 16-Bit-Portwert für den ersten Port und die Anzahl der ports fest, die für eine Sitzung erforderlich sind.
ms.assetid: 4726b39b-cd10-4630-8f38-8671db4f432b
title: ITMedia::SetPortInfo-Methode (Sdpblb.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0db052c631fee1427b4d31c9149a2ef68f8819d8cacb24b632dc9b2f61d198c3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119140313"
---
# <a name="itmediasetportinfo-method"></a>ITMedia::SetPortInfo-Methode

\[Steuerelemente und Schnittstellen für Rendezvous-IP-Telefoniekonferenzen sind nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die RTC-Client-API bietet ähnliche Funktionen.\]

Die **SetPortInfo-Methode** legt den 16-Bit-Portwert für den ersten Port und die Anzahl der ports fest, die für eine Sitzung erforderlich sind.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetPortInfo(
  [in] LONG StartPort,
  [in] LONG NumPorts
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*StartPort* \[ In\]
</dt> <dd>

Startport. Dies kann ein Wert im Bereich von 0 bis 65535 sein.

</dd> <dt>

*NumPorts* \[ In\]
</dt> <dd>

Anzahl der Ports. Dies kann ein Wert im Bereich von 0 bis 65535 sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Rückgabecode                                                                                   | Beschreibung                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Methode war erfolgreich.<br/>                                    |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Der *StartPort- oder NumPorts-Parameter* ist ungültig.<br/>  |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Es ist nicht genügend Arbeitsspeicher vorhanden, um den Vorgang durchzuführen.<br/> |
| <dl> <dt>**E \_ FAIL**</dt> </dl>        | Unbekannter Fehler.<br/>                                   |
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl>     | Diese Methode ist noch nicht implementiert.<br/>                  |



 

## <a name="remarks"></a>Hinweise

Diese Funktion kann Daten unverschlüsselt über das Netzwerk senden. Aus diesem Grund kann eine Person, die im Netzwerk abhört, die Daten lesen. Das Sicherheitsrisiko des Sendens der Daten in Klartext sollte vor der Verwendung dieser Methode berücksichtigt werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|---------------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 3.0 oder höher<br/>                                                 |
| Header<br/>       | <dl> <dt>Sdpblb.h</dt> </dl>   |
| Bibliothek<br/>      | <dl> <dt>Uuid.lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**ITMedia**](itmedia.md)
</dt> </dl>

 

 




