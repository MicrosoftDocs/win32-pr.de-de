---
title: IUniversalOrchestrator-Schnittstelle
description: Eine COM-Schnittstelle, die Methoden bereitstellt, mit denen ein Client mit dem universellen Orchestrator kommunizieren kann.
ms.date: 01/14/2021
ms.topic: reference
ms.openlocfilehash: 5dbbaafb38ab9d790d32beca9b014f933d5d53d5
ms.sourcegitcommit: 3cea99a2ed9579a94236fa7924abd6149db51a58
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/30/2021
ms.locfileid: "114991847"
---
# <a name="iuniversalorchestrator-interface"></a>IUniversalOrchestrator-Schnittstelle

> [!NOTE] 
> Diese API gehört zur Universal Orchestrator-API.

**IUniversalOrchestrator** ist eine COM-Schnittstelle, die die folgenden Methoden bereitstellt, um einem Client die Kommunikation mit dem universalen Orchestrator zu ermöglichen.

## <a name="methods"></a>Methoden

|Methode | BESCHREIBUNG |
|---|---|
|[::ScheduleWork](universalorchestrator-schedulework.md) | Registriert ausstehende Arbeit beim Universellen Orchestrator. |
|[::WorkCompleted](universalorchestrator-workcompleted.md) | Informiert den Universal Orchestrator, dass alle Arbeiten abgeschlossen sind. |
|[::HasMunterpassed](universalorchestrator-hasmoratoriumpassed.md) | Fragt den universellen Orchestrator ab, um zu ermitteln, ob er unmittelbar nach dem neuen Gerät ausgeführt wird. |


## <a name="requirements"></a>Anforderungen

| Anforderung | Version |
|---|---|
| Unterstützte Mindestversion (Client) | Windows 10 1903 |
|   |   |