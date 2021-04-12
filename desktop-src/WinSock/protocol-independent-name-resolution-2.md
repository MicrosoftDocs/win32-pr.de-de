---
description: Protokoll unabhängige Namensauflösung und Windows Sockets (Winsock).
ms.assetid: f55219b9-1518-4b49-a0da-6a3fa025cca3
title: Auflösung von Protocol-Independent Namen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21cafed9759a4ca5431dafb230e7f09578ff1c75
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104343478"
---
# <a name="protocol-independent-name-resolution"></a>Auflösung von Protocol-Independent Namen

Beim Entwickeln einer Protokoll unabhängigen Client/Server-Anwendung gibt es zwei grundlegende Anforderungen in Bezug auf die Namensauflösung und Registrierung:

-   Die Fähigkeit der Server Hälfte der Anwendung (Dienst), Ihr vorhanden sein in einem oder mehreren Namespaces zu registrieren (oder für Sie zugänglich).
-   Die Fähigkeit der Client Anwendung, den Dienst innerhalb eines Namespace zu finden und das erforderliche Transportprotokoll und die Adressierungs Informationen abzurufen.

Für diejenigen, die an die Entwicklung von TCP/IP-basierten Anwendungen gewöhnt sind, kann dies anscheinend kaum mehr als die Suche nach einer Host Adresse und dann die Verwendung einer vereinbarten Portnummer bedeuten. Andere Netzwerk Schemas ermöglichen jedoch den Speicherort des Dienstanbieter, das Protokoll, das für den Dienst verwendet wird, und andere Attribute, die zur Laufzeit ermittelt werden. Die Windows Sockets 2-Schnittstelle übernimmt das in den Themen in diesem Abschnitt beschriebene Modell, um die umfangreiche Vielfalt der in vorhandenen namens Diensten gefundenen Funktionen zu unterstützen.

In diesem Abschnitt werden die Protokoll unabhängigen namens Auflösungs Funktionen beschrieben, die Winsock-Entwicklern zur Verfügung stehen. In der folgenden Liste werden die Themen in diesem Abschnitt beschrieben:

-   [Namens Auflösungs Modell](name-resolution-model-2.md)
-   [Zusammenfassung der namens Auflösungs Funktionen](summary-of-name-resolution-functions-2.md)
-   [Datenstrukturen für die Namensauflösung](name-resolution-data-structures-2.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Registrierung und Namensauflösung](registration-and-name-resolution-2.md)
</dt> </dl>

 

 



