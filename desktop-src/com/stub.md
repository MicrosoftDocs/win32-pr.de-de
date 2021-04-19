---
title: Stub
description: Der Stub besteht wie der Proxy aus einem oder mehreren Schnittstellen teilen und einem Manager.
ms.assetid: ed7d5546-2d19-4055-b078-62b39d0317b7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 109936ae16827dce7779b080902dbca74a8dfc51
ms.sourcegitcommit: d39e82e232f6510f843fdb8d55d25b4e9e02e880
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/03/2021
ms.locfileid: "106369916"
---
# <a name="stub"></a>Stub

Der Stub besteht wie der Proxy aus einem oder mehreren Schnittstellen teilen und einem Manager. Jeder schnittstellenstub stellt Code bereit, um die Parameter und den Code, der eine der unterstützten Schnittstellen des Objekts aufruft, zu entmarshalling. Jeder Stub stellt außerdem eine Schnittstelle für die interne Kommunikation bereit. Der Stub-Manager verfolgt die verfügbaren Schnittstellenstubs nach.

Es gibt jedoch die folgenden Unterschiede zwischen dem Stub und dem Proxy:

-   Der wichtigste Unterschied besteht darin, dass der Stub den Client im Adressraum des Objekts darstellt.
-   Der Stub wird nicht als Aggregat Objekt implementiert, weil es nicht erforderlich ist, dass der Client als einzelne Einheit angezeigt wird. jedes Element im Stub ist eine separate Komponente.
-   Die schnittstellenstubweisen sind privat und nicht öffentlich.
-   Die schnittstellenstubvorgänge implementieren " [**unpcstubbuffer**](/windows/win32/api/objidlbase/nn-objidlbase-irpcstubbuffer)", nicht " [**unpcproxybuffer**](/windows/win32/api/objidlbase/nn-objidlbase-irpcproxybuffer)".
-   Anstatt Parameter zu verpacken, die gemarshallt werden sollen, entpackt der Stub diese, nachdem Sie gemarshallt wurden, und verpackt dann die Antwort.

## <a name="structure-of-the-stub"></a>Struktur des Stubs

Das folgende Diagramm zeigt die Struktur des Stub. Jeder schnittstellenstub ist mit einer Schnittstelle für das Objekt verbunden. Der Kanal sendet eingehende Nachrichten an den entsprechenden schnittstellenstub. Alle Komponenten kommunizieren mit dem Kanal über " [**iripcchannelbuffer**](/windows/win32/api/objidlbase/nn-objidlbase-irpcchannelbuffer)", die Schnittstelle, die Zugriff auf die RPC-Lauf Zeit Bibliothek bietet.

![Screenshot, der die Struktur des Stubs anzeigt.](images/98714a22-733e-432f-bb90-408bbeecc23f.png)

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

[Proxy](proxy.md)
</dt> </dl>

 

 