---
description: Die globalen Flags-Konstanten werden verwendet, um Benutzer Energierichtlinien-Optionen zu aktivieren oder zu deaktivieren.
ms.assetid: d98190ef-f70e-4796-960e-ff32d2cf6f4f
title: Globale Flags-Konstanten (POWRPROF. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4fd31340e3e7daf4f9dd034c3fa2db333680a626
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106367939"
---
# <a name="global-flags-constants"></a><span data-ttu-id="18cbe-103">Globale Flags-Konstanten</span><span class="sxs-lookup"><span data-stu-id="18cbe-103">Global Flags Constants</span></span>

<span data-ttu-id="18cbe-104">Die globalen Flags-Konstanten werden verwendet, um Benutzer Energierichtlinien-Optionen zu aktivieren oder zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="18cbe-104">The global flags constants are used to enable or disable user power policy options.</span></span>



| <span data-ttu-id="18cbe-105">Konstante/Wert</span><span class="sxs-lookup"><span data-stu-id="18cbe-105">Constant/value</span></span>                                                                                                                                                                                                                                                                                         | <span data-ttu-id="18cbe-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="18cbe-106">Description</span></span>                                                                                                                                        |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="EnableMultiBatteryDisplay"></span><span id="enablemultibatterydisplay"></span><span id="ENABLEMULTIBATTERYDISPLAY"></span><dl> <span data-ttu-id="18cbe-107"><dt>**Enablemultibatterydisplay**</dt> <dt>0x02</dt></span><span class="sxs-lookup"><span data-stu-id="18cbe-107"><dt>**EnableMultiBatteryDisplay**</dt> <dt>0x02</dt></span></span> </dl> | <span data-ttu-id="18cbe-108">Aktiviert oder deaktiviert die Anzeige mehrerer Akkus im System Energie Messgerät.</span><span class="sxs-lookup"><span data-stu-id="18cbe-108">Enables or disables multiple battery display in the system Power Meter.</span></span><br/>                                                                 |
| <span id="EnablePasswordLogon"></span><span id="enablepasswordlogon"></span><span id="ENABLEPASSWORDLOGON"></span><dl> <span data-ttu-id="18cbe-109"><dt>**Enablepasswordlogon**</dt> <dt>0x04</dt></span><span class="sxs-lookup"><span data-stu-id="18cbe-109"><dt>**EnablePasswordLogon**</dt> <dt>0x04</dt></span></span> </dl>                         | <span data-ttu-id="18cbe-110">Aktiviert oder deaktiviert die Anforderung der Kenn Wort Anmeldung, wenn das System aus dem Standby-oder Ruhezustand wieder aufgenommen wird.</span><span class="sxs-lookup"><span data-stu-id="18cbe-110">Enables or disables requiring password logon when the system resumes from standby or hibernate.</span></span><br/>                                         |
| <span id="EnableSysTrayBatteryMeter"></span><span id="enablesystraybatterymeter"></span><span id="ENABLESYSTRAYBATTERYMETER"></span><dl> <span data-ttu-id="18cbe-111"><dt>**Enablesystraybatterymeter**</dt> <dt>0x01</dt></span><span class="sxs-lookup"><span data-stu-id="18cbe-111"><dt>**EnableSysTrayBatteryMeter**</dt> <dt>0x01</dt></span></span> </dl> | <span data-ttu-id="18cbe-112">Aktiviert oder deaktiviert das Akku leisten Symbol in der Taskleiste.</span><span class="sxs-lookup"><span data-stu-id="18cbe-112">Enables or disables the battery meter icon in the system tray.</span></span> <span data-ttu-id="18cbe-113">Wenn dieses Flag deaktiviert ist, wird das Akku Meter Symbol nicht angezeigt.</span><span class="sxs-lookup"><span data-stu-id="18cbe-113">When this flag is cleared, the battery meter icon is not displayed.</span></span><br/>      |
| <span id="EnableVideoDimDisplay"></span><span id="enablevideodimdisplay"></span><span id="ENABLEVIDEODIMDISPLAY"></span><dl> <span data-ttu-id="18cbe-114"><dt>**Enablevideodimdisplay**</dt> <dt>0x10</dt></span><span class="sxs-lookup"><span data-stu-id="18cbe-114"><dt>**EnableVideoDimDisplay**</dt> <dt>0x10</dt></span></span> </dl>                 | <span data-ttu-id="18cbe-115">Aktiviert oder deaktiviert die Unterstützung für das Abblenden der Videoanzeige, wenn sich das System von der Ausführung bei der Stromversorgung in den Akku Betrieb ändert.</span><span class="sxs-lookup"><span data-stu-id="18cbe-115">Enables or disables support for dimming the video display when the system changes from running on AC power to running on battery power.</span></span><br/> |
| <span id="EnableWakeOnRing"></span><span id="enablewakeonring"></span><span id="ENABLEWAKEONRING"></span><dl> <span data-ttu-id="18cbe-116"><dt>**Enablewakeonring**</dt> <dt>0x08</dt></span><span class="sxs-lookup"><span data-stu-id="18cbe-116"><dt>**EnableWakeOnRing**</dt> <dt>0x08</dt></span></span> </dl>                                     | <span data-ttu-id="18cbe-117">Aktiviert oder deaktiviert die Unterstützung für Wake-on-Ring.</span><span class="sxs-lookup"><span data-stu-id="18cbe-117">Enables or disables wake on ring support.</span></span><br/>                                                                                               |



## <a name="requirements"></a><span data-ttu-id="18cbe-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="18cbe-118">Requirements</span></span>



| <span data-ttu-id="18cbe-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="18cbe-119">Requirement</span></span> | <span data-ttu-id="18cbe-120">Wert</span><span class="sxs-lookup"><span data-stu-id="18cbe-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="18cbe-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="18cbe-121">Minimum supported client</span></span><br/> | <span data-ttu-id="18cbe-122">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="18cbe-122">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="18cbe-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="18cbe-123">Minimum supported server</span></span><br/> | <span data-ttu-id="18cbe-124">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="18cbe-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="18cbe-125">Header</span><span class="sxs-lookup"><span data-stu-id="18cbe-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="18cbe-126"><dt>POWRPROF. h</dt></span><span class="sxs-lookup"><span data-stu-id="18cbe-126"><dt>PowrProf.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="18cbe-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="18cbe-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="18cbe-128">**globale \_ Benutzer \_ Energie \_ Richtlinie**</span><span class="sxs-lookup"><span data-stu-id="18cbe-128">**GLOBAL\_USER\_POWER\_POLICY**</span></span>](/windows/desktop/api/PowrProf/ns-powrprof-global_user_power_policy)
</dt> </dl>

 

 




