---
description: Wenn Sie eine Remoteverbindung mit einem anderen Active Directory-Server als dem in Ihrer aktuellen Domäne herstellen, müssen Sie den Namen eines Computers angeben, der bereits Mitglied der Domäne ist, die zu dem gewünschten Active Directory gehört.
ms.assetid: f1478b9d-4a92-4340-8721-1f443eb6ace2
ms.tgt_platform: multiple
title: Beschreiben des LDAP-Namespace
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad19ea98e5bd6f36ff78159bfe0a106f0772921c152aa167c38e435732188446
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119568620"
---
# <a name="describing-the-ldap-namespace"></a>Beschreiben des LDAP-Namespace

Wenn Sie eine Remoteverbindung mit einem anderen Active Directory-Server als dem in Ihrer aktuellen Domäne herstellen, müssen Sie den Namen eines Computers angeben, der bereits Mitglied der Domäne ist, die zu dem gewünschten Active Directory gehört.

Geben Sie den folgenden Befehl ein, um eine Remoteverbindung mit einem Computer herzustellen, der bereits Mitglied der Domäne ist, die zum Active Directory-Server gehört.

**\\\\RemoteComputer \\ root \\ directory \\ LDAP**

Dieses Beispiel zeigt, dass es zwei Teile gibt, die einen vollqualifizierten Namespacenamen bilden. Der erste Teil \\ \\ (RemoteComputer) stellt den Computer dar, der bereits Mitglied der Domäne ist, die zum gewünschten Active Directory-Server gehört. Der zweite Teil \\ \\ \\ (Stammverzeichnis-LDAP) stellt das Active Directory-Schema im Verzeichnisdienstanbieter dar.

> [!Note]  
> Weitere Informationen zur Unterstützung und Installation dieser Komponente unter einem bestimmten Betriebssystem finden Sie unter [Betriebssystemverfügbarkeit von WMI-Komponenten.](operating-system-availability-of-wmi-components.md)

 

 

 



