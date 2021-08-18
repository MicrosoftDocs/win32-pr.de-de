---
title: Microsoft RPC
description: Microsoft RPC
ms.assetid: a9ca629a-2766-43d5-89da-73d0628b3c5e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed515b1ca8e58e8e9daaa2bb037dbb9c33ad1d6bb15bd7dc42abd52771e8267a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119130172"
---
# <a name="microsoft-rpc"></a>Microsoft RPC

Microsoft RPC ist ein Modell für die Programmierung in einer verteilten Computingumgebung. Das Ziel von RPC ist es, eine transparente Kommunikation zu ermöglichen, damit der Client scheinbar direkt mit dem Server kommuniziert. Die Rpc-Implementierung von Microsoft ist mit dem RPC von Open Software Foundation (OSF) Distributed Computing Environment (DCE) kompatibel.

Sie können RPC so konfigurieren, dass mindestens ein Transport, ein oder mehrere Namensdienste und mindestens ein Sicherheitsserver verwendet werden. Die Schnittstellen zu diesen Anbietern werden von RPC verarbeitet. Da Microsoft RPC für die Verwendung mit mehreren Anbietern konzipiert ist, können Sie die Anbieter auswählen, die für Ihr Netzwerk am besten funktionieren. Der Transport ist für die Übertragung der Daten über das Netzwerk verantwortlich. Der Name-Dienst verwendet einen Objektnamen, z. B. einen Moniker, und findet seinen Speicherort im Netzwerk. Der Sicherheitsserver bietet Anwendungen die Möglichkeit, bestimmten Benutzern und/oder Gruppen den Zugriff zu verweigern. Ausführlichere [Informationen zur Anwendungssicherheit](interface-design-rules.md) finden Sie unter Schnittstellenentwurfsregeln.

Zusätzlich zu den RPC-Laufzeitbibliotheken enthält Microsoft RPC die Interface Definition Language (IDL) und deren Compiler. Obwohl die IDL-Datei ein Standardteil von RPC ist, hat Microsoft sie erweitert, um ihre Funktionalität zur Unterstützung benutzerdefinierter COM-Schnittstellen zu erweitern. Der Microsoft Interface Definition Language(MIDL)-Compiler verwendet die IDL-Datei, die Ihre benutzerdefinierte Schnittstelle beschreibt, um mehrere Dateien zu generieren, die unter Erstellen und Registrieren einer [Proxy-DLL erläutert werden.](building-and-registering-a-proxy-dll.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Kanal](channel.md)
</dt> <dt>

[Objektübergreifende Kommunikation](inter-object-communication.md)
</dt> <dt>

[Marshallingdetails](marshaling-details.md)
</dt> <dt>

[Proxy](proxy.md)
</dt> <dt>

[Stub](stub.md)
</dt> </dl>

 

 




