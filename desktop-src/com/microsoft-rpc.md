---
title: Microsoft RPC
description: Microsoft RPC
ms.assetid: a9ca629a-2766-43d5-89da-73d0628b3c5e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53be9d46368ae01aee25815327aafeaf7f44525b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103707253"
---
# <a name="microsoft-rpc"></a>Microsoft RPC

Microsoft RPC ist ein Modell für die Programmierung in einer verteilten Computerumgebung. Das Ziel von RPC besteht darin, eine transparente Kommunikation bereitzustellen, sodass der Client scheinbar direkt mit dem Server kommuniziert. Die Microsoft-Implementierung von RPC ist mit dem DCE-RPC (Open Software Foundation) der verteilten Rechen Umgebung (natürlich) kompatibel.

Sie können RPC so konfigurieren, dass ein oder mehrere Transporte, mindestens ein Namensdienst und ein oder mehrere Sicherheitsserver verwendet werden. Die Schnittstellen zu diesen Anbietern werden von RPC verarbeitet. Da Microsoft RPC für die Zusammenarbeit mit mehreren Anbietern konzipiert ist, können Sie die Anbieter auswählen, die für Ihr Netzwerk am besten geeignet sind. Der Transport ist dafür verantwortlich, die Daten über das Netzwerk zu übertragen. Der Namensdienst nimmt einen Objektnamen, z. b. einen Moniker, auf und findet seinen Speicherort im Netzwerk. Der Sicherheitsserver bietet Anwendungen die Möglichkeit, den Zugriff auf bestimmte Benutzer und/oder Gruppen zu verweigern. Ausführlichere Informationen zur Anwendungssicherheit finden Sie unter [Schnittstellen Entwurfs Regeln](interface-design-rules.md) .

Zusätzlich zu den RPC-Laufzeitbibliotheken enthält Microsoft RPC die IDL (Interface Definition Language) und den zugehörigen Compiler. Obwohl die IDL-Datei ein Standard Teil von RPC ist, hat Microsoft Sie erweitert, um ihre Funktionalität zur Unterstützung benutzerdefinierter COM-Schnittstellen zu erweitern. Der Microsoft Interface Definition Language (mittlerer l)-Compiler verwendet die IDL-Datei, die die benutzerdefinierte Schnittstelle beschreibt, um mehrere Dateien zu generieren, die unter [Erstellen und Registrieren einer Proxy-dll](building-and-registering-a-proxy-dll.md)erläutert werden

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Kanal](channel.md)
</dt> <dt>

[Kommunikation zwischen Objekten](inter-object-communication.md)
</dt> <dt>

[Marshalling von Details](marshaling-details.md)
</dt> <dt>

[Proxy](proxy.md)
</dt> <dt>

[Stub](stub.md)
</dt> </dl>

 

 




