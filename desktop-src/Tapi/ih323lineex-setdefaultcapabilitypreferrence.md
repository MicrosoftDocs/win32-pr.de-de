---
description: Konfiguriert die Einstellung der Standardfunktionen.
ms.assetid: 0afcb25a-2499-4baa-82ad-0706164e2e72
title: IH323LineEx::SetDefaultCapabilityPreferrence-Methode (H323priv.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 64eb3385edb758529f27f9fb90eb0cce998eca60f202c72a28ba48a5318c6b08
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119992080"
---
# <a name="ih323lineexsetdefaultcapabilitypreferrence-method"></a>IH323LineEx::SetDefaultCapabilityPreferrence-Methode

\[**SetDefaultCapabilityPreferrence** ist nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die RTC-Client-API bietet ähnliche Funktionen.\]

Die **SetDefaultCapabilityPreferrence-Methode** konfiguriert die Einstellung der Standardfunktionen. Funktionen haben eine Standardgewichtung von 100. Wenn die Anwendung eine höhere Gewichtung für eine Funktion angibt, hat sie während der H.245-Aushandlung eine höhere Priorität. Wenn die Anwendung die Gewichtung einer Funktion auf 0 fest legt, wird sie nicht in der H.245-Aushandlung verwendet.

Diese Methode ist kumulativ. Wenn diese Methode beispielsweise zuerst aufgerufen wird, um eine Funktion zu deaktivieren, und erneut aufgerufen wird, um eine andere zu deaktivieren, werden beide Funktionen als Ergebnis dieser beiden Aufrufe deaktiviert.

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

*dwNumCaps* \[ In\]
</dt> <dd>

Ein **DWORD-Wert,** der die Anzahl der mit dieser Methode festgelegten Funktionen enthält.

</dd> <dt>

*pCapabilities* \[ In\]
</dt> <dd>

Ein Array von Funktionen. Jedes Element des Arrays ist ein [**H245 \_ CAPABILITY-Wert.**](h245-capability.md)

</dd> <dt>

*pWeights* \[ In\]
</dt> <dd>

Ein Array von Gewichtungen, die den Funktionen zugeordnet sind.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Rückgabecode                                                                                   | Beschreibung                                                                                                                                                                                                                 |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Methode war erfolgreich.<br/>                                                                                                                                                                                                |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Es ist nicht genügend Arbeitsspeicher vorhanden, um den Vorgang durchzuführen.<br/>                                                                                                                                                             |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Der *pCapabilities-Parameter* ist **NULL,** oder der *pWeights-Parameter* **ist NULL,** oder *sowohl pCapabilities* als auch *pWeights* sind **NULL,** oder das pCapabilities-Array enthält ein ungültiges H.245-Funktionsobjekt.<br/> |
| <dl> <dt>**\_E-ZEIGER**</dt> </dl>     | Ein Element des *pWeights-Arrays* oder eines Elements des *pCapabilities-Arrays* kann nicht gelesen werden.<br/>                                                                                                                    |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|---------------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 3.0 oder höher<br/>                                                 |
| Header<br/>       | <dl> <dt>H323priv.h</dt> </dl> |
| Bibliothek<br/>      | <dl> <dt>Uuid.lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl>  |



 

 




