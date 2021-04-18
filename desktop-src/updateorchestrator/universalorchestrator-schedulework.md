---
title: IUniversalOrchestrator::ScheduleWork
description: Ruft Universal Orchestrator auf, um Arbeit zu planen.
ms.topic: method
ms.date: 01/14/2021
ms.openlocfilehash: 456df8f975114f7bdf750a0449f3bd98efcc3b2e
ms.sourcegitcommit: 9c8ddec1e955f181beecad0478c1fb79013b5e9d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/21/2021
ms.locfileid: "106361095"
---
# <a name="iuniversalorchestratorschedulework-method"></a>Iuniversalorchestrator:: schedulework-Methode

> [!NOTE] 
> Diese API gehört der universellen Orchestrator-API an.

Ermöglicht Clients, den universellen Orchestrator zu informieren, dass die Arbeit aussteht, und eine Binärdatei bereitzustellen, die von Universal Orchestrator aufgerufen wird, um die Update Arbeit zu einem späteren Zeitpunkt auszuführen.

Die Rückruf Binärdatei muss mit einem gültigen Microsoft-Zertifikat signiert werden, und der Aufrufer muss den schedulework-Aufruf aus dem System Kontext aufrufen.

## <a name="syntax"></a>Syntax

```C++
HRESULT ScheduleWork(
  LPCWSTR callerIdentifier,
  LPCWSTR cmdLine
  LPCWSTR startArg,
  LPCWSTR pauseArg);
```

## <a name="parameters"></a>Parameter

`callerIdentifier`

Eine eindeutige Zeichenfolge, die alle Aufrufe von diesem bestimmten Client identifiziert.

`cmdLine`

Der vollständige Pfad zur Rückruf Binärdatei, die von Universal Orchestrator aufgerufen wird, um Arbeit auszuführen.

`startArg`

Parameter, die an die Rückruf Binärdatei übergeben werden, um anzugeben, dass der Start angefordert wird

`pauseArg`

*(optional)* Parameter, die an die Rückruf Binärdatei übergeben werden, um anzugeben, dass die Pause angefordert wird

## <a name="return-value"></a>Rückgabewert
Wenn diese Methode erfolgreich ausgeführt wird, wird **S_OK** zurückgegeben.  Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="requirements"></a>Anforderungen

| Anforderung | Version |
|---|---|
| Unterstützte Mindestversion (Client) | Windows 10 1903 |
|   |   |



 

 



