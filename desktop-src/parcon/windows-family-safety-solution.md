---
description: Windows Family Safety-Lösung
ms.assetid: b89cf0c7-bf9f-4bcb-b008-8b7c792f3300
title: Windows Family Safety-Lösung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7cc5e5749201fc849e7c9476c97c6fbd3dc5ee5b2d3f26ed3988eb72ac59c1ac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119951650"
---
# <a name="windows-family-safety-solution"></a>Windows Family Safety-Lösung

Die wichtigsten Anforderungen, die von Microsoft für eine umfassendere Lösung definiert werden, lauten wie folgt. Beachten Sie, dass es sich bei der Definition für online in erster Linie um eine Technologie mit Internetzugriff handelt, im Gegensatz zu einem Offlineclient, der normalerweise am Computer gebunden ist.

-   Stellen Sie einen einzelnen, leicht zu findenden Bereich auf der Benutzeroberfläche des Betriebssystems bereit, in dem alle Richtlinien für die Jugendkontrolle, die Steuerung der Aktivitätsüberwachung und Aktivitätsdaten für eine Identität leicht gefunden werden können.

-   Unterstützung der Überwachung einer ausreichenden Aktivität des kontrollierten Benutzers, damit ein übergeordnetes Element oder ein Vormähre ein angemessenes Maß an Sicherheit hat, dass riskante Aktivitäten entdeckt werden können. Protokollieren Sie außerdem die Neukonfiguration der Richtlinien des kontrollierten Benutzers, damit unbeabsichtigte oder nicht autorisierte Änderungen erkennbar sind.

-   Machen Sie Funktionen zur Aktivitätsüberwachung über Windows Vista-Ereignisprotokollierungsschnittstellen verfügbar, und stellen Sie eine In-Box-Viewer-Lösung bereit. Definieren Sie Standardaktivitätsereignisse, und stellen Sie die Erweiterbarkeit für die benutzerdefinierte Ereignisgenerierung durch ISVs zur Verfügung.

-   Stellen Sie sicher, dass alle Überwachungen und Einschränkungen für einen Benutzer nur von den Eltern oder Wächtern auf Zustimmungsbasis aktiviert werden. Nach Möglichkeit sollten Einschränkungen für nicht kontrollierte Benutzer vollständig inaktiv sein, um Sicherheits- und Anwendungskompatibilitätsrisiken zu minimieren.

-   Microsoft ist bestrebt, nach Möglichkeit keine Mehrwerte nach Alter oder anderen Parametern für den kontrollierten Benutzer zu treffen (dritte Parteien können dies tun). Solche Entscheidungen bleiben den übergeordneten Oder-Wächtern obliegt, die häufig von Communitys oder Organisationen beeinflusst werden.

-   Stellen Sie Implementierungen im Produkt für die Überwachung von Offlineaktivitäten und Einschränkungen bereit, bei denen derzeit nur wenige oder gar keine Angebote verfügbar sind, die zugehörige Sicherheitsrisikofunktion im Produkt verfügbar ist oder eine Microsoft-Lösung leistungsfähige und stabile Funktionen bietet, die vollständig in das Design des Betriebssystems integriert sind.

-   Im Allgemeinen sollten Anwendungen ihre eigene Protokollierung und Einschränkungen durchführen, um optimale Kontext- und Benutzeroberflächenerfahrung zu bieten.

    Ausnahme: Stellen Sie eine umfassende Onlineaktivitätsüberwachung und Einschränkungen in ausgewählten Bereichen zur Verfügung, in denen der Vorteil für Verbraucher und die Branche die Kosten übersteigt.

-   Machen Sie Einstellungen der Jugendschutz-Benutzeroberfläche und Aktivitätsereignisdefinitionen verfügbar, indem Sie öffentliche APIs verwenden, damit Dritte Statusabfragen ausführen, Einstellungen ändern und Aktivitätsprotokolle lesen können, wenn sie mit ausreichenden berechtigungen Windows ausgeführt werden.

Ein übergeordnetes Ziel besteht in der Förderung der Koexistenz von Lösungen für die Jugendschutz von Drittanbietern mit der integrierten Funktionalität und der Unterstützung des Mehrwerts durch Integration, Erweiterung oder Bereitstellung alternativer Funktionen, sofern dies geeignet ist.

 

 



