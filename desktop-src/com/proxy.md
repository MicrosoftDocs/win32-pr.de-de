---
title: Proxy
description: Ein Proxy befindet sich im Adressraum des aufrufenden Prozesses und fungiert als Ersatz für das Remote Objekt.
ms.assetid: 6c82f655-ac46-4ed9-992b-0387b324a8f9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a11257dd060f51bef118a4afc0cc35acf995c111
ms.sourcegitcommit: d39e82e232f6510f843fdb8d55d25b4e9e02e880
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/03/2021
ms.locfileid: "106361101"
---
# <a name="proxy"></a>Proxy

Ein Proxy befindet sich im Adressraum des aufrufenden Prozesses und fungiert als Ersatz für das Remote Objekt. Aus der Perspektive des aufrufenden Objekts ist der Proxy das-Objekt. In der Regel besteht die Rolle des Proxys darin, die Schnittstellenparameter für Aufrufe von Methoden in seinen Objekt Schnittstellen zu verpacken. Der Proxy verpackt die Parameter in einem Nachrichten Puffer und übergibt den Puffer an den Kanal, der den Transport zwischen Prozessen verarbeitet. Der Proxy wird als Aggregat-oder zusammengesetztes Objekt implementiert. Es enthält ein vom System bereitgestelltes Manager-Element, das als Proxy Manager und eine oder mehrere Schnittstellen spezifische Komponenten bezeichnet wird, die als Schnittstellen Proxys bezeichnet werden Die Anzahl der Schnittstellen Proxys entspricht der Anzahl von Objekt Schnittstellen, die für diesen bestimmten Client verfügbar gemacht wurden. Für den Client, der das Komponentenobjektmodell erfüllt, scheint der Proxy das echte Objekt zu sein.

> [!Note]  
> Mit benutzerdefiniertem Marshalling kann der Proxy ähnlich implementiert werden, oder er kann direkt mit dem Objekt kommunizieren, ohne einen Stub zu verwenden.

 

Jeder Schnittstellen Proxy ist ein Komponenten Objekt, das den Marshallingcode für eine der Schnittstellen des-Objekts implementiert. Der Proxy stellt das Objekt dar, für das es Marshallingcode bereitstellt. Jeder Proxy implementiert auch die Schnittstelle " [**iripcproxybuffer**](/windows/win32/api/objidlbase/nn-objidlbase-irpcproxybuffer) ". Obwohl die vom Proxy dargestellte Objektschnittstelle öffentlich ist, ist die Implementierung von " **typcproxybuffer** " Privat und wird intern innerhalb des Proxys verwendet. Der Proxy-Manager verfolgt die Schnittstellen Proxys und enthält auch die öffentliche Implementierung der kontrollierten [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) -Schnittstelle für das Aggregat. Jeder Schnittstellen Proxy kann in einer separaten dll vorhanden sein, die geladen wird, wenn die Schnittstelle, die er unterstützt, auf den Client materialisiert wird.

## <a name="structure-of-the-proxy"></a>Struktur des Proxys

Das folgende Diagramm zeigt die Struktur eines Proxys, der das Standardmarshalling von Parametern unterstützt, die zu zwei Schnittstellen gehören: IA1 und IA2. Jeder Schnittstellen Proxy implementiert " [**iripcproxybuffer**](/windows/win32/api/objidlbase/nn-objidlbase-irpcproxybuffer) " für die interne Kommunikation zwischen den Aggregat teilen. Wenn der Proxy bereit ist, seine gemarshallten Parameter über die Prozess Grenze hinweg zu übergeben, ruft er Methoden in der Schnittstelle " [**iripcchannelbuffer**](/windows/win32/api/objidlbase/nn-objidlbase-irpcchannelbuffer) " auf, die vom Kanal implementiert wird. Der-Kanal leitet wiederum den Aufruf an die RPC-Lauf Zeit Bibliothek weiter, sodass er sein Ziel im-Objekt erreichen kann.

![Diagramm, das die Struktur des Proxys anzeigt.](images/4432d8d3-dfab-4635-90f8-408aecf70134.png)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Kanal](channel.md)
</dt> <dt>

[Kommunikation zwischen Objekten](inter-object-communication.md)
</dt> <dt>

[Marshalling von Details](marshaling-details.md)
</dt> <dt>

[Microsoft RPC](microsoft-rpc.md)
</dt> <dt>

[Stub](stub.md)
</dt> </dl>

 

 