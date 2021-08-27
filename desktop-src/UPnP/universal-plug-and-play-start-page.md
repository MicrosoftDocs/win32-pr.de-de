---
title: UPnP-APIs
description: Das UPnP-Framework ermöglicht dynamische Netzwerke von intelligenten Geräten, Drahtlosgeräten und PCs.
ms.assetid: 1dc05d6e-19ae-45e2-82c2-d3b63b16bf9d
keywords:
- UPnP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dfadd64dbee845f62052e8b140ca1f0b69837ece78cf7b0cc5f24e61563a6e22
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120124800"
---
# <a name="upnp-apis"></a>UPnP-APIs

## <a name="purpose"></a>Zweck

Das UPnP-Framework ermöglicht dynamische Netzwerke von intelligenten Geräten, Drahtlosgeräten und PCs. Es gibt zwei APIs für die Arbeit mit UPnP-zertifizierten Geräten:

-   Die Steuerungspunkt-API, die aus einer Reihe von COM-Schnittstellen besteht, die zum Suchen und Steuern von Geräten verwendet werden.
-   Die Gerätehost-API, die aus einer Reihe von COM-Schnittstellen besteht, die zum Implementieren von Geräten verwendet werden, die von einem Computer gehostet werden.

## <a name="where-applicable"></a>Anwendungsbereich

Mit der Steuerungspunkt-API können Entwickler Anwendungen schreiben, die UPnP-zertifizierte Geräte suchen und steuern. Mit der Gerätehost-API können Entwickler die Funktionalität von UPnP-zertifizierten Geräten implementieren und den Gerätehost verwenden, um die Ermittlungs-, Beschreibungs-, Steuerungs-, Präsentations- und Ereignisfunktionen eines UPnP-zertifizierten Geräts zu verwalten.

## <a name="developer-audience"></a>Entwicklergruppe

Entwickler, die die Steuerungspunkt-APIs und Gerätehost-APIs verwenden, müssen mit der UPnP-Gerätearchitektur vertraut sein. Weitere Informationen finden Sie in der [UPnP-Implementierungsdokumentation](https://openconnectivity.org/resources/upnpresources.zip) und im [UPnP-Forum.](https://openconnectivity.org/)

Entwickler, die die Gerätehost-APIs verwenden, sollten mit den Active Template Library (ATL) und COM-Schnittstellen vertraut sein.

Die Steuerungspunkt-APIs und Gerätehost-APIs werden von einer Vielzahl von Anwendungen verwendet, von Skripts, die in HTML-Seiten eingebettet sind, bis hin zu vollständigen C++- und Microsoft Visual Basic-Programmen.

Nur die Steuerungspunkt-API unterstützt Visual Basic Scripting Edition (VBScript).

## <a name="run-time-requirements"></a>Laufzeitanforderungen

Die Steuerungspunkt-API wird auf Computern verwendet, auf denen Microsoft Windows Edition, Windows XP, Windows XP Professional und Windows CE .NET ausgeführt wird.

Die Gerätehost-API wird auf Computern verwendet, auf denen Windows XP, Windows XP Professional und Windows CE .NET ausgeführt wird.

Spezifischere Informationen dazu, welche Betriebssysteme eine bestimmte Funktion unterstützen, finden Sie unter "Anforderungen" in der Dokumentation.

## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                                                          | Beschreibung                                                                                        |
|------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| [Übersicht über die UPnP-Architektur](overview-of-universal-plug-and-play.md)<br/>            | Allgemeine Informationen und Hintergrundinformationen.<br/>                                                     |
| [Übersicht über Kontrollpunkt](control-point-api.md)<br/>                                     | Allgemeine Informationen zur Kontrollpunkt-API.<br/>                                        |
| [Verwenden der Steuerungspunkt-API](using-the-control-point-api-with-upnp-technology.md)<br/> | Beispielcode, der zeigt, wie Anwendungen entwickelt werden, die UPnP-zertifizierte Geräte steuern.<br/> |
| [Referenz zur Kontrollpunkt-API](control-point-api-with-upnp-technology-reference.md)<br/> | Dokumentation zu Steuerungspunktkomponentenschnittstellen, -methoden und -ereignissen.<br/>               |
| [Übersicht über die Gerätehost-API](device-host-api.md)<br/>                                     | Allgemeine Informationen zur Gerätehost-API.<br/>                                          |
| [Verwenden der Gerätehost-API](using-the-device-host-api-with-upnp-technology.md)<br/>     | Beispielcode, der zeigt, wie Sie eine Anwendung für UPnP-zertifizierte Geräte entwickeln.<br/>        |
| [Referenz zur Gerätehost-API](device-host-api-with-upnp-technology-reference.md)<br/>     | Dokumentation zu Komponentenschnittstellen, Methoden und Ereignissen des Gerätehosts.<br/>                 |



 

 

 





