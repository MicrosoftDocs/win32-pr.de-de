---
title: Die Rolle des Netzwerklisten-Managers
description: Die Rolle des Netzwerklisten-Managers
ms.assetid: 056d7b0f-5ff7-4b87-8bfe-d4e2018ee638
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec37d0cf157b87bf43fe12e9aa3a33eb316b7800474dd75ef3a6d4e23bb6189d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119780490"
---
# <a name="the-role-of-network-list-manager"></a>Die Rolle des Netzwerklisten-Managers

Vor Windows XP und Windows Server 2003 mussten Anwendungen eine Reihe von nicht verknüpften APIs aufrufen, um Daten zu Netzwerkattributen wie der IP-Adresse, dem Domänencontroller oder dem Domain Name System (DNS) abzurufen. Ab Windows XP und Windows Server 2003 verfügte die Winsock-API zur Netzwerkstandorterkennung über einen begrenzten Satz von Netzwerkspeicherortfunktionen. In Windows Server 2008 und Windows Vista erfasst der Netzwerkerkennungsdienst die Netzwerkattribute an einem Ort und ermöglicht Anwendungen das Abfragen und Abrufen bestimmter Netzwerke und Attribute. Der Netzwerklisten-Manager ersetzt die Funktionalität der vorherigen Winsock-API (verfügbar als Winsock-Namensspeicherplatzanbieter), während die Kompatibilität mit älteren Anwendungen mithilfe der Winsock-API erhalten bleibt.

 

 




