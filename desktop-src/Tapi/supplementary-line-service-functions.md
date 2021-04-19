---
description: Die Funktionen für den ergänzenden Zeilen Dienst sind in den folgenden Themen nach Kategorie aufgelistet.
ms.assetid: d4338b3c-cd84-4abb-b74e-9df895c8355b
title: Funktionen für ergänzende Zeilen Dienste
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21a29831369fd6b886d57cfae075b5b8bf7a83b2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106349850"
---
# <a name="supplementary-line-service-functions"></a><span data-ttu-id="eee1f-103">Funktionen für ergänzende Zeilen Dienste</span><span class="sxs-lookup"><span data-stu-id="eee1f-103">Supplementary Line Service Functions</span></span>

<span data-ttu-id="eee1f-104">Die Funktionen für den ergänzenden Zeilen Dienst sind in den folgenden Themen nach Kategorie aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="eee1f-104">The supplementary line service functions are listed by category in the following topics.</span></span> <span data-ttu-id="eee1f-105">Eine Funktion wird als [*asynchron*](a-tapgloss.md) identifiziert, wenn Sie die Vervollständigung in einer Antwortmeldung an die Anwendung angibt.</span><span class="sxs-lookup"><span data-stu-id="eee1f-105">A function is identified as [*asynchronous*](a-tapgloss.md) if it will indicate completion in a REPLY message to the application.</span></span> <span data-ttu-id="eee1f-106">Wenn die Funktion das Ergebnis immer sofort an die Anwendung zurückgibt, gilt die Funktion als [*synchron*](s-tapgloss.md).</span><span class="sxs-lookup"><span data-stu-id="eee1f-106">If the function always returns its result to the application immediately, the function is considered [*synchronous*](s-tapgloss.md).</span></span>

<span data-ttu-id="eee1f-107">Im folgenden finden Sie eine funktionale Gruppierung der Funktionen für den ergänzenden Zeilen Dienst:</span><span class="sxs-lookup"><span data-stu-id="eee1f-107">Following is a functional grouping of the supplementary line service functions:</span></span>

-   [<span data-ttu-id="eee1f-108">Agents</span><span class="sxs-lookup"><span data-stu-id="eee1f-108">Agents</span></span>](#agents)
-   [<span data-ttu-id="eee1f-109">Anwendungs Priorität</span><span class="sxs-lookup"><span data-stu-id="eee1f-109">Application priority</span></span>](#application-priority)
-   [<span data-ttu-id="eee1f-110">Bearermodus und-Rate</span><span class="sxs-lookup"><span data-stu-id="eee1f-110">Bearer mode and rate</span></span>](#bearer-mode-and-rate)
-   [<span data-ttu-id="eee1f-111">Akzeptieren und Umleiten von Anrufen</span><span class="sxs-lookup"><span data-stu-id="eee1f-111">Call accept and redirect</span></span>](#call-accept-and-redirect)
-   [<span data-ttu-id="eee1f-112">Rückruf Abschluss</span><span class="sxs-lookup"><span data-stu-id="eee1f-112">Call completion</span></span>](#call-completion)
-   [<span data-ttu-id="eee1f-113">Telefonkonferenz</span><span class="sxs-lookup"><span data-stu-id="eee1f-113">Call conference</span></span>](#call-conference)
-   [<span data-ttu-id="eee1f-114">Weiterleitungs Weiterleitung</span><span class="sxs-lookup"><span data-stu-id="eee1f-114">Call forwarding</span></span>](#call-forwarding)
-   [<span data-ttu-id="eee1f-115">Halt halten</span><span class="sxs-lookup"><span data-stu-id="eee1f-115">Call hold</span></span>](#call-hold)
-   [<span data-ttu-id="eee1f-116">Callpark</span><span class="sxs-lookup"><span data-stu-id="eee1f-116">Call park</span></span>](#call-park)
-   [<span data-ttu-id="eee1f-117">Abhol Anrufe</span><span class="sxs-lookup"><span data-stu-id="eee1f-117">Call pickup</span></span>](#call-pickup)
-   [<span data-ttu-id="eee1f-118">Rückruf ablehnen</span><span class="sxs-lookup"><span data-stu-id="eee1f-118">Call reject</span></span>](#call-reject)
-   [<span data-ttu-id="eee1f-119">Aufrufe übertragen</span><span class="sxs-lookup"><span data-stu-id="eee1f-119">Call transfer</span></span>](#call-transfer)
-   [<span data-ttu-id="eee1f-120">Ziffern Überwachung und-Erfassung</span><span class="sxs-lookup"><span data-stu-id="eee1f-120">Digit monitoring and gathering</span></span>](#digit-monitoring-and-gathering)
-   [<span data-ttu-id="eee1f-121">Erstellen von Inband-Ziffern und-Tönen</span><span class="sxs-lookup"><span data-stu-id="eee1f-121">Generating inband digits and tones</span></span>](#generating-inband-digits-and-tones)
-   [<span data-ttu-id="eee1f-122">Aufrufen</span><span class="sxs-lookup"><span data-stu-id="eee1f-122">Making calls</span></span>](basic-telephony-services-reference.md)
-   [<span data-ttu-id="eee1f-123">Mediensteuer Element</span><span class="sxs-lookup"><span data-stu-id="eee1f-123">Media control</span></span>](#media-control)
-   [<span data-ttu-id="eee1f-124">Medienüberwachung</span><span class="sxs-lookup"><span data-stu-id="eee1f-124">Media monitoring</span></span>](#media-monitoring)
-   [<span data-ttu-id="eee1f-125">Proxys</span><span class="sxs-lookup"><span data-stu-id="eee1f-125">Proxies</span></span>](#proxies)
-   [<span data-ttu-id="eee1f-126">Quality of Service (QoS, Dienstqualität)</span><span class="sxs-lookup"><span data-stu-id="eee1f-126">Quality of Service</span></span>](#quality-of-service)
-   [<span data-ttu-id="eee1f-127">Senden von Informationen an eine Remote Partei</span><span class="sxs-lookup"><span data-stu-id="eee1f-127">Sending information to remote party</span></span>](#sending-information-to-remote-party)
-   [<span data-ttu-id="eee1f-128">Verwaltung von Dienstanbietern</span><span class="sxs-lookup"><span data-stu-id="eee1f-128">Service provider management</span></span>](#service-provider-management)
-   [<span data-ttu-id="eee1f-129">Festlegen eines Terminals für Telefon Konversationen</span><span class="sxs-lookup"><span data-stu-id="eee1f-129">Setting a terminal for phone conversations</span></span>](#setting-a-terminal-for-phone-conversations)
-   [<span data-ttu-id="eee1f-130">Tone-Überwachung</span><span class="sxs-lookup"><span data-stu-id="eee1f-130">Tone monitoring</span></span>](#tone-monitoring)

<span data-ttu-id="eee1f-131">Es gibt auch [verschiedene](#miscellaneous) ergänzende Zeilen Dienstfunktionen.</span><span class="sxs-lookup"><span data-stu-id="eee1f-131">There are also [miscellaneous](#miscellaneous) supplementary line service functions.</span></span>

## <a name="bearer-mode-and-rate"></a><span data-ttu-id="eee1f-132">Bearermodus und-Rate</span><span class="sxs-lookup"><span data-stu-id="eee1f-132">Bearer Mode and Rate</span></span>



| <span data-ttu-id="eee1f-133">Funktion</span><span class="sxs-lookup"><span data-stu-id="eee1f-133">Function</span></span>                                       | <span data-ttu-id="eee1f-134">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="eee1f-134">Description</span></span>                                                                |
|------------------------------------------------|----------------------------------------------------------------------------|
| [<span data-ttu-id="eee1f-135">**linesetcallparametriams**</span><span class="sxs-lookup"><span data-stu-id="eee1f-135">**lineSetCallParams**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linesetcallparams) | <span data-ttu-id="eee1f-136">Fordert eine Änderung in den callparametern eines vorhandenen Aufrufes an.</span><span class="sxs-lookup"><span data-stu-id="eee1f-136">Requests a change in the call parameters of an existing call.</span></span> <span data-ttu-id="eee1f-137">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="eee1f-137">Synchronous.</span></span> |



 

## <a name="media-monitoring"></a><span data-ttu-id="eee1f-138">Medienüberwachung</span><span class="sxs-lookup"><span data-stu-id="eee1f-138">Media Monitoring</span></span>



| <span data-ttu-id="eee1f-139">Funktion</span><span class="sxs-lookup"><span data-stu-id="eee1f-139">Function</span></span>                                     | <span data-ttu-id="eee1f-140">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="eee1f-140">Description</span></span>                                                                   |
|----------------------------------------------|-------------------------------------------------------------------------------|
| [<span data-ttu-id="eee1f-141">**linemonitormedia**</span><span class="sxs-lookup"><span data-stu-id="eee1f-141">**lineMonitorMedia**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linemonitormedia) | <span data-ttu-id="eee1f-142">Aktiviert oder deaktiviert die Benachrichtigung im Medien Modus für einen angegebenen-Befehl.</span><span class="sxs-lookup"><span data-stu-id="eee1f-142">Enables or disables media mode notification on a specified call.</span></span> <span data-ttu-id="eee1f-143">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="eee1f-143">Synchronous.</span></span> |



 

## <a name="digit-monitoring-and-gathering"></a><span data-ttu-id="eee1f-144">Ziffern Überwachung und-Erfassung</span><span class="sxs-lookup"><span data-stu-id="eee1f-144">Digit Monitoring and Gathering</span></span>



| <span data-ttu-id="eee1f-145">Funktion</span><span class="sxs-lookup"><span data-stu-id="eee1f-145">Function</span></span>                                       | <span data-ttu-id="eee1f-146">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="eee1f-146">Description</span></span>                                                                        |
|------------------------------------------------|------------------------------------------------------------------------------------|
| [<span data-ttu-id="eee1f-147">**linemonitordigits**</span><span class="sxs-lookup"><span data-stu-id="eee1f-147">**lineMonitorDigits**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linemonitordigits) | <span data-ttu-id="eee1f-148">Aktiviert oder deaktiviert die Benachrichtigung über die Ziffern Erkennung für einen angegebenen-Befehl.</span><span class="sxs-lookup"><span data-stu-id="eee1f-148">Enables or disables digit detection notification on a specified call.</span></span> <span data-ttu-id="eee1f-149">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="eee1f-149">Synchronous.</span></span> |
| [<span data-ttu-id="eee1f-150">**linegather-Ziffern**</span><span class="sxs-lookup"><span data-stu-id="eee1f-150">**lineGatherDigits**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegatherdigits)   | <span data-ttu-id="eee1f-151">Führt die gepufferte Erfassung von Ziffern bei einem-Befehl aus.</span><span class="sxs-lookup"><span data-stu-id="eee1f-151">Performs the buffered gathering of digits on a call.</span></span> <span data-ttu-id="eee1f-152">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="eee1f-152">Synchronous.</span></span>                  |



 

## <a name="tone-monitoring"></a><span data-ttu-id="eee1f-153">Tone-Überwachung</span><span class="sxs-lookup"><span data-stu-id="eee1f-153">Tone Monitoring</span></span>



| <span data-ttu-id="eee1f-154">Funktion</span><span class="sxs-lookup"><span data-stu-id="eee1f-154">Function</span></span>                                     | <span data-ttu-id="eee1f-155">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="eee1f-155">Description</span></span>                                                       |
|----------------------------------------------|-------------------------------------------------------------------|
| [<span data-ttu-id="eee1f-156">**linemonitortones**</span><span class="sxs-lookup"><span data-stu-id="eee1f-156">**lineMonitorTones**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linemonitortones) | <span data-ttu-id="eee1f-157">Gibt an, welche Töne bei einem angegebenen-Befehl erkannt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="eee1f-157">Specifies which tones to detect on a specified call.</span></span> <span data-ttu-id="eee1f-158">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="eee1f-158">Synchronous.</span></span> |



 

## <a name="media-control"></a><span data-ttu-id="eee1f-159">Mediensteuer Element</span><span class="sxs-lookup"><span data-stu-id="eee1f-159">Media Control</span></span>



| <span data-ttu-id="eee1f-160">Funktion</span><span class="sxs-lookup"><span data-stu-id="eee1f-160">Function</span></span>                                           | <span data-ttu-id="eee1f-161">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="eee1f-161">Description</span></span>                                                                                                          |
|----------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="eee1f-162">**linesetmediacontrol**</span><span class="sxs-lookup"><span data-stu-id="eee1f-162">**lineSetMediaControl**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linesetmediacontrol) | <span data-ttu-id="eee1f-163">Richtet den Mediendaten Strom eines Aufrufes für das mediensteuer Element ein.</span><span class="sxs-lookup"><span data-stu-id="eee1f-163">Sets up a call's media stream for media control.</span></span> <span data-ttu-id="eee1f-164">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="eee1f-164">Synchronous.</span></span>                                                        |
| [<span data-ttu-id="eee1f-165">**linesetmediamode**</span><span class="sxs-lookup"><span data-stu-id="eee1f-165">**lineSetMediaMode**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linesetmediamode)       | <span data-ttu-id="eee1f-166">Legt die Medien Modi des angegebenen Aufrufes in der [**LINECALLINFO**](/windows/desktop/api/Tapi/ns-tapi-linecallinfo) -Struktur fest.</span><span class="sxs-lookup"><span data-stu-id="eee1f-166">Sets the media mode(s) of the specified call in its [**LINECALLINFO**](/windows/desktop/api/Tapi/ns-tapi-linecallinfo) structure.</span></span> <span data-ttu-id="eee1f-167">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="eee1f-167">Synchronous.</span></span> |



 

## <a name="generating-inband-digits-and-tones"></a><span data-ttu-id="eee1f-168">Erstellen von Inband-Ziffern und-Tönen</span><span class="sxs-lookup"><span data-stu-id="eee1f-168">Generating Inband Digits and Tones</span></span>



| <span data-ttu-id="eee1f-169">Funktion</span><span class="sxs-lookup"><span data-stu-id="eee1f-169">Function</span></span>                                         | <span data-ttu-id="eee1f-170">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="eee1f-170">Description</span></span>                                                   |
|--------------------------------------------------|---------------------------------------------------------------|
| [<span data-ttu-id="eee1f-171">**linegeneratedigits**</span><span class="sxs-lookup"><span data-stu-id="eee1f-171">**lineGenerateDigits**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegeneratedigits) | <span data-ttu-id="eee1f-172">Generiert bei einem-aufrufzeichen inbandziffern.</span><span class="sxs-lookup"><span data-stu-id="eee1f-172">Generates inband digits on a call.</span></span> <span data-ttu-id="eee1f-173">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="eee1f-173">Synchronous.</span></span>               |
| [<span data-ttu-id="eee1f-174">**linegeneratetone**</span><span class="sxs-lookup"><span data-stu-id="eee1f-174">**lineGenerateTone**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegeneratetone)     | <span data-ttu-id="eee1f-175">Generiert einen angegebenen Satz von Tönen bei einem-Befehl in Inband.</span><span class="sxs-lookup"><span data-stu-id="eee1f-175">Generates a given set of tones inband on a call.</span></span> <span data-ttu-id="eee1f-176">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="eee1f-176">Synchronous.</span></span> |



 

## <a name="call-accept-and-redirect"></a><span data-ttu-id="eee1f-177">Akzeptieren und Umleiten von Anrufen</span><span class="sxs-lookup"><span data-stu-id="eee1f-177">Call Accept and Redirect</span></span>



| <span data-ttu-id="eee1f-178">Funktion</span><span class="sxs-lookup"><span data-stu-id="eee1f-178">Function</span></span>                             | <span data-ttu-id="eee1f-179">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="eee1f-179">Description</span></span>                                                                                               |
|--------------------------------------|-----------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="eee1f-180">**lineaccept**</span><span class="sxs-lookup"><span data-stu-id="eee1f-180">**lineAccept**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineaccept)     | <span data-ttu-id="eee1f-181">Akzeptiert einen angebotenen Aufruf und beginnt mit der Warnung des Aufrufers (Ringback) und der sogenannten Partei (Ring).</span><span class="sxs-lookup"><span data-stu-id="eee1f-181">Accepts an offered call and starts alerting both caller (ringback) and called party (ring).</span></span> <span data-ttu-id="eee1f-182">Asynchron.</span><span class="sxs-lookup"><span data-stu-id="eee1f-182">Asynchronous.</span></span> |
| [<span data-ttu-id="eee1f-183">**lineredirect**</span><span class="sxs-lookup"><span data-stu-id="eee1f-183">**lineRedirect**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineredirect) | <span data-ttu-id="eee1f-184">Leitet einen Angebots Rückruf an eine andere Adresse um.</span><span class="sxs-lookup"><span data-stu-id="eee1f-184">Redirects an offering call to another address.</span></span> <span data-ttu-id="eee1f-185">Asynchron.</span><span class="sxs-lookup"><span data-stu-id="eee1f-185">Asynchronous.</span></span>                                              |



 

## <a name="call-reject"></a><span data-ttu-id="eee1f-186">Rückruf ablehnen</span><span class="sxs-lookup"><span data-stu-id="eee1f-186">Call Reject</span></span>



| <span data-ttu-id="eee1f-187">Funktion</span><span class="sxs-lookup"><span data-stu-id="eee1f-187">Function</span></span>                     | <span data-ttu-id="eee1f-188">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="eee1f-188">Description</span></span>                                                               |
|------------------------------|---------------------------------------------------------------------------|
| [<span data-ttu-id="eee1f-189">**linedrop**</span><span class="sxs-lookup"><span data-stu-id="eee1f-189">**lineDrop**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linedrop) | <span data-ttu-id="eee1f-190">Trennt einen-Befehl oder bricht einen aufzurufenden Versuch ab.</span><span class="sxs-lookup"><span data-stu-id="eee1f-190">Disconnects a call, or abandons a call attempt in progress.</span></span> <span data-ttu-id="eee1f-191">Asynchron.</span><span class="sxs-lookup"><span data-stu-id="eee1f-191">Asynchronous.</span></span> |



 

## <a name="call-hold"></a><span data-ttu-id="eee1f-192">Halt halten</span><span class="sxs-lookup"><span data-stu-id="eee1f-192">Call Hold</span></span>



| <span data-ttu-id="eee1f-193">Funktion</span><span class="sxs-lookup"><span data-stu-id="eee1f-193">Function</span></span>                         | <span data-ttu-id="eee1f-194">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="eee1f-194">Description</span></span>                                           |
|----------------------------------|-------------------------------------------------------|
| [<span data-ttu-id="eee1f-195">**linehold**</span><span class="sxs-lookup"><span data-stu-id="eee1f-195">**lineHold**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linehold)     | <span data-ttu-id="eee1f-196">Platziert den angegebenen-aufrufungs-.</span><span class="sxs-lookup"><span data-stu-id="eee1f-196">Places the specified call on hard hold.</span></span> <span data-ttu-id="eee1f-197">Asynchron.</span><span class="sxs-lookup"><span data-stu-id="eee1f-197">Asynchronous.</span></span> |
| [<span data-ttu-id="eee1f-198">**lineunhold**</span><span class="sxs-lookup"><span data-stu-id="eee1f-198">**lineUnhold**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineunhold) | <span data-ttu-id="eee1f-199">Ruft einen gehaltenen-Befehl ab.</span><span class="sxs-lookup"><span data-stu-id="eee1f-199">Retrieves a held call.</span></span> <span data-ttu-id="eee1f-200">Asynchron.</span><span class="sxs-lookup"><span data-stu-id="eee1f-200">Asynchronous.</span></span>                  |



 

## <a name="securing-calls"></a><span data-ttu-id="eee1f-201">Sichern von Aufrufen</span><span class="sxs-lookup"><span data-stu-id="eee1f-201">Securing Calls</span></span>



| <span data-ttu-id="eee1f-202">Funktion</span><span class="sxs-lookup"><span data-stu-id="eee1f-202">Function</span></span>                                 | <span data-ttu-id="eee1f-203">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="eee1f-203">Description</span></span>                                                                                                              |
|------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="eee1f-204">**linesecurecall**</span><span class="sxs-lookup"><span data-stu-id="eee1f-204">**lineSecureCall**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linesecurecall) | <span data-ttu-id="eee1f-205">Sichert einen vorhandenen-Rückruf von Störungen durch andere Ereignisse wie z. b. Aufrufe, die auf Datenverbindungen warten.</span><span class="sxs-lookup"><span data-stu-id="eee1f-205">Secures an existing call from interference by other events such as call-waiting beeps on data connections.</span></span> <span data-ttu-id="eee1f-206">Asynchron.</span><span class="sxs-lookup"><span data-stu-id="eee1f-206">Asynchronous.</span></span> |



 

## <a name="call-transfer"></a><span data-ttu-id="eee1f-207">Aufrufe übertragen</span><span class="sxs-lookup"><span data-stu-id="eee1f-207">Call Transfer</span></span>



| <span data-ttu-id="eee1f-208">Funktion</span><span class="sxs-lookup"><span data-stu-id="eee1f-208">Function</span></span>                                             | <span data-ttu-id="eee1f-209">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="eee1f-209">Description</span></span>                                                                                                    |
|------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="eee1f-210">**lineSetupTransfer**</span><span class="sxs-lookup"><span data-stu-id="eee1f-210">**lineSetupTransfer**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linesetuptransfer)       | <span data-ttu-id="eee1f-211">Bereitet einen angegebenen-Befehl für die Übertragung an eine andere Adresse vor.</span><span class="sxs-lookup"><span data-stu-id="eee1f-211">Prepares a specified call for transfer to another address.</span></span> <span data-ttu-id="eee1f-212">Asynchron.</span><span class="sxs-lookup"><span data-stu-id="eee1f-212">Asynchronous.</span></span>                                       |
| [<span data-ttu-id="eee1f-213">**linecompletetransfer**</span><span class="sxs-lookup"><span data-stu-id="eee1f-213">**lineCompleteTransfer**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linecompletetransfer) | <span data-ttu-id="eee1f-214">Überträgt einen aufgerufen, der für die Übertragung an einen anderen-Befehl eingerichtet wurde, oder wechselt in eine drei-Wege-Konferenz.</span><span class="sxs-lookup"><span data-stu-id="eee1f-214">Transfers a call that was set up for transfer to another call, or enters a three-way conference.</span></span> <span data-ttu-id="eee1f-215">Asynchron.</span><span class="sxs-lookup"><span data-stu-id="eee1f-215">Asynchronous.</span></span> |
| [<span data-ttu-id="eee1f-216">**lineblintransfer**</span><span class="sxs-lookup"><span data-stu-id="eee1f-216">**lineBlindTransfer**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineblindtransfer)       | <span data-ttu-id="eee1f-217">Überträgt einen-Rückruf an eine andere Partei.</span><span class="sxs-lookup"><span data-stu-id="eee1f-217">Transfers a call to another party.</span></span> <span data-ttu-id="eee1f-218">Asynchron.</span><span class="sxs-lookup"><span data-stu-id="eee1f-218">Asynchronous.</span></span>                                                               |
| [<span data-ttu-id="eee1f-219">**lineswaphold**</span><span class="sxs-lookup"><span data-stu-id="eee1f-219">**lineSwapHold**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineswaphold)                 | <span data-ttu-id="eee1f-220">Vertauscht den aktiven-Befehl mit dem derzeit bei der Beratung angehaltenen-Rückruf.</span><span class="sxs-lookup"><span data-stu-id="eee1f-220">Swaps the active call with the call currently on consultation hold.</span></span> <span data-ttu-id="eee1f-221">Asynchron.</span><span class="sxs-lookup"><span data-stu-id="eee1f-221">Asynchronous.</span></span>                              |



 

## <a name="call-conference"></a><span data-ttu-id="eee1f-222">Telefonkonferenz</span><span class="sxs-lookup"><span data-stu-id="eee1f-222">Call Conference</span></span>



| <span data-ttu-id="eee1f-223">Funktion</span><span class="sxs-lookup"><span data-stu-id="eee1f-223">Function</span></span>                                                         | <span data-ttu-id="eee1f-224">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="eee1f-224">Description</span></span>                                                                                                                                                                                          |
|------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="eee1f-225">**linesetupconference**</span><span class="sxs-lookup"><span data-stu-id="eee1f-225">**lineSetupConference**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linesetupconference)               | <span data-ttu-id="eee1f-226">Bereitet einen angegebenen-Rückruf für das Hinzufügen einer anderen Partei vor.</span><span class="sxs-lookup"><span data-stu-id="eee1f-226">Prepares a given call for the addition of another party.</span></span> <span data-ttu-id="eee1f-227">Asynchron.</span><span class="sxs-lookup"><span data-stu-id="eee1f-227">Asynchronous.</span></span>                                                                                                                               |
| [<span data-ttu-id="eee1f-228">**lineprepareaddumconference**</span><span class="sxs-lookup"><span data-stu-id="eee1f-228">**linePrepareAddToConference**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineprepareaddtoconference) | <span data-ttu-id="eee1f-229">Bereitet das Hinzufügen einer Partei zu einem bestehenden Konferenzgespräch vor, indem der Konferenzanrufe in den Status "Hold" versetzt und ein Rückruf aufgerufen wird, der später dem Konferenztelefon hinzugefügt werden kann.</span><span class="sxs-lookup"><span data-stu-id="eee1f-229">Prepares to add a party to an existing conference call by placing the conference call in a hold state and creating a consultation call that can be added later to the conference call.</span></span> <span data-ttu-id="eee1f-230">Asynchron.</span><span class="sxs-lookup"><span data-stu-id="eee1f-230">Asynchronous.</span></span> |
| [<span data-ttu-id="eee1f-231">**lineaddumconference**</span><span class="sxs-lookup"><span data-stu-id="eee1f-231">**lineAddToConference**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineaddtoconference)               | <span data-ttu-id="eee1f-232">Fügt einen Rückruf für einen vorhandenen Konferenz Rückruf hinzu.</span><span class="sxs-lookup"><span data-stu-id="eee1f-232">Adds a consultation call to an existing conference call.</span></span> <span data-ttu-id="eee1f-233">Asynchron.</span><span class="sxs-lookup"><span data-stu-id="eee1f-233">Asynchronous.</span></span>                                                                                                                               |
| [<span data-ttu-id="eee1f-234">**lineremovefromconference**</span><span class="sxs-lookup"><span data-stu-id="eee1f-234">**lineRemoveFromConference**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineremovefromconference)     | <span data-ttu-id="eee1f-235">Entfernt eine Partei aus einem Konferenzgespräch.</span><span class="sxs-lookup"><span data-stu-id="eee1f-235">Removes a party from a conference call.</span></span> <span data-ttu-id="eee1f-236">Asynchron.</span><span class="sxs-lookup"><span data-stu-id="eee1f-236">Asynchronous.</span></span>                                                                                                                                                |



 

## <a name="call-park"></a><span data-ttu-id="eee1f-237">Callpark</span><span class="sxs-lookup"><span data-stu-id="eee1f-237">Call Park</span></span>



| <span data-ttu-id="eee1f-238">Funktion</span><span class="sxs-lookup"><span data-stu-id="eee1f-238">Function</span></span>                         | <span data-ttu-id="eee1f-239">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="eee1f-239">Description</span></span>                                          |
|----------------------------------|------------------------------------------------------|
| [<span data-ttu-id="eee1f-240">**linepark**</span><span class="sxs-lookup"><span data-stu-id="eee1f-240">**linePark**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linepark)     | <span data-ttu-id="eee1f-241">In wird ein angegebener-Rückruf an einer anderen Adresse</span><span class="sxs-lookup"><span data-stu-id="eee1f-241">Parks a given call at another address.</span></span> <span data-ttu-id="eee1f-242">Asynchron.</span><span class="sxs-lookup"><span data-stu-id="eee1f-242">Asynchronous.</span></span> |
| [<span data-ttu-id="eee1f-243">**lineunpark**</span><span class="sxs-lookup"><span data-stu-id="eee1f-243">**lineUnpark**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineunpark) | <span data-ttu-id="eee1f-244">Ruft einen geparkten-Befehl ab.</span><span class="sxs-lookup"><span data-stu-id="eee1f-244">Retrieves a parked call.</span></span> <span data-ttu-id="eee1f-245">Asynchron.</span><span class="sxs-lookup"><span data-stu-id="eee1f-245">Asynchronous.</span></span>               |



 

## <a name="call-forwarding"></a><span data-ttu-id="eee1f-246">Weiterleitungs Weiterleitung</span><span class="sxs-lookup"><span data-stu-id="eee1f-246">Call Forwarding</span></span>



| <span data-ttu-id="eee1f-247">Funktion</span><span class="sxs-lookup"><span data-stu-id="eee1f-247">Function</span></span>                           | <span data-ttu-id="eee1f-248">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="eee1f-248">Description</span></span>                                             |
|------------------------------------|---------------------------------------------------------|
| [<span data-ttu-id="eee1f-249">**lineforward**</span><span class="sxs-lookup"><span data-stu-id="eee1f-249">**lineForward**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineforward) | <span data-ttu-id="eee1f-250">Legt Anforderungs Weiterleitungs Anforderungen fest oder bricht Sie ab.</span><span class="sxs-lookup"><span data-stu-id="eee1f-250">Sets or cancels call forwarding requests.</span></span> <span data-ttu-id="eee1f-251">Asynchron.</span><span class="sxs-lookup"><span data-stu-id="eee1f-251">Asynchronous.</span></span> |



 

## <a name="call-pickup"></a><span data-ttu-id="eee1f-252">Abhol Anrufe</span><span class="sxs-lookup"><span data-stu-id="eee1f-252">Call Pickup</span></span>



| <span data-ttu-id="eee1f-253">Funktion</span><span class="sxs-lookup"><span data-stu-id="eee1f-253">Function</span></span>                         | <span data-ttu-id="eee1f-254">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="eee1f-254">Description</span></span>                                                                                                                                                                                      |
|----------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="eee1f-255">**linepickup**</span><span class="sxs-lookup"><span data-stu-id="eee1f-255">**linePickup**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linepickup) | <span data-ttu-id="eee1f-256">Ruft eine aufrufswarnung an einer angegebenen Zieladresse ab und gibt ein-Rückruf Handle für den aufzurufenden-Befehl zurück ([**linepickup**](/windows/desktop/api/Tapi/nf-tapi-linepickup) kann auch für das warten auf Aufrufe verwendet werden).</span><span class="sxs-lookup"><span data-stu-id="eee1f-256">Picks up a call alerting at a specified destination address and returns a call handle for the picked-up call ([**linePickup**](/windows/desktop/api/Tapi/nf-tapi-linepickup) can also be used for call waiting).</span></span> <span data-ttu-id="eee1f-257">Asynchron.</span><span class="sxs-lookup"><span data-stu-id="eee1f-257">Asynchronous.</span></span> |



 

## <a name="sending-information-to-remote-party"></a><span data-ttu-id="eee1f-258">Senden von Informationen an eine Remote Partei</span><span class="sxs-lookup"><span data-stu-id="eee1f-258">Sending Information to Remote Party</span></span>



| <span data-ttu-id="eee1f-259">Funktion</span><span class="sxs-lookup"><span data-stu-id="eee1f-259">Function</span></span>                                                   | <span data-ttu-id="eee1f-260">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="eee1f-260">Description</span></span>                                                                                                         |
|------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="eee1f-261">**linereleaseuseruserinfo**</span><span class="sxs-lookup"><span data-stu-id="eee1f-261">**lineReleaseUserUserInfo**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linereleaseuseruserinfo) | <span data-ttu-id="eee1f-262">Gibt Benutzer Benutzerinformationen frei und ermöglicht dem System, diesen Speicher mit neuen Informationen zu überschreiben.</span><span class="sxs-lookup"><span data-stu-id="eee1f-262">Releases user-user information, permitting the system to overwrite this storage with new information.</span></span> <span data-ttu-id="eee1f-263">Asynchron.</span><span class="sxs-lookup"><span data-stu-id="eee1f-263">Asynchronous.</span></span> |
| [<span data-ttu-id="eee1f-264">**linesenduseruserinfo**</span><span class="sxs-lookup"><span data-stu-id="eee1f-264">**lineSendUserUserInfo**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linesenduseruserinfo)       | <span data-ttu-id="eee1f-265">Sendet Benutzer Benutzerinformationen für den angegebenen-Befehl an die Remote Partei.</span><span class="sxs-lookup"><span data-stu-id="eee1f-265">Sends user-user information to the remote party on the specified call.</span></span> <span data-ttu-id="eee1f-266">Asynchron.</span><span class="sxs-lookup"><span data-stu-id="eee1f-266">Asynchronous.</span></span>                                |



 

## <a name="call-completion"></a><span data-ttu-id="eee1f-267">Rückruf Abschluss</span><span class="sxs-lookup"><span data-stu-id="eee1f-267">Call Completion</span></span>



| <span data-ttu-id="eee1f-268">Funktion</span><span class="sxs-lookup"><span data-stu-id="eee1f-268">Function</span></span>                                         | <span data-ttu-id="eee1f-269">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="eee1f-269">Description</span></span>                                      |
|--------------------------------------------------|--------------------------------------------------|
| [<span data-ttu-id="eee1f-270">**linecompletecall**</span><span class="sxs-lookup"><span data-stu-id="eee1f-270">**lineCompleteCall**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linecompletecall)     | <span data-ttu-id="eee1f-271">Fügt eine Anforderung zum Abschluss der Anforderung ein.</span><span class="sxs-lookup"><span data-stu-id="eee1f-271">Places a call completion request.</span></span> <span data-ttu-id="eee1f-272">Asynchron.</span><span class="sxs-lookup"><span data-stu-id="eee1f-272">Asynchronous.</span></span>  |
| [<span data-ttu-id="eee1f-273">**lineuncompletecall**</span><span class="sxs-lookup"><span data-stu-id="eee1f-273">**lineUncompleteCall**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineuncompletecall) | <span data-ttu-id="eee1f-274">Bricht eine Anforderung zum Abschließen des Aufrufes ab.</span><span class="sxs-lookup"><span data-stu-id="eee1f-274">Cancels a call completion request.</span></span> <span data-ttu-id="eee1f-275">Asynchron.</span><span class="sxs-lookup"><span data-stu-id="eee1f-275">Asynchronous.</span></span> |



 

## <a name="setting-a-terminal-for-phone-conversations"></a><span data-ttu-id="eee1f-276">Festlegen eines Terminals für Telefon Konversationen</span><span class="sxs-lookup"><span data-stu-id="eee1f-276">Setting a Terminal for Phone Conversations</span></span>



| <span data-ttu-id="eee1f-277">Funktion</span><span class="sxs-lookup"><span data-stu-id="eee1f-277">Function</span></span>                                   | <span data-ttu-id="eee1f-278">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="eee1f-278">Description</span></span>                                                                                                                      |
|--------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="eee1f-279">**linesetterminal**</span><span class="sxs-lookup"><span data-stu-id="eee1f-279">**lineSetTerminal**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linesetterminal) | <span data-ttu-id="eee1f-280">Gibt das Terminal Gerät an, an das die angegebene Zeile, die Adress Ereignisse oder die Ereignisse zum Abrufen von Medienströmen weitergeleitet werden.</span><span class="sxs-lookup"><span data-stu-id="eee1f-280">Specifies the terminal device to which the specified line, address events, or call media stream events are routed.</span></span> <span data-ttu-id="eee1f-281">Asynchron.</span><span class="sxs-lookup"><span data-stu-id="eee1f-281">Asynchronous.</span></span> |



 

## <a name="application-priority"></a><span data-ttu-id="eee1f-282">Anwendungs Priorität</span><span class="sxs-lookup"><span data-stu-id="eee1f-282">Application Priority</span></span>



| <span data-ttu-id="eee1f-283">Funktion</span><span class="sxs-lookup"><span data-stu-id="eee1f-283">Function</span></span>                                         | <span data-ttu-id="eee1f-284">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="eee1f-284">Description</span></span>                                                                                       |
|--------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="eee1f-285">**linegetapppriority**</span><span class="sxs-lookup"><span data-stu-id="eee1f-285">**lineGetAppPriority**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetapppriority) | <span data-ttu-id="eee1f-286">Ruft die Informationen zur Übergabe und/oder zur unterstützten telefoniepriorität für eine Anwendung ab.</span><span class="sxs-lookup"><span data-stu-id="eee1f-286">Retrieves handoff and/or Assisted Telephony priority information for an application.</span></span> <span data-ttu-id="eee1f-287">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="eee1f-287">Synchronous.</span></span> |
| [<span data-ttu-id="eee1f-288">**linesetapppriority**</span><span class="sxs-lookup"><span data-stu-id="eee1f-288">**lineSetAppPriority**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linesetapppriority) | <span data-ttu-id="eee1f-289">Legt die Übergabe und/oder die unterstützte telefoniepriorität für eine Anwendung fest.</span><span class="sxs-lookup"><span data-stu-id="eee1f-289">Sets the handoff and/or Assisted Telephony priority for an application.</span></span> <span data-ttu-id="eee1f-290">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="eee1f-290">Synchronous.</span></span>              |



 

## <a name="service-provider-management"></a><span data-ttu-id="eee1f-291">Verwaltung von Dienstanbietern</span><span class="sxs-lookup"><span data-stu-id="eee1f-291">Service Provider Management</span></span>



| <span data-ttu-id="eee1f-292">Funktion</span><span class="sxs-lookup"><span data-stu-id="eee1f-292">Function</span></span>                                           | <span data-ttu-id="eee1f-293">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="eee1f-293">Description</span></span>                                                           |
|----------------------------------------------------|-----------------------------------------------------------------------|
| [<span data-ttu-id="eee1f-294">**lineaddprovider**</span><span class="sxs-lookup"><span data-stu-id="eee1f-294">**lineAddProvider**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineaddprovider)         | <span data-ttu-id="eee1f-295">Installiert einen Telefoniedienstanbieter.</span><span class="sxs-lookup"><span data-stu-id="eee1f-295">Installs a telephony service provider.</span></span> <span data-ttu-id="eee1f-296">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="eee1f-296">Synchronous.</span></span>                   |
| [<span data-ttu-id="eee1f-297">**lineconfigprovider**</span><span class="sxs-lookup"><span data-stu-id="eee1f-297">**lineConfigProvider**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineconfigprovider)   | <span data-ttu-id="eee1f-298">Zeigt das Konfigurations Dialogfeld eines Dienstanbieters an.</span><span class="sxs-lookup"><span data-stu-id="eee1f-298">Displays configuration dialog box of a service provider.</span></span> <span data-ttu-id="eee1f-299">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="eee1f-299">Synchronous.</span></span> |
| [<span data-ttu-id="eee1f-300">**lineremoveprovider**</span><span class="sxs-lookup"><span data-stu-id="eee1f-300">**lineRemoveProvider**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineremoveprovider)   | <span data-ttu-id="eee1f-301">Entfernt einen vorhandenen Telefoniedienstanbieter.</span><span class="sxs-lookup"><span data-stu-id="eee1f-301">Removes an existing telephony service provider.</span></span> <span data-ttu-id="eee1f-302">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="eee1f-302">Synchronous.</span></span>          |
| [<span data-ttu-id="eee1f-303">**linegetproviderlist**</span><span class="sxs-lookup"><span data-stu-id="eee1f-303">**lineGetProviderList**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetproviderlist) | <span data-ttu-id="eee1f-304">Ruft eine Liste installierter Dienstanbieter ab.</span><span class="sxs-lookup"><span data-stu-id="eee1f-304">Retrieves a list of installed service providers.</span></span> <span data-ttu-id="eee1f-305">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="eee1f-305">Synchronous.</span></span>         |



 

## <a name="agents"></a><span data-ttu-id="eee1f-306">Agents</span><span class="sxs-lookup"><span data-stu-id="eee1f-306">Agents</span></span>



| <span data-ttu-id="eee1f-307">Funktion</span><span class="sxs-lookup"><span data-stu-id="eee1f-307">Function</span></span>                                                     | <span data-ttu-id="eee1f-308">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="eee1f-308">Description</span></span>                                                                                                                             |
|--------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="eee1f-309">**lineagentspecific**</span><span class="sxs-lookup"><span data-stu-id="eee1f-309">**lineAgentSpecific**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineagentspecific)               | <span data-ttu-id="eee1f-310">Ermöglicht der Anwendung den Zugriff auf proprietäre handlerspezifische Funktionen des mit der Adresse verknüpften Agent-Handlers.</span><span class="sxs-lookup"><span data-stu-id="eee1f-310">Allows the application to access proprietary handler-specific functions of the agent handler associated with the address.</span></span> <span data-ttu-id="eee1f-311">Asynchron.</span><span class="sxs-lookup"><span data-stu-id="eee1f-311">Asynchronous.</span></span> |
| [<span data-ttu-id="eee1f-312">**linegetagentactivitylist**</span><span class="sxs-lookup"><span data-stu-id="eee1f-312">**lineGetAgentActivityList**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetagentactivitylista) | <span data-ttu-id="eee1f-313">Ruft die Liste der Aktivitäten ab, von denen eine Anwendung die Funktionen auswählt, die ein Agent ausführt.</span><span class="sxs-lookup"><span data-stu-id="eee1f-313">Obtains the list of activities from which an application selects the functions an agent is performing.</span></span> <span data-ttu-id="eee1f-314">Asynchron.</span><span class="sxs-lookup"><span data-stu-id="eee1f-314">Asynchronous.</span></span>                    |
| [<span data-ttu-id="eee1f-315">**linegetagentcaps**</span><span class="sxs-lookup"><span data-stu-id="eee1f-315">**lineGetAgentCaps**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetagentcapsa)                 | <span data-ttu-id="eee1f-316">Ruft die agentbezogenen Funktionen ab, die auf dem angegebenen Zeilen Gerät unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="eee1f-316">Obtains the agent-related capabilities supported on the specified line device.</span></span> <span data-ttu-id="eee1f-317">Asynchron.</span><span class="sxs-lookup"><span data-stu-id="eee1f-317">Asynchronous.</span></span>                                            |
| [<span data-ttu-id="eee1f-318">**linegetagentgrouplist**</span><span class="sxs-lookup"><span data-stu-id="eee1f-318">**lineGetAgentGroupList**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetagentgrouplista)       | <span data-ttu-id="eee1f-319">Ruft die Liste der Agentgruppen ab, in denen sich ein Agent auf dem automatischen-Anrufs anmelden kann.</span><span class="sxs-lookup"><span data-stu-id="eee1f-319">Obtains the list of agent groups into which an agent can log into on the automatic call distributor.</span></span> <span data-ttu-id="eee1f-320">Asynchron.</span><span class="sxs-lookup"><span data-stu-id="eee1f-320">Asynchronous.</span></span>                      |
| [<span data-ttu-id="eee1f-321">**linegetagentstatus**</span><span class="sxs-lookup"><span data-stu-id="eee1f-321">**lineGetAgentStatus**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetagentstatusa)             | <span data-ttu-id="eee1f-322">Ruft den agentbezogenen Status für die angegebene Adresse ab.</span><span class="sxs-lookup"><span data-stu-id="eee1f-322">Obtains the agent-related status on the specified address.</span></span> <span data-ttu-id="eee1f-323">Asynchron.</span><span class="sxs-lookup"><span data-stu-id="eee1f-323">Asynchronous.</span></span>                                                                |
| [<span data-ttu-id="eee1f-324">**linesetagentactivity**</span><span class="sxs-lookup"><span data-stu-id="eee1f-324">**lineSetAgentActivity**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linesetagentactivity)         | <span data-ttu-id="eee1f-325">Legt den Agent-Aktivitäts Code fest, der einer bestimmten Adresse zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="eee1f-325">Sets the agent activity code associated with a particular address.</span></span> <span data-ttu-id="eee1f-326">Asynchron.</span><span class="sxs-lookup"><span data-stu-id="eee1f-326">Asynchronous.</span></span>                                                        |
| [<span data-ttu-id="eee1f-327">**linesetagentgroup**</span><span class="sxs-lookup"><span data-stu-id="eee1f-327">**lineSetAgentGroup**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linesetagentgroup)               | <span data-ttu-id="eee1f-328">Legt die Agentgruppen fest, bei denen der Agent bei einer bestimmten Adresse angemeldet ist.</span><span class="sxs-lookup"><span data-stu-id="eee1f-328">Sets the agent groups that the agent is logged into on a particular address.</span></span> <span data-ttu-id="eee1f-329">Asynchron.</span><span class="sxs-lookup"><span data-stu-id="eee1f-329">Asynchronous.</span></span>                                              |
| [<span data-ttu-id="eee1f-330">**linesetagentstate**</span><span class="sxs-lookup"><span data-stu-id="eee1f-330">**lineSetAgentState**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linesetagentstate)               | <span data-ttu-id="eee1f-331">Legt den Agent-Status fest, der einer bestimmten Adresse zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="eee1f-331">Sets the agent state associated with a particular address.</span></span> <span data-ttu-id="eee1f-332">Asynchron.</span><span class="sxs-lookup"><span data-stu-id="eee1f-332">Asynchronous.</span></span>                                                                |



 

## <a name="proxies"></a><span data-ttu-id="eee1f-333">Proxys</span><span class="sxs-lookup"><span data-stu-id="eee1f-333">Proxies</span></span>



| <span data-ttu-id="eee1f-334">Funktion</span><span class="sxs-lookup"><span data-stu-id="eee1f-334">Function</span></span>                                       | <span data-ttu-id="eee1f-335">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="eee1f-335">Description</span></span>                                                                         |
|------------------------------------------------|-------------------------------------------------------------------------------------|
| [<span data-ttu-id="eee1f-336">**lineproxymess**</span><span class="sxs-lookup"><span data-stu-id="eee1f-336">**lineProxyMessage**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineproxymessage)   | <span data-ttu-id="eee1f-337">Wird von einem registrierten Proxy Anforderungs Handler zum Generieren von TAPI-Nachrichten verwendet.</span><span class="sxs-lookup"><span data-stu-id="eee1f-337">Used by a registered proxy request handler to generate TAPI messages.</span></span> <span data-ttu-id="eee1f-338">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="eee1f-338">Synchronous.</span></span>  |
| [<span data-ttu-id="eee1f-339">**lineproxyresponse**</span><span class="sxs-lookup"><span data-stu-id="eee1f-339">**lineProxyResponse**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineproxyresponse) | <span data-ttu-id="eee1f-340">Gibt den Abschluss einer Proxy Anforderung durch einen registrierten Proxy Handler an.</span><span class="sxs-lookup"><span data-stu-id="eee1f-340">Indicates completion of a proxy request by a registered proxy handler.</span></span> <span data-ttu-id="eee1f-341">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="eee1f-341">Synchronous.</span></span> |



 

## <a name="quality-of-service"></a><span data-ttu-id="eee1f-342">Quality of Service (QoS, Dienstqualität)</span><span class="sxs-lookup"><span data-stu-id="eee1f-342">Quality of Service</span></span>



| <span data-ttu-id="eee1f-343">Funktion</span><span class="sxs-lookup"><span data-stu-id="eee1f-343">Function</span></span>                                                           | <span data-ttu-id="eee1f-344">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="eee1f-344">Description</span></span>                                                                                |
|--------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| [<span data-ttu-id="eee1f-345">**linesetcallqualityofservice**</span><span class="sxs-lookup"><span data-stu-id="eee1f-345">**lineSetCallQualityOfService**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linesetcallqualityofservice) | <span data-ttu-id="eee1f-346">Fordert eine Änderung der Quality of Service-Parameter für einen vorhandenen-Rückruf an.</span><span class="sxs-lookup"><span data-stu-id="eee1f-346">Requests a change of the quality of service parameters for an existing call.</span></span> <span data-ttu-id="eee1f-347">Asynchron.</span><span class="sxs-lookup"><span data-stu-id="eee1f-347">Asynchronous.</span></span> |



 

## <a name="miscellaneous"></a><span data-ttu-id="eee1f-348">Verschiedenes</span><span class="sxs-lookup"><span data-stu-id="eee1f-348">Miscellaneous</span></span>



| <span data-ttu-id="eee1f-349">Funktion</span><span class="sxs-lookup"><span data-stu-id="eee1f-349">Function</span></span>                                             | <span data-ttu-id="eee1f-350">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="eee1f-350">Description</span></span>                                                                                           |
|------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="eee1f-351">**linesetcalldata**</span><span class="sxs-lookup"><span data-stu-id="eee1f-351">**lineSetCallData**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linesetcalldata)           | <span data-ttu-id="eee1f-352">Legt den **calldata** -Member der [**LINECALLINFO**](/windows/desktop/api/Tapi/ns-tapi-linecallinfo) -Struktur fest.</span><span class="sxs-lookup"><span data-stu-id="eee1f-352">Sets the **CallData** member of the [**LINECALLINFO**](/windows/desktop/api/Tapi/ns-tapi-linecallinfo) structure.</span></span> <span data-ttu-id="eee1f-353">Asynchron.</span><span class="sxs-lookup"><span data-stu-id="eee1f-353">Asynchronous.</span></span> |
| [<span data-ttu-id="eee1f-354">**linesetcalltreatment**</span><span class="sxs-lookup"><span data-stu-id="eee1f-354">**lineSetCallTreatment**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linesetcalltreatment) | <span data-ttu-id="eee1f-355">Legt die Sounds fest, die der Benutzer erfährt, wenn ein Rückruf nicht offen ist oder angehalten wird.</span><span class="sxs-lookup"><span data-stu-id="eee1f-355">Sets the sounds that the user hears when a call is unanswered or on hold.</span></span> <span data-ttu-id="eee1f-356">Asynchron.</span><span class="sxs-lookup"><span data-stu-id="eee1f-356">Asynchronous.</span></span>               |
| [<span data-ttu-id="eee1f-357">**linesetlinedevstatus**</span><span class="sxs-lookup"><span data-stu-id="eee1f-357">**lineSetLineDevStatus**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linesetlinedevstatus) | <span data-ttu-id="eee1f-358">Legt den Gerätestatus der Zeile fest.</span><span class="sxs-lookup"><span data-stu-id="eee1f-358">Sets the line device status.</span></span> <span data-ttu-id="eee1f-359">Asynchron.</span><span class="sxs-lookup"><span data-stu-id="eee1f-359">Asynchronous.</span></span>                                                            |



 

 

 



