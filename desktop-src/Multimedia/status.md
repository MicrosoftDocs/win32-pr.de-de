---
title: Status Befehl
description: Mit dem Status Befehl werden Statusinformationen von einem Gerät angefordert. Alle Geräte erkennen diesen Befehl.
ms.assetid: 39961bd7-866d-450d-9fbf-347a8f508481
keywords:
- Status Befehl Windows-Multimedia
topic_type:
- apiref
api_name:
- status
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 14ab184ddaca16d0ea96b86a6b062f1e66e2eee2
ms.sourcegitcommit: 8276af9231bdbf5a7334299f0d13fc8ff069a065
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/12/2021
ms.locfileid: "106361735"
---
# <a name="status-command"></a><span data-ttu-id="c4827-105">Status Befehl</span><span class="sxs-lookup"><span data-stu-id="c4827-105">status command</span></span>

> [!NOTE]
> <span data-ttu-id="c4827-106">Bias-freie Kommunikation Microsoft unterstützt eine unterschiedlichste und inklusive Umgebung.</span><span class="sxs-lookup"><span data-stu-id="c4827-106">Bias-free Communication Microsoft supports a diverse and inclusionary environment.</span></span>  <span data-ttu-id="c4827-107">In diesem Dokument sind Verweise auf das Wort "Slave" vorhanden.</span><span class="sxs-lookup"><span data-stu-id="c4827-107">Within this document, there are references to the word 'slave.'</span></span> <span data-ttu-id="c4827-108">Im [Stil Handbuch von Microsoft für die Bias-Free-Kommunikation](https://github.com/MicrosoftDocs/microsoft-style-guide/blob/master/styleguide/bias-free-communication.md) wird dies als ausschließendes Wort erkannt.</span><span class="sxs-lookup"><span data-stu-id="c4827-108">Microsoft's [Style Guide for Bias-Free Communications](https://github.com/MicrosoftDocs/microsoft-style-guide/blob/master/styleguide/bias-free-communication.md) recognizes this as an exclusionary word.</span></span>  <span data-ttu-id="c4827-109">Dieser Wortlaut wird verwendet, da es sich zurzeit um den in den Befehlen verwendeten Wortlaut handelt.</span><span class="sxs-lookup"><span data-stu-id="c4827-109">This wording is used as it is currently the wording used within the commands.</span></span> <span data-ttu-id="c4827-110">Aus Konsistenz Gründen enthält dieses Dokument dieses Wort.</span><span class="sxs-lookup"><span data-stu-id="c4827-110">For consistency, this document contains this word.</span></span> <span data-ttu-id="c4827-111">Wenn dieses Wort in den Befehlen geändert wird, korrigieren wir dieses Dokument als Ausrichtung.</span><span class="sxs-lookup"><span data-stu-id="c4827-111">When this word is altered in the commands, we will correct this document to be in alignment.</span></span>

<span data-ttu-id="c4827-112">Mit dem Status Befehl werden Statusinformationen von einem Gerät angefordert.</span><span class="sxs-lookup"><span data-stu-id="c4827-112">The status command requests status information from a device.</span></span> <span data-ttu-id="c4827-113">Alle Geräte erkennen diesen Befehl.</span><span class="sxs-lookup"><span data-stu-id="c4827-113">All devices recognize this command.</span></span>

<span data-ttu-id="c4827-114">Um diesen Befehl zu senden, wenden Sie die [**mciSendString**](/previous-versions//dd757161(v=vs.85)) -Funktion mit dem festgelegten *lpszcommand* -Parameter wie folgt an.</span><span class="sxs-lookup"><span data-stu-id="c4827-114">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand,
  TEXT("status %s %s %s"),
  lpszDeviceID,
  lpszRequest,
  lpszFlags
);
      
```

## <a name="parameters"></a><span data-ttu-id="c4827-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="c4827-115">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c4827-116"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszde viceid*</span><span class="sxs-lookup"><span data-stu-id="c4827-116"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="c4827-117">Der Bezeichner eines MCI-Geräts.</span><span class="sxs-lookup"><span data-stu-id="c4827-117">Identifier of an MCI device.</span></span> <span data-ttu-id="c4827-118">Dieser Bezeichner oder Alias wird zugewiesen, wenn das Gerät geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="c4827-118">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="c4827-119"><span id="lpszRequest"></span><span id="lpszrequest"></span><span id="LPSZREQUEST"></span>*lpszrequest*</span><span class="sxs-lookup"><span data-stu-id="c4827-119"><span id="lpszRequest"></span><span id="lpszrequest"></span><span id="LPSZREQUEST"></span>*lpszRequest*</span></span>
</dt> <dd>

<span data-ttu-id="c4827-120">Flag zum Anfordern von Statusinformationen.</span><span class="sxs-lookup"><span data-stu-id="c4827-120">Flag for requesting status information.</span></span> <span data-ttu-id="c4827-121">In der folgenden Tabelle werden die Gerätetypen aufgelistet, die den **Status** Befehl und die von den einzelnen Typen verwendeten Flags erkennen.</span><span class="sxs-lookup"><span data-stu-id="c4827-121">The following table lists device types that recognize the **status** command and the flags used by each type.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c4827-122">Gerätetyp</span><span class="sxs-lookup"><span data-stu-id="c4827-122">Device Type</span></span></th>
<th><span data-ttu-id="c4827-123">Anforderungs Flags</span><span class="sxs-lookup"><span data-stu-id="c4827-123">Request Flags</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c4827-124">CDAudio</span><span class="sxs-lookup"><span data-stu-id="c4827-124">cdaudio</span></span></td>
<td><ul>
<li><span data-ttu-id="c4827-125">CDAudio-typspur <em>Nummer</em></span><span class="sxs-lookup"><span data-stu-id="c4827-125">cdaudio type track <em>number</em></span></span></li>
<li><span data-ttu-id="c4827-126">aktuelle Spur</span><span class="sxs-lookup"><span data-stu-id="c4827-126">current track</span></span></li>
<li><span data-ttu-id="c4827-127">length</span><span class="sxs-lookup"><span data-stu-id="c4827-127">length</span></span></li>
<li><span data-ttu-id="c4827-128">Länge der <em>Nachverfolgung</em></span><span class="sxs-lookup"><span data-stu-id="c4827-128">length track <em>number</em></span></span></li>
<li><span data-ttu-id="c4827-129">Medien vorhanden</span><span class="sxs-lookup"><span data-stu-id="c4827-129">media present</span></span></li>
<li><span data-ttu-id="c4827-130">Modus</span><span class="sxs-lookup"><span data-stu-id="c4827-130">mode</span></span></li>
<li><span data-ttu-id="c4827-131">Anzahl der Spuren</span><span class="sxs-lookup"><span data-stu-id="c4827-131">number of tracks</span></span></li>
<li><span data-ttu-id="c4827-132">position</span><span class="sxs-lookup"><span data-stu-id="c4827-132">position</span></span></li>
<li><span data-ttu-id="c4827-133">Positions <em>Nummer</em></span><span class="sxs-lookup"><span data-stu-id="c4827-133">position track <em>number</em></span></span></li>
<li><span data-ttu-id="c4827-134">ready</span><span class="sxs-lookup"><span data-stu-id="c4827-134">ready</span></span></li>
<li><span data-ttu-id="c4827-135">Startposition</span><span class="sxs-lookup"><span data-stu-id="c4827-135">start position</span></span></li>
<li><span data-ttu-id="c4827-136">Zeitformat</span><span class="sxs-lookup"><span data-stu-id="c4827-136">time format</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c4827-137">Digitalvideo</span><span class="sxs-lookup"><span data-stu-id="c4827-137">digitalvideo</span></span></td>
<td><ul>
<li><span data-ttu-id="c4827-138">Audio</span><span class="sxs-lookup"><span data-stu-id="c4827-138">audio</span></span></li>
<li><span data-ttu-id="c4827-139">Audioausrichtung</span><span class="sxs-lookup"><span data-stu-id="c4827-139">audio alignment</span></span></li>
<li><span data-ttu-id="c4827-140">AudioBitsPerSample</span><span class="sxs-lookup"><span data-stu-id="c4827-140">audio bitspersample</span></span></li>
<li><span data-ttu-id="c4827-141">audioumbrüche</span><span class="sxs-lookup"><span data-stu-id="c4827-141">audio breaks</span></span></li>
<li><span data-ttu-id="c4827-142">audiobytespersec</span><span class="sxs-lookup"><span data-stu-id="c4827-142">audio bytespersec</span></span></li>
<li><span data-ttu-id="c4827-143">Audioeingabe</span><span class="sxs-lookup"><span data-stu-id="c4827-143">audio input</span></span></li>
<li><span data-ttu-id="c4827-144">audiodatensatz</span><span class="sxs-lookup"><span data-stu-id="c4827-144">audio record</span></span></li>
<li><span data-ttu-id="c4827-145">Audioquelle</span><span class="sxs-lookup"><span data-stu-id="c4827-145">audio source</span></span></li>
<li><span data-ttu-id="c4827-146">Audiodatei (samplespersec)</span><span class="sxs-lookup"><span data-stu-id="c4827-146">audio samplespersec</span></span></li>
<li><span data-ttu-id="c4827-147">Audiodatenstrom</span><span class="sxs-lookup"><span data-stu-id="c4827-147">audio stream</span></span></li>
<li><span data-ttu-id="c4827-148">Barsch</span><span class="sxs-lookup"><span data-stu-id="c4827-148">bass</span></span></li>
<li><span data-ttu-id="c4827-149">BitsPerPel</span><span class="sxs-lookup"><span data-stu-id="c4827-149">bitsperpel</span></span></li>
<li><span data-ttu-id="c4827-150">Helligkeit</span><span class="sxs-lookup"><span data-stu-id="c4827-150">brightness</span></span></li>
<li><span data-ttu-id="c4827-151">color</span><span class="sxs-lookup"><span data-stu-id="c4827-151">color</span></span></li>
<li><span data-ttu-id="c4827-152">Kontrast</span><span class="sxs-lookup"><span data-stu-id="c4827-152">contrast</span></span></li>
<li><span data-ttu-id="c4827-153">aktuelle Spur</span><span class="sxs-lookup"><span data-stu-id="c4827-153">current track</span></span></li>
<li><span data-ttu-id="c4827-154"><em>Festplatten Speicherplatz</em></span><span class="sxs-lookup"><span data-stu-id="c4827-154">disk space <em>drive</em></span></span></li>
<li><span data-ttu-id="c4827-155">Datei Abschluss</span><span class="sxs-lookup"><span data-stu-id="c4827-155">file completion</span></span></li>
<li><span data-ttu-id="c4827-156">Dateiformat</span><span class="sxs-lookup"><span data-stu-id="c4827-156">file format</span></span></li>
<li><span data-ttu-id="c4827-157">Dateimodus</span><span class="sxs-lookup"><span data-stu-id="c4827-157">file mode</span></span></li>
<li><span data-ttu-id="c4827-158">forward</span><span class="sxs-lookup"><span data-stu-id="c4827-158">forward</span></span></li>
<li><span data-ttu-id="c4827-159">Übersprungene Frames</span><span class="sxs-lookup"><span data-stu-id="c4827-159">frames skipped</span></span></li>
<li><span data-ttu-id="c4827-160">Gamma</span><span class="sxs-lookup"><span data-stu-id="c4827-160">gamma</span></span></li>
<li><span data-ttu-id="c4827-161">input</span><span class="sxs-lookup"><span data-stu-id="c4827-161">input</span></span></li>
<li><span data-ttu-id="c4827-162">Linkes Volume</span><span class="sxs-lookup"><span data-stu-id="c4827-162">left volume</span></span></li>
<li><span data-ttu-id="c4827-163">length</span><span class="sxs-lookup"><span data-stu-id="c4827-163">length</span></span></li>
<li><span data-ttu-id="c4827-164">Länge der <em>Nachverfolgung</em></span><span class="sxs-lookup"><span data-stu-id="c4827-164">length track <em>number</em></span></span></li>
<li><span data-ttu-id="c4827-165">Medien vorhanden</span><span class="sxs-lookup"><span data-stu-id="c4827-165">media present</span></span></li>
<li><span data-ttu-id="c4827-166">Modus</span><span class="sxs-lookup"><span data-stu-id="c4827-166">mode</span></span></li>
<li><span data-ttu-id="c4827-167">Überwachen</span><span class="sxs-lookup"><span data-stu-id="c4827-167">monitor</span></span></li>
<li><span data-ttu-id="c4827-168">Monitor-Methode</span><span class="sxs-lookup"><span data-stu-id="c4827-168">monitor method</span></span></li>
<li><span data-ttu-id="c4827-169">ell</span><span class="sxs-lookup"><span data-stu-id="c4827-169">nominal</span></span></li>
<li><span data-ttu-id="c4827-170">Nominale Bildrate</span><span class="sxs-lookup"><span data-stu-id="c4827-170">nominal frame rate</span></span></li>
<li><span data-ttu-id="c4827-171">Nominale Daten Satz Rahmenrate</span><span class="sxs-lookup"><span data-stu-id="c4827-171">nominal record frame rate</span></span></li>
<li><span data-ttu-id="c4827-172">Anzahl der Spuren</span><span class="sxs-lookup"><span data-stu-id="c4827-172">number of tracks</span></span></li>
<li><span data-ttu-id="c4827-173">output</span><span class="sxs-lookup"><span data-stu-id="c4827-173">output</span></span></li>
<li><span data-ttu-id="c4827-174">Palettenhandle</span><span class="sxs-lookup"><span data-stu-id="c4827-174">palette handle</span></span></li>
<li><span data-ttu-id="c4827-175">Pausenmodus</span><span class="sxs-lookup"><span data-stu-id="c4827-175">pause mode</span></span></li>
<li><span data-ttu-id="c4827-176">Wiedergabegeschwindigkeit</span><span class="sxs-lookup"><span data-stu-id="c4827-176">play speed</span></span></li>
<li><span data-ttu-id="c4827-177">position</span><span class="sxs-lookup"><span data-stu-id="c4827-177">position</span></span></li>
<li><span data-ttu-id="c4827-178">Positions <em>Nummer</em></span><span class="sxs-lookup"><span data-stu-id="c4827-178">position track <em>number</em></span></span></li>
<li><span data-ttu-id="c4827-179">ready</span><span class="sxs-lookup"><span data-stu-id="c4827-179">ready</span></span></li>
<li><span data-ttu-id="c4827-180">Frame Frequenz aufzeichnen</span><span class="sxs-lookup"><span data-stu-id="c4827-180">record frame rate</span></span></li>
<li><span data-ttu-id="c4827-181">Verweis <em>Rahmen</em></span><span class="sxs-lookup"><span data-stu-id="c4827-181">reference <em>frame</em></span></span></li>
<li><span data-ttu-id="c4827-182">reservierte Größe</span><span class="sxs-lookup"><span data-stu-id="c4827-182">reserved size</span></span></li>
<li><span data-ttu-id="c4827-183">richtiges Volume</span><span class="sxs-lookup"><span data-stu-id="c4827-183">right volume</span></span></li>
<li><span data-ttu-id="c4827-184">genau suchen</span><span class="sxs-lookup"><span data-stu-id="c4827-184">seek exactly</span></span></li>
<li><span data-ttu-id="c4827-185">Schärfe</span><span class="sxs-lookup"><span data-stu-id="c4827-185">sharpness</span></span></li>
<li><span data-ttu-id="c4827-186">SMPTE</span><span class="sxs-lookup"><span data-stu-id="c4827-186">smpte</span></span></li>
<li><span data-ttu-id="c4827-187">Geschwindigkeit</span><span class="sxs-lookup"><span data-stu-id="c4827-187">speed</span></span></li>
<li><span data-ttu-id="c4827-188">Startposition</span><span class="sxs-lookup"><span data-stu-id="c4827-188">start position</span></span></li>
<li><span data-ttu-id="c4827-189">immer noch Dateiformat</span><span class="sxs-lookup"><span data-stu-id="c4827-189">still file format</span></span></li>
<li><span data-ttu-id="c4827-190">Zeitformat</span><span class="sxs-lookup"><span data-stu-id="c4827-190">time format</span></span></li>
<li><span data-ttu-id="c4827-191">Tönungs</span><span class="sxs-lookup"><span data-stu-id="c4827-191">tint</span></span></li>
<li><span data-ttu-id="c4827-192">Höhen</span><span class="sxs-lookup"><span data-stu-id="c4827-192">treble</span></span></li>
<li><span data-ttu-id="c4827-193">nicht gespeicherte</span><span class="sxs-lookup"><span data-stu-id="c4827-193">unsaved</span></span></li>
<li><span data-ttu-id="c4827-194">video</span><span class="sxs-lookup"><span data-stu-id="c4827-194">video</span></span></li>
<li><span data-ttu-id="c4827-195">Video Schlüssel Index</span><span class="sxs-lookup"><span data-stu-id="c4827-195">video key index</span></span></li>
<li><span data-ttu-id="c4827-196">Farbe des Video Schlüssels</span><span class="sxs-lookup"><span data-stu-id="c4827-196">video key color</span></span></li>
<li><span data-ttu-id="c4827-197">Videodaten Satz</span><span class="sxs-lookup"><span data-stu-id="c4827-197">video record</span></span></li>
<li><span data-ttu-id="c4827-198">Videoquelle</span><span class="sxs-lookup"><span data-stu-id="c4827-198">video source</span></span></li>
<li><span data-ttu-id="c4827-199">Video Quellnummer</span><span class="sxs-lookup"><span data-stu-id="c4827-199">video source number</span></span></li>
<li><span data-ttu-id="c4827-200">Videostream</span><span class="sxs-lookup"><span data-stu-id="c4827-200">video stream</span></span></li>
<li><span data-ttu-id="c4827-201">Volume</span><span class="sxs-lookup"><span data-stu-id="c4827-201">volume</span></span></li>
<li><span data-ttu-id="c4827-202">Fenster handle</span><span class="sxs-lookup"><span data-stu-id="c4827-202">window handle</span></span></li>
<li><span data-ttu-id="c4827-203">Fenster sichtbar</span><span class="sxs-lookup"><span data-stu-id="c4827-203">window visible</span></span></li>
<li><span data-ttu-id="c4827-204">Fenster minimiert</span><span class="sxs-lookup"><span data-stu-id="c4827-204">window minimized</span></span></li>
<li><span data-ttu-id="c4827-205">Fenster maximiert</span><span class="sxs-lookup"><span data-stu-id="c4827-205">window maximized</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c4827-206">overlay</span><span class="sxs-lookup"><span data-stu-id="c4827-206">overlay</span></span></td>
<td><ul>
<li><span data-ttu-id="c4827-207">Medien vorhanden</span><span class="sxs-lookup"><span data-stu-id="c4827-207">media present</span></span></li>
<li><span data-ttu-id="c4827-208">Modus</span><span class="sxs-lookup"><span data-stu-id="c4827-208">mode</span></span></li>
<li><span data-ttu-id="c4827-209">Anzahl der Spuren</span><span class="sxs-lookup"><span data-stu-id="c4827-209">number of tracks</span></span></li>
<li><span data-ttu-id="c4827-210">ready</span><span class="sxs-lookup"><span data-stu-id="c4827-210">ready</span></span></li>
<li><span data-ttu-id="c4827-211">strecken</span><span class="sxs-lookup"><span data-stu-id="c4827-211">stretch</span></span></li>
<li><span data-ttu-id="c4827-212">Fenster handle</span><span class="sxs-lookup"><span data-stu-id="c4827-212">window handle</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c4827-213">sequencer</span><span class="sxs-lookup"><span data-stu-id="c4827-213">sequencer</span></span></td>
<td><ul>
<li><span data-ttu-id="c4827-214">aktuelle Spur</span><span class="sxs-lookup"><span data-stu-id="c4827-214">current track</span></span></li>
<li><span data-ttu-id="c4827-215">Divisions Typ</span><span class="sxs-lookup"><span data-stu-id="c4827-215">division type</span></span></li>
<li><span data-ttu-id="c4827-216">length</span><span class="sxs-lookup"><span data-stu-id="c4827-216">length</span></span></li>
<li><span data-ttu-id="c4827-217">Längen Spur- <em>Zahlen</em> Master</span><span class="sxs-lookup"><span data-stu-id="c4827-217">length track <em>number</em> master</span></span></li>
<li><span data-ttu-id="c4827-218">Medien vorhanden</span><span class="sxs-lookup"><span data-stu-id="c4827-218">media present</span></span></li>
<li><span data-ttu-id="c4827-219">Modus</span><span class="sxs-lookup"><span data-stu-id="c4827-219">mode</span></span></li>
<li><span data-ttu-id="c4827-220">Anzahl der Spuren</span><span class="sxs-lookup"><span data-stu-id="c4827-220">number of tracks</span></span></li>
<li><span data-ttu-id="c4827-221">offset</span><span class="sxs-lookup"><span data-stu-id="c4827-221">offset</span></span></li>
<li><span data-ttu-id="c4827-222">port</span><span class="sxs-lookup"><span data-stu-id="c4827-222">port</span></span></li>
<li><span data-ttu-id="c4827-223">position</span><span class="sxs-lookup"><span data-stu-id="c4827-223">position</span></span></li>
<li><span data-ttu-id="c4827-224">Positions <em>Nummer</em></span><span class="sxs-lookup"><span data-stu-id="c4827-224">position track <em>number</em></span></span></li>
<li><span data-ttu-id="c4827-225">ready</span><span class="sxs-lookup"><span data-stu-id="c4827-225">ready</span></span></li>
<li><span data-ttu-id="c4827-226">Sklaverei</span><span class="sxs-lookup"><span data-stu-id="c4827-226">slave</span></span></li>
<li><span data-ttu-id="c4827-227">Startposition</span><span class="sxs-lookup"><span data-stu-id="c4827-227">start position</span></span></li>
<li><span data-ttu-id="c4827-228">Lern</span><span class="sxs-lookup"><span data-stu-id="c4827-228">tempo</span></span></li>
<li><span data-ttu-id="c4827-229">Zeitformat</span><span class="sxs-lookup"><span data-stu-id="c4827-229">time format</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c4827-230">VCR</span><span class="sxs-lookup"><span data-stu-id="c4827-230">vcr</span></span></td>
<td><ul>
<li><span data-ttu-id="c4827-231">Datensatz Assemblieren</span><span class="sxs-lookup"><span data-stu-id="c4827-231">assemble record</span></span></li>
<li><span data-ttu-id="c4827-232">audiomonitor</span><span class="sxs-lookup"><span data-stu-id="c4827-232">audio monitor</span></span></li>
<li><span data-ttu-id="c4827-233">audiomonitornummer</span><span class="sxs-lookup"><span data-stu-id="c4827-233">audio monitor number</span></span></li>
<li><span data-ttu-id="c4827-234">audiodatensatz</span><span class="sxs-lookup"><span data-stu-id="c4827-234">audio record</span></span></li>
<li><span data-ttu-id="c4827-235"><em>Anzahl</em> der Audiodaten Satz-Spuren</span><span class="sxs-lookup"><span data-stu-id="c4827-235">audio record track <em>number</em></span></span></li>
<li><span data-ttu-id="c4827-236">Audioquelle</span><span class="sxs-lookup"><span data-stu-id="c4827-236">audio source</span></span></li>
<li><span data-ttu-id="c4827-237">audioquellnummer</span><span class="sxs-lookup"><span data-stu-id="c4827-237">audio source number</span></span></li>
<li><span data-ttu-id="c4827-238">Kanal</span><span class="sxs-lookup"><span data-stu-id="c4827-238">channel</span></span></li>
<li><span data-ttu-id="c4827-239">Kanal-Tuner- <em>Nummer</em></span><span class="sxs-lookup"><span data-stu-id="c4827-239">channel tuner <em>number</em></span></span></li>
<li><span data-ttu-id="c4827-240">clock</span><span class="sxs-lookup"><span data-stu-id="c4827-240">clock</span></span></li>
<li><span data-ttu-id="c4827-241">Takt-ID</span><span class="sxs-lookup"><span data-stu-id="c4827-241">clock id</span></span></li>
<li><span data-ttu-id="c4827-242">Zähler</span><span class="sxs-lookup"><span data-stu-id="c4827-242">counter</span></span></li>
<li><span data-ttu-id="c4827-243">Counter-Format</span><span class="sxs-lookup"><span data-stu-id="c4827-243">counter format</span></span></li>
<li><span data-ttu-id="c4827-244">Auflösung von Zählern</span><span class="sxs-lookup"><span data-stu-id="c4827-244">counter resolution</span></span></li>
<li><span data-ttu-id="c4827-245">aktuelle Spur</span><span class="sxs-lookup"><span data-stu-id="c4827-245">current track</span></span></li>
<li><span data-ttu-id="c4827-246">Framerate</span><span class="sxs-lookup"><span data-stu-id="c4827-246">frame rate</span></span></li>
<li><span data-ttu-id="c4827-247">Index</span><span class="sxs-lookup"><span data-stu-id="c4827-247">index</span></span></li>
<li><span data-ttu-id="c4827-248">Index für</span><span class="sxs-lookup"><span data-stu-id="c4827-248">index on</span></span></li>
<li><span data-ttu-id="c4827-249">length</span><span class="sxs-lookup"><span data-stu-id="c4827-249">length</span></span></li>
<li><span data-ttu-id="c4827-250">Länge der <em>Nachverfolgung</em></span><span class="sxs-lookup"><span data-stu-id="c4827-250">length track <em>number</em></span></span></li>
<li><span data-ttu-id="c4827-251">Medien vorhanden</span><span class="sxs-lookup"><span data-stu-id="c4827-251">media present</span></span></li>
<li><span data-ttu-id="c4827-252">Medientyp</span><span class="sxs-lookup"><span data-stu-id="c4827-252">media type</span></span></li>
<li><span data-ttu-id="c4827-253">Modus</span><span class="sxs-lookup"><span data-stu-id="c4827-253">mode</span></span></li>
<li><span data-ttu-id="c4827-254">Anzahl von Audiospuren</span><span class="sxs-lookup"><span data-stu-id="c4827-254">number of audio tracks</span></span></li>
<li><span data-ttu-id="c4827-255">Anzahl der Spuren</span><span class="sxs-lookup"><span data-stu-id="c4827-255">number of tracks</span></span></li>
<li><span data-ttu-id="c4827-256">Anzahl der Videospuren</span><span class="sxs-lookup"><span data-stu-id="c4827-256">number of video tracks</span></span></li>
<li><span data-ttu-id="c4827-257"><em>Timeout</em> für Pause</span><span class="sxs-lookup"><span data-stu-id="c4827-257">pause <em>timeout</em></span></span></li>
<li><span data-ttu-id="c4827-258">Wiedergabe Format</span><span class="sxs-lookup"><span data-stu-id="c4827-258">play format</span></span></li>
<li><span data-ttu-id="c4827-259">position</span><span class="sxs-lookup"><span data-stu-id="c4827-259">position</span></span></li>
<li><span data-ttu-id="c4827-260">Positions Anfang</span><span class="sxs-lookup"><span data-stu-id="c4827-260">position start</span></span></li>
<li><span data-ttu-id="c4827-261">Positions <em>Nummer</em></span><span class="sxs-lookup"><span data-stu-id="c4827-261">position track <em>number</em></span></span></li>
<li><span data-ttu-id="c4827-262">Postroll <em>Dauer</em></span><span class="sxs-lookup"><span data-stu-id="c4827-262">postroll <em>duration</em></span></span></li>
<li><span data-ttu-id="c4827-263">Einschalten</span><span class="sxs-lookup"><span data-stu-id="c4827-263">power on</span></span></li>
<li><span data-ttu-id="c4827-264">Vorabversion <em></em></span><span class="sxs-lookup"><span data-stu-id="c4827-264">preroll <em>duration</em></span></span></li>
<li><span data-ttu-id="c4827-265">ready</span><span class="sxs-lookup"><span data-stu-id="c4827-265">ready</span></span></li>
<li><span data-ttu-id="c4827-266">Daten Satz Format</span><span class="sxs-lookup"><span data-stu-id="c4827-266">record format</span></span></li>
<li><span data-ttu-id="c4827-267">Geschwindigkeit</span><span class="sxs-lookup"><span data-stu-id="c4827-267">speed</span></span></li>
<li><span data-ttu-id="c4827-268">Zeitformat</span><span class="sxs-lookup"><span data-stu-id="c4827-268">time format</span></span></li>
<li><span data-ttu-id="c4827-269">Zeit Modus</span><span class="sxs-lookup"><span data-stu-id="c4827-269">time mode</span></span></li>
<li><span data-ttu-id="c4827-270">Uhrzeittyp</span><span class="sxs-lookup"><span data-stu-id="c4827-270">time type</span></span></li>
<li><span data-ttu-id="c4827-271">Zeit Code vorhanden</span><span class="sxs-lookup"><span data-stu-id="c4827-271">timecode present</span></span></li>
<li><span data-ttu-id="c4827-272">Zeitcode-Datensatz</span><span class="sxs-lookup"><span data-stu-id="c4827-272">timecode record</span></span></li>
<li><span data-ttu-id="c4827-273">timecodetyp</span><span class="sxs-lookup"><span data-stu-id="c4827-273">timecode type</span></span></li>
<li><span data-ttu-id="c4827-274">Nummer des Tuners</span><span class="sxs-lookup"><span data-stu-id="c4827-274">tuner number</span></span></li>
<li><span data-ttu-id="c4827-275">Videomonitor</span><span class="sxs-lookup"><span data-stu-id="c4827-275">video monitor</span></span></li>
<li><span data-ttu-id="c4827-276">Videomonitor Nummer</span><span class="sxs-lookup"><span data-stu-id="c4827-276">video monitor number</span></span></li>
<li><span data-ttu-id="c4827-277">Videodaten Satz</span><span class="sxs-lookup"><span data-stu-id="c4827-277">video record</span></span></li>
<li><span data-ttu-id="c4827-278"><em>Nummer</em> der Videodaten Satz Verfolgung</span><span class="sxs-lookup"><span data-stu-id="c4827-278">video record track <em>number</em></span></span></li>
<li><span data-ttu-id="c4827-279">Videoquelle</span><span class="sxs-lookup"><span data-stu-id="c4827-279">video source</span></span></li>
<li><span data-ttu-id="c4827-280">Video Quellnummer</span><span class="sxs-lookup"><span data-stu-id="c4827-280">video source number</span></span></li>
<li><span data-ttu-id="c4827-281">schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c4827-281">write protected</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c4827-282">Videodisk</span><span class="sxs-lookup"><span data-stu-id="c4827-282">videodisc</span></span></td>
<td><ul>
<li><span data-ttu-id="c4827-283">aktuelle Spur</span><span class="sxs-lookup"><span data-stu-id="c4827-283">current track</span></span></li>
<li><span data-ttu-id="c4827-284">Größe der Festplatte</span><span class="sxs-lookup"><span data-stu-id="c4827-284">disc size</span></span></li>
<li><span data-ttu-id="c4827-285">forward</span><span class="sxs-lookup"><span data-stu-id="c4827-285">forward</span></span></li>
<li><span data-ttu-id="c4827-286">length</span><span class="sxs-lookup"><span data-stu-id="c4827-286">length</span></span></li>
<li><span data-ttu-id="c4827-287">Länge der <em>Nachverfolgung</em></span><span class="sxs-lookup"><span data-stu-id="c4827-287">length track <em>number</em></span></span></li>
<li><span data-ttu-id="c4827-288">Medien vorhanden</span><span class="sxs-lookup"><span data-stu-id="c4827-288">media present</span></span></li>
<li><span data-ttu-id="c4827-289">Medientyp</span><span class="sxs-lookup"><span data-stu-id="c4827-289">media type</span></span></li>
<li><span data-ttu-id="c4827-290">Modus</span><span class="sxs-lookup"><span data-stu-id="c4827-290">mode</span></span></li>
<li><span data-ttu-id="c4827-291">Anzahl der Spuren</span><span class="sxs-lookup"><span data-stu-id="c4827-291">number of tracks</span></span></li>
<li><span data-ttu-id="c4827-292">position</span><span class="sxs-lookup"><span data-stu-id="c4827-292">position</span></span></li>
<li><span data-ttu-id="c4827-293">Positions <em>Nummer</em></span><span class="sxs-lookup"><span data-stu-id="c4827-293">position track <em>number</em></span></span></li>
<li><span data-ttu-id="c4827-294">ready</span><span class="sxs-lookup"><span data-stu-id="c4827-294">ready</span></span></li>
<li><span data-ttu-id="c4827-295">Seite</span><span class="sxs-lookup"><span data-stu-id="c4827-295">side</span></span></li>
<li><span data-ttu-id="c4827-296">Geschwindigkeit</span><span class="sxs-lookup"><span data-stu-id="c4827-296">speed</span></span></li>
<li><span data-ttu-id="c4827-297">Startposition</span><span class="sxs-lookup"><span data-stu-id="c4827-297">start position</span></span></li>
<li><span data-ttu-id="c4827-298">Zeitformat</span><span class="sxs-lookup"><span data-stu-id="c4827-298">time format</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c4827-299">waveaudiodatei</span><span class="sxs-lookup"><span data-stu-id="c4827-299">waveaudio</span></span></td>
<td><ul>
<li><span data-ttu-id="c4827-300">Ausrichtung</span><span class="sxs-lookup"><span data-stu-id="c4827-300">alignment</span></span></li>
<li><span data-ttu-id="c4827-301">BitsPerSample</span><span class="sxs-lookup"><span data-stu-id="c4827-301">bitspersample</span></span></li>
<li><span data-ttu-id="c4827-302">bytespersec</span><span class="sxs-lookup"><span data-stu-id="c4827-302">bytespersec</span></span></li>
<li><span data-ttu-id="c4827-303">channels</span><span class="sxs-lookup"><span data-stu-id="c4827-303">channels</span></span></li>
<li><span data-ttu-id="c4827-304">aktuelle Spur</span><span class="sxs-lookup"><span data-stu-id="c4827-304">current track</span></span></li>
<li><span data-ttu-id="c4827-305">Tag formatieren</span><span class="sxs-lookup"><span data-stu-id="c4827-305">format tag</span></span></li>
<li><span data-ttu-id="c4827-306">input</span><span class="sxs-lookup"><span data-stu-id="c4827-306">input</span></span></li>
<li><span data-ttu-id="c4827-307">length</span><span class="sxs-lookup"><span data-stu-id="c4827-307">length</span></span></li>
<li><span data-ttu-id="c4827-308">Länge der <em>Nachverfolgung</em></span><span class="sxs-lookup"><span data-stu-id="c4827-308">length track <em>number</em></span></span></li>
<li><span data-ttu-id="c4827-309">Level</span><span class="sxs-lookup"><span data-stu-id="c4827-309">level</span></span></li>
<li><span data-ttu-id="c4827-310">Medien vorhanden</span><span class="sxs-lookup"><span data-stu-id="c4827-310">media present</span></span></li>
<li><span data-ttu-id="c4827-311">Modus</span><span class="sxs-lookup"><span data-stu-id="c4827-311">mode</span></span></li>
<li><span data-ttu-id="c4827-312">Anzahl der Spuren</span><span class="sxs-lookup"><span data-stu-id="c4827-312">number of tracks</span></span></li>
<li><span data-ttu-id="c4827-313">output</span><span class="sxs-lookup"><span data-stu-id="c4827-313">output</span></span></li>
<li><span data-ttu-id="c4827-314">position</span><span class="sxs-lookup"><span data-stu-id="c4827-314">position</span></span></li>
<li><span data-ttu-id="c4827-315">Positions <em>Nummer</em></span><span class="sxs-lookup"><span data-stu-id="c4827-315">position track <em>number</em></span></span></li>
<li><span data-ttu-id="c4827-316">ready</span><span class="sxs-lookup"><span data-stu-id="c4827-316">ready</span></span></li>
<li><span data-ttu-id="c4827-317">samplespersec</span><span class="sxs-lookup"><span data-stu-id="c4827-317">samplespersec</span></span></li>
<li><span data-ttu-id="c4827-318">Startposition</span><span class="sxs-lookup"><span data-stu-id="c4827-318">start position</span></span></li>
<li><span data-ttu-id="c4827-319">Zeitformat</span><span class="sxs-lookup"><span data-stu-id="c4827-319">time format</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="c4827-320">In der folgenden Tabelle werden die Flags aufgelistet, die im **lpszrequest** -Parameter und deren Bedeutung angegeben werden können.</span><span class="sxs-lookup"><span data-stu-id="c4827-320">The following table lists the flags that can be specified in the **lpszRequest** parameter and their meanings.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c4827-321">Wert</span><span class="sxs-lookup"><span data-stu-id="c4827-321">Value</span></span></th>
<th><span data-ttu-id="c4827-322">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="c4827-322">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c4827-323">Ausrichtung</span><span class="sxs-lookup"><span data-stu-id="c4827-323">alignment</span></span></td>
<td><span data-ttu-id="c4827-324">Gibt die Block Ausrichtung der Daten in Bytes zurück.</span><span class="sxs-lookup"><span data-stu-id="c4827-324">Returns the block alignment of data, in bytes.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c4827-325">Datensatz Assemblieren</span><span class="sxs-lookup"><span data-stu-id="c4827-325">assemble record</span></span></td>
<td><span data-ttu-id="c4827-326">Gibt <strong>true</strong> zurück, wenn das Gerät auf assemblierungsmodusaufzeichnung festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="c4827-326">Returns <strong>TRUE</strong> if the device is set to assemble mode recording.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c4827-327">Audio</span><span class="sxs-lookup"><span data-stu-id="c4827-327">audio</span></span></td>
<td><span data-ttu-id="c4827-328">Gibt ein- &quot; &quot; oder &quot; ausschalten &quot; abhängig vom letzten Befehl " <a href="setaudio.md">setaudioon</a> &quot; " &quot; &quot; oder "Off" &quot; .</span><span class="sxs-lookup"><span data-stu-id="c4827-328">Returns &quot;on&quot; or &quot;off&quot; depending on the most recent <a href="setaudio.md">setaudio</a> &quot;on&quot; or &quot;off&quot; command.</span></span> <span data-ttu-id="c4827-329">Es wird ein zurückgegeben &quot; &quot; , wenn entweder oder beide Redner aktiviert sind, &quot; &quot; andernfalls.</span><span class="sxs-lookup"><span data-stu-id="c4827-329">It returns &quot;on&quot; if either or both speakers are enabled, and &quot;off&quot; otherwise.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c4827-330">Audioausrichtung</span><span class="sxs-lookup"><span data-stu-id="c4827-330">audio alignment</span></span></td>
<td><span data-ttu-id="c4827-331">Gibt die Ausrichtung von Datenblöcken relativ zum Anfang der Eingabe-Waveform-Audiodaten zurück.</span><span class="sxs-lookup"><span data-stu-id="c4827-331">Returns the alignment of data blocks relative to the start of input waveform-audio data.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c4827-332">AudioBitsPerSample</span><span class="sxs-lookup"><span data-stu-id="c4827-332">audio bitspersample</span></span></td>
<td><span data-ttu-id="c4827-333">Gibt die Anzahl der Bits pro Stichprobe zurück, die vom Gerät für die Aufzeichnung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c4827-333">Returns the number of bits per sample the device uses for recording.</span></span> <span data-ttu-id="c4827-334">Dieses Flag gilt nur für Geräte, die den PCM-Algorithmus unterstützen &quot; &quot; .</span><span class="sxs-lookup"><span data-stu-id="c4827-334">This flag applies only to devices supporting the &quot;pcm&quot; algorithm.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c4827-335">audioumbrüche</span><span class="sxs-lookup"><span data-stu-id="c4827-335">audio breaks</span></span></td>
<td><span data-ttu-id="c4827-336">Gibt die Häufigkeit zurück, mit der der Audioteil der letzten AVI-Sequenz abgebrochen wurde.</span><span class="sxs-lookup"><span data-stu-id="c4827-336">Returns the number of times the audio portion of the last AVI sequence broke up.</span></span> <span data-ttu-id="c4827-337">Das System zählt immer dann eine audiopause, wenn versucht wird, Audiodaten in den Gerätetreiber zu schreiben und feststellt, dass der Treiber bereits alle verfügbaren Daten wiedergegeben hat.</span><span class="sxs-lookup"><span data-stu-id="c4827-337">The system counts an audio break whenever it attempts to write audio data to the device driver and discovers that the driver has already played all of the available data.</span></span> <span data-ttu-id="c4827-338">Dieses Flag wird nur vom MCIAVI Digital-Video-Treiber erkannt.</span><span class="sxs-lookup"><span data-stu-id="c4827-338">This flag is recognized only by the MCIAVI digital-video driver.</span></span> <span data-ttu-id="c4827-339">Es ist nur für die Leistungs Auswertung gedacht. der Rückgabewert ist schwierig zu interpretieren.</span><span class="sxs-lookup"><span data-stu-id="c4827-339">It is meant for performance evaluation only; the return value is difficult to interpret.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c4827-340">audiobytespersec</span><span class="sxs-lookup"><span data-stu-id="c4827-340">audio bytespersec</span></span></td>
<td><span data-ttu-id="c4827-341">Gibt die durchschnittliche Anzahl der Bytes zurück, die pro Sekunde für die Aufzeichnung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c4827-341">Returns the average number of bytes per second used for recording.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c4827-342">Audioeingabe</span><span class="sxs-lookup"><span data-stu-id="c4827-342">audio input</span></span></td>
<td><span data-ttu-id="c4827-343">Gibt die ungefähre sofortige Audioebene des analogen eingabeaudiosignals zurück.</span><span class="sxs-lookup"><span data-stu-id="c4827-343">Returns the approximate instantaneous audio level of the analog input audio signal.</span></span> <span data-ttu-id="c4827-344">Ein Wert größer als 1000 impliziert clippingverzerrung.</span><span class="sxs-lookup"><span data-stu-id="c4827-344">A value greater than 1000 implies clipping distortion.</span></span> <span data-ttu-id="c4827-345">Einige Geräte können diesen Wert nur beim Aufzeichnen von Audiodaten zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="c4827-345">Some devices can return this value only while recording audio.</span></span> <span data-ttu-id="c4827-346">Dem Wert ist kein <a href="set.md">Set</a> -oder <a href="setaudio.md">setaudiobefehl</a> zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="c4827-346">The value has no associated <a href="set.md">set</a> or <a href="setaudio.md">setaudio</a> command.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c4827-347">audiomonitor</span><span class="sxs-lookup"><span data-stu-id="c4827-347">audio monitor</span></span></td>
<td><span data-ttu-id="c4827-348">Gibt &quot; &quot; die Ausgabe oder einen der gültigen Quell Eingabetypen zurück.</span><span class="sxs-lookup"><span data-stu-id="c4827-348">Returns &quot;output&quot;, or one of the valid source-input types.</span></span> <span data-ttu-id="c4827-349">Weitere Informationen finden Sie unter dem Befehl " <strong>setaudiomonitor</strong> " &quot; &quot; .</span><span class="sxs-lookup"><span data-stu-id="c4827-349">For more information, see the <strong>setaudio</strong> &quot;monitor&quot; command.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c4827-350">audiomonitornummer</span><span class="sxs-lookup"><span data-stu-id="c4827-350">audio monitor number</span></span></td>
<td><span data-ttu-id="c4827-351">Gibt die überwachte Video Nummer des Typs zurück, der vom <strong>Status</strong> &quot; -audiomonitor angegeben wird &quot; .</span><span class="sxs-lookup"><span data-stu-id="c4827-351">Returns the monitored-video number of the type specified by <strong>status</strong> &quot;audio monitor&quot;.</span></span> <span data-ttu-id="c4827-352">Weitere Informationen finden Sie unter dem Befehl <a href="setaudio.md">SetAudio.</a></span><span class="sxs-lookup"><span data-stu-id="c4827-352">For more information, see the <a href="setaudio.md">setaudio</a> command.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c4827-353">audiodatensatz</span><span class="sxs-lookup"><span data-stu-id="c4827-353">audio record</span></span></td>
<td><span data-ttu-id="c4827-354">Gibt &quot; ein &quot; oder &quot; aus zurück &quot; , das den durch <strong>setaudiodatensatz</strong> festgelegten Status widerspiegelt &quot; &quot; .</span><span class="sxs-lookup"><span data-stu-id="c4827-354">Returns &quot;on&quot; or &quot;off&quot;, reflecting the state set by <strong>setaudio</strong> &quot;record&quot;.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c4827-355"><em>Anzahl</em> der Audiodaten Satz-Spuren</span><span class="sxs-lookup"><span data-stu-id="c4827-355">audio record track <em>number</em></span></span></td>
<td><span data-ttu-id="c4827-356">Gibt " <strong>true</strong> " zurück, wenn der VCR zum Aufzeichnen von Audiodaten festgelegt ist</span><span class="sxs-lookup"><span data-stu-id="c4827-356">Returns <strong>TRUE</strong> if the VCR is set to record audio.</span></span> <span data-ttu-id="c4827-357">Wenn keine Nachverfolgung angegeben ist, wird der Standardwert 1 angenommen.</span><span class="sxs-lookup"><span data-stu-id="c4827-357">If no track number is given, the default value of 1 is assumed.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c4827-358">Audiodatei (samplespersec)</span><span class="sxs-lookup"><span data-stu-id="c4827-358">audio samplespersec</span></span></td>
<td><span data-ttu-id="c4827-359">Gibt die Anzahl der Stichproben pro Sekunde zurück, die aufgezeichnet wurden.</span><span class="sxs-lookup"><span data-stu-id="c4827-359">Returns the number of samples per second recorded.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c4827-360">Audioquelle</span><span class="sxs-lookup"><span data-stu-id="c4827-360">audio source</span></span></td>
<td><span data-ttu-id="c4827-361">Gibt die aktuelle audiodigitalisierungs Quelle zurück: &quot; left &quot; , &quot; right &quot; , &quot; Average &quot; oder &quot; Stereo &quot; .</span><span class="sxs-lookup"><span data-stu-id="c4827-361">Returns the current audio digitizer source: &quot;left&quot;, &quot;right&quot;, &quot;average&quot;, or &quot;stereo&quot;.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c4827-362">audioquellnummer</span><span class="sxs-lookup"><span data-stu-id="c4827-362">audio source number</span></span></td>
<td><span data-ttu-id="c4827-363">Gibt die audioquellnummer des Typs zurück, der von der <strong>statusaudioquelle</strong> zurückgegeben wird &quot; &quot; .</span><span class="sxs-lookup"><span data-stu-id="c4827-363">Returns the audio-source number of the type returned by <strong>status</strong> &quot;audio source&quot;.</span></span> <span data-ttu-id="c4827-364">Weitere Informationen finden Sie unter dem Befehl <a href="setaudio.md">SetAudio.</a></span><span class="sxs-lookup"><span data-stu-id="c4827-364">For more information, see the <a href="setaudio.md">setaudio</a> command.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c4827-365">Audiodatenstrom</span><span class="sxs-lookup"><span data-stu-id="c4827-365">audio stream</span></span></td>
<td><span data-ttu-id="c4827-366">Gibt die aktuelle audiostreamnummer zurück.</span><span class="sxs-lookup"><span data-stu-id="c4827-366">Returns the current audio-stream number.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c4827-367">Barsch</span><span class="sxs-lookup"><span data-stu-id="c4827-367">bass</span></span></td>
<td><span data-ttu-id="c4827-368">Gibt die aktuelle audiobass-Ebene zurück.</span><span class="sxs-lookup"><span data-stu-id="c4827-368">Returns the current audio-bass level.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c4827-369">BitsPerPel</span><span class="sxs-lookup"><span data-stu-id="c4827-369">bitsperpel</span></span></td>
<td><span data-ttu-id="c4827-370">Gibt die Anzahl von Bits pro Pixel zum Speichern erfasster oder aufgezeichneter Daten zurück.</span><span class="sxs-lookup"><span data-stu-id="c4827-370">Returns the number of bits per pixel for saving captured or recorded data.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c4827-371">BitsPerSample</span><span class="sxs-lookup"><span data-stu-id="c4827-371">bitspersample</span></span></td>
<td><span data-ttu-id="c4827-372">Gibt die Bits pro Stichprobe zurück.</span><span class="sxs-lookup"><span data-stu-id="c4827-372">Returns the bits per sample.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c4827-373">Helligkeit</span><span class="sxs-lookup"><span data-stu-id="c4827-373">brightness</span></span></td>
<td><span data-ttu-id="c4827-374">Gibt die aktuelle videohelligkeits Ebene zurück.</span><span class="sxs-lookup"><span data-stu-id="c4827-374">Returns the current video-brightness level.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c4827-375">bytespersec</span><span class="sxs-lookup"><span data-stu-id="c4827-375">bytespersec</span></span></td>
<td><span data-ttu-id="c4827-376">Gibt die durchschnittliche Anzahl von Bytes pro Sekunde wiedergegeben oder aufgezeichnet zurück.</span><span class="sxs-lookup"><span data-stu-id="c4827-376">Returns the average number of bytes per second played or recorded.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c4827-377">CDAudio-typspur <em>Nummer</em></span><span class="sxs-lookup"><span data-stu-id="c4827-377">cdaudio type track <em>number</em></span></span></td>
<td><span data-ttu-id="c4827-378">Gibt den Typ der angegebenen Nachverfolgung zurück.</span><span class="sxs-lookup"><span data-stu-id="c4827-378">Returns the type of the specified track number.</span></span> <span data-ttu-id="c4827-379">Hierbei kann es sich um &quot; Audiodaten &quot; oder &quot; andere handeln.&quot;</span><span class="sxs-lookup"><span data-stu-id="c4827-379">This can be &quot;audio&quot; or &quot;other.&quot;</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c4827-380">Kanal</span><span class="sxs-lookup"><span data-stu-id="c4827-380">channel</span></span></td>
<td><span data-ttu-id="c4827-381">Gibt den ganzzahligen Wert des Kanals zurück, der für den Tuner festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="c4827-381">Returns the integer value of the channel set on the tuner.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c4827-382">Kanal-Tuner- <em>Nummer</em></span><span class="sxs-lookup"><span data-stu-id="c4827-382">channel tuner <em>number</em></span></span></td>
<td><span data-ttu-id="c4827-383">Wenn eine &quot; Tuner- &quot; <em>Nummer</em> angegeben wird, wird der aktuell ausgewählte Kanal für die logische Tuner- <em>Nummer</em> zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="c4827-383">If &quot;tuner&quot; <em>number</em> is given, then the currently selected channel on the logical tuner <em>number</em> will be returned.</span></span> <span data-ttu-id="c4827-384">Beachten Sie, dass es mehrere logische Tuner geben kann.</span><span class="sxs-lookup"><span data-stu-id="c4827-384">Note that there can be several logical tuners.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c4827-385">channels</span><span class="sxs-lookup"><span data-stu-id="c4827-385">channels</span></span></td>
<td><span data-ttu-id="c4827-386">Gibt die Anzahl der festgelegten Kanäle zurück (1 für Mono, 2 für Stereo).</span><span class="sxs-lookup"><span data-stu-id="c4827-386">Returns the number of channels set (1 for mono, 2 for stereo).</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c4827-387">clock</span><span class="sxs-lookup"><span data-stu-id="c4827-387">clock</span></span></td>
<td><span data-ttu-id="c4827-388">Gibt die externe Zeit zurück.</span><span class="sxs-lookup"><span data-stu-id="c4827-388">Returns the external time.</span></span> <span data-ttu-id="c4827-389">Die Zeit muss eine lange ganze Zahl ohne Vorzeichen sein, die die Gesamt Inkremente ausdrückt.</span><span class="sxs-lookup"><span data-stu-id="c4827-389">The time must be an unsigned long integer expressing total increments.</span></span> <span data-ttu-id="c4827-390">Weitere Informationen finden Sie im Befehl <a href="capability.md">Capability</a> &quot; Clock Inkrement Rate &quot; .</span><span class="sxs-lookup"><span data-stu-id="c4827-390">For more information, see the <a href="capability.md">capability</a> &quot;clock increment rate&quot; command.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c4827-391">Takt-ID</span><span class="sxs-lookup"><span data-stu-id="c4827-391">clock id</span></span></td>
<td><span data-ttu-id="c4827-392">Gibt eine eindeutige Ganzzahl zurück, die die Uhr identifiziert.</span><span class="sxs-lookup"><span data-stu-id="c4827-392">Returns a unique integer identifying the clock.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c4827-393">color</span><span class="sxs-lookup"><span data-stu-id="c4827-393">color</span></span></td>
<td><span data-ttu-id="c4827-394">Gibt die aktuelle Farb Ebene zurück.</span><span class="sxs-lookup"><span data-stu-id="c4827-394">Returns the current color level.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c4827-395">Kontrast</span><span class="sxs-lookup"><span data-stu-id="c4827-395">contrast</span></span></td>
<td><span data-ttu-id="c4827-396">Gibt die aktuelle Kontrast Ebene zurück.</span><span class="sxs-lookup"><span data-stu-id="c4827-396">Returns the current contrast level.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c4827-397">Zähler</span><span class="sxs-lookup"><span data-stu-id="c4827-397">counter</span></span></td>
<td><span data-ttu-id="c4827-398">Gibt die Gegenposition im aktuellen Leistungs Zählers zurück.</span><span class="sxs-lookup"><span data-stu-id="c4827-398">Returns the counter position, in the current counter format.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c4827-399">Counter-Format</span><span class="sxs-lookup"><span data-stu-id="c4827-399">counter format</span></span></td>
<td><span data-ttu-id="c4827-400">Gibt das aktuelle Leistungs Zähl Format zurück.</span><span class="sxs-lookup"><span data-stu-id="c4827-400">Returns the current counter format.</span></span> <span data-ttu-id="c4827-401">Weitere Informationen finden Sie unter dem Befehl <a href="set.md">Set</a> &quot; Counter Format &quot; .</span><span class="sxs-lookup"><span data-stu-id="c4827-401">For more information, see the <a href="set.md">set</a> &quot;counter format&quot; command.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c4827-402">Auflösung von Zählern</span><span class="sxs-lookup"><span data-stu-id="c4827-402">counter resolution</span></span></td>
<td><span data-ttu-id="c4827-403">Gibt &quot; Frames &quot; oder &quot; Sekunden zurück &quot; , die die Auflösung des Zählers angeben.</span><span class="sxs-lookup"><span data-stu-id="c4827-403">Returns &quot;frames&quot; or &quot;seconds&quot;, indicating the counter's resolution.</span></span> <span data-ttu-id="c4827-404">Dies ist nicht mit der Genauigkeit identisch.</span><span class="sxs-lookup"><span data-stu-id="c4827-404">This is not the same as accuracy.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c4827-405">aktuelle Spur</span><span class="sxs-lookup"><span data-stu-id="c4827-405">current track</span></span></td>
<td><span data-ttu-id="c4827-406">Gibt den aktuellen Titel zurück. Der mcist-Sequencer gibt 1 zurück.</span><span class="sxs-lookup"><span data-stu-id="c4827-406">Returns the current track. The MCISEQ sequencer returns 1.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c4827-407">Größe der Festplatte</span><span class="sxs-lookup"><span data-stu-id="c4827-407">disc size</span></span></td>
<td><span data-ttu-id="c4827-408">Gibt entweder 8 oder 12 zurück, was die Größe der geladenen CD in Zoll angibt.</span><span class="sxs-lookup"><span data-stu-id="c4827-408">Returns either 8 or 12, indicating the size of the loaded disc in inches.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c4827-409"><em>Festplatten Speicherplatz</em></span><span class="sxs-lookup"><span data-stu-id="c4827-409">disk space <em>drive</em></span></span></td>
<td><span data-ttu-id="c4827-410">Gibt den ungefähren Speicherplatz im aktuellen Zeitformat zurück, der durch einen <a href="reserve.md">Reserve</a> Befehl für das angegebene Laufwerk abgerufen werden kann <em>.</em></span><span class="sxs-lookup"><span data-stu-id="c4827-410">Returns the approximate disk space, in the current time format, that can be obtained by a <a href="reserve.md">reserve</a> command for the specified disk <em>drive.</em></span></span> <span data-ttu-id="c4827-411">Das <em>Laufwerk</em> wird in der Regel als einzelner Buchstabe oder als einzelner Buchstabe angegeben, gefolgt von einem Doppelpunkt (:).</span><span class="sxs-lookup"><span data-stu-id="c4827-411">The <em>drive</em> is usually specified as a single letter or a single letter followed by a colon (:).</span></span> <span data-ttu-id="c4827-412">Einige Geräte verwenden jedoch möglicherweise einen Pfad.</span><span class="sxs-lookup"><span data-stu-id="c4827-412">Some devices, however, might use a path.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c4827-413">Divisions Typ</span><span class="sxs-lookup"><span data-stu-id="c4827-413">division type</span></span></td>
<td><span data-ttu-id="c4827-414">Gibt einen der folgenden Typen von Datei Teilungen zurück:</span><span class="sxs-lookup"><span data-stu-id="c4827-414">Returns one of the following file division types:</span></span>
<ul>
<li><span data-ttu-id="c4827-415">Ppqn</span><span class="sxs-lookup"><span data-stu-id="c4827-415">PPQN</span></span></li>
<li><span data-ttu-id="c4827-416">SMPTE 24-Frame</span><span class="sxs-lookup"><span data-stu-id="c4827-416">SMPTE 24 frame</span></span></li>
<li><span data-ttu-id="c4827-417">SMPTE 25-Frame</span><span class="sxs-lookup"><span data-stu-id="c4827-417">SMPTE 25 frame</span></span></li>
<li><span data-ttu-id="c4827-418">SMPTE 30-Ablage Rahmen</span><span class="sxs-lookup"><span data-stu-id="c4827-418">SMPTE 30 drop frame</span></span></li>
<li><span data-ttu-id="c4827-419">SMPTE 30-Frame</span><span class="sxs-lookup"><span data-stu-id="c4827-419">SMPTE 30 frame</span></span></li>
</ul>
<br/> <span data-ttu-id="c4827-420">Verwenden Sie diese Informationen, um das Format der Datei "MIDI" und die Bedeutung von "Tempo" und Positionsinformationen zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="c4827-420">Use this information to determine the format of the MIDI file and the meaning of tempo and position information.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c4827-421">Datei Abschluss</span><span class="sxs-lookup"><span data-stu-id="c4827-421">file completion</span></span></td>
<td><span data-ttu-id="c4827-422">Gibt den geschätzten Prozentsatz für das <a href="load.md">Laden</a>, <a href="save.md">Speichern</a>, <a href="capture.md">erfassen</a>, <a href="cut.md">Ausschneiden</a>, <a href="copy.md">Kopieren</a>, <a href="delete.md">Löschen</a>, <a href="paste.md">Einfügen</a>oder Rückgängigmachen fort. <a href="undo.md"></a></span><span class="sxs-lookup"><span data-stu-id="c4827-422">Returns the estimated percentage a <a href="load.md">load</a>, <a href="save.md">save</a>, <a href="capture.md">capture</a>, <a href="cut.md">cut</a>, <a href="copy.md">copy</a>, <a href="delete.md">delete</a>, <a href="paste.md">paste</a>, or <a href="undo.md">undo</a> operation has progressed.</span></span> <span data-ttu-id="c4827-423">(Anwendungen können dies verwenden, um einen visuellen Indikator für den Fortschritt bereitzustellen.)</span><span class="sxs-lookup"><span data-stu-id="c4827-423">(Applications can use this to provide a visual indicator of progress.)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c4827-424">Dateiformat</span><span class="sxs-lookup"><span data-stu-id="c4827-424">file format</span></span></td>
<td><span data-ttu-id="c4827-425">Gibt das aktuelle Dateiformat für <a href="record.md">Daten Satz</a> -oder <strong>Speicher</strong> Befehle zurück.</span><span class="sxs-lookup"><span data-stu-id="c4827-425">Returns the current file format for <a href="record.md">record</a> or <strong>save</strong> commands.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c4827-426">Dateimodus</span><span class="sxs-lookup"><span data-stu-id="c4827-426">file mode</span></span></td>
<td><span data-ttu-id="c4827-427">Gibt das &quot; Laden &quot; , &quot; speichern &quot; , &quot; Bearbeiten oder im Leerlauf zurück &quot; &quot; &quot; .</span><span class="sxs-lookup"><span data-stu-id="c4827-427">Returns &quot;loading&quot;, &quot;saving&quot;, &quot;editing&quot;, or &quot;idle&quot;.</span></span> <span data-ttu-id="c4827-428">Während eines <a href="load.md"><strong>Lade</strong></a> Vorgangs wird das Laden zurückgegeben &quot; &quot; .</span><span class="sxs-lookup"><span data-stu-id="c4827-428">During a <a href="load.md"><strong>load</strong></a> operation, it returns &quot;loading&quot;.</span></span> <span data-ttu-id="c4827-429">Während der <a href="https://www.bing.com/search?q=<strong>save</strong>"><strong>Speicher</strong></a> -und <a href="capture.md"><strong>Aufzeichnungs</strong></a> Vorgänge wird das Speichern zurückgegeben &quot; &quot; .</span><span class="sxs-lookup"><span data-stu-id="c4827-429">During <a href="https://www.bing.com/search?q=<strong>save</strong>"><strong>save</strong></a> and <a href="capture.md"><strong>capture</strong></a> operations, it returns &quot;saving&quot;.</span></span> <span data-ttu-id="c4827-430">Beim <a href="cut.md"><strong>Ausschneiden</strong></a>, <a href="copy.md"><strong>Kopieren</strong></a>, <a href="delete.md"><strong>Löschen</strong></a>, <a href="paste.md"><strong>Einfügen</strong></a>oder Rückgängigmachen wird die Bearbeitung zurückgegeben <a href="undo.md"><strong></strong></a> &quot; &quot; .</span><span class="sxs-lookup"><span data-stu-id="c4827-430">During <a href="cut.md"><strong>cut</strong></a>, <a href="copy.md"><strong>copy</strong></a>, <a href="delete.md"><strong>delete</strong></a>, <a href="paste.md"><strong>paste</strong></a>, or <a href="undo.md"><strong>undo</strong></a> operations, it returns &quot;editing&quot;.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c4827-431">Tag formatieren</span><span class="sxs-lookup"><span data-stu-id="c4827-431">format tag</span></span></td>
<td><span data-ttu-id="c4827-432">Gibt das Formattag zurück.</span><span class="sxs-lookup"><span data-stu-id="c4827-432">Returns the format tag.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c4827-433">forward</span><span class="sxs-lookup"><span data-stu-id="c4827-433">forward</span></span></td>
<td><span data-ttu-id="c4827-434">Gibt <strong>true</strong> zurück, wenn die Wiedergabe Richtung vorwärts ist oder wenn das Gerät nicht wiedergegeben wird.</span><span class="sxs-lookup"><span data-stu-id="c4827-434">Returns <strong>TRUE</strong> if the play direction is forward or if the device is not playing.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c4827-435">Framerate</span><span class="sxs-lookup"><span data-stu-id="c4827-435">frame rate</span></span></td>
<td><span data-ttu-id="c4827-436">Gibt die Anzahl von Frames pro Sekunde zurück, die vom Gerät standardmäßig verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c4827-436">Returns the number of frames per second that the device will use by default.</span></span> <span data-ttu-id="c4827-437">Von NTSC-Geräten werden 30, PAL 25 usw. zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="c4827-437">NTSC devices return 30, PAL 25, and so on.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c4827-438">Übersprungene Frames</span><span class="sxs-lookup"><span data-stu-id="c4827-438">frames skipped</span></span></td>
<td><span data-ttu-id="c4827-439">Gibt die Anzahl der Frames zurück, die beim Abspielen der letzten AVI-Sequenz nicht gezeichnet wurden.</span><span class="sxs-lookup"><span data-stu-id="c4827-439">Returns the number of frames that were not drawn when the last AVI sequence was played.</span></span> <span data-ttu-id="c4827-440">Dieses Flag wird nur vom MCIAVI Digital-Video-Treiber erkannt.</span><span class="sxs-lookup"><span data-stu-id="c4827-440">This flag is recognized only by the MCIAVI digital-video driver.</span></span> <span data-ttu-id="c4827-441">Es ist nur für die Leistungs Auswertung gedacht. der Rückgabewert ist schwierig zu interpretieren.</span><span class="sxs-lookup"><span data-stu-id="c4827-441">It is meant for performance evaluation only; the return value is difficult to interpret.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c4827-442">Gamma</span><span class="sxs-lookup"><span data-stu-id="c4827-442">gamma</span></span></td>
<td><span data-ttu-id="c4827-443">Gibt den Wert zurück, der mit <a href="setvideo.md"><strong>setvideo</strong></a> &quot; Gamma auf Value festgelegt wurde &quot; <em></em>.</span><span class="sxs-lookup"><span data-stu-id="c4827-443">Returns the value set with <a href="setvideo.md"><strong>setvideo</strong></a> &quot;gamma to&quot; <em>value</em>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c4827-444">Index</span><span class="sxs-lookup"><span data-stu-id="c4827-444">index</span></span></td>
<td><span data-ttu-id="c4827-445">Gibt die aktuelle Index Anzeige zurück.</span><span class="sxs-lookup"><span data-stu-id="c4827-445">Returns the current index display.</span></span> <span data-ttu-id="c4827-446">Weitere Informationen finden Sie unter dem Befehl <a href="set.md"><strong>Set</strong></a> &quot; Index &quot; .</span><span class="sxs-lookup"><span data-stu-id="c4827-446">For more information, see the <a href="set.md"><strong>set</strong></a> &quot;index&quot; command.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c4827-447">Index für</span><span class="sxs-lookup"><span data-stu-id="c4827-447">index on</span></span></td>
<td><span data-ttu-id="c4827-448">Gibt <strong>true</strong> zurück, wenn der Index on ist.</span><span class="sxs-lookup"><span data-stu-id="c4827-448">Returns <strong>TRUE</strong> if the index is on.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c4827-449">input</span><span class="sxs-lookup"><span data-stu-id="c4827-449">input</span></span></td>
<td><span data-ttu-id="c4827-450">Gibt den Eingabe Satz zurück.</span><span class="sxs-lookup"><span data-stu-id="c4827-450">Returns the input set.</span></span> <span data-ttu-id="c4827-451">Wenn kein Wert festgelegt ist, gibt der zurückgegebene Fehler an, dass ein beliebiges Gerät verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="c4827-451">If one is not set, the error returned indicates that any device can be used.</span></span> <span data-ttu-id="c4827-452">Bei Digital Video-Geräten werden die Flags "Bass", "Höhen", "Volume", "Helligkeit", "Farbe", " &quot; &quot; Kontrast", "Gamma", " &quot; Schärfe" &quot; &quot; &quot; &quot; oder " &quot; &quot; &quot; &quot; &quot; &quot; &quot; Tönungs" so geändert, &quot; &quot; &quot; &quot; dass Sie nur</span><span class="sxs-lookup"><span data-stu-id="c4827-452">For digital-video devices, modifies the &quot;bass&quot;, &quot;treble&quot;, &quot;volume&quot;, &quot;brightness&quot;, &quot;color&quot;, &quot;contrast&quot;, &quot;gamma&quot;, &quot;sharpness&quot;, or &quot;tint&quot; flag so that it applies only to the input.</span></span> <span data-ttu-id="c4827-453">Dies ist die Standardeinstellung, wenn die Eingabe überwacht wird.</span><span class="sxs-lookup"><span data-stu-id="c4827-453">This is the default when monitoring the input.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c4827-454">Linkes Volume</span><span class="sxs-lookup"><span data-stu-id="c4827-454">left volume</span></span></td>
<td><span data-ttu-id="c4827-455">Gibt das für den linken Audiokanal festgelegte Volume zurück.</span><span class="sxs-lookup"><span data-stu-id="c4827-455">Returns the volume set for the left audio channel.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c4827-456">length</span><span class="sxs-lookup"><span data-stu-id="c4827-456">length</span></span></td>
<td><span data-ttu-id="c4827-457">Gibt die Gesamtlänge des Mediums im aktuellen Zeitformat zurück.</span><span class="sxs-lookup"><span data-stu-id="c4827-457">Returns the total length of the media, in the current time format.</span></span> <span data-ttu-id="c4827-458">Bei ppqn-Dateien wird die Länge in Song Zeiger Einheiten zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="c4827-458">For PPQN files, the length is returned in song pointer units.</span></span> <span data-ttu-id="c4827-459">Für SMPTE-Dateien wird dieser Wert als <em>hh: mm: SS: FF</em>zurückgegeben, wobei <em>HH</em> Stunden, <em>mm</em> den Wert Minutes, <em>SS</em> den Wert seconds und <em>FF</em> ein Rahmen ist.</span><span class="sxs-lookup"><span data-stu-id="c4827-459">For SMPTE files, it is returned as <em>hh:mm:ss:ff</em>, where <em>hh</em> is hours, <em>mm</em> is minutes, <em>ss</em> is seconds, and <em>ff</em> is frames.</span></span> <span data-ttu-id="c4827-460">Bei VCR-Geräten beträgt die Länge 2 Stunden (es sei denn, die Länge wurde explizit mit dem <a href="https://www.bing.com/search?q=<strong>set</strong>"><strong>Set</strong></a> -Befehl geändert).</span><span class="sxs-lookup"><span data-stu-id="c4827-460">For VCR devices, the length is 2 hours (unless the length has been explicitly changed using the <a href="https://www.bing.com/search?q=<strong>set</strong>"><strong>set</strong></a> command).</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c4827-461">Länge der <em>Nachverfolgung</em></span><span class="sxs-lookup"><span data-stu-id="c4827-461">length track <em>number</em></span></span></td>
<td><span data-ttu-id="c4827-462">Gibt die Länge der Spur (in Zeit oder Rahmen) zurück, die durch <em>Number</em>angegeben wird. Bei ppqn-Dateien wird die Länge in Song Zeiger Einheiten zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="c4827-462">Returns the length of the track, in time or frames, specified by <em>number</em>.For PPQN files, the length is returned in song pointer units.</span></span> <span data-ttu-id="c4827-463">Für SMPTE-Dateien wird dieser Wert als <em>hh: mm: SS: FF</em>zurückgegeben, wobei <em>HH</em> Stunden, <em>mm</em> den Wert Minutes, <em>SS</em> den Wert seconds und <em>FF</em> ein Rahmen ist.</span><span class="sxs-lookup"><span data-stu-id="c4827-463">For SMPTE files, it is returned as <em>hh:mm:ss:ff</em>, where <em>hh</em> is hours, <em>mm</em> is minutes, <em>ss</em> is seconds, and <em>ff</em> is frames.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c4827-464">Level</span><span class="sxs-lookup"><span data-stu-id="c4827-464">level</span></span></td>
<td><span data-ttu-id="c4827-465">Gibt den aktuellen PCM-audiobeispielwert zurück.</span><span class="sxs-lookup"><span data-stu-id="c4827-465">Returns the current PCM audio sample value.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c4827-466">master</span><span class="sxs-lookup"><span data-stu-id="c4827-466">master</span></span></td>
<td><span data-ttu-id="c4827-467">Gibt " &quot; MIDI", "None" oder " &quot; &quot; &quot; &quot; SMPTE" &quot; abhängig vom Typ des Synchronisierungs Satzes zurück.</span><span class="sxs-lookup"><span data-stu-id="c4827-467">Returns &quot;midi&quot;, &quot;none&quot;, or &quot;smpte&quot; depending on the type of synchronization set.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c4827-468">Medien vorhanden</span><span class="sxs-lookup"><span data-stu-id="c4827-468">media present</span></span></td>
<td><span data-ttu-id="c4827-469">Gibt " <strong>true</strong> " zurück, wenn das Medium in das Gerät eingefügt wird, andernfalls " <strong>false</strong> ".</span><span class="sxs-lookup"><span data-stu-id="c4827-469">Returns <strong>TRUE</strong> if the media is inserted in the device or <strong>FALSE</strong> otherwise.</span></span> <span data-ttu-id="c4827-470">Sequencer-, Video-Overlay-, Digital Video-und Waveform-Audiogeräte geben " <strong>true</strong>" zurück.</span><span class="sxs-lookup"><span data-stu-id="c4827-470">Sequencer, video-overlay, digital-video, and waveform-audio devices return <strong>TRUE</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c4827-471">Medientyp</span><span class="sxs-lookup"><span data-stu-id="c4827-471">media type</span></span></td>
<td><span data-ttu-id="c4827-472">Gibt den Typ des Mediums zurück.</span><span class="sxs-lookup"><span data-stu-id="c4827-472">Returns the type of the media.</span></span> <span data-ttu-id="c4827-473">Bei VCRs sind dies &quot; 8mm &quot; , &quot; VHS &quot; , &quot; SVHS &quot; , &quot; Beta &quot; , &quot; Hi8 &quot; , &quot; edbeta &quot; oder &quot; andere &quot; .</span><span class="sxs-lookup"><span data-stu-id="c4827-473">For VCRS, this is &quot;8mm&quot;, &quot;vhs&quot;, &quot;svhs&quot;, &quot;beta&quot;, &quot;Hi8&quot;, &quot;edbeta&quot;, or &quot;other&quot;.</span></span> <span data-ttu-id="c4827-474">Bei Video Disks handelt es sich hierbei um &quot; CAV &quot; , &quot; CLV &quot; oder &quot; andere &quot; , abhängig vom Typ der Videodisk.</span><span class="sxs-lookup"><span data-stu-id="c4827-474">For videodiscs, this is &quot;CAV&quot;, &quot;CLV&quot;, or &quot;other&quot;, depending on the type of videodisc.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c4827-475">Modus</span><span class="sxs-lookup"><span data-stu-id="c4827-475">mode</span></span></td>
<td><span data-ttu-id="c4827-476">Gibt den aktuellen Modus des Geräts zurück.</span><span class="sxs-lookup"><span data-stu-id="c4827-476">Returns the current mode of the device.</span></span> <span data-ttu-id="c4827-477">Alle Geräte können die Werte "nicht bereit", "angehalten", "wieder &quot; Gabe" &quot; und " &quot; &quot; &quot; &quot; &quot; angehalten &quot; "</span><span class="sxs-lookup"><span data-stu-id="c4827-477">All devices can return the &quot;not ready&quot;, &quot;paused&quot;, &quot;playing&quot;, and &quot;stopped&quot; values.</span></span> <span data-ttu-id="c4827-478">Einige Geräte können die zusätzlichen &quot; Werte für geöffnete, geöffnetes &quot; &quot; &quot; , &quot; aufzeichnen &quot; und &quot; Suchen &quot; zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="c4827-478">Some devices can return the additional &quot;open&quot;, &quot;parked&quot;, &quot;recording&quot;, and &quot;seeking&quot; values.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c4827-479">Überwachen</span><span class="sxs-lookup"><span data-stu-id="c4827-479">monitor</span></span></td>
<td><span data-ttu-id="c4827-480">Gibt die &quot; Datei &quot; oder die Eingabe zurück &quot; &quot; .</span><span class="sxs-lookup"><span data-stu-id="c4827-480">Returns &quot;file&quot; or &quot;input&quot;.</span></span> <span data-ttu-id="c4827-481">Der zurückgegebene Wert gibt die aktuelle Präsentations Quelle an.</span><span class="sxs-lookup"><span data-stu-id="c4827-481">The returned value indicates the current presentation source.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c4827-482">Monitor-Methode</span><span class="sxs-lookup"><span data-stu-id="c4827-482">monitor method</span></span></td>
<td><span data-ttu-id="c4827-483">Gibt &quot; Pre &quot; , &quot; Post &quot; oder &quot; Direct zurück &quot; .</span><span class="sxs-lookup"><span data-stu-id="c4827-483">Returns &quot;pre&quot;, &quot;post&quot;, or &quot;direct&quot;.</span></span> <span data-ttu-id="c4827-484">Der zurückgegebene Wert gibt die für die Eingabe Überwachung verwendete Methode an.</span><span class="sxs-lookup"><span data-stu-id="c4827-484">The returned value indicates the method used for input monitoring.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c4827-485">ell</span><span class="sxs-lookup"><span data-stu-id="c4827-485">nominal</span></span></td>
<td><span data-ttu-id="c4827-486">Das Element ändert die Flags "Bass", "Helligkeit", "Color", "Contrast", "Gamma", "Schärding", "Tönungs", "Treble" und "Volume", sodass &quot; &quot; &quot; &quot; &quot; &quot; &quot; &quot; &quot; &quot; &quot; &quot; &quot; &quot; &quot; &quot; &quot; &quot; anstelle der aktuellen Einstellung der</span><span class="sxs-lookup"><span data-stu-id="c4827-486">The item modifies the &quot;bass&quot;, &quot;brightness&quot;, &quot;color&quot;, &quot;contrast&quot;, &quot;gamma&quot;, &quot;sharpness&quot;, &quot;tint&quot;, &quot;treble,&quot; and &quot;volume&quot; flags to return the nominal value instead of the current setting.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c4827-487">Nominale Bildrate</span><span class="sxs-lookup"><span data-stu-id="c4827-487">nominal frame rate</span></span></td>
<td><span data-ttu-id="c4827-488">Gibt die nominale Frame Rate zurück, die der Datei zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="c4827-488">Returns the nominal frame rate associated with the file.</span></span> <span data-ttu-id="c4827-489">Die Einheiten werden in Frames pro Sekunde multipliziert mit 1000.</span><span class="sxs-lookup"><span data-stu-id="c4827-489">The units are in frames per second multiplied by 1000.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c4827-490">Nominale Daten Satz Rahmenrate</span><span class="sxs-lookup"><span data-stu-id="c4827-490">nominal record frame rate</span></span></td>
<td><span data-ttu-id="c4827-491">Gibt die nominale Frame Rate zurück, die mit dem Eingabe Videosignal verknüpft ist.</span><span class="sxs-lookup"><span data-stu-id="c4827-491">Returns the nominal frame rate associated with the input video signal.</span></span> <span data-ttu-id="c4827-492">Die Einheiten werden in Frames pro Sekunde multipliziert mit 1000.</span><span class="sxs-lookup"><span data-stu-id="c4827-492">The units are in frames per second multiplied by 1000.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c4827-493">Anzahl von Audiospuren</span><span class="sxs-lookup"><span data-stu-id="c4827-493">number of audio tracks</span></span></td>
<td><span data-ttu-id="c4827-494">Gibt die Anzahl der Audiospuren auf den Medien zurück.</span><span class="sxs-lookup"><span data-stu-id="c4827-494">Returns the number of audio tracks on the media.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c4827-495">Anzahl der Spuren</span><span class="sxs-lookup"><span data-stu-id="c4827-495">number of tracks</span></span></td>
<td><span data-ttu-id="c4827-496">Gibt die Anzahl der Spuren auf den Medien zurück.</span><span class="sxs-lookup"><span data-stu-id="c4827-496">Returns the number of tracks on the media.</span></span> <span data-ttu-id="c4827-497">Die Geräte mcite q und MCIWave geben 1 zurück, wie die meisten VCR-Geräte.</span><span class="sxs-lookup"><span data-stu-id="c4827-497">The MCISEQ and MCIWAVE devices return 1, as do most VCR devices.</span></span> <span data-ttu-id="c4827-498">Dieses Flag wird vom mcipionr-Gerät nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="c4827-498">The MCIPIONR device does not support this flag.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c4827-499">Anzahl der Videospuren</span><span class="sxs-lookup"><span data-stu-id="c4827-499">number of video tracks</span></span></td>
<td><span data-ttu-id="c4827-500">Gibt die Anzahl der Videospuren auf den Medien zurück.</span><span class="sxs-lookup"><span data-stu-id="c4827-500">Returns the number of video tracks on the media.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c4827-501">offset</span><span class="sxs-lookup"><span data-stu-id="c4827-501">offset</span></span></td>
<td><span data-ttu-id="c4827-502">Gibt den Offset einer SMPTE-basierten Datei zurück.</span><span class="sxs-lookup"><span data-stu-id="c4827-502">Returns the offset of a SMPTE-based file.</span></span> <span data-ttu-id="c4827-503">Der Offset ist die Startzeit einer SMPTE-basierten Sequenz.</span><span class="sxs-lookup"><span data-stu-id="c4827-503">The offset is the start time of a SMPTE-based sequence.</span></span> <span data-ttu-id="c4827-504">Die Zeit wird als <em>hh: mm: SS: FF</em>zurückgegeben, <em>wobei HH</em> Stunden, <em>mm</em> den Wert Minutes, <em>SS</em> den Wert Sekunden und <em>FF</em> ein Rahmen ist.</span><span class="sxs-lookup"><span data-stu-id="c4827-504">The time is returned as <em>hh:mm:ss:ff</em>, where <em>hh</em> is hours, <em>mm</em> is minutes, <em>ss</em> is seconds, and <em>ff</em> is frames.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c4827-505">output</span><span class="sxs-lookup"><span data-stu-id="c4827-505">output</span></span></td>
<td><span data-ttu-id="c4827-506">Gibt die aktuell festgelegte Ausgabe zurück.</span><span class="sxs-lookup"><span data-stu-id="c4827-506">Returns the currently set output.</span></span> <span data-ttu-id="c4827-507">Wenn keine Ausgabe festgelegt ist, gibt der zurückgegebene Fehler an, dass ein beliebiges Gerät verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="c4827-507">If no output is set, the error returned indicates that any device can be used.</span></span> <span data-ttu-id="c4827-508">Bei Digital Video-Geräten werden die Flags "Bass", "Höhen", "Volume", "Helligkeit", "Farbe", " &quot; &quot; Kontrast", "Gamma", " &quot; Schärfe" &quot; &quot; &quot; &quot; oder " &quot; &quot; &quot; &quot; &quot; &quot; &quot; Tönungs" so geändert, &quot; &quot; &quot; &quot; dass Sie nur</span><span class="sxs-lookup"><span data-stu-id="c4827-508">For digital-video devices, modifies the &quot;bass&quot;, &quot;treble&quot;, &quot;volume&quot;, &quot;brightness&quot;, &quot;color&quot;, &quot;contrast&quot;, &quot;gamma&quot;, &quot;sharpness&quot;, or &quot;tint&quot; flag so that it applies only to the output.</span></span> <span data-ttu-id="c4827-509">Dies ist die Standardeinstellung beim Überwachen einer Datei.</span><span class="sxs-lookup"><span data-stu-id="c4827-509">This is the default when monitoring a file.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c4827-510">Pausenmodus</span><span class="sxs-lookup"><span data-stu-id="c4827-510">pause mode</span></span></td>
<td><span data-ttu-id="c4827-511">Gibt eine Aufzeichnung zurück, &quot; &quot; Wenn das Gerät während der Aufzeichnung angehalten wird.</span><span class="sxs-lookup"><span data-stu-id="c4827-511">Returns &quot;recording&quot; if the device is paused while recording.</span></span> <span data-ttu-id="c4827-512">Die Wiedergabe wird zurückgegeben, &quot; &quot; Wenn das Gerät während der Wiedergabe angehalten wird.</span><span class="sxs-lookup"><span data-stu-id="c4827-512">It returns &quot;playing&quot; if the device is paused while playing.</span></span> <span data-ttu-id="c4827-513">Sie gibt die Fehler Aktion zurück, die &quot; im aktuellen Modus nicht anwendbar &quot; ist, wenn das Gerät nicht angehalten wurde.</span><span class="sxs-lookup"><span data-stu-id="c4827-513">It returns the error &quot;Action not applicable in current mode&quot; if the device is not paused.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c4827-514">Timeout für Pause</span><span class="sxs-lookup"><span data-stu-id="c4827-514">pause timeout</span></span></td>
<td><span data-ttu-id="c4827-515">Gibt die maximale Dauer eines <a href="pause.md"><strong>Pause</strong></a> -Befehls in Millisekunden zurück.</span><span class="sxs-lookup"><span data-stu-id="c4827-515">Returns the maximum duration, in milliseconds, of a <a href="pause.md"><strong>pause</strong></a> command.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c4827-516">Wiedergabe Format</span><span class="sxs-lookup"><span data-stu-id="c4827-516">play format</span></span></td>
<td><span data-ttu-id="c4827-517">Gibt einen Code zurück, der das Format angibt, in dem das Videoband wiedergegeben wird, wenn es erkennbar ist: &quot; LP &quot; , &quot; EP &quot; , &quot; SP &quot; oder &quot; andere &quot; .</span><span class="sxs-lookup"><span data-stu-id="c4827-517">Returns a code indicating the format that the videotape will be played back in, if detectable: &quot;lp&quot;, &quot;ep&quot;, &quot;sp&quot;, or &quot;other&quot;.</span></span> <span data-ttu-id="c4827-518">Weitere Informationen finden Sie unter Flag für das &quot; Daten Satz Format &quot; .</span><span class="sxs-lookup"><span data-stu-id="c4827-518">For more information, see the &quot;record format&quot; flag.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c4827-519">Wiedergabegeschwindigkeit</span><span class="sxs-lookup"><span data-stu-id="c4827-519">play speed</span></span></td>
<td><span data-ttu-id="c4827-520">Gibt einen Wert zurück, der angibt, wie genau die tatsächliche Wiedergabezeit der letzten AVI-Sequenz mit der Ziel Wiedergabezeit übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="c4827-520">Returns a value representing how closely the actual playing time of the last AVI sequence matched the target playing time.</span></span> <span data-ttu-id="c4827-521">Der Wert 1000 gibt an, dass die Zielzeit und die tatsächliche zeitgleich sind.</span><span class="sxs-lookup"><span data-stu-id="c4827-521">The value 1000 indicates that the target time and the actual time were the same.</span></span> <span data-ttu-id="c4827-522">Der Wert 2000 gibt z. b. an, dass die AVI-Sequenz zweimal so lange gedauert hat, wie Sie vorhanden sein sollte.</span><span class="sxs-lookup"><span data-stu-id="c4827-522">A value of 2000, for example, would indicate that the AVI sequence took twice as long to play as it should have.</span></span> <span data-ttu-id="c4827-523">Dieses Flag wird nur vom MCIAVI Digital-Video-Treiber erkannt.</span><span class="sxs-lookup"><span data-stu-id="c4827-523">This flag is recognized only by the MCIAVI digital-video driver.</span></span> <span data-ttu-id="c4827-524">Es ist nur für die Leistungs Auswertung gedacht. der Rückgabewert ist schwierig zu interpretieren.</span><span class="sxs-lookup"><span data-stu-id="c4827-524">It is meant for performance evaluation only; the return value is difficult to interpret.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c4827-525">port</span><span class="sxs-lookup"><span data-stu-id="c4827-525">port</span></span></td>
<td><span data-ttu-id="c4827-526">Gibt die der Sequenz zugewiesene Nummer des MIDI-Ports zurück.</span><span class="sxs-lookup"><span data-stu-id="c4827-526">Returns the MIDI port number assigned to the sequence.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c4827-527">position</span><span class="sxs-lookup"><span data-stu-id="c4827-527">position</span></span></td>
<td><span data-ttu-id="c4827-528">Gibt die aktuelle Position zurück. Bei ppqn-Dateien wird die Position in den Zeiger Einheiten des Titels zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="c4827-528">Returns the current position.For PPQN files, the position is returned in song pointer units.</span></span> <span data-ttu-id="c4827-529">Für SMPTE-Dateien wird dieser Wert als <em>hh: mm: SS: FF</em>zurückgegeben, wobei <em>HH</em> Stunden, <em>mm</em> den Wert Minutes, SS den Wert seconds und <em>FF</em> ein Rahmen ist.</span><span class="sxs-lookup"><span data-stu-id="c4827-529">For SMPTE files, it is returned as <em>hh:mm:ss:ff</em>, where <em>hh</em> is hours, <em>mm</em> is minutes, ss is seconds, and <em>ff</em> is frames.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c4827-530">Positions Anfang</span><span class="sxs-lookup"><span data-stu-id="c4827-530">position start</span></span></td>
<td><span data-ttu-id="c4827-531">Gibt die Position des Starts der verwendbaren Medien zurück.</span><span class="sxs-lookup"><span data-stu-id="c4827-531">Returns the position of the start of the usable media.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c4827-532">Positions <em>Nummer</em></span><span class="sxs-lookup"><span data-stu-id="c4827-532">position track <em>number</em></span></span></td>
<td><span data-ttu-id="c4827-533">Gibt die Position des Starts der Spur zurück, die durch <em>Number</em>angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="c4827-533">Returns the position of the start of the track specified by <em>number</em>.</span></span> <span data-ttu-id="c4827-534">Bei ppqn-Dateien wird das Zeitformat in den zeigerpointer-Einheiten zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="c4827-534">For PPQN files, the time format is returned in song pointer units.</span></span> <span data-ttu-id="c4827-535">Für SMPTE-Dateien wird dieser Wert als <em>hh: mm: SS: FF</em>zurückgegeben, wobei <em>HH</em> Stunden, <em>mm</em> den Wert Minutes, <em>SS</em> den Wert seconds und <em>FF</em> ein Rahmen ist.</span><span class="sxs-lookup"><span data-stu-id="c4827-535">For SMPTE files, it is returned as <em>hh:mm:ss:ff</em>, where <em>hh</em> is hours, <em>mm</em> is minutes, <em>ss</em> is seconds, and <em>ff</em> is frames.</span></span> <span data-ttu-id="c4827-536">Der mcist-Sequencer gibt 0 (null) zurück.</span><span class="sxs-lookup"><span data-stu-id="c4827-536">The MCISEQ sequencer returns zero.</span></span> <span data-ttu-id="c4827-537">Dieses Flag wird vom mcipionr-Gerät nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="c4827-537">The MCIPIONR device does not support this flag.</span></span> <span data-ttu-id="c4827-538">Das MCIWave-Gerät gibt NULL zurück.</span><span class="sxs-lookup"><span data-stu-id="c4827-538">The MCIWAVE device returns zero.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c4827-539">Postroll Dauer</span><span class="sxs-lookup"><span data-stu-id="c4827-539">postroll duration</span></span></td>
<td><span data-ttu-id="c4827-540">Gibt die Länge von Videotape im aktuellen Zeitformat zurück, das zum Abbremsen des VCR-Transports erforderlich ist, <a href="pause.md"><strong></strong></a> wenn ein Befehl zum <a href="stop.md"><strong>Beenden oder anhalten</strong></a> ausgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="c4827-540">Returns the length of videotape, in the current time format, needed to brake the VCR transport when a <a href="stop.md"><strong>stop</strong></a> or <a href="pause.md"><strong>pause</strong></a> command is issued.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c4827-541">Einschalten</span><span class="sxs-lookup"><span data-stu-id="c4827-541">power on</span></span></td>
<td><span data-ttu-id="c4827-542">Gibt " <strong>true</strong> " zurück, wenn die VCR-Stromversorgung eingeschaltet ist.</span><span class="sxs-lookup"><span data-stu-id="c4827-542">Returns <strong>TRUE</strong> if the VCR's power is on.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c4827-543">Vorabversion</span><span class="sxs-lookup"><span data-stu-id="c4827-543">preroll duration</span></span></td>
<td><span data-ttu-id="c4827-544">Gibt die Länge von Videotape im aktuellen Zeitformat zurück, das zum stabilisieren der VCR-Ausgabe benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="c4827-544">Returns the length of videotape, in the current time format, needed to stabilize the VCR output.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c4827-545">ready</span><span class="sxs-lookup"><span data-stu-id="c4827-545">ready</span></span></td>
<td><span data-ttu-id="c4827-546">Gibt " <strong>true</strong> " zurück, wenn das Gerät bereit ist, einen anderen Befehl zu akzeptieren.</span><span class="sxs-lookup"><span data-stu-id="c4827-546">Returns <strong>TRUE</strong> if the device is ready to accept another command.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c4827-547">Daten Satz Format</span><span class="sxs-lookup"><span data-stu-id="c4827-547">record format</span></span></td>
<td><span data-ttu-id="c4827-548">Gibt einen Code zurück, der das Format angibt, in dem das Videoband aufgezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="c4827-548">Returns a code indicating the format that the videotape will be recorded in.</span></span> <span data-ttu-id="c4827-549">Die aktuellen Rückgabe Typen sind &quot; LP &quot; , &quot; EP &quot; , &quot; SP &quot; oder &quot; andere &quot; .</span><span class="sxs-lookup"><span data-stu-id="c4827-549">The current return types are &quot;lp&quot;, &quot;ep&quot;, &quot;sp&quot;, or &quot;other&quot;.</span></span> <span data-ttu-id="c4827-550">Diese Formate sind nicht für die VHS spezifisch und können auf alle VCR angewendet werden, die über mehrere auswählbare Aufzeichnungs Formate verfügen.</span><span class="sxs-lookup"><span data-stu-id="c4827-550">These formats are not VHS specific and can be applied to any VCR that has multiple selectable recording formats.</span></span> <span data-ttu-id="c4827-551">Der &quot; SP &quot; -Typ ist das schnellste, qualitativ hochwertige Aufzeichnungsformat und wird als Standardeinstellung für VCRs mit einem einzelnen Format verwendet.</span><span class="sxs-lookup"><span data-stu-id="c4827-551">The &quot;sp&quot; type is the fastest, highest quality recording format and is used as default on single format VCRs.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c4827-552">Frame Frequenz aufzeichnen</span><span class="sxs-lookup"><span data-stu-id="c4827-552">record frame rate</span></span></td>
<td><span data-ttu-id="c4827-553">Gibt die für die Komprimierung verwendete Frame Rate in Frames pro Sekunde multipliziert mit 1000 zurück.</span><span class="sxs-lookup"><span data-stu-id="c4827-553">Returns the frame rate, in frames per second multiplied by 1000, used for compression.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c4827-554">Verweis <em>Rahmen</em></span><span class="sxs-lookup"><span data-stu-id="c4827-554">reference <em>frame</em></span></span></td>
<td><span data-ttu-id="c4827-555">Gibt die Frame Nummer für das nächste Keyframe-Bild zurück, das dem angegebenen <em>Frame</em>vorangestellt ist.</span><span class="sxs-lookup"><span data-stu-id="c4827-555">Returns the frame number for the nearest key frame image that precedes the specified <em>frame</em>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c4827-556">reservierte Größe</span><span class="sxs-lookup"><span data-stu-id="c4827-556">reserved size</span></span></td>
<td><span data-ttu-id="c4827-557">Gibt die Größe des reservierten Arbeitsbereichs im aktuellen Zeitformat zurück.</span><span class="sxs-lookup"><span data-stu-id="c4827-557">Returns the size, in the current time format, of the reserved workspace.</span></span> <span data-ttu-id="c4827-558">Die Größe entspricht der ungefähren Zeit, die für die Wiedergabe der komprimierten Daten aus einem vollständigen Arbeitsbereich benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="c4827-558">The size corresponds to the approximate time it would take to play the compressed data from a full workspace.</span></span> <span data-ttu-id="c4827-559">Wenn kein reservierter Speicherplatz vorhanden ist, wird NULL zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="c4827-559">It returns zero if there is no reserved disk space.</span></span> <span data-ttu-id="c4827-560">Dieses Flag gibt die ungefähre Größe zurück, da der genaue Speicherplatz für komprimierte Daten im allgemeinen erst vorhergesagt werden kann, nachdem die Daten komprimiert wurden.</span><span class="sxs-lookup"><span data-stu-id="c4827-560">This flag returns the approximate size because the precise disk space for compressed data cannot, in general, be predicted until after the data has been compressed.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c4827-561">richtiges Volume</span><span class="sxs-lookup"><span data-stu-id="c4827-561">right volume</span></span></td>
<td><span data-ttu-id="c4827-562">Gibt das für den rechten Audiokanal festgelegte Volume zurück.</span><span class="sxs-lookup"><span data-stu-id="c4827-562">Returns the volume set for the right audio channel.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c4827-563">samplespersec</span><span class="sxs-lookup"><span data-stu-id="c4827-563">samplespersec</span></span></td>
<td><span data-ttu-id="c4827-564">Gibt die Anzahl der Stichproben pro Sekunde zurück, die abgespielt oder aufgezeichnet wurden.</span><span class="sxs-lookup"><span data-stu-id="c4827-564">Returns the number of samples per second played or recorded.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c4827-565">genau suchen</span><span class="sxs-lookup"><span data-stu-id="c4827-565">seek exactly</span></span></td>
<td><span data-ttu-id="c4827-566">Gibt &quot; ein &quot; oder &quot; aus zurück und gibt an &quot; , ob das &quot; suchgenau- &quot; Flag festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="c4827-566">Returns &quot;on&quot; or &quot;off&quot;, indicating whether or not the &quot;seek exactly&quot; flag is set.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c4827-567">Schärfe</span><span class="sxs-lookup"><span data-stu-id="c4827-567">sharpness</span></span></td>
<td><span data-ttu-id="c4827-568">Gibt die aktuelle Schärfe Ebene des Geräts zurück.</span><span class="sxs-lookup"><span data-stu-id="c4827-568">Returns the current sharpness level of the device.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c4827-569">Seite</span><span class="sxs-lookup"><span data-stu-id="c4827-569">side</span></span></td>
<td><span data-ttu-id="c4827-570">Gibt 1 oder 2 zurück, um anzugeben, welche Seite der Video Platte geladen wird.</span><span class="sxs-lookup"><span data-stu-id="c4827-570">Returns 1 or 2 to indicate which side of the videodisc is loaded.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c4827-571">Sklaverei</span><span class="sxs-lookup"><span data-stu-id="c4827-571">slave</span></span></td>
<td><span data-ttu-id="c4827-572">Gibt " &quot; file", "MIDI", "None" oder " &quot; &quot; &quot; &quot; &quot; &quot; SMPTE" &quot; abhängig vom Typ des Synchronisierungs Satzes zurück.</span><span class="sxs-lookup"><span data-stu-id="c4827-572">Returns &quot;file&quot; , &quot;midi&quot;, &quot;none&quot;, or &quot;smpte&quot; depending on the type of synchronization set.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c4827-573">SMPTE</span><span class="sxs-lookup"><span data-stu-id="c4827-573">smpte</span></span></td>
<td><span data-ttu-id="c4827-574">Gibt den SMPTE-Zeit Code zurück, der der aktuellen Position im Arbeitsbereich zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="c4827-574">Returns the SMPTE timecode associated with the current position in the workspace.</span></span> <span data-ttu-id="c4827-575">Dies ist eine Zeichenfolge mit dem Format <em>DD: DD: DD: DD</em>, wobei jede <em>d</em> eine Ziffer zwischen 0 und 9 bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="c4827-575">This is a string with the form <em>dd:dd:dd:dd</em>, where each <em>d</em> denotes a digit from 0 to 9.</span></span> <span data-ttu-id="c4827-576">Wenn die Arbeitsbereichs Daten keine Zeitcode-Daten enthalten, gibt dieses Flag 00:00:00:00 zurück.</span><span class="sxs-lookup"><span data-stu-id="c4827-576">If the workspace data does not include timecode data, then this flag returns 00:00:00:00.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c4827-577">Geschwindigkeit</span><span class="sxs-lookup"><span data-stu-id="c4827-577">speed</span></span></td>
<td><span data-ttu-id="c4827-578">Gibt die aktuelle Geschwindigkeit des Geräts in Frames pro Sekunde zurück (oder im gleichen Format, das vom Befehl <a href="https://www.bing.com/search?q=<strong>set</strong>"><strong>Set</strong></a> &quot; Speed verwendet wird &quot; ).</span><span class="sxs-lookup"><span data-stu-id="c4827-578">Returns the current speed of the device in frames per second (or in the same format used by the <a href="https://www.bing.com/search?q=<strong>set</strong>"><strong>set</strong></a> &quot;speed&quot; command).</span></span> <span data-ttu-id="c4827-579">Der mcipionr-Videodisk-Player unterstützt dieses Flag nicht.</span><span class="sxs-lookup"><span data-stu-id="c4827-579">The MCIPIONR videodisc player does not support this flag.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c4827-580">Startposition</span><span class="sxs-lookup"><span data-stu-id="c4827-580">start position</span></span></td>
<td><span data-ttu-id="c4827-581">Gibt die Anfangsposition der Medien zurück.</span><span class="sxs-lookup"><span data-stu-id="c4827-581">Returns the starting position of the media.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c4827-582">immer noch Dateiformat</span><span class="sxs-lookup"><span data-stu-id="c4827-582">still file format</span></span></td>
<td><span data-ttu-id="c4827-583">Gibt das aktuelle Dateiformat für den <a href="capture.md"><strong>Aufzeichnungs</strong></a> Befehl zurück.</span><span class="sxs-lookup"><span data-stu-id="c4827-583">Returns the current file format for the <a href="capture.md"><strong>capture</strong></a> command.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c4827-584">strecken</span><span class="sxs-lookup"><span data-stu-id="c4827-584">stretch</span></span></td>
<td><span data-ttu-id="c4827-585">Gibt <strong>true</strong> zurück, wenn die Streckung aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="c4827-585">Returns <strong>TRUE</strong> if stretching is enabled.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c4827-586">Lern</span><span class="sxs-lookup"><span data-stu-id="c4827-586">tempo</span></span></td>
<td><span data-ttu-id="c4827-587">Gibt das aktuelle Tempo einer MIDI-Sequenz im aktuellen Zeitformat zurück.</span><span class="sxs-lookup"><span data-stu-id="c4827-587">Returns the current tempo of a MIDI sequence in the current time format.</span></span> <span data-ttu-id="c4827-588">Für Dateien mit dem ppqn-Format liegt das Tempo in den Beats pro Minute.</span><span class="sxs-lookup"><span data-stu-id="c4827-588">For files with PPQN format, the tempo is in beats per minute.</span></span> <span data-ttu-id="c4827-589">Für Dateien mit dem SMPTE-Format wird das Tempo in Frames pro Sekunde angezeigt.</span><span class="sxs-lookup"><span data-stu-id="c4827-589">For files with SMPTE format, the tempo is in frames per second.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c4827-590">Zeitformat</span><span class="sxs-lookup"><span data-stu-id="c4827-590">time format</span></span></td>
<td><span data-ttu-id="c4827-591">Gibt das aktuelle Zeitformat zurück.</span><span class="sxs-lookup"><span data-stu-id="c4827-591">Returns the current time format.</span></span> <span data-ttu-id="c4827-592">Weitere Informationen finden Sie unter den Zeitformaten im <a href="set.md"><strong>Set</strong></a> -Befehl.</span><span class="sxs-lookup"><span data-stu-id="c4827-592">For more information, see the time formats in the <a href="set.md"><strong>set</strong></a> command.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c4827-593">Zeit Modus</span><span class="sxs-lookup"><span data-stu-id="c4827-593">time mode</span></span></td>
<td><span data-ttu-id="c4827-594">Gibt den aktuellen Positions Zeit Modus zurück.</span><span class="sxs-lookup"><span data-stu-id="c4827-594">Returns the current position time mode.</span></span> <span data-ttu-id="c4827-595">Es kann &quot; erkannt &quot; , &quot; Zeitcode &quot; oder Counter sein &quot; &quot; .</span><span class="sxs-lookup"><span data-stu-id="c4827-595">It can be &quot;detect&quot;, &quot;timecode&quot;, or &quot;counter&quot;.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c4827-596">Uhrzeittyp</span><span class="sxs-lookup"><span data-stu-id="c4827-596">time type</span></span></td>
<td><span data-ttu-id="c4827-597">Gibt die aktuelle Positions Zeit zurück, die verwendet wird: &quot; Zeitcode &quot; oder &quot; counter &quot; .</span><span class="sxs-lookup"><span data-stu-id="c4827-597">Returns the current position time in use: &quot;timecode&quot; or &quot;counter&quot;.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c4827-598">Zeit Code vorhanden</span><span class="sxs-lookup"><span data-stu-id="c4827-598">timecode present</span></span></td>
<td><span data-ttu-id="c4827-599">Gibt <strong>true</strong> zurück, wenn der Zeitcode an der aktuellen Position auf dem Band aufgezeichnet wurde.</span><span class="sxs-lookup"><span data-stu-id="c4827-599">Returns <strong>TRUE</strong> if timecode has been recorded at the current position on the tape.</span></span> <span data-ttu-id="c4827-600">Der Zeitcode muss von der aktuellen Position aus fortfahren.</span><span class="sxs-lookup"><span data-stu-id="c4827-600">The timecode must advance from the current position.</span></span> <span data-ttu-id="c4827-601">Möglicherweise muss ein VCR wiedergegeben werden, um diese Bedingung zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="c4827-601">A VCR might need to be played to check this condition.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c4827-602">Zeitcode-Datensatz</span><span class="sxs-lookup"><span data-stu-id="c4827-602">timecode record</span></span></td>
<td><span data-ttu-id="c4827-603">Gibt " <strong>true</strong> " zurück, wenn die VCR auf "Timecode aufzeichnen" festgelegt ist</span><span class="sxs-lookup"><span data-stu-id="c4827-603">Returns <strong>TRUE</strong> if the VCR is set to record timecode.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c4827-604">timecodetyp</span><span class="sxs-lookup"><span data-stu-id="c4827-604">timecode type</span></span></td>
<td><span data-ttu-id="c4827-605">Gibt &quot; SMPTE &quot; , &quot; SMPTE Drop &quot; , &quot; other &quot; oder &quot; None zurück &quot; .</span><span class="sxs-lookup"><span data-stu-id="c4827-605">Returns &quot;smpte&quot;, &quot;smpte drop&quot;, &quot;other&quot;, or &quot;none&quot;.</span></span> <span data-ttu-id="c4827-606">Beachten Sie, dass die Frames pro Sekunde über den Befehl "Status-Frame Rate" abgerufen werden können &quot; &quot; . die Genauigkeit des Geräts kann vom Befehl " <a href="capability.md"><strong>Capability</strong></a> Seek Accuracy" zurückgegeben werden &quot; &quot; .</span><span class="sxs-lookup"><span data-stu-id="c4827-606">Note the frames per second can be obtained from the status &quot;frame rate&quot; command, and the accuracy of the device can be returned by the <a href="capability.md"><strong>capability</strong></a> &quot;seek accuracy&quot; command.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c4827-607">Tönungs</span><span class="sxs-lookup"><span data-stu-id="c4827-607">tint</span></span></td>
<td><span data-ttu-id="c4827-608">Gibt die aktuelle Video-tint-Ebene zurück.</span><span class="sxs-lookup"><span data-stu-id="c4827-608">Returns the current video-tint level.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c4827-609">Höhen</span><span class="sxs-lookup"><span data-stu-id="c4827-609">treble</span></span></td>
<td><span data-ttu-id="c4827-610">Gibt die aktuelle audiotreble-Ebene zurück.</span><span class="sxs-lookup"><span data-stu-id="c4827-610">Returns the current audio-treble level.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c4827-611">Nummer des Tuners</span><span class="sxs-lookup"><span data-stu-id="c4827-611">tuner number</span></span></td>
<td><span data-ttu-id="c4827-612">Gibt die aktuelle logische-Tuner-Nummer zurück.</span><span class="sxs-lookup"><span data-stu-id="c4827-612">Returns the current logical-tuner number.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c4827-613">nicht gespeicherte</span><span class="sxs-lookup"><span data-stu-id="c4827-613">unsaved</span></span></td>
<td><span data-ttu-id="c4827-614">Gibt " <strong>true</strong> " zurück, wenn im Arbeitsbereich aufgezeichnete Daten verloren gehen, die als Ergebnis eines Befehls zum <a href="close.md"><strong>Schließen</strong></a>, <a href="load.md"><strong>Laden</strong></a>, <a href="record.md"><strong>aufzeichnen</strong></a>, <a href="reserve.md"><strong>reservieren</strong></a>, <a href="cut.md"><strong>Ausschneiden</strong></a>, <a href="delete.md"><strong>Löschen</strong></a>oder <a href="paste.md"><strong>Einfügen</strong></a> verloren gehen.</span><span class="sxs-lookup"><span data-stu-id="c4827-614">Returns <strong>TRUE</strong> if there is recorded data in the workspace that might be lost as a result of a <a href="close.md"><strong>close</strong></a>, <a href="load.md"><strong>load</strong></a>, <a href="record.md"><strong>record</strong></a>, <a href="reserve.md"><strong>reserve</strong></a>, <a href="cut.md"><strong>cut</strong></a>, <a href="delete.md"><strong>delete</strong></a>, or <a href="paste.md"><strong>paste</strong></a> command.</span></span> <span data-ttu-id="c4827-615">Gibt andernfalls <strong>false</strong> zurück.</span><span class="sxs-lookup"><span data-stu-id="c4827-615">Returns <strong>FALSE</strong> otherwise.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c4827-616">video</span><span class="sxs-lookup"><span data-stu-id="c4827-616">video</span></span></td>
<td><span data-ttu-id="c4827-617">Gibt &quot; ein &quot; oder &quot; aus zurück &quot; , das den vom <a href="setvideo.md"><strong>setvideo</strong></a> -Befehl festgelegten Status widerspiegelt.</span><span class="sxs-lookup"><span data-stu-id="c4827-617">Returns &quot;on&quot; or &quot;off&quot;, reflecting the state set by the <a href="setvideo.md"><strong>setvideo</strong></a> command.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c4827-618">Farbe des Video Schlüssels</span><span class="sxs-lookup"><span data-stu-id="c4827-618">video key color</span></span></td>
<td><span data-ttu-id="c4827-619">Gibt den Wert für die Schlüsselfarbe zurück.</span><span class="sxs-lookup"><span data-stu-id="c4827-619">Returns the value for the key color.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c4827-620">Video Schlüssel Index</span><span class="sxs-lookup"><span data-stu-id="c4827-620">video key index</span></span></td>
<td><span data-ttu-id="c4827-621">Gibt den Wert für den Schlüssel Index zurück.</span><span class="sxs-lookup"><span data-stu-id="c4827-621">Returns the value for the key index.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c4827-622">Videomonitor</span><span class="sxs-lookup"><span data-stu-id="c4827-622">video monitor</span></span></td>
<td><span data-ttu-id="c4827-623">Gibt &quot; &quot; die Ausgabe oder einen der gültigen Quell Eingabetypen zurück.</span><span class="sxs-lookup"><span data-stu-id="c4827-623">Returns &quot;output&quot; or one of the valid source-input types.</span></span> <span data-ttu-id="c4827-624">Weitere Informationen finden Sie unter dem Befehl " <a href="setvideo.md"><strong>setvideo</strong></a> &quot; Monitor" &quot; .</span><span class="sxs-lookup"><span data-stu-id="c4827-624">For more information, see the <a href="setvideo.md"><strong>setvideo</strong></a> &quot;monitor&quot; command.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c4827-625">Videomonitor Nummer</span><span class="sxs-lookup"><span data-stu-id="c4827-625">video monitor number</span></span></td>
<td><span data-ttu-id="c4827-626">Gibt die überwachte Video Nummer des vom Status Videomonitor zurückgegebenen Typs zurück &quot; &quot; .</span><span class="sxs-lookup"><span data-stu-id="c4827-626">Returns the monitored-video number of the type returned by status &quot;video monitor&quot;.</span></span> <span data-ttu-id="c4827-627">Weitere Informationen finden Sie unter dem Befehl <a href="setvideo.md">setvideo</a> .</span><span class="sxs-lookup"><span data-stu-id="c4827-627">For more information, see the <a href="setvideo.md">setvideo</a> command.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c4827-628">Videodaten Satz</span><span class="sxs-lookup"><span data-stu-id="c4827-628">video record</span></span></td>
<td><span data-ttu-id="c4827-629">Gibt &quot; ein &quot; oder &quot; aus &quot; dem aktuellen Zustand zurück, der durch den <a href="setvideo.md"><strong>setvideo</strong></a> -Datensatz festgelegt wird &quot; &quot; .</span><span class="sxs-lookup"><span data-stu-id="c4827-629">Returns &quot;on&quot; or &quot;off&quot;, reflecting the current state set by <a href="setvideo.md"><strong>setvideo</strong></a> &quot;record&quot;.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c4827-630"><em>Nummer</em> der Videodaten Satz Verfolgung</span><span class="sxs-lookup"><span data-stu-id="c4827-630">video record track <em>number</em></span></span></td>
<td><span data-ttu-id="c4827-631">Gibt " <strong>true</strong> " zurück, wenn VCR auf "Video aufzeichnen" festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="c4827-631">Return <strong>TRUE</strong> if the VCR is set to record video.</span></span> <span data-ttu-id="c4827-632">Wenn keine Nachverfolgung angegeben ist, wird der Standardwert 1 angenommen.</span><span class="sxs-lookup"><span data-stu-id="c4827-632">If no track number is given, the default value of 1 is assumed.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c4827-633">Videoquelle</span><span class="sxs-lookup"><span data-stu-id="c4827-633">video source</span></span></td>
<td><span data-ttu-id="c4827-634">Gibt den Typ der Videoquelle zurück.</span><span class="sxs-lookup"><span data-stu-id="c4827-634">Returns the video-source type.</span></span> <span data-ttu-id="c4827-635">Weitere Informationen finden Sie unter dem Befehl <a href="setvideo.md"><strong>setvideo</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="c4827-635">For more information, see the <a href="setvideo.md"><strong>setvideo</strong></a> command.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c4827-636">Video Quellnummer</span><span class="sxs-lookup"><span data-stu-id="c4827-636">video source number</span></span></td>
<td><span data-ttu-id="c4827-637">Gibt eine Zahl zurück, die der Videoquelle des verwendeten Typs entspricht.</span><span class="sxs-lookup"><span data-stu-id="c4827-637">Returns a number corresponding to the video source of the type in use.</span></span> <span data-ttu-id="c4827-638">Er gibt beispielsweise 2 zurück, wenn die zweite NTSC-Video Quell Eingabe verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="c4827-638">For example, it returns 2 if the second NTSC video source input is being used.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c4827-639">Videostream</span><span class="sxs-lookup"><span data-stu-id="c4827-639">video stream</span></span></td>
<td><span data-ttu-id="c4827-640">Gibt die aktuelle videostreamnummer zurück.</span><span class="sxs-lookup"><span data-stu-id="c4827-640">Returns the current video-stream number.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c4827-641">Volume</span><span class="sxs-lookup"><span data-stu-id="c4827-641">volume</span></span></td>
<td><span data-ttu-id="c4827-642">Gibt das durchschnittliche Volume für den linken und den rechten Redner zurück.</span><span class="sxs-lookup"><span data-stu-id="c4827-642">Returns the average volume to the left and right speaker.</span></span> <span data-ttu-id="c4827-643">Dadurch wird ein Fehler zurückgegeben, wenn das Gerät nicht wiedergegeben wurde oder kein Volume festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="c4827-643">This returns an error if the device has not been played or volume has not been set.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c4827-644">Fenster handle</span><span class="sxs-lookup"><span data-stu-id="c4827-644">window handle</span></span></td>
<td><span data-ttu-id="c4827-645">Gibt den ASCII-Dezimalwert für das Fenster Handle in dem nieder wertigen Wort des Rückgabewerts zurück.</span><span class="sxs-lookup"><span data-stu-id="c4827-645">Returns the ASCII decimal value for the window handle in the low-order word of the return value.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c4827-646">Fenster maximiert</span><span class="sxs-lookup"><span data-stu-id="c4827-646">window maximized</span></span></td>
<td><span data-ttu-id="c4827-647">Gibt " <strong>true</strong> " zurück, wenn das Fenster maximiert ist.</span><span class="sxs-lookup"><span data-stu-id="c4827-647">Returns <strong>TRUE</strong> if the window is maximized.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c4827-648">Fenster minimiert</span><span class="sxs-lookup"><span data-stu-id="c4827-648">window minimized</span></span></td>
<td><span data-ttu-id="c4827-649">Gibt <strong>true</strong> zurück, wenn das Fenster minimiert wird.</span><span class="sxs-lookup"><span data-stu-id="c4827-649">Returns <strong>TRUE</strong> if the window is minimized.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c4827-650">Fenster sichtbar</span><span class="sxs-lookup"><span data-stu-id="c4827-650">window visible</span></span></td>
<td><span data-ttu-id="c4827-651">Gibt " <strong>true</strong> " zurück, wenn das Fenster nicht ausgeblendet ist.</span><span class="sxs-lookup"><span data-stu-id="c4827-651">Returns <strong>TRUE</strong> if the window is not hidden.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c4827-652">schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c4827-652">write protected</span></span></td>
<td><span data-ttu-id="c4827-653">Gibt <strong>true</strong> zurück, wenn das Gerät erkennt, dass es nicht aufzeichnen kann (d. h., wenn der Schreibschutz auf ON fest liegt).</span><span class="sxs-lookup"><span data-stu-id="c4827-653">Returns <strong>TRUE</strong> if the device detects that it cannot record (that is, if the write protect is on).</span></span> <span data-ttu-id="c4827-654">Wenn er aufzeichnen kann, oder wenn er nicht ermitteln kann, ob er aufzeichnen kann (ohne tatsächlich zu schreiben), gibt der Treiber <strong>false</strong>zurück.</span><span class="sxs-lookup"><span data-stu-id="c4827-654">If it can record, or if it is unable to determine whether or not it can record (without actually writing), the driver returns <strong>FALSE</strong>.</span></span></td>
</tr>
</tbody>
</table>



 

</dd> <dt>

<span data-ttu-id="c4827-655"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszflags*</span><span class="sxs-lookup"><span data-stu-id="c4827-655"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="c4827-656">Kann "wait", "notify" oder beides sein.</span><span class="sxs-lookup"><span data-stu-id="c4827-656">Can be "wait", "notify", or both.</span></span> <span data-ttu-id="c4827-657">Für Digital Video-und VCR-Geräte kann auch "Test" angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="c4827-657">For digital-video and VCR devices, "test" can also be specified.</span></span> <span data-ttu-id="c4827-658">Weitere Informationen zu diesen Flags finden Sie [unter warte-, Benachrichtigungs-und testflags](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="c4827-658">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c4827-659">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c4827-659">Return Value</span></span>

<span data-ttu-id="c4827-660">Gibt Informationen im *lpszreturnstring* -Parameter von [**mciSendString**](/previous-versions//dd757161(v=vs.85))zurück.</span><span class="sxs-lookup"><span data-stu-id="c4827-660">Returns information in the *lpszReturnString* parameter of [**mciSendString**](/previous-versions//dd757161(v=vs.85)).</span></span> <span data-ttu-id="c4827-661">Die Informationen hängen vom Anforderungstyp ab.</span><span class="sxs-lookup"><span data-stu-id="c4827-661">The information is dependent on the request type.</span></span>

## <a name="remarks"></a><span data-ttu-id="c4827-662">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c4827-662">Remarks</span></span>

<span data-ttu-id="c4827-663">Vor dem Ausgeben von Befehlen, die Positionswerte verwenden, sollten Sie das gewünschte Zeitformat mithilfe des [Set](set.md) -Befehls festlegen.</span><span class="sxs-lookup"><span data-stu-id="c4827-663">Before issuing any commands that use position values, you should set the desired time format by using the [set](set.md) command.</span></span>

## <a name="examples"></a><span data-ttu-id="c4827-664">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c4827-664">Examples</span></span>

<span data-ttu-id="c4827-665">Mit dem folgenden Befehl wird der aktuelle Modus des Geräts "mysound" zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="c4827-665">The following command returns the current mode of the "mysound" device.</span></span>

``` syntax
status mysound mode
```

## <a name="requirements"></a><span data-ttu-id="c4827-666">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c4827-666">Requirements</span></span>



| <span data-ttu-id="c4827-667">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c4827-667">Requirement</span></span> | <span data-ttu-id="c4827-668">Wert</span><span class="sxs-lookup"><span data-stu-id="c4827-668">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="c4827-669">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c4827-669">Minimum supported client</span></span><br/> | <span data-ttu-id="c4827-670">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c4827-670">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="c4827-671">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c4827-671">Minimum supported server</span></span><br/> | <span data-ttu-id="c4827-672">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c4827-672">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="c4827-673">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c4827-673">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c4827-674">MCI</span><span class="sxs-lookup"><span data-stu-id="c4827-674">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="c4827-675">MCI-Befehls Zeichenfolgen</span><span class="sxs-lookup"><span data-stu-id="c4827-675">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> <dt>

[<span data-ttu-id="c4827-676">capability</span><span class="sxs-lookup"><span data-stu-id="c4827-676">capability</span></span>](capability.md)
</dt> <dt>

[<span data-ttu-id="c4827-677">einver</span><span class="sxs-lookup"><span data-stu-id="c4827-677">capture</span></span>](capture.md)
</dt> <dt>

[<span data-ttu-id="c4827-678">close</span><span class="sxs-lookup"><span data-stu-id="c4827-678">close</span></span>](close.md)
</dt> <dt>

[<span data-ttu-id="c4827-679">Schnitts</span><span class="sxs-lookup"><span data-stu-id="c4827-679">cut</span></span>](cut.md)
</dt> <dt>

[<span data-ttu-id="c4827-680">delete</span><span class="sxs-lookup"><span data-stu-id="c4827-680">delete</span></span>](delete.md)
</dt> <dt>

[<span data-ttu-id="c4827-681">Laden</span><span class="sxs-lookup"><span data-stu-id="c4827-681">load</span></span>](load.md)
</dt> <dt>

[<span data-ttu-id="c4827-682">pause</span><span class="sxs-lookup"><span data-stu-id="c4827-682">pause</span></span>](pause.md)
</dt> <dt>

[<span data-ttu-id="c4827-683">kle</span><span class="sxs-lookup"><span data-stu-id="c4827-683">paste</span></span>](paste.md)
</dt> <dt>

[<span data-ttu-id="c4827-684">record</span><span class="sxs-lookup"><span data-stu-id="c4827-684">record</span></span>](record.md)
</dt> <dt>

[<span data-ttu-id="c4827-685">Reserve</span><span class="sxs-lookup"><span data-stu-id="c4827-685">reserve</span></span>](reserve.md)
</dt> <dt>

[<span data-ttu-id="c4827-686">Speichern</span><span class="sxs-lookup"><span data-stu-id="c4827-686">save</span></span>](save.md)
</dt> <dt>

[<span data-ttu-id="c4827-687">set</span><span class="sxs-lookup"><span data-stu-id="c4827-687">set</span></span>](set.md)
</dt> <dt>

[<span data-ttu-id="c4827-688">setaudiodatei</span><span class="sxs-lookup"><span data-stu-id="c4827-688">setaudio</span></span>](setaudio.md)
</dt> <dt>

[<span data-ttu-id="c4827-689">setvideo</span><span class="sxs-lookup"><span data-stu-id="c4827-689">setvideo</span></span>](setvideo.md)
</dt> <dt>

[<span data-ttu-id="c4827-690">stop</span><span class="sxs-lookup"><span data-stu-id="c4827-690">stop</span></span>](stop.md)
</dt> <dt>

[<span data-ttu-id="c4827-691">Rückgängig</span><span class="sxs-lookup"><span data-stu-id="c4827-691">undo</span></span>](undo.md)
</dt> </dl>

 

