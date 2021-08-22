---
description: 'Microsoft Message Queuing (MSMQ): Entfernen des Windows 2000-Clientsupportdiensts'
ms.assetid: e29b477e-f7e9-413c-8eb9-2e764b7dd910
title: 'Microsoft Message Queuing (MSMQ): Entfernen des Windows 2000-Clientsupportdiensts'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8bdcba684faa0a25994f66cc9cd205ba22b5ed949d8dcdd3e67497484f2784ff
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119053048"
---
# <a name="microsoft-message-queuing-msmq---removal-of-windows-2000-client-support-service"></a>Microsoft Message Queuing (MSMQ): Entfernen des Windows 2000-Clientsupportdiensts

## <a name="affected-platforms"></a>Betroffene Plattformen

**Server** – Windows Server 2008 R2  



## <a name="feature-impact"></a>Auswirkungen auf Features

 **Schweregrad –** Hoch  
**Häufigkeit** : Niedrig  

## <a name="description"></a>Beschreibung

Der Windows 2000-Clientsupportdienst ist eine optionale Komponente des Message Queuing-Servers, die Sie auf einem Windows 2003- oder Windows 2008-Domänencontrollercomputer installieren können. Dieser Dienst ermöglicht Windows 2000-Clients den Betrieb in einem domänenintegrierten Modus mit einem beliebigen Message Queuing Server, der auf Windows 2003/2008-Computern installiert ist. MSMQ-Clients, die auf Windows XP aufwärts arbeiten, benötigen diesen Dienst nicht.

### <a name="manifestation-of-impact"></a>Auswirkungen

Diese Änderung wirkt sich auf Windows 2000 aus, wenn in einer Windows 7-Domäne interoperiert wird, in der alle Domänencontroller Windows Server 2008 R2 sind. Wenn ein Kunde auf die Domäne Windows 7 aktualisiert, können die vorhandenen MSMQ-Anwendungen auf allen Windows 2000 Computern in der Domäne nicht in einem domänenintegrierbaren Modus ausgeführt werden, es sei denn, diese Clients führen ein Upgrade auf eine höhere Windows-Version durch.

### <a name="mitigation"></a>Minderung

Benutzer mit Windows 2000-Clientcomputern in einer Windows 7-Domäne können einen Windows 2003/2008-Domänencontroller in der Domäne konfigurieren und den MSMQ Windows 2000-Clientsupportdienst auf diesem Domänencontroller installieren.

### <a name="leveraging-feature-capabilities"></a>Nutzen von Featurefunktionen

Benutzer mit Windows 2000-Clientcomputern, auf denen MSMQ ausgeführt wird, sollten ein Upgrade auf eine höhere Windows Version durchführen, um die Active Directory-basierte Implementierung des MSMQ-Servers nutzen zu können.

### <a name="compatibility-performance-reliability-and-usability-testing"></a>Kompatibilitäts-, Leistungs-, Zuverlässigkeits- und Benutzerfreundlichkeitstests

Benutzer mit Windows 2000-Clientcomputern, auf denen MSMQ in einer Windows 7-Domäne mit einem oder mehreren down-level-Domänencontrollern ausgeführt wird, sollten überprüfen, ob ihre Anwendungen in dieser gemischten Domäne funktionieren.

 

 



