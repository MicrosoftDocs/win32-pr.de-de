---
title: Sammeln von User-Mode Dumps
description: Ab Windows Server 2008 und Windows Vista mit Service Pack 1 (SP1) können Windows-Fehlerberichterstattung (wer) so konfiguriert werden, dass vollständige benutzermodusdumps gesammelt und lokal gespeichert werden, nachdem eine Anwendung im Benutzermodus abstürzt.
ms.assetid: 8dad892b-04df-4aeb-b6c4-82f7676d382a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b7b1e7850e84d9fa6c8d10953d23640b41b1bc6
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/17/2020
ms.locfileid: "103858163"
---
# <a name="collecting-user-mode-dumps"></a><span data-ttu-id="5755c-103">Sammeln von User-Mode Dumps</span><span class="sxs-lookup"><span data-stu-id="5755c-103">Collecting User-Mode Dumps</span></span>

<span data-ttu-id="5755c-104">Ab Windows Server 2008 und Windows Vista mit Service Pack 1 (SP1) können Windows-Fehlerberichterstattung (wer) so konfiguriert werden, dass vollständige benutzermodusdumps gesammelt und lokal gespeichert werden, nachdem eine Anwendung im Benutzermodus abstürzt.</span><span class="sxs-lookup"><span data-stu-id="5755c-104">Starting with Windows Server 2008 and Windows Vista with Service Pack 1 (SP1), Windows Error Reporting (WER) can be configured so that full user-mode dumps are collected and stored locally after a user-mode application crashes.</span></span> <span data-ttu-id="5755c-105">Anwendungen, die eigene benutzerdefinierte Absturzberichte ausführen, einschließlich .NET-Anwendungen, werden von dieser Funktion nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="5755c-105">Applications that do their own custom crash reporting, including .NET applications, are not supported by this feature.</span></span>

<span data-ttu-id="5755c-106">Diese Funktion ist standardmäßig nicht aktiviert.</span><span class="sxs-lookup"><span data-stu-id="5755c-106">This feature is not enabled by default.</span></span> <span data-ttu-id="5755c-107">Zum Aktivieren des Features sind Administratorrechte erforderlich.</span><span class="sxs-lookup"><span data-stu-id="5755c-107">Enabling the feature requires administrator privileges.</span></span> <span data-ttu-id="5755c-108">Um die Funktion zu aktivieren und zu konfigurieren, verwenden Sie die folgenden Registrierungs Werte unter dem Schlüssel **HKEY \_ local \_ Machine \\ Software \\ Microsoft \\ Windows \\ Windows-Fehlerberichterstattung \\ localdumps** Key.</span><span class="sxs-lookup"><span data-stu-id="5755c-108">To enable and configure the feature, use the following registry values under the **HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Windows\\Windows Error Reporting\\LocalDumps** key.</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="5755c-109">Wert</span><span class="sxs-lookup"><span data-stu-id="5755c-109">Value</span></span></th>
<th><span data-ttu-id="5755c-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5755c-110">Description</span></span></th>
<th><span data-ttu-id="5755c-111">type</span><span class="sxs-lookup"><span data-stu-id="5755c-111">Type</span></span></th>
<th><span data-ttu-id="5755c-112">Standardwert</span><span class="sxs-lookup"><span data-stu-id="5755c-112">Default value</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="5755c-113"><strong>Dumpfolder</strong></span><span class="sxs-lookup"><span data-stu-id="5755c-113"><strong>DumpFolder</strong></span></span></td>
<td><span data-ttu-id="5755c-114">Der Pfad, in dem die Dumpdateien gespeichert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="5755c-114">The path where the dump files are to be stored.</span></span> <span data-ttu-id="5755c-115">Wenn Sie nicht den Standardpfad verwenden, stellen Sie sicher, dass der Ordner ACLs enthält, die es dem Absturz Prozess ermöglichen, Daten in den Ordner zu schreiben.</span><span class="sxs-lookup"><span data-stu-id="5755c-115">If you do not use the default path, then make sure that the folder contains ACLs that allow the crashing process to write data to the folder.</span></span> <span data-ttu-id="5755c-116">Für Dienst Abstürze wird das Dump abhängig vom verwendeten Dienst Konto in Dienst spezifische Profilordner geschrieben.</span><span class="sxs-lookup"><span data-stu-id="5755c-116">For service crashes, the dump is written to service specific profile folders depending on the service account used.</span></span> <span data-ttu-id="5755c-117">Beispielsweise lautet der Profilordner für System Dienste%windir%\system32\config\systemprofile.</span><span class="sxs-lookup"><span data-stu-id="5755c-117">For example, the profile folder for System services is %WINDIR%\System32\Config\SystemProfile.</span></span> <span data-ttu-id="5755c-118">Für Netzwerkdienste und lokale Dienste lautet der Ordner%windir%\serviceprofiles.</span><span class="sxs-lookup"><span data-stu-id="5755c-118">For Network and Local Services, the folder is %WINDIR%\ServiceProfiles.</span></span><br/></td>
<td><span data-ttu-id="5755c-119">REG_EXPAND_SZ</span><span class="sxs-lookup"><span data-stu-id="5755c-119">REG_EXPAND_SZ</span></span></td>
<td><span data-ttu-id="5755c-120">%LocalAppData%\crashdumps</span><span class="sxs-lookup"><span data-stu-id="5755c-120">%LOCALAPPDATA%\CrashDumps</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5755c-121"><strong>Dumpcount</strong></span><span class="sxs-lookup"><span data-stu-id="5755c-121"><strong>DumpCount</strong></span></span></td>
<td><span data-ttu-id="5755c-122">Die maximale Anzahl von Dumpdateien im Ordner.</span><span class="sxs-lookup"><span data-stu-id="5755c-122">The maximum number of dump files in the folder.</span></span> <span data-ttu-id="5755c-123">Wenn der Höchstwert überschritten wird, wird die älteste Dumpdatei im Ordner durch die neue Dumpdatei ersetzt.</span><span class="sxs-lookup"><span data-stu-id="5755c-123">When the maximum value is exceeded, the oldest dump file in the folder will be replaced with the new dump file.</span></span></td>
<td><span data-ttu-id="5755c-124">REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="5755c-124">REG_DWORD</span></span></td>
<td><span data-ttu-id="5755c-125">10</span><span class="sxs-lookup"><span data-stu-id="5755c-125">10</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5755c-126"><strong>Dumptype</strong></span><span class="sxs-lookup"><span data-stu-id="5755c-126"><strong>DumpType</strong></span></span></td>
<td><span data-ttu-id="5755c-127">Geben Sie einen der folgenden dumptypen an:</span><span class="sxs-lookup"><span data-stu-id="5755c-127">Specify one of the following dump types:</span></span>
<ul>
<li><span data-ttu-id="5755c-128">0: benutzerdefiniertes Dump</span><span class="sxs-lookup"><span data-stu-id="5755c-128">0: Custom dump</span></span></li>
<li><span data-ttu-id="5755c-129">1: Mini Abbild</span><span class="sxs-lookup"><span data-stu-id="5755c-129">1: Mini dump</span></span></li>
<li><span data-ttu-id="5755c-130">2: vollständiges Dump</span><span class="sxs-lookup"><span data-stu-id="5755c-130">2: Full dump</span></span></li>
</ul></td>
<td><span data-ttu-id="5755c-131">REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="5755c-131">REG_DWORD</span></span></td>
<td><span data-ttu-id="5755c-132">1</span><span class="sxs-lookup"><span data-stu-id="5755c-132">1</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5755c-133"><strong>Customdumpflags</strong></span><span class="sxs-lookup"><span data-stu-id="5755c-133"><strong>CustomDumpFlags</strong></span></span></td>
<td><span data-ttu-id="5755c-134">Die benutzerdefinierten dumpoptionen, die verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="5755c-134">The custom dump options to be used.</span></span> <span data-ttu-id="5755c-135">Dieser Wert wird nur verwendet, wenn <strong>dumptype</strong> auf 0 festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="5755c-135">This value is used only when <strong>DumpType</strong> is set to 0.</span></span><br/> <span data-ttu-id="5755c-136">Bei den Optionen handelt es sich um eine bitweise Kombination der <a href="/windows/desktop/api/minidumpapiset/ne-minidumpapiset-minidump_type"><strong>MINIDUMP_TYPE</strong></a> Enumerationswerte.</span><span class="sxs-lookup"><span data-stu-id="5755c-136">The options are a bitwise combination of the <a href="/windows/desktop/api/minidumpapiset/ne-minidumpapiset-minidump_type"><strong>MINIDUMP_TYPE</strong></a> enumeration values.</span></span><br/></td>
<td><span data-ttu-id="5755c-137">REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="5755c-137">REG_DWORD</span></span></td>
<td><code>MiniDumpWithDataSegs | MiniDumpWithUnloadedModules | MiniDumpWithProcessThreadData.</code></td>
</tr>
</tbody>
</table>

>[!NOTE]
> <span data-ttu-id="5755c-138">Beim Festlegen [des automatischen Debuggens für **Anwendungs** Abstürze](../debug/configuring-automatic-debugging.md#configuring-automatic-debugging-for-application-crashes)wird kein Absturz Abbild erfasst.</span><span class="sxs-lookup"><span data-stu-id="5755c-138">A crash dump is not collected when you set [automatic debugging for **application** crashes](../debug/configuring-automatic-debugging.md#configuring-automatic-debugging-for-application-crashes).</span></span> 

<span data-ttu-id="5755c-139">Diese Registrierungs Werte stellen die globalen Einstellungen dar.</span><span class="sxs-lookup"><span data-stu-id="5755c-139">These registry values represent the global settings.</span></span> <span data-ttu-id="5755c-140">Sie können auch anwendungsspezifische Einstellungen angeben, die die globalen Einstellungen außer Kraft setzen.</span><span class="sxs-lookup"><span data-stu-id="5755c-140">You can also provide per-application settings that override the global settings.</span></span> <span data-ttu-id="5755c-141">Erstellen Sie einen neuen Schlüssel für Ihre Anwendung unter **HKEY \_ local \_ Machine \\ Software \\ Microsoft \\ Windows \\ Windows-Fehlerberichterstattung \\ localdumps** (z. b. **HKEY \_ local \_ Machine \\ Software \\ Microsoft \\ Windows \\ Windows-Fehlerberichterstattung \\ localdumps \\MyApplication.exe**), um eine Einstellung pro Anwendung zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="5755c-141">To create a per-application setting, create a new key for your application under **HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\Windows\\Windows Error Reporting\\LocalDumps** (for example, **HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\Windows\\Windows Error Reporting\\LocalDumps\\MyApplication.exe**).</span></span> <span data-ttu-id="5755c-142">Fügen Sie die dumpeinstellungen unter dem **MyApplication.exe** -Schlüssel hinzu.</span><span class="sxs-lookup"><span data-stu-id="5755c-142">Add your dump settings under the **MyApplication.exe** key.</span></span> <span data-ttu-id="5755c-143">Wenn die Anwendung abstürzt, liest wer zuerst die globalen Einstellungen und setzt dann alle Einstellungen mit den anwendungsspezifischen Einstellungen außer Kraft.</span><span class="sxs-lookup"><span data-stu-id="5755c-143">If your application crashes, WER will first read the global settings, and then will override any of the settings with your application-specific settings.</span></span>

<span data-ttu-id="5755c-144">Nachdem eine Anwendung abstürzt und vor deren Beendigung, überprüft das System die Registrierungs Einstellungen, um zu bestimmen, ob ein lokales Dump gesammelt werden soll.</span><span class="sxs-lookup"><span data-stu-id="5755c-144">After an application crashes and prior to its termination, the system will check the registry settings to determine whether a local dump is to be collected.</span></span> <span data-ttu-id="5755c-145">Nachdem die dumpsammlung abgeschlossen wurde, kann die Anwendung normal beendet werden.</span><span class="sxs-lookup"><span data-stu-id="5755c-145">After the dump collection has completed, the application will be allowed to terminate normally.</span></span> <span data-ttu-id="5755c-146">Wenn die Anwendung die Wiederherstellung unterstützt, wird das lokale Dump vor dem Aufrufen des Wiederherstellungs Rückrufs gesammelt.</span><span class="sxs-lookup"><span data-stu-id="5755c-146">If the application supports recovery, the local dump is collected before the recovery callback is called.</span></span>

<span data-ttu-id="5755c-147">Diese Abbilder werden unabhängig vom Rest der Wer-Infrastruktur konfiguriert und gesteuert.</span><span class="sxs-lookup"><span data-stu-id="5755c-147">These dumps are configured and controlled independently of the rest of the WER infrastructure.</span></span> <span data-ttu-id="5755c-148">Sie können die lokale dumpsammlung auch dann verwenden, wenn wer deaktiviert ist oder der Benutzer die wer-Berichterstattung abbricht.</span><span class="sxs-lookup"><span data-stu-id="5755c-148">You can make use of the local dump collection even if WER is disabled or if the user cancels WER reporting.</span></span> <span data-ttu-id="5755c-149">Das lokale Abbild kann sich von dem an Microsoft gesendeten Dump unterscheiden.</span><span class="sxs-lookup"><span data-stu-id="5755c-149">The local dump can be different than the dump sent to Microsoft.</span></span>

 

