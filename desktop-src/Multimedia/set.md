---
title: SET-Befehl
description: Mit dem SET-Befehl werden Steuerungseinstellungen für das Gerät festgelegt. CD-Audiodateien, Digital Video, MIDI Sequencer, VCR, Videodisk, Video-Overlay und Waveform-Audiogeräte erkennen diesen Befehl.
ms.assetid: 1ec4d84e-372a-4b6d-b694-f5afb41f90b2
keywords:
- SET-Befehl Windows Multimedia
topic_type:
- apiref
api_name:
- set
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 914743db038b0cae32b53fa79b7696ddba1ad05b
ms.sourcegitcommit: 8276af9231bdbf5a7334299f0d13fc8ff069a065
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/12/2021
ms.locfileid: "106363823"
---
# <a name="set-command"></a><span data-ttu-id="12cf5-105">SET-Befehl</span><span class="sxs-lookup"><span data-stu-id="12cf5-105">set command</span></span>

> [!NOTE]
> <span data-ttu-id="12cf5-106">Bias-freie Kommunikation Microsoft unterstützt eine unterschiedlichste und inklusive Umgebung.</span><span class="sxs-lookup"><span data-stu-id="12cf5-106">Bias-free Communication Microsoft supports a diverse and inclusionary environment.</span></span>  <span data-ttu-id="12cf5-107">In diesem Dokument sind Verweise auf das Wort "Slave" vorhanden.</span><span class="sxs-lookup"><span data-stu-id="12cf5-107">Within this document, there are references to the word 'slave.'</span></span> <span data-ttu-id="12cf5-108">Im [Stil Handbuch von Microsoft für die Bias-Free-Kommunikation](https://github.com/MicrosoftDocs/microsoft-style-guide/blob/master/styleguide/bias-free-communication.md) wird dies als ausschließendes Wort erkannt.</span><span class="sxs-lookup"><span data-stu-id="12cf5-108">Microsoft's [Style Guide for Bias-Free Communications](https://github.com/MicrosoftDocs/microsoft-style-guide/blob/master/styleguide/bias-free-communication.md) recognizes this as an exclusionary word.</span></span>  <span data-ttu-id="12cf5-109">Dieser Wortlaut wird verwendet, da es sich zurzeit um den in den Befehlen verwendeten Wortlaut handelt.</span><span class="sxs-lookup"><span data-stu-id="12cf5-109">This wording is used as it is currently the wording used within the commands.</span></span> <span data-ttu-id="12cf5-110">Aus Konsistenz Gründen enthält dieses Dokument dieses Wort.</span><span class="sxs-lookup"><span data-stu-id="12cf5-110">For consistency, this document contains this word.</span></span> <span data-ttu-id="12cf5-111">Wenn dieses Wort in den Befehlen geändert wird, korrigieren wir dieses Dokument als Ausrichtung.</span><span class="sxs-lookup"><span data-stu-id="12cf5-111">When this word is altered in the commands, we will correct this document to be in alignment.</span></span>


<span data-ttu-id="12cf5-112">Mit dem SET-Befehl werden Steuerungseinstellungen für das Gerät festgelegt.</span><span class="sxs-lookup"><span data-stu-id="12cf5-112">The set command establishes control settings for the device.</span></span> <span data-ttu-id="12cf5-113">CD-Audiodateien, Digital Video, MIDI Sequencer, VCR, Videodisk, Video-Overlay und Waveform-Audiogeräte erkennen diesen Befehl.</span><span class="sxs-lookup"><span data-stu-id="12cf5-113">CD audio, digital-video, MIDI sequencer, VCR, videodisc, video-overlay, and waveform-audio devices recognize this command.</span></span>

<span data-ttu-id="12cf5-114">Um diesen Befehl zu senden, wenden Sie die [**mciSendString**](/previous-versions//dd757161(v=vs.85)) -Funktion mit dem festgelegten *lpszcommand* -Parameter wie folgt an.</span><span class="sxs-lookup"><span data-stu-id="12cf5-114">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand,
  TEXT("set %s %s %s"),
  lpszDeviceID,
  lpszSetting,
  lpszFlags
);
      
```

## <a name="parameters"></a><span data-ttu-id="12cf5-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="12cf5-115">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="12cf5-116"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszde viceid*</span><span class="sxs-lookup"><span data-stu-id="12cf5-116"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="12cf5-117">Der Bezeichner eines MCI-Geräts.</span><span class="sxs-lookup"><span data-stu-id="12cf5-117">Identifier of an MCI device.</span></span> <span data-ttu-id="12cf5-118">Dieser Bezeichner oder Alias wird zugewiesen, wenn das Gerät geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="12cf5-118">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="12cf5-119"><span id="lpszSetting"></span><span id="lpszsetting"></span><span id="LPSZSETTING"></span>*lpszsetting*</span><span class="sxs-lookup"><span data-stu-id="12cf5-119"><span id="lpszSetting"></span><span id="lpszsetting"></span><span id="LPSZSETTING"></span>*lpszSetting*</span></span>
</dt> <dd>

<span data-ttu-id="12cf5-120">Flag zum Einrichten von Steuerungseinstellungen.</span><span class="sxs-lookup"><span data-stu-id="12cf5-120">Flag for establishing control settings.</span></span> <span data-ttu-id="12cf5-121">In der folgenden Tabelle werden die Gerätetypen aufgelistet, die den **Set** -Befehl und die von den einzelnen Typen verwendeten Flags erkennen.</span><span class="sxs-lookup"><span data-stu-id="12cf5-121">The following table lists device types that recognize the **set** command and the flags used by each type.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="12cf5-122">Gerätetyp</span><span class="sxs-lookup"><span data-stu-id="12cf5-122">Device Type</span></span></th>
<th><span data-ttu-id="12cf5-123">Befehlsflags</span><span class="sxs-lookup"><span data-stu-id="12cf5-123">Command Flags</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="12cf5-124">CDAudio</span><span class="sxs-lookup"><span data-stu-id="12cf5-124">cdaudio</span></span></td>
<td><ul>
<li><span data-ttu-id="12cf5-125">audioalles aus</span><span class="sxs-lookup"><span data-stu-id="12cf5-125">audio all off</span></span></li>
<li><span data-ttu-id="12cf5-126">alles audioon</span><span class="sxs-lookup"><span data-stu-id="12cf5-126">audio all on</span></span></li>
<li><span data-ttu-id="12cf5-127">Audiodaten ausgelassen</span><span class="sxs-lookup"><span data-stu-id="12cf5-127">audio left off</span></span></li>
<li><span data-ttu-id="12cf5-128">Audiodatei Links</span><span class="sxs-lookup"><span data-stu-id="12cf5-128">audio left on</span></span></li>
<li><span data-ttu-id="12cf5-129">Audiodaten direkt aus</span><span class="sxs-lookup"><span data-stu-id="12cf5-129">audio right off</span></span></li>
<li><span data-ttu-id="12cf5-130">Audiodaten direkt am</span><span class="sxs-lookup"><span data-stu-id="12cf5-130">audio right on</span></span></li>
<li><span data-ttu-id="12cf5-131">Tür geschlossen</span><span class="sxs-lookup"><span data-stu-id="12cf5-131">door closed</span></span></li>
<li><span data-ttu-id="12cf5-132">Tür geöffnet</span><span class="sxs-lookup"><span data-stu-id="12cf5-132">door open</span></span></li>
<li><span data-ttu-id="12cf5-133">Zeitformat (Millisekunden)</span><span class="sxs-lookup"><span data-stu-id="12cf5-133">time format milliseconds</span></span></li>
<li><span data-ttu-id="12cf5-134">Zeitformat MSF</span><span class="sxs-lookup"><span data-stu-id="12cf5-134">time format msf</span></span></li>
<li><span data-ttu-id="12cf5-135">Zeitformat-TMSF</span><span class="sxs-lookup"><span data-stu-id="12cf5-135">time format tmsf</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="12cf5-136">Digitalvideo</span><span class="sxs-lookup"><span data-stu-id="12cf5-136">digitalvideo</span></span></td>
<td><ul>
<li><span data-ttu-id="12cf5-137">audioalles aus</span><span class="sxs-lookup"><span data-stu-id="12cf5-137">audio all off</span></span></li>
<li><span data-ttu-id="12cf5-138">alles audioon</span><span class="sxs-lookup"><span data-stu-id="12cf5-138">audio all on</span></span></li>
<li><span data-ttu-id="12cf5-139">Audiodaten ausgelassen</span><span class="sxs-lookup"><span data-stu-id="12cf5-139">audio left off</span></span></li>
<li><span data-ttu-id="12cf5-140">Audiodatei Links</span><span class="sxs-lookup"><span data-stu-id="12cf5-140">audio left on</span></span></li>
<li><span data-ttu-id="12cf5-141">Audiodaten direkt aus</span><span class="sxs-lookup"><span data-stu-id="12cf5-141">audio right off</span></span></li>
<li><span data-ttu-id="12cf5-142">Audiodaten direkt am</span><span class="sxs-lookup"><span data-stu-id="12cf5-142">audio right on</span></span></li>
<li><span data-ttu-id="12cf5-143">Tür geschlossen</span><span class="sxs-lookup"><span data-stu-id="12cf5-143">door closed</span></span></li>
<li><span data-ttu-id="12cf5-144">Tür geöffnet</span><span class="sxs-lookup"><span data-stu-id="12cf5-144">door open</span></span></li>
<li><span data-ttu-id="12cf5-145">Dateiformat <em>Format</em></span><span class="sxs-lookup"><span data-stu-id="12cf5-145">file format <em>format</em></span></span></li>
<li><span data-ttu-id="12cf5-146">genau suchen</span><span class="sxs-lookup"><span data-stu-id="12cf5-146">seek exactly on</span></span></li>
<li><span data-ttu-id="12cf5-147">genau suchen</span><span class="sxs-lookup"><span data-stu-id="12cf5-147">seek exactly off</span></span></li>
<li><span data-ttu-id="12cf5-148">Geschwindigkeits <em>Faktor</em></span><span class="sxs-lookup"><span data-stu-id="12cf5-148">speed <em>factor</em></span></span></li>
<li><span data-ttu-id="12cf5-149">immer noch Dateiformat <em>Format</em></span><span class="sxs-lookup"><span data-stu-id="12cf5-149">still file format <em>format</em></span></span></li>
<li><span data-ttu-id="12cf5-150">Zeitformat Rahmen</span><span class="sxs-lookup"><span data-stu-id="12cf5-150">time format frames</span></span></li>
<li><span data-ttu-id="12cf5-151">Zeitformat (Millisekunden)</span><span class="sxs-lookup"><span data-stu-id="12cf5-151">time format milliseconds</span></span></li>
<li><span data-ttu-id="12cf5-152">Video aus</span><span class="sxs-lookup"><span data-stu-id="12cf5-152">video off</span></span></li>
<li><span data-ttu-id="12cf5-153">Video zum</span><span class="sxs-lookup"><span data-stu-id="12cf5-153">video on</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="12cf5-154">overlay</span><span class="sxs-lookup"><span data-stu-id="12cf5-154">overlay</span></span></td>
<td><ul>
<li><span data-ttu-id="12cf5-155">audioalles aus</span><span class="sxs-lookup"><span data-stu-id="12cf5-155">audio all off</span></span></li>
<li><span data-ttu-id="12cf5-156">alles audioon</span><span class="sxs-lookup"><span data-stu-id="12cf5-156">audio all on</span></span></li>
<li><span data-ttu-id="12cf5-157">Audiodaten ausgelassen</span><span class="sxs-lookup"><span data-stu-id="12cf5-157">audio left off</span></span></li>
<li><span data-ttu-id="12cf5-158">Audiodatei Links</span><span class="sxs-lookup"><span data-stu-id="12cf5-158">audio left on</span></span></li>
<li><span data-ttu-id="12cf5-159">Audiodaten direkt aus</span><span class="sxs-lookup"><span data-stu-id="12cf5-159">audio right off</span></span></li>
<li><span data-ttu-id="12cf5-160">Audiodaten direkt am</span><span class="sxs-lookup"><span data-stu-id="12cf5-160">audio right on</span></span></li>
<li><span data-ttu-id="12cf5-161">Tür geschlossen</span><span class="sxs-lookup"><span data-stu-id="12cf5-161">door closed</span></span></li>
<li><span data-ttu-id="12cf5-162">Tür geöffnet</span><span class="sxs-lookup"><span data-stu-id="12cf5-162">door open</span></span></li>
<li><span data-ttu-id="12cf5-163">Video aus</span><span class="sxs-lookup"><span data-stu-id="12cf5-163">video off</span></span></li>
<li><span data-ttu-id="12cf5-164">Video zum</span><span class="sxs-lookup"><span data-stu-id="12cf5-164">video on</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="12cf5-165">sequencer</span><span class="sxs-lookup"><span data-stu-id="12cf5-165">sequencer</span></span></td>
<td><ul>
<li><span data-ttu-id="12cf5-166">audioalles aus</span><span class="sxs-lookup"><span data-stu-id="12cf5-166">audio all off</span></span></li>
<li><span data-ttu-id="12cf5-167">alles audioon</span><span class="sxs-lookup"><span data-stu-id="12cf5-167">audio all on</span></span></li>
<li><span data-ttu-id="12cf5-168">Audiodaten ausgelassen</span><span class="sxs-lookup"><span data-stu-id="12cf5-168">audio left off</span></span></li>
<li><span data-ttu-id="12cf5-169">Audiodatei Links</span><span class="sxs-lookup"><span data-stu-id="12cf5-169">audio left on</span></span></li>
<li><span data-ttu-id="12cf5-170">Audiodaten direkt aus</span><span class="sxs-lookup"><span data-stu-id="12cf5-170">audio right off</span></span></li>
<li><span data-ttu-id="12cf5-171">Audiodaten direkt am</span><span class="sxs-lookup"><span data-stu-id="12cf5-171">audio right on</span></span></li>
<li><span data-ttu-id="12cf5-172">Tür geschlossen</span><span class="sxs-lookup"><span data-stu-id="12cf5-172">door closed</span></span></li>
<li><span data-ttu-id="12cf5-173">Tür geöffnet</span><span class="sxs-lookup"><span data-stu-id="12cf5-173">door open</span></span></li>
<li><span data-ttu-id="12cf5-174">Master-MIDI</span><span class="sxs-lookup"><span data-stu-id="12cf5-174">master MIDI</span></span></li>
<li><span data-ttu-id="12cf5-175">Master-None</span><span class="sxs-lookup"><span data-stu-id="12cf5-175">master none</span></span></li>
<li><span data-ttu-id="12cf5-176">Master-SMPTE</span><span class="sxs-lookup"><span data-stu-id="12cf5-176">master SMPTE</span></span></li>
<li><span data-ttu-id="12cf5-177">Offset <em>Zeit</em></span><span class="sxs-lookup"><span data-stu-id="12cf5-177">offset <em>time</em></span></span></li>
<li><span data-ttu-id="12cf5-178">Port-Mapper</span><span class="sxs-lookup"><span data-stu-id="12cf5-178">port mapper</span></span></li>
<li><span data-ttu-id="12cf5-179">Port None</span><span class="sxs-lookup"><span data-stu-id="12cf5-179">port none</span></span></li>
<li><span data-ttu-id="12cf5-180">Port <em>port_number</em></span><span class="sxs-lookup"><span data-stu-id="12cf5-180">port <em>port_number</em></span></span></li>
<li><span data-ttu-id="12cf5-181">Slave-Datei</span><span class="sxs-lookup"><span data-stu-id="12cf5-181">slave file</span></span></li>
<li><span data-ttu-id="12cf5-182">Slave (MIDI)</span><span class="sxs-lookup"><span data-stu-id="12cf5-182">slave MIDI</span></span></li>
<li><span data-ttu-id="12cf5-183">Slave None</span><span class="sxs-lookup"><span data-stu-id="12cf5-183">slave none</span></span></li>
<li><span data-ttu-id="12cf5-184">Slave-SMPTE</span><span class="sxs-lookup"><span data-stu-id="12cf5-184">slave SMPTE</span></span></li>
<li><span data-ttu-id="12cf5-185"><em>tempo_value</em> in Tempo</span><span class="sxs-lookup"><span data-stu-id="12cf5-185">tempo <em>tempo_value</em></span></span></li>
<li><span data-ttu-id="12cf5-186">Zeitformat (Millisekunden)</span><span class="sxs-lookup"><span data-stu-id="12cf5-186">time format milliseconds</span></span></li>
<li><span data-ttu-id="12cf5-187">Zeitformat-SMPTE- <em>fps</em></span><span class="sxs-lookup"><span data-stu-id="12cf5-187">time format SMPTE <em>fps</em></span></span></li>
<li><span data-ttu-id="12cf5-188">Zeitformat SMPTE 30 Drop</span><span class="sxs-lookup"><span data-stu-id="12cf5-188">time format SMPTE 30 drop</span></span></li>
<li><span data-ttu-id="12cf5-189">Zeiger für Zeitformat Titel</span><span class="sxs-lookup"><span data-stu-id="12cf5-189">time format song pointer</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="12cf5-190"><strong>VCR</strong></span><span class="sxs-lookup"><span data-stu-id="12cf5-190"><strong>vcr</strong></span></span></td>
<td><ul>
<li><span data-ttu-id="12cf5-191">Datensatz Assemblieren auf</span><span class="sxs-lookup"><span data-stu-id="12cf5-191">assemble record on</span></span></li>
<li><span data-ttu-id="12cf5-192">Datensatz aus Assemblieren</span><span class="sxs-lookup"><span data-stu-id="12cf5-192">assemble record off</span></span></li>
<li><span data-ttu-id="12cf5-193">audioalles aus</span><span class="sxs-lookup"><span data-stu-id="12cf5-193">audio all off</span></span></li>
<li><span data-ttu-id="12cf5-194">alles audioon</span><span class="sxs-lookup"><span data-stu-id="12cf5-194">audio all on</span></span></li>
<li><span data-ttu-id="12cf5-195">Audiodaten ausgelassen</span><span class="sxs-lookup"><span data-stu-id="12cf5-195">audio left off</span></span></li>
<li><span data-ttu-id="12cf5-196">Audiodatei Links</span><span class="sxs-lookup"><span data-stu-id="12cf5-196">audio left on</span></span></li>
<li><span data-ttu-id="12cf5-197">Audiodaten direkt aus</span><span class="sxs-lookup"><span data-stu-id="12cf5-197">audio right off</span></span></li>
<li><span data-ttu-id="12cf5-198">Audiodaten direkt am</span><span class="sxs-lookup"><span data-stu-id="12cf5-198">audio right on</span></span></li>
<li><span data-ttu-id="12cf5-199"><em>Uhrzeit</em></span><span class="sxs-lookup"><span data-stu-id="12cf5-199">clock <em>time</em></span></span></li>
<li><span data-ttu-id="12cf5-200">Counter-Format</span><span class="sxs-lookup"><span data-stu-id="12cf5-200">counter format</span></span></li>
<li><span data-ttu-id="12cf5-201"><em>Leistungswert</em></span><span class="sxs-lookup"><span data-stu-id="12cf5-201">counter <em>value</em></span></span></li>
<li><span data-ttu-id="12cf5-202">Tür geschlossen</span><span class="sxs-lookup"><span data-stu-id="12cf5-202">door closed</span></span></li>
<li><span data-ttu-id="12cf5-203">Tür geöffnet</span><span class="sxs-lookup"><span data-stu-id="12cf5-203">door open</span></span></li>
<li><span data-ttu-id="12cf5-204">Index Indikator</span><span class="sxs-lookup"><span data-stu-id="12cf5-204">index counter</span></span></li>
<li><span data-ttu-id="12cf5-205">Index Datum</span><span class="sxs-lookup"><span data-stu-id="12cf5-205">index date</span></span></li>
<li><span data-ttu-id="12cf5-206">Index Zeit</span><span class="sxs-lookup"><span data-stu-id="12cf5-206">index time</span></span></li>
<li><span data-ttu-id="12cf5-207">Index Zeit</span><span class="sxs-lookup"><span data-stu-id="12cf5-207">index time</span></span></li>
<li><span data-ttu-id="12cf5-208">codelta ength- <em>Dauer</em></span><span class="sxs-lookup"><span data-stu-id="12cf5-208">codelength <em>duration</em></span></span></li>
<li><span data-ttu-id="12cf5-209"><em>Timeout</em> für Pause</span><span class="sxs-lookup"><span data-stu-id="12cf5-209">pause <em>timeout</em></span></span></li>
<li><span data-ttu-id="12cf5-210">Postroll Dauer-</span><span class="sxs-lookup"><span data-stu-id="12cf5-210">postroll duration -</span></span></li>
<li><span data-ttu-id="12cf5-211"><em>duration</em></span><span class="sxs-lookup"><span data-stu-id="12cf5-211"><em>duration</em></span></span></li>
<li><span data-ttu-id="12cf5-212">Einschalten</span><span class="sxs-lookup"><span data-stu-id="12cf5-212">power on</span></span></li>
<li><span data-ttu-id="12cf5-213">Ausschalten</span><span class="sxs-lookup"><span data-stu-id="12cf5-213">power off</span></span></li>
<li><span data-ttu-id="12cf5-214"><em>Dauer der</em> Vorabversion</span><span class="sxs-lookup"><span data-stu-id="12cf5-214">preroll duration <em>duration</em></span></span></li>
<li><span data-ttu-id="12cf5-215">Daten Satz Format SP</span><span class="sxs-lookup"><span data-stu-id="12cf5-215">record format SP</span></span></li>
<li><span data-ttu-id="12cf5-216">Daten Satz Format-LP</span><span class="sxs-lookup"><span data-stu-id="12cf5-216">record format LP</span></span></li>
<li><span data-ttu-id="12cf5-217">Daten Satz Format EP</span><span class="sxs-lookup"><span data-stu-id="12cf5-217">record format EP</span></span></li>
<li><span data-ttu-id="12cf5-218">Geschwindigkeits <em>Faktor</em></span><span class="sxs-lookup"><span data-stu-id="12cf5-218">speed <em>factor</em></span></span></li>
<li><span data-ttu-id="12cf5-219">Zeitformat Rahmen</span><span class="sxs-lookup"><span data-stu-id="12cf5-219">time format frames</span></span></li>
<li><span data-ttu-id="12cf5-220">Zeitformat (HMS)</span><span class="sxs-lookup"><span data-stu-id="12cf5-220">time format hms</span></span></li>
<li><span data-ttu-id="12cf5-221">Zeitformat (Millisekunden)</span><span class="sxs-lookup"><span data-stu-id="12cf5-221">time format milliseconds</span></span></li>
<li><span data-ttu-id="12cf5-222">Zeitformat MSF</span><span class="sxs-lookup"><span data-stu-id="12cf5-222">time format msf</span></span></li>
<li><span data-ttu-id="12cf5-223">Zeitformat-SMPTE- <em>fps</em></span><span class="sxs-lookup"><span data-stu-id="12cf5-223">time format SMPTE <em>fps</em></span></span></li>
<li><span data-ttu-id="12cf5-224">Zeitformat SMPTE 30 Drop</span><span class="sxs-lookup"><span data-stu-id="12cf5-224">time format SMPTE 30 drop</span></span></li>
<li><span data-ttu-id="12cf5-225">Zeitformat-TMSF</span><span class="sxs-lookup"><span data-stu-id="12cf5-225">time format tmsf</span></span></li>
<li><span data-ttu-id="12cf5-226">Zeit Modus-Counter</span><span class="sxs-lookup"><span data-stu-id="12cf5-226">time mode counter</span></span></li>
<li><span data-ttu-id="12cf5-227">Zeit Modus-Erkennung</span><span class="sxs-lookup"><span data-stu-id="12cf5-227">time mode detect</span></span></li>
<li><span data-ttu-id="12cf5-228">Zeit Modus-Zeitcode</span><span class="sxs-lookup"><span data-stu-id="12cf5-228">time mode timecode</span></span></li>
<li><span data-ttu-id="12cf5-229">Nachverfolgung Plus</span><span class="sxs-lookup"><span data-stu-id="12cf5-229">tracking plus</span></span></li>
<li><span data-ttu-id="12cf5-230">Nachverfolgung minus</span><span class="sxs-lookup"><span data-stu-id="12cf5-230">tracking minus</span></span></li>
<li><span data-ttu-id="12cf5-231">Nachverfolgung zurücksetzen</span><span class="sxs-lookup"><span data-stu-id="12cf5-231">tracking reset</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="12cf5-232">Videodisk</span><span class="sxs-lookup"><span data-stu-id="12cf5-232">videodisc</span></span></td>
<td><ul>
<li><span data-ttu-id="12cf5-233">audioalles aus</span><span class="sxs-lookup"><span data-stu-id="12cf5-233">audio all off</span></span></li>
<li><span data-ttu-id="12cf5-234">alles audioon</span><span class="sxs-lookup"><span data-stu-id="12cf5-234">audio all on</span></span></li>
<li><span data-ttu-id="12cf5-235">Audiodaten ausgelassen</span><span class="sxs-lookup"><span data-stu-id="12cf5-235">audio left off</span></span></li>
<li><span data-ttu-id="12cf5-236">Audiodatei Links</span><span class="sxs-lookup"><span data-stu-id="12cf5-236">audio left on</span></span></li>
<li><span data-ttu-id="12cf5-237">Audiodaten direkt aus</span><span class="sxs-lookup"><span data-stu-id="12cf5-237">audio right off</span></span></li>
<li><span data-ttu-id="12cf5-238">Audiodaten direkt am</span><span class="sxs-lookup"><span data-stu-id="12cf5-238">audio right on</span></span></li>
<li><span data-ttu-id="12cf5-239">Tür geschlossen</span><span class="sxs-lookup"><span data-stu-id="12cf5-239">door closed</span></span></li>
<li><span data-ttu-id="12cf5-240">Tür geöffnet</span><span class="sxs-lookup"><span data-stu-id="12cf5-240">door open</span></span></li>
<li><span data-ttu-id="12cf5-241">Zeitformat Rahmen</span><span class="sxs-lookup"><span data-stu-id="12cf5-241">time format frames</span></span></li>
<li><span data-ttu-id="12cf5-242">Zeitformat (HMS)</span><span class="sxs-lookup"><span data-stu-id="12cf5-242">time format hms</span></span></li>
<li><span data-ttu-id="12cf5-243">Zeitformat (Millisekunden)</span><span class="sxs-lookup"><span data-stu-id="12cf5-243">time format milliseconds</span></span></li>
<li><span data-ttu-id="12cf5-244">Zeitformat Verfolgung</span><span class="sxs-lookup"><span data-stu-id="12cf5-244">time format track</span></span></li>
<li><span data-ttu-id="12cf5-245">Video aus</span><span class="sxs-lookup"><span data-stu-id="12cf5-245">video off</span></span></li>
<li><span data-ttu-id="12cf5-246">Video zum</span><span class="sxs-lookup"><span data-stu-id="12cf5-246">video on</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="12cf5-247">waveaudiodatei</span><span class="sxs-lookup"><span data-stu-id="12cf5-247">waveaudio</span></span></td>
<td><ul>
<li><span data-ttu-id="12cf5-248">Ausrichtungs <em>Ganzzahl</em></span><span class="sxs-lookup"><span data-stu-id="12cf5-248">alignment <em>integer</em></span></span></li>
<li><span data-ttu-id="12cf5-249">beliebige Eingabe</span><span class="sxs-lookup"><span data-stu-id="12cf5-249">any input</span></span></li>
<li><span data-ttu-id="12cf5-250">beliebige Ausgabe</span><span class="sxs-lookup"><span data-stu-id="12cf5-250">any output</span></span></li>
<li><span data-ttu-id="12cf5-251">audioalles aus</span><span class="sxs-lookup"><span data-stu-id="12cf5-251">audio all off</span></span></li>
<li><span data-ttu-id="12cf5-252">alles audioon</span><span class="sxs-lookup"><span data-stu-id="12cf5-252">audio all on</span></span></li>
<li><span data-ttu-id="12cf5-253">Audiodaten ausgelassen</span><span class="sxs-lookup"><span data-stu-id="12cf5-253">audio left off</span></span></li>
<li><span data-ttu-id="12cf5-254">Audiodatei Links</span><span class="sxs-lookup"><span data-stu-id="12cf5-254">audio left on</span></span></li>
<li><span data-ttu-id="12cf5-255">Audiodaten direkt aus</span><span class="sxs-lookup"><span data-stu-id="12cf5-255">audio right off</span></span></li>
<li><span data-ttu-id="12cf5-256">Audiodaten direkt am</span><span class="sxs-lookup"><span data-stu-id="12cf5-256">audio right on</span></span></li>
<li><span data-ttu-id="12cf5-257">BitsPerSample- <em>BIT_COUNT</em></span><span class="sxs-lookup"><span data-stu-id="12cf5-257">bitspersample <em>bit_count</em></span></span></li>
<li><span data-ttu-id="12cf5-258">bytespersec- <em>byte_rate</em></span><span class="sxs-lookup"><span data-stu-id="12cf5-258">bytespersec <em>byte_rate</em></span></span></li>
<li><span data-ttu-id="12cf5-259">Kanäle <em>channel_count</em></span><span class="sxs-lookup"><span data-stu-id="12cf5-259">channels <em>channel_count</em></span></span></li>
<li><span data-ttu-id="12cf5-260">Tür geschlossen</span><span class="sxs-lookup"><span data-stu-id="12cf5-260">door closed</span></span></li>
<li><span data-ttu-id="12cf5-261">Tür geöffnet</span><span class="sxs-lookup"><span data-stu-id="12cf5-261">door open</span></span></li>
<li><span data-ttu-id="12cf5-262">Formattag PCM</span><span class="sxs-lookup"><span data-stu-id="12cf5-262">format tag pcm</span></span></li>
<li><span data-ttu-id="12cf5-263">tagtag <em></em> formatieren</span><span class="sxs-lookup"><span data-stu-id="12cf5-263">format tag <em>tag</em></span></span></li>
<li><span data-ttu-id="12cf5-264">Eingabe <em>Ganzzahl</em></span><span class="sxs-lookup"><span data-stu-id="12cf5-264">input <em>integer</em></span></span></li>
<li><span data-ttu-id="12cf5-265">Ausgabe <em>Ganzzahl</em></span><span class="sxs-lookup"><span data-stu-id="12cf5-265">output <em>integer</em></span></span></li>
<li><span data-ttu-id="12cf5-266">samplespersec- <em>Ganzzahl</em></span><span class="sxs-lookup"><span data-stu-id="12cf5-266">samplespersec <em>integer</em></span></span></li>
<li><span data-ttu-id="12cf5-267">Zeitformat (Bytes)</span><span class="sxs-lookup"><span data-stu-id="12cf5-267">time format bytes</span></span></li>
<li><span data-ttu-id="12cf5-268">Zeitformat (Millisekunden)</span><span class="sxs-lookup"><span data-stu-id="12cf5-268">time format milliseconds</span></span></li>
<li><span data-ttu-id="12cf5-269">Zeitformat Beispiele</span><span class="sxs-lookup"><span data-stu-id="12cf5-269">time format samples</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="12cf5-270">In der folgenden Tabelle werden die Flags aufgelistet, die im **lpszsetting** -Parameter und deren Bedeutung angegeben werden können.</span><span class="sxs-lookup"><span data-stu-id="12cf5-270">The following table lists the flags that can be specified in the **lpszSetting** parameter and their meanings.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="12cf5-271">Wert</span><span class="sxs-lookup"><span data-stu-id="12cf5-271">Value</span></span></th>
<th><span data-ttu-id="12cf5-272">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="12cf5-272">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="12cf5-273">Ausrichtungs <em>Ganzzahl</em></span><span class="sxs-lookup"><span data-stu-id="12cf5-273">alignment <em>integer</em></span></span></td>
<td><span data-ttu-id="12cf5-274">Legt die Ausrichtung von Datenblöcken relativ zum Beginn von Daten fest, die an das Waveform-Audiogerät übermittelt werden.</span><span class="sxs-lookup"><span data-stu-id="12cf5-274">Sets the alignment of data blocks relative to the start of data passed to the waveform-audio device.</span></span> <span data-ttu-id="12cf5-275">Die Datei wird in diesem Format gespeichert.</span><span class="sxs-lookup"><span data-stu-id="12cf5-275">The file is saved in this format.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="12cf5-276">beliebige Eingabe</span><span class="sxs-lookup"><span data-stu-id="12cf5-276">any input</span></span></td>
<td><span data-ttu-id="12cf5-277">Verwenden Sie alle Eingaben, die beim Aufzeichnen das aktuelle Format unterstützen.</span><span class="sxs-lookup"><span data-stu-id="12cf5-277">Use any input that supports the current format when recording.</span></span> <span data-ttu-id="12cf5-278">Dies ist die Standardeinstellung.</span><span class="sxs-lookup"><span data-stu-id="12cf5-278">This is the default setting.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="12cf5-279">beliebige Ausgabe</span><span class="sxs-lookup"><span data-stu-id="12cf5-279">any output</span></span></td>
<td><span data-ttu-id="12cf5-280">Verwenden Sie bei der Wiedergabe jede Ausgabe, die das aktuelle Format unterstützt.</span><span class="sxs-lookup"><span data-stu-id="12cf5-280">Use any output that supports the current format when playing.</span></span> <span data-ttu-id="12cf5-281">Dies ist die Standardoption.</span><span class="sxs-lookup"><span data-stu-id="12cf5-281">This is the default.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="12cf5-282">Datensatz Assemblieren auf</span><span class="sxs-lookup"><span data-stu-id="12cf5-282">assemble record on</span></span> <br/> <span data-ttu-id="12cf5-283">Datensatz aus Assemblieren</span><span class="sxs-lookup"><span data-stu-id="12cf5-283">assemble record off</span></span> <br/></td>
<td><span data-ttu-id="12cf5-284">Im Assemblierungs Modus werden alle Spuren gemäß der Definition des Geräts aufgezeichnet.</span><span class="sxs-lookup"><span data-stu-id="12cf5-284">In assemble mode, all tracks are recorded as defined by the device.</span></span> <span data-ttu-id="12cf5-285">Die meisten VCRs befinden sich standardmäßig im assemblierungsmodus.</span><span class="sxs-lookup"><span data-stu-id="12cf5-285">Most VCRs are in assemble mode by default.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="12cf5-286">audioalles aus</span><span class="sxs-lookup"><span data-stu-id="12cf5-286">audio all off</span></span> <br/> <span data-ttu-id="12cf5-287">alles audioon</span><span class="sxs-lookup"><span data-stu-id="12cf5-287">audio all on</span></span> <br/></td>
<td><span data-ttu-id="12cf5-288">Deaktiviert oder aktiviert die Audioausgabe.</span><span class="sxs-lookup"><span data-stu-id="12cf5-288">Disables or enables audio output.</span></span> <span data-ttu-id="12cf5-289">Dieses Flag wird von Video Überlagerungs Geräten, dem mciseq-Sequencer und dem MCIWave Waveform-Audiogerät nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="12cf5-289">Video-overlay devices, the MCISEQ sequencer, and the MCIWAVE waveform-audio device do not support this flag.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="12cf5-290">Audiodaten ausgelassen</span><span class="sxs-lookup"><span data-stu-id="12cf5-290">audio left off</span></span> <br/> <span data-ttu-id="12cf5-291">Audiodatei Links</span><span class="sxs-lookup"><span data-stu-id="12cf5-291">audio left on</span></span> <br/> <span data-ttu-id="12cf5-292">Audiodaten direkt aus</span><span class="sxs-lookup"><span data-stu-id="12cf5-292">audio right off</span></span> <br/> <span data-ttu-id="12cf5-293">Audiodaten direkt am</span><span class="sxs-lookup"><span data-stu-id="12cf5-293">audio right on</span></span> <br/></td>
<td><span data-ttu-id="12cf5-294">Deaktiviert oder aktiviert die Ausgabe entweder auf den linken oder den rechten Audiokanal.</span><span class="sxs-lookup"><span data-stu-id="12cf5-294">Disables or enables output to either the left or the right audio channel.</span></span> <span data-ttu-id="12cf5-295">Dieses Flag wird von Video Überlagerungs Geräten, dem mciseq-Sequencer und dem MCIWave Waveform-Audiogerät nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="12cf5-295">Video-overlay devices, the MCISEQ sequencer, and the MCIWAVE waveform-audio device do not support this flag.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="12cf5-296">BitsPerSample- <em>BIT_COUNT</em></span><span class="sxs-lookup"><span data-stu-id="12cf5-296">bitspersample <em>bit_count</em></span></span></td>
<td><span data-ttu-id="12cf5-297">Legt die Anzahl von Bits pro PCM (Pulse Code-Modulation) fest, die abgespielt oder aufgezeichnet werden.</span><span class="sxs-lookup"><span data-stu-id="12cf5-297">Sets the number of bits per PCM (Pulse Code Modulation) sample played or recorded.</span></span> <span data-ttu-id="12cf5-298">Die Datei wird in diesem Format gespeichert.</span><span class="sxs-lookup"><span data-stu-id="12cf5-298">The file is saved in this format.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="12cf5-299">bytespersec- <em>byte_rate</em></span><span class="sxs-lookup"><span data-stu-id="12cf5-299">bytespersec <em>byte_rate</em></span></span></td>
<td><span data-ttu-id="12cf5-300">Legt die durchschnittliche Anzahl der wiedergegebenen oder aufgezeichneten Bytes pro Sekunde fest.</span><span class="sxs-lookup"><span data-stu-id="12cf5-300">Sets the average number of bytes per second played or recorded.</span></span> <span data-ttu-id="12cf5-301">Die Datei wird in diesem Format gespeichert.</span><span class="sxs-lookup"><span data-stu-id="12cf5-301">The file is saved in this format.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="12cf5-302">Kanäle <em>channel_count</em></span><span class="sxs-lookup"><span data-stu-id="12cf5-302">channels <em>channel_count</em></span></span></td>
<td><span data-ttu-id="12cf5-303">Legt die Kanäle für die Wiedergabe und Aufzeichnung fest.</span><span class="sxs-lookup"><span data-stu-id="12cf5-303">Sets the channels for playing and recording.</span></span> <span data-ttu-id="12cf5-304">Die Datei wird in diesem Format gespeichert.</span><span class="sxs-lookup"><span data-stu-id="12cf5-304">The file is saved in this format.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="12cf5-305"><em>Uhrzeit</em></span><span class="sxs-lookup"><span data-stu-id="12cf5-305">clock <em>time</em></span></span></td>
<td><span data-ttu-id="12cf5-306">Legt die Zeit für die externe Uhr auf die <em>Zeit fest.</em></span><span class="sxs-lookup"><span data-stu-id="12cf5-306">Sets time on the external clock to <em>time.</em></span></span> <span data-ttu-id="12cf5-307">Das Format wird als lange ganze Zahl ohne Vorzeichen angegeben.</span><span class="sxs-lookup"><span data-stu-id="12cf5-307">The format is specified as a long unsigned integer.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="12cf5-308">Counter-Format</span><span class="sxs-lookup"><span data-stu-id="12cf5-308">counter format</span></span></td>
<td><span data-ttu-id="12cf5-309">Legen Sie das Zeitformat des Zählers fest, wie vom <a href="status.md">Status</a> -Counter zurückgegeben &quot; &quot; .</span><span class="sxs-lookup"><span data-stu-id="12cf5-309">Set the time format for the counter, as returned by <a href="status.md">status</a> &quot;counter&quot;.</span></span> <span data-ttu-id="12cf5-310">Informationen zu den entsprechenden Typen finden Sie unter dem Befehl <strong>Set</strong> &quot; Time Format &quot; .</span><span class="sxs-lookup"><span data-stu-id="12cf5-310">For information about applicable types, see the <strong>set</strong> &quot;time format&quot; command.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="12cf5-311"><em>Leistungswert</em></span><span class="sxs-lookup"><span data-stu-id="12cf5-311">counter <em>value</em></span></span></td>
<td><span data-ttu-id="12cf5-312">Legt den VCR-Leistungsindikators auf den angegebenen Wert fest.</span><span class="sxs-lookup"><span data-stu-id="12cf5-312">Sets the VCR counter to the specified value.</span></span> <span data-ttu-id="12cf5-313">Der Wert muss im aktuellen Leistungswert Format angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="12cf5-313">The value must be specified in the current counter format.</span></span> <span data-ttu-id="12cf5-314">Weitere Informationen finden Sie unter dem Befehl <strong>Set</strong> &quot; Counter Format &quot; .</span><span class="sxs-lookup"><span data-stu-id="12cf5-314">For more information, see the <strong>set</strong> &quot;counter format&quot; command.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="12cf5-315">Tür geschlossen</span><span class="sxs-lookup"><span data-stu-id="12cf5-315">door closed</span></span></td>
<td><span data-ttu-id="12cf5-316">Zieht die Leiste zurück und schließt die Tür, wenn möglich.</span><span class="sxs-lookup"><span data-stu-id="12cf5-316">Retracts the tray and closes the door, if possible.</span></span> <span data-ttu-id="12cf5-317">Bei VCRs lädt das Band automatisch.</span><span class="sxs-lookup"><span data-stu-id="12cf5-317">For VCRs, loads the tape automatically.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="12cf5-318">Tür geöffnet</span><span class="sxs-lookup"><span data-stu-id="12cf5-318">door open</span></span></td>
<td><span data-ttu-id="12cf5-319">Öffnet die Tür und fügt, wenn möglich, die Leiste oder das Band ein.</span><span class="sxs-lookup"><span data-stu-id="12cf5-319">Opens the door and ejects the tray or tape, if possible.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="12cf5-320">Dateiformat <em>Format</em></span><span class="sxs-lookup"><span data-stu-id="12cf5-320">file format <em>format</em></span></span></td>
<td><span data-ttu-id="12cf5-321">Gibt ein Dateiformat an, das für Befehle zum <a href="save.md">Speichern</a> oder <a href="capture.md">erfassen</a> verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="12cf5-321">Specifies a file format that is used for <a href="save.md">save</a> or <a href="capture.md">capture</a> commands.</span></span> <span data-ttu-id="12cf5-322">Wenn der Wert nicht angegeben wird, wird standardmäßig ein Gerätetreiber definiertes Format festgelegt.</span><span class="sxs-lookup"><span data-stu-id="12cf5-322">If omitted, this might default to a device driver defined format.</span></span> <span data-ttu-id="12cf5-323">Wenn das angegebene Dateiformat mit dem aktuell ausgewählten Algorithmus und der ausgewählten Qualität in Konflikt steht, werden diese in die Standardwerte für das Dateiformat geändert.</span><span class="sxs-lookup"><span data-stu-id="12cf5-323">If the specified file format conflicts with the currently selected algorithm and quality, then they are changed to the defaults for the file format.</span></span> <span data-ttu-id="12cf5-324">Die folgenden Dateiformate sind definiert:</span><span class="sxs-lookup"><span data-stu-id="12cf5-324">The following file formats are defined:</span></span>
<ul>
<li><span data-ttu-id="12cf5-325">AVI: gibt das AVI-Format an.</span><span class="sxs-lookup"><span data-stu-id="12cf5-325">avi: Specifies AVI format.</span></span></li>
<li><span data-ttu-id="12cf5-326">avss: gibt das avss-Format an.</span><span class="sxs-lookup"><span data-stu-id="12cf5-326">avss: Specifies AVSS format.</span></span></li>
<li><span data-ttu-id="12cf5-327">DIB: gibt das DIB-Format an.</span><span class="sxs-lookup"><span data-stu-id="12cf5-327">dib: Specifies DIB format.</span></span></li>
<li><span data-ttu-id="12cf5-328">jff: gibt das jff-Format an.</span><span class="sxs-lookup"><span data-stu-id="12cf5-328">jfif: Specifies JFIF format.</span></span></li>
<li><span data-ttu-id="12cf5-329">JPEG: gibt das JPEG-Format an.</span><span class="sxs-lookup"><span data-stu-id="12cf5-329">jpeg: Specifies JPEG format.</span></span></li>
<li><span data-ttu-id="12cf5-330">MPEG: gibt das MPEG-Format an.</span><span class="sxs-lookup"><span data-stu-id="12cf5-330">mpeg: Specifies MPEG format.</span></span></li>
<li><span data-ttu-id="12cf5-331">rdib: gibt das RLE-DIB-Format an.</span><span class="sxs-lookup"><span data-stu-id="12cf5-331">rdib: Specifies RLE DIB format.</span></span></li>
<li><span data-ttu-id="12cf5-332">rjpeg: gibt das rjpeg-Format an.</span><span class="sxs-lookup"><span data-stu-id="12cf5-332">rjpeg: Specifies RJPEG format.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="12cf5-333">Formattag PCM</span><span class="sxs-lookup"><span data-stu-id="12cf5-333">format tag pcm</span></span></td>
<td><span data-ttu-id="12cf5-334">Legt den Formattyp für die Wiedergabe und Aufzeichnung auf PCM fest.</span><span class="sxs-lookup"><span data-stu-id="12cf5-334">Sets the format type to PCM for playing and recording.</span></span> <span data-ttu-id="12cf5-335">Die Datei wird in diesem Format gespeichert.</span><span class="sxs-lookup"><span data-stu-id="12cf5-335">The file is saved in this format.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="12cf5-336">tagtag <em></em> formatieren</span><span class="sxs-lookup"><span data-stu-id="12cf5-336">format tag <em>tag</em></span></span></td>
<td><span data-ttu-id="12cf5-337">Legt den Formattyp für die Wiedergabe und Aufzeichnung fest.</span><span class="sxs-lookup"><span data-stu-id="12cf5-337">Sets the format type for playing and recording.</span></span> <span data-ttu-id="12cf5-338">Die Datei wird in diesem Format gespeichert.</span><span class="sxs-lookup"><span data-stu-id="12cf5-338">The file is saved in this format.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="12cf5-339">Index Zeit Code</span><span class="sxs-lookup"><span data-stu-id="12cf5-339">index timecode</span></span> <br/> <span data-ttu-id="12cf5-340">Index Indikator</span><span class="sxs-lookup"><span data-stu-id="12cf5-340">index counter</span></span> <br/> <span data-ttu-id="12cf5-341">Index Datum</span><span class="sxs-lookup"><span data-stu-id="12cf5-341">index date</span></span> <br/> <span data-ttu-id="12cf5-342">Index Zeit</span><span class="sxs-lookup"><span data-stu-id="12cf5-342">index time</span></span> <br/></td>
<td><span data-ttu-id="12cf5-343">Legt den aktuellen Anzeige Bildschirm auf dem VCR fest.</span><span class="sxs-lookup"><span data-stu-id="12cf5-343">Sets the current display screen on the VCR.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="12cf5-344">Eingabe <em>Ganzzahl</em></span><span class="sxs-lookup"><span data-stu-id="12cf5-344">input <em>integer</em></span></span></td>
<td><span data-ttu-id="12cf5-345">Legt den Audiokanal fest, der als Eingabe verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="12cf5-345">Sets the audio channel used as the input.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="12cf5-346">Längen <em>Dauer</em></span><span class="sxs-lookup"><span data-stu-id="12cf5-346">length <em>duration</em></span></span></td>
<td><span data-ttu-id="12cf5-347">Legt die vom Benutzer angegebene Länge des Bands in der VCR fest.</span><span class="sxs-lookup"><span data-stu-id="12cf5-347">Sets the user-specified length of the tape in the VCR.</span></span> <span data-ttu-id="12cf5-348">Diese Länge wird durch den Befehl " <a href="status.md">Status</a> Länge" zurückgegeben &quot; &quot; und wird aus Gründen der Kompatibilität mit Anwendungen bereitgestellt, die erfordern, dass dieser Befehl eine gültige Länge zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="12cf5-348">This length is returned by the <a href="status.md">status</a> &quot;length&quot; command and is provided for compatibility with applications that require this command to return a valid length.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="12cf5-349">Master-MIDI</span><span class="sxs-lookup"><span data-stu-id="12cf5-349">master midi</span></span></td>
<td><span data-ttu-id="12cf5-350">Legt den MIDI-Sequencer als Synchronisierungs Quelle fest.</span><span class="sxs-lookup"><span data-stu-id="12cf5-350">Sets the MIDI sequencer as the synchronization source.</span></span> <span data-ttu-id="12cf5-351">Synchronisierungs Daten werden im Format "MIDI" gesendet.</span><span class="sxs-lookup"><span data-stu-id="12cf5-351">Synchronization data is sent in MIDI format.</span></span> <span data-ttu-id="12cf5-352">Das Flag wird von mciseq Sequencer nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="12cf5-352">The MCISEQ sequencer does not support this flag.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="12cf5-353">Master-None</span><span class="sxs-lookup"><span data-stu-id="12cf5-353">master none</span></span></td>
<td><span data-ttu-id="12cf5-354">Verhindert, dass der MIDI-Sequencer Synchronisierungs Daten sendet.</span><span class="sxs-lookup"><span data-stu-id="12cf5-354">Inhibits the MIDI sequencer from sending synchronization data.</span></span> <span data-ttu-id="12cf5-355">Das Flag wird von mciseq Sequencer nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="12cf5-355">The MCISEQ sequencer does not support this flag.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="12cf5-356">Master-SMPTE</span><span class="sxs-lookup"><span data-stu-id="12cf5-356">master smpte</span></span></td>
<td><span data-ttu-id="12cf5-357">Legt den MIDI-Sequencer als Synchronisierungs Quelle fest.</span><span class="sxs-lookup"><span data-stu-id="12cf5-357">Sets the MIDI sequencer as the synchronization source.</span></span> <span data-ttu-id="12cf5-358">Synchronisierungs Daten werden in SMPTE (Society of Motion Picture and TV Engineers)-Format gesendet.</span><span class="sxs-lookup"><span data-stu-id="12cf5-358">Synchronization data is sent in SMPTE (Society of Motion Picture and Television Engineers) format.</span></span> <span data-ttu-id="12cf5-359">Das Flag wird von mciseq Sequencer nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="12cf5-359">The MCISEQ sequencer does not support this flag.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="12cf5-360">Offset <em>Zeit</em></span><span class="sxs-lookup"><span data-stu-id="12cf5-360">offset <em>time</em></span></span></td>
<td><span data-ttu-id="12cf5-361">Legt die SMPTE-Offset <em>Zeit</em>fest.</span><span class="sxs-lookup"><span data-stu-id="12cf5-361">Sets the SMPTE offset <em>time</em>.</span></span> <span data-ttu-id="12cf5-362">Der Offset ist die Anfangszeit einer SMPTE-basierten Sequenz.</span><span class="sxs-lookup"><span data-stu-id="12cf5-362">The offset is the beginning time of a SMPTE based sequence.</span></span> <span data-ttu-id="12cf5-363">Die <em>Zeit</em> wird als <em>HH</em>: <em>mm</em>: <em>SS</em>: <em>FF</em>ausgedrückt, wobei <em>HH</em> Stunden, <em>mm</em> den Wert Minutes, <em>SS</em> den Wert Sekunden und <em>FF</em> ein Rahmen ist.</span><span class="sxs-lookup"><span data-stu-id="12cf5-363">The <em>time</em> is expressed as <em>hh</em>: <em>mm</em>: <em>ss</em>: <em>ff</em>, where <em>hh</em> is hours, <em>mm</em> is minutes, <em>ss</em> is seconds, and <em>ff</em> is frames.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="12cf5-364">Ausgabe <em>Ganzzahl</em></span><span class="sxs-lookup"><span data-stu-id="12cf5-364">output <em>integer</em></span></span></td>
<td><span data-ttu-id="12cf5-365">Legt den Audiokanal fest, der als Ausgabe verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="12cf5-365">Sets the audio channel used as the output.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="12cf5-366"><em>Timeout</em> für Pause</span><span class="sxs-lookup"><span data-stu-id="12cf5-366">pause <em>timeout</em></span></span></td>
<td><span data-ttu-id="12cf5-367">Legt die maximale Dauer eines <a href="pause.md">Pause</a> -Befehls in Millisekunden fest.</span><span class="sxs-lookup"><span data-stu-id="12cf5-367">Sets the maximum duration, in milliseconds, of a <a href="pause.md">pause</a> command.</span></span> <span data-ttu-id="12cf5-368">Ein <em>Timeout</em> Wert von 0 (null) gibt an, dass kein Timeout auftritt.</span><span class="sxs-lookup"><span data-stu-id="12cf5-368">A <em>timeout</em> value of zero indicates that no time-out will occur.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="12cf5-369"><em>Dauer des</em> postrollbacks</span><span class="sxs-lookup"><span data-stu-id="12cf5-369">postroll duration <em>duration</em></span></span></td>
<td><span data-ttu-id="12cf5-370">Legt die Länge im aktuellen Zeitformat fest, die zum Bremsen des VCR-Transports erforderlich ist, wenn <strong>ein Befehl zum</strong> <a href="stop.md">Beenden oder anhalten</a> ausgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="12cf5-370">Sets the length, in the current time format, needed to brake the VCR transport when a <a href="stop.md">stop</a> or <strong>pause</strong> command is issued.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="12cf5-371">Port-Mapper</span><span class="sxs-lookup"><span data-stu-id="12cf5-371">port mapper</span></span></td>
<td><span data-ttu-id="12cf5-372">Legt den MIDI-Mapper als Port fest, der die MIDI-Nachrichten empfängt.</span><span class="sxs-lookup"><span data-stu-id="12cf5-372">Sets the MIDI mapper as the port receiving the MIDI messages.</span></span> <span data-ttu-id="12cf5-373">Bei diesem Befehl tritt ein Fehler auf, wenn der von ihm benötigte MIDI-Mapper oder Port von einer anderen Anwendung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="12cf5-373">This command fails if the MIDI mapper or a port it needs is being used by another application.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="12cf5-374">Port None</span><span class="sxs-lookup"><span data-stu-id="12cf5-374">port none</span></span></td>
<td><span data-ttu-id="12cf5-375">Deaktiviert das Senden von MIDI-Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="12cf5-375">Disables the sending of MIDI messages.</span></span> <span data-ttu-id="12cf5-376">Dieser Befehl schließt außerdem einen MIDI-Port.</span><span class="sxs-lookup"><span data-stu-id="12cf5-376">This command also closes a MIDI port.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="12cf5-377">Port <em>port_number</em></span><span class="sxs-lookup"><span data-stu-id="12cf5-377">port <em>port_number</em></span></span></td>
<td><span data-ttu-id="12cf5-378">Legt den zum Empfangen der MIDI-Nachrichten empfangenden MIDI-Port</span><span class="sxs-lookup"><span data-stu-id="12cf5-378">Sets the MIDI port receiving the MIDI messages.</span></span> <span data-ttu-id="12cf5-379">Dieser Befehl schlägt fehl, wenn der Port, den Sie öffnen möchten, von einer anderen Anwendung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="12cf5-379">This command fails if the port you are trying to open is being used by another application.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="12cf5-380">Einschalten</span><span class="sxs-lookup"><span data-stu-id="12cf5-380">power on</span></span> <br/> <span data-ttu-id="12cf5-381">Ausschalten</span><span class="sxs-lookup"><span data-stu-id="12cf5-381">power off</span></span> <br/></td>
<td><span data-ttu-id="12cf5-382">Legt den Geräte Strom auf ein oder aus fest.</span><span class="sxs-lookup"><span data-stu-id="12cf5-382">Sets the device power to on or off.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="12cf5-383"><em>Dauer der</em> Vorabversion</span><span class="sxs-lookup"><span data-stu-id="12cf5-383">preroll duration <em>duration</em></span></span></td>
<td><span data-ttu-id="12cf5-384">Legt die Länge des aktuellen Zeit Formats fest, das zur Stabilisierung der VCR-Ausgabe benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="12cf5-384">Sets the length, in the current time format, needed to stabilize the VCR output.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="12cf5-385">Daten Satz Format SP</span><span class="sxs-lookup"><span data-stu-id="12cf5-385">record format SP</span></span> <br/> <span data-ttu-id="12cf5-386">Daten Satz Format-LP</span><span class="sxs-lookup"><span data-stu-id="12cf5-386">record format LP</span></span> <br/> <span data-ttu-id="12cf5-387">Daten Satz Format EP</span><span class="sxs-lookup"><span data-stu-id="12cf5-387">record format EP</span></span> <br/></td>
<td><span data-ttu-id="12cf5-388">Legt den Aufzeichnungsmodus für VCR auf SP für Standard Wiedergabe, EP für erweitertes spielen oder LP für langes spielen fest.</span><span class="sxs-lookup"><span data-stu-id="12cf5-388">Sets the recording mode for the VCR to SP for standard play, EP for extended play, or LP for long play.</span></span> <span data-ttu-id="12cf5-389">Diese Werte sind nicht als VHS-spezifisch vorgesehen.</span><span class="sxs-lookup"><span data-stu-id="12cf5-389">These values are not intended to be VHS specific.</span></span> <span data-ttu-id="12cf5-390">Sie werden drei geeigneten Modi mit anderen Band Formaten zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="12cf5-390">They map to any three appropriate modes with other tape formats.</span></span> <span data-ttu-id="12cf5-391">Beispielsweise wird SP der schnellsten, qualitativ hochwertigen Aufzeichnung zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="12cf5-391">For example, SP maps to the fastest, highest quality recording.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="12cf5-392">samplespersec- <em>Ganzzahl</em></span><span class="sxs-lookup"><span data-stu-id="12cf5-392">samplespersec <em>integer</em></span></span></td>
<td><span data-ttu-id="12cf5-393">Legt die Stichprobenrate für die Wiedergabe und Aufzeichnung fest.</span><span class="sxs-lookup"><span data-stu-id="12cf5-393">Sets the sample rate for playing and recording.</span></span> <span data-ttu-id="12cf5-394">Die Datei wird in diesem Format gespeichert.</span><span class="sxs-lookup"><span data-stu-id="12cf5-394">The file is saved in this format.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="12cf5-395">genau suchen</span><span class="sxs-lookup"><span data-stu-id="12cf5-395">seek exactly on</span></span><br/> <span data-ttu-id="12cf5-396">genau suchen</span><span class="sxs-lookup"><span data-stu-id="12cf5-396">seek exactly off</span></span> <br/></td>
<td><span data-ttu-id="12cf5-397">Wählt einen von zwei Suchmodi aus.</span><span class="sxs-lookup"><span data-stu-id="12cf5-397">Selects one of two seek modes.</span></span> <span data-ttu-id="12cf5-398">Wenn &quot; Sie die Suche genau durchführen &quot; , wechselt Seek immer zum angegebenen Frame.</span><span class="sxs-lookup"><span data-stu-id="12cf5-398">With &quot;seek exactly on&quot;, seek will always move to the frame specified.</span></span> <span data-ttu-id="12cf5-399">Bei einer &quot; genauen Suche &quot; wird die Suche zum nächsten Keyframe vor dem angegebenen Frame verschoben.</span><span class="sxs-lookup"><span data-stu-id="12cf5-399">With &quot;seek exactly off&quot;, seek will move to the closest key frame prior to the frame specified.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="12cf5-400">Slave-Datei</span><span class="sxs-lookup"><span data-stu-id="12cf5-400">slave file</span></span></td>
<td><span data-ttu-id="12cf5-401">Legt fest, dass der MIDI-Sequencer Datei Daten als Synchronisierungs Quelle verwendet.</span><span class="sxs-lookup"><span data-stu-id="12cf5-401">Sets the MIDI sequencer to use file data as the synchronization source.</span></span> <span data-ttu-id="12cf5-402">Dies ist die Standardeinstellung.</span><span class="sxs-lookup"><span data-stu-id="12cf5-402">This is the default setting.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="12cf5-403">Slave (MIDI)</span><span class="sxs-lookup"><span data-stu-id="12cf5-403">slave midi</span></span></td>
<td><span data-ttu-id="12cf5-404">Legt fest, dass der MIDI-Sequencer eingehende MIDI-Daten für die Synchronisierungs Quelle verwendet.</span><span class="sxs-lookup"><span data-stu-id="12cf5-404">Sets the MIDI sequencer to use incoming MIDI data for the synchronization source.</span></span> <span data-ttu-id="12cf5-405">Die Synchronisierungs Daten werden vom Sequencer mit dem Format "MIDI" erkannt.</span><span class="sxs-lookup"><span data-stu-id="12cf5-405">The sequencer recognizes synchronization data with the MIDI format.</span></span> <span data-ttu-id="12cf5-406">Das Flag wird von mciseq Sequencer nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="12cf5-406">The MCISEQ sequencer does not support this flag.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="12cf5-407">Slave None</span><span class="sxs-lookup"><span data-stu-id="12cf5-407">slave none</span></span></td>
<td><span data-ttu-id="12cf5-408">Legt fest, dass die Synchronisierung ignoriert wird.</span><span class="sxs-lookup"><span data-stu-id="12cf5-408">Sets the MIDI sequencer to ignore synchronization</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="12cf5-409">Slave-SMPTE</span><span class="sxs-lookup"><span data-stu-id="12cf5-409">slave smpte</span></span></td>
<td><span data-ttu-id="12cf5-410">Legt fest, dass der MIDI-Sequencer eingehende MIDI-Daten für die Synchronisierungs Quelle verwendet.</span><span class="sxs-lookup"><span data-stu-id="12cf5-410">Sets the MIDI sequencer to use incoming MIDI data for the synchronization source.</span></span> <span data-ttu-id="12cf5-411">Der Sequencer erkennt Synchronisierungs Daten mit dem SMPTE-Format.</span><span class="sxs-lookup"><span data-stu-id="12cf5-411">The sequencer recognizes synchronization data with the SMPTE format.</span></span> <span data-ttu-id="12cf5-412">Das Flag wird von mciseq Sequencer nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="12cf5-412">The MCISEQ sequencer does not support this flag.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="12cf5-413">Geschwindigkeitsfaktor</span><span class="sxs-lookup"><span data-stu-id="12cf5-413">speed factor</span></span></td>
<td><span data-ttu-id="12cf5-414">Legt die relative Geschwindigkeit der Video-und Audiowiedergabe aus dem Arbeitsbereich fest.</span><span class="sxs-lookup"><span data-stu-id="12cf5-414">Sets the relative speed of video and audio playback from the workspace.</span></span> <span data-ttu-id="12cf5-415">Der Faktor ist das Verhältnis zwischen der nominalen Frame Rate und der gewünschten Framerate, bei der die nominale frametrate als 1000 festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="12cf5-415">Factor is the ratio between the nominal frame rate and the desired frame rate, where the nominal frame rate is designated as 1000.</span></span> <span data-ttu-id="12cf5-416">(Eine Rate von 500 ist die halb normale Geschwindigkeit, 2000 ist die doppelte normale Geschwindigkeit usw.) Wenn Sie die Geschwindigkeit auf NULL festlegen, wird das Video so schnell wie möglich abgespielt, ohne Frames und ohne Audiodaten zu löschen.</span><span class="sxs-lookup"><span data-stu-id="12cf5-416">(A rate of 500 is half normal speed, 2000 is twice normal speed, and so on.) Setting the speed to zero plays the video as fast as possible without dropping frames and without audio.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="12cf5-417">immer noch Dateiformat <em>Format</em></span><span class="sxs-lookup"><span data-stu-id="12cf5-417">still file format <em>format</em></span></span></td>
<td><span data-ttu-id="12cf5-418">Gibt das für Aufzeichnungs Befehle verwendete Dateiformat an.</span><span class="sxs-lookup"><span data-stu-id="12cf5-418">Specifies the file format used for capture commands.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="12cf5-419">tempo_value in Tempo</span><span class="sxs-lookup"><span data-stu-id="12cf5-419">tempo tempo_value</span></span></td>
<td><span data-ttu-id="12cf5-420">Legt das Tempo der Sequenz entsprechend dem aktuellen Zeitformat fest.</span><span class="sxs-lookup"><span data-stu-id="12cf5-420">Sets the tempo of the sequence according to the current time format.</span></span> <span data-ttu-id="12cf5-421">Bei einer ppqn-basierten Datei wird die tempo_value als Beats pro Minute interpretiert.</span><span class="sxs-lookup"><span data-stu-id="12cf5-421">For a PPQN-based file, the tempo_value is interpreted as beats per minute.</span></span> <span data-ttu-id="12cf5-422">Bei einer SMPTE-basierten Datei wird die tempo_value als Frames pro Sekunde interpretiert.</span><span class="sxs-lookup"><span data-stu-id="12cf5-422">For a SMPTE-based file, the tempo_value is interpreted as frames per second.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="12cf5-423">Zeitformat (Bytes)</span><span class="sxs-lookup"><span data-stu-id="12cf5-423">time format bytes</span></span></td>
<td><span data-ttu-id="12cf5-424">In einem PCM-Dateiformat wird das Zeitformat auf Bytes festgelegt.</span><span class="sxs-lookup"><span data-stu-id="12cf5-424">In a PCM file format, sets the time format to bytes.</span></span> <span data-ttu-id="12cf5-425">Alle Positionsinformationen werden nach diesem Befehl als Bytes angegeben.</span><span class="sxs-lookup"><span data-stu-id="12cf5-425">All position information is specified as bytes following this command.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="12cf5-426">Zeitformat Rahmen</span><span class="sxs-lookup"><span data-stu-id="12cf5-426">time format frames</span></span></td>
<td><span data-ttu-id="12cf5-427">Legt das Zeitformat auf Frames fest.</span><span class="sxs-lookup"><span data-stu-id="12cf5-427">Sets the time format to frames.</span></span> <span data-ttu-id="12cf5-428">Alle Befehle, die Positionswerte verwenden, setzen Frames voraus.</span><span class="sxs-lookup"><span data-stu-id="12cf5-428">All commands that use position values will assume frames.</span></span> <span data-ttu-id="12cf5-429">Wenn das Gerät geöffnet ist, ist Frames der Standardmodus.</span><span class="sxs-lookup"><span data-stu-id="12cf5-429">When the device is opened, frames is the default mode.</span></span> <span data-ttu-id="12cf5-430">Wird von Videodisks unter Verwendung des CAV-Formats unterstützt.</span><span class="sxs-lookup"><span data-stu-id="12cf5-430">Supported by videodiscs using CAV format.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="12cf5-431">Zeitformat (HMS)</span><span class="sxs-lookup"><span data-stu-id="12cf5-431">time format hms</span></span></td>
<td><span data-ttu-id="12cf5-432">Legt das Zeitformat auf Stunden, Minuten und Sekunden fest.</span><span class="sxs-lookup"><span data-stu-id="12cf5-432">Sets the time format to hours, minutes, and seconds.</span></span> <span data-ttu-id="12cf5-433">Alle Befehle, die Positionswerte verwenden, gehen von "HMS" aus.</span><span class="sxs-lookup"><span data-stu-id="12cf5-433">All commands that use position values will assume HMS.</span></span> <span data-ttu-id="12cf5-434">HMS ist das Standardformat für CLV-Videodisks.</span><span class="sxs-lookup"><span data-stu-id="12cf5-434">HMS is the default format for CLV videodiscs.</span></span> <span data-ttu-id="12cf5-435">Geben Sie einen HMS-Wert als hh: mm: SS an, wobei HH Stunden, mm den Wert Minutes und SS den Wert Sekunden hat.</span><span class="sxs-lookup"><span data-stu-id="12cf5-435">Specify an HMS value as hh:mm:ss, where hh is hours, mm is minutes, and ss is seconds.</span></span> <span data-ttu-id="12cf5-436">Sie können ein Feld weglassen, wenn es und alle folgenden Felder NULL sind.</span><span class="sxs-lookup"><span data-stu-id="12cf5-436">You can omit a field if it and all following fields are zero.</span></span> <span data-ttu-id="12cf5-437">Beispielsweise sind 3, 3:0 und 3:0:0 alle gültigen Möglichkeiten, um 3 Stunden auszudrücken.</span><span class="sxs-lookup"><span data-stu-id="12cf5-437">For example, 3, 3:0, and 3:0:0 are all valid ways to express 3 hours.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="12cf5-438">Zeitformat (Millisekunden)</span><span class="sxs-lookup"><span data-stu-id="12cf5-438">time format milliseconds</span></span></td>
<td><span data-ttu-id="12cf5-439">Legt das Zeitformat auf Millisekunden fest.</span><span class="sxs-lookup"><span data-stu-id="12cf5-439">Sets the time format to milliseconds.</span></span> <span data-ttu-id="12cf5-440">Alle Befehle, die Positionswerte verwenden, nehmen Millisekunden an.</span><span class="sxs-lookup"><span data-stu-id="12cf5-440">All commands that use position values will assume milliseconds.</span></span> <span data-ttu-id="12cf5-441">Sie können Millisekunden als &quot; MS abkürzen &quot; .</span><span class="sxs-lookup"><span data-stu-id="12cf5-441">You can abbreviate milliseconds as &quot;ms&quot;.</span></span> <span data-ttu-id="12cf5-442">Bei Sequencer-Geräten legt die Sequenz Datei das Standardformat auf ppqn oder SMPTE fest.</span><span class="sxs-lookup"><span data-stu-id="12cf5-442">For sequencer devices, the sequence file sets the default format to PPQN or SMPTE.</span></span> <span data-ttu-id="12cf5-443">Das Flag wird von Video Überlagerungs Geräten nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="12cf5-443">Video-overlay devices do not support this flag.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="12cf5-444">Zeitformat MSF</span><span class="sxs-lookup"><span data-stu-id="12cf5-444">time format msf</span></span></td>
<td><span data-ttu-id="12cf5-445">Legt das Zeitformat auf Minuten, Sekunden und Frames fest.</span><span class="sxs-lookup"><span data-stu-id="12cf5-445">Sets the time format to minutes, seconds, and frames.</span></span> <span data-ttu-id="12cf5-446">Bei allen Befehlen, die Positionswerte verwenden, wird MSF (das Standardformat für CD-Audiodaten) angenommen.</span><span class="sxs-lookup"><span data-stu-id="12cf5-446">All commands that use position values will assume MSF (the default format for CD audio).</span></span> <span data-ttu-id="12cf5-447">Geben Sie einen MSF-Wert als mm: SS: FF an, wobei mm für Minuten, SS für Sekunden und FF für Frames steht.</span><span class="sxs-lookup"><span data-stu-id="12cf5-447">Specify an MSF value as mm:ss:ff, where mm is minutes, ss is seconds, and ff is frames.</span></span> <span data-ttu-id="12cf5-448">Sie können ein Feld weglassen, wenn es und alle folgenden Felder NULL sind.</span><span class="sxs-lookup"><span data-stu-id="12cf5-448">You can omit a field if it and all following fields are zero.</span></span> <span data-ttu-id="12cf5-449">Beispielsweise sind 3, 3:0 und 3:0:0 gültige Möglichkeiten, um 3 Minuten auszudrücken.</span><span class="sxs-lookup"><span data-stu-id="12cf5-449">For example, 3, 3:0, and 3:0:0 are valid ways to express 3 minutes.</span></span><br/> <span data-ttu-id="12cf5-450">Die MSF-Felder haben die folgenden maximalen Werte:</span><span class="sxs-lookup"><span data-stu-id="12cf5-450">The MSF fields have the following maximum values:</span></span><br/>
<ul>
<li><span data-ttu-id="12cf5-451">Minuten 99</span><span class="sxs-lookup"><span data-stu-id="12cf5-451">Minutes 99</span></span></li>
<li><span data-ttu-id="12cf5-452">Sekunden 59</span><span class="sxs-lookup"><span data-stu-id="12cf5-452">Seconds 59</span></span></li>
<li><span data-ttu-id="12cf5-453">Frames 74</span><span class="sxs-lookup"><span data-stu-id="12cf5-453">Frames 74</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="12cf5-454">Zeitformat Beispiele</span><span class="sxs-lookup"><span data-stu-id="12cf5-454">time format samples</span></span></td>
<td><span data-ttu-id="12cf5-455">Legt das Zeitformat auf Samples fest.</span><span class="sxs-lookup"><span data-stu-id="12cf5-455">Sets the time format to samples.</span></span> <span data-ttu-id="12cf5-456">Alle Positionsinformationen werden als Beispiele angegeben, die diesem Befehl folgen.</span><span class="sxs-lookup"><span data-stu-id="12cf5-456">All position information is specified as samples following this command.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="12cf5-457">Zeitformat SMPTE 24</span><span class="sxs-lookup"><span data-stu-id="12cf5-457">time format smpte 24</span></span><br/> <span data-ttu-id="12cf5-458">Uhrzeit Format SMPTE 25</span><span class="sxs-lookup"><span data-stu-id="12cf5-458">time format smpte 25</span></span><br/> <span data-ttu-id="12cf5-459">Uhrzeit Format SMPTE 30</span><span class="sxs-lookup"><span data-stu-id="12cf5-459">time format smpte 30</span></span><br/></td>
<td><span data-ttu-id="12cf5-460">Legt das Zeitformat auf eine SMPTE-Frame Rate fest.</span><span class="sxs-lookup"><span data-stu-id="12cf5-460">Sets the time format to an SMPTE frame rate.</span></span> <span data-ttu-id="12cf5-461">Für VCRs wird das Zeitformat auf HH: mm: SS: FF festgelegt, wobei die zulässigen Werte 00:00:00:00 bis 23:59:59: XX und XX kleiner als die Frames pro Sekunde sind, wie in der Zahl 24, 25 oder 30 angegeben, wie im-Flag angegeben.</span><span class="sxs-lookup"><span data-stu-id="12cf5-461">For VCRs, sets the time format to hh:mm:ss:ff, where the legal values are 00:00:00:00 through 23:59:59:xx, and xx is one less than the frames per second as specified by the number 24, 25, or 30 as specified in the flag.</span></span> <span data-ttu-id="12cf5-462">Bei Eingabe Doppelpunkte (:) sind erforderlich, um die Komponenten zu trennen.</span><span class="sxs-lookup"><span data-stu-id="12cf5-462">On input, colons (:) are required to separate the components.</span></span> <span data-ttu-id="12cf5-463">Die am wenigsten wichtigen Einheiten können ausgelassen werden, wenn Sie 00 sind. Beispielsweise ist 02:00 identisch mit 02:00:00:00.</span><span class="sxs-lookup"><span data-stu-id="12cf5-463">The least significant units can be omitted if they are 00; for example, 02:00 is the same as 02:00:00:00.</span></span> <span data-ttu-id="12cf5-464">Bei allen Befehlen, die Positionswerte verwenden, wird das SMPTE-Format angenommen.</span><span class="sxs-lookup"><span data-stu-id="12cf5-464">All commands that use position values will assume SMPTE format.</span></span><br/> <span data-ttu-id="12cf5-465">Die Sequenz Datei legt das Standardformat auf ppqn oder SMPTE fest.</span><span class="sxs-lookup"><span data-stu-id="12cf5-465">The sequence file sets the default format to PPQN or SMPTE.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="12cf5-466">Zeitformat SMPTE 30 Drop</span><span class="sxs-lookup"><span data-stu-id="12cf5-466">time format smpte 30 drop</span></span></td>
<td><span data-ttu-id="12cf5-467">Legt das Zeitformat auf SMPTE 30 Drop Frame Rate fest.</span><span class="sxs-lookup"><span data-stu-id="12cf5-467">Sets the time format to SMPTE 30 drop frame rate.</span></span> <span data-ttu-id="12cf5-468">Für VCRs, identisch mit SMPTE 30, mit der Ausnahme, dass bestimmte Zeit Code Positionen aus dem Format gelöscht werden, damit die aufgezeichneten Zeit Code Positionen für jeden Frame (mit der NTSC-frametrate von 29,97 fps) der Echt Zeit (bei 30 fps) entsprechen.</span><span class="sxs-lookup"><span data-stu-id="12cf5-468">For VCRs, same as SMPTE 30, except that certain timecode positions are dropped from the format to have the recorded timecode positions for each frame (at the NTSC frame rate of 29.97 fps) correspond to real time (at 30 fps).</span></span> <span data-ttu-id="12cf5-469">Die gelöschten Zeit Code Positionen lauten wie folgt: zwei Minuten pro Minute für die ersten neun von zehn Minuten aufgezeichneten Inhalts.</span><span class="sxs-lookup"><span data-stu-id="12cf5-469">Timecode positions that are dropped are as follows: two every minute, on the minute, for the first nine of every ten minutes of recorded content.</span></span> <span data-ttu-id="12cf5-470">Beispielsweise wäre bei 01:04:59:29 die nächste Zeit Code Position 01:05:00:02, nicht 01:05:00:00.</span><span class="sxs-lookup"><span data-stu-id="12cf5-470">For example, at 01:04:59:29, the next timecode position would be 01:05:00:02, not 01:05:00:00.</span></span> <span data-ttu-id="12cf5-471">Bei allen Befehlen, die Positionswerte verwenden, wird das SMPTE-Format angenommen.</span><span class="sxs-lookup"><span data-stu-id="12cf5-471">All commands that use position values will assume SMPTE format.</span></span><br/> <span data-ttu-id="12cf5-472">Die Sequenz Datei legt das Standardformat auf ppqn oder SMPTE fest.</span><span class="sxs-lookup"><span data-stu-id="12cf5-472">The sequence file sets the default format to PPQN or SMPTE.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="12cf5-473">Zeiger für Zeitformat Titel</span><span class="sxs-lookup"><span data-stu-id="12cf5-473">time format song pointer</span></span></td>
<td><span data-ttu-id="12cf5-474">Legt das Zeitformat auf einen Song Zeiger fest (sechzehnte Notizen).</span><span class="sxs-lookup"><span data-stu-id="12cf5-474">Sets the time format to song pointer (sixteenth notes).</span></span> <span data-ttu-id="12cf5-475">Bei allen Befehlen, die Positionswerte verwenden, wird von den Song Zeiger Einheiten ausgegangen.</span><span class="sxs-lookup"><span data-stu-id="12cf5-475">All commands that use position values will assume song pointer units.</span></span> <span data-ttu-id="12cf5-476">Dieses Flag ist nur für eine Sequenz des Divisions Typs "ppqn" gültig.</span><span class="sxs-lookup"><span data-stu-id="12cf5-476">This flag is valid only for a sequence of division type PPQN.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="12cf5-477">Zeitformat-TMSF</span><span class="sxs-lookup"><span data-stu-id="12cf5-477">time format tmsf</span></span></td>
<td><span data-ttu-id="12cf5-478">Legt das Zeitformat auf nachverfolgt, Minuten, Sekunden und Frames fest.</span><span class="sxs-lookup"><span data-stu-id="12cf5-478">Sets the time format to tracks, minutes, seconds, and frames.</span></span> <span data-ttu-id="12cf5-479">Alle Befehle, die Positionswerte verwenden, setzen TMSF voraus.</span><span class="sxs-lookup"><span data-stu-id="12cf5-479">All commands that use position values will assume TMSF.</span></span> <span data-ttu-id="12cf5-480">Geben Sie einen TMSF-Wert als TT: mm: SS: FF an, wobei TT nachverfolgt, mm den Wert Minutes, SS den Wert Sekunden und FF ein Rahmen ist.</span><span class="sxs-lookup"><span data-stu-id="12cf5-480">Specify a TMSF value as tt:mm:ss:ff, where tt is tracks, mm is minutes, ss is seconds, and ff is frames.</span></span> <span data-ttu-id="12cf5-481">Sie können ein Feld weglassen, wenn es und alle folgenden Felder NULL sind.</span><span class="sxs-lookup"><span data-stu-id="12cf5-481">You can omit a field if it and all following fields are zero.</span></span> <span data-ttu-id="12cf5-482">Beispielsweise sind 3, 3:0, 3:0:0 und 3:0:0:0 alle gültigen Methoden zum Ausdrücken von Track 3.</span><span class="sxs-lookup"><span data-stu-id="12cf5-482">For example, 3, 3:0, 3:0:0, and 3:0:0:0 are all valid ways to express track 3.</span></span> <br/> <span data-ttu-id="12cf5-483">Die TMSF-Felder haben die folgenden maximalen Werte:</span><span class="sxs-lookup"><span data-stu-id="12cf5-483">The TMSF fields have the following maximum values:</span></span><br/>
<ul>
<li><span data-ttu-id="12cf5-484">Nachverfolgt 99</span><span class="sxs-lookup"><span data-stu-id="12cf5-484">Tracks 99</span></span></li>
<li><span data-ttu-id="12cf5-485">Minuten 90</span><span class="sxs-lookup"><span data-stu-id="12cf5-485">Minutes 90</span></span></li>
<li><span data-ttu-id="12cf5-486">Sekunden 59</span><span class="sxs-lookup"><span data-stu-id="12cf5-486">Seconds 59</span></span></li>
<li><span data-ttu-id="12cf5-487">Frames 74</span><span class="sxs-lookup"><span data-stu-id="12cf5-487">Frames 74</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="12cf5-488">Zeitformat Verfolgung</span><span class="sxs-lookup"><span data-stu-id="12cf5-488">time format track</span></span></td>
<td><span data-ttu-id="12cf5-489">Legt das Positions Format auf "verfolgt" fest.</span><span class="sxs-lookup"><span data-stu-id="12cf5-489">Sets the position format to tracks.</span></span> <span data-ttu-id="12cf5-490">Alle Befehle, die Positionswerte verwenden, werden nachverfolgt.</span><span class="sxs-lookup"><span data-stu-id="12cf5-490">All commands that use position values will assume tracks.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="12cf5-491">Zeit Modus-Counter</span><span class="sxs-lookup"><span data-stu-id="12cf5-491">time mode counter</span></span></td>
<td><span data-ttu-id="12cf5-492">Legt den Positions Informationsmodus für die Verwendung der VCR-Indikatoren fest.</span><span class="sxs-lookup"><span data-stu-id="12cf5-492">Sets the position-information mode to use the VCR counters.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="12cf5-493">Zeit Modus-Erkennung</span><span class="sxs-lookup"><span data-stu-id="12cf5-493">time mode detect</span></span></td>
<td><span data-ttu-id="12cf5-494">Legt den Positions Informationsmodus basierend auf der Erkennung von Zeitcode-Informationen auf dem Band fest.</span><span class="sxs-lookup"><span data-stu-id="12cf5-494">Sets the position information mode based on detection of timecode information on the tape.</span></span> <span data-ttu-id="12cf5-495">Wenn Zeit Code Informationen erkannt werden, wird der Zeittyp auf &quot; Zeitcode festgelegt &quot; . andernfalls wird der Zeittyp auf Counter festgelegt &quot; &quot; .</span><span class="sxs-lookup"><span data-stu-id="12cf5-495">If timecode information is detected, the time type is set to &quot;timecode&quot;; otherwise, the time type is set to &quot;counter&quot;.</span></span> <span data-ttu-id="12cf5-496">&quot;"Erkennen" &quot; ist ein spezieller Modus.</span><span class="sxs-lookup"><span data-stu-id="12cf5-496">&quot;Detect&quot; is a special mode.</span></span> <span data-ttu-id="12cf5-497">Wenn der Treiber geöffnet wird, ein neues Band eingefügt oder der &quot; Zeit Modus- &quot; Befehl ausgegeben wird, überprüft der Treiber den aktuellen auf dem Band verfügbaren Zeit Modus und legt den &quot; Zeittyp &quot; auf &quot; Zeitcode &quot; oder Counter fest &quot; &quot; .</span><span class="sxs-lookup"><span data-stu-id="12cf5-497">Whenever the driver is opened, a new tape is inserted, or the &quot;time mode&quot; command is issued, the driver checks the current time mode available on the tape and sets &quot;time type&quot; to either &quot;timecode&quot; or &quot;counter&quot;.</span></span> <span data-ttu-id="12cf5-498">Sobald &quot; der Typ &quot; festgelegt ist, ändert der Treiber ihn erst, wenn eine der oben genannten Bedingungen erneut auftritt.</span><span class="sxs-lookup"><span data-stu-id="12cf5-498">Once &quot;time type&quot; is set, the driver doesn't change it until one of the above conditions occurs again.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="12cf5-499">Zeit Modus-Zeitcode</span><span class="sxs-lookup"><span data-stu-id="12cf5-499">time mode timecode</span></span></td>
<td><span data-ttu-id="12cf5-500">Legt den Positions Informationsmodus für die Verwendung &quot; von Zeit Code &quot; Informationen auf dem Band fest.</span><span class="sxs-lookup"><span data-stu-id="12cf5-500">Sets the position information mode to use &quot;timecode&quot; information on the tape.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="12cf5-501">Nachverfolgung Plus</span><span class="sxs-lookup"><span data-stu-id="12cf5-501">tracking plus</span></span> <br/> <span data-ttu-id="12cf5-502">Nachverfolgung minus</span><span class="sxs-lookup"><span data-stu-id="12cf5-502">tracking minus</span></span> <br/> <span data-ttu-id="12cf5-503">Nachverfolgung zurücksetzen</span><span class="sxs-lookup"><span data-stu-id="12cf5-503">tracking reset</span></span> <br/></td>
<td><span data-ttu-id="12cf5-504">Passt die Geschwindigkeit des Videoband-Transports in fein Inkrementen an.</span><span class="sxs-lookup"><span data-stu-id="12cf5-504">Adjusts the speed of the videotape transport in fine increments.</span></span> <span data-ttu-id="12cf5-505">Verwenden Sie &quot; die &quot; nachverfolgungsflags, wenn ein lautes Bild von einem VCR abgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="12cf5-505">Use the &quot;tracking&quot; flags when a noisy picture is obtained from a VCR.</span></span> <span data-ttu-id="12cf5-506">&quot;Die Nachverfolgung Plus &quot; erhöht die Transportgeschwindigkeit.</span><span class="sxs-lookup"><span data-stu-id="12cf5-506">&quot;Tracking plus&quot; increases the transport speed.</span></span> <span data-ttu-id="12cf5-507">&quot;Durch die Nachverfolgung minus wird &quot; die Transportgeschwindigkeit verringert.</span><span class="sxs-lookup"><span data-stu-id="12cf5-507">&quot;Tracking minus&quot; decreases the transport speed.</span></span> <span data-ttu-id="12cf5-508">&quot;Beim Zurücksetzen &quot; der Nachverfolgung wird die nach Verfolgungs Anpassung an 0</span><span class="sxs-lookup"><span data-stu-id="12cf5-508">&quot;Tracking reset&quot; returns the tracking adjustment to zero.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="12cf5-509">Video aus</span><span class="sxs-lookup"><span data-stu-id="12cf5-509">video off</span></span></td>
<td><span data-ttu-id="12cf5-510">Deaktiviert die Videoausgabe.</span><span class="sxs-lookup"><span data-stu-id="12cf5-510">Disables video output.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="12cf5-511">Video zum</span><span class="sxs-lookup"><span data-stu-id="12cf5-511">video on</span></span></td>
<td><span data-ttu-id="12cf5-512">Aktiviert die Videoausgabe.</span><span class="sxs-lookup"><span data-stu-id="12cf5-512">Enables video output.</span></span></td>
</tr>
</tbody>
</table>



 

</dd> <dt>

<span data-ttu-id="12cf5-513"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszflags*</span><span class="sxs-lookup"><span data-stu-id="12cf5-513"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="12cf5-514">Kann "wait", "notify" oder beides sein.</span><span class="sxs-lookup"><span data-stu-id="12cf5-514">Can be "wait", "notify", or both.</span></span> <span data-ttu-id="12cf5-515">Für Digital Video-und VCR-Geräte kann auch "Test" angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="12cf5-515">For digital-video and VCR devices, "test" can also be specified.</span></span> <span data-ttu-id="12cf5-516">Weitere Informationen zu diesen Flags finden Sie [unter warte-, Benachrichtigungs-und testflags](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="12cf5-516">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="12cf5-517">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="12cf5-517">Return Value</span></span>

<span data-ttu-id="12cf5-518">Gibt 0 (null) zurück, wenn erfolgreich, andernfalls einen Fehler.</span><span class="sxs-lookup"><span data-stu-id="12cf5-518">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="12cf5-519">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="12cf5-519">Remarks</span></span>

<span data-ttu-id="12cf5-520">Wenn die Datei zum Speichern der Daten erstellt wird, werden mehrere Eigenschaften von Waveform-Audiodaten definiert.</span><span class="sxs-lookup"><span data-stu-id="12cf5-520">Several properties of waveform-audio data are defined when the file to store the data is created.</span></span> <span data-ttu-id="12cf5-521">Diese Eigenschaften beschreiben, wie die Daten innerhalb der Datei strukturiert sind und nicht geändert werden können, wenn die Aufzeichnung beginnt.</span><span class="sxs-lookup"><span data-stu-id="12cf5-521">These properties describe how the data is structured within the file and cannot be changed once recording begins.</span></span> <span data-ttu-id="12cf5-522">Die folgenden Eigenschaften werden in der folgenden Liste aufgeführt:</span><span class="sxs-lookup"><span data-stu-id="12cf5-522">The following list identifies these properties:</span></span>

-   <span data-ttu-id="12cf5-523">Ausrichtung</span><span class="sxs-lookup"><span data-stu-id="12cf5-523">alignment</span></span>
-   <span data-ttu-id="12cf5-524">BitsPerSample</span><span class="sxs-lookup"><span data-stu-id="12cf5-524">bitspersample</span></span>
-   <span data-ttu-id="12cf5-525">bytespersec</span><span class="sxs-lookup"><span data-stu-id="12cf5-525">bytespersec</span></span>
-   <span data-ttu-id="12cf5-526">channels</span><span class="sxs-lookup"><span data-stu-id="12cf5-526">channels</span></span>
-   <span data-ttu-id="12cf5-527">Tag formatieren</span><span class="sxs-lookup"><span data-stu-id="12cf5-527">format tag</span></span>
-   <span data-ttu-id="12cf5-528">samplespersec</span><span class="sxs-lookup"><span data-stu-id="12cf5-528">samplespersec</span></span>

## <a name="examples"></a><span data-ttu-id="12cf5-529">Beispiele</span><span class="sxs-lookup"><span data-stu-id="12cf5-529">Examples</span></span>

<span data-ttu-id="12cf5-530">Mit dem folgenden Befehl wird das Zeitformat auf Millisekunden festgelegt, und das Waveform-Audioformat wird auf 8 Bit, Mono, 11 kHz festgelegt.</span><span class="sxs-lookup"><span data-stu-id="12cf5-530">The following command sets the time format to milliseconds and sets the waveform-audio format to 8 bit, mono, 11 kHz.</span></span>

``` syntax
set mysound time format ms bitspersample 8 channels 1 samplespersec 11025
```

## <a name="requirements"></a><span data-ttu-id="12cf5-531">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="12cf5-531">Requirements</span></span>



| <span data-ttu-id="12cf5-532">Anforderung</span><span class="sxs-lookup"><span data-stu-id="12cf5-532">Requirement</span></span> | <span data-ttu-id="12cf5-533">Wert</span><span class="sxs-lookup"><span data-stu-id="12cf5-533">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="12cf5-534">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="12cf5-534">Minimum supported client</span></span><br/> | <span data-ttu-id="12cf5-535">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="12cf5-535">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="12cf5-536">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="12cf5-536">Minimum supported server</span></span><br/> | <span data-ttu-id="12cf5-537">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="12cf5-537">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="12cf5-538">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="12cf5-538">See also</span></span>

<dl> <dt>

[<span data-ttu-id="12cf5-539">MCI</span><span class="sxs-lookup"><span data-stu-id="12cf5-539">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="12cf5-540">MCI-Befehls Zeichenfolgen</span><span class="sxs-lookup"><span data-stu-id="12cf5-540">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> <dt>

[<span data-ttu-id="12cf5-541">einver</span><span class="sxs-lookup"><span data-stu-id="12cf5-541">capture</span></span>](capture.md)
</dt> <dt>

[<span data-ttu-id="12cf5-542">pause</span><span class="sxs-lookup"><span data-stu-id="12cf5-542">pause</span></span>](pause.md)
</dt> <dt>

[<span data-ttu-id="12cf5-543">Speichern</span><span class="sxs-lookup"><span data-stu-id="12cf5-543">save</span></span>](save.md)
</dt> <dt>

[<span data-ttu-id="12cf5-544">stop</span><span class="sxs-lookup"><span data-stu-id="12cf5-544">stop</span></span>](stop.md)
</dt> </dl>

 

