---
title: IUniversalOrchestrator-Schnittstelle
description: Eine COM-Schnittstelle, die Methoden bereitstellt, mit denen ein Client mit dem universellen Orchestrator kommunizieren kann.
ms.date: 01/14/2021
ms.topic: interface
ms.openlocfilehash: 6fa5dfd9f7853159645fbe3b543c228450f4e1c4
ms.sourcegitcommit: 9c8ddec1e955f181beecad0478c1fb79013b5e9d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/21/2021
ms.locfileid: "106355690"
---
# <a name="iuniversalorchestrator-interface"></a>IUniversalOrchestrator-Schnittstelle

> [!NOTE] 
> Diese API gehört der universellen Orchestrator-API an.

**Iuniversalorchestrator** ist eine COM-Schnittstelle, die die folgenden Methoden bereitstellt, um einem Client die Kommunikation mit dem universellen Orchestrator zu ermöglichen.

## <a name="methods"></a>Methoden

|Methode | BESCHREIBUNG |
|---|---|
|[:: Schedulework](universalorchestrator-schedulework.md) | Registriert ausstehende Arbeit beim universellen Orchestrator. |
|[:: Workabgeschlossene](universalorchestrator-workcompleted.md) | Informiert den universellen Orchestrator, dass die gesamte Arbeit vollständig ist. |
|[:: Hasmoratoriumbestandene](universalorchestrator-hasmoratoriumpassed.md) | Fragt den universellen Orchestrator ab, um zu bestimmen, ob er unmittelbar nach dem neuen Gerät außerhalb des Felds funktioniert. |


## <a name="requirements"></a>Anforderungen

| Anforderung | Version |
|---|---|
| Unterstützte Mindestversion (Client) | Windows 10 1903 |
|   |   |