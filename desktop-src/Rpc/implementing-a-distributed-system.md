---
title: Implementieren eines verteilten Systems
description: Eine Möglichkeit, Software in einem verteilten System zu implementieren, ist die Verwendung von Rohnetzwerkunterstützung.
ms.assetid: 46abbbec-caa1-4fee-a713-4a4a2b462051
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 098263f916129115f41840e15ac689fab7e4544621989d1a4d3179e50ef17d27
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120020529"
---
# <a name="implementing-a-distributed-system"></a>Implementieren eines verteilten Systems

Eine Möglichkeit, Software in einem verteilten System zu implementieren, ist die Verwendung von Rohnetzwerkunterstützung. Dieser Ansatz umfasst Sockets, Named Pipes oder HTTP POSTs, GETs und so weiter. All diese Modelle zwingen den Entwickler, primitive Programmiergrundtypen auf niedriger Ebene auf die eine oder andere Weise zu verwenden, die den Entwickler zwingen, sich mit der Darstellung von Netzwerkdaten (Network Data Representation, NDR), dem Packen von Daten, der Verwaltung von Netzwerkdatenverkehr und Fehlerbedingungen, dem Schutz und der Verschlüsselung von Daten und so weiter zu befassen.

RPC bietet ein Programmiermodell, bei dem der Entwickler die präzise Kontrolle über die Netzwerkinteraktion zwischen Client und Server über eine umfangreiche API behält und Entwicklern gleichzeitig die Details und Lasten erspart, die ein verteiltes System tendenziell einleitet.

Betrachten Sie beispielsweise die Belastung, die mit verschiedenen Ansätzen zum Schutz der Integrität und des Datenschutzes des Nachrichtenaustauschs in einem verteilten System verbunden ist. Bei der Berücksichtigung der Netzwerksicherheit für den Paketaustausch sind einige Schutzmaßnahmen schwächer, einige stärker. Es gibt keine echte Netzwerksicherheit, sondern nur verschiedene paketbasierte Sicherheitsmechanismen. Sicherheit, die den Aufrufer identifiziert (was tendenziell auch schwach ist, da Paketinhalte häufig während der Übertragung geändert werden können), Sicherheit zum Schutz der Integrität des Pakets ohne Schutz seiner Privatsphäre (verschiedene Signaturen und Hashes) und Sicherheit zum Schutz der Privatsphäre des Nachrichtenaustauschs (verschiedene Verschlüsselungsmechanismen).

Eine weitere Belastung für die Implementierung eines sicheren verteilten Systems sind die Algorithmen, die zum Implementieren von Sicherheitsprimitiven wie Verschlüsselung, Signierung, Authentifizierung und so weiter erforderlich sind. Ein Entwickler kann diese Algorithmen implementieren, aber dies ist schwierig, fehleranfällig und sogar riskant, da die resultierenden Algorithmen oft kleine Sicherheitslücken aufweisen. Alternativ kann ein Entwickler einen verfügbaren Sicherheitsanbieter verwenden, um schutz für die Netzwerkinteraktionen innerhalb eines verteilten Systems zu implementieren.

MitHILFE von RPC lassen sich diese beiden Lasten sehr einfach lösen. Ein Entwickler muss RPC lediglich mitteilen, welches Sicherheitspaket verwendet werden soll und welcher Sicherheitsschutz auf den Nachrichtenaustausch angewendet werden soll (in Bezug auf Authentifizierung, Verschlüsselung, gegenseitige Authentifizierung, Nachverfolgung von Aufrufer-Identitäten und so weiter). RPC kümmert sich auf effiziente Weise um alle Details im Hintergrund, bietet dem Entwickler jedoch die vollständige Kontrolle darüber, wie die Daten genau geschützt werden.

 

 




