---
title: Übersicht über die UPnP-Architektur
description: Die UPnP-Architektur definiert die Peer-zu-Peer-Netzwerk Konnektivität von intelligenten Geräten, Geräten und Steuerungs Punkten.
ms.assetid: 09aba033-6229-4a55-9421-a7b967508bf4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10ce11009bfecfe03fa176c1e6c75be173fbde86
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103858391"
---
# <a name="overview-of-upnp-architecture"></a>Übersicht über die UPnP-Architektur

Die UPnP-Architektur definiert die Peer-zu-Peer-Netzwerk Konnektivität von intelligenten Geräten, Geräten und [*Steuerungs Punkten*](c-gly.md). Es wurde entwickelt, um benutzerfreundliche, flexible, auf Standards basierende Konnektivität mit Ad-hoc-, verwalteten oder nicht verwalteten Netzwerken zu bieten, unabhängig davon, ob sich diese Netzwerke in der Nähe oder in kleinen Unternehmen befinden oder direkt an das Internet angeschlossen sind. Die UPnP-Architektur ist eine verteilte, offene Netzwerkarchitektur, bei der vorhandene TCP/IP-und Webtechnologien verwendet werden, um nahtloses near Networking zusätzlich zur Steuerung und Datenübertragung zwischen vernetzten Geräten zu ermöglichen.

UPnP ist eine IP-basierte Protokoll Sammlung, die auf vorläufigen Versionen von Webdienst Protokollen wie XML und SOAP (Simple Object Access Protocol) basiert. Mit UPnP kann ein Gerät dynamisch einem Netzwerk beitreten, eine IP-Adresse abrufen, seine Funktion vermitteln und das vorhanden sein und die Funktionen anderer Geräte im Netzwerk ermitteln.

Bei einem UPnP-Gerät handelt es sich um einen Container für Dienste und geduckte Geräte. Ein VCR kann beispielsweise aus einem Band Transportdienst, einem Gatewaydienst und einem Takt Dienst bestehen. Unterschiedliche UPnP-Gerätekategorien sind mit unterschiedlichen Gruppen von Diensten und eingebetteten Geräten verknüpft. Beispielsweise unterscheiden sich die Dienste innerhalb eines VCR von denen innerhalb eines Druckers. Informationen zu den Diensten, die von einem bestimmten Gerätetyp bereitgestellt werden können, werden in einem XML-Geräte Beschreibungs Dokument aufgezeichnet, das das Gerät hostet. In der Geräte Beschreibung werden auch Eigenschaften wie der Gerätename und die dem Gerät zugeordneten Symbole aufgelistet. Microsoft verfügt über erweiterte UPnP-Unterstützung, um die Integration in die [PnP-X-](/previous-versions/windows/desktop/fundisc/pnp-x) und [Funktions](/previous-versions/windows/desktop/fundisc/fd-portal)Ermittlung einzubeziehen.

Die UPnP-Architektur ist mehr als nur eine einfache Erweiterung des Peripherie Modells für Plug-and-Play. Es unterstützt die Konfiguration mit nicht sichtbarem Netzwerk und die automatische Ermittlung für eine Reihe von Gerätekategorien von vielen Anbietern. Dadurch kann ein Gerät dynamisch einem Netzwerk beitreten, eine IP-Adresse abrufen und seine Fähigkeiten auf Anforderung übermitteln. Anschließend können andere Steuerungs Punkte die Steuerungspunkt-API mit der UPnP-Technologie verwenden, um mehr über das vorhanden sein und die Funktionen anderer Geräte zu erfahren. Ein Gerät kann ein Netzwerk reibungslos und automatisch verlassen, wenn es nicht mehr verwendet wird.

Was ist universell bei der UPnP-Technologie?

-   Medien-und Geräteunabhängigkeit. Die UPnP-Technologie kann auf jedem Medium ausgeführt werden, einschließlich Telefonleitung, netzwerkline, Ethernet, RF und 1394.
-   Unabhängigkeit von der Plattform. Anbieter verwenden jedes Betriebssystem und jede beliebige Programmiersprache, um UPnP-basierte Produkte zu erstellen.
-   Internet basierte Technologien. Die UPnP-Technologie basiert u.a. auf IP, TCP, UDP, http und XML.
-   UI-Steuerelement. Die UPnP-Architektur ermöglicht der Hersteller Kontrolle über Gerätebenutzer Oberfläche und Interaktion mithilfe des Browsers.
-   Programm gesteuertes Steuerelement Die UPnP-Architektur ermöglicht auch herkömmliche programmgesteuerte Anwendungssteuerung.
-   Allgemeine Basis Protokolle. Die Anbieter Stimmen für Basisprotokoll Sätze pro Gerät zu.
-   Erweiterbar. Auf jedem UPnP-basierten Produkt können von den einzelnen Herstellern durch einen Wert hinzugefügte Dienste oberhalb der grundlegenden Geräte Architektur angeordnet werden.

Die UPnP-Technologie ist umfangreich, da Sie sich auf Heimnetzwerke, near-Netzwerke und Netzwerke in kleinen Unternehmen und kommerziellen Gebäuden bezieht. Dadurch wird die Datenkommunikation zwischen zwei Geräten unter dem Befehl eines beliebigen Steuerungs Geräts im Netzwerk ermöglicht. Die UPnP-Technologie ist unabhängig von einem bestimmten Betriebssystem, einer Programmiersprache oder einem physischen Medium.

Microsoft stellt zwei APIs zum Arbeiten mit UPnP-basierten Geräten bereit:

-   [Steuerungspunkt-API](control-point-api.md) : stellt einen Satz von COM-Schnittstellen bereit, mit denen Anwendungen UPnP-basierte Geräte suchen und steuern können.
-   [Geräte Host-API](device-host-api.md) : stellt einen Satz von COM-Schnittstellen bereit, die es Entwicklern ermöglichen, kerngeräte Funktionen zu schreiben und das Gerät beim Geräte Host zu registrieren. Der Geräte Host verarbeitet die Ermittlungs-, Beschreibungs-, Steuerungs-und Ereignis Teile der UPnP-basierten Gerätefunktionalität.

 

 