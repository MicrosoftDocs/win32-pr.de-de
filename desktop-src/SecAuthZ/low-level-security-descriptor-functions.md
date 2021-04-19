---
description: Funktionen zum Festlegen und Abrufen eines Sicherheits Deskriptors für Objekte.
ms.assetid: 22bf0d6b-3ec6-4c28-ace4-49e48714f4bf
title: 'Sicherheitsbeschreibungsfunktionen auf niedriger Eben '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72406dc2481e4671d8d535327f416a2d003c3a89
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106363004"
---
# <a name="low-level-security-descriptor-functions"></a><span data-ttu-id="8f31f-103">Sicherheitsbeschreibungsfunktionen auf niedriger Eben </span><span class="sxs-lookup"><span data-stu-id="8f31f-103">Low-level Security Descriptor Functions</span></span>

<span data-ttu-id="8f31f-104">Es gibt mehrere Paare von Low-Level-Funktionen zum Festlegen und Abrufen der [*Sicherheits Beschreibung*](/windows/desktop/SecGloss/s-gly)eines Objekts.</span><span class="sxs-lookup"><span data-stu-id="8f31f-104">There are several pairs of low-level functions for setting and retrieving an object's [*security descriptor*](/windows/desktop/SecGloss/s-gly).</span></span> <span data-ttu-id="8f31f-105">Jedes dieser Paare funktioniert nur mit einem begrenzten Satz von Windows-Objekten.</span><span class="sxs-lookup"><span data-stu-id="8f31f-105">Each of these pairs works only with a limited set of Windows objects.</span></span> <span data-ttu-id="8f31f-106">Beispielsweise funktioniert ein paar mit Datei Objekten, und ein anderes funktioniert mit Registrierungs Schlüsseln.</span><span class="sxs-lookup"><span data-stu-id="8f31f-106">For example, one pair works with file objects and another works with registry keys.</span></span> <span data-ttu-id="8f31f-107">In der folgenden Tabelle werden die Funktionen auf niedriger Ebene angezeigt, die mit den verschiedenen Typen von Sicherungs fähigen Objekten verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="8f31f-107">The following table shows the low-level functions to use with the different types of securable objects.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="8f31f-108">Objekttyp</span><span class="sxs-lookup"><span data-stu-id="8f31f-108">Object type</span></span></th>
<th><span data-ttu-id="8f31f-109">Low-Level-Funktionen</span><span class="sxs-lookup"><span data-stu-id="8f31f-109">Low-level functions</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="8f31f-110"><a href="/windows/desktop/FileIO/file-security-and-access-rights">Dateien</a></span><span class="sxs-lookup"><span data-stu-id="8f31f-110"><a href="/windows/desktop/FileIO/file-security-and-access-rights">Files</a></span></span></li>
<li><span data-ttu-id="8f31f-111"><a href="/windows/desktop/FileIO/file-security-and-access-rights">Verzeichnisse</a></span><span class="sxs-lookup"><span data-stu-id="8f31f-111"><a href="/windows/desktop/FileIO/file-security-and-access-rights">Directories</a></span></span></li>
<li><span data-ttu-id="8f31f-112">Postslots</span><span class="sxs-lookup"><span data-stu-id="8f31f-112">Mailslots</span></span></li>
<li><span data-ttu-id="8f31f-113"><a href="/windows/desktop/ipc/named-pipe-security-and-access-rights">Named Pipes</a></span><span class="sxs-lookup"><span data-stu-id="8f31f-113"><a href="/windows/desktop/ipc/named-pipe-security-and-access-rights">Named pipes</a></span></span></li>
</ul></td>
<td><span data-ttu-id="8f31f-114">Verwenden Sie die Funktionen <a href="/windows/desktop/api/Winbase/nf-winbase-getfilesecuritya"><strong>getfilesecurity</strong></a> und <a href="/windows/desktop/api/Winbase/nf-winbase-setfilesecuritya"><strong>setfilesecurity</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="8f31f-114">Use the <a href="/windows/desktop/api/Winbase/nf-winbase-getfilesecuritya"><strong>GetFileSecurity</strong></a> and <a href="/windows/desktop/api/Winbase/nf-winbase-setfilesecuritya"><strong>SetFileSecurity</strong></a> functions.</span></span> <span data-ttu-id="8f31f-115">Diese Funktionen verwenden Zeichen folgen, um das Sicherungs fähige Objekt zu identifizieren, anstatt Handles zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="8f31f-115">These functions use character strings to identify the securable object, instead of using handles.</span></span></td>
</tr>
<tr class="even">
<td><ul>
<li><span data-ttu-id="8f31f-116"><a href="/windows/desktop/ProcThread/process-security-and-access-rights">Prozesse</a></span><span class="sxs-lookup"><span data-stu-id="8f31f-116"><a href="/windows/desktop/ProcThread/process-security-and-access-rights">Processes</a></span></span></li>
<li><span data-ttu-id="8f31f-117"><a href="/windows/desktop/ProcThread/thread-security-and-access-rights">Threads</a></span><span class="sxs-lookup"><span data-stu-id="8f31f-117"><a href="/windows/desktop/ProcThread/thread-security-and-access-rights">Threads</a></span></span></li>
<li><span data-ttu-id="8f31f-118"><a href="access-rights-for-access-token-objects.md">Zugriffstoken</a></span><span class="sxs-lookup"><span data-stu-id="8f31f-118"><a href="access-rights-for-access-token-objects.md">Access tokens</a></span></span></li>
<li><span data-ttu-id="8f31f-119"><a href="/windows/desktop/Memory/file-mapping-security-and-access-rights">Datei Zuordnung von Objekten</a></span><span class="sxs-lookup"><span data-stu-id="8f31f-119"><a href="/windows/desktop/Memory/file-mapping-security-and-access-rights">File-mapping objects</a></span></span></li>
<li><span data-ttu-id="8f31f-120"><a href="/windows/desktop/Sync/synchronization-object-security-and-access-rights">Semaphoren</a></span><span class="sxs-lookup"><span data-stu-id="8f31f-120"><a href="/windows/desktop/Sync/synchronization-object-security-and-access-rights">Semaphores</a></span></span></li>
<li><span data-ttu-id="8f31f-121"><a href="/windows/desktop/Sync/synchronization-object-security-and-access-rights">Ereignisse</a></span><span class="sxs-lookup"><span data-stu-id="8f31f-121"><a href="/windows/desktop/Sync/synchronization-object-security-and-access-rights">Events</a></span></span></li>
<li><span data-ttu-id="8f31f-122"><a href="/windows/desktop/Sync/synchronization-object-security-and-access-rights">Mutexe</a></span><span class="sxs-lookup"><span data-stu-id="8f31f-122"><a href="/windows/desktop/Sync/synchronization-object-security-and-access-rights">Mutexes</a></span></span></li>
<li><span data-ttu-id="8f31f-123"><a href="/windows/desktop/Sync/synchronization-object-security-and-access-rights">Wanutzbare Timer</a></span><span class="sxs-lookup"><span data-stu-id="8f31f-123"><a href="/windows/desktop/Sync/synchronization-object-security-and-access-rights">Waitable timers</a></span></span></li>
</ul></td>
<td><span data-ttu-id="8f31f-124">Verwenden Sie die Funktionen <a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getkernelobjectsecurity"><strong>getkernelobjectsecurity</strong></a> und <a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-setkernelobjectsecurity"><strong>setkernelobjectsecurity</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="8f31f-124">Use the <a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getkernelobjectsecurity"><strong>GetKernelObjectSecurity</strong></a> and <a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-setkernelobjectsecurity"><strong>SetKernelObjectSecurity</strong></a> functions.</span></span></td>
</tr>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="8f31f-125"><a href="/windows/desktop/winstation/window-station-security-and-access-rights">Fenster Stationen</a></span><span class="sxs-lookup"><span data-stu-id="8f31f-125"><a href="/windows/desktop/winstation/window-station-security-and-access-rights">Window stations</a></span></span></li>
<li><span data-ttu-id="8f31f-126"><a href="/windows/desktop/winstation/desktop-security-and-access-rights">Desktops</a></span><span class="sxs-lookup"><span data-stu-id="8f31f-126"><a href="/windows/desktop/winstation/desktop-security-and-access-rights">Desktops</a></span></span></li>
</ul></td>
<td><span data-ttu-id="8f31f-127">Verwenden Sie die Funktionen <a href="/windows/desktop/api/Winuser/nf-winuser-getuserobjectsecurity"><strong>getuserobjectsecurity</strong></a> und <a href="/windows/desktop/api/Winuser/nf-winuser-setuserobjectsecurity"><strong>setuserobjectsecurity</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="8f31f-127">Use the <a href="/windows/desktop/api/Winuser/nf-winuser-getuserobjectsecurity"><strong>GetUserObjectSecurity</strong></a> and <a href="/windows/desktop/api/Winuser/nf-winuser-setuserobjectsecurity"><strong>SetUserObjectSecurity</strong></a> functions.</span></span></td>
</tr>
<tr class="even">
<td><ul>
<li><span data-ttu-id="8f31f-128"><a href="/windows/desktop/SysInfo/registry-key-security-and-access-rights">Registrierungsschlüssel</a></span><span class="sxs-lookup"><span data-stu-id="8f31f-128"><a href="/windows/desktop/SysInfo/registry-key-security-and-access-rights">Registry keys</a></span></span></li>
</ul></td>
<td><span data-ttu-id="8f31f-129">Verwenden Sie die Funktionen <a href="/windows/desktop/api/Winreg/nf-winreg-reggetkeysecurity"><strong>reggetkeysecurity</strong></a> und <a href="/windows/desktop/api/Winreg/nf-winreg-regsetkeysecurity"><strong>regsetkeysecurity</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="8f31f-129">Use the <a href="/windows/desktop/api/Winreg/nf-winreg-reggetkeysecurity"><strong>RegGetKeySecurity</strong></a> and <a href="/windows/desktop/api/Winreg/nf-winreg-regsetkeysecurity"><strong>RegSetKeySecurity</strong></a> functions.</span></span></td>
</tr>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="8f31f-130"><a href="/windows/desktop/Services/service-security-and-access-rights">Windows-Dienst Objekte</a></span><span class="sxs-lookup"><span data-stu-id="8f31f-130"><a href="/windows/desktop/Services/service-security-and-access-rights">Windows service objects</a></span></span></li>
</ul></td>
<td><span data-ttu-id="8f31f-131">Verwenden Sie die Funktionen <a href="/windows/desktop/api/Winsvc/nf-winsvc-queryserviceobjectsecurity"><strong>QueryServiceObjectSecurity</strong></a> und <a href="/windows/desktop/api/Winsvc/nf-winsvc-setserviceobjectsecurity"><strong>SetServiceObjectSecurity</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="8f31f-131">Use the <a href="/windows/desktop/api/Winsvc/nf-winsvc-queryserviceobjectsecurity"><strong>QueryServiceObjectSecurity</strong></a> and <a href="/windows/desktop/api/Winsvc/nf-winsvc-setserviceobjectsecurity"><strong>SetServiceObjectSecurity</strong></a> functions.</span></span></td>
</tr>
<tr class="even">
<td><ul>
<li><span data-ttu-id="8f31f-132">Drucker Objekte</span><span class="sxs-lookup"><span data-stu-id="8f31f-132">Printer objects</span></span></li>
</ul></td>
<td><span data-ttu-id="8f31f-133">Verwenden Sie die <a href="/windows/desktop/printdocs/printer-info-2"><strong>PRINTER_INFO_2</strong></a> -Struktur mit den Funktionen " <a href="/windows/desktop/printdocs/getprinter"><strong>GetPrinter</strong></a> " und " <a href="/windows/desktop/printdocs/setprinter"><strong>SetPrinter</strong></a> ".</span><span class="sxs-lookup"><span data-stu-id="8f31f-133">Use the <a href="/windows/desktop/printdocs/printer-info-2"><strong>PRINTER_INFO_2</strong></a> structure with the <a href="/windows/desktop/printdocs/getprinter"><strong>GetPrinter</strong></a> and <a href="/windows/desktop/printdocs/setprinter"><strong>SetPrinter</strong></a> functions.</span></span></td>
</tr>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="8f31f-134"><a href="/windows/desktop/NetMgmt/security-requirements-for-the-network-management-functions">Netzwerkfreigaben</a></span><span class="sxs-lookup"><span data-stu-id="8f31f-134"><a href="/windows/desktop/NetMgmt/security-requirements-for-the-network-management-functions">Network shares</a></span></span></li>
</ul></td>
<td><span data-ttu-id="8f31f-135">Verwenden Sie Level 502 mit den Funktionen <a href="/windows/desktop/api/lmshare/nf-lmshare-netsharegetinfo"><strong>NetShareGetInfo</strong></a> und <a href="/windows/desktop/api/lmshare/nf-lmshare-netsharesetinfo"><strong>NetShareSetInfo</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="8f31f-135">Use level 502 with the <a href="/windows/desktop/api/lmshare/nf-lmshare-netsharegetinfo"><strong>NetShareGetInfo</strong></a> and <a href="/windows/desktop/api/lmshare/nf-lmshare-netsharesetinfo"><strong>NetShareSetInfo</strong></a> functions.</span></span></td>
</tr>
<tr class="even">
<td><ul>
<li><span data-ttu-id="8f31f-136"><a href="acl-based-access-control.md">Private Objekte (Objekte, die für die Erstellungsanwendung privat sind)</a></span><span class="sxs-lookup"><span data-stu-id="8f31f-136"><a href="acl-based-access-control.md">Private objects (objects private to the creating application)</a></span></span></li>
</ul></td>
<td><span data-ttu-id="8f31f-137">Verwenden Sie die Funktionen " <a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-createprivateobjectsecurity"><strong>kreateprivateobjectsecurity</strong></a>", " <a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-destroyprivateobjectsecurity"><strong>DestroyPrivateObjectSecurity</strong></a>", " <a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getprivateobjectsecurity"><strong>GetPrivateObjectSecurity</strong></a> " und " <a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-setprivateobjectsecurity"><strong>setprivateobjectsecurity</strong></a> ".</span><span class="sxs-lookup"><span data-stu-id="8f31f-137">Use the <a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-createprivateobjectsecurity"><strong>CreatePrivateObjectSecurity</strong></a>, <a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-destroyprivateobjectsecurity"><strong>DestroyPrivateObjectSecurity</strong></a>, <a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getprivateobjectsecurity"><strong>GetPrivateObjectSecurity</strong></a> and <a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-setprivateobjectsecurity"><strong>SetPrivateObjectSecurity</strong></a> functions.</span></span></td>
</tr>
</tbody>
</table>



 

 

 
