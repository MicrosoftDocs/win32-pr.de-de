---
description: Die uikreatepatchpackageex-Funktion nimmt eine Paket Erstellungs Datei (PCP-Datei) und generiert ein Windows Installer Patchpaket (MSP-Paket). Das Aufrufen von Msimsp.exe ist die empfohlene Methode für die Verwendung von Patchwiz.dll.
ms.assetid: 76d9a21d-73bc-41fc-8ed0-7d7d7deff815
title: Uikreatepatchpackageex (Patchwiz.dll)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac61371d1e7bf1809880c8f10a403d1730adc8e1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106341168"
---
# <a name="uicreatepatchpackageex-patchwizdll"></a><span data-ttu-id="40d40-104">Uikreatepatchpackageex (Patchwiz.dll)</span><span class="sxs-lookup"><span data-stu-id="40d40-104">UiCreatePatchPackageEx (Patchwiz.dll)</span></span>

<span data-ttu-id="40d40-105">Die uikreatepatchpackageex-Funktion nimmt eine Paket Erstellungs Datei (PCP-Datei) und generiert ein Windows Installer Patchpaket (MSP-Paket).</span><span class="sxs-lookup"><span data-stu-id="40d40-105">The UiCreatePatchPackageEx function takes a package creation file (.pcp file) and generates a Windows Installer patch package (.msp package).</span></span> <span data-ttu-id="40d40-106">Das Aufrufen von [Msimsp.exe](msimsp-exe.md) ist die empfohlene Methode für die Verwendung von [Patchwiz.dll](patchwiz-dll.md).</span><span class="sxs-lookup"><span data-stu-id="40d40-106">Calling [Msimsp.exe](msimsp-exe.md) is the recommended method for using [Patchwiz.dll](patchwiz-dll.md).</span></span>

<span data-ttu-id="40d40-107">Die uikreatepatchpackageex-Funktion ist ab Patchwiz.dll Version 4,0 verfügbar und erweitert die Funktionalität der [uikreatepatchpackage](uicreatepatchpackage-patchwiz-dll-.md) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="40d40-107">The UiCreatePatchPackageEx function is available beginning with Patchwiz.dll version 4.0 and extends the functionality of the [UiCreatePatchPackage](uicreatepatchpackage-patchwiz-dll-.md) function.</span></span>

``` syntax
UINT UiCreatePatchPackageEx(
  LPCTSTR szPcpPath,              
  LPCTSTR szPatchPath,            
  LPCTSTR szLogPath,             
  HWND hwndStatus,                
  LPCTSTR szTempFolder,           
  BOOL fRemoveTempFolderContents,
  DWORD dwFlags,
  DWORD dwReserved    
);
```

## <a name="parameters"></a><span data-ttu-id="40d40-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="40d40-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="40d40-109"><span id="szPcpPath"></span><span id="szpcppath"></span><span id="SZPCPPATH"></span>*szpcppath*</span><span class="sxs-lookup"><span data-stu-id="40d40-109"><span id="szPcpPath"></span><span id="szpcppath"></span><span id="SZPCPPATH"></span>*szPcpPath*</span></span>
</dt> <dd>

<span data-ttu-id="40d40-110">Vollständiger Pfad zur Eigenschaften Datei für die Patcherstellung (PCP-Datei) für diesen Patch.</span><span class="sxs-lookup"><span data-stu-id="40d40-110">Full path to the patch creation properties file (.pcp file) for this patch.</span></span>

</dd> <dt>

<span data-ttu-id="40d40-111"><span id="szPatchPath"></span><span id="szpatchpath"></span><span id="SZPATCHPATH"></span>*szpatchpfad*</span><span class="sxs-lookup"><span data-stu-id="40d40-111"><span id="szPatchPath"></span><span id="szpatchpath"></span><span id="SZPATCHPATH"></span>*szPatchPath*</span></span>
</dt> <dd>

<span data-ttu-id="40d40-112">Vollständiger Pfad zum Windows Installer Patchpaket (MSP-Datei), das erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="40d40-112">Full path to the Windows Installer patch package (.msp file) that is to be created.</span></span> <span data-ttu-id="40d40-113">Dieser Parameter kann **null** oder eine leere Zeichenfolge sein, wird jedoch möglicherweise nicht ausgelassen.</span><span class="sxs-lookup"><span data-stu-id="40d40-113">This parameter may be **NULL** or an empty string but may not be omitted.</span></span> <span data-ttu-id="40d40-114">Wenn Sie **null** oder eine leere Zeichenfolge ist, verwendet die Funktion den Wert von "patchoutputpath" in der [Properties-Tabelle (Patchwiz.dll)](properties-table-patchwiz-dll-.md).</span><span class="sxs-lookup"><span data-stu-id="40d40-114">If it is **NULL** or an empty string, the function uses the value of PatchOutputPath in the [Properties Table (Patchwiz.dll)](properties-table-patchwiz-dll-.md).</span></span>

</dd> <dt>

<span data-ttu-id="40d40-115"><span id="szLogPath"></span><span id="szlogpath"></span><span id="SZLOGPATH"></span>*szlogpath*</span><span class="sxs-lookup"><span data-stu-id="40d40-115"><span id="szLogPath"></span><span id="szlogpath"></span><span id="SZLOGPATH"></span>*szLogPath*</span></span>
</dt> <dd>

<span data-ttu-id="40d40-116">Vollständiger Pfad zu einer Text Protokolldatei, die angefügt wird.</span><span class="sxs-lookup"><span data-stu-id="40d40-116">Full path to a text log file that will be appended.</span></span> <span data-ttu-id="40d40-117">Dieser Parameter kann **null** oder eine leere Zeichenfolge sein, wird jedoch möglicherweise nicht ausgelassen.</span><span class="sxs-lookup"><span data-stu-id="40d40-117">This parameter may be **NULL** or an empty string but may not be omitted.</span></span>

</dd> <dt>

<span data-ttu-id="40d40-118"><span id="hwndStatus"></span><span id="hwndstatus"></span><span id="HWNDSTATUS"></span>*hwndstatus*</span><span class="sxs-lookup"><span data-stu-id="40d40-118"><span id="hwndStatus"></span><span id="hwndstatus"></span><span id="HWNDSTATUS"></span>*hwndStatus*</span></span>
</dt> <dd>

<span data-ttu-id="40d40-119">Handle für ein Fenster, in dem der Status Text angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="40d40-119">Handle to a window that displays the status text.</span></span> <span data-ttu-id="40d40-120">Dieser Parameter kann **null** oder eine leere Zeichenfolge sein, wird jedoch möglicherweise nicht ausgelassen.</span><span class="sxs-lookup"><span data-stu-id="40d40-120">This parameter may be **NULL** or an empty string but may not be omitted.</span></span>

</dd> <dt>

<span data-ttu-id="40d40-121"><span id="szTempFolder"></span><span id="sztempfolder"></span><span id="SZTEMPFOLDER"></span>*sztempfolder*</span><span class="sxs-lookup"><span data-stu-id="40d40-121"><span id="szTempFolder"></span><span id="sztempfolder"></span><span id="SZTEMPFOLDER"></span>*szTempFolder*</span></span>
</dt> <dd>

<span data-ttu-id="40d40-122">Speicherort für temporäre Dateien.</span><span class="sxs-lookup"><span data-stu-id="40d40-122">Location for temporary files.</span></span> <span data-ttu-id="40d40-123">Dieser Parameter kann **null** oder eine leere Zeichenfolge sein, wird jedoch möglicherweise nicht ausgelassen.</span><span class="sxs-lookup"><span data-stu-id="40d40-123">This parameter may be **NULL** or an empty string but may not be omitted.</span></span> <span data-ttu-id="40d40-124">Der Benutzer muss über ausreichende Berechtigungen zum Lesen und Schreiben in diesen Ordner verfügen.</span><span class="sxs-lookup"><span data-stu-id="40d40-124">The user must have sufficient privileges to read and write to this folder.</span></span> <span data-ttu-id="40d40-125">Der Standard Speicherort ist% tmp% \\ ~ PCW \_ tmp. tmp \\ .</span><span class="sxs-lookup"><span data-stu-id="40d40-125">The default location is %TMP%\\~pcw\_tmp.tmp\\.</span></span>

</dd> <dt>

<span data-ttu-id="40d40-126"><span id="fRemoveTempFolderContents"></span><span id="fremovetempfoldercontents"></span><span id="FREMOVETEMPFOLDERCONTENTS"></span>*fremuvetempfoldercontents*</span><span class="sxs-lookup"><span data-stu-id="40d40-126"><span id="fRemoveTempFolderContents"></span><span id="fremovetempfoldercontents"></span><span id="FREMOVETEMPFOLDERCONTENTS"></span>*fRemoveTempFolderContents*</span></span>
</dt> <dd>

<span data-ttu-id="40d40-127">Wenn **true**, entfernen Sie den temporären Ordner und seinen gesamten Inhalt, falls vorhanden.</span><span class="sxs-lookup"><span data-stu-id="40d40-127">If **TRUE**, remove the temporary folder and all of its contents if present.</span></span> <span data-ttu-id="40d40-128">Wenn **false** und der Ordner vorhanden ist, schlägt die Funktion fehl.</span><span class="sxs-lookup"><span data-stu-id="40d40-128">If **FALSE**, and folder is present, the function fails.</span></span>

</dd> <dt>

<span data-ttu-id="40d40-129"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="40d40-129"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="40d40-130">Dieser Parameter kann auf eine oder eine Kombination der folgenden Werte festgelegt werden, um Protokollierungs-oder Benutzeroberflächen Optionen anzugeben.</span><span class="sxs-lookup"><span data-stu-id="40d40-130">This parameter can be set to one or a combination of the following values to specify logging or user interface options.</span></span>



| <span data-ttu-id="40d40-131">Flag</span><span class="sxs-lookup"><span data-stu-id="40d40-131">Flag</span></span>            | <span data-ttu-id="40d40-132">Wert</span><span class="sxs-lookup"><span data-stu-id="40d40-132">Value</span></span>       | <span data-ttu-id="40d40-133">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="40d40-133">Meaning</span></span>                                  |
|-----------------|-------------|------------------------------------------|
| <span data-ttu-id="40d40-134">Lognone</span><span class="sxs-lookup"><span data-stu-id="40d40-134">LOGNONE</span></span>         | <span data-ttu-id="40d40-135">0x00000000</span><span class="sxs-lookup"><span data-stu-id="40d40-135">0x00000000</span></span>  | <span data-ttu-id="40d40-136">Schreiben Sie keine Nachrichten in das Protokoll.</span><span class="sxs-lookup"><span data-stu-id="40d40-136">Write no messages to the log.</span></span>            |
| <span data-ttu-id="40d40-137">LOGINFO</span><span class="sxs-lookup"><span data-stu-id="40d40-137">LOGINFO</span></span>         | <span data-ttu-id="40d40-138">0x00000001</span><span class="sxs-lookup"><span data-stu-id="40d40-138">0x00000001</span></span>  | <span data-ttu-id="40d40-139">Schreiben Sie Informationsmeldungen in das Protokoll.</span><span class="sxs-lookup"><span data-stu-id="40d40-139">Write informational messages to the log.</span></span> |
| <span data-ttu-id="40d40-140">Logwarn</span><span class="sxs-lookup"><span data-stu-id="40d40-140">LOGWARN</span></span>         | <span data-ttu-id="40d40-141">0x00000002</span><span class="sxs-lookup"><span data-stu-id="40d40-141">0x00000002</span></span>  | <span data-ttu-id="40d40-142">Schreiben Sie Warnungen in das Protokoll.</span><span class="sxs-lookup"><span data-stu-id="40d40-142">Write warnings to the log.</span></span>               |
| <span data-ttu-id="40d40-143">Logerr</span><span class="sxs-lookup"><span data-stu-id="40d40-143">LOGERR</span></span>          | <span data-ttu-id="40d40-144">0x00000004</span><span class="sxs-lookup"><span data-stu-id="40d40-144">0x00000004</span></span>  | <span data-ttu-id="40d40-145">Schreiben Sie Fehlermeldungen in das Protokoll.</span><span class="sxs-lookup"><span data-stu-id="40d40-145">Write error messages to the log.</span></span>         |
| <span data-ttu-id="40d40-146">Logperfmessages</span><span class="sxs-lookup"><span data-stu-id="40d40-146">LOGPERFMESSAGES</span></span> | <span data-ttu-id="40d40-147">0x00000008</span><span class="sxs-lookup"><span data-stu-id="40d40-147">0x00000008</span></span>  | <span data-ttu-id="40d40-148">Schreiben Sie Leistungs Meldungen in das Protokoll.</span><span class="sxs-lookup"><span data-stu-id="40d40-148">Write performance messages to the log.</span></span>   |
| <span data-ttu-id="40d40-149">Uinone</span><span class="sxs-lookup"><span data-stu-id="40d40-149">UINONE</span></span>          | <span data-ttu-id="40d40-150">0x00000000f</span><span class="sxs-lookup"><span data-stu-id="40d40-150">0x00000000f</span></span> | <span data-ttu-id="40d40-151">Die Benutzeroberfläche wird nicht angezeigt.</span><span class="sxs-lookup"><span data-stu-id="40d40-151">Do not display the user interface.</span></span>       |
| <span data-ttu-id="40d40-152">Uiall</span><span class="sxs-lookup"><span data-stu-id="40d40-152">UIALL</span></span>           | <span data-ttu-id="40d40-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="40d40-153">0x00000010</span></span>  | <span data-ttu-id="40d40-154">Zeigen Sie die Benutzeroberfläche an.</span><span class="sxs-lookup"><span data-stu-id="40d40-154">Display the user interface.</span></span>              |



 

</dd> <dt>

<span data-ttu-id="40d40-155"><span id="dwReserved"></span><span id="dwreserved"></span><span id="DWRESERVED"></span>*dwReserved*</span><span class="sxs-lookup"><span data-stu-id="40d40-155"><span id="dwReserved"></span><span id="dwreserved"></span><span id="DWRESERVED"></span>*dwReserved*</span></span>
</dt> <dd>

<span data-ttu-id="40d40-156">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="40d40-156">Reserved.</span></span> <span data-ttu-id="40d40-157">Dieser Parameter muss auf 0 (null) festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="40d40-157">This parameter must be set to zero.</span></span>

</dd> </dl>

## <a name="return-values"></a><span data-ttu-id="40d40-158">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="40d40-158">Return Values</span></span>

<span data-ttu-id="40d40-159">Weitere Informationen finden Sie in der Tabelle unter [Rückgabewerte für uikreatepatchpackage](return-values-for-uicreatepatchpackage.md).</span><span class="sxs-lookup"><span data-stu-id="40d40-159">See the table in [Return Values for UiCreatePatchPackage](return-values-for-uicreatepatchpackage.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="40d40-160">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="40d40-160">Remarks</span></span>

<span data-ttu-id="40d40-161">Ein Beispiel für das Erstellen einer PCP-Datei und die Verwendung von [uikreatepatchpackage](uicreatepatchpackage-patchwiz-dll-.md) zum Generieren eines Windows Installer Patchpakets finden Sie im Abschnitt [ein Beispiel für ein kleines Update Patching](a-small-update-patching-example.md).</span><span class="sxs-lookup"><span data-stu-id="40d40-161">For an example of authoring a .pcp file and using [UiCreatePatchPackage](uicreatepatchpackage-patchwiz-dll-.md) to generate a Windows Installer patch package, see the section [A Small Update Patching Example](a-small-update-patching-example.md).</span></span>

<span data-ttu-id="40d40-162">Zum Erstellen eines Patches ist ein nicht komprimiertes Setup Image erforderlich, z. b. ein administratives Image oder ein nicht komprimiertes Setup-Image von einer CD-ROM.</span><span class="sxs-lookup"><span data-stu-id="40d40-162">Creating a patch requires an uncompressed setup image, such as an administrative image or an uncompressed setup image from a CD-ROM.</span></span> <span data-ttu-id="40d40-163">[Uikreatepatchpackage](uicreatepatchpackage-patchwiz-dll-.md) generiert keine binären Patches für Dateien in den CAB-Dateien.</span><span class="sxs-lookup"><span data-stu-id="40d40-163">[UiCreatePatchPackage](uicreatepatchpackage-patchwiz-dll-.md) does not generate binary patches for files in cabinets.</span></span>

 

 



