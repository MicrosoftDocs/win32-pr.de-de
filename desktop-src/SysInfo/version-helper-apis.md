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
# <a name="version-helper-functions"></a>Versions Hilfsfunktionen

Die folgenden Funktionen können verwendet werden, um die aktuelle Betriebssystemversion zu bestimmen oder um zu ermitteln, ob es sich um ein Windows-oder Windows Server-Release handelt. Diese Funktionen bieten einfache Tests, bei denen die [verifyversioninfo](/windows/win32/api/Winbase/nf-winbase-verifyversioninfoa) -Funktion verwendet wird, sowie die empfohlenen Vergleiche größer oder gleich, die als robuste Mittel zum Ermitteln der Betriebssystemversion erwiesen werden.

> [!Note]  
> Diese APIs werden von " **versionhilfsprogramme. h**" definiert, die im Windows 8.1 Software Development Kit (SDK) enthalten ist. Diese Datei kann mit anderen Microsoft Visual Studio Releases verwendet werden, um die gleiche Funktionalität für Windows-Versionen vor Windows 8.1 zu implementieren.

<table>
<thead>
<tr class="header">
<th>Funktion</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindowsxporgreater"><strong>Iswindowsxporgreater</strong></a></td>
<td>Gibt an, ob die aktuelle Betriebssystemversion mit der Version von Windows XP übereinstimmt oder größer als ist.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindowsxpsp1orgreater"><strong>IsWindowsXPSP1OrGreater</strong></a></td>
<td>Gibt an, ob die aktuelle Betriebssystemversion oder höher als die Version von Windows XP mit Service Pack 1 (SP1) entspricht.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindowsxpsp2orgreater"><strong>IsWindowsXPSP2OrGreater</strong></a></td>
<td>Gibt an, ob die aktuelle Betriebssystemversion mit der Version Windows XP mit Service Pack 2 (SP2) übereinstimmt oder höher ist.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindowsxpsp3orgreater"><strong>IsWindowsXPSP3OrGreater</strong></a></td>
<td>Gibt an, ob die aktuelle Betriebssystemversion oder höher als die Version von Windows XP mit Service Pack 3 (SP3) entspricht.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindowsvistaorgreater"><strong>Iswindowsvistaorgreater</strong></a></td>
<td>Gibt an, ob die aktuelle Betriebssystemversion mit der Windows Vista-Version übereinstimmt oder größer als ist.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindowsvistasp1orgreater"><strong>IsWindowsVistaSP1OrGreater</strong></a></td>
<td>Gibt an, ob die aktuelle Betriebssystemversion oder höher als die Version von Windows Vista mit Service Pack 1 (SP1) ist.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindowsvistasp2orgreater"><strong>IsWindowsVistaSP2OrGreater</strong></a></td>
<td>Gibt an, ob die aktuelle Betriebssystemversion mit der Version Windows Vista mit Service Pack 2 (SP2) übereinstimmt oder größer als ist.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindows7orgreater"><strong>IsWindows7OrGreater</strong></a></td>
<td>Gibt an, ob die aktuelle Betriebssystemversion mit der Windows 7-Version übereinstimmt oder größer als ist.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindows7sp1orgreater"><strong>IsWindows7SP1OrGreater</strong></a></td>
<td>Gibt an, ob die aktuelle Betriebssystemversion mit der Version Windows 7 mit Service Pack 1 (SP1) übereinstimmt oder höher ist.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindows8orgreater"><strong>IsWindows8OrGreater</strong></a></td>
<td>Gibt an, ob die aktuelle Betriebssystemversion mit der Windows 8-Version übereinstimmt oder größer als ist.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindows8point1orgreater"><strong>IsWindows8Point1OrGreater</strong></a></td>
<td>Gibt an, ob die aktuelle Betriebssystemversion mit der Windows 8.1 Version übereinstimmt oder größer als ist.<br/> Für Windows 10 gibt <a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindows8point1orgreater"><strong>IsWindows8Point1OrGreater</strong></a> false zurück, es sei denn, die Anwendung enthält ein Manifest, das einen Kompatibilitäts Abschnitt enthält, der die GUIDs enthält, die Windows 8.1 und/oder Windows 10 angeben.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindows10orgreater"><strong>IsWindows10OrGreater</strong></a></td>
<td>Gibt an, ob die aktuelle Betriebssystemversion mit der Windows 10-Version übereinstimmt oder größer als ist.<br/> Für Windows 10 gibt <a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindows10orgreater"><strong>IsWindows10OrGreater</strong></a> false zurück, es sei denn, die Anwendung enthält ein Manifest, das einen Kompatibilitäts Abschnitt enthält, der die GUID enthält, die Windows 10 bezeichnet.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindowsserver"><strong>Iswindowsserver</strong></a></td>
<td>Gibt an, ob das aktuelle Betriebssystem ein Windows Server-Release ist. Anwendungen, die zwischen Server-und Client Versionen von Windows unterscheiden müssen, sollten diese Funktion aufruft.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindowsversionorgreater"><strong>Iswindowsversionorgreater</strong></a></td>
<td>
<blockquote>Sie sollten diese Funktion nur verwenden, wenn die anderen bereitgestellten Versions Hilfsobjekte nicht zu Ihrem Szenario passen.</blockquote>
<br/>Gibt an, ob die aktuelle Betriebssystemversion mit den angegebenen Versionsinformationen übereinstimmt oder größer als ist. Diese Funktion ist nützlich, um eine Version von Windows Server zu bestätigen, die keine Versionsnummer für eine Client Version freigibt.
</td>
</tr>
</tbody>
</table>

## <a name="example"></a>Beispiel

Mit den Inline Funktionen, die in der Header Datei " **versionhilfsprogramme. h** " definiert sind, können Sie die Betriebssystemversion überprüfen, indem Sie beim Testen für eine Version von Windows einen **booleschen** Wert zurückgeben.

Wenn Ihre Anwendung z. b. Windows 8 oder höher erfordert, verwenden Sie den folgenden Test.

```C++
#include <VersionHelpers.h>
 
if (!IsWindows8OrGreater())
{
   MessageBox(NULL, "You need at least Windows 8", "Version Not Supported", MB_OK);
}
```

## <a name="related-topics"></a>Zugehörige Themen

- [OSVERSIONINFOEX](/windows/desktop/api/Winnt/ns-winnt-osversioninfoexa)
