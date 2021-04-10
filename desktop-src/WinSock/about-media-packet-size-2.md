---
description: Die Medienpaket Größe wirkt sich auf die Fähigkeit von IPX-Protokollen aus, Daten über Netzwerke hinweg zu übertragen, und kann sich als schwierig erweisen, eine Transport unabhängige Lösung zu behandeln.
ms.assetid: cce31a6a-c187-4ec4-976c-5f9984211ccb
title: Informationen zur Medienpaket Größe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39f97e36a81b90b72d4d1148e9461f58ae2147ba
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "103961211"
---
# <a name="about-media-packet-size"></a>Informationen zur Medienpaket Größe

Die Medienpaket Größe wirkt sich auf die Fähigkeit von IPX-Protokollen aus, Daten über Netzwerke hinweg zu übertragen, und kann sich als schwierig erweisen, eine Transport unabhängige Lösung zu behandeln. IPX segmentiert keine Pakete und meldet nicht, wenn Pakete aufgrund von Größen Verletzungen gelöscht werden. Dies bedeutet, dass die maximale Paketgröße, die für einen bestimmten internetzwerkpfad verwendet werden soll, von einer Entität auf der Endstation beibehalten werden muss. In der Regel haben IPX-Datagramme und Verbindungs orientierte SPX-Dienste diese Belastung für die Anwendung beibehalten, während SPXII eine große Internet Paket Aushandlung verwendet hat, um Sie transparent zu verarbeiten.

Winsock versucht, für die verschiedenen IPX-Protokolle, wie im nächsten Abschnitt beschrieben, rationale Paketgrößen Limits festzulegen. Diese Grenzwerte können von Anwendungen mithilfe von Get/Set-Socketoptionen angezeigt und geändert werden. Wenn Sie die maximale Paketgröße ermitteln, sind die folgenden drei Bereiche von Bedeutung:

-   \# Größe des Medienpakets
-   \# Routing fähige Paketgröße
-   \# Größe des Endstations Pakets

Die *Größe des Medienpakets* gibt die maximale Paketgröße an, die auf allen Medien zulässig ist, die das Paket auf sein Ziel durchläuft. Die Paketgröße variiert je nach Medium, z. b. Ethernet und TokenRing. Die Menge des Daten Platzes innerhalb eines Pakets kann je nach Paket Header Anordnung auch innerhalb eines bestimmten Mediums variieren. Die effektive Datengröße eines Ethernet-Pakets variiert beispielsweise abhängig davon, ob es sich um den Typ Ethernet II, Ethernet 802,2 oder das Ethernet-Snap-in handelt.

*Routing fähige Paketgröße* gibt die maximale Paketgröße an, die ein zwischen Router weiterleiten soll. Die meisten IPX-Router werden erstellt, um beliebige Größen Datagramm weiterzuleiten, solange Sie in der Mediengröße des sendenden und empfangenden Netzwerks verbleibt. Ältere Router können jedoch die maximale Paketgröße auf 576 Bytes beschränken, einschließlich Protokoll Header.

Die *Größe des Endstations Pakets* spiegelt die Größe der Abhör Puffer wider, die von den Endstationen zum Empfangen eingehender Pakete gepostet wurden. Selbst wenn die Medien-und routerlimits ein Paket durchzulassen, wird es möglicherweise von der Endstation verworfen, wenn die empfangende Anwendung einen kleineren Puffer gepostet hat. Viele herkömmliche IPX/SPX-Anwendungen beschränken die Größe des Empfangspuffers so, dass der Daten Teil nicht größer als 512 oder 1024 Bytes sein darf.

 

 



