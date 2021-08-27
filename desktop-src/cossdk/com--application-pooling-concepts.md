---
description: Com+-Anwendungspooling ermöglicht die Skalierung von Singlethreadprozessen, ähnlich wie beim Threadpooling singlethreaded-Objekte skaliert werden können.
ms.assetid: 28bd13d9-ff5c-456e-ab98-d2ff3a499f1c
title: COM+-Anwendungspoolingkonzepte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9aab46350e3c6084c0d5e8ca61d2f3c90d27e06795f7d08568ee4a7c1e0fc26
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120096910"
---
# <a name="com-application-pooling-concepts"></a>COM+-Anwendungspoolingkonzepte

Com+-Anwendungspooling ermöglicht die Skalierung von Singlethreadprozessen, ähnlich wie beim Threadpooling singlethreaded-Objekte skaliert werden können. Anwendungspooling kann auch bei der Wiederherstellung nach Fehlern in einzelnen Prozessen helfen, indem andere ausgeführte Prozesse zur Verfügung gestellt werden, die Aktivierungen verarbeiten können.

> [!Note]  
> Bibliotheksanwendungen verfügen über die Wiederverwendungs- und Poolingeigenschaften ihres Hostprozesses.

 

Alle Methoden der [**ICOMAdminCatalog2-Schnittstelle**](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog2) unterstützen Anwendungspooling.

COM+-Anwendungspooling kann pro Anwendung konfiguriert werden, indem die ConcurrentApps-Eigenschaft des [**COMAdminCatalogObject-Objekts**](comadmincatalogobject.md) in der [**Applications-Sammlung**](applications.md) verwendet wird. ConcurrentApps ist ein ganzzahliger Wert, der die maximale Anzahl gleichzeitiger Dllhost-Prozesse angibt, die für die Dienstaktivierung für eine Anwendung gestartet werden sollen. Diese Eigenschaft kann mithilfe des Component Services-Verwaltungstools oder programmgesteuert festgelegt werden.

Wenn die ConcurrentApps-Eigenschaft auf 1 (Standardwert) festgelegt ist, ist der COM+-Anwendungspoolingdienst deaktiviert.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[COM+-Anwendungspoolingtasks](com--application-pooling-tasks.md)
</dt> <dt>

[KONZEPTE DER COM+-Anwendungswiederverwendung](com--application-recycling-concepts.md)
</dt> </dl>

 

 



