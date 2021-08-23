---
description: Die Medienpaketgröße wirkt sich auf die Fähigkeit von IPX-Protokollen aus, Daten über Netzwerke hinweg zu übertragen, und kann sich als schwierig erweisen, mit transportunabhängigen Aufgaben umzugehen.
ms.assetid: cce31a6a-c187-4ec4-976c-5f9984211ccb
title: Informationen zur Medienpaketgröße
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03be30402dc94b22315292b281565572f04cbc89803eeed79f67d55a77ceeef6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119412190"
---
# <a name="about-media-packet-size"></a>Informationen zur Medienpaketgröße

Die Medienpaketgröße wirkt sich auf die Fähigkeit von IPX-Protokollen aus, Daten über Netzwerke hinweg zu übertragen, und kann sich als schwierig erweisen, mit transportunabhängigen Aufgaben umzugehen. IPX segmentiert keine Pakete und meldet auch nicht, wenn Pakete aufgrund von Größenverletzungen gelöscht werden. Dies bedeutet, dass eine Entität auf der Endstation wissen muss, welche maximale Paketgröße für einen bestimmten Internetarbeitspfad verwendet werden soll. Bisher haben IPX-Datagramme und verbindungsorientierte SPX-Dienste diese Last der Anwendung überlassen, während SPXII große Internetpaketaushandlungen verwendet hat, um sie transparent zu behandeln.

Winsock versucht, rationale Paketgrößenlimits für die verschiedenen IPX-Protokolle festzulegen, wie im nächsten Abschnitt beschrieben. Diese Grenzwerte können von Anwendungen über Get/Set-Socketoptionen angezeigt und geändert werden. Bei der Bestimmung der maximalen Paketgröße sind die drei Bereiche von Bedeutung:

-   \# Medienpaketgröße
-   \# Routingfähige Paketgröße
-   \# Paketgröße der Endstation

Die Größe des *Medienpakets* spiegelt die maximale Paketgröße wider, die auf allen Medien zulässig ist, die das Paket an das Ziel durchläuft. Die Paketgröße variiert zwischen unterschiedlichen Medien wie Ethernet und Tokenring. Die Menge des Datenspeicherplatzes innerhalb eines Pakets kann je nach Paketheaderanordnung auch innerhalb eines bestimmten Mediums variieren. Die effektive Datengröße eines Ethernet-Pakets hängt beispielsweise davon ab, ob es sich um den Typ Ethernet II, Ethernet 802.2 oder Ethernet SNAP handelt.

*Die routingfähige Paketgröße* spiegelt die maximale Paketgröße wider, die ein Zwischenrouter weiterleiten möchte. Die meisten IPX-Router sind so aufgebaut, dass ein Beliebiges Größen-Datagramm weitergeleitet wird, solange es innerhalb der Mediengröße des sendenden und empfangenden Netzwerks verbleibt. Ältere Router können jedoch die maximale Paketgröße auf 576 Bytes beschränken, einschließlich Protokollheadern.

*Die Paketgröße* der Endstation gibt die Größe der Lauschenpuffer an, die Von Endstationen bereitgestellt wurden, um eingehende Pakete zu empfangen. Selbst wenn die Grenzwerte für Medien und Router ein Paket passieren lassen, kann es von der Endstation verworfen werden, wenn die empfangende Anwendung einen kleineren Puffer bereitgestellt hat. Viele herkömmliche IPX-/SPX-Anwendungen beschränken die Puffergröße so, dass der Datenteil nicht größer als 512 oder 1024 Bytes sein darf.

 

 



