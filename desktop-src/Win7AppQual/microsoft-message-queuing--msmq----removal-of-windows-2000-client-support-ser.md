---
description: 'Microsoft Message Queuing (MSMQ): Entfernen des Windows 2000-Clientsupportdiensts'
ms.assetid: e29b477e-f7e9-413c-8eb9-2e764b7dd910
title: 'Microsoft Message Queuing (MSMQ): Entfernen des Windows 2000-Clientsupportdiensts'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4be68d40271153567bdaf6b04d73218aaf3d3977
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108088148"
---
# <a name="microsoft-message-queuing-msmq---removal-of-windows-2000-client-support-service"></a>Microsoft Message Queuing (MSMQ): Entfernen des Windows 2000-Clientsupportdiensts

## <a name="affected-platforms"></a>Betroffene Plattformen

**Server** – Windows Server 2008 R2  



## <a name="feature-impact"></a>Auswirkungen auf Das Feature

 **Schweregrad –** Hoch  
**Häufigkeit** : Niedrig  

## <a name="description"></a>BESCHREIBUNG

Der Windows 2000-Clientsupportdienst ist eine optionale Komponente des Message Queuing-Servers, die Sie auf einem Windows 2003- oder Windows 2008-Domänencontrollercomputer installieren können. Dieser Dienst ermöglicht Windows 2000-Clients den Betrieb in einem domänenintegrierten Modus mit einem beliebigen Message Queuing Server, der auf Windows 2003/2008-Computern installiert ist. MSMQ-Clients, die unter Windows XP aufwärts arbeiten, benötigen diesen Dienst nicht.

### <a name="manifestation-of-impact"></a>Wirkungserz weiter

Diese Änderung wirkt sich auf Windows 2000 aus, wenn in einer Windows 7-Domäne interoperiert wird, in der alle Domänencontroller Windows Server 2008 R2 sind. Wenn ein Kunde ein Upgrade auf die Windows 7-Domäne vorliegt, können die vorhandenen MSMQ-Anwendungen auf allen Windows 2000-Computern in der Domäne nicht in einem in die Domäne integrierten Modus ausgeführt werden, es sei denn, diese Clients führen ein Upgrade auf eine höhere Windows-Version durch.

### <a name="mitigation"></a>Minderung

Benutzer mit Windows 2000-Clientcomputern in einer Windows 7-Domäne können einen Windows 2003/2008-Domänencontroller in der Domäne konfigurieren und den MSMQ Windows 2000-Clientsupportdienst auf diesem Domänencontroller installieren.

### <a name="leveraging-feature-capabilities"></a>Nutzen von Featurefunktionen

Benutzer mit Windows 2000-Clientcomputern, auf denen MSMQ ausgeführt wird, sollten ein Upgrade auf eine höhere Windows-Version durchführen, um die Active Directory-basierte Implementierung des MSMQ-Servers nutzen zu können.

### <a name="compatibility-performance-reliability-and-usability-testing"></a>Kompatibilitäts-, Leistungs-, Zuverlässigkeits- und Benutzerfreundlichkeitstests

Benutzer, die über Windows 2000-Clientcomputer verfügen, auf denen MSMQ in einer Windows 7-Domäne mit einem oder mehreren downleveln Domänencontrollern ausgeführt wird, sollten überprüfen, ob ihre Anwendungen in dieser gemischten Domäne funktionieren.

 

 



