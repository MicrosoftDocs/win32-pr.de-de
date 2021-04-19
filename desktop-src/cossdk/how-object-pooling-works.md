---
description: Wenn Sie eine Komponente so konfigurieren, dass Sie in einem Pool zusammengefasst wird, verwaltet com+ Instanzen, die für jeden Client aktiviert werden können, der die Komponente anfordert. Alle Anforderungen zur Objekt Erstellung werden über den Pool-Manager verarbeitet.
ms.assetid: 34978b50-cd20-42fd-ad46-410190478ef8
title: Funktionsweise des Objekt Pooling
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f78784fc0e5362c14ceb598b404976c6ca494a19
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346227"
---
# <a name="how-object-pooling-works"></a>Funktionsweise des Objekt Pooling

Wenn Sie eine Komponente so konfigurieren, dass Sie in einem Pool zusammengefasst wird, verwaltet com+ Instanzen, die für jeden Client aktiviert werden können, der die Komponente anfordert. Alle Anforderungen zur Objekt Erstellung werden über den Pool-Manager verarbeitet.

Pools werden pro Komponente konfiguriert und verwaltet. Ein Pool besteht aus homogenen Objekten, die dieselbe CLSID gemeinsam verwenden. Die einzige Ausnahme ist bei Transaktions Objekten, bei denen unter Pools verwaltet werden, die Objekte enthalten, die Transaktions Affinität aufweisen, während eine Transaktion aussteht.

Wenn die Anwendung gestartet wird, wird der Pool auf die minimale Ebene aufgefüllt, die Sie administrativ angegeben haben, solange die Objekt Erstellung erfolgreich ist. Wenn Client Anforderungen für die Komponente eingehen, werden Sie bei der ersten bereitgestellten Basis aus dem Pool erfüllt. Wenn keine in einem Pool zusammengefassten Objekte verfügbar sind und sich der Pool noch nicht auf der angegebenen maximalen Ebene befindet, wird ein neues Objekt erstellt und für den Client aktiviert.

Wenn die maximale Ebene des Pools erreicht wird, werden Client Anforderungen in die Warteschlange eingereiht und empfangen das erste verfügbare Objekt aus dem Pool. Die Anzahl der Objekte, einschließlich aktivierter und deaktivierter Objekte, überschreitet niemals den maximalen poolwert. Bei Objekt Erstellungs Anforderungen tritt nach einem administrativ angegebenen Zeitraum ein Timeout auf, sodass Sie steuern können, wie lange Clients auf die Objekt Erstellung warten werden. Nach einem Timeout Fehler erhält der Client den Fehler E \_ Timeout von [**cokreateinstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance).

Nach Möglichkeit versucht com+, ein Objekt wieder zu verwenden, nachdem es von einem Client freigegeben wurde, bis der Pool seine maximale Stufe erreicht hat. Das Objekt ist für die Überwachung seines Zustands zuständig, um zu bestimmen, ob es wieder verwendet werden kann, und sollte einen entsprechenden Wert für [**IObjectControl:: CanBePooled**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-canbepooled)zurückgeben.

Wenn ein in einem Pool zusammengestelltes Objekt erstellt wird, wird es in ein größeres Objekt aggregiert, das die Lebensdauer des Objekts verwaltet. Das äußere Objekt ruft Methoden für [**IObjectControl**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontrol) zu den entsprechenden Zeitpunkten im Lebenszyklus des Objekts wie folgt auf:

-   Die [**Aktivierungs**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-activate) Methode wird immer dann aufgerufen, wenn das Objekt an einen Client zurückgegeben wird, der in einem bestimmten Kontext aktiviert ist.
-   Die [**Deaktivierungs Methode wird**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-deactivate) immer dann aufgerufen, wenn ein Objekt vom Client freigegeben wird, oder im Fall eines JIT-aktivierten Objekts, wenn es deaktiviert wird.
-   Die [**CanBePooled**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-canbepooled) -Methode wird immer dann aufgerufen, wenn ein Objekt an den allgemeinen Pool zurückgegeben wird. Wenn das-Objekt erkennt, dass sich eine wiederverwendbare Ressource in einem ungültigen Zustand befindet, sollte für diese Methode **false** zurückgegeben werden, und der Pool-Manager verwirft das-Objekt.

Ein Objekt muss [**IObjectControl**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontrol)nicht unbedingt implementieren. Wenn dies nicht der Fall ist, werden die Instanzen immer wieder verwendet, bis die maximale Pool Ebene erreicht wird.

Ausführliche Informationen zum Konfigurieren von Komponenten, die in einem Pool zusammengefasst werden sollen, finden Sie unter [Konfigurieren einer zu poolenden Komponente](configuring-a-component-to-be-pooled.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Com+-objektkonstruktorzeichenfolgen](com--object-constructor-strings.md)
</dt> <dt>

[Steuern der Objekt Lebensdauer und des Zustands](controlling-object-lifetime-and-state.md)
</dt> <dt>

[Verbessern der Leistung durch Objekt Pooling](improving-performance-with-object-pooling.md)
</dt> <dt>

[Pooling von transaktionalen Objekten](pooling-transactional-objects.md)
</dt> <dt>

[Anforderungen für in einem Pool Bare Objekte](requirements-for-poolable-objects.md)
</dt> </dl>

 

 
