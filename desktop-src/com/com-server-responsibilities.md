---
title: COM-Serveraufgaben
description: COM-Serveraufgaben
ms.assetid: 9853bbf5-b989-45b7-8fa8-8cd2f0d48d3c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5c6604a8f42804867e797087ffb346fe69152cb84440d052560c3f40a42140c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119854770"
---
# <a name="com-server-responsibilities"></a>COM-Serveraufgaben

Eine der wichtigsten Möglichkeiten für einen Client, einen Zeiger auf ein Objekt zu erhalten, besteht im Bitten des Clients, einen Server zu starten und eine Instanz des vom Server bereitgestellten Objekts zu erstellen und zu aktivieren. Es liegt in der Verantwortung des Servers, sicherzustellen, dass dies ordnungsgemäß erfolgt. Dazu gibt es mehrere wichtige Teile.

Der Server muss Code für ein Klassenobjekt über eine Implementierung der [**IClassFactory-**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory) oder [**IClassFactory2-Schnittstelle**](/windows/desktop/api/OCIdl/nn-ocidl-iclassfactory2) implementieren.

Der Server muss seine CLSID in der Systemregistrierung auf dem Computer registrieren, auf dem er sich befindet, und hat darüber hinaus die Möglichkeit, seinen Computerstandort auf anderen Systemen in einem Netzwerk zu veröffentlichen, damit Clients sie aufrufen können, ohne dass der Client den Standort des Servers kennen muss.

Der Server ist in erster Linie für die Sicherheit verantwortlich. Das heißt, der Server bestimmt in den meisten Jahren, ob er einen Zeiger auf eines seiner Objekte für einen Client bereitstellen wird.

In-Process-Server sollten bestimmte Funktionen implementieren und exportieren, die es dem Clientprozess ermöglichen, sie zu instanziieren.

Die folgenden Themen beschreiben die Zuständigkeiten des COM-Servers:

-   [Implementieren von IClassFactory](implementing-iclassfactory.md)
-   [Lizenzierung und IClassFactory2](licensing-and-iclassfactory2.md)
-   [Registrieren von COM-Servern](registering-com-servers.md)
-   [Out-of-Process-Serverimplementierungshilfen](out-of-process-server-implementation-helpers.md)
-   [GUID-Erstellung und -Optimierungen](guid-creation-and-optimizations.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[COM-Clients und -Server](com-clients-and-servers.md)
</dt> </dl>

 

 