---
description: Namensauflösung und Registrierungsmodell für die Windows Sockets (Winsock) SPI.
ms.assetid: b173b63e-42c7-4f85-b55f-1f7b3bff7c4f
title: Namensauflösungsmodell für die SPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82f012a5c14a6dae9045b303ecb7c4e39f1d93d264285138d98c0e93274ef921
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119132113"
---
# <a name="name-resolution-model-for-the-spi"></a>Namensauflösungsmodell für die SPI

Bei der Entwicklung einer protokollunabhängigen Client-/Serveranwendung gibt es zwei grundlegende Anforderungen an die Namensauflösung und -registrierung:

-   Die Möglichkeit, dass die Serverhälfte der Anwendung (im Folgenden als Dienst bezeichnet) ihr Vorhandensein in einem oder mehr Namespaces registrieren kann (oder für die darauf zugegriffen werden kann).
-   Die Fähigkeit der Clientanwendung, den Dienst in einem Namespace zu finden und das erforderliche Transportprotokoll und Adressierungsinformationen zu erhalten.

Für diejenigen, die mit der Entwicklung von TCP/IP-basierten Anwendungen vertraut sind, kann dies nur das Suchen einer Hostadresse und das anschließende Verwenden einer vereinbarten Portnummer umfassen. Andere Netzwerkschemas ermöglichen es jedoch, den Speicherort des Diensts, das für den Dienst verwendete Protokoll und andere Attribute zur Laufzeit zu finden. Um die Bandbreite der Funktionen in vorhandenen Namensdiensten zu unterstützen, übernimmt die Windows Sockets 2-Schnittstelle das unten beschriebene Modell.

Ein *Namespace* bezieht sich auf eine Funktion zum Zuordnen (mindestens) des Protokolls und der Adressierungsattribute eines Netzwerkdiensts zu mindestens einem benutzerfreundlichen Namen. Viele Namespaces werden derzeit verwendet, einschließlich der Domain Name System (DNS), NetWare-Verzeichnisdienste (NDS), X.500 usw. Diese Namespaces unterscheiden sich stark in ihrer Organisation und Ihrer Umsetzung. Einige ihrer Eigenschaften sind aus Der Perspektive der Socketsnamensauflösung Windows besonders wichtig zu verstehen.

 

 



