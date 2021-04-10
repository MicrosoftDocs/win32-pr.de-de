---
description: Der NLA-Dienstanbieter (Network Location Awareness) ist wichtig für Computer oder Geräte, die möglicherweise zwischen verschiedenen Netzwerken verschoben werden, und für die Auswahl optimaler Konfigurationen, wenn mehr als eine verfügbar ist.
ms.assetid: 307f384d-e59a-4fc5-8f6a-ed81a102df60
title: Die NLA-Rolle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28034d0d08353b3e794b5a30a6900e24d214e977
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215463"
---
# <a name="the-role-of-nla"></a>Die NLA-Rolle

Der NLA-Dienstanbieter (Network Location Awareness) ist wichtig für Computer oder Geräte, die möglicherweise zwischen verschiedenen Netzwerken verschoben werden, und für die Auswahl optimaler Konfigurationen, wenn mehr als eine verfügbar ist. Beispielsweise kann ein drahtloses Computer Roaming zwischen physischen Netzwerken NLA verwenden, um die richtige Konfiguration basierend auf Informationen über die verfügbare Netzwerkverbindung zu ermitteln. NLA erweist sich auch als wertvoll, wenn ein mehrfach vernetzter Computer über eine physische Verbindung mit einem Netzwerk verfügt, während auch über eine DFÜ-Verbindung oder einen Tunnel eine Verbindung mit einem anderen Netzwerk besteht.

In der Vergangenheit mussten Entwicklerinformationen zu einer logischen Netzwerkschnittstelle abrufen und daher Entscheidungen über die Netzwerk Konnektivität treffen, basierend auf einer Vielzahl von unterschiedlichen Netzwerkinformationen. In diesen Fällen mussten Entwickler die geeignete Netzwerkschnittstelle basierend auf der IP-Adresse, dem Subnetz der Schnittstelle, dem Domain Name System (DNS)-Namen, der der Schnittstelle zugeordnet ist, der Mac-Adresse einer NIC, einem drahtlos Netzwerknamen oder anderen Netzwerkinformationen auswählen. NLA verringert dieses Problem durch Bereitstellen einer Standardschnittstelle zum Auflisten von Informationen zu logischen Netzwerk Anlagen, Korrelieren der Informationen zu physischen Netzwerkschnittstellen Informationen und anschließende Bereitstellung von Benachrichtigungen, wenn zuvor zurückgegebene Informationen ungültig werden.

NLA bietet die folgenden Informationen zum Netzwerk Speicherort:

<dl> <dt>

<span id="Logical_Network_Identity"></span><span id="logical_network_identity"></span><span id="LOGICAL_NETWORK_IDENTITY"></span>Identität des logischen Netzwerks
</dt> <dd>

NLA versucht zunächst, ein logisches Netzwerk mit dem DNS-Domänen Namen zu identifizieren. Wenn ein logisches Netzwerk keinen Domänen Namen hat, identifiziert NLA das Netzwerk aus benutzerdefinierten statischen Informationen, die in der Registrierung gespeichert sind, und schließlich über seine Subnetzadresse.

</dd> <dt>

<span id="Logical_Network_Interfaces"></span><span id="logical_network_interfaces"></span><span id="LOGICAL_NETWORK_INTERFACES"></span>Logische Netzwerkschnittstellen
</dt> <dd>

Für jedes Netzwerk, dem ein Computer angefügt ist, stellt NLA einen *Adaptername* bereit, der eine physische Schnittstelle (z. b. eine NIC) oder eine logische Schnittstelle wie eine RAS-Verbindung eindeutig identifiziert. Der Adapter Name kann dann mit Funktionen verwendet werden, die in der IP Helper-API verfügbar sind, um weitere Schnittstelleneigenschaften zu erhalten.

</dd> </dl>

NLA implementiert das logische Netzwerk als Dienstklasse mit zugeordneten Klassen-GUID und-Eigenschaften. Jedes logische Netzwerk, für das NLA Informationen zurückgibt, ist eine Instanz der Dienstklasse.

 

 



