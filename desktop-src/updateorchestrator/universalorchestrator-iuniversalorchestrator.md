---
title: IUniversalOrchestrator-Schnittstelle
description: Eine COM-Schnittstelle, die Methoden bereitstellt, mit denen ein Client mit dem universellen Orchestrator kommunizieren kann.
ms.date: 01/14/2021
ms.topic: reference
ms.openlocfilehash: f3635f76236eb6c7a11bfa62311003b7d76357a9fbacc9fde85f0bdffed0c129
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118966138"
---
# <a name="iuniversalorchestrator-interface"></a>IUniversalOrchestrator-Schnittstelle

> [!NOTE] 
> Diese API gehört zur Universal Orchestrator-API.

**IUniversalOrchestrator** ist eine COM-Schnittstelle, die die folgenden Methoden bereitstellt, um einem Client die Kommunikation mit dem universellen Orchestrator zu ermöglichen.

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