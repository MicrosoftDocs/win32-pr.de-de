---
description: Mit dem System File Checker-Hilfsprogramm (Sfc.exe) können Administratoren alle geschützten Ressourcen überprüfen, um Ihre Versionen zu überprüfen.
ms.assetid: 72f69ad2-15d9-4191-a8aa-4c23a2392006
title: System File Checker
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da4e0d67f6de6aba62fe262969d7f30db0c45335
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106351120"
---
# <a name="system-file-checker"></a><span data-ttu-id="30913-103">System File Checker</span><span class="sxs-lookup"><span data-stu-id="30913-103">System File Checker</span></span>

<span data-ttu-id="30913-104">Mit dem System File Checker-Hilfsprogramm (Sfc.exe) können Administratoren alle geschützten Ressourcen überprüfen, um Ihre Versionen zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="30913-104">The system file checker utility, Sfc.exe, allows administrators to scan all protected resources to verify their versions.</span></span>

<span data-ttu-id="30913-105">Dateien, die für den Neustart von Fenstern wichtig sind und nicht mit der erwarteten Windows-Version identisch sind, können durch die richtigen Versionen ersetzt werden.</span><span class="sxs-lookup"><span data-stu-id="30913-105">Files critical to restart Windows that do not match the expected Windows version may be replaced with the correct versions.</span></span> <span data-ttu-id="30913-106">Wenn eine Datei repariert wird, werden auch die entsprechenden Registrierungsdaten repariert.</span><span class="sxs-lookup"><span data-stu-id="30913-106">If a file is repaired, the corresponding registry data is also repaired.</span></span> <span data-ttu-id="30913-107">Geschützte Dateien, die für den Neustart von Windows nicht wichtig sind, werden nicht repariert</span><span class="sxs-lookup"><span data-stu-id="30913-107">Protected files not critical to restart Windows are not repaired.</span></span>

## <a name="syntax"></a><span data-ttu-id="30913-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="30913-108">Syntax</span></span>

<span data-ttu-id="30913-109">Im folgenden finden Sie die Befehlszeilen Syntax für SFC.</span><span class="sxs-lookup"><span data-stu-id="30913-109">The following is the command-line syntax for Sfc.</span></span>

<span data-ttu-id="30913-110">**SFC-Optionen \[ = Vollständiger Dateipfad\]**</span><span class="sxs-lookup"><span data-stu-id="30913-110">**SFC options \[=full file path\]**</span></span>

## <a name="options"></a><span data-ttu-id="30913-111">Optionen</span><span class="sxs-lookup"><span data-stu-id="30913-111">Options</span></span>

<dl> <dt>

<span data-ttu-id="30913-112"><span id="_CACHESIZE_x"></span><span id="_cachesize_x"></span><span id="_CACHESIZE_X"></span>/CacheSize =*x*</span><span class="sxs-lookup"><span data-stu-id="30913-112"><span id="_CACHESIZE_x"></span><span id="_cachesize_x"></span><span id="_CACHESIZE_X"></span>/CACHESIZE=*x*</span></span>
</dt> <dd>

<span data-ttu-id="30913-113">Dieser Wert wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="30913-113">This value is not supported.</span></span>

<span data-ttu-id="30913-114">**Windows Server 2003 und Windows XP:** Legt die Dateicache Größe fest.</span><span class="sxs-lookup"><span data-stu-id="30913-114">**Windows Server 2003 and Windows XP:** Sets the file cache size.</span></span> <span data-ttu-id="30913-115">Die Standardgröße des Caches beträgt 0x32 (50 MB).</span><span class="sxs-lookup"><span data-stu-id="30913-115">The default size of the cache is 0x32 (50 MB).</span></span>

</dd> <dt>

<span data-ttu-id="30913-116"><span id="_CANCEL"></span><span id="_cancel"></span>/CANCEL</span><span class="sxs-lookup"><span data-stu-id="30913-116"><span id="_CANCEL"></span><span id="_cancel"></span>/CANCEL</span></span>
</dt> <dd>

<span data-ttu-id="30913-117">Dieser Wert wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="30913-117">This value is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="30913-118"><span id="_ENABLE"></span><span id="_enable"></span>/ENABLE</span><span class="sxs-lookup"><span data-stu-id="30913-118"><span id="_ENABLE"></span><span id="_enable"></span>/ENABLE</span></span>
</dt> <dd>

<span data-ttu-id="30913-119">Dieser Wert wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="30913-119">This value is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="30913-120"><span id="_FILESONLY"></span><span id="_filesonly"></span>/FILESONLY</span><span class="sxs-lookup"><span data-stu-id="30913-120"><span id="_FILESONLY"></span><span id="_filesonly"></span>/FILESONLY</span></span>
</dt> <dd>

<span data-ttu-id="30913-121">Nur Dateien überprüfen oder reparieren.</span><span class="sxs-lookup"><span data-stu-id="30913-121">Verify or repair only files.</span></span> <span data-ttu-id="30913-122">Überprüfen oder reparieren Sie keine Registrierungsschlüssel.</span><span class="sxs-lookup"><span data-stu-id="30913-122">Do not verify or repair registry keys.</span></span>

<span data-ttu-id="30913-123">**Windows XP:** Nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="30913-123">**Windows XP:** Not supported.</span></span>

</dd> <dt>

<span data-ttu-id="30913-124"><span id="_OFFBOOTDIR"></span><span id="_offbootdir"></span>/OFFBOOTDIR</span><span class="sxs-lookup"><span data-stu-id="30913-124"><span id="_OFFBOOTDIR"></span><span id="_offbootdir"></span>/OFFBOOTDIR</span></span>
</dt> <dd>

<span data-ttu-id="30913-125">Verwenden Sie diese Option für Offline Reparaturen.</span><span class="sxs-lookup"><span data-stu-id="30913-125">Use this option for offline repairs.</span></span> <span data-ttu-id="30913-126">Geben Sie den Speicherort des Offline-Start Verzeichnisses an.</span><span class="sxs-lookup"><span data-stu-id="30913-126">Specify the location of the offline boot directory.</span></span>

<span data-ttu-id="30913-127">**Windows XP:** Nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="30913-127">**Windows XP:** Not supported.</span></span>

</dd> <dt>

<span data-ttu-id="30913-128"><span id="_OFFWINDIR"></span><span id="_offwindir"></span>/OFFWINDIR</span><span class="sxs-lookup"><span data-stu-id="30913-128"><span id="_OFFWINDIR"></span><span id="_offwindir"></span>/OFFWINDIR</span></span>
</dt> <dd>

<span data-ttu-id="30913-129">Verwenden Sie diese Option für Offline Reparaturen.</span><span class="sxs-lookup"><span data-stu-id="30913-129">Use this option for offline repairs.</span></span> <span data-ttu-id="30913-130">Geben Sie den Speicherort des Windows-offline Verzeichnisses an.</span><span class="sxs-lookup"><span data-stu-id="30913-130">Specify the location of the offline Windows directory.</span></span>

<span data-ttu-id="30913-131">**Windows XP:** Nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="30913-131">**Windows XP:** Not supported.</span></span>

</dd> <dt>

<span data-ttu-id="30913-132"><span id="_PURGECACHE"></span><span id="_purgecache"></span>/PURGECACHE</span><span class="sxs-lookup"><span data-stu-id="30913-132"><span id="_PURGECACHE"></span><span id="_purgecache"></span>/PURGECACHE</span></span>
</dt> <dd>

<span data-ttu-id="30913-133">Dieser Wert wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="30913-133">This value is not supported.</span></span>

<span data-ttu-id="30913-134">**Windows Server 2003 und Windows XP:** Leert den Dateicache und scannt alle geschützten Systemdateien.</span><span class="sxs-lookup"><span data-stu-id="30913-134">**Windows Server 2003 and Windows XP:** Empties the file cache and scans all protected system files.</span></span>

</dd> <dt>

<span data-ttu-id="30913-135"><span id="_QUIET"></span><span id="_quiet"></span>/Quiet</span><span class="sxs-lookup"><span data-stu-id="30913-135"><span id="_QUIET"></span><span id="_quiet"></span>/QUIET</span></span>
</dt> <dd>

<span data-ttu-id="30913-136">Dieser Wert wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="30913-136">This value is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="30913-137"><span id="_REVERT"></span><span id="_revert"></span>/REVERT</span><span class="sxs-lookup"><span data-stu-id="30913-137"><span id="_REVERT"></span><span id="_revert"></span>/REVERT</span></span>
</dt> <dd>

<span data-ttu-id="30913-138">Kehren Sie zu den Standardeinstellungen zurück.</span><span class="sxs-lookup"><span data-stu-id="30913-138">Return to default settings.</span></span>

<span data-ttu-id="30913-139">**Windows Server 2008 und Windows Vista:** Nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="30913-139">**Windows Server 2008 and Windows Vista:** Not supported.</span></span>

</dd> <dt>

<span data-ttu-id="30913-140"><span id="_SCANBOOT"></span><span id="_scanboot"></span>/SCANBOOT</span><span class="sxs-lookup"><span data-stu-id="30913-140"><span id="_SCANBOOT"></span><span id="_scanboot"></span>/SCANBOOT</span></span>
</dt> <dd>

<span data-ttu-id="30913-141">Dieser Wert wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="30913-141">This value is not supported.</span></span>

<span data-ttu-id="30913-142">**Windows Server 2003 und Windows XP:** Scannt alle geschützten Systemdateien bei jedem Start.</span><span class="sxs-lookup"><span data-stu-id="30913-142">**Windows Server 2003 and Windows XP:** Scans all protected system files at every boot.</span></span>

</dd> <dt>

<span data-ttu-id="30913-143"><span id="_SCANFILE"></span><span id="_scanfile"></span>/SCANFILE</span><span class="sxs-lookup"><span data-stu-id="30913-143"><span id="_SCANFILE"></span><span id="_scanfile"></span>/SCANFILE</span></span>
</dt> <dd>

<span data-ttu-id="30913-144">Scannt und repariert die Datei, die sich unter dem angegebenen vollständigen Pfad befindet.</span><span class="sxs-lookup"><span data-stu-id="30913-144">Scans and repairs the file located at the specified full path.</span></span>

<span data-ttu-id="30913-145">**Windows XP:** Nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="30913-145">**Windows XP:** Not supported.</span></span>

</dd> <dt>

<span data-ttu-id="30913-146"><span id="_SCANNOW"></span><span id="_scannow"></span>/SCANNOW</span><span class="sxs-lookup"><span data-stu-id="30913-146"><span id="_SCANNOW"></span><span id="_scannow"></span>/SCANNOW</span></span>
</dt> <dd>

<span data-ttu-id="30913-147">Scannt alle geschützten Systemdateien sofort.</span><span class="sxs-lookup"><span data-stu-id="30913-147">Scans all protected system files immediately.</span></span>

</dd> <dt>

<span data-ttu-id="30913-148"><span id="_SCANONCE"></span><span id="_scanonce"></span>/SCANONCE</span><span class="sxs-lookup"><span data-stu-id="30913-148"><span id="_SCANONCE"></span><span id="_scanonce"></span>/SCANONCE</span></span>
</dt> <dd>

<span data-ttu-id="30913-149">Dieser Wert wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="30913-149">This value is not supported.</span></span>

<span data-ttu-id="30913-150">**Windows Server 2003 und Windows XP:** Scannt beim nächsten Start alle geschützten Systemdateien.</span><span class="sxs-lookup"><span data-stu-id="30913-150">**Windows Server 2003 and Windows XP:** Scans all protected system files at the next boot.</span></span>

</dd> <dt>

<span data-ttu-id="30913-151"><span id="_VERIFYFILE"></span><span id="_verifyfile"></span>/VERIFYFILE</span><span class="sxs-lookup"><span data-stu-id="30913-151"><span id="_VERIFYFILE"></span><span id="_verifyfile"></span>/VERIFYFILE</span></span>
</dt> <dd>

<span data-ttu-id="30913-152">Überprüft die Datei am angegebenen vollständigen Pfad.</span><span class="sxs-lookup"><span data-stu-id="30913-152">Verifies the file at the specified full path.</span></span> <span data-ttu-id="30913-153">Mit dieser Option wird die Datei nicht repariert.</span><span class="sxs-lookup"><span data-stu-id="30913-153">This option does not repair the file.</span></span>

<span data-ttu-id="30913-154">**Windows XP:** Nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="30913-154">**Windows XP:** Not supported.</span></span>

</dd> <dt>

<span data-ttu-id="30913-155"><span id="_VERIFYONLY"></span><span id="_verifyonly"></span>/VERIFYONLY</span><span class="sxs-lookup"><span data-stu-id="30913-155"><span id="_VERIFYONLY"></span><span id="_verifyonly"></span>/VERIFYONLY</span></span>
</dt> <dd>

<span data-ttu-id="30913-156">Scannt alle geschützten Systemdateien, repariert jedoch keine Dateien.</span><span class="sxs-lookup"><span data-stu-id="30913-156">Scans all protected system files but does not repair files.</span></span>

<span data-ttu-id="30913-157">**Windows XP:** Nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="30913-157">**Windows XP:** Not supported.</span></span>

</dd> </dl>

<span data-ttu-id="30913-158">SFC legt den folgenden Registrierungs Wert fest:</span><span class="sxs-lookup"><span data-stu-id="30913-158">Sfc sets the following registry value:</span></span>

 <span data-ttu-id="30913-159">= HKEY \_ local \_ Machine \\ Software \\ Microsoft \\ Windows NT \\ CurrentVersion \\ Winlogon \\ SfcScan</span><span class="sxs-lookup"><span data-stu-id="30913-159">= HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Windows NT\\CurrentVersion\\Winlogon\\SFCScan</span></span>

<span data-ttu-id="30913-160">Weitere Informationen finden Sie unter [WFP-Registrierungs Werte](wfp-registry-values.md).</span><span class="sxs-lookup"><span data-stu-id="30913-160">For more information, see [WFP Registry Values](wfp-registry-values.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="30913-161">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="30913-161">Remarks</span></span>

<span data-ttu-id="30913-162">Nur unter Windows Vista können Sie die Umgebungsvariable **Windows \_ Tracing \_ logfile** auf den Speicherort eines gültigen Verzeichnisses festlegen, um eine Protokolldatei zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="30913-162">On Windows Vista only, you can set the **WINDOWS\_TRACING\_LOGFILE** environment variable to the location of a valid directory to receive a log file.</span></span>

## <a name="examples"></a><span data-ttu-id="30913-163">Beispiele</span><span class="sxs-lookup"><span data-stu-id="30913-163">Examples</span></span>

<span data-ttu-id="30913-164">Die folgenden Beispiel Befehlszeilen sind Beispiele für sfc.exe-Syntax.</span><span class="sxs-lookup"><span data-stu-id="30913-164">The following sample command lines are examples of sfc.exe syntax.</span></span>

<span data-ttu-id="30913-165">**sfc-/scannow**</span><span class="sxs-lookup"><span data-stu-id="30913-165">**sfc /SCANNOW**</span></span>

<span data-ttu-id="30913-166">**SFC/VERIFYFILE = c: \\ Windows \\ system32 \\kernel32.dll**</span><span class="sxs-lookup"><span data-stu-id="30913-166">**sfc /VERIFYFILE=c:\\windows\\system32\\kernel32.dll**</span></span>

<span data-ttu-id="30913-167">**SFC/SCANFILE = d: \\ Windows \\ system32 \\kernel32.dll/OFFBOOTDIR = d: \\ /OFFWINDIR = d: \\ Windows**</span><span class="sxs-lookup"><span data-stu-id="30913-167">**sfc /SCANFILE=d:\\windows\\system32\\kernel32.dll /OFFBOOTDIR=d:\\ /OFFWINDIR=d:\\windows**</span></span>

<span data-ttu-id="30913-168">**SFC/VERIFYONLY/FILESONLY**</span><span class="sxs-lookup"><span data-stu-id="30913-168">**sfc /VERIFYONLY /FILESONLY**</span></span>

 

 



