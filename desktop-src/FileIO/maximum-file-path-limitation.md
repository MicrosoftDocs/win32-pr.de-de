---
description: Maximale Pfadlängenbeschränkung.
title: Maximale Längenbeschränkung für Pfade
ms.topic: article
ms.custom: contperf-fy21q1
ms.date: 09/15/2020
ms.openlocfilehash: f57aba8d022e3b193289c8abf884e661797a0cf8585b7537fae19c171250eb12
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119914760"
---
# <a name="maximum-path-length-limitation"></a>Maximale Längenbeschränkung für Pfade

In der Windows-API (mit einigen Ausnahmen, die in den folgenden Absätzen erläutert werden) ist die maximale Länge für einen Pfad **MAX \_ PATH**, der als 260 Zeichen definiert ist. Ein lokaler Pfad ist in der folgenden Reihenfolge strukturiert: Laufwerkbuchstaben, Doppelpunkt, schräger Schrägstrich, Durch schräge Schrägstriche getrennte Namenskomponenten und ein beendendes NULL-Zeichen. Der maximale Pfad auf Laufwerk D ist z. B. "D: einige \\ *256-Zeichen-Pfadzeichenfolge* NUL ", wobei " NUL " das unsichtbare beendende NULL-Zeichen für die aktuelle &lt; &gt; &lt; Systemcodepage &gt; darstellt. (Die hier < > Zeichen werden aus Gründen der visuellen Übersichtlichkeit verwendet und können nicht Teil einer gültigen Pfadzeichenfolge sein.)

Diese Einschränkung kann beispielsweise gelten, wenn Sie ein Git-Repository mit langen Dateinamen in einen Ordner klonen, der selbst einen langen Namen hat.


> [!Note]  
> Datei-E/A-Funktionen in der Windows-API konvertieren "/" in " " als Teil der Konvertierung des Namens in einen NT-Formatnamen, mit Ausnahme der Verwendung des Präfixes " ? ", wie in den folgenden Abschnitten \\ \\ \\ \\ beschrieben.

Die Windows-API verfügt über viele Funktionen, die auch Über Unicode-Versionen verfügen, um einen Pfad mit erweiterter Länge für eine maximale Gesamtlänge von 32.767 Zeichen zu ermöglichen. Dieser Pfadtyp besteht aus Komponenten, die durch schräge Schrägstriche getrennt sind, jeweils bis zu dem Wert, der im *lpMaximumComponentLength-Parameter* der [**GetVolumeInformation-Funktion**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumeinformationa) zurückgegeben wird (dieser Wert ist in der Regel 255 Zeichen). Um einen Pfad mit erweiterter Länge anzugeben, verwenden Sie das Präfix " \\ \\ ? \\ ". Beispiel: " \\ \\ ? \\ D: \\ *sehr langer Pfad*".

> [!Note]  
> Der maximale Pfad von 32.767 Zeichen ist ungefähr, da das Präfix " ? " vom System zur Laufzeit auf eine längere Zeichenfolge erweitert werden kann, und diese Erweiterung gilt für die \\ \\ \\ Gesamtlänge.

Das Präfix " ? " kann auch mit Pfaden verwendet werden, die gemäß der universal \\ \\ naming convention \\ (UNC) erstellt wurden. Um einen solchen Pfad mit UNC anzugeben, verwenden Sie " \\ \\ ? \\ \\UNC"-Präfix. Beispiel: " \\ \\ ? \\ UNC-Serverfreigabe", wobei "server" der Name des Computers \\ \\ und "freigabe" der Name des freigegebenen Ordners ist. Diese Präfixe werden nicht als Teil des Pfads selbst verwendet. Sie geben an, dass der Pfad mit minimaler Änderung an das System übergeben werden soll. Das bedeutet, dass Sie keine Schrägstriche zur Darstellung von Pfadtrennzeichen oder einen Punkt zur Darstellung des aktuellen Verzeichnisses oder doppelte Punkte verwenden können, um das übergeordnete Verzeichnis zu darstellen. Da Sie das Präfix " ? " nicht mit einem relativen Pfad verwenden können, sind relative Pfade immer auf eine Gesamtanzahl von \\ \\ \\ **MAX \_ PATH-Zeichen** beschränkt.

Es ist nicht notwendig, eine Unicode-Normalisierung für Pfad- und Dateinamenzeichenfolgen auszuführen, die von den E/A-API-Funktionen der Windows-Datei verwendet werden, da das Dateisystem Pfad- und Dateinamen als nicht transparente Sequenz von **WCHAR-Dateien** behandelt. Jede Normalisierung, die für Ihre Anwendung erforderlich ist, sollte vor diesem Hintergrund durchgeführt werden, außerhalb aller Aufrufe verwandter Windows-E/A-API-Funktionen.

Wenn Sie eine API zum Erstellen eines Verzeichnisses verwenden, darf der angegebene Pfad nicht so lang sein, dass Sie keinen 8.3-Dateinamen anfügen können (d. h., der Verzeichnisname darf **MAX \_ PATH** minus 12 nicht überschreiten).

Die Shell und das Dateisystem haben unterschiedliche Anforderungen. Es ist möglich, einen Pfad mit der Windows-API zu erstellen, die die Shell-Benutzeroberfläche nicht ordnungsgemäß interpretieren kann.

## <a name="enable-long-paths-in-windows-10-version-1607-and-later"></a>Aktivieren von langen Pfaden in Windows 10 Version 1607 und höher

Ab Version Windows 10 Version 1607 wurden **MAX \_ PATH-Einschränkungen** aus allgemeinen Win32-Datei- und -Verzeichnisfunktionen entfernt. Sie müssen sich jedoch für das neue Verhalten entscheiden.

Um das neue Verhalten für lange Pfade zu aktivieren, müssen die beiden folgenden Bedingungen erfüllt sein:

* Der Registrierungsschlüssel `Computer\HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Control\FileSystem\LongPathsEnabled (Type: REG_DWORD)` muss vorhanden sein und auf 1 festgelegt werden. Der Wert des Schlüssels wird vom System (pro Prozess) nach dem ersten Aufruf einer betroffenen Win32-Datei oder Verzeichnisfunktion zwischengespeichert (siehe unten für die Liste der Funktionen). Der Registrierungsschlüssel wird während der Lebensdauer des Prozesses nicht erneut geladen. Damit alle Apps im System den Wert des Schlüssels erkennen können, ist möglicherweise ein Neustart erforderlich, da einige Prozesse möglicherweise gestartet wurden, bevor der Schlüssel festgelegt wurde.

Sie können diesen Code auch in eine Datei kopieren, die dies für Sie festlegen kann, oder den PowerShell-Befehl aus einem Terminalfenster mit `.reg` erhöhten Rechten verwenden:
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
> Dieser Registrierungsschlüssel kann auch über die -Gruppenrichtlinie gesteuert `Computer Configuration > Administrative Templates > System > Filesystem > Enable Win32 long paths` werden.

* Das [Anwendungsmanifest](../sbscs/application-manifests.md) muss auch das -Element `longPathAware` enthalten.

    ```XML
    <application xmlns="urn:schemas-microsoft-com:asm.v3">
        <windowsSettings xmlns:ws2="http://schemas.microsoft.com/SMI/2016/WindowsSettings">
            <ws2:longPathAware>true</ws2:longPathAware>
        </windowsSettings>
    </application>
    ```

Dies sind die Verzeichnisverwaltungsfunktionen, die keine **MAX \_ PATH-Einschränkungen** mehr haben, wenn Sie langes Pfadverhalten verwenden: CreateDirectoryW, CreateDirectoryExW GetCurrentDirectoryW RemoveDirectoryW SetCurrentDirectoryW.

Dies sind die Dateiverwaltungsfunktionen, für die keine **MAX \_ PATH-Einschränkungen** mehr gelten, wenn Sie langes Pfadverhalten verwenden: CopyFileW, CopyFile2, CopyFileExW, CreateFileW, CreateFile2, CreateHardLinkW, CreateSymbolicLinkW, DeleteFileW, FindFirstFileW, FindFirstFileExW, FindNextFileW, GetFileAttributesW, GetFileAttributesExW, SetFileAttributesW, GetFullPathNameW, GetLongPathNameW, MoveFileW, MoveFileExW, MoveFileWithProgressW, ReplaceFileW, SearchPathW, FindFirstFileNameW, FindNextFileNameW, FindFirstStreamW, FindNextStreamW, GetCompressedFileSizeW, GetFinalPathNameByHandleW.
