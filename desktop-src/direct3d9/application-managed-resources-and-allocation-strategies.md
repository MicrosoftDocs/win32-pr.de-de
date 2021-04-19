---
description: Verwaltete Vertex-Puffer-oder Index Puffer Ressourcen können nicht als dynamisch deklariert werden, indem D3DUSAGE \_ Dynamic zum Erstellungs Zeitpunkt angegeben wird.
ms.assetid: 440d9d94-3a56-4b34-a5e3-1b4712b078fc
title: Application-Managed Ressourcen und Zuordnungs Strategien (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e4f5ce23cac4bf46b8580a31d7c6d71fdc3de15
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343584"
---
# <a name="application-managed-resources-and-allocation-strategies-direct3d-9"></a>Application-Managed Ressourcen und Zuordnungs Strategien (Direct3D 9)

Verwaltete Vertex-Puffer-oder Index Puffer Ressourcen können nicht als dynamisch deklariert werden, indem D3DUSAGE \_ Dynamic zum Erstellungs Zeitpunkt angegeben wird. Dies erfordert eine zusätzliche Kopie für jede Änderung am Inhalt des Vertexpuffers. Dynamische Scheitelpunkt Puffer sind zum Rendern dynamischer Geometrie und aus Daten, die aus dem Binär Raum partitionierte Strukturen oder anderen sichtbaren Datenstrukturen abgerufen werden sollen. Dies kann erreicht werden, indem Puffer im gewünschten Format vorab zugeordnet werden. Diese Ressourcen werden dann zur Unterstützung von Anwendungsanforderungen durch einen Ressourcen-Manager innerhalb der Anwendung verarbeitet. Die Gesamtanzahl dynamischer Scheitelpunkt Puffer ist klein, weil eine Anwendung gleichzeitig nur ein paar unterschiedliche Scheitel Punkte verwendet, und weil ein anderer Scheitelpunkt Puffer nur für eindeutige Schritte erforderlich ist. Wenn Sie dynamische Ressourcen auf diese Weise verwalten, stellen Sie sicher, dass die Leistung der Anwendung durch hoch frequente Anforderungen an die Ressourcen nicht erheblich beeinträchtigt wird.

Wenn Sie Ressourcen verwenden, die von Direct3D und Anwendungen verwaltet werden, sollten Sie von der Anwendung verwaltete Ressourcen im D3DPOOL \_ -Standard Speicher zuordnen, bevor Sie von Direct3D verwaltete Ressourcen erstellen. Dadurch kann der Speicher-Manager eine genaue Anzahl von verfügbarem Arbeitsspeicher beibehalten.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Direct3D-Ressourcen](direct3d-resources.md)
</dt> </dl>

 

 



