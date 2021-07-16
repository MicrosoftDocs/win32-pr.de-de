---
title: Sammeln von User-Mode Dumps
description: Ab Windows Server 2008 und Windows Vista mit Service Pack 1 (SP1) können Windows-Fehlerberichterstattung (WER) so konfiguriert werden, dass vollständige Speicherabbilder im Benutzermodus erfasst und lokal gespeichert werden, nachdem eine Anwendung im Benutzermodus abstürzt.
ms.assetid: 8dad892b-04df-4aeb-b6c4-82f7676d382a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e6291d3ad8dfeb641582a93f6789ca7844594ad
ms.sourcegitcommit: 892997f4126d44df413286074e08a9c6065313ec
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/16/2021
ms.locfileid: "114300185"
---
# <a name="collecting-user-mode-dumps"></a><span data-ttu-id="2a403-103">Sammeln von User-Mode Dumps</span><span class="sxs-lookup"><span data-stu-id="2a403-103">Collecting User-Mode Dumps</span></span>

<span data-ttu-id="2a403-104">Ab Windows Server 2008 und Windows Vista mit Service Pack 1 (SP1) können Windows-Fehlerberichterstattung (WER) so konfiguriert werden, dass vollständige Speicherabbilder im Benutzermodus erfasst und lokal gespeichert werden, nachdem eine Anwendung im Benutzermodus abstürzt.</span><span class="sxs-lookup"><span data-stu-id="2a403-104">Starting with Windows Server 2008 and Windows Vista with Service Pack 1 (SP1), Windows Error Reporting (WER) can be configured so that full user-mode dumps are collected and stored locally after a user-mode application crashes.</span></span> <span data-ttu-id="2a403-105">Anwendungen, die ihre eigene benutzerdefinierte Absturzberichterstellung durchführen, einschließlich .NET-Anwendungen, werden von diesem Feature nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="2a403-105">Applications that do their own custom crash reporting, including .NET applications, are not supported by this feature.</span></span>

<span data-ttu-id="2a403-106">Diese Funktion ist standardmäßig nicht aktiviert.</span><span class="sxs-lookup"><span data-stu-id="2a403-106">This feature is not enabled by default.</span></span> <span data-ttu-id="2a403-107">Zum Aktivieren des Features sind Administratorrechte erforderlich.</span><span class="sxs-lookup"><span data-stu-id="2a403-107">Enabling the feature requires administrator privileges.</span></span> <span data-ttu-id="2a403-108">Verwenden Sie zum Aktivieren und Konfigurieren des Features die folgenden Registrierungswerte unter **HKEY \_ LOCAL MACHINE SOFTWARE Microsoft Windows Windows-Fehlerberichterstattung \_ \\ \\ \\ \\ \\ LocalDumps-Schlüssel.**</span><span class="sxs-lookup"><span data-stu-id="2a403-108">To enable and configure the feature, use the following registry values under the **HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Windows\\Windows Error Reporting\\LocalDumps** key.</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="2a403-109">Wert</span><span class="sxs-lookup"><span data-stu-id="2a403-109">Value</span></span></th>
<th><span data-ttu-id="2a403-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2a403-110">Description</span></span></th>
<th><span data-ttu-id="2a403-111">Typ</span><span class="sxs-lookup"><span data-stu-id="2a403-111">Type</span></span></th>
<th><span data-ttu-id="2a403-112">Standardwert</span><span class="sxs-lookup"><span data-stu-id="2a403-112">Default value</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="2a403-113"><strong>DumpFolder</strong></span><span class="sxs-lookup"><span data-stu-id="2a403-113"><strong>DumpFolder</strong></span></span></td>
<td><span data-ttu-id="2a403-114">Der Pfad, in dem die Dumpdateien gespeichert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="2a403-114">The path where the dump files are to be stored.</span></span> <span data-ttu-id="2a403-115">Wenn Sie den Standardpfad nicht verwenden, stellen Sie sicher, dass der Ordner ACLs enthält, die es dem abstürzenden Prozess ermöglichen, Daten in den Ordner zu schreiben.</span><span class="sxs-lookup"><span data-stu-id="2a403-115">If you do not use the default path, then make sure that the folder contains ACLs that allow the crashing process to write data to the folder.</span></span> <span data-ttu-id="2a403-116">Bei Dienstabstürzen wird das Speicherabbild abhängig vom verwendeten Dienstkonto in dienstspezifische Profilordner geschrieben.</span><span class="sxs-lookup"><span data-stu-id="2a403-116">For service crashes, the dump is written to service specific profile folders depending on the service account used.</span></span> <span data-ttu-id="2a403-117">Der Profilordner für Systemdienste lautet beispielsweise %WINDIR%\System32\Config\SystemProfile.</span><span class="sxs-lookup"><span data-stu-id="2a403-117">For example, the profile folder for System services is %WINDIR%\System32\Config\SystemProfile.</span></span> <span data-ttu-id="2a403-118">Für Netzwerk- und lokale Dienste lautet der Ordner %WINDIR%\ServiceProfiles.</span><span class="sxs-lookup"><span data-stu-id="2a403-118">For Network and Local Services, the folder is %WINDIR%\ServiceProfiles.</span></span><br/></td>
<td><span data-ttu-id="2a403-119">Reg_expand_sz</span><span class="sxs-lookup"><span data-stu-id="2a403-119">REG_EXPAND_SZ</span></span></td>
<td><span data-ttu-id="2a403-120">%LOCALAPPDATA%\CrashDumps</span><span class="sxs-lookup"><span data-stu-id="2a403-120">%LOCALAPPDATA%\CrashDumps</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2a403-121"><strong>DumpCount</strong></span><span class="sxs-lookup"><span data-stu-id="2a403-121"><strong>DumpCount</strong></span></span></td>
<td><span data-ttu-id="2a403-122">Die maximale Anzahl von Sicherungsdateien im Ordner.</span><span class="sxs-lookup"><span data-stu-id="2a403-122">The maximum number of dump files in the folder.</span></span> <span data-ttu-id="2a403-123">Wenn der maximale Wert überschritten wird, wird die älteste Speicherabbilddatei im Ordner durch die neue Dumpdatei ersetzt.</span><span class="sxs-lookup"><span data-stu-id="2a403-123">When the maximum value is exceeded, the oldest dump file in the folder will be replaced with the new dump file.</span></span></td>
<td><span data-ttu-id="2a403-124">REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="2a403-124">REG_DWORD</span></span></td>
<td><span data-ttu-id="2a403-125">10</span><span class="sxs-lookup"><span data-stu-id="2a403-125">10</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2a403-126"><strong>DumpType</strong></span><span class="sxs-lookup"><span data-stu-id="2a403-126"><strong>DumpType</strong></span></span></td>
<td><span data-ttu-id="2a403-127">Geben Sie einen der folgenden Speicherabbildtypen an:</span><span class="sxs-lookup"><span data-stu-id="2a403-127">Specify one of the following dump types:</span></span>
<ul>
<li><span data-ttu-id="2a403-128">0: Benutzerdefiniertes Speicherabbild</span><span class="sxs-lookup"><span data-stu-id="2a403-128">0: Custom dump</span></span></li>
<li><span data-ttu-id="2a403-129">1: Miniabbild</span><span class="sxs-lookup"><span data-stu-id="2a403-129">1: Mini dump</span></span></li>
<li><span data-ttu-id="2a403-130">2: Vollständiges Speicherabbild</span><span class="sxs-lookup"><span data-stu-id="2a403-130">2: Full dump</span></span></li>
</ul></td>
<td><span data-ttu-id="2a403-131">REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="2a403-131">REG_DWORD</span></span></td>
<td><span data-ttu-id="2a403-132">1</span><span class="sxs-lookup"><span data-stu-id="2a403-132">1</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2a403-133"><strong>CustomDumpFlags</strong></span><span class="sxs-lookup"><span data-stu-id="2a403-133"><strong>CustomDumpFlags</strong></span></span></td>
<td><span data-ttu-id="2a403-134">Die zu verwendenden benutzerdefinierten Speicherabbildoptionen.</span><span class="sxs-lookup"><span data-stu-id="2a403-134">The custom dump options to be used.</span></span> <span data-ttu-id="2a403-135">Dieser Wert wird nur verwendet, wenn <strong>DumpType</strong> auf 0 festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="2a403-135">This value is used only when <strong>DumpType</strong> is set to 0.</span></span><br/> <span data-ttu-id="2a403-136">Die Optionen sind eine bitweise Kombination der <a href="/windows/desktop/api/minidumpapiset/ne-minidumpapiset-minidump_type"><strong>MINIDUMP_TYPE</strong></a> Enumerationswerte.</span><span class="sxs-lookup"><span data-stu-id="2a403-136">The options are a bitwise combination of the <a href="/windows/desktop/api/minidumpapiset/ne-minidumpapiset-minidump_type"><strong>MINIDUMP_TYPE</strong></a> enumeration values.</span></span><br/></td>
<td><span data-ttu-id="2a403-137">REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="2a403-137">REG_DWORD</span></span></td>
 <td><span data-ttu-id="2a403-138"><code>0x00000121</code> (<code>MiniDumpWithDataSegs | MiniDumpWithUnloadedModules | MiniDumpWithProcessThreadData == 0x00000001 | 0x00000020 | 0x00000100)</code></span><span class="sxs-lookup"><span data-stu-id="2a403-138"><code>0x00000121</code> (<code>MiniDumpWithDataSegs | MiniDumpWithUnloadedModules | MiniDumpWithProcessThreadData == 0x00000001 | 0x00000020 | 0x00000100)</code></span></span></td>
</tr>
</tbody>
</table>

>[!NOTE]
> <span data-ttu-id="2a403-139">Ein Absturzabbild wird nicht erfasst, wenn Sie [das automatische Debuggen für **Anwendungsabstürze**](../debug/configuring-automatic-debugging.md#configuring-automatic-debugging-for-application-crashes)festlegen.</span><span class="sxs-lookup"><span data-stu-id="2a403-139">A crash dump is not collected when you set [automatic debugging for **application** crashes](../debug/configuring-automatic-debugging.md#configuring-automatic-debugging-for-application-crashes).</span></span> 

<span data-ttu-id="2a403-140">Diese Registrierungswerte stellen die globalen Einstellungen dar.</span><span class="sxs-lookup"><span data-stu-id="2a403-140">These registry values represent the global settings.</span></span> <span data-ttu-id="2a403-141">Sie können auch Anwendungsspezifische Einstellungen angeben, die die globalen Einstellungen außer Kraft setzen.</span><span class="sxs-lookup"><span data-stu-id="2a403-141">You can also provide per-application settings that override the global settings.</span></span> <span data-ttu-id="2a403-142">Um eine Anwendungseinstellung zu erstellen, erstellen Sie einen neuen Schlüssel für Ihre Anwendung unter **HKEY \_ LOCAL MACHINE Software Microsoft Windows Windows-Fehlerberichterstattung \_ \\ \\ \\ \\ \\ LocalDumps** (z.B. **HKEY LOCAL MACHINE Software \_ Microsoft Windows Windows-Fehlerberichterstattung \_ \\ \\ \\ \\ \\ LocalDumps \\MyApplication.exe**).</span><span class="sxs-lookup"><span data-stu-id="2a403-142">To create a per-application setting, create a new key for your application under **HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\Windows\\Windows Error Reporting\\LocalDumps** (for example, **HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\Windows\\Windows Error Reporting\\LocalDumps\\MyApplication.exe**).</span></span> <span data-ttu-id="2a403-143">Fügen Sie Ihre Speicherabbildeinstellungen unter dem **MyApplication.exe** Schlüssel hinzu.</span><span class="sxs-lookup"><span data-stu-id="2a403-143">Add your dump settings under the **MyApplication.exe** key.</span></span> <span data-ttu-id="2a403-144">Wenn Ihre Anwendung abstürzt, liest WER zuerst die globalen Einstellungen und überschreibt dann alle Einstellungen mit Ihren anwendungsspezifischen Einstellungen.</span><span class="sxs-lookup"><span data-stu-id="2a403-144">If your application crashes, WER will first read the global settings, and then will override any of the settings with your application-specific settings.</span></span>

<span data-ttu-id="2a403-145">Nach dem Absturz einer Anwendung und vor dem Beenden überprüft das System die Registrierungseinstellungen, um zu ermitteln, ob ein lokales Speicherabbild erfasst werden soll.</span><span class="sxs-lookup"><span data-stu-id="2a403-145">After an application crashes and prior to its termination, the system will check the registry settings to determine whether a local dump is to be collected.</span></span> <span data-ttu-id="2a403-146">Nach Abschluss der Speicherabbildsammlung kann die Anwendung normal beendet werden.</span><span class="sxs-lookup"><span data-stu-id="2a403-146">After the dump collection has completed, the application will be allowed to terminate normally.</span></span> <span data-ttu-id="2a403-147">Wenn die Anwendung die Wiederherstellung unterstützt, wird das lokale Speicherabbild erfasst, bevor der Wiederherstellungsrückruf aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="2a403-147">If the application supports recovery, the local dump is collected before the recovery callback is called.</span></span>

<span data-ttu-id="2a403-148">Diese Dumps werden unabhängig von der restlichen WER-Infrastruktur konfiguriert und gesteuert.</span><span class="sxs-lookup"><span data-stu-id="2a403-148">These dumps are configured and controlled independently of the rest of the WER infrastructure.</span></span> <span data-ttu-id="2a403-149">Sie können die lokale Speicherabbildsammlung auch dann verwenden, wenn WER deaktiviert ist oder der Benutzer die WER-Berichterstellung abbricht.</span><span class="sxs-lookup"><span data-stu-id="2a403-149">You can make use of the local dump collection even if WER is disabled or if the user cancels WER reporting.</span></span> <span data-ttu-id="2a403-150">Das lokale Speicherabbild kann sich von dem an Microsoft gesendeten Dump unterscheiden.</span><span class="sxs-lookup"><span data-stu-id="2a403-150">The local dump can be different than the dump sent to Microsoft.</span></span>

 

