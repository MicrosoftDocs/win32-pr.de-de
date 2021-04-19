---
description: Die WMI-Protokolldateien werden nicht mehr unterstützt.
ms.assetid: 4ba80063-7aa6-42df-a620-1b366b795034
ms.tgt_platform: multiple
title: Protokollieren der WMI-Aktivität
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6ced8645eb7ad9005e6ba751d011ae7f0ccb3dd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106348126"
---
# <a name="logging-wmi-activity"></a><span data-ttu-id="45234-103">Protokollieren der WMI-Aktivität</span><span class="sxs-lookup"><span data-stu-id="45234-103">Logging WMI Activity</span></span>

<span data-ttu-id="45234-104">Die WMI-Protokolldateien werden nicht mehr unterstützt.</span><span class="sxs-lookup"><span data-stu-id="45234-104">The WMI log files are no longer supported.</span></span> <span data-ttu-id="45234-105">Ab Windows Vista verwendet WMI die [Ereignis Ablauf Verfolgung für Windows (Event Tracing for Windows, etw](/windows/desktop/ETW/event-tracing-portal)) und Ereignisse, die über die **Ereignisanzeige** -Benutzeroberfläche oder das Befehlszeilen Tool wevtutil verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="45234-105">Starting with Windows Vista, WMI uses [Event Tracing for Windows (ETW](/windows/desktop/ETW/event-tracing-portal)) and events that are available through the **Event Viewer** UI or the Wevtutil command line tool.</span></span> <span data-ttu-id="45234-106">Weitere Informationen finden Sie unter der ETW-Anbieter und in der Befehlszeilen Dokumentation von [wevutil](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/cc732848(v=ws.11)) .</span><span class="sxs-lookup"><span data-stu-id="45234-106">For more information, see the ETW provider and the [Wevutil](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/cc732848(v=ws.11)) command-line documentation.</span></span>

<span data-ttu-id="45234-107">In diesem Thema werden die folgenden Abschnitte erläutert:</span><span class="sxs-lookup"><span data-stu-id="45234-107">The following sections are discussed in this topic:</span></span>

-   [<span data-ttu-id="45234-108">WMI-Protokolldateien vor Windows Vista</span><span class="sxs-lookup"><span data-stu-id="45234-108">WMI Log Files Before Windows Vista</span></span>](#wmi-log-files-before-windows-vista)
-   [<span data-ttu-id="45234-109">Protokollieren von Aktivitäten für WMI-Kernkomponenten vor Windows Vista</span><span class="sxs-lookup"><span data-stu-id="45234-109">Logging Activities for WMI Core Components Before Windows Vista</span></span>](#logging-activities-for-wmi-core-components-before-windows-vista)
-   [<span data-ttu-id="45234-110">Protokollieren von Aktivitäten für WMI-Anbieter Komponenten vor Windows Vista</span><span class="sxs-lookup"><span data-stu-id="45234-110">Logging Activities for WMI Provider Components Before Windows Vista</span></span>](#logging-activities-for-wmi-provider-components-before-windows-vista)
-   [<span data-ttu-id="45234-111">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="45234-111">Related topics</span></span>](#related-topics)

## <a name="wmi-log-files-before-windows-vista"></a><span data-ttu-id="45234-112">WMI-Protokolldateien vor Windows Vista</span><span class="sxs-lookup"><span data-stu-id="45234-112">WMI Log Files Before Windows Vista</span></span>

<span data-ttu-id="45234-113">Die von WMI und verschiedenen Anbietern erstellten Protokolldateien zeichnen auf: Ereignisse, Ablauf Verfolgungs-oder Diagnosedaten, Fehler und verschiedene Aktivitäten.</span><span class="sxs-lookup"><span data-stu-id="45234-113">The log files created by WMI and various providers record: events, trace or diagnostic data, errors, and various activities.</span></span> <span data-ttu-id="45234-114">Nur Administratoren verfügen über Lesezugriff auf den WMI-Protokoll Ordner unter% windir% \\ system32 \\ WBEM \\ Logs.</span><span class="sxs-lookup"><span data-stu-id="45234-114">Only administrators have read access to the WMI log folder found at %windir%\\system32\\wbem\\logs.</span></span>

<span data-ttu-id="45234-115">Nur WMI-Kernkomponenten oder WMI-Anbieter schreiben in Protokolldateien.</span><span class="sxs-lookup"><span data-stu-id="45234-115">Only WMI core components or WMI providers write to log files.</span></span> <span data-ttu-id="45234-116">Sie können die Daten in diesen Protokollen nur zu Diagnose Zwecken lesen oder anzeigen.</span><span class="sxs-lookup"><span data-stu-id="45234-116">You can only read or view the data in these logs for diagnostic purposes.</span></span> <span data-ttu-id="45234-117">Sie können eigene Protokolldateien im WMI-Protokoll Verzeichnis erstellen und speichern.</span><span class="sxs-lookup"><span data-stu-id="45234-117">You can create and store your own log files in the WMI log directory.</span></span>

## <a name="logging-activities-for-wmi-core-components-before-windows-vista"></a><span data-ttu-id="45234-118">Protokollieren von Aktivitäten für WMI-Kernkomponenten vor Windows Vista</span><span class="sxs-lookup"><span data-stu-id="45234-118">Logging Activities for WMI Core Components Before Windows Vista</span></span>

<span data-ttu-id="45234-119">Diese Dateien enthalten kein konsistentes Format, das zum programmgesteuerten Lesen geeignet ist.</span><span class="sxs-lookup"><span data-stu-id="45234-119">These files do not contain a consistent format that is suitable for reading programmatically.</span></span> <span data-ttu-id="45234-120">Weitere Informationen zu bestimmten Protokollen finden Sie unter [WMI-Protokolldateien](wmi-log-files.md).</span><span class="sxs-lookup"><span data-stu-id="45234-120">For more information about specific logs, see [WMI Log Files](wmi-log-files.md).</span></span>

<span data-ttu-id="45234-121">Protokollierungs Aktivitäten für WMI-Kernkomponenten treten auf, wenn die folgenden Registrierungsschlüssel festgelegt sind:</span><span class="sxs-lookup"><span data-stu-id="45234-121">Logging activities for WMI core components occurs when the following registry keys are set:</span></span>

-   <span data-ttu-id="45234-122">Protokolliergrad</span><span class="sxs-lookup"><span data-stu-id="45234-122">Logging level</span></span>

    <span data-ttu-id="45234-123">Änderungen am Registrierungs Wert der Protokollierungsebene treten sofort in Kraft.</span><span class="sxs-lookup"><span data-stu-id="45234-123">Changes to the logging level registry value take effect immediately.</span></span> <span data-ttu-id="45234-124">Der WMI-Dienst muss nicht neu gestartet werden.</span><span class="sxs-lookup"><span data-stu-id="45234-124">No restart of the WMI service is necessary.</span></span>

    <span data-ttu-id="45234-125">**HKEY \_ Lokale \_ Computer** \\ **Software** \\ **Microsoft** \\ **WBEM** \\ **CIMOM** \\ **Logging** = 2</span><span class="sxs-lookup"><span data-stu-id="45234-125">**HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**\\**WBEM**\\**CIMOM**\\**Logging** = 2</span></span>

    <span data-ttu-id="45234-126">In der folgenden Liste sind die Protokolliergrade aufgelistet, die in der Registrierung definiert werden können.</span><span class="sxs-lookup"><span data-stu-id="45234-126">The following list lists the logging levels that can be defined in the registry.</span></span>

    

    | <span data-ttu-id="45234-127">Protokolliergrad</span><span class="sxs-lookup"><span data-stu-id="45234-127">Logging level</span></span> | <span data-ttu-id="45234-128">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="45234-128">Description</span></span>               |
    |---------------|---------------------------|
    | <span data-ttu-id="45234-129">0</span><span class="sxs-lookup"><span data-stu-id="45234-129">0</span></span>             | <span data-ttu-id="45234-130">Keine Protokollierung</span><span class="sxs-lookup"><span data-stu-id="45234-130">No Logging</span></span>                |
    | <span data-ttu-id="45234-131">1</span><span class="sxs-lookup"><span data-stu-id="45234-131">1</span></span>             | <span data-ttu-id="45234-132">Nur Fehler protokollieren</span><span class="sxs-lookup"><span data-stu-id="45234-132">Log only errors</span></span>           |
    | <span data-ttu-id="45234-133">2</span><span class="sxs-lookup"><span data-stu-id="45234-133">2</span></span>             | <span data-ttu-id="45234-134">Ausführliche Protokollierung (Standard)</span><span class="sxs-lookup"><span data-stu-id="45234-134">Verbose Logging (default)</span></span> |

    

     

-   <span data-ttu-id="45234-135">Speicherort der Protokolldatei</span><span class="sxs-lookup"><span data-stu-id="45234-135">Log file location</span></span>

    <span data-ttu-id="45234-136">Damit Änderungen am Speicherort der Protokolldatei wirksam werden, starten Sie den WMI-Dienst neu.</span><span class="sxs-lookup"><span data-stu-id="45234-136">For changes to log file location to take effect, restart the WMI service.</span></span>

    <span data-ttu-id="45234-137">**HKEY \_ Lokale \_ Computer** \\ **Software** \\ **Microsoft** \\ **WBEM** \\ **CIMOM** \\ **Logging Directory** =% windir% \\ system32 \\ WBEM \\ Logs</span><span class="sxs-lookup"><span data-stu-id="45234-137">**HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**\\**WBEM**\\**CIMOM**\\**Logging Directory** = %windir%\\system32\\wbem\\logs</span></span>

-   <span data-ttu-id="45234-138">Maximale Protokolldatei Größe in Bytes</span><span class="sxs-lookup"><span data-stu-id="45234-138">Maximum log file size, in bytes</span></span>

    <span data-ttu-id="45234-139">**HKEY \_ Lokale \_ Computer** \\ **Software** \\ **Microsoft** \\ **WBEM** \\ **CIMOM**- \\ **Protokolldatei maximale Größe** = 65536</span><span class="sxs-lookup"><span data-stu-id="45234-139">**HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**\\**WBEM**\\**CIMOM**\\**Log File Max Size** = 65536</span></span>

<span data-ttu-id="45234-140">Sie können diese Registrierungsschlüssel Werte über den Registrierungs-Editor oder über das WMI-Snap-in für die Microsoft Management Console ändern.</span><span class="sxs-lookup"><span data-stu-id="45234-140">You can change these registry key values through the Registry Editor or through the WMI snap-in for the Microsoft Management Console.</span></span>

<span data-ttu-id="45234-141">**So legen Sie den Protokolliergrad für WMI vor Windows Vista fest**</span><span class="sxs-lookup"><span data-stu-id="45234-141">**To set the logging level for WMI before Windows Vista**</span></span>

1.  <span data-ttu-id="45234-142">Klicken Sie im **Startmenü** auf **Ausführen**.</span><span class="sxs-lookup"><span data-stu-id="45234-142">Click **Start**, and then click **Run**.</span></span>
2.  <span data-ttu-id="45234-143">Geben Sie **Wmimgmt. msc ein.**</span><span class="sxs-lookup"><span data-stu-id="45234-143">Type **wmimgmt.msc**</span></span>
3.  <span data-ttu-id="45234-144">Klicken Sie im Menü **Aktion** auf **Eigenschaften**.</span><span class="sxs-lookup"><span data-stu-id="45234-144">On the **Action** menu, click **Properties**.</span></span>
4.  <span data-ttu-id="45234-145">Legen Sie auf der Registerkarte **Protokollierung** den Protokolliergrad auf **deaktiviert**, **aktiviert** **oder ausführlich** fest.</span><span class="sxs-lookup"><span data-stu-id="45234-145">On the **Logging** tab, set the logging level to **Disabled**, **Enabled**, or **Verbose**.</span></span>
5.  <span data-ttu-id="45234-146">Geben Sie unter **Speicherort:** den Pfad zum Protokolldatei Ordner und in **Maximale Größe (Bytes)** ein, und legen Sie die maximale Größe (in Bytes) der Protokolldatei fest.</span><span class="sxs-lookup"><span data-stu-id="45234-146">In **Location:**, type the path to the log file folder and in **Maximum size (bytes):**, set the maximum size, in bytes, of the log file.</span></span>

<span data-ttu-id="45234-147">Weitere Informationen zum Festlegen der Eigenschaften der Protokolldatei finden Sie in der Online Hilfe für die WMI-Steuerungsanwendung.</span><span class="sxs-lookup"><span data-stu-id="45234-147">For more information about setting the log file properties, see the online Help for the WMI Control application.</span></span>

## <a name="logging-activities-for-wmi-provider-components-before-windows-vista"></a><span data-ttu-id="45234-148">Protokollieren von Aktivitäten für WMI-Anbieter Komponenten vor Windows Vista</span><span class="sxs-lookup"><span data-stu-id="45234-148">Logging Activities for WMI Provider Components Before Windows Vista</span></span>

<span data-ttu-id="45234-149">Wenn die Protokollierung für WMI-Kernkomponenten aktiviert ist, wird die Protokollierung auch für jeden Anbieter mit Protokollierungsfunktionen aktiviert.</span><span class="sxs-lookup"><span data-stu-id="45234-149">When logging for WMI core components is enabled, logging is also enabled for any provider with logging capabilities.</span></span>

<span data-ttu-id="45234-150">In der folgenden Liste sind die erforderlichen Werte aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="45234-150">The following list lists the required values.</span></span>

<dl> <dt>

<span data-ttu-id="45234-151"><span id="File"></span><span id="file"></span><span id="FILE"></span>**Datei**</span><span class="sxs-lookup"><span data-stu-id="45234-151"><span id="File"></span><span id="file"></span><span id="FILE"></span>**File**</span></span>
</dt> <dd>

<span data-ttu-id="45234-152">Vollständiger Pfad und Dateiname der Protokolldatei.</span><span class="sxs-lookup"><span data-stu-id="45234-152">Full path and file name of the log file.</span></span> <span data-ttu-id="45234-153">Der Standardwert ist% windir% \\ system32 \\ WBEM \\ Logs.</span><span class="sxs-lookup"><span data-stu-id="45234-153">The default value is %windir%\\system32\\wbem\\logs.</span></span> <span data-ttu-id="45234-154">Der **Typ** mit dem Namen value muss auf = File festgelegt werden, damit dieser benannte Wert verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="45234-154">The **Type** named value must be set to = File for this named value to be used.</span></span>

</dd> <dt>

<span data-ttu-id="45234-155"><span id="Level"></span><span id="level"></span><span id="LEVEL"></span>**Geringen**</span><span class="sxs-lookup"><span data-stu-id="45234-155"><span id="Level"></span><span id="level"></span><span id="LEVEL"></span>**Level**</span></span>
</dt> <dd>

<span data-ttu-id="45234-156">Eine logische 32-Bit-Maske, die den Typ der Debugausgabe definiert, die vom Anbieter generiert wurde.</span><span class="sxs-lookup"><span data-stu-id="45234-156">A 32-bit logical mask that defines the type of debugging output generated by the provider.</span></span> <span data-ttu-id="45234-157">Dieser Wert ist vom Anbieter abhängig.</span><span class="sxs-lookup"><span data-stu-id="45234-157">This value is provider-dependent.</span></span> <span data-ttu-id="45234-158">Der Standardwert ist 0 (null).</span><span class="sxs-lookup"><span data-stu-id="45234-158">The default value is 0 (zero).</span></span>

</dd> <dt>

<span data-ttu-id="45234-159"><span id="MaxFileSize"></span><span id="maxfilesize"></span><span id="MAXFILESIZE"></span>**MaxFileSize**</span><span class="sxs-lookup"><span data-stu-id="45234-159"><span id="MaxFileSize"></span><span id="maxfilesize"></span><span id="MAXFILESIZE"></span>**MaxFileSize**</span></span>
</dt> <dd>

<span data-ttu-id="45234-160">Maximale Dateigröße (in Bytes) der Protokolldatei.</span><span class="sxs-lookup"><span data-stu-id="45234-160">Maximum file size, in bytes, of the log file.</span></span> <span data-ttu-id="45234-161">Dieser ganzzahlige Wert muss zwischen 1024 und 2 ^ 32-1 liegen.</span><span class="sxs-lookup"><span data-stu-id="45234-161">This integer value must be in the range 1024 to 2^32-1.</span></span> <span data-ttu-id="45234-162">Wenn die Dateigröße diesen Wert überschreitet, wird die Datei in **~ filename** umbenannt, und eine neue, leere Protokolldatei wird erstellt.</span><span class="sxs-lookup"><span data-stu-id="45234-162">When the file size exceeds this value, the file is renamed to **~filename** and a new, empty log file is created.</span></span> <span data-ttu-id="45234-163">Der erforderliche Speicherplatz für die Protokolldatei ist zweimal der Wert von **MaxFileSize**.</span><span class="sxs-lookup"><span data-stu-id="45234-163">The disk space required for the log file is twice the value of **MaxFileSize**.</span></span> <span data-ttu-id="45234-164">Der Standardwert ist 65.535.</span><span class="sxs-lookup"><span data-stu-id="45234-164">The default value is 65,535.</span></span>

</dd> <dt>

<span data-ttu-id="45234-165"><span id="Type"></span><span id="type"></span><span id="TYPE"></span>**Sorte**</span><span class="sxs-lookup"><span data-stu-id="45234-165"><span id="Type"></span><span id="type"></span><span id="TYPE"></span>**Type**</span></span>
</dt> <dd>

<span data-ttu-id="45234-166">Kann auf = File oder = Debugger festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="45234-166">Can be set to = File or = Debugger.</span></span> <span data-ttu-id="45234-167">Wenn auf = File festgelegt, werden die Ablauf Verfolgungs Informationen in die Protokolldatei geschrieben, die in der **Datei** mit dem Namen value angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="45234-167">If set to = File, the trace information is written to the log file specified in the **File** named value.</span></span> <span data-ttu-id="45234-168">Der Standardwert ist = File.</span><span class="sxs-lookup"><span data-stu-id="45234-168">The default value is = File.</span></span>

</dd> </dl>

<span data-ttu-id="45234-169">Verwenden Sie z. b. die folgenden Registrierungsschlüssel Werte, um Abfragen zu protokollieren und Instanzaufrufe vom Ansichts Anbieter zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="45234-169">For example, to log query and get instance calls from the View Provider, use the following registry key values.</span></span> <span data-ttu-id="45234-170">Das Protokoll befindet sich im Protokoll Ordner und ist die Standarddatei Größe.</span><span class="sxs-lookup"><span data-stu-id="45234-170">The log will be located in the log folder and will be the default file size.</span></span>

<span data-ttu-id="45234-171">**HKEY \_ Lokale \_ Computer** \\ **Software** \\ **Microsoft** \\ **WBEM**- \\ **Anbieter** \\ **Protokollieren** \\ **viewprovider**- \\ **Datei** = C: \\ Windows \\ system32 \\ WBEM \\ Logs \\ viewprovider. log</span><span class="sxs-lookup"><span data-stu-id="45234-171">**HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**\\**WBEM**\\**PROVIDERS**\\**Logging**\\**ViewProvider**\\**File** = C:\\Windows\\system32\\WBEM\\Logs\\ViewProvider.log</span></span>

<span data-ttu-id="45234-172">**HKEY \_ Lokale \_ Computer** \\ **Software** \\ **Microsoft** \\ **WBEM**- \\ **Anbieter** \\ **Protokollieren** \\ **viewprovider**- \\ **Ebene** = 2</span><span class="sxs-lookup"><span data-stu-id="45234-172">**HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**\\**WBEM**\\**PROVIDERS**\\**Logging**\\**ViewProvider**\\**Level** = 2</span></span>

<span data-ttu-id="45234-173">**HKEY \_ Lokale \_ Computer** \\ **Software** \\ **Microsoft** \\ **WBEM**- \\ **Anbieter** \\ **Protokollieren** \\ **viewprovider** \\ **MaxFileSize** = 65535</span><span class="sxs-lookup"><span data-stu-id="45234-173">**HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**\\**WBEM**\\**PROVIDERS**\\**Logging**\\**ViewProvider**\\**MaxFileSize** = 65535</span></span>

<span data-ttu-id="45234-174">**HKEY \_ Lokale \_ Computer** \\ **Software** \\ **Microsoft** \\ **WBEM**- \\ **Anbieter** \\ **Protokollieren** \\ **viewprovider** \\ **Type** = file</span><span class="sxs-lookup"><span data-stu-id="45234-174">**HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**\\**WBEM**\\**PROVIDERS**\\**Logging**\\**ViewProvider**\\**Type** = File</span></span>

> [!Note]  
> <span data-ttu-id="45234-175">Für Ihre eigenen Anbieter mit Protokollierungsfunktionen müssen Sie die erforderlichen Registrierungsschlüssel und-Werte schreiben, um die Protokollierung zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="45234-175">For your own providers with logging capabilities, you need to write the necessary registry keys and values to enable logging.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="45234-176">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="45234-176">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="45234-177">WMI-Problembehandlung</span><span class="sxs-lookup"><span data-stu-id="45234-177">WMI Troubleshooting</span></span>](wmi-troubleshooting.md)
</dt> <dt>

[<span data-ttu-id="45234-178">WMI-Protokolldateien</span><span class="sxs-lookup"><span data-stu-id="45234-178">WMI Log Files</span></span>](wmi-log-files.md)
</dt> <dt>

[<span data-ttu-id="45234-179">WMI-Fehler Behebungs Klassen</span><span class="sxs-lookup"><span data-stu-id="45234-179">WMI Troubleshooting Classes</span></span>](wmi-troubleshooting-classes.md)
</dt> <dt>

[<span data-ttu-id="45234-180">WMI-Ablauf Verfolgung</span><span class="sxs-lookup"><span data-stu-id="45234-180">Tracing WMI Activity</span></span>](tracing-wmi-activity.md)
</dt> </dl>

 

 
