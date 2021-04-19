---
title: IUniversalOrchestrator::HasMoratoriumPassed
description: Fragt den universellen Orchestrator ab, um zu bestimmen, ob der Post-OOBE-Zeitraum überschritten wurde.
ms.topic: method
ms.date: 01/14/2021
ms.openlocfilehash: 2ed354d365b795a0c959396e6b26d6bc73baad97
ms.sourcegitcommit: 9c8ddec1e955f181beecad0478c1fb79013b5e9d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/21/2021
ms.locfileid: "106349744"
---
# <a name="iuniversalorchestratorhasmoratoriumpassed-method"></a>Iuniversalorchestrator:: hasmoratoriumbestandene-Methode

> [!NOTE] 
> Diese API gehört der universellen Orchestrator-API an.

Ermöglicht Clients festzustellen, ob universelle Orchestrator unmittelbar nach der Out-of-Box-Obergrenze des neuen Geräts betrieben wird, was die Arbeit bei der Minimierung von Benutzer Unterbrechungen einschränkt. 

## <a name="syntax"></a>Syntax

```C++
HRESULT HasMoratoriumPassed(
  LPCWSTR callerIdentifier,
  BOOL*   moratoriumPassed);
```

## <a name="parameters"></a>Parameter

`callerIdentifier`

Eine eindeutige Zeichenfolge, die alle Aufrufe von diesem bestimmten Client identifiziert.

`hasMoratoriumPassed`

Ausgabeparameter, der das Ergebnis der Abfrage speichert.

## <a name="return-value"></a>Rückgabewert
Wenn diese Methode erfolgreich ausgeführt wird, wird **S_OK** zurückgegeben.  Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="requirements"></a>Anforderungen

| Anforderung | Version |
|---|---|
| Unterstützte Mindestversion (Client) | Windows 10 1903 |
|   |   |



 

 



