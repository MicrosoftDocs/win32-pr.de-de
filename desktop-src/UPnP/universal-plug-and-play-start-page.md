---
title: UPnP-APIs
description: Das UPnP-Framework ermöglicht das dynamische Netzwerk von intelligenten Geräten, drahtlosen Geräten und PCs.
ms.assetid: 1dc05d6e-19ae-45e2-82c2-d3b63b16bf9d
keywords:
- UPnP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 022ede01a62230194969d7789e0ace70f960debb
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/09/2020
ms.locfileid: "104102503"
---
# <a name="upnp-apis"></a>UPnP-APIs

## <a name="purpose"></a>Zweck

Das UPnP-Framework ermöglicht das dynamische Netzwerk von intelligenten Geräten, drahtlosen Geräten und PCs. Für das Arbeiten mit UPnP-zertifizierten Geräten gibt es zwei APIs:

-   Die Kontrollpunkt-API, die aus einem Satz von COM-Schnittstellen besteht, die zum Suchen und Steuern von Geräten verwendet werden.
-   Die Geräte Host-API, die aus einem Satz von COM-Schnittstellen besteht, die zum Implementieren von Geräten verwendet werden, die von einem Computer gehostet werden.

## <a name="where-applicable"></a>Anwendungsbereich

Die Kontrollpunkt-API ermöglicht Entwicklern das Schreiben von Anwendungen, die nach UPnP-zertifizierten Geräten suchen und diese Steuern. Die Geräte Host-API ermöglicht Entwicklern die Implementierung der Funktionalität von UPnP-zertifizierten Geräten und die Verwendung des Geräte Hosts zum Verwalten der Ermittlungs-, Beschreibungs-, Steuerungs-, Präsentations-und Ereignis Funktionen eines UPnP-zertifizierten Geräts.

## <a name="developer-audience"></a>Entwicklergruppe

Entwickler, die die Steuerungspunkt-APIs und die Geräte Host-APIs verwenden, müssen mit der UPnP-Geräte Architektur vertraut sein. Weitere Informationen finden Sie in der [UPnP-Implementierungs Dokumentation](https://openconnectivity.org/resources/upnpresources.zip) und im [UPnP-Forum](https://openconnectivity.org/).

Entwickler, die die Geräte Host-APIs verwenden, sollten mit den Active Template Library (ATL) und COM-Schnittstellen vertraut sein.

Die Steuerungspunkt-APIs und die Geräte Host-APIs werden von einer Vielzahl von Anwendungen verwendet, von Skripts, die in HTML-Seiten eingebettet sind, in vollständige C++-und Microsoft Visual Basic-Programme.

Nur die Kontrollpunkt-API unterstützt Visual Basic Scripting Edition (VBScript).

## <a name="run-time-requirements"></a>Laufzeitanforderungen

Die Kontrollpunkt-API wird auf Computern verwendet, auf denen Microsoft Windows Millennium Edition, Windows XP, Windows XP Professional und Windows CE .NET ausgeführt werden.

Die Geräte Host-API wird auf Computern verwendet, auf denen Windows XP, Windows XP Professional und Windows CE .NET ausgeführt werden.

Spezifischere Informationen dazu, welche Betriebssysteme eine bestimmte Funktion unterstützen, finden Sie in der Dokumentation unter "Anforderungen".

## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                                                          | BESCHREIBUNG                                                                                        |
|------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| [Übersicht über die UPnP-Architektur](overview-of-universal-plug-and-play.md)<br/>            | Allgemeine Informationen und Hintergrundinformationen.<br/>                                                     |
| [Übersicht über den Steuerungspunkt](control-point-api.md)<br/>                                     | Allgemeine Informationen zur Steuerungspunkt-API.<br/>                                        |
| [Verwenden der Steuerungspunkt-API](using-the-control-point-api-with-upnp-technology.md)<br/> | Beispielcode, der zeigt, wie Sie Anwendungen entwickeln, mit denen UPnP-zertifizierte Geräte gesteuert werden.<br/> |
| [API-Referenz für Steuerungspunkt](control-point-api-with-upnp-technology-reference.md)<br/> | Dokumentation der Schnittstellen, Methoden und Ereignisse von Steuerungspunkt Komponenten.<br/>               |
| [Übersicht über die Geräte Host-API](device-host-api.md)<br/>                                     | Allgemeine Informationen zur Geräte Host-API.<br/>                                          |
| [Verwenden der Geräte Host-API](using-the-device-host-api-with-upnp-technology.md)<br/>     | Beispielcode, der zeigt, wie eine Anwendung für UPnP-zertifizierte Geräte entwickelt wird.<br/>        |
| [Referenz zur Geräte Host-API](device-host-api-with-upnp-technology-reference.md)<br/>     | Dokumentation zu Geräte Host Komponenten-Schnittstellen, Methoden und Ereignissen.<br/>                 |



 

 

 





