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
# <a name="configuring-snmp-group-policy"></a><span data-ttu-id="5a215-103">Konfigurieren von SNMP-Gruppenrichtlinie</span><span class="sxs-lookup"><span data-stu-id="5a215-103">Configuring SNMP Group Policy</span></span>

<span data-ttu-id="5a215-104">Wenn Sie das MMC-Snap-in (Microsoft Management Console) für Gruppenrichtlinie verwenden, um Registrierungs basierte Richtlinien Einstellungen zu verwalten, die für SNMP gelten, kann mindestens einer der folgenden Unterschlüssel vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="5a215-104">If you use the Microsoft Management Console (MMC) snap-in for Group Policy to administer registry-based policy settings that apply to SNMP, one or more of the following subkeys may exist.</span></span>

<span data-ttu-id="5a215-105">**HKEY \_ Software Richtlinien für den lokalen \_ Computer** \\  \\  \\ **SNMP**- \\ **Parameter** \\ **validcommunities**</span><span class="sxs-lookup"><span data-stu-id="5a215-105">**HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Policies**\\**SNMP**\\**Parameters**\\**ValidCommunities**</span></span>

<span data-ttu-id="5a215-106">**HKEY \_ Software Richtlinien für den lokalen \_ Computer** \\  \\  \\ **SNMP**- \\ **Parameter** \\ **permittedmanagers**</span><span class="sxs-lookup"><span data-stu-id="5a215-106">**HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Policies**\\**SNMP**\\**Parameters**\\**PermittedManagers**</span></span>

<span data-ttu-id="5a215-107">**HKEY \_ Richtlinien für lokale \_ Computer** \\ **Software** \\ **Richtlinien** \\ **SNMP**- \\ **Parameter** \\ **trapconfiguration**</span><span class="sxs-lookup"><span data-stu-id="5a215-107">**HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Policies**\\**SNMP**\\**Parameters**\\**TrapConfiguration**</span></span>

<span data-ttu-id="5a215-108">In der Regel können nur Mitglieder der lokalen Gruppe "Administratoren" auf die folgenden Registrierungs Unterschlüssel zugreifen, die Konfigurationsdaten für den SNMP-Dienst speichern:</span><span class="sxs-lookup"><span data-stu-id="5a215-108">Typically, only members of the Administrators local group can access the following registry subkeys that store configuration data for the SNMP service:</span></span>

<span data-ttu-id="5a215-109">**HKEY \_ Lokales \_ Computer** \\ **System** \\ **CurrentControlSet** \\ **Services** \\ **SNMP**- \\ **Parameter** \\ **validcommunities**</span><span class="sxs-lookup"><span data-stu-id="5a215-109">**HKEY\_LOCAL\_MACHINE**\\**System**\\**CurrentControlSet**\\**Services**\\**SNMP**\\**Parameters**\\**ValidCommunities**</span></span>

<span data-ttu-id="5a215-110">**HKEY \_ Lokales \_ Computer** \\ **System** \\ **CurrentControlSet** \\ **Services** \\ **SNMP**- \\ **Parameter** \\ **permittedmanager**</span><span class="sxs-lookup"><span data-stu-id="5a215-110">**HKEY\_LOCAL\_MACHINE**\\**System**\\**CurrentControlSet**\\**Services**\\**SNMP**\\**Parameters**\\**PermittedManagers**</span></span>

<span data-ttu-id="5a215-111">Weitere Informationen zu Registrierungs basierten Richtlinien Einstellungen finden Sie unter [Informationen zu Gruppenrichtlinie](/previous-versions/windows/desktop/Policy/about-group-policy).</span><span class="sxs-lookup"><span data-stu-id="5a215-111">For more information about registry-based policy settings, see [About Group Policy](/previous-versions/windows/desktop/Policy/about-group-policy).</span></span>

 

 