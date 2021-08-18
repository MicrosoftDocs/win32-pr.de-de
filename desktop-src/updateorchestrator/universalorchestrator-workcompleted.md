---
title: IUniversalOrchestrator::WorkCompleted
description: Ruft Universal Orchestrator auf, um anzugeben, dass die Arbeit abgeschlossen ist.
ms.topic: reference
ms.date: 01/14/2021
ms.openlocfilehash: 5094ae864b4df9a3dd53b90c3b7d099a206a0ad8db1d1176b603b5ba45ca8194
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118966074"
---
# <a name="iuniversalorchestratorworkcompleted-method"></a>IUniversalOrchestrator::WorkCompleted-Methode

> [!NOTE] 
> Diese API gehört zur Universal Orchestrator-API.

Ermöglicht Clients, Universal Orchestrator darüber zu informieren, dass die zuvor geplante Arbeit abgeschlossen wurde, und Rückrufe bis zum nächsten erfolgreichen ScheduleWork-Aufruf zu beenden, um Aufgaben durchzuführen.

## <a name="syntax"></a>Syntax

```C++
HRESULT WorkCompleted(
  LPCWSTR callerIdentifier,
  BOOL    workCompleted);
```

## <a name="parameters"></a>Parameter

`callerIdentifier`

Eine eindeutige Zeichenfolge, die alle Aufrufe von diesem bestimmten Client identifiziert.

`workCompleted`

**TRUE,** wenn die Arbeit erfolgreich abgeschlossen wurde. **Andernfalls FALSE,** wenn der Arbeitsversuch fehlgeschlagen ist und in Zukunft wiederholt werden soll. 

## <a name="return-value"></a>Rückgabewert
Wenn diese Methode erfolgreich ist, gibt **sie** S_OK.  Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="requirements"></a>Anforderungen

| Anforderung | Version |
|---|---|
| Unterstützte Mindestversion (Client) | Windows 10 1903 |
|   |   |



 

 



