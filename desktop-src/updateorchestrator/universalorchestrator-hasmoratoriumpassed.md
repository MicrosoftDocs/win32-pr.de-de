---
title: IUniversalOrchestrator::HasMoratoriumPassed
description: Fragt den universellen Orchestrator ab, um zu ermitteln, ob der Zeitraum nach der OOBE überschritten wurde.
ms.topic: reference
ms.date: 01/14/2021
ms.openlocfilehash: 61870e1bd57f54afded3f905da34ddc9198bcdb555c42adc4c799e08f2acf392
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118966127"
---
# <a name="iuniversalorchestratorhasmoratoriumpassed-method"></a>IUniversalOrchestrator::HasMfangPassed-Methode

> [!NOTE] 
> Diese API gehört zur Universal Orchestrator-API.

Ermöglicht Clients, zu bestimmen, ob Universal Orchestrator unmittelbar nach der neuen Out-of-Box-Benutzeroberfläche des Geräts ausgeführt wird. Dies schränkt Arbeitsversuche ein, um Benutzerunterbrechungen zu minimieren. 

## <a name="syntax"></a>Syntax

```C++
HRESULT HasMoratoriumPassed(
  LPCWSTR callerIdentifier,
  BOOL*   moratoriumPassed);
```

## <a name="parameters"></a>Parameter

`callerIdentifier`

Eine eindeutige Zeichenfolge, die alle Aufrufe von diesem spezifischen Client identifiziert.

`hasMoratoriumPassed`

Ausgabeparameter, der das Ergebnis der Abfrage speichert.

## <a name="return-value"></a>Rückgabewert
Wenn diese Methode erfolgreich ist, wird **S_OK** zurückgegeben.  Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="requirements"></a>Anforderungen

| Anforderung | Version |
|---|---|
| Unterstützte Mindestversion (Client) | Windows 10 1903 |
|   |   |



 

 



