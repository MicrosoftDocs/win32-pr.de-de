---
description: Mit Energie Einstellungs-GUIDs werden Energie Änderungs Ereignisse identifiziert.
ms.assetid: 39D432A7-54F8-4135-B98C-7290F95B054A
title: Energie Einstellungs-GUIDs (WinNT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b67dfd619d93f4318dbcfe2b44b5f8ba24460bd3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354778"
---
# <a name="power-setting-guids"></a><span data-ttu-id="02db1-103">Energie Einstellungs-GUIDs</span><span class="sxs-lookup"><span data-stu-id="02db1-103">Power Setting GUIDs</span></span>

<span data-ttu-id="02db1-104">Mit der Energie Einstellungs- **GUID** s werden Strom Änderungs Ereignisse identifiziert.</span><span class="sxs-lookup"><span data-stu-id="02db1-104">Power setting **GUID** s identify power change events.</span></span> <span data-ttu-id="02db1-105">In diesem Thema werden die Energie Einstellungs- **GUID** s für Benachrichtigungen aufgelistet, die für-Anwendungen am nützlichsten sind.</span><span class="sxs-lookup"><span data-stu-id="02db1-105">This topic lists power setting **GUID** s for notifications that are most useful to applications.</span></span> <span data-ttu-id="02db1-106">Eine Anwendung sollte für jedes Strom Änderungs Ereignis registriert werden, das sich auf das Verhalten auswirken könnte.</span><span class="sxs-lookup"><span data-stu-id="02db1-106">An application should register for each power change event that might impact its behavior.</span></span> <span data-ttu-id="02db1-107">Die Benachrichtigung wird jedes Mal gesendet, wenn eine Einstellung geändert wird.</span><span class="sxs-lookup"><span data-stu-id="02db1-107">Notification is sent each time a setting changes.</span></span>

<span data-ttu-id="02db1-108">Die Energie Einstellungs- **GUID** s sind in "Winnt. h" definiert.</span><span class="sxs-lookup"><span data-stu-id="02db1-108">Power setting **GUID** s are defined in WinNT.h.</span></span>

<dl> <dt>

<span data-ttu-id="02db1-109"><span id="GUID_ACDC_POWER_SOURCE"></span><span id="guid_acdc_power_source"></span>**GUID- \_ ACDC- \_ Strom \_ Quelle**</span><span class="sxs-lookup"><span data-stu-id="02db1-109"><span id="GUID_ACDC_POWER_SOURCE"></span><span id="guid_acdc_power_source"></span>**GUID\_ACDC\_POWER\_SOURCE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="02db1-110">5d3e9a59-e9d5-4b00-a6bd-ff34ff516548</span><span class="sxs-lookup"><span data-stu-id="02db1-110">5D3E9A59-E9D5-4B00-A6BD-FF34FF516548</span></span>
</dt> <dt>



<span data-ttu-id="02db1-111">Die Stromquelle des Systems hat sich geändert.</span><span class="sxs-lookup"><span data-stu-id="02db1-111">The system power source has changed.</span></span> <span data-ttu-id="02db1-112">Der **Datenmember** ist ein **DWORD** mit Werten aus der [**\_ systemstrombedingungs \_**](/windows/desktop/api/WinNT/ne-winnt-system_power_condition) -Enumeration, die die aktuelle Stromquelle angibt.</span><span class="sxs-lookup"><span data-stu-id="02db1-112">The **Data** member is a **DWORD** with values from the [**SYSTEM\_POWER\_CONDITION**](/windows/desktop/api/WinNT/ne-winnt-system_power_condition) enumeration that indicates the current power source.</span></span>

<dl> <dt>

<span data-ttu-id="02db1-113">**POAC** (0): der Computer wird durch eine Stromversorgung der Stromversorgung (oder ähnliches, z. b. durch einen 12-v-Auto Mobil Adapter) betrieben.</span><span class="sxs-lookup"><span data-stu-id="02db1-113">**PoAc** (0) - The computer is powered by an AC power source (or similar, such as a laptop powered by a 12V automotive adapter).</span></span>
</dt> <dt>

<span data-ttu-id="02db1-114">**PODC** (1): der Computer wird durch eine Stromquelle für den Akku Betrieb betrieben.</span><span class="sxs-lookup"><span data-stu-id="02db1-114">**PoDc** (1) - The computer is powered by an onboard battery power source.</span></span>
</dt> <dt>

<span data-ttu-id="02db1-115">**Pohot** (2): der Computer wird durch eine kurzfristige Stromquelle, z. b. ein UPS-Gerät, betrieben.</span><span class="sxs-lookup"><span data-stu-id="02db1-115">**PoHot** (2) - The computer is powered by a short-term power source such as a UPS device.</span></span>
</dt> </dl>

</dl> </dd> <dt>

<span data-ttu-id="02db1-116"><span id="GUID_BATTERY_PERCENTAGE_REMAINING"></span><span id="guid_battery_percentage_remaining"></span>**\_ \_ verbleibender GUID-Akku Anteil \_**</span><span class="sxs-lookup"><span data-stu-id="02db1-116"><span id="GUID_BATTERY_PERCENTAGE_REMAINING"></span><span id="guid_battery_percentage_remaining"></span>**GUID\_BATTERY\_PERCENTAGE\_REMAINING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="02db1-117">A7AD8041-B45A-4CAE-87A3-EECBB468A9E1</span><span class="sxs-lookup"><span data-stu-id="02db1-117">A7AD8041-B45A-4CAE-87A3-EECBB468A9E1</span></span>
</dt> <dt>



<span data-ttu-id="02db1-118">Die verbleibende Akkukapazität hat sich geändert.</span><span class="sxs-lookup"><span data-stu-id="02db1-118">The remaining battery capacity has changed.</span></span> <span data-ttu-id="02db1-119">Die Granularität variiert von System zu System, die feinste Granularität ist jedoch 1 Prozent.</span><span class="sxs-lookup"><span data-stu-id="02db1-119">The granularity varies from system to system but the finest granularity is 1 percent.</span></span> <span data-ttu-id="02db1-120">Der **Datenmember** ist ein **DWORD** , das die aktuelle Akkukapazität angibt, die als Prozentsatz zwischen 0 und 100 verbleiben.</span><span class="sxs-lookup"><span data-stu-id="02db1-120">The **Data** member is a **DWORD** that indicates the current battery capacity remaining as a percentage from 0 through 100.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="02db1-121"><span id="GUID_CONSOLE_DISPLAY_STATE"></span><span id="guid_console_display_state"></span>**\_ \_ Anzeige \_ Status der GUID-Konsole**</span><span class="sxs-lookup"><span data-stu-id="02db1-121"><span id="GUID_CONSOLE_DISPLAY_STATE"></span><span id="guid_console_display_state"></span>**GUID\_CONSOLE\_DISPLAY\_STATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="02db1-122">6fe69556-704A-47a0-8F 24-c28d936fida47</span><span class="sxs-lookup"><span data-stu-id="02db1-122">6FE69556-704A-47A0-8F24-C28D936FDA47</span></span>
</dt> <dt>



<span data-ttu-id="02db1-123">Der Anzeige Zustand des aktuellen Monitors hat sich geändert.</span><span class="sxs-lookup"><span data-stu-id="02db1-123">The current monitor's display state has changed.</span></span>

<span data-ttu-id="02db1-124">**Windows 7, Windows Server 2008 R2, Windows Vista und Windows Server 2008:** Diese Benachrichtigung ist ab Windows 8 und Windows Server 2012 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="02db1-124">**Windows 7, Windows Server 2008 R2, Windows Vista and Windows Server 2008:** This notification is available starting with Windows 8 and Windows Server 2012.</span></span>

<span data-ttu-id="02db1-125">Der **Datenmember** ist ein **DWORD** mit einem der folgenden Werte.</span><span class="sxs-lookup"><span data-stu-id="02db1-125">The **Data** member is a **DWORD** with one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="02db1-126">0x0-die Anzeige ist deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="02db1-126">0x0 - The display is off.</span></span>
</dt> <dt>

<span data-ttu-id="02db1-127">0x1-die Anzeige ist on.</span><span class="sxs-lookup"><span data-stu-id="02db1-127">0x1 - The display is on.</span></span>
</dt> <dt>

<span data-ttu-id="02db1-128">0x2-die Anzeige ist abgedimmt.</span><span class="sxs-lookup"><span data-stu-id="02db1-128">0x2 - The display is dimmed.</span></span>
</dt> </dl>

</dl> </dd> <dt>

<span data-ttu-id="02db1-129"><span id="GUID_GLOBAL_USER_PRESENCE"></span><span id="guid_global_user_presence"></span>**globale GUID- \_ \_ Benutzer \_ Präsenz**</span><span class="sxs-lookup"><span data-stu-id="02db1-129"><span id="GUID_GLOBAL_USER_PRESENCE"></span><span id="guid_global_user_presence"></span>**GUID\_GLOBAL\_USER\_PRESENCE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="02db1-130">786e8a1d-B427-4344-9207-09e70bdcbea9</span><span class="sxs-lookup"><span data-stu-id="02db1-130">786E8A1D-B427-4344-9207-09E70BDCBEA9</span></span>
</dt> <dt>



<span data-ttu-id="02db1-131">Der Benutzer Status, der einer Sitzung zugeordnet ist, wurde geändert.</span><span class="sxs-lookup"><span data-stu-id="02db1-131">The user status associated with any session has changed.</span></span> <span data-ttu-id="02db1-132">Dies stellt den kombinierten Status der Benutzer Präsenz in allen lokalen und Remote Sitzungen des Systems dar.</span><span class="sxs-lookup"><span data-stu-id="02db1-132">This represents the combined status of user presence across all local and remote sessions on the system.</span></span>

<span data-ttu-id="02db1-133">Dieser Benachrichtigung werden nur Dienste und andere Programme, die in Sitzung 0 ausgeführt werden, gesendet.</span><span class="sxs-lookup"><span data-stu-id="02db1-133">This notification is sent only services and other programs running in session 0.</span></span> <span data-ttu-id="02db1-134">Benutzermodusanwendungen sollten sich stattdessen für die **\_ \_ Benutzer \_ Präsenz der GUID-Sitzung** registrieren.</span><span class="sxs-lookup"><span data-stu-id="02db1-134">User-mode applications should register for **GUID\_SESSION\_USER\_PRESENCE** instead.</span></span>

<span data-ttu-id="02db1-135">**Windows 7, Windows Server 2008 R2, Windows Vista und Windows Server 2008:** Diese Benachrichtigung ist ab Windows 8 und Windows Server 2012 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="02db1-135">**Windows 7, Windows Server 2008 R2, Windows Vista and Windows Server 2008:** This notification is available starting with Windows 8 and Windows Server 2012.</span></span>

<span data-ttu-id="02db1-136">Der **Datenmember** ist ein **DWORD** mit einem der folgenden Werte.</span><span class="sxs-lookup"><span data-stu-id="02db1-136">The **Data** member is a **DWORD** with one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="02db1-137">**Poweruserpresent** (0): der Benutzer ist in einer lokalen oder Remote Sitzung auf dem System vorhanden.</span><span class="sxs-lookup"><span data-stu-id="02db1-137">**PowerUserPresent** (0) - The user is present in any local or remote session on the system.</span></span>
</dt> <dt>

<span data-ttu-id="02db1-138">**Poweruserinaktiv** (2): der Benutzer ist in keiner lokalen oder Remote Sitzung auf dem System vorhanden.</span><span class="sxs-lookup"><span data-stu-id="02db1-138">**PowerUserInactive** (2) - The user is not present in any local or remote session on the system.</span></span>
</dt> </dl>

</dl> </dd> <dt>

<span data-ttu-id="02db1-139"><span id="GUID_IDLE_BACKGROUND_TASK"></span><span id="guid_idle_background_task"></span>**GUID \_ - \_ Hintergrund \_ Aufgabe im Leerlauf**</span><span class="sxs-lookup"><span data-stu-id="02db1-139"><span id="GUID_IDLE_BACKGROUND_TASK"></span><span id="guid_idle_background_task"></span>**GUID\_IDLE\_BACKGROUND\_TASK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="02db1-140">515c31d8-f 734-163D-a0ld-11a08c91e8f 1</span><span class="sxs-lookup"><span data-stu-id="02db1-140">515C31D8-F734-163D-A0FD-11A08C91E8F1</span></span>
</dt> <dt>



<span data-ttu-id="02db1-141">Das System ist ausgelastet.</span><span class="sxs-lookup"><span data-stu-id="02db1-141">The system is busy.</span></span> <span data-ttu-id="02db1-142">Dies weist darauf hin, dass das System in naher Zukunft nicht in den Leerlauf wechselt und dass die aktuelle Zeit für Komponenten zum Ausführen von Hintergrund-oder Leerlauf Aufgaben geeignet ist, die andernfalls verhindern, dass der Computer in den Leerlauf wechselt.</span><span class="sxs-lookup"><span data-stu-id="02db1-142">This indicates that the system will not be moving into an idle state in the near future and that the current time is a good time for components to perform background or idle tasks that would otherwise prevent the computer from entering an idle state.</span></span>

<span data-ttu-id="02db1-143">Es gibt keine Benachrichtigung, wenn sich das System in den Leerlauf versetzen kann.</span><span class="sxs-lookup"><span data-stu-id="02db1-143">There is no notification when the system is able to move into an idle state.</span></span> <span data-ttu-id="02db1-144">Die Benachrichtigung im Hintergrund des Hintergrund Tasks gibt nicht an, ob ein Benutzer auf dem Computer vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="02db1-144">The idle background task notification does not indicate whether a user is present at the computer.</span></span> <span data-ttu-id="02db1-145">Der **Datenmember** weist keine Informationen auf und kann ignoriert werden.</span><span class="sxs-lookup"><span data-stu-id="02db1-145">The **Data** member has no information and can be ignored.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="02db1-146"><span id="GUID_MONITOR_POWER_ON"></span><span id="guid_monitor_power_on"></span>**\_ \_ Einschalten des GUID-Monitors \_**</span><span class="sxs-lookup"><span data-stu-id="02db1-146"><span id="GUID_MONITOR_POWER_ON"></span><span id="guid_monitor_power_on"></span>**GUID\_MONITOR\_POWER\_ON**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="02db1-147">02731015-4510-4526-99e6-e5a17ebd1aea</span><span class="sxs-lookup"><span data-stu-id="02db1-147">02731015-4510-4526-99E6-E5A17EBD1AEA</span></span>
</dt> <dt>



<span data-ttu-id="02db1-148">Der primäre System Monitor wurde eingeschaltet oder ausgeschaltet.</span><span class="sxs-lookup"><span data-stu-id="02db1-148">The primary system monitor has been powered on or off.</span></span> <span data-ttu-id="02db1-149">Diese Benachrichtigung ist nützlich für Komponenten, die Inhalte aktiv auf dem Anzeigegerät darstellen, wie z. b. Medien Visualisierung.</span><span class="sxs-lookup"><span data-stu-id="02db1-149">This notification is useful for components that actively render content to the display device, such as media visualization.</span></span> <span data-ttu-id="02db1-150">Diese Anwendungen sollten sich für diese Benachrichtigung registrieren und das Rendering von Grafikinhalten beenden, wenn der Monitor deaktiviert ist, um den Energieverbrauch des Systems zu reduzieren.</span><span class="sxs-lookup"><span data-stu-id="02db1-150">These applications should register for this notification and stop rendering graphics content when the monitor is off to reduce system power consumption.</span></span> <span data-ttu-id="02db1-151">Der **Datenmember** ist ein **DWORD** , das den aktuellen Monitor Zustand angibt.</span><span class="sxs-lookup"><span data-stu-id="02db1-151">The **Data** member is a **DWORD** that indicates the current monitor state.</span></span>

<dl> <dt>

<span data-ttu-id="02db1-152">0x0-der Monitor ist deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="02db1-152">0x0 - The monitor is off.</span></span>
</dt> <dt>

<span data-ttu-id="02db1-153">0x1-der Monitor ist on.</span><span class="sxs-lookup"><span data-stu-id="02db1-153">0x1 - The monitor is on.</span></span>
</dt> </dl>

<span data-ttu-id="02db1-154">**Windows 8 und Windows Server 2012:** In neuen Anwendungen sollte der **\_ \_ Anzeige \_ Zustand der GUID-Konsole** anstelle dieser Benachrichtigung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="02db1-154">**Windows 8 and Windows Server 2012:** New applications should use **GUID\_CONSOLE\_DISPLAY\_STATE** instead of this notification.</span></span>

</dl> </dd> <dt>

<span data-ttu-id="02db1-155"><span id="GUID_POWER_SAVING_STATUS"></span><span id="guid_power_saving_status"></span>**GUID- \_ Energie \_ Spar \_ Status**</span><span class="sxs-lookup"><span data-stu-id="02db1-155"><span id="GUID_POWER_SAVING_STATUS"></span><span id="guid_power_saving_status"></span>**GUID\_POWER\_SAVING\_STATUS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="02db1-156">E00958C0-C213-4ACE-AC77-FECCED2EEEA5</span><span class="sxs-lookup"><span data-stu-id="02db1-156">E00958C0-C213-4ACE-AC77-FECCED2EEEA5</span></span>
</dt> <dt>



<span data-ttu-id="02db1-157">Der Akku Schoner wurde als Reaktion auf veränderliche Energiebedingungen ausgeschaltet oder eingeschaltet.</span><span class="sxs-lookup"><span data-stu-id="02db1-157">Battery saver has been turned off or on in response to changing power conditions.</span></span> <span data-ttu-id="02db1-158">Diese Benachrichtigung ist nützlich für Komponenten, die an der Energieeinsparung beteiligt sind.</span><span class="sxs-lookup"><span data-stu-id="02db1-158">This notification is useful for components that participate in energy conservation.</span></span> <span data-ttu-id="02db1-159">Diese Anwendungen sollten sich für diese Benachrichtigung registrieren und die Stromversorgung einsparen, wenn der Akku Schoner eingeschaltet ist.</span><span class="sxs-lookup"><span data-stu-id="02db1-159">These applications should register for this notification and save power when battery saver is on.</span></span>

<span data-ttu-id="02db1-160">Der **Datenmember** ist ein **DWORD** , das den Akku Zustand angibt.</span><span class="sxs-lookup"><span data-stu-id="02db1-160">The **Data** member is a **DWORD** that indicates battery saver state.</span></span>

<dl> <dt>

<span data-ttu-id="02db1-161">0x0-Akku Schoner ist deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="02db1-161">0x0 - Battery saver is off.</span></span>
</dt> <dt>

<span data-ttu-id="02db1-162">0x1-Akku Schoner ist eingeschaltet.</span><span class="sxs-lookup"><span data-stu-id="02db1-162">0x1 - Battery saver is on.</span></span> <span data-ttu-id="02db1-163">Sparen Sie nach Möglichkeit Energie.</span><span class="sxs-lookup"><span data-stu-id="02db1-163">Save energy where possible.</span></span>
</dt> </dl>

<span data-ttu-id="02db1-164">Allgemeine Informationen zum Akku Schoner finden Sie unter [Batterie Schoner (in den Richtlinien für die Hardwarekomponente)](/windows-hardware/design/component-guidelines/battery-saver).</span><span class="sxs-lookup"><span data-stu-id="02db1-164">For general information about battery saver, see [battery saver (in the hardware component guidelines)](/windows-hardware/design/component-guidelines/battery-saver).</span></span>

</dl> </dd> <dt>

<span data-ttu-id="02db1-165"><span id="GUID_POWERSCHEME_PERSONALITY"></span><span id="guid_powerscheme_personality"></span>**GUID- \_ powerscheme- \_ Persönlichkeit**</span><span class="sxs-lookup"><span data-stu-id="02db1-165"><span id="GUID_POWERSCHEME_PERSONALITY"></span><span id="guid_powerscheme_personality"></span>**GUID\_POWERSCHEME\_PERSONALITY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="02db1-166">245d8541-3943-4422-B025-13a784f 679b7</span><span class="sxs-lookup"><span data-stu-id="02db1-166">245d8541-3943-4422-b025-13A784F679B7</span></span>
</dt> <dt>



<span data-ttu-id="02db1-167">Die aktive Energie Schema-Persönlichkeit hat sich geändert.</span><span class="sxs-lookup"><span data-stu-id="02db1-167">The active power scheme personality has changed.</span></span> <span data-ttu-id="02db1-168">Alle Energie Schemas werden einer dieser Persönlichkeiten zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="02db1-168">All power schemes map to one of these personalities.</span></span> <span data-ttu-id="02db1-169">Der **Datenmember** ist eine **GUID** , die die neue aktive Energie Schema-Persönlichkeit angibt.</span><span class="sxs-lookup"><span data-stu-id="02db1-169">The **Data** member is a **GUID** that indicates the new active power scheme personality.</span></span>

<dl> <dt>



<span data-ttu-id="02db1-170">**GUID \_ Minimale \_ Energie \_ Einsparung** (8c5e7f da-e8bf -4a96-9a85-a6e23a8c635c)</span><span class="sxs-lookup"><span data-stu-id="02db1-170">**GUID\_MIN\_POWER\_SAVINGS** (8C5E7FDA-E8BF-4A96-9A85-A6E23A8C635C)</span></span>

<span data-ttu-id="02db1-171">Hohe Leistung: das Schema ist darauf ausgelegt, eine maximale Leistung auf Kosten der Stromverbrauchs Einsparungen zu erzielen.</span><span class="sxs-lookup"><span data-stu-id="02db1-171">High Performance - The scheme is designed to deliver maximum performance at the expense of power consumption savings.</span></span>


</dt> <dt>



<span data-ttu-id="02db1-172">**GUID \_ Maximale \_ Energie \_ Einsparung** (A1841308-3541-4FAB-BC81-F71556F20B4A)</span><span class="sxs-lookup"><span data-stu-id="02db1-172">**GUID\_MAX\_POWER\_SAVINGS** (A1841308-3541-4FAB-BC81-F71556F20B4A)</span></span>

<span data-ttu-id="02db1-173">Energiesparmodus: das Schema ist so konzipiert, dass es auf Kosten der Systemleistung und Reaktionsfähigkeit einen maximalen Stromverbrauch ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="02db1-173">Power Saver - The scheme is designed to deliver maximum power consumption savings at the expense of system performance and responsiveness.</span></span>


</dt> <dt>



<span data-ttu-id="02db1-174">**GUID \_ Typische \_ Strom \_ Einsparung** (381b4222-f694-41f0-9685-ff5bb260df2e)</span><span class="sxs-lookup"><span data-stu-id="02db1-174">**GUID\_TYPICAL\_POWER\_SAVINGS** (381B4222-F694-41F0-9685-FF5BB260DF2E)</span></span>

<span data-ttu-id="02db1-175">Automatisch: das Schema ist so konzipiert, dass die Leistung und der Energieverbrauch automatisch ausgeglichen werden.</span><span class="sxs-lookup"><span data-stu-id="02db1-175">Automatic - The scheme is designed to automatically balance performance and power consumption savings.</span></span>


</dt> </dl>

</dl> </dd> <dt>

<span data-ttu-id="02db1-176"><span id="GUID_SESSION_DISPLAY_STATUS"></span><span id="guid_session_display_status"></span>**\_ \_ Anzeige \_ Status der GUID-Sitzung**</span><span class="sxs-lookup"><span data-stu-id="02db1-176"><span id="GUID_SESSION_DISPLAY_STATUS"></span><span id="guid_session_display_status"></span>**GUID\_SESSION\_DISPLAY\_STATUS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="02db1-177">2b84 c20e-AD23-4ddf-93dB-05ffbd7efca5</span><span class="sxs-lookup"><span data-stu-id="02db1-177">2B84C20E-AD23-4ddf-93DB-05FFBD7EFCA5</span></span>
</dt> <dt>



<span data-ttu-id="02db1-178">Die Anzeige, die der Sitzung der Anwendung zugeordnet ist, wurde eingeschaltet oder deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="02db1-178">The display associated with the application's session has been powered on or off.</span></span>

<span data-ttu-id="02db1-179">**Windows 7, Windows Server 2008 R2, Windows Vista und Windows Server 2008:** Diese Benachrichtigung ist ab Windows 8 und Windows Server 2012 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="02db1-179">**Windows 7, Windows Server 2008 R2, Windows Vista and Windows Server 2008:** This notification is available starting with Windows 8 and Windows Server 2012.</span></span>

<span data-ttu-id="02db1-180">Diese Benachrichtigung wird nur an Benutzermodusanwendungen gesendet.</span><span class="sxs-lookup"><span data-stu-id="02db1-180">This notification is sent only to user-mode applications.</span></span> <span data-ttu-id="02db1-181">Dienste und andere Programme, die in Sitzung 0 ausgeführt werden, erhalten diese Benachrichtigung nicht.</span><span class="sxs-lookup"><span data-stu-id="02db1-181">Services and other programs running in session 0 do not receive this notification.</span></span> <span data-ttu-id="02db1-182">Der **Datenmember** ist ein **DWORD** mit einem der folgenden Werte.</span><span class="sxs-lookup"><span data-stu-id="02db1-182">The **Data** member is a **DWORD** with one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="02db1-183">0x0-die Anzeige ist deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="02db1-183">0x0 - The display is off.</span></span>
</dt> <dt>

<span data-ttu-id="02db1-184">0x1-die Anzeige ist on.</span><span class="sxs-lookup"><span data-stu-id="02db1-184">0x1 - The display is on.</span></span>
</dt> <dt>

<span data-ttu-id="02db1-185">0x2-die Anzeige ist abgedimmt.</span><span class="sxs-lookup"><span data-stu-id="02db1-185">0x2 - The display is dimmed.</span></span>
</dt> </dl>

</dl> </dd> <dt>

<span data-ttu-id="02db1-186"><span id="GUID_SESSION_USER_PRESENCE"></span><span id="guid_session_user_presence"></span>**\_ \_ Benutzer \_ Präsenz in GUID-Sitzung**</span><span class="sxs-lookup"><span data-stu-id="02db1-186"><span id="GUID_SESSION_USER_PRESENCE"></span><span id="guid_session_user_presence"></span>**GUID\_SESSION\_USER\_PRESENCE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="02db1-187">3c0f 4548-c03f -4c4d-b9f 2-237ede686376</span><span class="sxs-lookup"><span data-stu-id="02db1-187">3C0F4548-C03F-4c4d-B9F2-237EDE686376</span></span>
</dt> <dt>



<span data-ttu-id="02db1-188">Der Benutzer Status, der der Sitzung der Anwendung zugeordnet ist, wurde geändert.</span><span class="sxs-lookup"><span data-stu-id="02db1-188">The user status associated with the application's session has changed.</span></span>

<span data-ttu-id="02db1-189">**Windows 7, Windows Server 2008 R2, Windows Vista und Windows Server 2008:** Diese Benachrichtigung ist ab Windows 8 und Windows Server 2012 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="02db1-189">**Windows 7, Windows Server 2008 R2, Windows Vista and Windows Server 2008:** This notification is available starting with Windows 8 and Windows Server 2012.</span></span>

<span data-ttu-id="02db1-190">Diese Benachrichtigung wird nur an Benutzermodusanwendungen gesendet, die in einer interaktiven Sitzung ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="02db1-190">This notification is sent only to user-mode applications running in an interactive session.</span></span> <span data-ttu-id="02db1-191">Dienste und andere Programme, die in Sitzung 0 ausgeführt werden, sollten sich für die **globale GUID- \_ \_ Benutzer \_ Präsenz** registrieren.</span><span class="sxs-lookup"><span data-stu-id="02db1-191">Services and other programs running in session 0 should register for **GUID\_GLOBAL\_USER\_PRESENCE**.</span></span> <span data-ttu-id="02db1-192">Der **Datenmember** ist ein **DWORD** mit einem der folgenden Werte.</span><span class="sxs-lookup"><span data-stu-id="02db1-192">The **Data** member is a **DWORD** with one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="02db1-193">**Poweruserpresent** (0): der Benutzer stellt Eingaben für die Sitzung bereit.</span><span class="sxs-lookup"><span data-stu-id="02db1-193">**PowerUserPresent** (0) - The user is providing input to the session.</span></span>
</dt> <dt>

<span data-ttu-id="02db1-194">**Poweruserinaktiv** (2): das Timeout der Benutzeraktivität ist ohne Interaktion mit dem Benutzer abgelaufen.</span><span class="sxs-lookup"><span data-stu-id="02db1-194">**PowerUserInactive** (2) - The user activity timeout has elapsed with no interaction from the user.</span></span>
</dt> </dl>

> [!Note]  
> <span data-ttu-id="02db1-195">Diese Einstellung sollte von allen Anwendungen verwendet werden, die in einer interaktiven benutzermodussitzung ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="02db1-195">All applications that run in an interactive user-mode session should use this setting.</span></span> <span data-ttu-id="02db1-196">Wenn kernelmodusanwendungen den Monitor Status registrieren, sollten Sie stattdessen den **\_ \_ Anzeige \_ Status der GUID-Konsole** verwenden.</span><span class="sxs-lookup"><span data-stu-id="02db1-196">When kernel mode applications register for monitor status they should use **GUID\_CONSOLE\_DISPLAY\_STATUS** instead.</span></span>

 

</dl> </dd> <dt>

<span data-ttu-id="02db1-197"><span id="GUID_SYSTEM_AWAYMODE"></span><span id="guid_system_awaymode"></span>**GUID- \_ System- \_ awaymode**</span><span class="sxs-lookup"><span data-stu-id="02db1-197"><span id="GUID_SYSTEM_AWAYMODE"></span><span id="guid_system_awaymode"></span>**GUID\_SYSTEM\_AWAYMODE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="02db1-198">98a7f 580-017-48aa-9c0f -44352c29e5c0</span><span class="sxs-lookup"><span data-stu-id="02db1-198">98A7F580-01F7-48AA-9C0F-44352C29E5C0</span></span>
</dt> <dt>



<span data-ttu-id="02db1-199">Das System wechselt in den Modus und verlässt den Modus.</span><span class="sxs-lookup"><span data-stu-id="02db1-199">The system is entering or exiting away mode.</span></span> <span data-ttu-id="02db1-200">Der **Datenmember** ist ein **DWORD** , das den aktuellen Status des entfernten Modus angibt.</span><span class="sxs-lookup"><span data-stu-id="02db1-200">The **Data** member is a **DWORD** that indicates the current away mode state.</span></span>

<dl> <dt>

<span data-ttu-id="02db1-201">0x0-der Computer verlässt den Modus.</span><span class="sxs-lookup"><span data-stu-id="02db1-201">0x0 - The computer is exiting away mode.</span></span>
</dt> <dt>

<span data-ttu-id="02db1-202">0x1-der Computer wechselt in den Modus "entfernt".</span><span class="sxs-lookup"><span data-stu-id="02db1-202">0x1 - The computer is entering away mode.</span></span>
</dt> </dl>

</dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="02db1-203">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="02db1-203">Requirements</span></span>



| <span data-ttu-id="02db1-204">Anforderung</span><span class="sxs-lookup"><span data-stu-id="02db1-204">Requirement</span></span> | <span data-ttu-id="02db1-205">Wert</span><span class="sxs-lookup"><span data-stu-id="02db1-205">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="02db1-206">Header</span><span class="sxs-lookup"><span data-stu-id="02db1-206">Header</span></span><br/> | <dl> <span data-ttu-id="02db1-207"><dt>WinNT. h</dt></span><span class="sxs-lookup"><span data-stu-id="02db1-207"><dt>WinNT.h</dt></span></span> </dl> |



 

