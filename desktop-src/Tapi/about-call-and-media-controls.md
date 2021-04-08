---
description: TAPI 3-und mediensteuer Elemente sind ein generischer Satz von COM-Objekten, Schnittstellen und Methoden zum Aufrufen von zwei oder mehr Computern.
ms.assetid: e345df2f-1b68-41be-ac2d-b771136ee831
title: Informationen zu den Steuerelementen "Callcenter"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae65d1a10d004cb16e0ba8753c27665cb7a30ff3
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "103869564"
---
# <a name="about-call-and-media-controls"></a>Informationen zu den Steuerelementen "Callcenter"

TAPI 3-und mediensteuer Elemente sind ein generischer Satz von COM-Objekten, Schnittstellen und Methoden zum Aufrufen von zwei oder mehr Computern. Im Zusammenhang mit TAPI 3 bezieht sich der *Anruf* nicht nur auf die Sprachübertragung über das Public-Switched-Telefon Netzwerk (PSTN), sondern auf alle Mittel-und Transportmechanismen, für die Dienstanbieter vorhanden sind, z. b. eine Multicast Konferenz für Multimedia, die auf einem Unternehmens Intranet ausgeführt wird.

Die fünf Hauptobjekte im TAPI 3-Aufruf und die Medien Steuerungsarchitektur sind [TAPI](tapi-object.md), [Address](address-object.md), [Terminal](terminal-object.md) [,](call-object.md) [callhub und callhub](callhub-object.md). Außerdem wurde Bereitstellung für [anbieterspezifische Schnittstellen](provider-specific-interfaces.md)vorgenommen.

Im folgenden Diagramm wird veranschaulicht, wie diese Objekte interagieren.

![Interaktionen zwischen TAPI 3,0-anrufen und Medien steuerungsobjekten](images/sdkobj2.png)

## <a name="features"></a>Features

-   Abstrahiert sowohl die Funktion zum Abrufen als auch der Medien, um unterschiedliche und scheinbar nicht kompatible Kommunikationsprotokolle zu ermöglichen und eine gemeinsame Schnittstelle
-   Basierend auf dem Component Object Model (com), sodass Anwendungen in nahezu jeder Sprache geschrieben werden können. Wenn Sie zusätzliche Informationen zu com benötigen, wenden Sie sich an das Platform Software Development Kit (SDK).
-   Die von Telefoniedienstanbietern (TSPS) bereitgestellte Telefon Steuerung, die Transport spezifische Mechanismen implementiert.
-   Mediensteuer Element, das von Media Service Providers (MSPs) bereitgestellt wird. Aktuelle MSPs verwenden DirectShow. DirectShow ist ein modulares System aus austauschbaren Komponenten, die als Filter bezeichnet werden und in einer Konfiguration mit dem Namen Filter Diagramm angeordnet sind. Der Filter Graph-Manager überwacht die Verbindung dieser Filter und steuert den Datenfluss des Streams. Wenn Sie weitere Informationen zu DirectShow benötigen, wenden Sie sich an das Platform SDK.

 

 



