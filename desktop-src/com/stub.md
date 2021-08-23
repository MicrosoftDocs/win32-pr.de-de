---
title: Stub
description: Der Stub besteht wie der Proxy aus einem oder mehr Schnittstellenteilen und einem Manager.
ms.assetid: ed7d5546-2d19-4055-b078-62b39d0317b7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f182cd2d47eec18f129d53d57c283d54862660a126d2d9e171989695418b3a8e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119678425"
---
# <a name="stub"></a>Stub

Der Stub besteht wie der Proxy aus einem oder mehr Schnittstellenteilen und einem Manager. Jeder Schnittstellenstub stellt Code zum Entmarten der Parameter und des Codes bereit, der eine der unterstützten Schnittstellen des Objekts aufruft. Jeder Stub stellt auch eine Schnittstelle für die interne Kommunikation bereit. Der Stub-Manager verfolgt die verfügbaren Schnittstellenstubs nach.

Es gibt jedoch die folgenden Unterschiede zwischen dem Stub und dem Proxy:

-   Der wichtigste Unterschied ist, dass der Stub den Client im Adressraum des Objekts darstellt.
-   Der Stub wird nicht als Aggregatobjekt implementiert, da der Client nicht als einzelne Einheit angezeigt werden muss. Jedes Element im Stub ist eine separate Komponente.
-   Die Schnittstellenstubs sind privat und nicht öffentlich.
-   Die Schnittstellenstubs implementieren [**IRpcStubBuffer**](/windows/win32/api/objidlbase/nn-objidlbase-irpcstubbuffer)und nicht [**IRpcProxyBuffer.**](/windows/win32/api/objidlbase/nn-objidlbase-irpcproxybuffer)
-   Anstatt Parameter zu packen, die gemarshallt werden sollen, entpackt der Stub sie, nachdem sie gemarshallt wurden, und packt dann die Antwort.

## <a name="structure-of-the-stub"></a>Struktur des Stubs

Das folgende Diagramm zeigt die Struktur des Stubs. Jeder Schnittstellenstub ist mit einer Schnittstelle im -Objekt verbunden. Der Kanal gibt eingehende Nachrichten an den entsprechenden Schnittstellenstub weiter. Alle Komponenten sprechen mit dem Kanal über [**IRpcChannelBuffer,**](/windows/win32/api/objidlbase/nn-objidlbase-irpcchannelbuffer)die Schnittstelle, die Zugriff auf die RPC-Laufzeitbibliothek bietet.

![Screenshot: Struktur des Stubs](images/98714a22-733e-432f-bb90-408bbeecc23f.png)

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

[Proxy](proxy.md)
</dt> </dl>

 

 