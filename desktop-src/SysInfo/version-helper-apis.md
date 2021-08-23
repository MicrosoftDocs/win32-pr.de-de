---
description: Die folgenden Funktionen können verwendet werden, um die aktuelle Betriebssystemversion zu bestimmen oder zu ermitteln, ob es sich um ein Windows oder Windows Server-Release handelt.
ms.assetid: 2FAF67CD-CEEA-4096-B482-F5E2DF8D6C34
title: Versionshilfsfunktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a7156070e9c793e537d976c82a632142e04cd6669b110b7d0b9fc8da95671b3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118884171"
---
# <a name="version-helper-functions"></a>Versionshilfsfunktionen

Die folgenden Funktionen können verwendet werden, um die aktuelle Betriebssystemversion zu bestimmen oder zu ermitteln, ob es sich um ein Windows oder Windows Server-Release handelt. Diese Funktionen stellen einfache Tests bereit, die die [VerifyVersionInfo-Funktion](/windows/win32/api/Winbase/nf-winbase-verifyversioninfoa) und die empfohlenen Größer-als-oder-gleich-Vergleiche verwenden, die sich als robustes Mittel zum Bestimmen der Betriebssystemversion erwiesen haben.

> [!Note]  
> Diese APIs werden durch **versionhelpers.h** definiert, das im Windows 8.1 Software Development Kit (SDK) enthalten ist. Diese Datei kann mit anderen Microsoft Visual Studio Releases verwendet werden, um die gleiche Funktionalität für Windows Versionen vor Windows 8.1 zu implementieren.

<table>
<thead>
<tr class="header">
<th>Funktion</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindowsxporgreater"><strong>IsWindowsXPOrGreater</strong></a></td>
<td>Gibt an, ob die aktuelle Betriebssystemversion mit der Windows XP-Version übereinstimmt oder größer als ist.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindowsxpsp1orgreater"><strong>IsWindowsXPSP1OrGreater</strong></a></td>
<td>Gibt an, ob die aktuelle Betriebssystemversion mit der Version Windows XP mit Service Pack 1 (SP1) übereinstimmt oder größer als ist.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindowsxpsp2orgreater"><strong>IsWindowsXPSP2OrGreater</strong></a></td>
<td>Gibt an, ob die aktuelle Betriebssystemversion mit der Version Windows XP mit Service Pack 2 (SP2) übereinstimmt oder größer als ist.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindowsxpsp3orgreater"><strong>IsWindowsXPSP3OrGreater</strong></a></td>
<td>Gibt an, ob die aktuelle Betriebssystemversion mit der Version Windows XP mit Service Pack 3 (SP3) übereinstimmt oder größer ist.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindowsvistaorgreater"><strong>IsWindowsVistaOrGreater</strong></a></td>
<td>Gibt an, ob die aktuelle Betriebssystemversion mit der Version Windows Vista übereinstimmt oder größer als ist.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindowsvistasp1orgreater"><strong>IsWindowsVistaSP1OrGreater</strong></a></td>
<td>Gibt an, ob die aktuelle Betriebssystemversion mit der Version von Service Pack 1 (SP1) Windows Vista übereinstimmt oder größer ist.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindowsvistasp2orgreater"><strong>IsWindowsVistaSP2OrGreater</strong></a></td>
<td>Gibt an, ob die aktuelle Betriebssystemversion mit der Version Windows Vista mit Service Pack 2 (SP2) übereinstimmt oder größer als ist.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindows7orgreater"><strong>IsWindows7OrGreater</strong></a></td>
<td>Gibt an, ob die aktuelle Betriebssystemversion mit der Version Windows 7 übereinstimmt oder größer als ist.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindows7sp1orgreater"><strong>IsWindows7SP1OrGreater</strong></a></td>
<td>Gibt an, ob die aktuelle Betriebssystemversion mit der Service Pack 1-Version (SP1) übereinstimmt oder größer als der Windows 7 ist.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindows8orgreater"><strong>IsWindows8OrGreater</strong></a></td>
<td>Gibt an, ob die aktuelle Betriebssystemversion mit der Windows 8 Version übereinstimmt oder größer als ist.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindows8point1orgreater"><strong>IsWindows8Point1OrGreater</strong></a></td>
<td>Gibt an, ob die aktuelle Betriebssystemversion mit der Windows 8.1 Version übereinstimmt oder größer als ist.<br/> Für Windows 10 gibt <a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindows8point1orgreater"><strong>IsWindows8Point1OrGreater</strong></a> false zurück, es sei denn, die Anwendung enthält ein Manifest mit einem Kompatibilitätsabschnitt, der die GUIDs enthält, die Windows 8.1 und/oder Windows 10 festlegen.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindows10orgreater"><strong>IsWindows10OrGreater</strong></a></td>
<td>Gibt an, ob die aktuelle Betriebssystemversion mit der Windows 10 Version übereinstimmt oder größer als ist.<br/> Für Windows 10 gibt <a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindows10orgreater"><strong>IsWindows10OrGreater</strong></a> false zurück, es sei denn, die Anwendung enthält ein Manifest mit einem Kompatibilitätsabschnitt, der die GUID enthält, die Windows 10 angibt.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindowsserver"><strong>IsWindowsServer</strong></a></td>
<td>Gibt an, ob das aktuelle Betriebssystem ein Windows Server-Release ist. Anwendungen, die zwischen Server- und Clientversionen von Windows unterscheiden müssen, sollten diese Funktion aufrufen.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindowsversionorgreater"><strong>IsWindowsVersionOrGreater</strong></a></td>
<td>
<blockquote>Sie sollten diese Funktion nur verwenden, wenn die anderen bereitgestellten Versionshilfsfunktionen nicht zu Ihrem Szenario passen.</blockquote>
<br/>Gibt an, ob die aktuelle Betriebssystemversion mit den bereitgestellten Versionsinformationen übereinstimmt oder größer als ist. Diese Funktion ist nützlich, um eine Version von Windows Server zu bestätigen, die keine Versionsnummer mit einer Clientversion gemeinsam verwendet.
</td>
</tr>
</tbody>
</table>

## <a name="example"></a>Beispiel

Mit den in der **Headerdatei VersionHelpers.h** definierten Inlinefunktionen können Sie die Betriebssystemversion überprüfen, indem Sie beim Testen auf eine Version von Windows einen **booleschen** Wert zurückgeben.

Wenn Ihre Anwendung beispielsweise Windows 8 oder höher erfordert, verwenden Sie den folgenden Test.

```C++
#include <VersionHelpers.h>
 
if (!IsWindows8OrGreater())
{
   MessageBox(NULL, "You need at least Windows 8", "Version Not Supported", MB_OK);
}
```

## <a name="related-topics"></a>Zugehörige Themen

- [OSVERSIONINFOEX](/windows/desktop/api/Winnt/ns-winnt-osversioninfoexa)
