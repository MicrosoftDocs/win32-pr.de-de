---
title: Erstellen eines Objekts über ein Klassenobjekt
description: Erstellen eines Objekts über ein Klassenobjekt
ms.assetid: cecf21b0-e509-425f-8dd6-ca6b1ac04f5e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ea76e8ecb826d8bba6e9f0ea84af894f4632d3d4bb5f41708d84c2f37e416b4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119993500"
---
# <a name="creating-an-object-through-a-class-object"></a>Erstellen eines Objekts über ein Klassenobjekt

Mit der zunehmenden Bedeutung von Computernetzwerken ist es erforderlich geworden, dass Clients und Server einfach und effizient interagieren, unabhängig davon, ob sie sich auf demselben Computer oder über ein Netzwerk befinden. Entscheidend ist die Fähigkeit eines Clients, einen Server zu starten, eine Instanz des Serverobjekts zu erstellen und Zugriff auf die Methoden der Schnittstellen im Objekt zu haben.

COM stellt Erweiterungen für diesen grundlegenden COM-Prozess zur Verfügung, die ihn nahezu nahtlos über ein Netzwerk hinweg ermöglichen. Wenn ein Client in der Lage ist, den Server über seine CLSID zu identifizieren, ermöglicht der Aufruf von einigen einfachen Funktionen COM das Auffinden und Starten des Servers sowie das Aktivieren des Objekts. Mit Unterschlüsseln in der Registrierung können Remoteserver ihren Speicherort registrieren, sodass der Client diese Informationen nicht benötigt. Für Anwendungen, die Netzwerkfeatures nutzen möchten, ermöglichen die COM-Objekterstellungsfunktionen mehr Flexibilität und Effizienz.

Weitere Informationen finden Sie in den folgenden Themen:

-   [COM-Klassenobjekte und CLSIDs](com-class-objects-and-clsids.md)
-   [Suchen eines Remoteobjekts](locating-a-remote-object.md)
-   [Hilfsfunktionen für die Instanzerstellung](instance-creation-helper-functions.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[COM-Clients und -Server](com-clients-and-servers.md)
</dt> </dl>

 

 




