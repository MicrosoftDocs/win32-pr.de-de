---
description: Wenn Sie eine Remote Verbindung mit einem Active Directory-Server herstellen, der nicht der in Ihrer aktuellen Domäne ist, müssen Sie den Namen eines Computers angeben, der bereits Mitglied der Domäne ist, die zum gewünschten Active Directory gehört.
ms.assetid: f1478b9d-4a92-4340-8721-1f443eb6ace2
ms.tgt_platform: multiple
title: Beschreiben des LDAP-Namespace
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe1f27c3e2ebc48a0dfa14563822e34bc06d6223
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104050266"
---
# <a name="describing-the-ldap-namespace"></a>Beschreiben des LDAP-Namespace

Wenn Sie eine Remote Verbindung mit einem Active Directory-Server herstellen, der nicht der in Ihrer aktuellen Domäne ist, müssen Sie den Namen eines Computers angeben, der bereits Mitglied der Domäne ist, die zum gewünschten Active Directory gehört.

Geben Sie den folgenden Befehl ein, um eine Remote Verbindung mit einem Computer herzustellen, der bereits Mitglied der Domäne ist, die zum Active Directory-Server gehört.

**\\\\Remote Computer- \\ Stamm \\ Verzeichnis \\ LDAP**

Dieses Beispiel zeigt, dass es zwei Teile gibt, die einen voll qualifizierten Namespace Namen bilden. Der erste Teil ( \\ \\ Remotecomputer) stellt den Computer dar, der bereits Mitglied der Domäne ist, die zum gewünschten Active Directory Server gehört. Der zweite Teil ( \\ Stamm \\ Verzeichnis \\ LDAP) stellt das Active Directory Schema im Verzeichnisdienst Anbieter dar.

> [!Note]  
> Weitere Informationen zur Unterstützung und Installation dieser Komponente auf einem bestimmten Betriebssystem finden Sie unter [Betriebssystem Verfügbarkeit von WMI-Komponenten](operating-system-availability-of-wmi-components.md).

 

 

 



