---
title: Die Rolle des Netzwerk Listen-Managers
description: Die Rolle des Netzwerk Listen-Managers
ms.assetid: 056d7b0f-5ff7-4b87-8bfe-d4e2018ee638
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3976cdee7a8fa93a7c0dc883f25d65c2e4ae6e6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856940"
---
# <a name="the-role-of-network-list-manager"></a>Die Rolle des Netzwerk Listen-Managers

Vor Windows XP und Windows Server 2003 mussten Anwendungen eine Reihe von nicht verknüpften APIs aufzurufen, um Daten zu Netzwerk Attributen wie IP-Adresse, Domänen Controller oder Domain Name System (DNS) abzurufen. Ab Windows XP und Windows Server 2003 hat die Winsock-API für Network Location Awareness eine begrenzte Menge an Netzwerkadressen Funktionen verwendet. In Windows Server 2008 und Windows Vista erfasst der Network Awareness Service die Netzwerk Attribute an einem Ort und ermöglicht Anwendungen, bestimmte Netzwerke und Attribute abzufragen und abzurufen. Der Netzwerk Listen-Manager ersetzt die Funktionalität der vorherigen Winsock-API (verfügbar als Winsock-Namespace Anbieter) und unter Beibehaltung der Kompatibilität mit älteren Anwendungen, die die Winsock-API verwenden.

 

 




