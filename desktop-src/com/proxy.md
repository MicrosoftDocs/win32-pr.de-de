---
title: Proxy
description: Ein Proxy befindet sich im Adressraum des aufrufenden Prozesses und fungiert als Ersatz für das Remoteobjekt.
ms.assetid: 6c82f655-ac46-4ed9-992b-0387b324a8f9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c0478ce9ad1e08d343f1536fcd4bba63e59ae0fd229390be31c978bd20f737b4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119130006"
---
# <a name="proxy"></a>Proxy

Ein Proxy befindet sich im Adressraum des aufrufenden Prozesses und fungiert als Ersatz für das Remoteobjekt. Aus der Perspektive des aufrufenden Objekts ist der Proxy das -Objekt. In der Regel besteht die Rolle des Proxys darin, die Schnittstellenparameter für Aufrufe von Methoden in seinen Objektschnittstellen zu packen. Der Proxy packt die Parameter in einen Nachrichtenpuffer und übergibt den Puffer an den Kanal, der den Transport zwischen Prozessen verarbeitet. Der Proxy wird als Aggregatobjekt oder zusammengesetztes Objekt implementiert. Sie enthält ein vom System bereitgestelltes Manager-Element namens Proxy-Manager und eine oder mehrere schnittstellenspezifische Komponenten, die als Schnittstellenproxys bezeichnet werden. Die Anzahl der Schnittstellenproxys entspricht der Anzahl der Objektschnittstellen, die für diesen bestimmten Client verfügbar gemacht wurden. Für den Client, der das Komponentenobjektmodell erfüllt, scheint der Proxy das echte Objekt zu sein.

> [!Note]  
> Beim benutzerdefinierten Marshalling kann der Proxy auf ähnliche Weise implementiert werden, oder er kann direkt mit dem Objekt kommunizieren, ohne einen Stub zu verwenden.

 

Jeder Schnittstellenproxy ist ein Komponentenobjekt, das den Marshallingcode für eine der Schnittstellen des Objekts implementiert. Der Proxy stellt das Objekt dar, für das er Marshallingcode bereitstellt. Jeder Proxy implementiert auch die [**IRpcProxyBuffer-Schnittstelle.**](/windows/win32/api/objidlbase/nn-objidlbase-irpcproxybuffer) Obwohl die vom Proxy dargestellte Objektschnittstelle öffentlich ist, ist die **IRpcProxyBuffer-Implementierung** privat und wird intern innerhalb des Proxys verwendet. Der Proxy-Manager verfolgt die Schnittstellenproxys und enthält auch die öffentliche Implementierung der steuernden [**IUnknown-Schnittstelle**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) für das Aggregat. Jeder Schnittstellenproxy kann in einer separaten DLL vorhanden sein, die geladen wird, wenn die von ihm unterstützte Schnittstelle für den Client materialisiert wird.

## <a name="structure-of-the-proxy"></a>Struktur des Proxys

Das folgende Diagramm zeigt die Struktur eines Proxys, der das standardmäßige Marshalling von Parametern unterstützt, die zu zwei Schnittstellen gehören: IA1 und IA2. Jeder Schnittstellenproxy implementiert [**IRpcProxyBuffer**](/windows/win32/api/objidlbase/nn-objidlbase-irpcproxybuffer) für die interne Kommunikation zwischen den Aggregatteilen. Wenn der Proxy bereit ist, seine gemarshallten Parameter über die Prozessgrenze zu übergeben, ruft er Methoden in der [**IRpcChannelBuffer-Schnittstelle**](/windows/win32/api/objidlbase/nn-objidlbase-irpcchannelbuffer) auf, die vom Kanal implementiert wird. Der Kanal leitet wiederum den Aufruf der RPC-Laufzeitbibliothek weiter, damit sie ihr Ziel im -Objekt erreichen kann.

![Diagramm, das die Struktur des Proxys zeigt.](images/4432d8d3-dfab-4635-90f8-408aecf70134.png)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Kanal](channel.md)
</dt> <dt>

[Objektübergreifende Kommunikation](inter-object-communication.md)
</dt> <dt>

[Marshallingdetails](marshaling-details.md)
</dt> <dt>

[Microsoft RPC](microsoft-rpc.md)
</dt> <dt>

[Stub](stub.md)
</dt> </dl>

 

 