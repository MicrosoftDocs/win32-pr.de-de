---
title: IUniversalOrchestrator::ScheduleWork
description: Aufrufe von Universal Orchestrator zum Planen von Arbeiten
ms.topic: reference
ms.date: 01/14/2021
ms.openlocfilehash: bb2ecc67167e0651663856354a07ec86f985c664f1d2bccff98917adf72f054d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118966083"
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

Eine eindeutige Zeichenfolge, die alle Aufrufe von diesem spezifischen Client identifiziert.

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



 

 



