---
description: Die Flags in der folgenden Tabelle geben den Status einer OPM-Sitzung (Output Protection Manager) an.
ms.assetid: d6d85fd4-e735-4610-93e0-bb2b1782f11b
title: OPM-Statusflags (opmapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0cbf9d299d6d53a26a61d19372e56e42bd2cdf99
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527872"
---
# <a name="opm-status-flags"></a><span data-ttu-id="ce0c2-103">OPM-Statusflags</span><span class="sxs-lookup"><span data-stu-id="ce0c2-103">OPM Status Flags</span></span>

<span data-ttu-id="ce0c2-104">Die Flags in der folgenden Tabelle geben den Status einer OPM-Sitzung (Output Protection Manager) an.</span><span class="sxs-lookup"><span data-stu-id="ce0c2-104">The flags in the following table specify the status of an Output Protection Manager (OPM) session.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="ce0c2-105">Konstante/Wert</span><span class="sxs-lookup"><span data-stu-id="ce0c2-105">Constant/value</span></span></th>
<th style="text-align: left;"><span data-ttu-id="ce0c2-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ce0c2-106">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="OPM_STATUS_NORMAL"></span><span id="opm_status_normal"></span><dl> <span data-ttu-id="ce0c2-107"><dt><strong>OPM_STATUS_NORMAL</strong></dt> <dt>0x00</dt> </span><span class="sxs-lookup"><span data-stu-id="ce0c2-107"><dt><strong>OPM_STATUS_NORMAL</strong></dt> <dt>0x00</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="ce0c2-108">Normaler Status.</span><span class="sxs-lookup"><span data-stu-id="ce0c2-108">Normal status.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="OPM_STATUS_LINK_LOST"></span><span id="opm_status_link_lost"></span><dl> <span data-ttu-id="ce0c2-109"><dt><strong>OPM_STATUS_LINK_LOST</strong></dt> <dt>0x01</dt> </span><span class="sxs-lookup"><span data-stu-id="ce0c2-109"><dt><strong>OPM_STATUS_LINK_LOST</strong></dt> <dt>0x01</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="ce0c2-110">Die Integrität der Verbindung wurde beeinträchtigt.</span><span class="sxs-lookup"><span data-stu-id="ce0c2-110">The integrity of the connection has been compromised.</span></span> <span data-ttu-id="ce0c2-111">Beispiele für Ereignisse, die bewirken, dass der Treiber dieses Flag festgelegt hat, sind:</span><span class="sxs-lookup"><span data-stu-id="ce0c2-111">Examples of events that cause the driver to set this flag include:</span></span><br/>
<ul>
<li><span data-ttu-id="ce0c2-112">Der Treiber kann die aktuelle Schutz Ebene nicht mehr erzwingen.</span><span class="sxs-lookup"><span data-stu-id="ce0c2-112">The driver can no longer enforce the current protection level.</span></span></li>
<li><span data-ttu-id="ce0c2-113">Der Treiber hat einen internen Integritäts Fehler festgestellt.</span><span class="sxs-lookup"><span data-stu-id="ce0c2-113">The driver detected an internal integrity error.</span></span></li>
<li><span data-ttu-id="ce0c2-114">Der Connector zwischen dem Computer und dem Anzeigegerät wurde getrennt.</span><span class="sxs-lookup"><span data-stu-id="ce0c2-114">The connector between the computer and the display device was unplugged.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="OPM_STATUS_RENEGOTIATION_REQUIRED"></span><span id="opm_status_renegotiation_required"></span><dl> <span data-ttu-id="ce0c2-115"><dt><strong>OPM_STATUS_RENEGOTIATION_REQUIRED</strong></dt> <dt>0x02</dt> </span><span class="sxs-lookup"><span data-stu-id="ce0c2-115"><dt><strong>OPM_STATUS_RENEGOTIATION_REQUIRED</strong></dt> <dt>0x02</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="ce0c2-116">Die Verbindungs Konfiguration wurde geändert.</span><span class="sxs-lookup"><span data-stu-id="ce0c2-116">The connection configuration has changed.</span></span> <span data-ttu-id="ce0c2-117">Der Benutzer hat z. b. den Anzeigemodus für den Desktop geändert.</span><span class="sxs-lookup"><span data-stu-id="ce0c2-117">For example, the user has changed the desktop display mode.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="OPM_STATUS_TAMPERING_DETECTED"></span><span id="opm_status_tampering_detected"></span><dl> <span data-ttu-id="ce0c2-118"><dt><strong>OPM_STATUS_TAMPERING_DETECTED</strong></dt> <dt>0x04</dt> </span><span class="sxs-lookup"><span data-stu-id="ce0c2-118"><dt><strong>OPM_STATUS_TAMPERING_DETECTED</strong></dt> <dt>0x04</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="ce0c2-119">Der Grafikadapter oder der Treiber wurde manipuliert.</span><span class="sxs-lookup"><span data-stu-id="ce0c2-119">The graphics adapter or the driver has been tampered with.</span></span><br/> <span data-ttu-id="ce0c2-120">Dieses Flag wird im <em>COPP-Emulations Modus</em>nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="ce0c2-120">This flag is not used in <em>COPP emulation mode</em>.</span></span> <span data-ttu-id="ce0c2-121">Stattdessen wird bei der Videoausgabe das OPM_STATUS_LINK_LOST-Flag festgelegt, wenn Manipulationen erkannt werden.</span><span class="sxs-lookup"><span data-stu-id="ce0c2-121">Instead, the video output will set the OPM_STATUS_LINK_LOST flag if it detects tampering.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="OPM_STATUS_REVOKED_HDCP_DEVICE_ATTACHED"></span><span id="opm_status_revoked_hdcp_device_attached"></span><dl> <span data-ttu-id="ce0c2-122"><dt><strong>OPM_STATUS_REVOKED_HDCP_DEVICE_ATTACHED</strong></dt> <dt>0x08</dt> </span><span class="sxs-lookup"><span data-stu-id="ce0c2-122"><dt><strong>OPM_STATUS_REVOKED_HDCP_DEVICE_ATTACHED</strong></dt> <dt>0x08</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="ce0c2-123">Ein gesperrtes High-Bandwidth Digital Content Protection-Gerät (HDCP) ist an die Videoausgabe angefügt.</span><span class="sxs-lookup"><span data-stu-id="ce0c2-123">A revoked High-Bandwidth Digital Content Protection (HDCP) device is attached to the video output.</span></span><br/> <span data-ttu-id="ce0c2-124">Dieses Statusflag kann von einer <a href="opm-get-virtual-protection-level.md">OPM_GET_VIRTUAL_PROTECTION_LEVEL</a> oder <a href="opm-get-actual-protection-level.md">OPM_GET_ACTUAL_PROTECTION_LEVEL</a> Abfrage zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="ce0c2-124">This status flag can be returned from an <a href="opm-get-virtual-protection-level.md">OPM_GET_VIRTUAL_PROTECTION_LEVEL</a> or <a href="opm-get-actual-protection-level.md">OPM_GET_ACTUAL_PROTECTION_LEVEL</a> query.</span></span> <br/> <span data-ttu-id="ce0c2-125">Das widerrufene Gerät kann direkt an die Videoausgabe oder indirekt über einen HDCP-Repeater angefügt werden.</span><span class="sxs-lookup"><span data-stu-id="ce0c2-125">The revoked device might be attached directly to the video output, or indirectly through an HDCP repeater.</span></span> <span data-ttu-id="ce0c2-126">Eine Videoausgabe ist erforderlich, um diese Bedingung zu erkennen, während HDCP aktiviert ist, aber nicht anders.</span><span class="sxs-lookup"><span data-stu-id="ce0c2-126">A video output is required to detect this condition while HDCP is enabled, but not otherwise.</span></span><br/> <span data-ttu-id="ce0c2-127">Dieses Flag wird im <em>COPP-Emulations Modus</em>nicht verwendet, da die Videoausgabe keine gesperrten Geräte in diesem Modus erkennt.</span><span class="sxs-lookup"><span data-stu-id="ce0c2-127">This flag is not used in <em>COPP emulation mode</em>, because the video output does not detect revoked devices in that mode.</span></span><br/></td>
</tr>
</tbody>
</table>



## <a name="remarks"></a><span data-ttu-id="ce0c2-128">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ce0c2-128">Remarks</span></span>

<span data-ttu-id="ce0c2-129">Einige dieser Konstanten entsprechen den Werten aus der **COPP \_** -Enumeration "Enumeration", die im Certified Output Protection Protocol (COPP) verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="ce0c2-129">Some of these constants are equivalent to values from the **COPP\_StatusFlags** enumeration used in Certified Output Protection Protocol (COPP).</span></span>

## <a name="requirements"></a><span data-ttu-id="ce0c2-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ce0c2-130">Requirements</span></span>



| <span data-ttu-id="ce0c2-131">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ce0c2-131">Requirement</span></span> | <span data-ttu-id="ce0c2-132">Wert</span><span class="sxs-lookup"><span data-stu-id="ce0c2-132">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="ce0c2-133">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ce0c2-133">Minimum supported client</span></span><br/> | <span data-ttu-id="ce0c2-134">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ce0c2-134">Windows Vista \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="ce0c2-135">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ce0c2-135">Minimum supported server</span></span><br/> | <span data-ttu-id="ce0c2-136">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ce0c2-136">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="ce0c2-137">Header</span><span class="sxs-lookup"><span data-stu-id="ce0c2-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="ce0c2-138"><dt>Opmapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="ce0c2-138"><dt>Opmapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ce0c2-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ce0c2-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ce0c2-140">OPM-Enumerationen</span><span class="sxs-lookup"><span data-stu-id="ce0c2-140">OPM Enumerations</span></span>](opm-enumerations.md)
</dt> </dl>

 

 




