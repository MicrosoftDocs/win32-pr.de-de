---
description: Das com+-Anwendungs Pooling ermöglicht das Skalieren von Single Thread-Prozessen, ähnlich wie beim Thread Pooling das Skalieren von Single Thread-Objekten ermöglicht wird.
ms.assetid: 28bd13d9-ff5c-456e-ab98-d2ff3a499f1c
title: Konzepte für das com+-Anwendungs Pooling
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87a72f5681896e8ac0e6a50b3bddfc16cf4303f4
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103860875"
---
# <a name="com-application-pooling-concepts"></a>Konzepte für das com+-Anwendungs Pooling

Das com+-Anwendungs Pooling ermöglicht das Skalieren von Single Thread-Prozessen, ähnlich wie beim Thread Pooling das Skalieren von Single Thread-Objekten ermöglicht wird. Das Anwendungs Pooling kann auch zur Wiederherstellung nach Fehlern in einzelnen Prozessen beitragen, indem andere laufende Prozesse bereitgestellt werden, die Aktivierungen verarbeiten können.

> [!Note]  
> Bibliotheksanwendungen verfügen über die Eigenschaften zum wieder verwenden und zum Pooling Ihres Host Prozesses.

 

Alle Methoden der [**ICOMAdminCatalog2**](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog2) -Schnittstelle unterstützen das Anwendungs Pooling.

Das com+-Anwendungs Pooling kann pro Anwendung mithilfe der concurrentapps-Eigenschaft des [**COMAdminCatalogObject**](comadmincatalogobject.md) -Objekts in der [**Anwendungs**](applications.md) Auflistung konfiguriert werden. Concurrentapps ist ein ganzzahliger Wert, der die maximale Anzahl gleichzeitiger dllhost-Prozesse angibt, die gestartet werden sollten, um Aktivierungen für eine Anwendung zu warten. Diese Eigenschaft kann mithilfe des Verwaltungs Tools für Komponenten Dienste oder Programm gesteuert festgelegt werden.

Wenn die concurrentapps-Eigenschaft auf 1 festgelegt ist, was der Standardwert ist, wird der com+-anwendungspoolingdienst deaktiviert.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Com+-anwendungspoolingaufgaben](com--application-pooling-tasks.md)
</dt> <dt>

[Konzepte der com+-Anwendungs Wiederverwendung](com--application-recycling-concepts.md)
</dt> </dl>

 

 



