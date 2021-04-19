---
description: Konfiguriert die Voreinstellung der Standardfunktionen.
ms.assetid: 0afcb25a-2499-4baa-82ad-0706164e2e72
title: 'IH323LineEx:: setdefaultcapabilitypreferrenz-Methode (H323priv. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5604348eb80a3f423f6902f0a9a6e57204280c83
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106356383"
---
# <a name="ih323lineexsetdefaultcapabilitypreferrence-method"></a>IH323LineEx:: setdefaultcapabilitypreferrenz-Methode

\[**Setdefaultcapabilityprefergenz** ist nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die RTC-Client-API bietet eine ähnliche Funktionalität.\]

Die **setdefaultcapabilitypreferrenz** -Methode konfiguriert die Voreinstellung der Standardfunktionen. Funktionen haben eine Standard Gewichtung von 100. Wenn die Anwendung eine höhere Gewichtung für eine Funktion angibt, erhält Sie während der H. 245-Aushandlung eine höhere Priorität. Wenn die Anwendung die Gewichtung einer Funktion auf 0 festlegt, wird Sie in der H. 245-Aushandlung nicht verwendet.

Diese Methode ist kumulativ. Wenn diese Methode z. b. zuerst aufgerufen wird, um eine Funktion zu deaktivieren und erneut aufgerufen wird, um eine andere zu deaktivieren, werden beide Funktionen als Ergebnis dieser beiden Aufrufe deaktiviert.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetDefaultCapabilityPreferrence(
  [in] DWORD           dwNumCaps,
  [in] H245_CAPABILITY *pCapabilities,
  [in] DWORD           *pWeights
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*dwnumcaps* \[ in\]
</dt> <dd>

Ein **DWORD** -Wert, der die Anzahl von Funktionen enthält, die mit dieser Methode festgelegt werden.

</dd> <dt>

*pfunktionen* \[ in\]
</dt> <dd>

Ein Array von Funktionen. Jedes Element des Arrays ist ein [**H245- \_**](h245-capability.md) Funktionswert.

</dd> <dt>

*pgewichtungen* \[ in\]
</dt> <dd>

Ein Array von Gewichtungen, die den Funktionen zugeordnet sind.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Rückgabecode                                                                                   | Beschreibung                                                                                                                                                                                                                 |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Methode war erfolgreich.<br/>                                                                                                                                                                                                |
| <dl> <dt>**E \_ outo-Memory**</dt> </dl> | Zum Ausführen des Vorgangs ist nicht genügend Arbeitsspeicher vorhanden.<br/>                                                                                                                                                             |
| <dl> <dt>**E \_ invalidArg**</dt> </dl>  | Der *pcapability* -Parameter ist **null**, oder der *pgewichtungs* - **Parameter ist NULL**, oder sowohl *pcapability* als auch *pgewichtungen* sind **null**, oder das pcapability-Array enthält ein ungültiges H. 245-Funktions Objekt.<br/> |
| <dl> <dt>**E- \_ Zeiger**</dt> </dl>     | Ein Element des *pgewichtungs* Arrays oder ein Element des *parrays* -Arrays konnte nicht gelesen werden.<br/>                                                                                                                    |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|---------------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 3,0 oder höher<br/>                                                 |
| Header<br/>       | <dl> <dt>H323priv. h</dt> </dl> |
| Bibliothek<br/>      | <dl> <dt>UUID. lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl>  |



 

 




