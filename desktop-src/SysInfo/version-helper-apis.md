---
description: Die folgenden Funktionen können verwendet werden, um die aktuelle Betriebssystemversion zu bestimmen oder um zu ermitteln, ob es sich um ein Windows-oder Windows Server-Release handelt.
ms.assetid: 2FAF67CD-CEEA-4096-B482-F5E2DF8D6C34
title: Versions Hilfsfunktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 746e6488d949fe6512355d7ef9910c26aaf3b54b
ms.sourcegitcommit: 49df0f62429d21bca96d8704205048267ee0eb59
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/23/2021
ms.locfileid: "106364507"
---
# <a name="version-helper-functions"></a><span data-ttu-id="f5611-103">Versions Hilfsfunktionen</span><span class="sxs-lookup"><span data-stu-id="f5611-103">Version Helper functions</span></span>

<span data-ttu-id="f5611-104">Die folgenden Funktionen können verwendet werden, um die aktuelle Betriebssystemversion zu bestimmen oder um zu ermitteln, ob es sich um ein Windows-oder Windows Server-Release handelt.</span><span class="sxs-lookup"><span data-stu-id="f5611-104">The following functions can be used to determine the current operating system version or identify whether it is a Windows or Windows Server release.</span></span> <span data-ttu-id="f5611-105">Diese Funktionen bieten einfache Tests, bei denen die [verifyversioninfo](/windows/win32/api/Winbase/nf-winbase-verifyversioninfoa) -Funktion verwendet wird, sowie die empfohlenen Vergleiche größer oder gleich, die als robuste Mittel zum Ermitteln der Betriebssystemversion erwiesen werden.</span><span class="sxs-lookup"><span data-stu-id="f5611-105">These functions provide simple tests that use the [VerifyVersionInfo](/windows/win32/api/Winbase/nf-winbase-verifyversioninfoa) function and the recommended greater than or equal to comparisons that are proven as a robust means to determine the operating system version.</span></span>

> [!Note]  
> <span data-ttu-id="f5611-106">Diese APIs werden von " **versionhilfsprogramme. h**" definiert, die im Windows 8.1 Software Development Kit (SDK) enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="f5611-106">These APIs are defined by **versionhelpers.h**, which is included in the Windows 8.1 software development kit (SDK).</span></span> <span data-ttu-id="f5611-107">Diese Datei kann mit anderen Microsoft Visual Studio Releases verwendet werden, um die gleiche Funktionalität für Windows-Versionen vor Windows 8.1 zu implementieren.</span><span class="sxs-lookup"><span data-stu-id="f5611-107">This file can be used with other Microsoft Visual Studio releases to implement the same functionality for Windows versions prior to Windows 8.1.</span></span>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="f5611-108">Funktion</span><span class="sxs-lookup"><span data-stu-id="f5611-108">Function</span></span></th>
<th><span data-ttu-id="f5611-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f5611-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f5611-110"><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindowsxporgreater"><strong>Iswindowsxporgreater</strong></a></span><span class="sxs-lookup"><span data-stu-id="f5611-110"><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindowsxporgreater"><strong>IsWindowsXPOrGreater</strong></a></span></span></td>
<td><span data-ttu-id="f5611-111">Gibt an, ob die aktuelle Betriebssystemversion mit der Version von Windows XP übereinstimmt oder größer als ist.</span><span class="sxs-lookup"><span data-stu-id="f5611-111">Indicates if the current OS version matches, or is greater than, the Windows XP version.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f5611-112"><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindowsxpsp1orgreater"><strong>IsWindowsXPSP1OrGreater</strong></a></span><span class="sxs-lookup"><span data-stu-id="f5611-112"><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindowsxpsp1orgreater"><strong>IsWindowsXPSP1OrGreater</strong></a></span></span></td>
<td><span data-ttu-id="f5611-113">Gibt an, ob die aktuelle Betriebssystemversion oder höher als die Version von Windows XP mit Service Pack 1 (SP1) entspricht.</span><span class="sxs-lookup"><span data-stu-id="f5611-113">Indicates if the current OS version matches, or is greater than, the Windows XP with Service Pack 1 (SP1) version.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f5611-114"><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindowsxpsp2orgreater"><strong>IsWindowsXPSP2OrGreater</strong></a></span><span class="sxs-lookup"><span data-stu-id="f5611-114"><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindowsxpsp2orgreater"><strong>IsWindowsXPSP2OrGreater</strong></a></span></span></td>
<td><span data-ttu-id="f5611-115">Gibt an, ob die aktuelle Betriebssystemversion mit der Version Windows XP mit Service Pack 2 (SP2) übereinstimmt oder höher ist.</span><span class="sxs-lookup"><span data-stu-id="f5611-115">Indicates if the current OS version matches, or is greater than, the Windows XP with Service Pack 2 (SP2) version.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f5611-116"><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindowsxpsp3orgreater"><strong>IsWindowsXPSP3OrGreater</strong></a></span><span class="sxs-lookup"><span data-stu-id="f5611-116"><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindowsxpsp3orgreater"><strong>IsWindowsXPSP3OrGreater</strong></a></span></span></td>
<td><span data-ttu-id="f5611-117">Gibt an, ob die aktuelle Betriebssystemversion oder höher als die Version von Windows XP mit Service Pack 3 (SP3) entspricht.</span><span class="sxs-lookup"><span data-stu-id="f5611-117">Indicates if the current OS version matches, or is greater than, the Windows XP with Service Pack 3 (SP3) version.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f5611-118"><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindowsvistaorgreater"><strong>Iswindowsvistaorgreater</strong></a></span><span class="sxs-lookup"><span data-stu-id="f5611-118"><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindowsvistaorgreater"><strong>IsWindowsVistaOrGreater</strong></a></span></span></td>
<td><span data-ttu-id="f5611-119">Gibt an, ob die aktuelle Betriebssystemversion mit der Windows Vista-Version übereinstimmt oder größer als ist.</span><span class="sxs-lookup"><span data-stu-id="f5611-119">Indicates if the current OS version matches, or is greater than, the Windows Vista version.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f5611-120"><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindowsvistasp1orgreater"><strong>IsWindowsVistaSP1OrGreater</strong></a></span><span class="sxs-lookup"><span data-stu-id="f5611-120"><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindowsvistasp1orgreater"><strong>IsWindowsVistaSP1OrGreater</strong></a></span></span></td>
<td><span data-ttu-id="f5611-121">Gibt an, ob die aktuelle Betriebssystemversion oder höher als die Version von Windows Vista mit Service Pack 1 (SP1) ist.</span><span class="sxs-lookup"><span data-stu-id="f5611-121">Indicates if the current OS version matches, or is greater than, the Windows Vista with Service Pack 1 (SP1) version.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f5611-122"><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindowsvistasp2orgreater"><strong>IsWindowsVistaSP2OrGreater</strong></a></span><span class="sxs-lookup"><span data-stu-id="f5611-122"><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindowsvistasp2orgreater"><strong>IsWindowsVistaSP2OrGreater</strong></a></span></span></td>
<td><span data-ttu-id="f5611-123">Gibt an, ob die aktuelle Betriebssystemversion mit der Version Windows Vista mit Service Pack 2 (SP2) übereinstimmt oder größer als ist.</span><span class="sxs-lookup"><span data-stu-id="f5611-123">Indicates if the current OS version matches, or is greater than, the Windows Vista with Service Pack 2 (SP2) version.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f5611-124"><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindows7orgreater"><strong>IsWindows7OrGreater</strong></a></span><span class="sxs-lookup"><span data-stu-id="f5611-124"><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindows7orgreater"><strong>IsWindows7OrGreater</strong></a></span></span></td>
<td><span data-ttu-id="f5611-125">Gibt an, ob die aktuelle Betriebssystemversion mit der Windows 7-Version übereinstimmt oder größer als ist.</span><span class="sxs-lookup"><span data-stu-id="f5611-125">Indicates if the current OS version matches, or is greater than, the Windows 7 version.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f5611-126"><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindows7sp1orgreater"><strong>IsWindows7SP1OrGreater</strong></a></span><span class="sxs-lookup"><span data-stu-id="f5611-126"><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindows7sp1orgreater"><strong>IsWindows7SP1OrGreater</strong></a></span></span></td>
<td><span data-ttu-id="f5611-127">Gibt an, ob die aktuelle Betriebssystemversion mit der Version Windows 7 mit Service Pack 1 (SP1) übereinstimmt oder höher ist.</span><span class="sxs-lookup"><span data-stu-id="f5611-127">Indicates if the current OS version matches, or is greater than, the Windows 7 with Service Pack 1 (SP1) version.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f5611-128"><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindows8orgreater"><strong>IsWindows8OrGreater</strong></a></span><span class="sxs-lookup"><span data-stu-id="f5611-128"><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindows8orgreater"><strong>IsWindows8OrGreater</strong></a></span></span></td>
<td><span data-ttu-id="f5611-129">Gibt an, ob die aktuelle Betriebssystemversion mit der Windows 8-Version übereinstimmt oder größer als ist.</span><span class="sxs-lookup"><span data-stu-id="f5611-129">Indicates if the current OS version matches, or is greater than, the Windows 8 version.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f5611-130"><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindows8point1orgreater"><strong>IsWindows8Point1OrGreater</strong></a></span><span class="sxs-lookup"><span data-stu-id="f5611-130"><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindows8point1orgreater"><strong>IsWindows8Point1OrGreater</strong></a></span></span></td>
<td><span data-ttu-id="f5611-131">Gibt an, ob die aktuelle Betriebssystemversion mit der Windows 8.1 Version übereinstimmt oder größer als ist.</span><span class="sxs-lookup"><span data-stu-id="f5611-131">Indicates if the current OS version matches, or is greater than, the Windows 8.1 version.</span></span><br/> <span data-ttu-id="f5611-132">Für Windows 10 gibt <a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindows8point1orgreater"><strong>IsWindows8Point1OrGreater</strong></a> false zurück, es sei denn, die Anwendung enthält ein Manifest, das einen Kompatibilitäts Abschnitt enthält, der die GUIDs enthält, die Windows 8.1 und/oder Windows 10 angeben.</span><span class="sxs-lookup"><span data-stu-id="f5611-132">For Windows 10, <a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindows8point1orgreater"><strong>IsWindows8Point1OrGreater</strong></a> returns false unless the application contains a manifest that includes a compatibility section that contains the GUIDs that designate Windows 8.1 and/or Windows 10.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f5611-133"><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindows10orgreater"><strong>IsWindows10OrGreater</strong></a></span><span class="sxs-lookup"><span data-stu-id="f5611-133"><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindows10orgreater"><strong>IsWindows10OrGreater</strong></a></span></span></td>
<td><span data-ttu-id="f5611-134">Gibt an, ob die aktuelle Betriebssystemversion mit der Windows 10-Version übereinstimmt oder größer als ist.</span><span class="sxs-lookup"><span data-stu-id="f5611-134">Indicates if the current OS version matches, or is greater than, the Windows 10 version.</span></span><br/> <span data-ttu-id="f5611-135">Für Windows 10 gibt <a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindows10orgreater"><strong>IsWindows10OrGreater</strong></a> false zurück, es sei denn, die Anwendung enthält ein Manifest, das einen Kompatibilitäts Abschnitt enthält, der die GUID enthält, die Windows 10 bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="f5611-135">For Windows 10, <a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindows10orgreater"><strong>IsWindows10OrGreater</strong></a> returns false unless the application contains a manifest that includes a compatibility section that contains the GUID that designates Windows 10.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f5611-136"><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindowsserver"><strong>Iswindowsserver</strong></a></span><span class="sxs-lookup"><span data-stu-id="f5611-136"><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindowsserver"><strong>IsWindowsServer</strong></a></span></span></td>
<td><span data-ttu-id="f5611-137">Gibt an, ob das aktuelle Betriebssystem ein Windows Server-Release ist.</span><span class="sxs-lookup"><span data-stu-id="f5611-137">Indicates if the current OS is a Windows Server release.</span></span> <span data-ttu-id="f5611-138">Anwendungen, die zwischen Server-und Client Versionen von Windows unterscheiden müssen, sollten diese Funktion aufruft.</span><span class="sxs-lookup"><span data-stu-id="f5611-138">Applications that need to distinguish between server and client versions of Windows should call this function.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f5611-139"><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindowsversionorgreater"><strong>Iswindowsversionorgreater</strong></a></span><span class="sxs-lookup"><span data-stu-id="f5611-139"><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindowsversionorgreater"><strong>IsWindowsVersionOrGreater</strong></a></span></span></td>
<td>
<blockquote><span data-ttu-id="f5611-140">Sie sollten diese Funktion nur verwenden, wenn die anderen bereitgestellten Versions Hilfsobjekte nicht zu Ihrem Szenario passen.</span><span class="sxs-lookup"><span data-stu-id="f5611-140">You should only use this function if the other provided version helper functions do not fit your scenario.</span></span></blockquote>
<br/><span data-ttu-id="f5611-141">Gibt an, ob die aktuelle Betriebssystemversion mit den angegebenen Versionsinformationen übereinstimmt oder größer als ist.</span><span class="sxs-lookup"><span data-stu-id="f5611-141">Indicates if the current OS version matches, or is greater than, the provided version information.</span></span> <span data-ttu-id="f5611-142">Diese Funktion ist nützlich, um eine Version von Windows Server zu bestätigen, die keine Versionsnummer für eine Client Version freigibt.</span><span class="sxs-lookup"><span data-stu-id="f5611-142">This function is useful in confirming a version of Windows Server that doesn't share a version number with a client release.</span></span>
</td>
</tr>
</tbody>
</table>

## <a name="example"></a><span data-ttu-id="f5611-143">Beispiel</span><span class="sxs-lookup"><span data-stu-id="f5611-143">Example</span></span>

<span data-ttu-id="f5611-144">Mit den Inline Funktionen, die in der Header Datei " **versionhilfsprogramme. h** " definiert sind, können Sie die Betriebssystemversion überprüfen, indem Sie beim Testen für eine Version von Windows einen **booleschen** Wert zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="f5611-144">The inline functions defined in the **VersionHelpers.h** header file let you verify the operating system version by returning a **Boolean** value when testing for a version of Windows.</span></span>

<span data-ttu-id="f5611-145">Wenn Ihre Anwendung z. b. Windows 8 oder höher erfordert, verwenden Sie den folgenden Test.</span><span class="sxs-lookup"><span data-stu-id="f5611-145">For example, if your application requires Windows 8 or later, use the following test.</span></span>

```C++
#include <VersionHelpers.h>
 
if (!IsWindows8OrGreater())
{
   MessageBox(NULL, "You need at least Windows 8", "Version Not Supported", MB_OK);
}
```

## <a name="related-topics"></a><span data-ttu-id="f5611-146">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="f5611-146">Related topics</span></span>

- [<span data-ttu-id="f5611-147">OSVERSIONINFOEX</span><span class="sxs-lookup"><span data-stu-id="f5611-147">OSVERSIONINFOEX</span></span>](/windows/desktop/api/Winnt/ns-winnt-osversioninfoexa)
