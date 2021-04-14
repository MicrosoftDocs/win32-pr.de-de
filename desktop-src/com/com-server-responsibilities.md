---
title: Zuständigkeiten von com-Servern
description: Zuständigkeiten von com-Servern
ms.assetid: 9853bbf5-b989-45b7-8fa8-8cd2f0d48d3c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86b9d3104af80a7b2dca49dbbd5b55e66a613ee7
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "104391064"
---
# <a name="com-server-responsibilities"></a>Zuständigkeiten von com-Servern

Eine der wichtigsten Möglichkeiten für einen Client, einen Zeiger auf ein Objekt zu erhalten, besteht darin, dass der Client fragt, ob ein Server gestartet und eine Instanz des vom Server bereitgestellten Objekts erstellt und aktiviert werden soll. Es liegt in der Verantwortung des Servers, sicherzustellen, dass dies ordnungsgemäß erfolgt. Hierfür gibt es mehrere wichtige Teile.

Der Server muss Code für ein Klassenobjekt über eine Implementierung der [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory) -oder [**IClassFactory2**](/windows/desktop/api/OCIdl/nn-ocidl-iclassfactory2) -Schnittstelle implementieren.

Der Server muss seine CLSID in der Systemregistrierung auf dem Computer, auf dem er sich befindet, registrieren und die Möglichkeit haben, seinen Computer Speicherort auf anderen Systemen in einem Netzwerk zu veröffentlichen, damit Clients ihn anrufen können, ohne dass der Client den Standort des Servers kennen muss.

Der Server ist hauptsächlich für die Sicherheit verantwortlich. der Server bestimmt zum größten Teil, ob er einen Zeiger auf eines seiner Objekte auf einen Client bereitstellt.

Prozess interne Server müssen bestimmte Funktionen implementieren und exportieren, die es dem Client Prozess ermöglichen, Sie zu instanziieren.

In den folgenden Themen werden die Zuständigkeiten des COM-Servers ausführlich erläutert:

-   [Implementieren von IClassFactory](implementing-iclassfactory.md)
-   [Lizenzierung und IClassFactory2](licensing-and-iclassfactory2.md)
-   [Registrieren von com-Servern](registering-com-servers.md)
-   [Hilfshilfsprogramme für die Out-of-Process-Server Implementierung](out-of-process-server-implementation-helpers.md)
-   [GUID-Erstellung und-Optimierungen](guid-creation-and-optimizations.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[COM-Clients und-Server](com-clients-and-servers.md)
</dt> </dl>

 

 