---
title: IUniversalOrchestrator::ScheduleWork
description: Aufrufe von Universal Orchestrator zum Planen von Arbeiten
ms.topic: reference
ms.date: 01/14/2021
ms.openlocfilehash: 4c49d06a28497c33e86cc1e919fdb59f2363d1f5
ms.sourcegitcommit: 3cea99a2ed9579a94236fa7924abd6149db51a58
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/30/2021
ms.locfileid: "114991817"
---
# <a name="iuniversalorchestratorschedulework-method"></a>IUniversalOrchestrator::ScheduleWork-Methode

> [!NOTE] 
> Diese API gehört zur Universal Orchestrator-API.

Ermöglicht Clients, universal Orchestrator darüber zu informieren, dass die Arbeit aussteht, und stellt eine Binärdatei bereit, die von Universal Orchestrator aufgerufen wird, um die Aktualisierungsarbeiten zu einem späteren Zeitpunkt auszuführen.

Die Rückrufbinärdatei muss mit einem gültigen Microsoft-Zertifikat signiert werden, und der Aufrufer muss den ScheduleWork-Aufruf aus dem SYSTEM-Kontext aufrufen.

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

Der vollständige Pfad zur Rückrufbinärdatei, die von Universal Orchestrator aufgerufen wird, um Aufgaben auszuführen.

`startArg`

Parameter, die an die Rückrufbinärdatei übergeben werden sollen, um anzugeben, dass Start angefordert wird.

`pauseArg`

*(optional)* Parameter, die an die Rückrufbinärdatei übergeben werden sollen, um anzugeben, dass Pause angefordert wird.

## <a name="return-value"></a>Rückgabewert
Wenn diese Methode erfolgreich ist, wird **S_OK** zurückgegeben.  Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="requirements"></a>Anforderungen

| Anforderung | Version |
|---|---|
| Unterstützte Mindestversion (Client) | Windows 10 1903 |
|   |   |



 

 



