---
description: Mit den DLP-APIs (Endpoint Data Loss Prevention) können Anwendungen das Betriebssystem vor und nach bestimmten Vorgängen benachrichtigen, z. B. beim Öffnen oder Speichern einer Datei.
title: Verhinderung von Endpunktdatenverlust
ms.topic: article
ms.date: 03/18/2021
ms.openlocfilehash: 3b8576f9eadd0037eca56c0ba183ea1d1825679a
ms.sourcegitcommit: 8b543a86e551cb5b4270a3cc3590ad0758fb6156
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2021
ms.locfileid: "107526090"
---
# <a name="endpoint-data-loss-prevention"></a><span data-ttu-id="9948d-103">Verhinderung von Endpunktdatenverlust</span><span class="sxs-lookup"><span data-stu-id="9948d-103">Endpoint data loss prevention</span></span>

<span data-ttu-id="9948d-104">Windows 10 implementiert Mechanismen, mit denen Datenverluste für sensible Dateien verhindert werden können.</span><span class="sxs-lookup"><span data-stu-id="9948d-104">Windows 10 implements mechanisms that help to prevent data loss for sensitive files.</span></span> <span data-ttu-id="9948d-105">Mit den DLP-APIs (Endpoint Data Loss Prevention) können Anwendungen das Betriebssystem vor und nach bestimmten Vorgängen benachrichtigen, z. B. beim Öffnen oder Speichern einer Datei.</span><span class="sxs-lookup"><span data-stu-id="9948d-105">The endpoint data loss prevention (DLP) APIs allow applications to notify the OS before and after certain operations, such as opening or saving a file.</span></span> <span data-ttu-id="9948d-106">Diese Benachrichtigungen dienen als "Hinweise", mit denen das System Datenverlustvorgänge optimieren kann.</span><span class="sxs-lookup"><span data-stu-id="9948d-106">These notifications serve as "hints" that allow the system to optimize data loss operations.</span></span>

## <a name="location-of-the-dlp-dll"></a><span data-ttu-id="9948d-107">Speicherort der DLP-DLL</span><span class="sxs-lookup"><span data-stu-id="9948d-107">Location of the DLP dll</span></span>

<span data-ttu-id="9948d-108">Da die Endpunkt-DLP-DLL nicht mit dem Windows SDK gebündelt ist, müssen Anwendungen die DLL zur Laufzeit manuell laden.</span><span class="sxs-lookup"><span data-stu-id="9948d-108">Since the endpoint DLP dll isn't bundled with the Windows SDK, applications will need to load the dll manually at runtime.</span></span> <span data-ttu-id="9948d-109">Der Pfad zum DLL-Speicherort wird in der Registrierung gespeichert.</span><span class="sxs-lookup"><span data-stu-id="9948d-109">The path to the dll location is stored in the registry.</span></span> <span data-ttu-id="9948d-110">In der folgenden Tabelle sind die Registrierungsschlüssel und -werte aufgeführt, die diese Informationen speichern.</span><span class="sxs-lookup"><span data-stu-id="9948d-110">The following table lists the registry keys and values that store this information.</span></span> <span data-ttu-id="9948d-111">Diese Pfade werden als Konstanten in der unten angegebenen Beispielcodeauflistung endpointdlp.h definiert, um Entwicklern zu erleichtern.</span><span class="sxs-lookup"><span data-stu-id="9948d-111">These paths are defined as constants in the sample endpointdlp.h code listing provided below as a convenience for developers.</span></span>

| <span data-ttu-id="9948d-112">Konstant</span><span class="sxs-lookup"><span data-stu-id="9948d-112">Constant</span></span> | <span data-ttu-id="9948d-113">Wert</span><span class="sxs-lookup"><span data-stu-id="9948d-113">Value</span></span> | <span data-ttu-id="9948d-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9948d-114">Description</span></span>   |
|----------|-------|---------------|
| <span data-ttu-id="9948d-115">ENDPOINTDLP_DLL_NAME</span><span class="sxs-lookup"><span data-stu-id="9948d-115">ENDPOINTDLP_DLL_NAME</span></span> | <span data-ttu-id="9948d-116">"EndpointDlp.dll"</span><span class="sxs-lookup"><span data-stu-id="9948d-116">"EndpointDlp.dll"</span></span> | <span data-ttu-id="9948d-117">Der Name der Endpunkt-DLP-DLL, die die API bereitstellt</span><span class="sxs-lookup"><span data-stu-id="9948d-117">The name of the Endpoint DLP DLL that provides the API</span></span> |
| <span data-ttu-id="9948d-118">ENDPOINTDLP_WINDOWS_DEFENDER_REGKEY</span><span class="sxs-lookup"><span data-stu-id="9948d-118">ENDPOINTDLP_WINDOWS_DEFENDER_REGKEY</span></span> | <span data-ttu-id="9948d-119">"SOFTWARE \\ Microsoft \\ Windows Defender"</span><span class="sxs-lookup"><span data-stu-id="9948d-119">"SOFTWARE\\Microsoft\\Windows Defender"</span></span> | <span data-ttu-id="9948d-120">Windows Defender Registrierungsschlüssel unter HKLM, in dem einige Endpunkt-DLP-Einstellungen gespeichert sind</span><span class="sxs-lookup"><span data-stu-id="9948d-120">Windows Defender registry key under HKLM where some Endpoint DLP settings are stored</span></span> |
| <span data-ttu-id="9948d-121">ENDPOINTDLP_DLL_INSTALL_LOCATION_REGKEY</span><span class="sxs-lookup"><span data-stu-id="9948d-121">ENDPOINTDLP_DLL_INSTALL_LOCATION_REGKEY</span></span> | <span data-ttu-id="9948d-122">Wert von ENDPOINTDLP_WINDOWS_DEFENDER_REGKEY</span><span class="sxs-lookup"><span data-stu-id="9948d-122">Value of ENDPOINTDLP_WINDOWS_DEFENDER_REGKEY</span></span> |  <span data-ttu-id="9948d-123">Der Registrierungspfad unter dem HKLM-Schlüssel, von dem der EndpointDlp.dll Installationsspeicherort abgerufen werden kann.</span><span class="sxs-lookup"><span data-stu-id="9948d-123">The registry path under HKLM key from which the EndpointDlp.dll install location can be obtained</span></span> |
| <span data-ttu-id="9948d-124">ENDPOINTDLP_DLL_INSTALL_LOCATION_REGVALUE</span><span class="sxs-lookup"><span data-stu-id="9948d-124">ENDPOINTDLP_DLL_INSTALL_LOCATION_REGVALUE</span></span> | <span data-ttu-id="9948d-125">"InstallLocation"</span><span class="sxs-lookup"><span data-stu-id="9948d-125">"InstallLocation"</span></span> | <span data-ttu-id="9948d-126">Der Registrierungswert unter ENDPOINTDLP_DLL_INSTALL_LOCATION_REGKEY, in dem der EndpointDlp.dll-Installationsspeicherort gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="9948d-126">The registry value under ENDPOINTDLP_DLL_INSTALL_LOCATION_REGKEY in which the EndpointDlp.dll install location is stored</span></span> |
| <span data-ttu-id="9948d-127">ENDPOINTDLP_DLL_WOW64_X86_INSTALL_LOCATION_SUFFIX</span><span class="sxs-lookup"><span data-stu-id="9948d-127">ENDPOINTDLP_DLL_WOW64_X86_INSTALL_LOCATION_SUFFIX</span></span> | <span data-ttu-id="9948d-128">"x86"</span><span class="sxs-lookup"><span data-stu-id="9948d-128">"x86"</span></span> | <span data-ttu-id="9948d-129">Verketten Sie dieses Verzeichnis auf x64-Plattformen, um die x86-Version des EndpointDlp.dll</span><span class="sxs-lookup"><span data-stu-id="9948d-129">On x64 platforms, concatenate this directory to obtain the x86 version of EndpointDlp.dll</span></span> |

## <a name="check-if-endpoint-dlp-is-enabled"></a><span data-ttu-id="9948d-130">Überprüfen, ob Endpunkt-DLP aktiviert ist</span><span class="sxs-lookup"><span data-stu-id="9948d-130">Check if endpoint DLP is enabled</span></span>

<span data-ttu-id="9948d-131">Überprüfen Sie den folgenden Registrierungsschlüsselwert, um zu ermitteln, ob die Endpunkt-DLP auf dem System aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="9948d-131">To determine if endpoint DLP is enabled on the system, check the following registry key value.</span></span> 

| <span data-ttu-id="9948d-132">Konstant</span><span class="sxs-lookup"><span data-stu-id="9948d-132">Constant</span></span> | <span data-ttu-id="9948d-133">Wert</span><span class="sxs-lookup"><span data-stu-id="9948d-133">Value</span></span> | <span data-ttu-id="9948d-134">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9948d-134">Description</span></span>   |
|----------|-------|---------------|
| <span data-ttu-id="9948d-135">ENDPOINTDLP_ENABLED_FLAG_REGKEY</span><span class="sxs-lookup"><span data-stu-id="9948d-135">ENDPOINTDLP_ENABLED_FLAG_REGKEY</span></span> |  <span data-ttu-id="9948d-136">" \\ Features"</span><span class="sxs-lookup"><span data-stu-id="9948d-136">"\\Features"</span></span> | <span data-ttu-id="9948d-137">Der Pfad zum Endpunkt-DLP-fähigen Flagschlüssel unter (HKLM) ENDPOINTDLP_WINDOWS_DEFENDER_REGKEY</span><span class="sxs-lookup"><span data-stu-id="9948d-137">The path to the Endpoint DLP enabled flag key under (HKLM) ENDPOINTDLP_WINDOWS_DEFENDER_REGKEY</span></span> |
| <span data-ttu-id="9948d-138">ENDPOINTDLP_ENABLED_FLAG_REGVALUE</span><span class="sxs-lookup"><span data-stu-id="9948d-138">ENDPOINTDLP_ENABLED_FLAG_REGVALUE</span></span> | <span data-ttu-id="9948d-139">"SenseDlpEnabled"</span><span class="sxs-lookup"><span data-stu-id="9948d-139">"SenseDlpEnabled"</span></span> | <span data-ttu-id="9948d-140">Der Registrierungswert unter ENDPOINTDLP_ENABLED_FLAG_REGKEY, der den Registrierungsschlüssel des DLP-fähigen Flags enthält.</span><span class="sxs-lookup"><span data-stu-id="9948d-140">The registry value under ENDPOINTDLP_ENABLED_FLAG_REGKEY containing the DLP enabled flag registry key</span></span>

## <a name="endpoint-dlp-apis"></a><span data-ttu-id="9948d-141">Endpunkt-DLP-APIs</span><span class="sxs-lookup"><span data-stu-id="9948d-141">Endpoint DLP APIs</span></span>

<span data-ttu-id="9948d-142">In den folgenden Tabellen sind die von der Endpunkt-DLP-DLL bereitgestellten APIs aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="9948d-142">The following tables list the APIs provided by the endpoint DLP dll.</span></span>

### <a name="initialization-and-versioning"></a><span data-ttu-id="9948d-143">Initialisierung und Versionsvererbung</span><span class="sxs-lookup"><span data-stu-id="9948d-143">Initialization and versioning</span></span>

| <span data-ttu-id="9948d-144">API</span><span class="sxs-lookup"><span data-stu-id="9948d-144">API</span></span> | <span data-ttu-id="9948d-145">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9948d-145">Description</span></span> |
|-----|-------------|
| [<span data-ttu-id="9948d-146">DlpInitializeEnforcementMode</span><span class="sxs-lookup"><span data-stu-id="9948d-146">DlpInitializeEnforcementMode</span></span>](endpointdlp-dlpinitializeenforcementmode.md)                       | <span data-ttu-id="9948d-147">Benachrichtigt das System über die gewünschten Erzwingungsmodi für eine Reihe von Endpunktvorgängen zur Verhinderung von Datenverlust (Data Loss Prevention, DLP).</span><span class="sxs-lookup"><span data-stu-id="9948d-147">Notifies the system of the desired enforcement modes for a set of endpoint Data Loss Prevention (DLP) operations.</span></span>                                  |
| [<span data-ttu-id="9948d-148">DlpGetEnforcementApiVersion</span><span class="sxs-lookup"><span data-stu-id="9948d-148">DlpGetEnforcementApiVersion</span></span>](endpointdlp-dlpgetenforcementapiversion.md)                       | <span data-ttu-id="9948d-149">Ruft die Version der DLP-API (Data Loss Prevention) des Endpunkts auf dem aktuellen Gerät ab.</span><span class="sxs-lookup"><span data-stu-id="9948d-149">Retrieves the version of the endpoint Data Loss Prevention (DLP) API on the current device.</span></span>                                  |


### <a name="document-operations"></a><span data-ttu-id="9948d-150">Dokumentenvorgänge</span><span class="sxs-lookup"><span data-stu-id="9948d-150">Document operations</span></span>

| <span data-ttu-id="9948d-151">API</span><span class="sxs-lookup"><span data-stu-id="9948d-151">API</span></span> | <span data-ttu-id="9948d-152">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9948d-152">Description</span></span> |
|-----|-------------|
| [<span data-ttu-id="9948d-153">DlpNotifyPreOpenDocument</span><span class="sxs-lookup"><span data-stu-id="9948d-153">DlpNotifyPreOpenDocument</span></span>](endpointdlp-dlpnotifypreopendocument.md) | <span data-ttu-id="9948d-154">Stellt dem System Informationen zu einem Dokument bereit, bevor der Öffnungsvorgang initiiert wird.</span><span class="sxs-lookup"><span data-stu-id="9948d-154">Provides the system with information about a document before the open operation is initiated.</span></span> |
| [<span data-ttu-id="9948d-155">DlpNotifyPostOpenDocument</span><span class="sxs-lookup"><span data-stu-id="9948d-155">DlpNotifyPostOpenDocument</span></span>](endpointdlp-dlpnotifypostopendocument.md) | <span data-ttu-id="9948d-156">Stellt dem System Informationen zu einem Dokument bereit, nachdem der Öffnungsvorgang abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="9948d-156">Provides the system with information about a document after the open operation is completed.</span></span>  |
| [<span data-ttu-id="9948d-157">DlpNotifyCloseDocument</span><span class="sxs-lookup"><span data-stu-id="9948d-157">DlpNotifyCloseDocument</span></span>](endpointdlp-dlpnotifyclosedocument.md)                       | <span data-ttu-id="9948d-158">Stellt dem System Informationen zu einem Dokument bereit, bevor der Vorgang zum Schließen des Dokuments initiiert wird.</span><span class="sxs-lookup"><span data-stu-id="9948d-158">Provides the system with information about a document before the document close operation is initiated.</span></span>                                  |
| [<span data-ttu-id="9948d-159">DlpNotifyPreOpenDocumentFile</span><span class="sxs-lookup"><span data-stu-id="9948d-159">DlpNotifyPreOpenDocumentFile</span></span>](endpointdlp-dlpnotifypreopendocumentfile.md)                         | <span data-ttu-id="9948d-160">Stellt dem System Informationen zu einem Dokument bereit, bevor der Öffnungsvorgang initiiert wird.</span><span class="sxs-lookup"><span data-stu-id="9948d-160">Provides the system with information about a document before the open operation is initiated.</span></span>  |
| [<span data-ttu-id="9948d-161">DlpNotifyPostOpenDocumentFile</span><span class="sxs-lookup"><span data-stu-id="9948d-161">DlpNotifyPostOpenDocumentFile</span></span>](endpointdlp-dlpnotifypostopendocumentfile.md)                       | <span data-ttu-id="9948d-162">Stellt dem System Informationen zu einem Dokument bereit, nachdem der Öffnungsvorgang abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="9948d-162">Provides the system with information about a document after the open operation is completed.</span></span>                                  |
| [<span data-ttu-id="9948d-163">DlpNotifyCloseDocumentFile</span><span class="sxs-lookup"><span data-stu-id="9948d-163">DlpNotifyCloseDocumentFile</span></span>](endpointdlp-dlpnotifyclosedocumentfile.md)                       | <span data-ttu-id="9948d-164">Stellt dem System Informationen zu einem Dokument bereit, bevor der Vorgang zum Schließen des Dokuments initiiert wird.</span><span class="sxs-lookup"><span data-stu-id="9948d-164">Provides the system with information about a document before the document close operation is initiated.</span></span>                                  |

### <a name="save-as-operations"></a><span data-ttu-id="9948d-165">Speichern als Vorgänge</span><span class="sxs-lookup"><span data-stu-id="9948d-165">Save as operations</span></span>
| <span data-ttu-id="9948d-166">API</span><span class="sxs-lookup"><span data-stu-id="9948d-166">API</span></span> | <span data-ttu-id="9948d-167">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9948d-167">Description</span></span> |
|-----|-------------|
| [<span data-ttu-id="9948d-168">DlpNotifyPreSaveAsDocument</span><span class="sxs-lookup"><span data-stu-id="9948d-168">DlpNotifyPreSaveAsDocument</span></span>](endpointdlp-dlpnotifypresaveasdocument.md)                       | <span data-ttu-id="9948d-169">Stellt dem System Informationen zu einem Dokument bereit, bevor ein Save-as-Vorgang initiiert wird.</span><span class="sxs-lookup"><span data-stu-id="9948d-169">Provides the system with information about a document before a save as operation is initiated.</span></span>                                  |
| [<span data-ttu-id="9948d-170">DlpNotifyPostSaveAsDocument</span><span class="sxs-lookup"><span data-stu-id="9948d-170">DlpNotifyPostSaveAsDocument</span></span>](endpointdlp-dlpnotifypostsaveasdocument.md)                       | <span data-ttu-id="9948d-171">Stellt dem System Informationen zu einem Dokument bereit, nachdem der Vorgang speichern unter abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="9948d-171">Provides the system with information about a document after the save as operation is completed.</span></span>                                  |


### <a name="drag-and-drop-operations"></a><span data-ttu-id="9948d-172">Drag &amp; Drop-Vorgänge</span><span class="sxs-lookup"><span data-stu-id="9948d-172">Drag and drop operations</span></span>

| <span data-ttu-id="9948d-173">API</span><span class="sxs-lookup"><span data-stu-id="9948d-173">API</span></span> | <span data-ttu-id="9948d-174">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9948d-174">Description</span></span> |
|-----|-------------|
| [<span data-ttu-id="9948d-175">DlpNotifyEnterDropTarget</span><span class="sxs-lookup"><span data-stu-id="9948d-175">DlpNotifyEnterDropTarget</span></span>](endpointdlp-dlpnotifyenterdroptarget.md)                       | <span data-ttu-id="9948d-176">Stellt dem System Informationen zu einem Dokument bereit, wenn ein Ablageziel eingegeben wird.</span><span class="sxs-lookup"><span data-stu-id="9948d-176">Provides the system with information about a document when a drop target is entered.</span></span>                                  |
| [<span data-ttu-id="9948d-177">DlpNotifyLeaveDropTarget</span><span class="sxs-lookup"><span data-stu-id="9948d-177">DlpNotifyLeaveDropTarget</span></span>](endpointdlp-dlpnotifyleavedroptarget.md)                       | <span data-ttu-id="9948d-178">Stellt dem System Informationen zu einem Dokument zur Verfügung, wenn ein Abbruchziel beendet wird.</span><span class="sxs-lookup"><span data-stu-id="9948d-178">Provides the system with information about a document when a drop target is exited.</span></span>                                  |
| [<span data-ttu-id="9948d-179">DlpNotifyPreDragDrop</span><span class="sxs-lookup"><span data-stu-id="9948d-179">DlpNotifyPreDragDrop</span></span>](endpointdlp-dlpnotifypredragdrop.md)                         | <span data-ttu-id="9948d-180">Stellt dem System Informationen zu einem Dokument zur Verfügung, bevor ein Drag Drop-Vorgang initiiert wird.</span><span class="sxs-lookup"><span data-stu-id="9948d-180">Provides the system with information about a document before a drag drop operation is initiated.</span></span>  |
| [<span data-ttu-id="9948d-181">DlpNotifyPostDragDrop</span><span class="sxs-lookup"><span data-stu-id="9948d-181">DlpNotifyPostDragDrop</span></span>](endpointdlp-dlpnotifypostdragdrop.md)                         | <span data-ttu-id="9948d-182">Stellt dem System Nach Abschluss eines Drag &amp; Drop-Vorgangs Informationen zu einem Dokument zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="9948d-182">Provides the system with information about a document after a drag drop operation is completed.</span></span>  |


### <a name="clipboard-operations"></a><span data-ttu-id="9948d-183">Zwischenablagevorgänge</span><span class="sxs-lookup"><span data-stu-id="9948d-183">Clipboard operations</span></span>

| <span data-ttu-id="9948d-184">API</span><span class="sxs-lookup"><span data-stu-id="9948d-184">API</span></span> | <span data-ttu-id="9948d-185">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9948d-185">Description</span></span> |
|-----|-------------|
| [<span data-ttu-id="9948d-186">DlpNotifyPreCopyToClipboard</span><span class="sxs-lookup"><span data-stu-id="9948d-186">DlpNotifyPreCopyToClipboard</span></span>](endpointdlp-dlpnotifyprecopytoclipboard.md)                         | <span data-ttu-id="9948d-187">Stellt dem System Informationen zu einem Dokument zur Verfügung, bevor ein Kopiervorgang in die Zwischenablage initiiert wird.</span><span class="sxs-lookup"><span data-stu-id="9948d-187">Provides the system with information about a document before a copy to clipboard operation is initiated.</span></span>  |
| [<span data-ttu-id="9948d-188">DlpNotifyPostCopyToClipboard</span><span class="sxs-lookup"><span data-stu-id="9948d-188">DlpNotifyPostCopyToClipboard</span></span>](endpointdlp-dlpnotifypostcopytoclipboard.md)                         | <span data-ttu-id="9948d-189">Stellt dem System Informationen zu einem Dokument zur Verfügung, nachdem ein Kopiervorgang in die Zwischenablage abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="9948d-189">Provides the system with information about a document after a copy to clipboard operation is completed.</span></span>  |
| [<span data-ttu-id="9948d-190">DlpNotifyPrePasteFromClipboard</span><span class="sxs-lookup"><span data-stu-id="9948d-190">DlpNotifyPrePasteFromClipboard</span></span>](endpointdlp-dlpnotifyprepastefromclipboard.md)                         | <span data-ttu-id="9948d-191">Stellt dem System Informationen zu einem Dokument zur Verfügung, bevor ein Einfügevorgang aus der Zwischenablage initiiert wird.</span><span class="sxs-lookup"><span data-stu-id="9948d-191">Provides the system with information about a document before a paste from clipboard operation is initiated.</span></span>  |
| [<span data-ttu-id="9948d-192">DlpNotifyPostPasteFromClipboard</span><span class="sxs-lookup"><span data-stu-id="9948d-192">DlpNotifyPostPasteFromClipboard</span></span>](endpointdlp-dlpnotifypostpastefromclipboard.md)                       | <span data-ttu-id="9948d-193">Stellt dem System Informationen zu einem Dokument zur Verfügung, nachdem ein Einfügevorgang aus der Zwischenablage abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="9948d-193">Provides the system with information about a document after a paste from clipboard operation has completed.</span></span>                                  |
| [<span data-ttu-id="9948d-194">DlpNotifyPostStashClipboard</span><span class="sxs-lookup"><span data-stu-id="9948d-194">DlpNotifyPostStashClipboard</span></span>](endpointdlp-dlpnotifypoststashclipboard.md)                       | <span data-ttu-id="9948d-195">Stellt dem System Nach Abschluss eines Stash-Zwischenablage-Vorgangs Statusinformationen zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="9948d-195">Provides the system with status information after a stash clipboard operation is completed.</span></span>                                  |
| [<span data-ttu-id="9948d-196">DlpNotifyPreStashClipboard</span><span class="sxs-lookup"><span data-stu-id="9948d-196">DlpNotifyPreStashClipboard</span></span>](endpointdlp-dlpnotifyprestashclipboard.md)                       | <span data-ttu-id="9948d-197">Benachrichtigt das System, bevor ein Stash-Zwischenablagevorgang initiiert wird.</span><span class="sxs-lookup"><span data-stu-id="9948d-197">Notifies the system before a stash clipboard operation is initiated.</span></span>                                  |
| [<span data-ttu-id="9948d-198">DlpMustPasteFromSystemClipboard</span><span class="sxs-lookup"><span data-stu-id="9948d-198">DlpMustPasteFromSystemClipboard</span></span>](endpointdlp-dlpmustpastefromsystemclipboard.md)                       | <span data-ttu-id="9948d-199">Bestimmt, ob die App die Daten aus der Systemablage pullen muss, anstatt sie aus ihrem internen Cache zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="9948d-199">Determines whether the app must pull the data from the system clipboard rather than taking it from its internal cache.</span></span>                                  |

### <a name="print-operations"></a><span data-ttu-id="9948d-200">Druckvorgänge</span><span class="sxs-lookup"><span data-stu-id="9948d-200">Print operations</span></span>

| <span data-ttu-id="9948d-201">API</span><span class="sxs-lookup"><span data-stu-id="9948d-201">API</span></span> | <span data-ttu-id="9948d-202">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9948d-202">Description</span></span> |
|-----|-------------|
| [<span data-ttu-id="9948d-203">DlpNotifyPrePrint</span><span class="sxs-lookup"><span data-stu-id="9948d-203">DlpNotifyPrePrint</span></span>](endpointdlp-dlpnotifypreprint.md)                         | <span data-ttu-id="9948d-204">Stellt dem System Informationen zu einem Dokument bereit, bevor ein Druckvorgang initiiert wird.</span><span class="sxs-lookup"><span data-stu-id="9948d-204">Provides the system with information about a document before a print operation is initiated.</span></span>  |
| [<span data-ttu-id="9948d-205">DlpNotifyPostStartPrint</span><span class="sxs-lookup"><span data-stu-id="9948d-205">DlpNotifyPostStartPrint</span></span>](endpointdlp-dlpnotifypoststartprint.md)                       | <span data-ttu-id="9948d-206">Stellt dem System Informationen zu einem Dokument bereit, nachdem ein Druckvorgang gestartet wurde.</span><span class="sxs-lookup"><span data-stu-id="9948d-206">Provides the system with information about a document after an print operation has started.</span></span>                                  |
| [<span data-ttu-id="9948d-207">DlpNotifyPostPrint</span><span class="sxs-lookup"><span data-stu-id="9948d-207">DlpNotifyPostPrint</span></span>](endpointdlp-dlpnotifypostprint.md)                       | <span data-ttu-id="9948d-208">Stellt dem System Informationen zu einem Dokument bereit, nachdem ein Druckvorgang abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="9948d-208">Provides the system with information about a document after a print operation has completed.</span></span>                                  |

## <a name="endpoint-dlp-example-header"></a><span data-ttu-id="9948d-209">Endpunkt-DLP-Beispielheader</span><span class="sxs-lookup"><span data-stu-id="9948d-209">Endpoint DLP example header</span></span>

<span data-ttu-id="9948d-210">Da der Endpunkt-DLP-Header nicht im Windows SDK enthalten ist, müssen Sie die Headerdatei selbst erstellen, um API-Signaturen abzurufen, die in Ihrer Implementierung verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="9948d-210">Because the endpoint DLP header is not included in the Windows SDK, you must create the header file yourself to get API signatures to use in your implementation.</span></span> <span data-ttu-id="9948d-211">Zur Vereinfachung stellen wir Beispielcode bereit, den Sie kopieren und in Ihre Anwendung einfügen können.</span><span class="sxs-lookup"><span data-stu-id="9948d-211">For your convenience we're providing example code that you can copy and paste into your application.</span></span> <span data-ttu-id="9948d-212">Zusätzlich zu Funktionsdeklarationen definiert diese Codeauflistung auch nützliche Konstanten wie Versionsinformationen und Registrierungsschlüsselpfade.</span><span class="sxs-lookup"><span data-stu-id="9948d-212">In addition to function declarations, this code listing also defines useful constants such as versioning information and registry key paths.</span></span>

```cpp
//
// EndpointDlp DLL name containing the Endpoint DLP API
//

#define ENDPOINTDLP_DLL_NAME L"EndpointDlp.dll"

//
// Windows Defender registry key under HKLM where some Endpoint DLP settings are stored
//

#define ENDPOINTDLP_WINDOWS_DEFENDER_REGKEY L"SOFTWARE\\Microsoft\\Windows Defender"

//
// EndpointDlp.dll install location can be obtained from the registry under the following HKLM key
//

#define ENDPOINTDLP_DLL_INSTALL_LOCATION_REGKEY ENDPOINTDLP_WINDOWS_DEFENDER_REGKEY

//
// EndpointDlp.dll install location is stored under ENDPOINTDLP_DLL_INSTALL_LOCATION_REGKEY in the following registry value
//

#define ENDPOINTDLP_DLL_INSTALL_LOCATION_REGVALUE L"InstallLocation"

//
// On x64 platforms, concatanate the following directory to obtain the x86 version of EndpointDlp.dll
//

#define ENDPOINTDLP_DLL_WOW64_X86_INSTALL_LOCATION_SUFFIX L"x86"

//
// Endpoint DLP enabled flag can be found under the following HKLM key
//

#define ENDPOINTDLP_ENABLED_FLAG_REGKEY ENDPOINTDLP_WINDOWS_DEFENDER_REGKEY L"\\Features"

//
// Endpoint DLP enabled flag can be found under ENDPOINTDLP_ENABLED_REGKEY in the following registry value
//

#define ENDPOINTDLP_ENABLED_FLAG_REGVALUE L"SenseDlpEnabled"


#define DLP_DOCUMENT_INFO_V_1 0x1     

#define DLP_DOCUMENT_INFO_V_LATEST DLP_DOCUMENT_INFO_V_1


//
//  Enlightened app enforcement capablities.
//

typedef enum _DlpAppEnforceLevel {
    DlpAppEnforceLevelNone = 0, // No enforcement, DLP enforces operation.
    DlpAppEnforceLevelNotify,   // App send notifications on operation, DLP enforces operation.
    DlpAppEnforceLevelPrevent,  // Currently not supported (App allows or blocks operation, DLP enforces warning, eventing and UI). 
    DlpAppEnforceLevelFull,     // Currently not supported (App handles all enforcement (blocks operation, enforces warning, UI), DLP will only handle auditing.)
    DlpAppEnforceLevelCount,
}DlpAppEnforceLevel;

typedef enum  
{
    DlpActionTypeCopyToRemovableMedia = 0,
    DlpActionTypeCopyToNetworkShare = 1,
    DlpActionTypeCopyToClipboard = 2,
    DlpActionTypePrint = 3,
    DlpActionTypeScreenClip = 4,
    DlpActionTypeAccessByUnallowedApp = 5,
    DlpActionTypeCloudAppEgress = 6,
    DlpActionTypeAccessByBluetoothApp = 7,
    DlpActionTypeAccessByRDPApp = 8,
    DlpActionTypeCount = 9
} DlpActionType;
    
//
//  The stucture describes the enforcement level for each operation.
//
    
typedef struct _DLP_APP_OP_ENLIGHTENED_LEVEL{
    DlpActionType Operation;
    DlpAppEnforceLevel AppEnforcementLevel;
}DLP_APP_OP_ENLIGHTENED_LEVEL, *PDLP_APP_OP_ENLIGHTENED_LEVEL;


/*
Function description:
     The application calls this functio to declares the enforcement level for each operation.

Parameters:
    _In_ DWORD Count - Number of operations. 
    _In_reads_opt_(Count) PDLP_APP_OP_ENLIGHTENED_LEVEL* OperationEnforcement - Array indicating operations
    supported by the application and enforcement level:
        DlpAppEnforceLevelNone - No enforcement, DLP enforces operation.
        DlpAppEnforceLevelNotify -  App send notifications on operation, DLP enforces operation.

Return:
    S_OK - Function completed successfully.
    E_INVALIDARG - Invalid parameters passed to function.
    E_OUTOFMEMORY - Memory allocation failed.
    E_XXX - Varius error codes.
*/       
HRESULT WINAPI DlpInitializeEnforcementMode(_In_ DWORD Count, _In_reads_(Count) PDLP_APP_OP_ENLIGHTENED_LEVEL OperationEnforcement);


/*
Function description:
    Returns the version of the enforcement API.
    MajorVersion indicates a new interfaces/API.
    MinorVersion indicates changes to existing interfaces/API-s.
   
Parameters:
    None.

Return:
    S_OK - Function completed successfully
    E_XXX - Varius error codes.
*/
HRESULT WINAPI DlpGetEnforcementApiVersion(_Out_ DWORD* MajorVersion, _Out_ DWORD* MinorVersion);


typedef struct _DLP_DOCUMENT_INFO {

    //
    //  Information version. Always set it to DLP_DOCUMENT_INFO_V_LATEST
    //
    
    DWORD Version;

    //
    //  Original path of the document.
    //  
    
    LPCWSTR PersistentFileName;

    //
    //  Path to the real backing file.
    //
    
    LPCWSTR LocalFileName;

}DLP_DOCUMENT_INFO, *PDLP_DOCUMENT_INFO;

//
//  Post operation status information.
//
    
#define DLP_POSTOP_STATUS_V_1 0x1     
        
#define DLP_POSTOP_STATUS_V_LATEST DLP_POSTOP_STATUS_V_1;
    
       
typedef struct _DLP_POSTOP_STATUS {

    //
    //  Information version. Always set it to DLP_POSTOP_STATUS_V_LATEST
    //
    
    DWORD Version;

    //
    //  Set to TRUE if app's operation succeeded, FALSE otherwise. 
    //
    
    BOOL OperationSuccess;  

} DLP_POSTOP_STATUS, *PDLP_POSTOP_STATUS;    


#define DLP_PRINT_INFO_V_1 0x1     
    
#define DLP_PRINT_INFO_V_LATEST DLP_PRINT_INFO_V_1;

typedef struct _DLP_PRINT_INFO {

    //
    //  Information version. Always set it to DLP_PRINT_INFO_V_LATEST
    //
    
    DWORD Version;

    //
    //  Destination printer.
    //
    
    LPCWSTR PrinterName;

    //
    //  Print job name.
    //
    
    LPCWSTR JobName;

    //
    //  Output file, if printing to file.
    //

    LPCWSTR OutputFileName;
    
}DLP_PRINT_INFO, *PDLP_PRINT_INFO;

    
void WINAPI DlpNotifyPreOpenDocument(_In_ const PDLP_DOCUMENT_INFO DocumentInfo);
void WINAPI DlpNotifyPostOpenDocument(_In_ const PDLP_DOCUMENT_INFO DocumentInfo, _In_ const PDLP_POSTOP_STATUS OpStatus); 

void WINAPI DlpNotifyCloseDocument(_In_ const PDLP_DOCUMENT_INFO DocumentInfo);

void WINAPI DlpNotifyPreOpenDocumentFile(_In_ const PDLP_DOCUMENT_INFO DocumentInfo);
void WINAPI DlpNotifyPostOpenDocumentFile(_In_ const PDLP_DOCUMENT_INFO DocumentInfo, _In_ const PDLP_POSTOP_STATUS OpStatus); 

void WINAPI DlpNotifyCloseDocumentFile(_In_ const PDLP_DOCUMENT_INFO DocumentInfo);

void WINAPI DlpNotifyPreSaveAsDocument(_In_ const PDLP_DOCUMENT_INFO DocumentInfo, _In_ LPCWSTR Destination);
void WINAPI DlpNotifyPostSaveAsDocument(_In_ const PDLP_DOCUMENT_INFO DocumentInfo, _In_ LPCWSTR Destination, _In_ const PDLP_POSTOP_STATUS OpStatus); 

void WINAPI DlpNotifyPrePrint(_In_ const PDLP_DOCUMENT_INFO DocumentInfo, _In_ const PDLP_PRINT_INFO PrintInfo);
void WINAPI DlpNotifyPostStartPrint(_In_ const PDLP_DOCUMENT_INFO DocumentInfo, _In_ const PDLP_PRINT_INFO PrintInfo);
void WINAPI DlpNotifyPostPrint(_In_ const PDLP_DOCUMENT_INFO DocumentInfo, _In_ const PDLP_PRINT_INFO PrintInfo, _In_ const PDLP_POSTOP_STATUS OpStatus);

void WINAPI DlpNotifyPreCopyToClipboard(_In_ const PDLP_DOCUMENT_INFO DocumentInfo);
void WINAPI DlpNotifyPostCopyToClipboard(_In_ const PDLP_DOCUMENT_INFO DocumentInfo, _In_ const PDLP_POSTOP_STATUS OpStatus);

void WINAPI DlpNotifyPrePasteFromClipboard(_In_ const PDLP_DOCUMENT_INFO DocumentInfo);
void WINAPI DlpNotifyPostPasteFromClipboard(_In_ const PDLP_DOCUMENT_INFO DocumentInfo, _In_ const PDLP_POSTOP_STATUS OpStatus);

void WINAPI DlpNotifyPreStashClipboard();
void WINAPI DlpNotifyPostStashClipboard(_In_ const PDLP_POSTOP_STATUS OpStatus);

void WINAPI DlpNotifyPreDragDrop(_In_ const PDLP_DOCUMENT_INFO DocumentInfo);
void WINAPI DlpNotifyPostDragDrop(_In_ const PDLP_DOCUMENT_INFO DocumentInfo, _In_ const PDLP_POSTOP_STATUS OpStatus);
    
void WINAPI DlpNotifyEnterDropTarget(_In_ const PDLP_DOCUMENT_INFO DocumentInfo);
void WINAPI DlpNotifyLeaveDropTarget(_In_ const PDLP_DOCUMENT_INFO DocumentInfo, _In_ const PDLP_POSTOP_STATUS OpStatus); 


/*
Function description:
    Determines whether the app must pull the data from the system clipboard rather than taking it from its internal cache.

Parameters:
    None

Return:
    TRUE if calling into the OS clipboard is mandatory, FALSE otherwise
*/
BOOL WINAPI DlpMustPasteFromSystemClipboard();

```


