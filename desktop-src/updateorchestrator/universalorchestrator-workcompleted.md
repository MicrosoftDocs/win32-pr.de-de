---
title: IUniversalOrchestrator::WorkCompleted
description: Ruft Universal Orchestrator auf, um anzugeben, dass die Arbeit abgeschlossen ist.
ms.topic: reference
ms.date: 01/14/2021
ms.openlocfilehash: e36a3ba744df807abbebc6332ac8433010afd667
ms.sourcegitcommit: 3cea99a2ed9579a94236fa7924abd6149db51a58
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/30/2021
ms.locfileid: "114991827"
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



 

 



