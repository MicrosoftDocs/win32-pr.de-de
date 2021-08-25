---
description: Zuordnen von Lösungen zur Infrastruktur für die Jugendkontrollen
ms.assetid: 09677019-2cf9-43fe-b16c-e802767bef3a
title: Zuordnen von Lösungen zur Infrastruktur für die Jugendkontrollen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5dcf16ec2d656828921ccd6992f2811dcf4590ab06731d1ac6474fd8d7625c26
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119951970"
---
# <a name="mapping-solutions-onto-the-parental-controls-infrastructure"></a>Zuordnen von Lösungen zur Infrastruktur für die Jugendkontrollen

Fünf Kategorien gängiger Angebote für ISV und ISP/Portal für Die Jugendschutzkontrollen sind sofort erkennbar:

-   Eigenständige Clientanwendung. Beispiele hierfür sind E-Mail-Clients und Media Player. Obwohl Media Player ein Risiko mit Internetanmelderisiko haben und einige über bestimmte Dienste verfügen, fördert Windows Der Jugendschutz in erster Linie die Protokollierung und Einschränkungen bei Wiedergabeaktivitäten, um die Auswirkungen auf die Bibliothek und das Protokollieren von Rauschen für Administratoren zu minimieren.
-   Client-/Serverlösungen. Die wichtigsten Beispiele sind Instant Messaging-Lösungen.
-   ISP-Sammlungen. Hierbei handelt es sich um Sammlungen von Client-/Serverlösungen und Clientanwendungen, die häufig in eine einzelne Client-Benutzeroberfläche integriert sind. Beachten Sie, dass die meisten dieser Funktionen auch die meisten oder alle Funktionen bereitstellen, indem Sie den Browserzugriff verwenden und zu webbasierten Lösungen übergekreuzt werden.
-   Lösungen, die nur im Web verfügbar sind. Der Zugriff erfolgt über den Browser. Beispiele hierfür sind webbasierte E-Mail- und Instant Messaging-Funktionen. Der Zugriff auf diese kann durch entsprechend aufgefüllte Webfilterkategorien blockiert werden.
-   Firewall-orientierte Lösungen. Bietet Filterung auf Netzwerkstapelebene und möglicherweise andere Betriebssystemeinschränkungen.

Empfehlungen implementierung konformer Lösungen für jede Kategorie sind in der folgenden Tabelle angegeben.



| Kategorie                           | Protokollierung                                                  | Einstellungen für Einschränkungen                                    | Erzwingung von Einschränkungen                                 | Ersetzen von Webinhaltsfiltern                                                        | Verwenden des Erweiterbarkeitslinks für den Protokollierungs- und Einstellungszugriff               |
|------------------------------------|----------------------------------------------------------|----------------------------------------------------------|----------------------------------------------------------|---------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| "Eigenständiger" Client<br/>    | Auf Client erforderlich<br/>                            | Auf Client erforderlich<br/>                            | Auf Client erforderlich<br/>                            | Nicht zutreffend<br/>                                                                        | Erforderlich, ist "exe". Kann einfach die App-Benutzeroberflächennavigation aufrufen<br/>   |
| Client-/Serverlösung<br/>  | Auf Dem Client erforderlich, wenn dies nicht vom Server ausgeführt wird<br/> | Auf Dem Client erforderlich, wenn dies nicht vom Server ausgeführt wird<br/> | Auf Dem Client erforderlich, wenn dies nicht vom Server ausgeführt wird<br/> | Nicht zutreffend<br/>                                                                        | Erforderlich, ist "exe".<br/>                                        |
| ISP-Suite<br/>               | Auf Dem Client erforderlich, wenn dies nicht vom Server ausgeführt wird<br/> | Auf Dem Client erforderlich, wenn dies nicht vom Server ausgeführt wird<br/> | Auf Dem Client erforderlich, wenn dies nicht vom Server ausgeführt wird<br/> | Es wird empfohlen, einen WPC-Filter zu verwenden, aber ersetzungen zu ermöglichen, wenn dies für mehrere Benutzer stabil ist.<br/> | Erforderlich, ist "exe".<br/>                                        |
| Lösung nur im Web<br/>       | Empfehlen der Ausführung auf dem Server<br/>                | Empfehlen der Ausführung auf dem Server<br/>                | Empfehlen der Ausführung auf dem Server<br/>                | Nicht zutreffend<br/>                                                                        | Empfohlen. Verfügbar machen der Serverprotokollierung und -einstellungen mithilfe von EXE<br/> |
| Firewall-orientierte Lösungen<br/> | Auf Client erforderlich<br/>                            | Auf Client erforderlich<br/>                            | Auf Client erforderlich<br/>                            | Es wird empfohlen, einen WPC-Filter zu verwenden, aber ersetzungen zu ermöglichen, wenn dies für mehrere Benutzer stabil ist.<br/> | Erforderlich, ist "exe".<br/>                                        |



 

 

 




