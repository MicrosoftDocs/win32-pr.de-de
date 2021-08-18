---
title: Konfigurieren von SNMP-Gruppenrichtlinie
description: Wenn Sie das mmc-Snap-In (Microsoft Management Console) für Gruppenrichtlinie verwenden, um registrierungsbasierte Richtlinieneinstellungen zu verwalten, die für SNMP gelten, sind möglicherweise mindestens einer der folgenden Unterschlüssel vorhanden.
ms.assetid: de21d2f5-3337-47ba-afcf-347e289873d3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e17bc3b1bac886a19791f57903920a11062072a81577a0a78ab01d461709ee3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119009658"
---
# <a name="configuring-snmp-group-policy"></a>Konfigurieren von SNMP-Gruppenrichtlinie

Wenn Sie das mmc-Snap-In (Microsoft Management Console) für Gruppenrichtlinie verwenden, um registrierungsbasierte Richtlinieneinstellungen zu verwalten, die für SNMP gelten, sind möglicherweise mindestens einer der folgenden Unterschlüssel vorhanden.

**HKEY \_ LOCAL \_ MACHINE** \\ **SOFTWARE** \\ **Policies** \\ **SNMP** \\ **Parameters** \\ **ValidCommunities**

**HKEY \_ LOCAL \_ MACHINE** \\ **SOFTWARE** \\ **Policies** \\ **SNMP** \\ **Parameters** \\ **PermittedManagers**

**HKEY \_ LOCAL \_ MACHINE** \\ **SOFTWARE** \\ **Policies** \\ **SNMP** \\ **Parameters** \\ **TrapConfiguration**

In der Regel können nur Mitglieder der lokalen Gruppe Administratoren auf die folgenden Registrierungsunterschlüssel zugreifen, die Konfigurationsdaten für den SNMP-Dienst speichern:

**HKEY \_ LOCAL \_ MACHINE** \\ **System** \\ **CurrentControlSet** \\ **Services** \\ **SNMP** \\ **Parameters** \\ **ValidCommunities**

**HKEY \_ LOCAL \_ MACHINE** \\ **System** \\ **CurrentControlSet** \\ **Services** \\ **SNMP** \\ **Parameters** \\ **PermittedManagers**

Weitere Informationen zu registrierungsbasierten Richtlinieneinstellungen finden Sie unter [Informationen Gruppenrichtlinie](/previous-versions/windows/desktop/Policy/about-group-policy).

 

 