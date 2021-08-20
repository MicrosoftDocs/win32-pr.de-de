---
title: Übersicht über die UPnP-Architektur
description: Die UPnP-Architektur definiert die Peer-zu-Peer-Netzwerkkonnektivität intelligenter Geräte, Geräte und Steuerungspunkte.
ms.assetid: 09aba033-6229-4a55-9421-a7b967508bf4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5866d3e701f53e95225538655ca45d159fb7c5f67d00e3c46c97357c7a9ee6a7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118126453"
---
# <a name="overview-of-upnp-architecture"></a>Übersicht über die UPnP-Architektur

Die UPnP-Architektur definiert die Peer-zu-Peer-Netzwerkkonnektivität intelligenter Geräte, Geräte und [*Steuerungspunkte.*](c-gly.md) Es wurde entwickelt, um eine benutzerfreundliche, flexible, standardbasierte Konnektivität mit Ad-hoc-, verwalteten oder nicht verwalteten Netzwerken zu bieten, unabhängig davon, ob sich diese Netzwerke zu Hause befinden, kleine Unternehmen sind oder direkt an das Internet angeschlossen sind. Die UPnP-Architektur ist eine verteilte, offene Netzwerkarchitektur, die vorhandene TCP/IP- und Webtechnologien verwendet, um ein nahtloses Näherungsnetzwerk zu ermöglichen, zusätzlich zur Steuerung und Datenübertragung zwischen Netzwerkgeräten.

UPnP ist eine IP-basierte Protokollsammlung, die auf vorläufigen Versionen von Webdienstprotokollen wie XML und SIMPLE Object Access Protocol (SOAP) basiert. Mit UPnP kann ein Gerät dynamisch in ein Netzwerk eingebunden werden, eine IP-Adresse abrufen, seine Funktionen vermitteln und das Vorhandensein und die Funktionen anderer Geräte im Netzwerk ermitteln.

Ein UPnP-Gerät ist ein Container mit Diensten und geschachtelten Geräten. Beispielsweise kann ein VCR aus einem Bandtransportdienst, einem Tunerdienst und einem Uhrdienst bestehen. Verschiedene Kategorien von UPnP-Geräten werden verschiedenen Sätzen von Diensten und eingebetteten Geräten zugeordnet. Beispielsweise unterscheiden sich Dienste innerhalb eines VCR von denen in einem Drucker. Informationen zu den Diensten, die ein bestimmter Gerätetyp bereitstellen kann, werden in einem XML-Gerätebeschreibungsdokument erfasst, das das Gerät hostet. In der Gerätebeschreibung sind auch Eigenschaften wie Gerätename und Symbole aufgeführt, die dem Gerät zugeordnet sind. Microsoft hat die UPnP-Unterstützung erweitert, um die Integration in [PnP-X](/previous-versions/windows/desktop/fundisc/pnp-x) und [die Funktionsermittlung](/previous-versions/windows/desktop/fundisc/fd-portal)einzubeziehen.

Die UPnP-Architektur ist mehr als nur eine einfache Erweiterung des Plug & Play-Peripheriemodells. Es unterstützt keine Konfiguration, unsichtbare Netzwerke und automatische Ermittlung für eine Reihe von Gerätekategorien von einer Vielzahl von Anbietern. Dadurch kann ein Gerät dynamisch einem Netzwerk beitreten, eine IP-Adresse abrufen und seine Funktionen auf Anforderung übermitteln. Anschließend können andere Steuerungspunkte die Steuerungspunkt-API mit UPnP-Technologie verwenden, um mehr über das Vorhandensein und die Funktionen anderer Geräte zu erfahren. Ein Gerät kann ein Netzwerk reibungslos und automatisch verlassen, wenn es nicht mehr verwendet wird.

Was ist universell an der UPnP-Technologie?

-   Medien- und Geräteunabhängigkeit. Die UPnP-Technologie kann auf jedem Medium ausgeführt werden, einschließlich Telefonleitung, Stromleitung, Ethernet, RF und 1394.
-   Unabhängigkeit von der Plattform. Anbieter verwenden ein beliebiges Betriebssystem und jede Programmiersprache, um UPnP-basierte Produkte zu erstellen.
-   Internetbasierte Technologien. Die UPnP-Technologie basiert unter anderem auf IP, TCP, UDP, HTTP und XML.
-   UI-Steuerelement. Die UPnP-Architektur ermöglicht es dem Anbieter, die Benutzeroberfläche des Geräts und die Interaktion mithilfe des Browsers zu steuern.
-   Programmgesteuertes Steuerelement. Die UPnP-Architektur ermöglicht auch die programmgesteuerte Steuerung herkömmlicher Anwendungen.
-   Allgemeine Basisprotokolle. Anbieter stimmen basisprotokollsätzen pro Gerät zu.
-   Erweiterbar. Jedes UPnP-basierte Produkt kann über Mehrwertdienste verfügen, die von den einzelnen Herstellern auf der basisbasierten Gerätearchitektur basieren.

Die UPnP-Technologie ist weit reichend, da sie auf Heimnetzwerke, Näherungsnetzwerke und Netzwerke in kleinen Unternehmen und Kommerziellen Gebäuden ausgerichtet ist. Sie ermöglicht die Datenkommunikation zwischen zwei beliebigen Geräten unter dem Befehl eines beliebigen Steuergeräts im Netzwerk. Die UPnP-Technologie ist unabhängig von einem bestimmten Betriebssystem, einer Programmiersprache oder einem physischen Medium.

Microsoft stellt zwei APIs für die Arbeit mit UPnP-basierten Geräten bereit:

-   [Steuerungspunkt-API:](control-point-api.md) Stellt eine Reihe von COM-Schnittstellen bereit, mit denen Anwendungen UPnP-basierte Geräte suchen und steuern können.
-   [Gerätehost-API:](device-host-api.md) Stellt eine Reihe von COM-Schnittstellen bereit, mit denen Entwickler Kerngerätefunktionen schreiben und das Gerät beim Gerätehost registrieren können. Der Gerätehost verarbeitet die Ermittlungs-, Beschreibungs-, Steuerungs- und Ereignisteile der UPnP-basierten Gerätefunktionalität.

 

 