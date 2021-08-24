---
description: Der Netzwerkadressenerkennungs-Dienstanbieter (Network Location Awareness, NLA) ist wichtig für Computer oder Geräte, die zwischen verschiedenen Netzwerken verschoben werden können, und für die Auswahl optimaler Konfigurationen, wenn mehrere verfügbar sind.
ms.assetid: 307f384d-e59a-4fc5-8f6a-ed81a102df60
title: Die Rolle der NLA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f44d517fc9f32d4fb61eb2b4d9b61c473bc946066e670fcb51f0ca2c753e692
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119733340"
---
# <a name="the-role-of-nla"></a>Die Rolle der NLA

Der Netzwerkadressenerkennungs-Dienstanbieter (Network Location Awareness, NLA) ist wichtig für Computer oder Geräte, die zwischen verschiedenen Netzwerken verschoben werden können, und für die Auswahl optimaler Konfigurationen, wenn mehrere verfügbar sind. Beispielsweise kann ein Drahtloscomputer, der zwischen physischen Netzwerken roaming möchte, die NLA verwenden, um die richtige Konfiguration anhand von Informationen über die verfügbare Netzwerkverbindung zu bestimmen. Die NLA erweist sich auch dann als nützlich, wenn ein mehrfach vernetzter Computer über eine physische Verbindung mit einem Netzwerk verfügt und gleichzeitig über eine DFÜ-Verbindung oder einen Tunnel mit einem anderen Netzwerk verbunden ist.

In der Vergangenheit mussten Entwickler Informationen zu einer logischen Netzwerkschnittstelle abrufen und daher Entscheidungen zur Netzwerkkonnektivität treffen, basierend auf einer Vielzahl unterschiedlicher Netzwerkinformationen. Unter diesen Umständen mussten Entwickler die entsprechende Netzwerkschnittstelle basierend auf der IP-Adresse, dem Subnetz der Schnittstelle, dem dns-Namen (Domain Name System), der der Schnittstelle zugeordnet ist, der MAC-Adresse einer NIC, einem Drahtlosnetzwerknamen oder anderen Netzwerkinformationen auswählen. Die NLA entschärft dieses Problem, indem eine Standardschnittstelle zum Aufzählen logischer Netzwerkanfügungsinformationen, korrelieren mit Informationen zur physischen Netzwerkschnittstelle und anschließendes Bereitstellen von Benachrichtigungen, wenn zuvor zurückgegebene Informationen ungültig werden, zur Verfügung gestellt werden.

Die NLA stellt die folgenden Informationen zum Netzwerkstandort bereit:

<dl> <dt>

<span id="Logical_Network_Identity"></span><span id="logical_network_identity"></span><span id="LOGICAL_NETWORK_IDENTITY"></span>Logische Netzwerkidentität
</dt> <dd>

Die NLA versucht zunächst, ein logisches Netzwerk anhand des DNS-Domänennamens zu identifizieren. Wenn ein logisches Netzwerk keinen Domänennamen hat, identifiziert die NLA das Netzwerk anhand von benutzerdefinierten statischen Informationen, die in der Registrierung gespeichert sind, und schließlich aus seiner Subnetzadresse.

</dd> <dt>

<span id="Logical_Network_Interfaces"></span><span id="logical_network_interfaces"></span><span id="LOGICAL_NETWORK_INTERFACES"></span>Logische Netzwerkschnittstellen
</dt> <dd>

Für jedes Netzwerk, an das ein Computer angefügt ist, stellt die NLA einen *AdapterName* bereit, der eine physische Schnittstelle wie eine NIC eindeutig identifiziert, oder eine logische Schnittstelle wie eine RAS-Verbindung. AdapterName kann dann mit Funktionen verwendet werden, die in der IP-Hilfs-API verfügbar sind, um weitere Schnittstellenmerkmale zu erhalten.

</dd> </dl>

Die NLA implementiert das logische Netzwerk als Dienstklasse mit einer zugeordneten Klassen-GUID und Eigenschaften. Jedes logische Netzwerk, für das die NLA Informationen zurückgibt, ist eine Instanz dieser Dienstklasse.

 

 



