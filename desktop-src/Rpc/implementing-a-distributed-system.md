---
title: Implementieren eines verteilten Systems
description: Eine Möglichkeit zum Implementieren von Software in einem verteilten System ist die Verwendung von unformatierten Netzwerkunterstützung.
ms.assetid: 46abbbec-caa1-4fee-a713-4a4a2b462051
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ab45f8175e82bdd1f5d6e49f3d94578473ed5c7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855787"
---
# <a name="implementing-a-distributed-system"></a>Implementieren eines verteilten Systems

Eine Möglichkeit zum Implementieren von Software in einem verteilten System ist die Verwendung von unformatierten Netzwerkunterstützung. Diese Vorgehensweise umfasst Sockets, Named Pipes oder http-Beiträge, Ruft ab usw. Alle diese Modelle erzwingen, dass der Entwickler auf eine oder andere Weise Programmier primitive auf niedriger Ebene verwendet, die es dem Entwickler zwingen, sich mit der Netzwerkdaten Darstellung (NDR), dem Verpacken von Daten, der Verwaltung von Netzwerk Datenverkehr und Fehlerzuständen, dem Schutz der Datenintegrität und der Verschlüsselung zu beschäftigen.

RPC bietet ein Programmiermodell, in dem der Entwickler eine differenzierte Steuerung der Netzwerk Interaktion zwischen dem Client und dem Server über eine umfassende API beibehält, während Entwickler aus den Details und Belastungen, die ein verteiltes System in der Regel einführt, bewahrt werden.

Stellen Sie sich z. b. die Belastung der verschiedenen Ansätze vor, um die Integrität und den Schutz von Nachrichtenaustausch Vorgängen in einem verteilten System zu schützen. Bei der Berücksichtigung der Netzwerksicherheit für den Paket Austausch sind einige Schutzmaßnahmen schwächer, und das ist noch stärker. Es gibt keine echte Netzwerksicherheit, sondern nur verschiedene paketbasierte Sicherheitsmechanismen. Sicherheit, die den Aufrufer identifiziert (der in der Regel auch schwach ist, da Paket Inhalte bei der Übertragung häufig geändert werden können), Sicherheit, die die Integrität des Pakets schützt, ohne seinen Datenschutz (verschiedene Signaturen und Hashs) zu schützen, und Sicherheit, die den Datenschutz des Nachrichten Austauschs schützt (verschiedene Verschlüsselungsmechanismen).

Ein weiterer Aufwand bei der Implementierung eines sicheren verteilten Systems sind die Algorithmen, die für die Implementierung von Sicherheits primitiven, z. b. Verschlüsselung, Signierung, Authentifizierung usw., erforderlich sind. Ein Entwickler kann diese Algorithmen implementieren, aber dies ist schwierig, fehleranfällig und sogar riskant, da die resultierenden Algorithmen häufig zu geringfügigen Sicherheitslücken führen. Alternativ kann ein Entwickler einen verfügbaren Sicherheitsanbieter verwenden, um den Schutz für die Netzwerk Interaktionen innerhalb eines verteilten Systems zu implementieren.

Bei Verwendung von RPC werden diese beiden Belastungen sehr leicht gelöst. Ein Entwickler muss lediglich angeben, welches Sicherheitspaket verwendet werden soll und welcher Sicherheitsschutz auf den Nachrichtenaustausch angewendet werden soll (im Hinblick auf Authentifizierung, Verschlüsselung, gegenseitige Authentifizierung, Überwachung der Identität des Aufrufers usw.). RPC kümmert sich um alle Details im Hintergrund auf effiziente Weise, bietet dem Entwickler jedoch vollständige Kontrolle darüber, wie die Daten geschützt werden.

 

 




