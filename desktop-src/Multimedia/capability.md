---
title: Funktionsbefehl
description: Der Funktionsbefehl fordert Informationen zu einer bestimmten Funktion eines Geräts an. Dieser Befehl wird von allen MCI-Geräten erkannt.
ms.assetid: 1b470473-0de6-41ba-9f6e-41f0b13ceaeb
keywords:
- Funktionsbefehl Windows-Multimedia
topic_type:
- apiref
api_name:
- capability
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9a6ac87b98fb8d748a5baf2665cc5a63230b6a98
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475708"
---
# <a name="capability-command"></a><span data-ttu-id="f67a2-105">Funktionsbefehl</span><span class="sxs-lookup"><span data-stu-id="f67a2-105">capability command</span></span>

<span data-ttu-id="f67a2-106">Der Funktionsbefehl fordert Informationen zu einer bestimmten Funktion eines Geräts an.</span><span class="sxs-lookup"><span data-stu-id="f67a2-106">The capability command requests information about a particular capability of a device.</span></span> <span data-ttu-id="f67a2-107">Dieser Befehl wird von allen MCI-Geräten erkannt.</span><span class="sxs-lookup"><span data-stu-id="f67a2-107">All MCI devices recognize this command.</span></span>

<span data-ttu-id="f67a2-108">Um diesen Befehl zu senden, wenden Sie die [**mciSendString**](/previous-versions//dd757161(v=vs.85)) -Funktion mit dem festgelegten *lpszcommand* -Parameter wie folgt an.</span><span class="sxs-lookup"><span data-stu-id="f67a2-108">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("capability %s %s %s"), 
  lpszDeviceID, 
  lpszRequest, 
  lpszFlags
); 
```

## <a name="parameters"></a><span data-ttu-id="f67a2-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="f67a2-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f67a2-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszde viceid*</span><span class="sxs-lookup"><span data-stu-id="f67a2-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="f67a2-111">Der Bezeichner eines MCI-Geräts.</span><span class="sxs-lookup"><span data-stu-id="f67a2-111">Identifier of an MCI device.</span></span> <span data-ttu-id="f67a2-112">Dieser Bezeichner oder Alias wird zugewiesen, wenn das Gerät geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="f67a2-112">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="f67a2-113"><span id="lpszRequest"></span><span id="lpszrequest"></span><span id="LPSZREQUEST"></span>*lpszrequest*</span><span class="sxs-lookup"><span data-stu-id="f67a2-113"><span id="lpszRequest"></span><span id="lpszrequest"></span><span id="LPSZREQUEST"></span>*lpszRequest*</span></span>
</dt> <dd>

<span data-ttu-id="f67a2-114">Flag, das eine Geräte Funktion identifiziert.</span><span class="sxs-lookup"><span data-stu-id="f67a2-114">Flag that identifies a device capability.</span></span> <span data-ttu-id="f67a2-115">In der folgenden Tabelle sind die Gerätetypen aufgeführt **, die den Funktionsbefehl und** die von den einzelnen Typen verwendeten Flags erkennen:</span><span class="sxs-lookup"><span data-stu-id="f67a2-115">The following table lists device types that recognize the **capability** command and the flags used by each type:</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f67a2-116">Wert</span><span class="sxs-lookup"><span data-stu-id="f67a2-116">Value</span></span></th>
<th><span data-ttu-id="f67a2-117">Typ</span><span class="sxs-lookup"><span data-stu-id="f67a2-117">Type</span></span></th>
<th><span data-ttu-id="f67a2-118">Typ</span><span class="sxs-lookup"><span data-stu-id="f67a2-118">Type</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f67a2-119">CDAudio</span><span class="sxs-lookup"><span data-stu-id="f67a2-119">cdaudio</span></span></td>
<td><ul>
<li><span data-ttu-id="f67a2-120">kann Auswerfen</span><span class="sxs-lookup"><span data-stu-id="f67a2-120">can eject</span></span></li>
<li><span data-ttu-id="f67a2-121">kann abspielen</span><span class="sxs-lookup"><span data-stu-id="f67a2-121">can play</span></span></li>
<li><span data-ttu-id="f67a2-122">kann aufzeichnen</span><span class="sxs-lookup"><span data-stu-id="f67a2-122">can record</span></span></li>
<li><span data-ttu-id="f67a2-123">kann speichern</span><span class="sxs-lookup"><span data-stu-id="f67a2-123">can save</span></span></li>
<li><span data-ttu-id="f67a2-124">Verbund Gerät</span><span class="sxs-lookup"><span data-stu-id="f67a2-124">compound device</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="f67a2-125">Gerätetyp</span><span class="sxs-lookup"><span data-stu-id="f67a2-125">device type</span></span></li>
<li><span data-ttu-id="f67a2-126">hat Audiodaten</span><span class="sxs-lookup"><span data-stu-id="f67a2-126">has audio</span></span></li>
<li><span data-ttu-id="f67a2-127">hat Video</span><span class="sxs-lookup"><span data-stu-id="f67a2-127">has video</span></span></li>
<li><span data-ttu-id="f67a2-128">verwendet Dateien</span><span class="sxs-lookup"><span data-stu-id="f67a2-128">uses files</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f67a2-129">Digitalvideo</span><span class="sxs-lookup"><span data-stu-id="f67a2-129">digitalvideo</span></span></td>
<td><ul>
<li><span data-ttu-id="f67a2-130">kann Auswerfen</span><span class="sxs-lookup"><span data-stu-id="f67a2-130">can eject</span></span></li>
<li><span data-ttu-id="f67a2-131">Einfrieren möglich</span><span class="sxs-lookup"><span data-stu-id="f67a2-131">can freeze</span></span></li>
<li><span data-ttu-id="f67a2-132">Sperre möglich</span><span class="sxs-lookup"><span data-stu-id="f67a2-132">can lock</span></span></li>
<li><span data-ttu-id="f67a2-133">kann abspielen</span><span class="sxs-lookup"><span data-stu-id="f67a2-133">can play</span></span></li>
<li><span data-ttu-id="f67a2-134">kann aufzeichnen</span><span class="sxs-lookup"><span data-stu-id="f67a2-134">can record</span></span></li>
<li><span data-ttu-id="f67a2-135">kann umkehren</span><span class="sxs-lookup"><span data-stu-id="f67a2-135">can reverse</span></span></li>
<li><span data-ttu-id="f67a2-136">kann speichern</span><span class="sxs-lookup"><span data-stu-id="f67a2-136">can save</span></span></li>
<li><span data-ttu-id="f67a2-137">kann gestreckt werden</span><span class="sxs-lookup"><span data-stu-id="f67a2-137">can stretch</span></span></li>
<li><span data-ttu-id="f67a2-138">kann Eingaben ausdehnen</span><span class="sxs-lookup"><span data-stu-id="f67a2-138">can stretch input</span></span></li>
<li><span data-ttu-id="f67a2-139">kann testen</span><span class="sxs-lookup"><span data-stu-id="f67a2-139">can test</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="f67a2-140">Verbund Gerät</span><span class="sxs-lookup"><span data-stu-id="f67a2-140">compound device</span></span></li>
<li><span data-ttu-id="f67a2-141">Gerätetyp</span><span class="sxs-lookup"><span data-stu-id="f67a2-141">device type</span></span></li>
<li><span data-ttu-id="f67a2-142">hat Audiodaten</span><span class="sxs-lookup"><span data-stu-id="f67a2-142">has audio</span></span></li>
<li><span data-ttu-id="f67a2-143">hat noch</span><span class="sxs-lookup"><span data-stu-id="f67a2-143">has still</span></span></li>
<li><span data-ttu-id="f67a2-144">hat Video</span><span class="sxs-lookup"><span data-stu-id="f67a2-144">has video</span></span></li>
<li><span data-ttu-id="f67a2-145">maximale Wiedergabe Rate</span><span class="sxs-lookup"><span data-stu-id="f67a2-145">maximum play rate</span></span></li>
<li><span data-ttu-id="f67a2-146">minimale Wiedergabe Rate</span><span class="sxs-lookup"><span data-stu-id="f67a2-146">minimum play rate</span></span></li>
<li><span data-ttu-id="f67a2-147">verwendet Dateien</span><span class="sxs-lookup"><span data-stu-id="f67a2-147">uses files</span></span></li>
<li><span data-ttu-id="f67a2-148">verwendet Paletten</span><span class="sxs-lookup"><span data-stu-id="f67a2-148">uses palettes</span></span></li>
<li><span data-ttu-id="f67a2-149">Windows</span><span class="sxs-lookup"><span data-stu-id="f67a2-149">windows</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f67a2-150">overlay</span><span class="sxs-lookup"><span data-stu-id="f67a2-150">overlay</span></span></td>
<td><ul>
<li><span data-ttu-id="f67a2-151">kann Auswerfen</span><span class="sxs-lookup"><span data-stu-id="f67a2-151">can eject</span></span></li>
<li><span data-ttu-id="f67a2-152">Einfrieren möglich</span><span class="sxs-lookup"><span data-stu-id="f67a2-152">can freeze</span></span></li>
<li><span data-ttu-id="f67a2-153">kann abspielen</span><span class="sxs-lookup"><span data-stu-id="f67a2-153">can play</span></span></li>
<li><span data-ttu-id="f67a2-154">kann aufzeichnen</span><span class="sxs-lookup"><span data-stu-id="f67a2-154">can record</span></span></li>
<li><span data-ttu-id="f67a2-155">kann speichern</span><span class="sxs-lookup"><span data-stu-id="f67a2-155">can save</span></span></li>
<li><span data-ttu-id="f67a2-156">kann gestreckt werden</span><span class="sxs-lookup"><span data-stu-id="f67a2-156">can stretch</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="f67a2-157">Verbund Gerät</span><span class="sxs-lookup"><span data-stu-id="f67a2-157">compound device</span></span></li>
<li><span data-ttu-id="f67a2-158">Gerätetyp</span><span class="sxs-lookup"><span data-stu-id="f67a2-158">device type</span></span></li>
<li><span data-ttu-id="f67a2-159">hat Audiodaten</span><span class="sxs-lookup"><span data-stu-id="f67a2-159">has audio</span></span></li>
<li><span data-ttu-id="f67a2-160">hat Video</span><span class="sxs-lookup"><span data-stu-id="f67a2-160">has video</span></span></li>
<li><span data-ttu-id="f67a2-161">verwendet Dateien</span><span class="sxs-lookup"><span data-stu-id="f67a2-161">uses files</span></span></li>
<li><span data-ttu-id="f67a2-162">Windows</span><span class="sxs-lookup"><span data-stu-id="f67a2-162">windows</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f67a2-163">sequencer</span><span class="sxs-lookup"><span data-stu-id="f67a2-163">sequencer</span></span></td>
<td><ul>
<li><span data-ttu-id="f67a2-164">kann Auswerfen</span><span class="sxs-lookup"><span data-stu-id="f67a2-164">can eject</span></span></li>
<li><span data-ttu-id="f67a2-165">kann abspielen</span><span class="sxs-lookup"><span data-stu-id="f67a2-165">can play</span></span></li>
<li><span data-ttu-id="f67a2-166">kann aufzeichnen</span><span class="sxs-lookup"><span data-stu-id="f67a2-166">can record</span></span></li>
<li><span data-ttu-id="f67a2-167">kann speichern</span><span class="sxs-lookup"><span data-stu-id="f67a2-167">can save</span></span></li>
<li><span data-ttu-id="f67a2-168">Verbund Gerät</span><span class="sxs-lookup"><span data-stu-id="f67a2-168">compound device</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="f67a2-169">Gerätetyp</span><span class="sxs-lookup"><span data-stu-id="f67a2-169">device type</span></span></li>
<li><span data-ttu-id="f67a2-170">hat Audiodaten</span><span class="sxs-lookup"><span data-stu-id="f67a2-170">has audio</span></span></li>
<li><span data-ttu-id="f67a2-171">hat Video</span><span class="sxs-lookup"><span data-stu-id="f67a2-171">has video</span></span></li>
<li><span data-ttu-id="f67a2-172">verwendet Dateien</span><span class="sxs-lookup"><span data-stu-id="f67a2-172">uses files</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f67a2-173">VCR</span><span class="sxs-lookup"><span data-stu-id="f67a2-173">vcr</span></span></td>
<td><ul>
<li><span data-ttu-id="f67a2-174">kann die Länge erkennen</span><span class="sxs-lookup"><span data-stu-id="f67a2-174">can detect length</span></span></li>
<li><span data-ttu-id="f67a2-175">kann Auswerfen</span><span class="sxs-lookup"><span data-stu-id="f67a2-175">can eject</span></span></li>
<li><span data-ttu-id="f67a2-176">Einfrieren möglich</span><span class="sxs-lookup"><span data-stu-id="f67a2-176">can freeze</span></span></li>
<li><span data-ttu-id="f67a2-177">kann Quellen überwachen</span><span class="sxs-lookup"><span data-stu-id="f67a2-177">can monitor sources</span></span></li>
<li><span data-ttu-id="f67a2-178">kann abspielen</span><span class="sxs-lookup"><span data-stu-id="f67a2-178">can play</span></span></li>
<li><span data-ttu-id="f67a2-179">kann vorab</span><span class="sxs-lookup"><span data-stu-id="f67a2-179">can preroll</span></span></li>
<li><span data-ttu-id="f67a2-180">Vorschau möglich</span><span class="sxs-lookup"><span data-stu-id="f67a2-180">can preview</span></span></li>
<li><span data-ttu-id="f67a2-181">kann aufzeichnen</span><span class="sxs-lookup"><span data-stu-id="f67a2-181">can record</span></span></li>
<li><span data-ttu-id="f67a2-182">kann umkehren</span><span class="sxs-lookup"><span data-stu-id="f67a2-182">can reverse</span></span></li>
<li><span data-ttu-id="f67a2-183">kann speichern</span><span class="sxs-lookup"><span data-stu-id="f67a2-183">can save</span></span></li>
<li><span data-ttu-id="f67a2-184">kann testen</span><span class="sxs-lookup"><span data-stu-id="f67a2-184">can test</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="f67a2-185">Takt Inkrement-Rate</span><span class="sxs-lookup"><span data-stu-id="f67a2-185">clock increment rate</span></span></li>
<li><span data-ttu-id="f67a2-186">Verbund Gerät</span><span class="sxs-lookup"><span data-stu-id="f67a2-186">compound device</span></span></li>
<li><span data-ttu-id="f67a2-187">Gerätetyp</span><span class="sxs-lookup"><span data-stu-id="f67a2-187">device type</span></span></li>
<li><span data-ttu-id="f67a2-188">hat Audiodaten</span><span class="sxs-lookup"><span data-stu-id="f67a2-188">has audio</span></span></li>
<li><span data-ttu-id="f67a2-189">hat Uhr</span><span class="sxs-lookup"><span data-stu-id="f67a2-189">has clock</span></span></li>
<li><span data-ttu-id="f67a2-190">hat Zeitcode</span><span class="sxs-lookup"><span data-stu-id="f67a2-190">has timecode</span></span></li>
<li><span data-ttu-id="f67a2-191">hat Video</span><span class="sxs-lookup"><span data-stu-id="f67a2-191">has video</span></span></li>
<li><span data-ttu-id="f67a2-192">Anzahl der Markierungen</span><span class="sxs-lookup"><span data-stu-id="f67a2-192">number of marks</span></span></li>
<li><span data-ttu-id="f67a2-193">Genauigkeit suchen</span><span class="sxs-lookup"><span data-stu-id="f67a2-193">seek accuracy</span></span></li>
<li><span data-ttu-id="f67a2-194">verwendet Dateien</span><span class="sxs-lookup"><span data-stu-id="f67a2-194">uses files</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f67a2-195">Videodisk</span><span class="sxs-lookup"><span data-stu-id="f67a2-195">videodisc</span></span></td>
<td><ul>
<li><span data-ttu-id="f67a2-196">kann Auswerfen</span><span class="sxs-lookup"><span data-stu-id="f67a2-196">can eject</span></span></li>
<li><span data-ttu-id="f67a2-197">kann abspielen</span><span class="sxs-lookup"><span data-stu-id="f67a2-197">can play</span></span></li>
<li><span data-ttu-id="f67a2-198">kann aufzeichnen</span><span class="sxs-lookup"><span data-stu-id="f67a2-198">can record</span></span></li>
<li><span data-ttu-id="f67a2-199">kann umkehren</span><span class="sxs-lookup"><span data-stu-id="f67a2-199">can reverse</span></span></li>
<li><span data-ttu-id="f67a2-200">kann speichern</span><span class="sxs-lookup"><span data-stu-id="f67a2-200">can save</span></span></li>
<li><span data-ttu-id="f67a2-201">CAV</span><span class="sxs-lookup"><span data-stu-id="f67a2-201">CAV</span></span></li>
<li><span data-ttu-id="f67a2-202">CLV</span><span class="sxs-lookup"><span data-stu-id="f67a2-202">CLV</span></span></li>
<li><span data-ttu-id="f67a2-203">Verbund Gerät</span><span class="sxs-lookup"><span data-stu-id="f67a2-203">compound device</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="f67a2-204">Gerätetyp</span><span class="sxs-lookup"><span data-stu-id="f67a2-204">device type</span></span></li>
<li><span data-ttu-id="f67a2-205">schnelle Wiedergabe Rate</span><span class="sxs-lookup"><span data-stu-id="f67a2-205">fast play rate</span></span></li>
<li><span data-ttu-id="f67a2-206">hat Audiodaten</span><span class="sxs-lookup"><span data-stu-id="f67a2-206">has audio</span></span></li>
<li><span data-ttu-id="f67a2-207">hat Video</span><span class="sxs-lookup"><span data-stu-id="f67a2-207">has video</span></span></li>
<li><span data-ttu-id="f67a2-208">normale Wiedergabe Rate</span><span class="sxs-lookup"><span data-stu-id="f67a2-208">normal play rate</span></span></li>
<li><span data-ttu-id="f67a2-209">Langsame Wiedergabe Rate</span><span class="sxs-lookup"><span data-stu-id="f67a2-209">slow play rate</span></span></li>
<li><span data-ttu-id="f67a2-210">verwendet Dateien</span><span class="sxs-lookup"><span data-stu-id="f67a2-210">uses files</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f67a2-211">waveaudiodatei</span><span class="sxs-lookup"><span data-stu-id="f67a2-211">waveaudio</span></span></td>
<td><ul>
<li><span data-ttu-id="f67a2-212">kann Auswerfen</span><span class="sxs-lookup"><span data-stu-id="f67a2-212">can eject</span></span></li>
<li><span data-ttu-id="f67a2-213">kann abspielen</span><span class="sxs-lookup"><span data-stu-id="f67a2-213">can play</span></span></li>
<li><span data-ttu-id="f67a2-214">kann aufzeichnen</span><span class="sxs-lookup"><span data-stu-id="f67a2-214">can record</span></span></li>
<li><span data-ttu-id="f67a2-215">kann speichern</span><span class="sxs-lookup"><span data-stu-id="f67a2-215">can save</span></span></li>
<li><span data-ttu-id="f67a2-216">Verbund Gerät</span><span class="sxs-lookup"><span data-stu-id="f67a2-216">compound device</span></span></li>
<li><span data-ttu-id="f67a2-217">Gerätetyp</span><span class="sxs-lookup"><span data-stu-id="f67a2-217">device type</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="f67a2-218">hat Audiodaten</span><span class="sxs-lookup"><span data-stu-id="f67a2-218">has audio</span></span></li>
<li><span data-ttu-id="f67a2-219">hat Video</span><span class="sxs-lookup"><span data-stu-id="f67a2-219">has video</span></span></li>
<li><span data-ttu-id="f67a2-220">inputs</span><span class="sxs-lookup"><span data-stu-id="f67a2-220">inputs</span></span></li>
<li><span data-ttu-id="f67a2-221">outputs</span><span class="sxs-lookup"><span data-stu-id="f67a2-221">outputs</span></span></li>
<li><span data-ttu-id="f67a2-222">verwendet Dateien</span><span class="sxs-lookup"><span data-stu-id="f67a2-222">uses files</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="f67a2-223">In der folgenden Tabelle werden die Flags aufgelistet, die im *lpszrequest* -Parameter und deren Bedeutung angegeben werden können:</span><span class="sxs-lookup"><span data-stu-id="f67a2-223">The following table lists the flags that can be specified in the *lpszRequest* parameter and their meanings:</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f67a2-224">Flags</span><span class="sxs-lookup"><span data-stu-id="f67a2-224">Flags</span></span></th>
<th><span data-ttu-id="f67a2-225">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="f67a2-225">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f67a2-226">kann die Länge erkennen</span><span class="sxs-lookup"><span data-stu-id="f67a2-226">can detect length</span></span></td>
<td><span data-ttu-id="f67a2-227">Gibt " <strong>true</strong> " zurück, wenn das Gerät die Länge des Mediums erkennen kann.</span><span class="sxs-lookup"><span data-stu-id="f67a2-227">Returns <strong>TRUE</strong> if the device can detect the length of the media.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f67a2-228">kann Auswerfen</span><span class="sxs-lookup"><span data-stu-id="f67a2-228">can eject</span></span></td>
<td><span data-ttu-id="f67a2-229">Gibt " <strong>true</strong> " zurück, wenn das Gerät das Medium auswerfen kann.</span><span class="sxs-lookup"><span data-stu-id="f67a2-229">Returns <strong>TRUE</strong> if the device can eject the media.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f67a2-230">Einfrieren möglich</span><span class="sxs-lookup"><span data-stu-id="f67a2-230">can freeze</span></span></td>
<td><span data-ttu-id="f67a2-231">Gibt " <strong>true</strong> " zurück, wenn das Gerät Daten im Frame Puffer Einfrieren kann.</span><span class="sxs-lookup"><span data-stu-id="f67a2-231">Returns <strong>TRUE</strong> if the device can freeze data in the frame buffer.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f67a2-232">Sperre möglich</span><span class="sxs-lookup"><span data-stu-id="f67a2-232">can lock</span></span></td>
<td><span data-ttu-id="f67a2-233">Gibt " <strong>true</strong> " zurück, wenn das Gerät Daten Sperren kann.</span><span class="sxs-lookup"><span data-stu-id="f67a2-233">Returns <strong>TRUE</strong> if the device can lock data.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f67a2-234">kann Quellen überwachen</span><span class="sxs-lookup"><span data-stu-id="f67a2-234">can monitor sources</span></span></td>
<td><span data-ttu-id="f67a2-235">Gibt " <strong>true</strong> " zurück, wenn das Gerät unabhängig von der aktuellen Eingabeauswahl eine Eingabe (Quelle) an die überwachte Ausgabe übergeben kann.</span><span class="sxs-lookup"><span data-stu-id="f67a2-235">Returns <strong>TRUE</strong> if the device can pass an input (source) to the monitored output, independent of the current input selection.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f67a2-236">kann abspielen</span><span class="sxs-lookup"><span data-stu-id="f67a2-236">can play</span></span></td>
<td><span data-ttu-id="f67a2-237">Gibt <strong>true</strong> zurück, wenn das Gerät wiedergegeben werden kann.</span><span class="sxs-lookup"><span data-stu-id="f67a2-237">Returns <strong>TRUE</strong> if the device can play.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f67a2-238">kann vorab</span><span class="sxs-lookup"><span data-stu-id="f67a2-238">can preroll</span></span></td>
<td><span data-ttu-id="f67a2-239">Gibt <strong>true</strong> zurück, wenn das Gerät das &quot; ein Vorlauf ausgeführt- &quot; Flag <a href="cue.md"></a> mit dem Hinweis Befehl unterstützt.</span><span class="sxs-lookup"><span data-stu-id="f67a2-239">Returns <strong>TRUE</strong> if the device supports the &quot;preroll&quot; flag with the <a href="cue.md">cue</a> command.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f67a2-240">Vorschau möglich</span><span class="sxs-lookup"><span data-stu-id="f67a2-240">can preview</span></span></td>
<td><span data-ttu-id="f67a2-241">Gibt <strong>true</strong> zurück, wenn das Gerät Vorschau Versionen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="f67a2-241">Returns <strong>TRUE</strong> if the device supports previews.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f67a2-242">kann aufzeichnen</span><span class="sxs-lookup"><span data-stu-id="f67a2-242">can record</span></span></td>
<td><span data-ttu-id="f67a2-243">Gibt <strong>true</strong> zurück, wenn das Gerät eine Aufzeichnung unterstützt.</span><span class="sxs-lookup"><span data-stu-id="f67a2-243">Returns <strong>TRUE</strong> if the device supports recording.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f67a2-244">kann umkehren</span><span class="sxs-lookup"><span data-stu-id="f67a2-244">can reverse</span></span></td>
<td><span data-ttu-id="f67a2-245">Gibt <strong>true</strong> zurück, wenn das Gerät in umgekehrter Richtung wiedergegeben werden kann</span><span class="sxs-lookup"><span data-stu-id="f67a2-245">Returns <strong>TRUE</strong> if the device can play in reverse.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f67a2-246">kann speichern</span><span class="sxs-lookup"><span data-stu-id="f67a2-246">can save</span></span></td>
<td><span data-ttu-id="f67a2-247">Gibt " <strong>true</strong> " zurück, wenn das Gerät Daten speichern kann.</span><span class="sxs-lookup"><span data-stu-id="f67a2-247">Returns <strong>TRUE</strong> if the device can save data.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f67a2-248">kann gestreckt werden</span><span class="sxs-lookup"><span data-stu-id="f67a2-248">can stretch</span></span></td>
<td><span data-ttu-id="f67a2-249">Gibt " <strong>true</strong> " zurück, wenn das Gerät Frames zum Ausfüllen eines angegebenen Anzeige Rechtecks erweitern kann.</span><span class="sxs-lookup"><span data-stu-id="f67a2-249">Returns <strong>TRUE</strong> if the device can stretch frames to fill a given display rectangle.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f67a2-250">kann Eingaben ausdehnen</span><span class="sxs-lookup"><span data-stu-id="f67a2-250">can stretch input</span></span></td>
<td><span data-ttu-id="f67a2-251">Gibt " <strong>true</strong> " zurück, wenn die Größe eines Bilds beim Digitalisieren des Geräts im Frame Puffer geändert werden kann.</span><span class="sxs-lookup"><span data-stu-id="f67a2-251">Returns <strong>TRUE</strong> if the device can resize an image in the process of digitizing it into the frame buffer.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f67a2-252">kann testen</span><span class="sxs-lookup"><span data-stu-id="f67a2-252">can test</span></span></td>
<td><span data-ttu-id="f67a2-253">Gibt <strong>true</strong> zurück, wenn das Gerät das Test Schlüsselwort erkennt.</span><span class="sxs-lookup"><span data-stu-id="f67a2-253">Returns <strong>TRUE</strong> if the device recognizes the test keyword.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f67a2-254">CAV</span><span class="sxs-lookup"><span data-stu-id="f67a2-254">cav</span></span></td>
<td><span data-ttu-id="f67a2-255">In Kombination mit anderen Elementen gibt dieses Flag an, dass die Rückgabe Informationen für Videodisks im CAV-Format gelten.</span><span class="sxs-lookup"><span data-stu-id="f67a2-255">When combined with other items, this flag specifies that the return information applies to CAV format videodiscs.</span></span> <span data-ttu-id="f67a2-256">Dies ist die Standardeinstellung, wenn keine Video Disk eingefügt wird.</span><span class="sxs-lookup"><span data-stu-id="f67a2-256">This is the default if no videodisc is inserted.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f67a2-257">Takt Inkrement-Rate</span><span class="sxs-lookup"><span data-stu-id="f67a2-257">clock increment rate</span></span></td>
<td><span data-ttu-id="f67a2-258">Gibt die Anzahl der untergeordneten Bereiche zurück, die die externe Uhr pro Sekunde unterstützt.</span><span class="sxs-lookup"><span data-stu-id="f67a2-258">Returns the number of subdivisions the external clock supports per second.</span></span> <span data-ttu-id="f67a2-259">Wenn die externe Uhr eine millisekundenuhr ist, ist der Rückgabewert 1000.</span><span class="sxs-lookup"><span data-stu-id="f67a2-259">If the external clock is a millisecond clock, the return value is 1000.</span></span> <span data-ttu-id="f67a2-260">Wenn der Rückgabewert 0 (null) ist, wird keine Uhr unterstützt.</span><span class="sxs-lookup"><span data-stu-id="f67a2-260">If the return value is 0, no clock is supported.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f67a2-261">clv</span><span class="sxs-lookup"><span data-stu-id="f67a2-261">clv</span></span></td>
<td><span data-ttu-id="f67a2-262">In Kombination mit anderen Elementen gibt dieses Flag an, dass die Rückgabe Informationen auf Videodisks im CLV-Format zutreffen.</span><span class="sxs-lookup"><span data-stu-id="f67a2-262">When combined with other items, this flag specifies that the return information applies to CLV format videodiscs.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f67a2-263">Verbund Gerät</span><span class="sxs-lookup"><span data-stu-id="f67a2-263">compound device</span></span></td>
<td><span data-ttu-id="f67a2-264">Gibt <strong>true</strong> zurück, wenn das Gerät einen Elementnamen (Dateiname) unterstützt.</span><span class="sxs-lookup"><span data-stu-id="f67a2-264">Returns <strong>TRUE</strong> if the device supports an element name (filename).</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f67a2-265">Gerätetyp</span><span class="sxs-lookup"><span data-stu-id="f67a2-265">device type</span></span></td>
<td><span data-ttu-id="f67a2-266">Gibt einen Gerätetyp Namen zurück, bei dem es sich um einen der folgenden Typen handeln kann:</span><span class="sxs-lookup"><span data-stu-id="f67a2-266">Returns a device type name, which can be one of the following:</span></span>
<ul>
<li><span data-ttu-id="f67a2-267">CDAudio</span><span class="sxs-lookup"><span data-stu-id="f67a2-267">cdaudio</span></span></li>
<li><span data-ttu-id="f67a2-268">Hütte</span><span class="sxs-lookup"><span data-stu-id="f67a2-268">dat</span></span></li>
<li><span data-ttu-id="f67a2-269">Digitalvideo</span><span class="sxs-lookup"><span data-stu-id="f67a2-269">digitalvideo</span></span></li>
<li><span data-ttu-id="f67a2-270">andere</span><span class="sxs-lookup"><span data-stu-id="f67a2-270">other</span></span></li>
<li><span data-ttu-id="f67a2-271">overlay</span><span class="sxs-lookup"><span data-stu-id="f67a2-271">overlay</span></span></li>
<li><span data-ttu-id="f67a2-272">Scanner</span><span class="sxs-lookup"><span data-stu-id="f67a2-272">scanner</span></span></li>
<li><span data-ttu-id="f67a2-273">sequencer</span><span class="sxs-lookup"><span data-stu-id="f67a2-273">sequencer</span></span></li>
<li><span data-ttu-id="f67a2-274">VCR</span><span class="sxs-lookup"><span data-stu-id="f67a2-274">vcr</span></span></li>
<li><span data-ttu-id="f67a2-275">Videodisk</span><span class="sxs-lookup"><span data-stu-id="f67a2-275">videodisc</span></span></li>
<li><span data-ttu-id="f67a2-276">waveaudiodatei</span><span class="sxs-lookup"><span data-stu-id="f67a2-276">waveaudio</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f67a2-277">schnelle Wiedergabe Rate</span><span class="sxs-lookup"><span data-stu-id="f67a2-277">fast play rate</span></span></td>
<td><span data-ttu-id="f67a2-278">Gibt die schnelle Wiedergabe Rate in Frames pro Sekunde zurück, oder 0 (null), wenn das Gerät nicht schnell wiedergegeben werden kann.</span><span class="sxs-lookup"><span data-stu-id="f67a2-278">Returns the fast play rate in frames per second, or zero if the device cannot play fast.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f67a2-279">hat Audiodaten</span><span class="sxs-lookup"><span data-stu-id="f67a2-279">has audio</span></span></td>
<td><span data-ttu-id="f67a2-280">Gibt " <strong>true</strong> " zurück, wenn das Gerät Audiowiedergabe unterstützt.</span><span class="sxs-lookup"><span data-stu-id="f67a2-280">Returns <strong>TRUE</strong> if the device supports audio playback.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f67a2-281">hat Uhr</span><span class="sxs-lookup"><span data-stu-id="f67a2-281">has clock</span></span></td>
<td><span data-ttu-id="f67a2-282">Gibt " <strong>true</strong> " zurück, wenn das Gerät eine Uhr hat.</span><span class="sxs-lookup"><span data-stu-id="f67a2-282">Returns <strong>TRUE</strong> if the device has a clock.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f67a2-283">hat noch</span><span class="sxs-lookup"><span data-stu-id="f67a2-283">has still</span></span></td>
<td><span data-ttu-id="f67a2-284">Gibt " <strong>true</strong> " zurück, wenn das Gerät Dateien mit einem einzelnen Bild effizienter behandelt als Bewegungsvideo Dateien.</span><span class="sxs-lookup"><span data-stu-id="f67a2-284">Returns <strong>TRUE</strong> if the device treats files with a single image more efficiently than motion video files.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f67a2-285">hat Zeitcode</span><span class="sxs-lookup"><span data-stu-id="f67a2-285">has timecode</span></span></td>
<td><span data-ttu-id="f67a2-286">Gibt " <strong>true</strong> " zurück, wenn das Gerät Timecode unterstützen kann oder unbekannt ist.</span><span class="sxs-lookup"><span data-stu-id="f67a2-286">Returns <strong>TRUE</strong> if the device is capable of supporting timecode, or if it is unknown.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f67a2-287">hat Video</span><span class="sxs-lookup"><span data-stu-id="f67a2-287">has video</span></span></td>
<td><span data-ttu-id="f67a2-288">Gibt <strong>true</strong> zurück, wenn das Gerät Video unterstützt.</span><span class="sxs-lookup"><span data-stu-id="f67a2-288">Returns <strong>TRUE</strong> if the device supports video.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f67a2-289">inputs</span><span class="sxs-lookup"><span data-stu-id="f67a2-289">inputs</span></span></td>
<td><span data-ttu-id="f67a2-290">Gibt die Gesamtzahl der Eingabegeräte zurück.</span><span class="sxs-lookup"><span data-stu-id="f67a2-290">Returns the total number of input devices.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f67a2-291">maximale Wiedergabe Rate</span><span class="sxs-lookup"><span data-stu-id="f67a2-291">maximum play rate</span></span></td>
<td><span data-ttu-id="f67a2-292">Gibt die maximale Wiedergabe Rate in Frames pro Sekunde für das Gerät zurück.</span><span class="sxs-lookup"><span data-stu-id="f67a2-292">Returns the maximum play rate, in frames per second, for the device.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f67a2-293">minimale Wiedergabe Rate</span><span class="sxs-lookup"><span data-stu-id="f67a2-293">minimum play rate</span></span></td>
<td><span data-ttu-id="f67a2-294">Gibt die minimale Wiedergabe Rate (in Frames pro Sekunde) für das Gerät zurück.</span><span class="sxs-lookup"><span data-stu-id="f67a2-294">Returns the minimum play rate, in frames per second, for the device.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f67a2-295">normale Wiedergabe Rate</span><span class="sxs-lookup"><span data-stu-id="f67a2-295">normal play rate</span></span></td>
<td><span data-ttu-id="f67a2-296">Gibt die normale Wiedergabe Rate in Frames pro Sekunde für das Gerät zurück.</span><span class="sxs-lookup"><span data-stu-id="f67a2-296">Returns the normal play rate, in frames per second, for the device.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f67a2-297">Anzahl der Markierungen</span><span class="sxs-lookup"><span data-stu-id="f67a2-297">number of marks</span></span></td>
<td><span data-ttu-id="f67a2-298">Gibt die maximale Anzahl von Markierungen zurück, die verwendet werden können. NULL gibt an, dass Marken nicht unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="f67a2-298">Returns the maximum number of marks that can be used; zero indicates that marks are unsupported.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f67a2-299">outputs</span><span class="sxs-lookup"><span data-stu-id="f67a2-299">outputs</span></span></td>
<td><span data-ttu-id="f67a2-300">Gibt die Gesamtanzahl der Ausgabegeräte zurück.</span><span class="sxs-lookup"><span data-stu-id="f67a2-300">Returns the total number of output devices.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f67a2-301">Genauigkeit suchen</span><span class="sxs-lookup"><span data-stu-id="f67a2-301">seek accuracy</span></span></td>
<td><span data-ttu-id="f67a2-302">Gibt die erwartete Genauigkeit einer Suche in Frames zurück. 0 gibt an, dass das Gerät Frame genau ist, 1 gibt an, dass das Gerät erwartet, dass es sich innerhalb eines Rahmens der bestimmten Suchposition befindet, usw.</span><span class="sxs-lookup"><span data-stu-id="f67a2-302">Returns the expected accuracy of a search in frames; 0 indicates that the device is frame accurate, 1 indicates that the device expects to be within one frame of the indicated seek position, and so on.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f67a2-303">Langsame Wiedergabe Rate</span><span class="sxs-lookup"><span data-stu-id="f67a2-303">slow play rate</span></span></td>
<td><span data-ttu-id="f67a2-304">Gibt die langsame Wiedergabe Rate in Frames pro Sekunde zurück, oder 0 (null), wenn das Gerät nicht langsam wiedergegeben werden kann.</span><span class="sxs-lookup"><span data-stu-id="f67a2-304">Returns the slow play rate in frames per second, or zero if the device cannot play slowly.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f67a2-305">verwendet Dateien</span><span class="sxs-lookup"><span data-stu-id="f67a2-305">uses files</span></span></td>
<td><span data-ttu-id="f67a2-306">Gibt <strong>true</strong> zurück, wenn der von einem Verbund Gerät verwendete Datenspeicher eine Datei ist.</span><span class="sxs-lookup"><span data-stu-id="f67a2-306">Returns <strong>TRUE</strong> if the data storage used by a compound device is a file.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f67a2-307">verwendet Paletten</span><span class="sxs-lookup"><span data-stu-id="f67a2-307">uses palettes</span></span></td>
<td><span data-ttu-id="f67a2-308">Gibt " <strong>true</strong> " zurück, wenn das Gerät Paletten verwendet.</span><span class="sxs-lookup"><span data-stu-id="f67a2-308">Returns <strong>TRUE</strong> if the device uses palettes.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f67a2-309">Windows</span><span class="sxs-lookup"><span data-stu-id="f67a2-309">windows</span></span></td>
<td><span data-ttu-id="f67a2-310">Gibt die Anzahl der gleichzeitigen Anzeige Fenster zurück, die vom Gerät unterstützt werden können.</span><span class="sxs-lookup"><span data-stu-id="f67a2-310">Returns the number of simultaneous display windows the device can support.</span></span></td>
</tr>
</tbody>
</table>



 

</dd> <dt>

<span data-ttu-id="f67a2-311"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszflags*</span><span class="sxs-lookup"><span data-stu-id="f67a2-311"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="f67a2-312">Kann "wait", "notify" oder beides sein.</span><span class="sxs-lookup"><span data-stu-id="f67a2-312">Can be "wait", "notify", or both.</span></span> <span data-ttu-id="f67a2-313">Für Digital Video-und VCR-Geräte kann auch "Test" angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="f67a2-313">For digital-video and VCR devices, "test" can also be specified.</span></span> <span data-ttu-id="f67a2-314">Weitere Informationen zu diesen Flags finden Sie [unter warte-, Benachrichtigungs-und testflags](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="f67a2-314">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f67a2-315">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f67a2-315">Return Value</span></span>

<span data-ttu-id="f67a2-316">Gibt Informationen im *lpszreturnstring* -Parameter der [**mciSendString**](/previous-versions//dd757161(v=vs.85)) -Funktion zurück.</span><span class="sxs-lookup"><span data-stu-id="f67a2-316">Returns information in the *lpszReturnString* parameter of the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function.</span></span> <span data-ttu-id="f67a2-317">Die Informationen hängen vom Anforderungstyp ab.</span><span class="sxs-lookup"><span data-stu-id="f67a2-317">The information is dependent on the request type.</span></span>

## <a name="examples"></a><span data-ttu-id="f67a2-318">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f67a2-318">Examples</span></span>

<span data-ttu-id="f67a2-319">Mit dem folgenden Befehl wird der Gerätetyp des Geräts "mysound" zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="f67a2-319">The following command returns the device type of the "mysound" device.</span></span>

``` syntax
capability mysound device type
```

## <a name="requirements"></a><span data-ttu-id="f67a2-320">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f67a2-320">Requirements</span></span>



| <span data-ttu-id="f67a2-321">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f67a2-321">Requirement</span></span> | <span data-ttu-id="f67a2-322">Wert</span><span class="sxs-lookup"><span data-stu-id="f67a2-322">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="f67a2-323">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f67a2-323">Minimum supported client</span></span><br/> | <span data-ttu-id="f67a2-324">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f67a2-324">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="f67a2-325">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f67a2-325">Minimum supported server</span></span><br/> | <span data-ttu-id="f67a2-326">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f67a2-326">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="f67a2-327">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f67a2-327">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f67a2-328">MCI</span><span class="sxs-lookup"><span data-stu-id="f67a2-328">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="f67a2-329">MCI-Befehls Zeichenfolgen</span><span class="sxs-lookup"><span data-stu-id="f67a2-329">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> <dt>

[<span data-ttu-id="f67a2-330">STI</span><span class="sxs-lookup"><span data-stu-id="f67a2-330">cue</span></span>](cue.md)
</dt> </dl>

 

