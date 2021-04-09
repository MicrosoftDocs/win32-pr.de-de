---
description: .
ms.assetid: e29b477e-f7e9-413c-8eb9-2e764b7dd910
title: Microsoft Message Queuing (MSMQ)-Entfernen des Windows 2000-Client Unterstützungs Dienstanbieter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54688ee4ad24eb691c95e4d70ce0acb881e212eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104050306"
---
# <a name="microsoft-message-queuing-msmq---removal-of-windows-2000-client-support-service"></a>Microsoft Message Queuing (MSMQ)-Entfernen des Windows 2000-Client Unterstützungs Dienstanbieter

## <a name="affected-platforms"></a>Betroffene Plattformen

**Server** -Windows Server 2008 R2  



## <a name="feature-impact"></a>Auswirkungen von Features

 **Schweregrad** -hoch  
**Häufigkeit** -niedrig  

## <a name="description"></a>BESCHREIBUNG

Der Windows 2000-Client Support Dienst ist eine optionale Komponente des Message Queuing Servers, den Sie auf einem Windows 2003-oder Windows 2008-Domänen Controller Computer installieren können. Dieser Dienst ermöglicht den Betrieb von Windows 2000-Clients in einem Domänen integrierten Modus mit jedem Message Queuing Server, der auf Windows 2003/2008-Computern installiert ist. MSMQ-Clients, die unter Windows XP aufwärts betrieben werden, benötigen diesen Dienst nicht.

### <a name="manifestation-of-impact"></a>Erscheinung der Auswirkung

Diese Änderung wirkt sich auf Windows 2000 aus, wenn Sie in einer Windows 7-Domäne interagiert, in der alle Domänen Controller Windows Server 2008 R2 sind. Wenn ein Kunde ein Upgrade auf die Windows 7-Domäne durchführt, können die vorhandenen MSMQ-Anwendungen auf allen Windows 2000-Computern in der Domäne nicht in einem Domänen integrierten Modus ausgeführt werden, es sei denn, diese Clients führen ein Upgrade auf eine höhere Windows-Version durch.

### <a name="mitigation"></a>Minderung

Benutzer mit Windows 2000-Client Computern in einer Windows 7-Domäne können einen Windows 2003/2008-Domänen Controller in der Domäne konfigurieren und den MSMQ Windows 2000-Client Unterstützungsdienst auf diesem Domänen Controller installieren.

### <a name="leveraging-feature-capabilities"></a>Nutzen von Featurefunktionen

Benutzer mit Windows 2000-Client Computern, auf denen MSMQ ausgeführt wird, sollten auf eine höhere Windows-Version aktualisieren, um die Active Directory basierte Implementierung des MSMQ-Servers zu nutzen.

### <a name="compatibility-performance-reliability-and-usability-testing"></a>Tests der Kompatibilität, Leistung, Zuverlässigkeit und Benutzerfreundlichkeit

Benutzer mit Windows 2000-Client Computern, auf denen MSMQ in einer Windows 7-Domäne mit einem oder mehreren untergeordneten Domänen Controllern ausgeführt wird, sollten überprüfen, ob Ihre Anwendungen in dieser gemischten Domäne funktionsfähig sind.

 

 



