---
description: Zuordnung von Projektmappen zur Jugend Steuerungs Infrastruktur
ms.assetid: 09677019-2cf9-43fe-b16c-e802767bef3a
title: Zuordnung von Projektmappen zur Jugend Steuerungs Infrastruktur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea410663af2e3b2363b7026a6997da5c19a1077a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106358438"
---
# <a name="mapping-solutions-onto-the-parental-controls-infrastructure"></a>Zuordnung von Projektmappen zur Jugend Steuerungs Infrastruktur

Fünf Kategorien allgemeiner ISV-und ISP/Portal-Angebote mit Jugend steuerungssteuerungssteuerungssteuerungskontrolle sind leicht erkennbar:

-   Eigenständige Client Anwendung. Beispiele hierfür sind e-Mail-Clients und Media Player. Obwohl Media Player Risiken mit dem Internet zusehen und einige bestimmte Dienste aufweisen, werden die Protokollierung und die Einschränkungen von Wiedergabe Aktivitäten in erster Linie durch Windows-Jugendschutz Mechanismen herauf gestuft, um die Auswirkungen auf die Bibliothek zu minimieren und
-   Client/Server-Lösungen. Die wichtigsten Beispiele sind Instant Messaging-Lösungen.
-   ISP-Suites. Dabei handelt es sich um Sammlungen von Client/Server-Lösungen und Client Anwendungen, die häufig in einer einzelnen Client Benutzeroberfläche integriert sind. Beachten Sie, dass die meisten dieser Funktionen auch die meisten oder alle Funktionen bereitstellen, indem Sie den Browser Zugriff verwenden und sich zu reinen Weblösungen wechseln.
-   Reine Weblösungen. Der Zugriff erfolgt über den Browser. Beispiele hierfür sind webbasierte e-Mail-und Instant Messaging-Funktionen. Der Zugriff auf diese kann durch entsprechend ausgefüllten Webfilter Kategorien blockiert werden.
-   Firewallähnliche Lösungen. Bietet Filter auf der Ebene des Netzwerk Stapels und möglicherweise andere Betriebssystem Einschränkungen.

In der folgenden Tabelle werden Empfehlungen zum Implementieren kompatibler Lösungen für jede Kategorie angegeben.



| Category                           | Protokollierung                                                  | Einschränkungs Einstellungen                                    | Erzwingen von Einschränkungen                                 | Ersetzung von Webinhalts Filtern                                                        | Verwendung des Erweiterbarkeits Links für den Zugriff auf Protokollierung und Einstellungen               |
|------------------------------------|----------------------------------------------------------|----------------------------------------------------------|----------------------------------------------------------|---------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| Eigenständiger Client<br/>    | Auf dem Client erforderlich<br/>                            | Auf dem Client erforderlich<br/>                            | Auf dem Client erforderlich<br/>                            | –<br/>                                                                        | Erforderlich, wird als exe verwendet. Kann einfach die Navigation der App-Benutzeroberfläche aufrufen<br/>   |
| Client/Server-Lösung<br/>  | Auf dem Client erforderlich, wenn nicht vom Server ausgeführt<br/> | Auf dem Client erforderlich, wenn nicht vom Server ausgeführt<br/> | Auf dem Client erforderlich, wenn nicht vom Server ausgeführt<br/> | –<br/>                                                                        | Erforderlich, wird exe lauten<br/>                                        |
| ISP-Suite<br/>               | Auf dem Client erforderlich, wenn nicht vom Server ausgeführt<br/> | Auf dem Client erforderlich, wenn nicht vom Server ausgeführt<br/> | Auf dem Client erforderlich, wenn nicht vom Server ausgeführt<br/> | Empfiehlt die Verwendung des WPC-Filters, lässt jedoch die Ersetzung zu<br/> | Erforderlich, wird exe lauten<br/>                                        |
| Reine Weblösung<br/>       | Empfohlene Ausführung auf dem Server<br/>                | Empfohlene Ausführung auf dem Server<br/>                | Empfohlene Ausführung auf dem Server<br/>                | –<br/>                                                                        | Empfohlen. Verfügbar machen von Server Protokollierung und Einstellungen mithilfe von exe<br/> |
| Firewallähnliche Lösungen<br/> | Auf dem Client erforderlich<br/>                            | Auf dem Client erforderlich<br/>                            | Auf dem Client erforderlich<br/>                            | Empfiehlt die Verwendung des WPC-Filters, lässt jedoch die Ersetzung zu<br/> | Erforderlich, wird exe lauten<br/>                                        |



 

 

 




