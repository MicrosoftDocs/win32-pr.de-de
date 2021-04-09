---
title: Konfigurieren von SNMP-Gruppenrichtlinie
description: Wenn Sie das MMC-Snap-in (Microsoft Management Console) für Gruppenrichtlinie verwenden, um Registrierungs basierte Richtlinien Einstellungen zu verwalten, die für SNMP gelten, kann mindestens einer der folgenden Unterschlüssel vorhanden sein.
ms.assetid: de21d2f5-3337-47ba-afcf-347e289873d3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 817797dbc0e67f6006e12751beca533cbbec3656
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104102114"
---
# <a name="configuring-snmp-group-policy"></a>Konfigurieren von SNMP-Gruppenrichtlinie

Wenn Sie das MMC-Snap-in (Microsoft Management Console) für Gruppenrichtlinie verwenden, um Registrierungs basierte Richtlinien Einstellungen zu verwalten, die für SNMP gelten, kann mindestens einer der folgenden Unterschlüssel vorhanden sein.

**HKEY \_ Software Richtlinien für den lokalen \_ Computer** \\  \\  \\ **SNMP**- \\ **Parameter** \\ **validcommunities**

**HKEY \_ Software Richtlinien für den lokalen \_ Computer** \\  \\  \\ **SNMP**- \\ **Parameter** \\ **permittedmanagers**

**HKEY \_ Richtlinien für lokale \_ Computer** \\ **Software** \\ **Richtlinien** \\ **SNMP**- \\ **Parameter** \\ **trapconfiguration**

In der Regel können nur Mitglieder der lokalen Gruppe "Administratoren" auf die folgenden Registrierungs Unterschlüssel zugreifen, die Konfigurationsdaten für den SNMP-Dienst speichern:

**HKEY \_ Lokales \_ Computer** \\ **System** \\ **CurrentControlSet** \\ **Services** \\ **SNMP**- \\ **Parameter** \\ **validcommunities**

**HKEY \_ Lokales \_ Computer** \\ **System** \\ **CurrentControlSet** \\ **Services** \\ **SNMP**- \\ **Parameter** \\ **permittedmanager**

Weitere Informationen zu Registrierungs basierten Richtlinien Einstellungen finden Sie unter [Informationen zu Gruppenrichtlinie](/previous-versions/windows/desktop/Policy/about-group-policy).

 

 