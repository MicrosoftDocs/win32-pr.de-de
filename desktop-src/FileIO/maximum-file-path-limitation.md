---
description: Maximale Pfadlängen Beschränkung.
title: Maximale Pfadlängen Beschränkung
ms.topic: article
ms.custom: contperf-fy21q1
ms.date: 09/15/2020
ms.openlocfilehash: 3d71d87f69aeb224cde256ce78bd29fd0bf5c291
ms.sourcegitcommit: 78b64f3865e64768b5319d4f010032ee68924a98
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/13/2021
ms.locfileid: "107314803"
---
# <a name="maximum-path-length-limitation"></a>Maximale Pfadlängen Beschränkung

In der Windows-API (mit einigen Ausnahmen, die in den folgenden Absätzen erläutert werden) ist die maximale Länge für einen Pfad **Max \_ path**, der als 260 Zeichen definiert ist. Ein lokaler Pfad ist in der folgenden Reihenfolge strukturiert: Laufwerk Buchstabe, Doppelpunkt, umgekehrter Schrägstrich, namens Komponenten getrennt durch umgekehrte Schrägstriche und ein abschließendes NULL-Zeichen. Der maximale Pfad auf Laufwerk D lautet z. b. "D: \\ *some 256-Zeichen Pfad Zeichenfolge* &lt; NUL &gt; ", wobei " &lt; NUL" &gt; das unsichtbare abschließende Null-Zeichen für die aktuelle System Codepage darstellt. (Die Zeichen < > werden hier zur visuellen Übersichtlichkeit verwendet und können nicht Teil einer gültigen Pfad Zeichenfolge sein.)

Beispielsweise können Sie diese Einschränkung erreichen, wenn Sie ein git-Repository mit langen Dateinamen in einen Ordner mit einem langen Namen Klonen.


> [!Note]  
> Datei-e/a-Funktionen in der Windows-API konvertieren "/" in " \\ " als Teil der Konvertierung des Namens in einen NT-Format Namen, es sei denn, Sie verwenden das \\ \\ \\ Präfix "?", wie in den folgenden Abschnitten beschrieben.

Die Windows-API verfügt über viele Funktionen, die auch über Unicode-Versionen verfügen, um einen Pfad mit erweiterter Länge für eine maximale Gesamt Pfadlänge von 32.767 Zeichen zuzulassen. Diese Art von Pfad besteht aus Komponenten, die durch umgekehrte Schrägstriche voneinander getrennt sind, bis zu dem Wert, der im *lpmaximumcomponentlength* -Parameter der [**GetVolumeInformation**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumeinformationa) -Funktion zurückgegeben wird (dieser Wert ist in der Regel 255 Zeichen). Um einen Pfad mit erweiterter Länge anzugeben, verwenden Sie das \\ \\ \\ Präfix "?". Beispiel: " \\ \\ ? \\ D: \\ *sehr langer Pfad*".

> [!Note]  
> Der maximal zulässige Pfad von 32.767 Zeichen ist ungefähre Werte, da das " \\ \\ ? \\ "-Präfix vom System zur Laufzeit auf eine längere Zeichenfolge erweitert werden kann. diese Erweiterung gilt für die Gesamtlänge.

Das " \\ \\ ? \\ "-Präfix kann auch mit Pfaden verwendet werden, die gemäß der Universal Naming Convention (UNC) erstellt wurden. Um einen solchen Pfad mithilfe von UNC anzugeben, verwenden Sie das " \\ \\ ? \\ UNC \\ "-Präfix. Beispiel: " \\ \\ ? \\ UNC \\ \\ -Server Freigabe ", wobei" Server "der Name des Computers und" Share "der Name des freigegebenen Ordners ist. Diese Präfixe werden nicht als Teil des Pfads verwendet. Sie geben an, dass der Pfad mit minimaler Änderung an das System übergeben werden soll. Dies bedeutet, dass Sie keine Schrägstriche verwenden können, um Pfad Trennzeichen darzustellen, oder einen Punkt, der das aktuelle Verzeichnis darstellt, oder doppelte Punkte, um das übergeordnete Verzeichnis darzustellen. Da Sie das " \\ \\ ?"- \\ Präfix nicht mit einem relativen Pfad verwenden können, sind relative Pfade immer auf die Summe der **maximalen \_ Pfad** Zeichen beschränkt.

Es ist nicht erforderlich, Unicode-Normalisierungen für Pfad-und Dateinamen Zeichenfolgen für die Verwendung durch die Windows-Datei-e/a-API-Funktionen auszuführen, da das Dateisystempfad-und Dateinamen als nicht transparente Sequenz von **WCHAR** s behandelt. Jede Normalisierung, die für Ihre Anwendung erforderlich ist, sollte vor allen Aufrufen von verknüpften Windows-Datei-e/a-API-Funktionen durchgeführt werden.

Wenn Sie eine API zum Erstellen eines Verzeichnisses verwenden, darf der angegebene Pfad nicht so lang sein, dass Sie keinen 8,3-Dateinamen anhängen können (d. h., der Verzeichnisname darf den **maximalen \_ Pfad** minus 12 nicht überschreiten).

Die Shell und das Dateisystem haben unterschiedliche Anforderungen. Es ist möglich, einen Pfad mit der Windows-API zu erstellen, die von der shellbenutzerschnittstelle nicht ordnungsgemäß interpretiert werden kann.

## <a name="enable-long-paths-in-windows-10-version-1607-and-later"></a>Aktivieren von langen Pfaden in Windows 10, Version 1607 und höher

Ab Windows 10, Version 1607, wurden die **maximalen \_ Pfad** Einschränkungen aus den gängigen Win32-Datei-und Verzeichnisfunktionen entfernt. Sie müssen sich jedoch für das neue Verhalten entscheiden.

Um das neue Verhalten für lange Pfade zu aktivieren, müssen die beiden folgenden Bedingungen erfüllt sein:

* Der Registrierungsschlüssel `Computer\HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Control\FileSystem\LongPathsEnabled (Type: REG_DWORD)` muss vorhanden und auf 1 festgelegt sein. Der Wert des Schlüssels wird vom System (pro Prozess) nach dem ersten Aufrufe einer betroffenen Win32-Datei oder-Verzeichnis Funktion zwischengespeichert (Weitere Informationen finden Sie unten in der Liste der Funktionen). Der Registrierungsschlüssel wird während der Lebensdauer des Prozesses nicht erneut geladen. Damit alle apps auf dem System den Wert des Schlüssels erkennen können, ist möglicherweise ein Neustart erforderlich, da einige Prozesse möglicherweise gestartet wurden, bevor der Schlüssel festgelegt wurde.

Sie können diesen Code auch in eine `.reg` Datei kopieren, die diese für Sie festlegen kann:
```cmd
Windows Registry Editor Version 5.00

[HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Control\FileSystem]
"LongPathsEnabled"=dword:00000001

```

> [!NOTE]  
> Dieser Registrierungsschlüssel kann auch über Gruppenrichtlinie unter gesteuert werden `Computer Configuration > Administrative Templates > System > Filesystem > Enable Win32 long paths` .

* Das [Anwendungs Manifest](../sbscs/application-manifests.md) muss auch das- `longPathAware` Element enthalten.

    ```XML
    <application xmlns="urn:schemas-microsoft-com:asm.v3">
        <windowsSettings xmlns:ws2="http://schemas.microsoft.com/SMI/2016/WindowsSettings">
            <ws2:longPathAware>true</ws2:longPathAware>
        </windowsSettings>
    </application>
    ```

Dabei handelt es sich um die verzeichnisverwaltungsfunktionen, für die Sie keine **maximalen \_ Pfad** Einschränkungen mehr haben, wenn Sie sich für langes Pfad Verhalten entscheiden: "kreatedirectoryw", "deatedirectoryexw getcurrentdirectoryw removedirectoryw setcurrentdirectoryw".

Dabei handelt es sich um die Dateiverwaltungsfunktionen, für die Sie keine **maximalen \_ Pfad** Einschränkungen mehr haben, wenn Sie sich für langes Pfad Verhalten entscheiden: copyfilew, CopyFile2, copyfileexw, kreatefilew, CreateFile2, | atehardlinkw, kreatesymboliclinkw, deletefilew, findfirstfilew, findfirstfileexw, findnextfilew, getfileattributesw, getfileattributesexw, setfileattributesw, getfullpathnamew, getlongpathnamew, wvefilew, muvefileexw, wvefilewithprogressw, replacefilew, searchpathw, findfirstfileamew, findnextfileamew, findfirststreamw, findnextstreamw, getcompressedfilesizew, getfinalpathnamebylenker w.
