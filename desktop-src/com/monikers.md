---
title: Moniker
description: Ein Moniker in com ist nicht nur eine Möglichkeit zum Identifizieren eines Objekts \ 8212; ein Moniker wird auch als Objekt implementiert.
ms.assetid: ae0cd2f3-8ac0-4388-8781-e86fc4a26b3b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf148d63611b5252eec9f5f5f69eacbcece8c65f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036395"
---
# <a name="monikers"></a>Moniker

Ein Moniker in com ist nicht nur eine Möglichkeit, ein Objekt zu identifizieren – ein Moniker wird auch als Objekt implementiert. Dieses Objekt stellt Dienste bereit, mit denen eine Komponente einen Zeiger auf das vom Moniker identifizierte Objekt abrufen kann. Dieser Vorgang wird als *Bindung* bezeichnet.

Moniker sind Objekte, die die [**IMoniker**](/windows/desktop/api/ObjIdl/nn-objidl-imoniker) -Schnittstelle implementieren und im Allgemeinen in DLLs als Komponenten Objekte implementiert werden. Es gibt zwei Möglichkeiten, die Verwendung von Monikern anzuzeigen: als monikerclient, eine Komponente, die einen Moniker verwendet, um einen Zeiger auf ein anderes Objekt zu erhalten. und als monikeranbieter eine Komponente, die Moniker bereitstellt, die ihre Objekte an monikerclients identifizieren.

OLE verwendet Moniker, um Verbindungen mit Objekten herzustellen und Sie zu aktivieren, unabhängig davon, ob Sie sich auf demselben Computer oder über ein Netzwerk befinden. Eine sehr wichtige Verwendung ist für Netzwerkverbindungen. Sie werden auch zum identifizieren, verbinden und Ausführen von OLE-Verbund Dokumenten Verknüpfungs Objekten verwendet. In diesem Fall fungiert die Link Quelle als monikeranbieter, und der Container, der das Link Objekt enthält, fungiert als monikerclient.

Weitere Informationen finden Sie unter den folgenden Themen:

-   [Monikerclients](moniker-clients.md)
-   [Monikeranbieter](moniker-providers.md)
-   [OLE-Monikerimplementierungen](ole-moniker-implementations.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Das Component Object Model](the-component-object-model.md)
</dt> </dl>

 

 




