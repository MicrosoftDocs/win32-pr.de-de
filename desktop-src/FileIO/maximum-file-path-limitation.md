---
description: Maximale Längenbeschränkung des Pfads.
title: Maximale Längenbeschränkung für Pfade
ms.topic: article
ms.custom: contperf-fy21q1
ms.date: 09/15/2020
ms.openlocfilehash: 4bf5050f24827a2033c1e56fd9413c04f4e59500
ms.sourcegitcommit: ece80b9b7082415b2f894b0696b6b3f0c8544d72
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/22/2021
ms.locfileid: "107899739"
---
# <a name="maximum-path-length-limitation"></a>Maximale Längenbeschränkung für Pfade

In der Windows-API (mit einigen Ausnahmen, die in den folgenden Abschnitten erläutert werden) ist die maximale Länge für einen Pfad **MAX \_ PATH**, die als 260 Zeichen definiert ist. Ein lokaler Pfad ist in der folgenden Reihenfolge strukturiert: Laufwerkbuchstabe, Doppelpunkt, umgekehrter Schrägstrich, durch umgekehrte Schrägstriche getrennte Namenskomponenten und ein abschließendes NULL-Zeichen. Der maximale Pfad auf Laufwerk D ist z. B. "D: \\ *einige 256-Zeichen Pfadzeichenfolge* &lt; NUL &gt; ", wobei " &lt; NUL &gt; " das unsichtbare abschließende NULL-Zeichen für die aktuelle Systemcodepage darstellt. (Die Zeichen < > werden hier zur visuellen Übersichtlichkeit verwendet und können nicht Teil einer gültigen Pfadzeichenfolge sein.)

Diese Einschränkung kann beispielsweise auftreten, wenn Sie ein Git-Repository mit langen Dateinamen in einen Ordner klonen, der selbst einen langen Namen hat.


> [!Note]  
> Datei-E/A-Funktionen in der Windows-API konvertieren "/" \\ in " " als Teil der Konvertierung des Namens in einen Namen im NT-Format, außer wenn das Präfix " ? " verwendet wird, \\ \\ wie in den \\ folgenden Abschnitten beschrieben.

Die Windows-API verfügt über viele Funktionen, die auch über Unicode-Versionen verfügen, um einen Pfad mit erweiterter Länge für eine maximale Gesamtpfadlänge von 32.767 Zeichen zuzulassen. Dieser Pfadtyp besteht aus Komponenten, die durch umgekehrte Schrägstriche getrennt sind, jeweils bis zu dem Wert, der im *lpMaximumComponentLength-Parameter* der [**GetVolumeInformation-Funktion**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumeinformationa) zurückgegeben wird (dieser Wert beträgt normalerweise 255 Zeichen). Um einen Pfad mit erweiterter Länge anzugeben, verwenden Sie das Präfix " \\ \\ ? \\ ". Beispiel: " \\ \\ ? \\ D: \\ *sehr langer Pfad*".

> [!Note]  
> Der maximale Pfad von 32.767 Zeichen ist ungefähr, da das Präfix " \\ \\ ? " vom System zur Laufzeit auf \\ eine längere Zeichenfolge erweitert werden kann, und diese Erweiterung gilt für die Gesamtlänge.

Das Präfix " \\ \\ ? " kann auch \\ mit Pfaden verwendet werden, die gemäß der Universal Naming Convention (UNC) erstellt wurden. Um einen solchen Pfad mit UNC anzugeben, verwenden Sie " \\ \\ ? \\ \\UNC"-Präfix. Beispiel: " \\ \\ ? \\ UNC-Serverfreigabe", wobei "server" der Name des Computers \\ \\ und "freigabe" der Name des freigegebenen Ordners ist. Diese Präfixe werden nicht als Teil des Pfads selbst verwendet. Sie geben an, dass der Pfad mit minimaler Änderung an das System übergeben werden soll. Das bedeutet, dass Sie keine Schrägstriche zur Darstellung von Pfadtrennzeichen oder einen Punkt zur Darstellung des aktuellen Verzeichnisses oder doppelte Punkte verwenden können, um das übergeordnete Verzeichnis zu darstellen. Da Sie das Präfix " ? " nicht mit einem relativen Pfad verwenden können, sind relative Pfade immer auf eine Gesamtanzahl von \\ \\ \\ **MAX \_ PATH-Zeichen** beschränkt.

Es ist nicht notwendig, eine Unicode-Normalisierung für Pfad- und Dateinamenzeichenfolgen für die Verwendung durch die Windows-Datei-E/A-API-Funktionen durchzuführen, da das Dateisystem Pfad- und Dateinamen als nicht transparente Sequenz von **WCHAR-Dateien** behandelt. Jede Normalisierung, die für Ihre Anwendung erforderlich ist, sollte vor diesem Hintergrund durchgeführt werden, also außerhalb aller Aufrufe verwandter Windows-Datei-E/A-API-Funktionen.

Wenn Sie eine API zum Erstellen eines Verzeichnisses verwenden, darf der angegebene Pfad nicht so lang sein, dass Sie keinen 8.3-Dateinamen anfügen können (d. h., der Verzeichnisname darf **MAX \_ PATH** minus 12 nicht überschreiten).

Die Shell und das Dateisystem haben unterschiedliche Anforderungen. Es ist möglich, einen Pfad mit der Windows-API zu erstellen, der von der Shellbenutzeroberfläche nicht ordnungsgemäß interpretiert werden kann.

## <a name="enable-long-paths-in-windows-10-version-1607-and-later"></a>Aktivieren von langen Pfaden in Windows 10 Version 1607 und höher

Ab Version Windows 10 Version 1607 wurden **MAX \_ PATH-Einschränkungen** aus allgemeinen Win32-Datei- und -Verzeichnisfunktionen entfernt. Sie müssen sich jedoch für das neue Verhalten entscheiden.

Um das neue Verhalten für lange Pfade zu aktivieren, müssen die beiden folgenden Bedingungen erfüllt sein:

* Der Registrierungsschlüssel `Computer\HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Control\FileSystem\LongPathsEnabled (Type: REG_DWORD)` muss vorhanden sein und auf 1 festgelegt werden. Der Wert des Schlüssels wird vom System (pro Prozess) nach dem ersten Aufruf einer betroffenen Win32-Datei oder Verzeichnisfunktion zwischengespeichert (siehe unten für die Liste der Funktionen). Der Registrierungsschlüssel wird während der Lebensdauer des Prozesses nicht erneut geladen. Damit alle Apps im System den Wert des Schlüssels erkennen können, ist möglicherweise ein Neustart erforderlich, da einige Prozesse möglicherweise gestartet wurden, bevor der Schlüssel festgelegt wurde.

Sie können diesen Code auch in eine `.reg` Datei kopieren, die dies für Sie festlegen kann, oder den PowerShell-Befehl über ein Terminalfenster mit erhöhten Rechten verwenden:
# <a name="cmd"></a>[cmd](#tab/cmd)

```cmd
Windows Registry Editor Version 5.00

[HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Control\FileSystem]
"LongPathsEnabled"=dword:00000001

```

# <a name="powershell"></a>[PowerShell](#tab/powershell)

```powershell
New-ItemProperty -Path "HKLM:\SYSTEM\CurrentControlSet\Control\FileSystem" `
-Name "LongPathsEnabled" -Value 1 -PropertyType DWORD -Force

```

---

> [!NOTE]  
> Dieser Registrierungsschlüssel kann auch über Gruppenrichtlinie unter gesteuert `Computer Configuration > Administrative Templates > System > Filesystem > Enable Win32 long paths` werden.

* Das [Anwendungsmanifest](../sbscs/application-manifests.md) muss auch das `longPathAware` -Element enthalten.

    ```XML
    <application xmlns="urn:schemas-microsoft-com:asm.v3">
        <windowsSettings xmlns:ws2="http://schemas.microsoft.com/SMI/2016/WindowsSettings">
            <ws2:longPathAware>true</ws2:longPathAware>
        </windowsSettings>
    </application>
    ```

Dies sind die Verzeichnisverwaltungsfunktionen, die keine **MAX \_ PATH-Einschränkungen** mehr aufweisen, wenn Sie sich für das Verhalten mit langen Pfaden entscheiden: CreateDirectoryW, CreateDirectoryExW GetCurrentDirectoryW RemoveDirectoryW SetCurrentDirectoryW.

Dies sind die Dateiverwaltungsfunktionen, die keine **MAX \_ PATH-Einschränkungen** mehr aufweisen, wenn Sie sich für das Verhalten des langen Pfads entscheiden: CopyFileW, CopyFile2, CopyFileExW, CreateFileW, CreateFile2, CreateHardLinkW, CreateSymbolicLinkW, DeleteFileW, FindFirstFileW, FindFirstFileExW, FindNextFileW, GetFileAttributesW, GetFileAttributesExW, SetFileAttributesW, GetFullPathNameW, GetLongPathNameW, MoveFileW, MoveFileExW, MoveFileWithProgressW, ReplaceFileW, SearchPathW, FindFirstFileNameW, FindNextFileNameW, FindFirstStreamW, FindNextStreamW, GetCompressedFileSizeW, GetFinalPathNameByHandleW.
