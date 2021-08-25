---
description: Wenn Sie eine Komponente für das Pooling konfigurieren, verwaltet COM+ Instanzen dieser Komponente in einem Pool, die für jeden Client aktiviert werden können, der die Komponente an fordert. Alle Objekterstellungsanforderungen werden über den Pool-Manager verarbeitet.
ms.assetid: 34978b50-cd20-42fd-ad46-410190478ef8
title: Funktionsweise von Objektpooling
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df937dd8e3d7a2fb111c7825df101cd2b53f6f39a94326efb1eafe878d74daa6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119954040"
---
# <a name="how-object-pooling-works"></a>Funktionsweise von Objektpooling

Wenn Sie eine Komponente für das Pooling konfigurieren, verwaltet COM+ Instanzen dieser Komponente in einem Pool, die für jeden Client aktiviert werden können, der die Komponente an fordert. Alle Objekterstellungsanforderungen werden über den Pool-Manager verarbeitet.

Pools werden pro Komponente konfiguriert und verwaltet. Ein Pool besteht aus homogenen Objekten, die dieselbe CLSID verwenden. Die einzige Ausnahme gilt für Transaktionsobjekte, für die Unterpools verwaltet werden, die Objekte enthalten, die transaktionsaffin sind, während eine Transaktion aussteht.

Wenn die Anwendung gestartet wird, wird der Pool bis zur minimalen Ebene aufgefüllt, die Sie administratorisch angegeben haben, solange die Objekterstellung erfolgreich ist. Wenn Clientanforderungen für die Komponente ins Spiel kommen, werden sie vom Pool aus zuerst erfüllt. Wenn keine Inpoolobjekte verfügbar sind und der Pool noch nicht die angegebene maximale Ebene erreicht hat, wird ein neues -Objekt für den Client erstellt und aktiviert.

Wenn der Pool die maximale Ebene erreicht, werden Clientanforderungen in die Warteschlange gestellt und erhalten das erste verfügbare Objekt aus dem Pool. Die Anzahl der Objekte, einschließlich aktivierter und deaktivierter Objekte, überschreitet nie den maximalen Poolwert. Bei Objekterstellungsanforderungen kommt es nach einem von der Verwaltung festgelegten Zeitraum zu einem Time out, sodass Sie steuern können, wie lange Clients auf die Objekterstellung warten. Bei einem Timeoutfehler wird dem Client der Fehler E \_ TIMEOUT von [**CoCreateInstance zurückgegeben.**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance)

Nach Möglichkeit versucht COM+, ein Objekt wiederzuverwenden, nachdem ein Client es wiederverwendet hat, bis der Pool seine maximale Ebene erreicht. Das -Objekt ist für die Überwachung seines Zustands verantwortlich, um zu bestimmen, ob es wiederverwendet werden kann, und sollte einen entsprechenden Wert für [**IObjectControl::CanBePooled zurückgeben.**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-canbepooled)

Wenn ein in einem Pool zusammengefasstes Objekt erstellt wird, wird es zu einem größeren Objekt aggregiert, das die Lebensdauer des Objekts verwaltet. Das äußere Objekt ruft Methoden für [**IObjectControl**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontrol) zu geeigneten Zeitpunkten im Lebenszyklus des Objekts wie folgt auf:

-   Die [**Activate-Methode**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-activate) wird immer dann aufgerufen, wenn das Objekt an einen Client zurückgegeben und in einem bestimmten Kontext aktiviert wird.
-   Die [**Deactivate-Methode**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-deactivate) wird immer dann aufgerufen, wenn ein Objekt vom Client freigegeben oder bei einem JIT-aktivierten Objekt deaktiviert wird.
-   Die [**CanBePooled-Methode**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-canbepooled) wird immer dann aufgerufen, wenn ein Objekt an den allgemeinen Pool zurückgegeben werden soll. Wenn das Objekt erkennt, dass sich eine wiederverwendbare Ressource in einem fehlerhaften Zustand befindet, sollte es **false** für diese Methode zurückgeben, und der Pool-Manager verwirft das Objekt.

Ein Objekt muss nicht notwendigerweise [**IObjectControl implementieren.**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontrol) Wenn dies nicht der Fall ist, werden Instanzen immer wiederverwendet, bis die maximale Poolebene erreicht ist.

Weitere Informationen zum Konfigurieren von Komponenten, die in einem Pool enthalten sein sollen, finden Sie unter [Configuring a Component to Be Pooled](configuring-a-component-to-be-pooled.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[COM+-Objektkonstruktorzeichenfolgen](com--object-constructor-strings.md)
</dt> <dt>

[Steuern der Objektlebensdauer und des Zustands](controlling-object-lifetime-and-state.md)
</dt> <dt>

[Verbessern der Leistung mit Objektpooling](improving-performance-with-object-pooling.md)
</dt> <dt>

[Pooling von Transaktionsobjekten](pooling-transactional-objects.md)
</dt> <dt>

[Anforderungen für poolfähige Objekte](requirements-for-poolable-objects.md)
</dt> </dl>

 

 
