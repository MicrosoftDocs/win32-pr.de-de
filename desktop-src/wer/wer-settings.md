---
title: WER-Einstellungen
description: Einstellungen zum Anpassen der Problembericht Erstellungs Umgebung. Alle diese Einstellungen können mit Gruppenrichtlinie festgelegt werden. Einige können auch im Aktions Center für Windows 7 und Windows 8 geändert werden. Verwenden Sie für Windows 10 die Suchfunktion in den Einstellungen, um Erweiterte Systemeinstellungen anzuzeigen.
ms.assetid: 031c5591-31b0-42f1-9a98-ecf10a5d5571
keywords:
- Windows-Fehlerberichterstattung für die Windows-Fehlerberichterstattung, Einstellungen
ms.topic: article
ms.date: 03/12/2021
ms.openlocfilehash: 28b6abbda7d851daddb75ec534b8128d1a831b3f
ms.sourcegitcommit: 434d5437d4c31c47358598ea5275177c2698f557
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/13/2021
ms.locfileid: "106366613"
---
# <a name="wer-settings"></a><span data-ttu-id="6b58f-107">WER-Einstellungen</span><span class="sxs-lookup"><span data-stu-id="6b58f-107">WER Settings</span></span>

<span data-ttu-id="6b58f-108">Windows-Fehlerberichterstattung (wer) bietet viele Einstellungen zum Anpassen der Problembericht Erstellungs Umgebung.</span><span class="sxs-lookup"><span data-stu-id="6b58f-108">Windows Error Reporting (WER) provides many settings to customize the problem reporting experience.</span></span> <span data-ttu-id="6b58f-109">Alle diese Einstellungen können mit Gruppenrichtlinie festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="6b58f-109">All of these settings can be set using Group Policy.</span></span> <span data-ttu-id="6b58f-110">Einige können auch im **Aktions Center** für Windows 7 und Windows 8 geändert werden.</span><span class="sxs-lookup"><span data-stu-id="6b58f-110">Some can also be changed in **Action Center** for Windows 7 and Windows 8.</span></span> <span data-ttu-id="6b58f-111">Verwenden Sie für Windows 10 die Suchfunktion in den Einstellungen, um **Erweiterte Systemeinstellungen anzuzeigen**.</span><span class="sxs-lookup"><span data-stu-id="6b58f-111">For Windows 10, use the search function in Settings to locate **View advanced system settings**.</span></span> <span data-ttu-id="6b58f-112">Die wer-Einstellungen befinden sich in einem der folgenden Registrierungs Unterschlüssel:</span><span class="sxs-lookup"><span data-stu-id="6b58f-112">WER settings are located in one of the following registry subkeys:</span></span>

-   <span data-ttu-id="6b58f-113">**HKEY \_ Aktuelle \_ Benutzer** \\ **Software** \\ **Microsoft** \\ **Windows** \\ **Windows-Fehlerberichterstattung**</span><span class="sxs-lookup"><span data-stu-id="6b58f-113">**HKEY\_CURRENT\_USER**\\**Software**\\**Microsoft**\\**Windows**\\**Windows Error Reporting**</span></span>
-   <span data-ttu-id="6b58f-114">**HKEY \_ Software für den lokalen \_ Computer** \\  \\ **Microsoft** \\ **Windows** \\ **Windows-Fehlerberichterstattung**</span><span class="sxs-lookup"><span data-stu-id="6b58f-114">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Microsoft**\\**Windows**\\**Windows Error Reporting**</span></span>

## <a name="windows-error-reporting-subkey"></a><span data-ttu-id="6b58f-115">Windows-Fehlerberichterstattung Unterschlüssel</span><span class="sxs-lookup"><span data-stu-id="6b58f-115">Windows Error Reporting subkey</span></span>

<dl> <dt>

<span data-ttu-id="6b58f-116"><span id="BypassDataThrottling"></span><span id="bypassdatathrottling"></span><span id="BYPASSDATATHROTTLING"></span>**Bypassdatathrottndes**</span><span class="sxs-lookup"><span data-stu-id="6b58f-116"><span id="BypassDataThrottling"></span><span id="bypassdatathrottling"></span><span id="BYPASSDATATHROTTLING"></span>**BypassDataThrottling**</span></span>
</dt> <dd>

<span data-ttu-id="6b58f-117">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="6b58f-117">**REG\_DWORD**</span></span>

<span data-ttu-id="6b58f-118">Mögliche Werte:</span><span class="sxs-lookup"><span data-stu-id="6b58f-118">Possible values:</span></span><dl> <dd>

<span data-ttu-id="6b58f-119">0-Drosselung der Daten Umgehung deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="6b58f-119">0 - Disable data bypass throttling.</span></span> <span data-ttu-id="6b58f-120">Wenn die Umgehung deaktiviert oder nicht als Richtlinien Einstellung konfiguriert ist, werden die Daten von wer standardmäßig gedrosselt.</span><span class="sxs-lookup"><span data-stu-id="6b58f-120">If the bypass is disabled or not configured as a policy setting, WER throttles data by default.</span></span> <span data-ttu-id="6b58f-121">Wer lädt nicht mehr als eine CAB-Datei für einen Bericht hoch, der Daten zu denselben Ereignis Typen enthält.</span><span class="sxs-lookup"><span data-stu-id="6b58f-121">WER does not upload more than one CAB file for a report that contains data about the same event types.</span></span>

</dd> <dd>

<span data-ttu-id="6b58f-122">1: Aktivieren Sie die Drosselung der Daten Umgehung.</span><span class="sxs-lookup"><span data-stu-id="6b58f-122">1 - Enable data bypass throttling.</span></span> <span data-ttu-id="6b58f-123">Wer führt keine Drosselung von Daten aus.</span><span class="sxs-lookup"><span data-stu-id="6b58f-123">WER does not throttle data.</span></span> <span data-ttu-id="6b58f-124">Wer lädt zusätzliche CAB-Dateien hoch, die Daten zu denselben Ereignis Typen wie ein früherer hochgeladener Bericht enthalten können.</span><span class="sxs-lookup"><span data-stu-id="6b58f-124">WER uploads additional CAB files that can contain data about the same event types as an earlier uploaded report.</span></span>

</dd> </dl>

<span data-ttu-id="6b58f-125">Gibt an, ob die Umgehung der wer-Client Daten Drosselung aktiviert werden soll.</span><span class="sxs-lookup"><span data-stu-id="6b58f-125">Whether to enable the bypass of WER client data throttling</span></span>

</dd> <dt>

<span data-ttu-id="6b58f-126"><span id="ConfigureArchive"></span><span id="configurearchive"></span><span id="CONFIGUREARCHIVE"></span>**Konfigurieren von rearchive**</span><span class="sxs-lookup"><span data-stu-id="6b58f-126"><span id="ConfigureArchive"></span><span id="configurearchive"></span><span id="CONFIGUREARCHIVE"></span>**ConfigureArchive**</span></span>
</dt> <dd>

<span data-ttu-id="6b58f-127">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="6b58f-127">**REG\_DWORD**</span></span>

<span data-ttu-id="6b58f-128">Mögliche Werte:</span><span class="sxs-lookup"><span data-stu-id="6b58f-128">Possible values:</span></span><dl> <dd><span data-ttu-id="6b58f-129">1-nur Parameter (Standard unter Windows 7)</span><span class="sxs-lookup"><span data-stu-id="6b58f-129">1 - Parameters only (default on Windows 7)</span></span></dd> <dd><span data-ttu-id="6b58f-130">2-alle Daten (Standard unter Windows Vista)</span><span class="sxs-lookup"><span data-stu-id="6b58f-130">2 - All data (default on Windows Vista)</span></span></dd> </dl>

<span data-ttu-id="6b58f-131">Ob nur Parameter oder alle Daten archiviert werden sollen</span><span class="sxs-lookup"><span data-stu-id="6b58f-131">Whether to archive parameters only or all data</span></span>

</dd> <dt>

<span data-ttu-id="6b58f-132"><span id="Consent_DefaultConsent"></span><span id="consent_defaultconsent"></span><span id="CONSENT_DEFAULTCONSENT"></span>**Zustimmung \\ defaultconsent**</span><span class="sxs-lookup"><span data-stu-id="6b58f-132"><span id="Consent_DefaultConsent"></span><span id="consent_defaultconsent"></span><span id="CONSENT_DEFAULTCONSENT"></span>**Consent\\DefaultConsent**</span></span>
</dt> <dd>

<span data-ttu-id="6b58f-133">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="6b58f-133">**REG\_DWORD**</span></span>

<span data-ttu-id="6b58f-134">Mögliche Werte:</span><span class="sxs-lookup"><span data-stu-id="6b58f-134">Possible values:</span></span><dl> <dd><span data-ttu-id="6b58f-135">1-immer Fragen (Standard)</span><span class="sxs-lookup"><span data-stu-id="6b58f-135">1 - Always ask (default)</span></span></dd> <dd><span data-ttu-id="6b58f-136">2: nur Parameter</span><span class="sxs-lookup"><span data-stu-id="6b58f-136">2 - Parameters only</span></span></dd> <dd><span data-ttu-id="6b58f-137">3-Parameter und sichere Daten</span><span class="sxs-lookup"><span data-stu-id="6b58f-137">3 - Parameters and safe data</span></span></dd> <dd><span data-ttu-id="6b58f-138">4-alle Daten</span><span class="sxs-lookup"><span data-stu-id="6b58f-138">4 - All data</span></span></dd> </dl>

<span data-ttu-id="6b58f-139">Standardmäßige Zustimmungs Auswahl</span><span class="sxs-lookup"><span data-stu-id="6b58f-139">Default consent choice</span></span>

</dd> <dt>

<span data-ttu-id="6b58f-140"><span id="Consent_DefaultOverrideBehavior"></span><span id="consent_defaultoverridebehavior"></span><span id="CONSENT_DEFAULTOVERRIDEBEHAVIOR"></span>**Zustimmung von \\ defauldeverridebehavior**</span><span class="sxs-lookup"><span data-stu-id="6b58f-140"><span id="Consent_DefaultOverrideBehavior"></span><span id="consent_defaultoverridebehavior"></span><span id="CONSENT_DEFAULTOVERRIDEBEHAVIOR"></span>**Consent\\DefaultOverrideBehavior**</span></span>
</dt> <dd>

<span data-ttu-id="6b58f-141">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="6b58f-141">**REG\_DWORD**</span></span>

<span data-ttu-id="6b58f-142">Mögliche Werte:</span><span class="sxs-lookup"><span data-stu-id="6b58f-142">Possible values:</span></span><dl> <dd><span data-ttu-id="6b58f-143">0-die vertikale Zustimmung überschreibt die Standard Zustimmung (Standard).</span><span class="sxs-lookup"><span data-stu-id="6b58f-143">0 - Vertical consent will override the default consent (default)</span></span></dd> <dd><span data-ttu-id="6b58f-144">1: die Standard Zustimmung wird die anwendungsspezifische Zustimmung überschreiben.</span><span class="sxs-lookup"><span data-stu-id="6b58f-144">1 - Default consent will override the application-specific consent</span></span></dd> </dl>

<span data-ttu-id="6b58f-145">Gibt an, ob die Standard Zustimmung die vertikale Zustimmung überschreibt</span><span class="sxs-lookup"><span data-stu-id="6b58f-145">Whether default consent overrides vertical consent</span></span>

</dd> <dt>

<span data-ttu-id="6b58f-146"><span id="Consent__VerticalName_"></span><span id="consent__verticalname_"></span><span id="CONSENT__VERTICALNAME_"></span>**\\ \[ Verticalname der Zustimmung\]**</span><span class="sxs-lookup"><span data-stu-id="6b58f-146"><span id="Consent__VerticalName_"></span><span id="consent__verticalname_"></span><span id="CONSENT__VERTICALNAME_"></span>**Consent\\\[VerticalName\]**</span></span>
</dt> <dd>

<span data-ttu-id="6b58f-147">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="6b58f-147">**REG\_DWORD**</span></span>

<span data-ttu-id="6b58f-148">Mögliche Werte:</span><span class="sxs-lookup"><span data-stu-id="6b58f-148">Possible values:</span></span><dl> <dd><span data-ttu-id="6b58f-149">1-immer Fragen (Standard)</span><span class="sxs-lookup"><span data-stu-id="6b58f-149">1 - Always ask (default)</span></span></dd> <dd><span data-ttu-id="6b58f-150">2: nur Parameter</span><span class="sxs-lookup"><span data-stu-id="6b58f-150">2 - Parameters only</span></span></dd> <dd><span data-ttu-id="6b58f-151">3-Parameter und sichere Daten</span><span class="sxs-lookup"><span data-stu-id="6b58f-151">3 - Parameters and safe data</span></span></dd> <dd><span data-ttu-id="6b58f-152">4-alle Daten</span><span class="sxs-lookup"><span data-stu-id="6b58f-152">4 - All data</span></span></dd> </dl>

<span data-ttu-id="6b58f-153">Zustimmungs Auswahl für das wer-Plug-in</span><span class="sxs-lookup"><span data-stu-id="6b58f-153">Consent choice for the WER plug-in</span></span>

</dd> <dt>

<span data-ttu-id="6b58f-154"><span id="CorporateWERDirectory"></span><span id="corporatewerdirectory"></span><span id="CORPORATEWERDIRECTORY"></span>**Corporatewerdirectory**</span><span class="sxs-lookup"><span data-stu-id="6b58f-154"><span id="CorporateWERDirectory"></span><span id="corporatewerdirectory"></span><span id="CORPORATEWERDIRECTORY"></span>**CorporateWERDirectory**</span></span>
</dt> <dd>

<span data-ttu-id="6b58f-155">**REG- \_ SZ**</span><span class="sxs-lookup"><span data-stu-id="6b58f-155">**REG\_SZ**</span></span>

<span data-ttu-id="6b58f-156">Der Verzeichnispfad</span><span class="sxs-lookup"><span data-stu-id="6b58f-156">The directory path</span></span>

<span data-ttu-id="6b58f-157">Zielverzeichnis auf dem Server</span><span class="sxs-lookup"><span data-stu-id="6b58f-157">Target directory on the server</span></span>

</dd> <dt>

<span data-ttu-id="6b58f-158"><span id="CorporateWERPortNumber"></span><span id="corporatewerportnumber"></span><span id="CORPORATEWERPORTNUMBER"></span>**Corporatewerportnumber**</span><span class="sxs-lookup"><span data-stu-id="6b58f-158"><span id="CorporateWERPortNumber"></span><span id="corporatewerportnumber"></span><span id="CORPORATEWERPORTNUMBER"></span>**CorporateWERPortNumber**</span></span>
</dt> <dd>

<span data-ttu-id="6b58f-159">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="6b58f-159">**REG\_DWORD**</span></span>

<span data-ttu-id="6b58f-160">Die Portnummer</span><span class="sxs-lookup"><span data-stu-id="6b58f-160">The port number</span></span>

<span data-ttu-id="6b58f-161">Port Nummer, die mit dem Unternehmensserver verwendet werden soll</span><span class="sxs-lookup"><span data-stu-id="6b58f-161">Port number to be used with the corporate server</span></span>

</dd> <dt>

<span data-ttu-id="6b58f-162"><span id="CorporateWERServer"></span><span id="corporatewerserver"></span><span id="CORPORATEWERSERVER"></span>**Corporatewerserver**</span><span class="sxs-lookup"><span data-stu-id="6b58f-162"><span id="CorporateWERServer"></span><span id="corporatewerserver"></span><span id="CORPORATEWERSERVER"></span>**CorporateWERServer**</span></span>
</dt> <dd>

<span data-ttu-id="6b58f-163">**REG- \_ SZ**</span><span class="sxs-lookup"><span data-stu-id="6b58f-163">**REG\_SZ**</span></span>

<span data-ttu-id="6b58f-164">Name des Servers</span><span class="sxs-lookup"><span data-stu-id="6b58f-164">The name of the server</span></span>

<span data-ttu-id="6b58f-165">Name des Unternehmens Servers</span><span class="sxs-lookup"><span data-stu-id="6b58f-165">Corporate server name</span></span>

</dd> <dt>

<span data-ttu-id="6b58f-166"><span id="CorporateWERUseAuthentication"></span><span id="corporateweruseauthentication"></span><span id="CORPORATEWERUSEAUTHENTICATION"></span>**Corporateweruseauthentication**</span><span class="sxs-lookup"><span data-stu-id="6b58f-166"><span id="CorporateWERUseAuthentication"></span><span id="corporateweruseauthentication"></span><span id="CORPORATEWERUSEAUTHENTICATION"></span>**CorporateWERUseAuthentication**</span></span>
</dt> <dd>

<span data-ttu-id="6b58f-167">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="6b58f-167">**REG\_DWORD**</span></span>

<span data-ttu-id="6b58f-168">Mögliche Werte:</span><span class="sxs-lookup"><span data-stu-id="6b58f-168">Possible values:</span></span><dl> <dd><span data-ttu-id="6b58f-169">0-Nein (Standard)</span><span class="sxs-lookup"><span data-stu-id="6b58f-169">0 - No (default)</span></span></dd> <dd><span data-ttu-id="6b58f-170">1 – Ja</span><span class="sxs-lookup"><span data-stu-id="6b58f-170">1 - Yes</span></span></dd> </dl>

<span data-ttu-id="6b58f-171">Ob die integrierte Windows-Authentifizierung verwendet werden soll</span><span class="sxs-lookup"><span data-stu-id="6b58f-171">Whether to use Windows Integrated Authentication</span></span>

</dd> <dt>

<span data-ttu-id="6b58f-172"><span id="CorporateWERUseSSL"></span><span id="corporatewerusessl"></span><span id="CORPORATEWERUSESSL"></span>**Corporatewerus Essl**</span><span class="sxs-lookup"><span data-stu-id="6b58f-172"><span id="CorporateWERUseSSL"></span><span id="corporatewerusessl"></span><span id="CORPORATEWERUSESSL"></span>**CorporateWERUseSSL**</span></span>
</dt> <dd>

<span data-ttu-id="6b58f-173">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="6b58f-173">**REG\_DWORD**</span></span>

<span data-ttu-id="6b58f-174">Mögliche Werte:</span><span class="sxs-lookup"><span data-stu-id="6b58f-174">Possible values:</span></span><dl> <dd><span data-ttu-id="6b58f-175">0-Nein (Standard)</span><span class="sxs-lookup"><span data-stu-id="6b58f-175">0 - No (default)</span></span></dd> <dd><span data-ttu-id="6b58f-176">1 – Ja</span><span class="sxs-lookup"><span data-stu-id="6b58f-176">1 - Yes</span></span></dd> </dl>

<span data-ttu-id="6b58f-177">Ob SSL verwendet werden soll</span><span class="sxs-lookup"><span data-stu-id="6b58f-177">Whether to use SSL</span></span>

</dd> <dt>

<span data-ttu-id="6b58f-178"><span id="DebugApplications__ExeName___replace___ExeName___with_an_actual_name_of_an_.exe_file__for_example___notepad.exe__"></span><span id="debugapplications__exename___replace___exename___with_an_actual_name_of_an_.exe_file__for_example___notepad.exe__"></span><span id="DEBUGAPPLICATIONS__EXENAME___REPLACE___EXENAME___WITH_AN_ACTUAL_NAME_OF_AN_.EXE_FILE__FOR_EXAMPLE___NOTEPAD.EXE__"></span>**Debugapplications \\ \[ EXEName \] (ersetzen Sie " \[ EXEName \] " durch den tatsächlichen Namen einer exe-Datei, z. b. "notepad.exe")**</span><span class="sxs-lookup"><span data-stu-id="6b58f-178"><span id="DebugApplications__ExeName___replace___ExeName___with_an_actual_name_of_an_.exe_file__for_example___notepad.exe__"></span><span id="debugapplications__exename___replace___exename___with_an_actual_name_of_an_.exe_file__for_example___notepad.exe__"></span><span id="DEBUGAPPLICATIONS__EXENAME___REPLACE___EXENAME___WITH_AN_ACTUAL_NAME_OF_AN_.EXE_FILE__FOR_EXAMPLE___NOTEPAD.EXE__"></span>**DebugApplications\\\[ExeName\] (replace "\[ExeName\]" with an actual name of an .exe file, for example, "notepad.exe")**</span></span>
</dt> <dd>

<span data-ttu-id="6b58f-179">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="6b58f-179">**REG\_DWORD**</span></span>

<span data-ttu-id="6b58f-180">Mögliche Werte:</span><span class="sxs-lookup"><span data-stu-id="6b58f-180">Possible values:</span></span>

<dl> <dd><span data-ttu-id="6b58f-181">0-für Prozesse mit dem ausführbaren Image Namen **\[ EXEName \]** ist es nicht erforderlich, dass der Benutzer **Debuggen** oder **fortfahren** auswählt (Standard).</span><span class="sxs-lookup"><span data-stu-id="6b58f-181">0 - Processes with an executable image name of **\[ExeName\]** do not require the user to choose **Debug** or **Continue** (default)</span></span></dd> <dd><span data-ttu-id="6b58f-182">1: für Prozesse mit dem Namen des ausführbaren Images von **\[ EXEName \]** muss der Benutzer **Debuggen** oder **fortfahren** auswählen.</span><span class="sxs-lookup"><span data-stu-id="6b58f-182">1 - Processes with an executable image name of **\[ExeName\]** require the user to choose **Debug** or **Continue**</span></span></dd> </dl> </dd> <dt>

<span data-ttu-id="6b58f-183"><span id="DebugApplications________is_the_literal_value_name_"></span><span id="debugapplications________is_the_literal_value_name_"></span><span id="DEBUGAPPLICATIONS________IS_THE_LITERAL_VALUE_NAME_"></span>**Debug Applications \\ \* (" \* " ist der literalwertname)**</span><span class="sxs-lookup"><span data-stu-id="6b58f-183"><span id="DebugApplications________is_the_literal_value_name_"></span><span id="debugapplications________is_the_literal_value_name_"></span><span id="DEBUGAPPLICATIONS________IS_THE_LITERAL_VALUE_NAME_"></span>**DebugApplications\\\* ("\*" is the literal value name)**</span></span>
</dt> <dd>

<span data-ttu-id="6b58f-184">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="6b58f-184">**REG\_DWORD**</span></span>

<span data-ttu-id="6b58f-185">Mögliche Werte:</span><span class="sxs-lookup"><span data-stu-id="6b58f-185">Possible values:</span></span>

<dl> <dd><span data-ttu-id="6b58f-186">0-alle Prozesse, ausgenommen der explizit in der Einstellung **debugapplications \\ \[ EXEName \]** angegebenen Prozesse, erfordern nicht, dass der Benutzer **Debuggen** oder **fortfahren** auswählt (Standard).</span><span class="sxs-lookup"><span data-stu-id="6b58f-186">0 - All processes except ones specified explicitly in the setting **DebugApplications\\\[ExeName\]** do not require the user to choose **Debug** or **Continue** (default)</span></span></dd> <dd><span data-ttu-id="6b58f-187">1: alle Prozesse außer den explizit in der Einstellung **debugapplications \\ \[ EXEName \]** angegebenen Prozessen erfordern, dass der **Benutzer Debuggen oder** **fortfahren** auswählt.</span><span class="sxs-lookup"><span data-stu-id="6b58f-187">1 - All processes except ones specified explicitly in the setting **DebugApplications\\\[ExeName\]** require the user to choose **Debug** or **Continue**</span></span></dd> </dl> </dd> <dt>

<span data-ttu-id="6b58f-188"><span id="DisableArchive"></span><span id="disablearchive"></span><span id="DISABLEARCHIVE"></span>**Disablearchive**</span><span class="sxs-lookup"><span data-stu-id="6b58f-188"><span id="DisableArchive"></span><span id="disablearchive"></span><span id="DISABLEARCHIVE"></span>**DisableArchive**</span></span>
</dt> <dd>

<span data-ttu-id="6b58f-189">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="6b58f-189">**REG\_DWORD**</span></span>

<span data-ttu-id="6b58f-190">Mögliche Werte:</span><span class="sxs-lookup"><span data-stu-id="6b58f-190">Possible values:</span></span><dl> <dd><span data-ttu-id="6b58f-191">0–Aktiviert</span><span class="sxs-lookup"><span data-stu-id="6b58f-191">0 - Enabled</span></span></dd> <dd><span data-ttu-id="6b58f-192">1 – Deaktiviert</span><span class="sxs-lookup"><span data-stu-id="6b58f-192">1 - Disabled</span></span></dd> </dl>

<span data-ttu-id="6b58f-193">Aktivieren oder Deaktivieren des Archivs</span><span class="sxs-lookup"><span data-stu-id="6b58f-193">Enable or disable the archive</span></span>

</dd> <dt>

<span data-ttu-id="6b58f-194"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deaktiviert**</span><span class="sxs-lookup"><span data-stu-id="6b58f-194"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled**</span></span>
</dt> <dd>

<span data-ttu-id="6b58f-195">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="6b58f-195">**REG\_DWORD**</span></span>

<span data-ttu-id="6b58f-196">Mögliche Werte:</span><span class="sxs-lookup"><span data-stu-id="6b58f-196">Possible values:</span></span><dl> <dd><span data-ttu-id="6b58f-197">0-aktiviert (Standard)</span><span class="sxs-lookup"><span data-stu-id="6b58f-197">0 - Enabled (default)</span></span></dd> <dd><span data-ttu-id="6b58f-198">1 – Deaktiviert</span><span class="sxs-lookup"><span data-stu-id="6b58f-198">1 - Disabled</span></span></dd> </dl>

<span data-ttu-id="6b58f-199">Aktivieren oder Deaktivieren von wer</span><span class="sxs-lookup"><span data-stu-id="6b58f-199">Enable or disable WER</span></span>

</dd> <dt>

<span data-ttu-id="6b58f-200"><span id="DisableQueue"></span><span id="disablequeue"></span><span id="DISABLEQUEUE"></span>**Disablequeue**</span><span class="sxs-lookup"><span data-stu-id="6b58f-200"><span id="DisableQueue"></span><span id="disablequeue"></span><span id="DISABLEQUEUE"></span>**DisableQueue**</span></span>
</dt> <dd>

<span data-ttu-id="6b58f-201">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="6b58f-201">**REG\_DWORD**</span></span>

<span data-ttu-id="6b58f-202">Mögliche Werte:</span><span class="sxs-lookup"><span data-stu-id="6b58f-202">Possible values:</span></span><dl> <dd><span data-ttu-id="6b58f-203">0–Aktiviert</span><span class="sxs-lookup"><span data-stu-id="6b58f-203">0 - Enabled</span></span></dd> <dd><span data-ttu-id="6b58f-204">1 – Deaktiviert</span><span class="sxs-lookup"><span data-stu-id="6b58f-204">1 - Disabled</span></span></dd> </dl>

<span data-ttu-id="6b58f-205">Aktivieren oder Deaktivieren von Berichts Warteschlangen</span><span class="sxs-lookup"><span data-stu-id="6b58f-205">Enable or disable report queuing</span></span>

</dd> <dt>

<span data-ttu-id="6b58f-206"><span id="DontShowUI"></span><span id="dontshowui"></span><span id="DONTSHOWUI"></span>**DontShowUI**</span><span class="sxs-lookup"><span data-stu-id="6b58f-206"><span id="DontShowUI"></span><span id="dontshowui"></span><span id="DONTSHOWUI"></span>**DontShowUI**</span></span>
</dt> <dd>

<span data-ttu-id="6b58f-207">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="6b58f-207">**REG\_DWORD**</span></span>

<span data-ttu-id="6b58f-208">Mögliche Werte:</span><span class="sxs-lookup"><span data-stu-id="6b58f-208">Possible values:</span></span><dl> <dd><span data-ttu-id="6b58f-209">0-UI (Standard)</span><span class="sxs-lookup"><span data-stu-id="6b58f-209">0 - UI (default)</span></span></dd> <dd><span data-ttu-id="6b58f-210">1-keine Benutzeroberfläche</span><span class="sxs-lookup"><span data-stu-id="6b58f-210">1 - No UI</span></span></dd> </dl>

<span data-ttu-id="6b58f-211">Aktivieren oder Deaktivieren der Wer-Benutzeroberfläche</span><span class="sxs-lookup"><span data-stu-id="6b58f-211">Enable or disable the WER UI</span></span>

</dd> <dt>

<span data-ttu-id="6b58f-212"><span id="DontSendAdditionalData"></span><span id="dontsendadditionaldata"></span><span id="DONTSENDADDITIONALDATA"></span>**Dontsendadditionaldata**</span><span class="sxs-lookup"><span data-stu-id="6b58f-212"><span id="DontSendAdditionalData"></span><span id="dontsendadditionaldata"></span><span id="DONTSENDADDITIONALDATA"></span>**DontSendAdditionalData**</span></span>
</dt> <dd>

<span data-ttu-id="6b58f-213">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="6b58f-213">**REG\_DWORD**</span></span>

<span data-ttu-id="6b58f-214">Mögliche Werte:</span><span class="sxs-lookup"><span data-stu-id="6b58f-214">Possible values:</span></span><dl> <dd><span data-ttu-id="6b58f-215">0-senden (Standard)</span><span class="sxs-lookup"><span data-stu-id="6b58f-215">0 - Send (default)</span></span></dd> <dd><span data-ttu-id="6b58f-216">1-nicht senden</span><span class="sxs-lookup"><span data-stu-id="6b58f-216">1 - Do not send</span></span></dd> </dl>

<span data-ttu-id="6b58f-217">Ob das Senden von Daten der zweiten Ebene verhindert werden soll</span><span class="sxs-lookup"><span data-stu-id="6b58f-217">Whether to prevent sending second-level data</span></span>

</dd> <dt>

<span data-ttu-id="6b58f-218"><span id="ExcludedApplications__Application_Name_"></span><span id="excludedapplications__application_name_"></span><span id="EXCLUDEDAPPLICATIONS__APPLICATION_NAME_"></span>**Ausschluss \\ \[ Anwendungs Name\]**</span><span class="sxs-lookup"><span data-stu-id="6b58f-218"><span id="ExcludedApplications__Application_Name_"></span><span id="excludedapplications__application_name_"></span><span id="EXCLUDEDAPPLICATIONS__APPLICATION_NAME_"></span>**ExcludedApplications\\\[Application Name\]**</span></span>
</dt> <dd>

<span data-ttu-id="6b58f-219">**REG- \_ SZ**</span><span class="sxs-lookup"><span data-stu-id="6b58f-219">**REG\_SZ**</span></span>

<span data-ttu-id="6b58f-220">Verwenden von [ **weraddexcludebug**](/windows/desktop/api/Werapi/nf-werapi-weraddexcludedapplication)</span><span class="sxs-lookup"><span data-stu-id="6b58f-220">Use [**WerAddExcludedApplication**](/windows/desktop/api/Werapi/nf-werapi-weraddexcludedapplication)</span></span>

<span data-ttu-id="6b58f-221">Liste ausgeschlossener Anwendungen</span><span class="sxs-lookup"><span data-stu-id="6b58f-221">List of excluded applications</span></span>

</dd> <dt>

<span data-ttu-id="6b58f-222"><span id="ForceQueue"></span><span id="forcequeue"></span><span id="FORCEQUEUE"></span>**Forcequeue**</span><span class="sxs-lookup"><span data-stu-id="6b58f-222"><span id="ForceQueue"></span><span id="forcequeue"></span><span id="FORCEQUEUE"></span>**ForceQueue**</span></span>
</dt> <dd>

<span data-ttu-id="6b58f-223">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="6b58f-223">**REG\_DWORD**</span></span>

<span data-ttu-id="6b58f-224">Mögliche Werte:</span><span class="sxs-lookup"><span data-stu-id="6b58f-224">Possible values:</span></span><dl> <dd><span data-ttu-id="6b58f-225">0-Nein (Standard)</span><span class="sxs-lookup"><span data-stu-id="6b58f-225">0 - No (default)</span></span></dd> <dd><span data-ttu-id="6b58f-226">1 – Ja</span><span class="sxs-lookup"><span data-stu-id="6b58f-226">1 - Yes</span></span></dd> </dl>

<span data-ttu-id="6b58f-227">Ob alle Berichte an die Warteschlange des Benutzers gesendet werden sollen</span><span class="sxs-lookup"><span data-stu-id="6b58f-227">Whether to send all reports to the user's queue</span></span>

</dd> <dt>

<span data-ttu-id="6b58f-228"><span id="LocalDumps_DumpFolder_or_LocalDumps__Application_Name__DumpFolder"></span><span id="localdumps_dumpfolder_or_localdumps__application_name__dumpfolder"></span><span id="LOCALDUMPS_DUMPFOLDER_OR_LOCALDUMPS__APPLICATION_NAME__DUMPFOLDER"></span>**Localdumps \\ Dumpfolder** oder **localdumps \\ \[ Anwendungs Name \] \\ dumpfolder**</span><span class="sxs-lookup"><span data-stu-id="6b58f-228"><span id="LocalDumps_DumpFolder_or_LocalDumps__Application_Name__DumpFolder"></span><span id="localdumps_dumpfolder_or_localdumps__application_name__dumpfolder"></span><span id="LOCALDUMPS_DUMPFOLDER_OR_LOCALDUMPS__APPLICATION_NAME__DUMPFOLDER"></span>**LocalDumps\\DumpFolder** or **LocalDumps\\\[Application Name\]\\DumpFolder**</span></span>
</dt> <dd>

<span data-ttu-id="6b58f-229">**REG \_ Expand \_ SZ**</span><span class="sxs-lookup"><span data-stu-id="6b58f-229">**REG\_EXPAND\_SZ**</span></span>

<span data-ttu-id="6b58f-230">Der Verzeichnispfad.</span><span class="sxs-lookup"><span data-stu-id="6b58f-230">The directory path.</span></span> <span data-ttu-id="6b58f-231">Der Standardwert ist% LocalAppData% \\ CrashDumps.</span><span class="sxs-lookup"><span data-stu-id="6b58f-231">The default value is %LOCALAPPDATA%\\CrashDumps.</span></span> <span data-ttu-id="6b58f-232">Wenn der Standardwert nicht verwendet wird, muss die Anwendung sicherstellen, dass der Ordner über eine ausreichende ACL verfügt.</span><span class="sxs-lookup"><span data-stu-id="6b58f-232">If the default is not used, the application must ensure that the folder has a sufficient ACL.</span></span>

<span data-ttu-id="6b58f-233">**Windows Vista:** Die Registrierungs Werte unter dem **localdumps** -Schlüssel werden nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="6b58f-233">**Windows Vista:** The registry values under the **LocalDumps** key are not supported.</span></span> <span data-ttu-id="6b58f-234">Beachten Sie, dass sich dieses Verhalten mit Windows Server 2008 und Windows Vista mit Service Pack 1 (SP1) geändert hat.</span><span class="sxs-lookup"><span data-stu-id="6b58f-234">Note that this behavior changed with Windows Server 2008 and Windows Vista with Service Pack 1 (SP1).</span></span>

<span data-ttu-id="6b58f-235">Der Pfad, in dem die Dumpdateien gespeichert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="6b58f-235">The path where the dump files are to be stored.</span></span>

<span data-ttu-id="6b58f-236">Beachten Sie, dass prozessspezifische Einstellungen sämtliche globalen Einstellungen überschreiben, die für weitere Informationen vorhanden sind. Weitere Informationen finden Sie unter [Erfassen von User-Mode Dumps](collecting-user-mode-dumps.md).</span><span class="sxs-lookup"><span data-stu-id="6b58f-236">Note that per-process settings will override any global settings that exist For more information, see [Collecting User-Mode Dumps](collecting-user-mode-dumps.md).</span></span>

<span data-ttu-id="6b58f-237">Diese Einstellung wird in der Registrierungs Struktur des **aktuellen HKEY- \_ \_ Benutzers** nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="6b58f-237">This setting is not supported in the **HKEY\_CURRENT\_USER** registry hive.</span></span>

</dd> <dt>

<span data-ttu-id="6b58f-238"><span id="LocalDumps_DumpCount_or_LocalDumps__Application_Name__DumpCount"></span><span id="localdumps_dumpcount_or_localdumps__application_name__dumpcount"></span><span id="LOCALDUMPS_DUMPCOUNT_OR_LOCALDUMPS__APPLICATION_NAME__DUMPCOUNT"></span>**Localdumps \\ Dumpcount** oder **localdumps \\ \[ Anwendungs Name \] \\ dumpcount**</span><span class="sxs-lookup"><span data-stu-id="6b58f-238"><span id="LocalDumps_DumpCount_or_LocalDumps__Application_Name__DumpCount"></span><span id="localdumps_dumpcount_or_localdumps__application_name__dumpcount"></span><span id="LOCALDUMPS_DUMPCOUNT_OR_LOCALDUMPS__APPLICATION_NAME__DUMPCOUNT"></span>**LocalDumps\\DumpCount** or **LocalDumps\\\[Application Name\]\\DumpCount**</span></span>
</dt> <dd>

<span data-ttu-id="6b58f-239">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="6b58f-239">**REG\_DWORD**</span></span>

<span data-ttu-id="6b58f-240">Die maximale Anzahl.</span><span class="sxs-lookup"><span data-stu-id="6b58f-240">The maximum number.</span></span> <span data-ttu-id="6b58f-241">Der Standardwert ist 10.</span><span class="sxs-lookup"><span data-stu-id="6b58f-241">The default is 10.</span></span> <span data-ttu-id="6b58f-242">Wenn der Höchstwert überschritten wird, wird die älteste Dumpdatei im Ordner durch die neue Dumpdatei ersetzt.</span><span class="sxs-lookup"><span data-stu-id="6b58f-242">When the maximum value is exceeded, the oldest dump file in the folder will be replaced with the new dump file.</span></span>

<span data-ttu-id="6b58f-243">**Windows Vista:** Die Registrierungs Werte unter dem **localdumps** -Schlüssel werden nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="6b58f-243">**Windows Vista:** The registry values under the **LocalDumps** key are not supported.</span></span> <span data-ttu-id="6b58f-244">Beachten Sie, dass sich dieses Verhalten in Windows Server 2008 und Windows Vista mit SP1 geändert hat.</span><span class="sxs-lookup"><span data-stu-id="6b58f-244">Note that this behavior changed with Windows Server 2008 and Windows Vista with SP1.</span></span>

<span data-ttu-id="6b58f-245">Die maximale Anzahl von Dumpdateien im Ordner.</span><span class="sxs-lookup"><span data-stu-id="6b58f-245">The maximum number of dump files in the folder.</span></span>

<span data-ttu-id="6b58f-246">Diese Einstellung wird in der Registrierungs Struktur des **aktuellen HKEY- \_ \_ Benutzers** nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="6b58f-246">This setting is not supported in the **HKEY\_CURRENT\_USER** registry hive.</span></span>

</dd> <dt>

<span data-ttu-id="6b58f-247"><span id="LocalDumps_DumpType_or_LocalDumps__Application_Name__DumpType"></span><span id="localdumps_dumptype_or_localdumps__application_name__dumptype"></span><span id="LOCALDUMPS_DUMPTYPE_OR_LOCALDUMPS__APPLICATION_NAME__DUMPTYPE"></span>**Localdumps \\ Dumptype** oder **localdumps \\ \[ Anwendungs Name \] \\ dumptype**</span><span class="sxs-lookup"><span data-stu-id="6b58f-247"><span id="LocalDumps_DumpType_or_LocalDumps__Application_Name__DumpType"></span><span id="localdumps_dumptype_or_localdumps__application_name__dumptype"></span><span id="LOCALDUMPS_DUMPTYPE_OR_LOCALDUMPS__APPLICATION_NAME__DUMPTYPE"></span>**LocalDumps\\DumpType** or **LocalDumps\\\[Application Name\]\\DumpType**</span></span>
</dt> <dd>

<span data-ttu-id="6b58f-248">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="6b58f-248">**REG\_DWORD**</span></span>

<span data-ttu-id="6b58f-249">Mögliche Werte:</span><span class="sxs-lookup"><span data-stu-id="6b58f-249">Possible values:</span></span><dl> <dd><span data-ttu-id="6b58f-250">0-benutzerdefiniertes Dump</span><span class="sxs-lookup"><span data-stu-id="6b58f-250">0 - Custom dump</span></span></dd> <dd><span data-ttu-id="6b58f-251">1-Minidump (Standard)</span><span class="sxs-lookup"><span data-stu-id="6b58f-251">1 - Minidump (default)</span></span></dd> <dd><span data-ttu-id="6b58f-252">2: vollständiges Dump</span><span class="sxs-lookup"><span data-stu-id="6b58f-252">2 - Full dump</span></span></dd> </dl>

<span data-ttu-id="6b58f-253">**Windows Vista:** Die Registrierungs Werte unter dem **localdumps** -Schlüssel werden nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="6b58f-253">**Windows Vista:** The registry values under the **LocalDumps** key are not supported.</span></span> <span data-ttu-id="6b58f-254">Beachten Sie, dass sich dieses Verhalten in Windows Server 2008 und Windows Vista mit SP1 geändert hat.</span><span class="sxs-lookup"><span data-stu-id="6b58f-254">Note that this behavior changed with Windows Server 2008 and Windows Vista with SP1.</span></span>

<span data-ttu-id="6b58f-255">Der dumptyp.</span><span class="sxs-lookup"><span data-stu-id="6b58f-255">The dump type.</span></span>

<span data-ttu-id="6b58f-256">Diese Einstellung wird in der Registrierungs Struktur des **aktuellen HKEY- \_ \_ Benutzers** nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="6b58f-256">This setting is not supported in the **HKEY\_CURRENT\_USER** registry hive.</span></span>

</dd> <dt>

<span data-ttu-id="6b58f-257"><span id="LocalDumps_CustomDumpFlags_or_LocalDumps__Application_Name__CustomDumpFlags"></span><span id="localdumps_customdumpflags_or_localdumps__application_name__customdumpflags"></span><span id="LOCALDUMPS_CUSTOMDUMPFLAGS_OR_LOCALDUMPS__APPLICATION_NAME__CUSTOMDUMPFLAGS"></span>**Localdumps \\ Customdumpflags** oder **localdumps \\ \[ Anwendungs Name \] \\ customdumpflags**</span><span class="sxs-lookup"><span data-stu-id="6b58f-257"><span id="LocalDumps_CustomDumpFlags_or_LocalDumps__Application_Name__CustomDumpFlags"></span><span id="localdumps_customdumpflags_or_localdumps__application_name__customdumpflags"></span><span id="LOCALDUMPS_CUSTOMDUMPFLAGS_OR_LOCALDUMPS__APPLICATION_NAME__CUSTOMDUMPFLAGS"></span>**LocalDumps\\CustomDumpFlags** or **LocalDumps\\\[Application Name\]\\CustomDumpFlags**</span></span>
</dt> <dd>

<span data-ttu-id="6b58f-258">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="6b58f-258">**REG\_DWORD**</span></span>

<span data-ttu-id="6b58f-259">Mindestens ein Wert aus der [**Minidump- \_ Typenumeration**](/windows/desktop/api/minidumpapiset/ne-minidumpapiset-minidump_type) .</span><span class="sxs-lookup"><span data-stu-id="6b58f-259">One or more values from the [**MINIDUMP\_TYPE**](/windows/desktop/api/minidumpapiset/ne-minidumpapiset-minidump_type) enumeration.</span></span> <span data-ttu-id="6b58f-260">Der Standardwert ist {**minidumpwithdatasegs** \| **minidumpwithunloadedmodules** \| **minidumpwithprocessthreaddata**}.</span><span class="sxs-lookup"><span data-stu-id="6b58f-260">The default is {**MiniDumpWithDataSegs**\|**MiniDumpWithUnloadedModules**\|**MiniDumpWithProcessThreadData**}.</span></span>

<span data-ttu-id="6b58f-261">**Windows Vista:** Die Registrierungs Werte unter dem **localdumps** -Schlüssel werden nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="6b58f-261">**Windows Vista:** The registry values under the **LocalDumps** key are not supported.</span></span> <span data-ttu-id="6b58f-262">Beachten Sie, dass sich dieses Verhalten in Windows Server 2008 und Windows Vista mit SP1 geändert hat.</span><span class="sxs-lookup"><span data-stu-id="6b58f-262">Note that this behavior changed with Windows Server 2008 and Windows Vista with SP1.</span></span>

<span data-ttu-id="6b58f-263">Die benutzerdefinierten dumpoptionen, die verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="6b58f-263">The custom dump options to be used.</span></span> <span data-ttu-id="6b58f-264">Dieser Wert wird nur verwendet, wenn **dumptype** auf 0 festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="6b58f-264">This value is used only when **DumpType** is set to 0.</span></span>

<span data-ttu-id="6b58f-265">Diese Einstellung wird in der Registrierungs Struktur des **aktuellen HKEY- \_ \_ Benutzers** nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="6b58f-265">This setting is not supported in the **HKEY\_CURRENT\_USER** registry hive.</span></span>

</dd> <dt>

<span data-ttu-id="6b58f-266"><span id="LoggingDisabled"></span><span id="loggingdisabled"></span><span id="LOGGINGDISABLED"></span>**Loggingdeaktiviert**</span><span class="sxs-lookup"><span data-stu-id="6b58f-266"><span id="LoggingDisabled"></span><span id="loggingdisabled"></span><span id="LOGGINGDISABLED"></span>**LoggingDisabled**</span></span>
</dt> <dd>

<span data-ttu-id="6b58f-267">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="6b58f-267">**REG\_DWORD**</span></span>

<span data-ttu-id="6b58f-268">Mögliche Werte:</span><span class="sxs-lookup"><span data-stu-id="6b58f-268">Possible values:</span></span><dl> <dd><span data-ttu-id="6b58f-269">0 – aktiviert (Standard)</span><span class="sxs-lookup"><span data-stu-id="6b58f-269">0–Enabled (default)</span></span></dd> <dd><span data-ttu-id="6b58f-270">1 – deaktiviert</span><span class="sxs-lookup"><span data-stu-id="6b58f-270">1–Disabled</span></span></dd> </dl>

<span data-ttu-id="6b58f-271">Aktivieren oder Deaktivieren der Protokollierung</span><span class="sxs-lookup"><span data-stu-id="6b58f-271">Enable or disable logging</span></span>

</dd> <dt>

<span data-ttu-id="6b58f-272"><span id="MaxArchiveCount"></span><span id="maxarchivecount"></span><span id="MAXARCHIVECOUNT"></span>**Maxarchivecount**</span><span class="sxs-lookup"><span data-stu-id="6b58f-272"><span id="MaxArchiveCount"></span><span id="maxarchivecount"></span><span id="MAXARCHIVECOUNT"></span>**MaxArchiveCount**</span></span>
</dt> <dd>

<span data-ttu-id="6b58f-273">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="6b58f-273">**REG\_DWORD**</span></span>

<span data-ttu-id="6b58f-274">Bereich möglicher Werte: 1 – 5.000.</span><span class="sxs-lookup"><span data-stu-id="6b58f-274">Range of possible values: 1–5000.</span></span> <span data-ttu-id="6b58f-275">Der Standardwert lautet 1000.</span><span class="sxs-lookup"><span data-stu-id="6b58f-275">The default is 1000.</span></span>

<span data-ttu-id="6b58f-276">Maximale Größe des Archivs in Dateien</span><span class="sxs-lookup"><span data-stu-id="6b58f-276">Maximum size of the archive, in files</span></span>

</dd> <dt>

<span data-ttu-id="6b58f-277"><span id="MaxQueueCount"></span><span id="maxqueuecount"></span><span id="MAXQUEUECOUNT"></span>**Maxqueuecount**</span><span class="sxs-lookup"><span data-stu-id="6b58f-277"><span id="MaxQueueCount"></span><span id="maxqueuecount"></span><span id="MAXQUEUECOUNT"></span>**MaxQueueCount**</span></span>
</dt> <dd>

<span data-ttu-id="6b58f-278">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="6b58f-278">**REG\_DWORD**</span></span>

<span data-ttu-id="6b58f-279">Bereich möglicher Werte: 1 – 500.</span><span class="sxs-lookup"><span data-stu-id="6b58f-279">Range of possible values: 1–500.</span></span> <span data-ttu-id="6b58f-280">Der Standardwert ist 50.</span><span class="sxs-lookup"><span data-stu-id="6b58f-280">The default is 50.</span></span>

<span data-ttu-id="6b58f-281">Maximale Größe der Warteschlange</span><span class="sxs-lookup"><span data-stu-id="6b58f-281">Maximum size of the queue</span></span>

</dd> <dt>

<span data-ttu-id="6b58f-282"><span id="QueuePesterInterval"></span><span id="queuepesterinterval"></span><span id="QUEUEPESTERINTERVAL"></span>**Queuepeer Interval**</span><span class="sxs-lookup"><span data-stu-id="6b58f-282"><span id="QueuePesterInterval"></span><span id="queuepesterinterval"></span><span id="QUEUEPESTERINTERVAL"></span>**QueuePesterInterval**</span></span>
</dt> <dd>

<span data-ttu-id="6b58f-283">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="6b58f-283">**REG\_DWORD**</span></span>

<span data-ttu-id="6b58f-284">Anzahl von Tagen</span><span class="sxs-lookup"><span data-stu-id="6b58f-284">Number of days</span></span>

<span data-ttu-id="6b58f-285">Intervall zwischen Erinnerungen an den Benutzer für die Überprüfung auf Lösungen in Tagen</span><span class="sxs-lookup"><span data-stu-id="6b58f-285">Interval between reminders to the user to check for solutions, in days</span></span>

</dd> <dt>

<span data-ttu-id="6b58f-286"><span id="RuntimeExceptionHelperModules___pwszOutOfProcessCallbackDll_name_including_path_"></span><span id="runtimeexceptionhelpermodules___pwszoutofprocesscallbackdll_name_including_path_"></span><span id="RUNTIMEEXCEPTIONHELPERMODULES___PWSZOUTOFPROCESSCALLBACKDLL_NAME_INCLUDING_PATH_"></span>**Runtimeexceptionhelpermodules! \[ pwszouybprocesscallbackdll-Name einschließlich Pfad\]**</span><span class="sxs-lookup"><span data-stu-id="6b58f-286"><span id="RuntimeExceptionHelperModules___pwszOutOfProcessCallbackDll_name_including_path_"></span><span id="runtimeexceptionhelpermodules___pwszoutofprocesscallbackdll_name_including_path_"></span><span id="RUNTIMEEXCEPTIONHELPERMODULES___PWSZOUTOFPROCESSCALLBACKDLL_NAME_INCLUDING_PATH_"></span>**RuntimeExceptionHelperModules!\[ pwszOutOfProcessCallbackDll name including path\]**</span></span>
</dt> <dd>

<span data-ttu-id="6b58f-287">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="6b58f-287">**REG\_DWORD**</span></span>

<span data-ttu-id="6b58f-288">Der Inhalt des Werts wird ignoriert.</span><span class="sxs-lookup"><span data-stu-id="6b58f-288">The contents of the value are ignored.</span></span>

<span data-ttu-id="6b58f-289">Der Name des Werts wird zum Abrufen des pwszouesfprocesscallbackdll-Werts verwendet.</span><span class="sxs-lookup"><span data-stu-id="6b58f-289">The name of the value is used to fetch the pwszOutOfProcessCallbackDll value.</span></span>

<span data-ttu-id="6b58f-290">**Windows Server 2008, Windows Vista, Windows Server 2003 und Windows XP:** Dieser Registrierungs Wert wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="6b58f-290">**Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:** This registry value is not supported.</span></span>

</dd> </dl>

## <a name="wer-live-kernel-reports-settings"></a><span data-ttu-id="6b58f-291">Einstellungen für wer Live Kernel Berichte</span><span class="sxs-lookup"><span data-stu-id="6b58f-291">WER Live Kernel Reports Settings</span></span>

<span data-ttu-id="6b58f-292">Die im nächsten beschriebenen Live Kernel Berichte-Einstellungen befinden sich beide unter dem folgenden Registrierungs Unterschlüssel:</span><span class="sxs-lookup"><span data-stu-id="6b58f-292">WER's Live Kernel Reports settings, which are described next, are both located under the following registry subkey:</span></span>

-   <span data-ttu-id="6b58f-293">**HKEY \_ Lokales \_ Computer** \\ **System** \\ **CurrentControlSet** \\ **Control** \\ **CrashControl**</span><span class="sxs-lookup"><span data-stu-id="6b58f-293">**HKEY\_LOCAL\_MACHINE**\\**SYSTEM**\\**CurrentControlSet**\\**Control**\\**CrashControl**</span></span>

## <a name="fulllivekernelreports-subkey"></a><span data-ttu-id="6b58f-294">Fulllivekernelreports-Unterschlüssel</span><span class="sxs-lookup"><span data-stu-id="6b58f-294">FullLiveKernelReports subkey</span></span>

<dl> <dt>

<span data-ttu-id="6b58f-295"><span id="ComponentThrottleThreshold"></span><span id="componentthrottlethreshold"></span><span id="COMPONENTTHROTTLETHRESHOLD"></span>**Componentthrottlethreshold**</span><span class="sxs-lookup"><span data-stu-id="6b58f-295"><span id="ComponentThrottleThreshold"></span><span id="componentthrottlethreshold"></span><span id="COMPONENTTHROTTLETHRESHOLD"></span>**ComponentThrottleThreshold**</span></span>
</dt> <dd>

<span data-ttu-id="6b58f-296">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="6b58f-296">**REG\_DWORD**</span></span>

<span data-ttu-id="6b58f-297">Der Schwellenwert (in Stunden), wie oft eine einzelne Komponente ein vollständiges livedump erstellen kann.</span><span class="sxs-lookup"><span data-stu-id="6b58f-297">The threshold (in hours) of how often any single component can create a full live dump.</span></span> <span data-ttu-id="6b58f-298">Dieser Wert muss größer oder gleich **systemthrottlethreshold** sein.</span><span class="sxs-lookup"><span data-stu-id="6b58f-298">This value must be greater than or equal to **SystemThrottleThreshold**.</span></span> <span data-ttu-id="6b58f-299">Wenn beide Werte auf 0 (null) festgelegt werden, wird die zeitbasierte Drosselung deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="6b58f-299">Setting both to zero (0) will disable all time-based throttling.</span></span> <span data-ttu-id="6b58f-300">Der Standardwert ist 168 (7 Tage).</span><span class="sxs-lookup"><span data-stu-id="6b58f-300">The default is 168 (7 days).</span></span>

</dd> <dt>

<span data-ttu-id="6b58f-301"><span id="FullLiveReportsMax"></span><span id="fulllivereportsmax"></span><span id="FULLLIVEREPORTSMAX"></span>**Fulllivereportsmax**</span><span class="sxs-lookup"><span data-stu-id="6b58f-301"><span id="FullLiveReportsMax"></span><span id="fulllivereportsmax"></span><span id="FULLLIVEREPORTSMAX"></span>**FullLiveReportsMax**</span></span>
</dt> <dd>

<span data-ttu-id="6b58f-302">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="6b58f-302">**REG\_DWORD**</span></span>

<span data-ttu-id="6b58f-303">Die maximale Anzahl vollständiger Live Abbilder, die zu einem beliebigen Zeitpunkt auf dem Datenträger gespeichert werden können.</span><span class="sxs-lookup"><span data-stu-id="6b58f-303">The maximum number of full live dumps that may be on disk at any given time.</span></span> <span data-ttu-id="6b58f-304">Der Standardwert ist 1.</span><span class="sxs-lookup"><span data-stu-id="6b58f-304">The default is 1.</span></span> <span data-ttu-id="6b58f-305">Wenn dieser Wert auf NULL (0) festgelegt wird, wird die Live Dump-Funktion deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="6b58f-305">Setting this value to zero (0) will disable the live dump feature.</span></span>

</dd> <dt>

<span data-ttu-id="6b58f-306"><span id="LastFullLiveReport"></span><span id="lastfulllivereport"></span><span id="LASTFULLLIVEREPORT"></span>**Lastfulllivereport**</span><span class="sxs-lookup"><span data-stu-id="6b58f-306"><span id="LastFullLiveReport"></span><span id="lastfulllivereport"></span><span id="LASTFULLLIVEREPORT"></span>**LastFullLiveReport**</span></span>
</dt> <dd>

<span data-ttu-id="6b58f-307">**REG \_ QWORD**</span><span class="sxs-lookup"><span data-stu-id="6b58f-307">**REG\_QWORD**</span></span>

<span data-ttu-id="6b58f-308">Ein [SYSTEMTIME](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) -Wert, der den Zeitpunkt des letzten vollständigen Live Berichts für das System oder einen bestimmten reportType angibt.</span><span class="sxs-lookup"><span data-stu-id="6b58f-308">A [SystemTime](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) indicating the last full live report time, for the system or a specific ReportType.</span></span> <span data-ttu-id="6b58f-309">Hiermit wird berechnet, ob ein Richtlinien Schwellenwert erfüllt wurde.</span><span class="sxs-lookup"><span data-stu-id="6b58f-309">This is used to calculate whether a policy threshold has been satisfied.</span></span>

</dd> <dt>

<span data-ttu-id="6b58f-310"><span id="SystemThrottleThreshold"></span><span id="systemthrottlethreshold"></span><span id="SYSTEMTHROTTLETHRESHOLD"></span>**Systemdrossellethreshold**</span><span class="sxs-lookup"><span data-stu-id="6b58f-310"><span id="SystemThrottleThreshold"></span><span id="systemthrottlethreshold"></span><span id="SYSTEMTHROTTLETHRESHOLD"></span>**SystemThrottleThreshold**</span></span>
</dt> <dd>

<span data-ttu-id="6b58f-311">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="6b58f-311">**REG\_DWORD**</span></span>

<span data-ttu-id="6b58f-312">Der Schwellenwert (in Stunden), wie oft eine beliebige Komponente im System ein vollständiges livedump erstellen kann.</span><span class="sxs-lookup"><span data-stu-id="6b58f-312">The threshold (in hours) of how often any component on the system can create a full live dump.</span></span> <span data-ttu-id="6b58f-313">Der Standardwert ist 120 (5 Tage).</span><span class="sxs-lookup"><span data-stu-id="6b58f-313">The default is 120 (5 days).</span></span>

</dd> </dl>

## <a name="livekernelreports-subkey"></a><span data-ttu-id="6b58f-314">Livekernelreports-Unterschlüssel</span><span class="sxs-lookup"><span data-stu-id="6b58f-314">LiveKernelReports subkey</span></span>

<dl> <dt>

<span data-ttu-id="6b58f-315"><span id="LiveKernelReportsPath"></span><span id="livekernelreportspath"></span><span id="LIVEKERNELREPORTSPATH"></span>**Livekernelreportspath**</span><span class="sxs-lookup"><span data-stu-id="6b58f-315"><span id="LiveKernelReportsPath"></span><span id="livekernelreportspath"></span><span id="LIVEKERNELREPORTSPATH"></span>**LiveKernelReportsPath**</span></span>
</dt> <dd>

<span data-ttu-id="6b58f-316">**REG- \_ SZ**</span><span class="sxs-lookup"><span data-stu-id="6b58f-316">**REG\_SZ**</span></span>


<span data-ttu-id="6b58f-317">Der umgeleitete Speicherort von Live-Kernel-Berichten.</span><span class="sxs-lookup"><span data-stu-id="6b58f-317">The redirected storage location of live kernel reports.</span></span> <span data-ttu-id="6b58f-318">Der Standard Speicherort ist%SystemRoot%\livekernelreports.</span><span class="sxs-lookup"><span data-stu-id="6b58f-318">The default location is %systemroot%\LiveKernelReports.</span></span> <span data-ttu-id="6b58f-319">Dieser Wert muss ein gültiger Pfad sein.</span><span class="sxs-lookup"><span data-stu-id="6b58f-319">This value must be a valid path.</span></span> <span data-ttu-id="6b58f-320">Der Pfad muss im NT-Pfad Format vorliegen.</span><span class="sxs-lookup"><span data-stu-id="6b58f-320">The path must be in NT path format.</span></span> <span data-ttu-id="6b58f-321">Beispiel \? :? \c: \livedumpsfolder.</span><span class="sxs-lookup"><span data-stu-id="6b58f-321">For example, \??\C:\LiveDumpsFolder.</span></span>  <span data-ttu-id="6b58f-322">Weitere Informationen zu Pfad Formaten finden Sie unter  [Datei Pfad Formate auf Windows-Systemen](/dotnet/standard/io/file-path-formats).</span><span class="sxs-lookup"><span data-stu-id="6b58f-322">For more information on path formats, see  [File path formats on Windows systems](/dotnet/standard/io/file-path-formats).</span></span>

</dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="6b58f-323">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="6b58f-323">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6b58f-324">Wer-Verweis</span><span class="sxs-lookup"><span data-stu-id="6b58f-324">WER Reference</span></span>](wer-reference.md)
</dt> </dl>

 

 
