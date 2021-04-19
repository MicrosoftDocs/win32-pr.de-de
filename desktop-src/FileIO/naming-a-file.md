---
description: Alle von Windows unterstützten Dateisysteme verwenden das Konzept von Dateien und Verzeichnissen, um auf Daten zuzugreifen, die auf einem Datenträger oder einem Gerät gespeichert sind.
ms.assetid: 121cd5b2-e6fd-4eb4-99b4-b652d27b53e8
title: Benennen von Dateien, Pfaden und Namespaces
ms.custom: contperf-fy21q1
ms.topic: article
ms.date: 09/15/2020
ms.openlocfilehash: 59f626c931a61255cef8be9ede594cb97924cfb0
ms.sourcegitcommit: f374b50b37160b683da16b59ac9340282a8f50a5
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/04/2021
ms.locfileid: "106343117"
---
# <a name="naming-files-paths-and-namespaces"></a>Benennen von Dateien, Pfaden und Namespaces

Alle von Windows unterstützten Dateisysteme verwenden das Konzept von Dateien und Verzeichnissen, um auf Daten zuzugreifen, die auf einem Datenträger oder einem Gerät gespeichert sind. Windows-Entwickler, die mit den Windows-APIs für die Datei-und Geräte-e/a arbeiten, sollten die verschiedenen Regeln, Konventionen und Einschränkungen von Namen für Dateien und Verzeichnisse verstehen.

Auf Daten kann von Datenträgern, Geräten und Netzwerkfreigaben mithilfe von Datei-e/a-APIs zugegriffen werden. Dateien und Verzeichnisse, zusammen mit Namespaces, sind Teil des Konzepts eines Pfades, bei dem es sich um eine Zeichen folgen Darstellung handelt, bei der die Daten unabhängig von einem Datenträger oder einem Gerät oder einer Netzwerkverbindung für einen bestimmten Vorgang abzurufen sind.

Einige Dateisysteme, wie z. b. NTFS, unterstützen verknüpfte Dateien und Verzeichnisse, die auch Datei Benennungs Konventionen und Regeln gemäß der normalen Datei oder des Verzeichnisses befolgen. Weitere Informationen finden Sie unter Feste [Links und Zusammenhänge](hard-links-and-junctions.md) und Analyse [Punkte und Datei Vorgänge](reparse-points-and-file-operations.md).

Weitere Informationen finden Sie in den folgenden Unterabschnitten:

-   [Datei-und Verzeichnisnamen](#file-and-directory-names)
    -   [Benennungs Konventionen](#naming-conventions)
    -   [Kurze und lange Namen](#short-vs-long-names)
-   [Paths](#fully-qualified-vs-relative-paths)
    -   [Voll qualifizierte und relative Pfade](#fully-qualified-vs-relative-paths)
    -   [Maximale Pfadlängen Beschränkung](#maximum-path-length-limitation)
-   [Namespaces](#win32-file-namespaces)
    -   [Win32-Dateinamespaces](#win32-file-namespaces)
    -   [Win32-Geräte Namespaces](#win32-device-namespaces)
    -   [NT-Namespaces](#nt-namespaces)
-   [Zugehörige Themen](#related-topics)


Weitere Informationen zum Konfigurieren von Windows 10 für die Unterstützung langer Dateipfade finden Sie unter [Einschränkung der maximalen Pfad Länge](./maximum-file-path-limitation.md).


## <a name="file-and-directory-names"></a>Datei-und Verzeichnisnamen

Alle Dateisysteme befolgen dieselben allgemeinen Benennungs Konventionen für eine einzelne Datei: einen Basis Dateinamen und eine optionale Erweiterung, die durch einen Punkt getrennt sind. Jedes Dateisystem, z. b. NTFS, CDFS, exFAT, UDFs, FAT und FAT32, kann jedoch über spezielle und abweichende Regeln bezüglich der Bildung der einzelnen Komponenten im Pfad zu einem Verzeichnis oder einer Datei verfügen. Beachten Sie, dass es sich bei einem *Verzeichnis* einfach um eine Datei mit einem speziellen Attribut handelt, das als Verzeichnis festgelegt wird. andernfalls müssen die gleichen Benennungs Regeln wie eine reguläre Datei befolgt werden. Da der Begriff " *Verzeichnis* " einfach auf einen speziellen Dateityp verweist, soweit es sich um das Dateisystem handelt, wird in einigen Referenzmaterialien die allgemeine Begriffs *Datei* verwendet, um beide Konzepte von Verzeichnissen und Datendateien als solche abzudecken. Wenn nichts anderes angegeben ist, sollten alle Benennungs-oder Verwendungs Regeln oder Beispiele für eine Datei auch für ein Verzeichnis gelten. Der Begriff *Pfad* verweist auf ein oder mehrere Verzeichnisse, umgekehrte Schrägstriche und möglicherweise auf einen Volumenamen. Weitere Informationen finden Sie im Abschnitt [Pfade](#fully-qualified-vs-relative-paths) .

Die Beschränkungen der Zeichen Anzahl können sich auch unterscheiden und können abhängig vom verwendeten Dateisystem-und Pfadnamen-Präfix Format variieren. Dies wird durch die Unterstützung von abwärts Kompatibilitäts Mechanismen weiter erschwert. Beispielsweise unterstützt das ältere DOS-FAT-Dateisystem maximal 8 Zeichen für den Basis Dateinamen und 3 Zeichen für die Erweiterung. Dies umfasst insgesamt 12 Zeichen, einschließlich des Punkt Trennzeichens. Dies wird in der Regel als *8,3-Dateiname* bezeichnet. Die Windows FAT-und NTFS-Dateisysteme sind nicht auf 8,3-Dateinamen beschränkt, da Sie *lange Dateinamen unterstützen*, aber dennoch die 8,3-Version von langen Dateinamen unterstützen.

### <a name="naming-conventions"></a>Namenskonventionen

Die folgenden grundlegenden Regeln ermöglichen es Anwendungen, gültige Namen für Dateien und Verzeichnisse unabhängig vom Dateisystem zu erstellen und zu verarbeiten:

-   Verwenden Sie einen Punkt, um den Basis Dateinamen von der Erweiterung im Namen eines Verzeichnisses oder einer Datei zu trennen.
-   Verwenden Sie einen umgekehrten Schrägstrich ( \\ ), um die *Komponenten* eines *Pfades* voneinander zu trennen. Durch den umgekehrten Schrägstrich wird der Dateiname aus dem Pfad zu ihm und ein Verzeichnisname aus einem anderen Verzeichnisnamen in einem Pfad unterteilt. Sie können keinen umgekehrten Schrägstrich im Namen für die tatsächliche Datei oder das tatsächliche Verzeichnis verwenden, da es sich um ein reserviertes Zeichen handelt, das die Namen in Komponenten trennt.
-   Verwenden Sie einen umgekehrten Schrägstrich, der als Teil der [Volumenamen](naming-a-volume.md)erforderlich ist, z. b. "c: \\ " in "c: \\ path- \\ Datei" oder " \\ \\ Server \\ Freigabe" in " \\ \\ Server \\ Freigabe \\ Pfad- \\ Datei" für Universal Naming Convention (UNC)-Namen. Weitere Informationen zu UNC-Namen finden Sie im Abschnitt [Beschränkung der maximalen Pfad Länge](#maximum-path-length-limitation) .
-   Beachten Sie nicht die Groß-/Kleinschreibung. Nehmen Sie beispielsweise an, dass die Namen "Oscar", "Oscar" und "Oscar" identisch sind, auch wenn einige Dateisysteme (z. b. ein POSIX-kompatibles Dateisystem) Sie als unterschiedlich betrachtet werden können. Beachten Sie, dass NTFS POSIX-Semantik für die Groß-/Kleinschreibung unterstützt, jedoch nicht das Standardverhalten. Weitere Informationen finden Sie unter " [**kreatefile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea)".
-   Bei volumebezeichnern (Laufwerk Buchstaben) wird die Groß-/Kleinschreibung nicht beachtet. Beispielsweise verweisen "d: \\ " und "d: \\ " auf dasselbe Volume.
-   Verwenden Sie ein beliebiges Zeichen in der aktuellen Codepage für einen Namen, einschließlich Unicode-Zeichen und Zeichen im erweiterten Zeichensatz (128 – 255), mit Ausnahme der folgenden:

    -   Die folgenden reservierten Zeichen:

        -   < (kleiner als)
        -   \> (größer als)
        -   : (Doppelpunkt)
        -   " (doppeltes Anführungszeichen)
        -   / (Schrägstrich)
        -   \\ umgekehrten Schrägstrich
        -   \| (senkrechter Strich oder Pipe)
        -   ? (Fragezeichen)
        -   \* (Sternchen)

    -   Ganzzahliger Wert 0 (manchmal auch als ASCII- *NUL* -Zeichen bezeichnet).
    -   Zeichen, deren ganzzahlige Darstellungen zwischen 1 und 31 liegen, mit Ausnahme alternativer Datenströme, in denen diese Zeichen zulässig sind. Weitere Informationen zu Dateistreams finden Sie unter [Dateistreams](file-streams.md).
    -   Alle anderen Zeichen, die das Ziel Dateisystem nicht zulässt.

-   Verwenden Sie einen Zeitraum als Verzeichnis *Komponente* in einem Pfad, der das aktuelle Verzeichnis darstellt, z. b. ". \\temp.txt ". Weitere Informationen finden Sie unter [Pfade](#fully-qualified-vs-relative-paths).
-   Verwenden Sie zwei aufeinander folgende Punkte (..) als Verzeichnis Komponente in einem Pfad, um das übergeordnete *Element* des aktuellen Verzeichnisses darzustellen, z. b. ".. \\temp.txt ". Weitere Informationen finden Sie unter [Pfade](#fully-qualified-vs-relative-paths).
-   Verwenden Sie für den Namen einer Datei nicht die folgenden reservierten Namen:

    CON, PRN, AUX, NUL, COM1, COM2, COM3, COM4, COM5, COM6, COM7, COM8, COM9, LPT1, LPT2, LPT3, LPT4, LPT5, LPT6, LPT7, LPT8, LPT9,,,, und. Vermeiden Sie auch diese Namen, gefolgt von einer Erweiterung. Beispielsweise ist NUL.txt nicht empfehlenswert. Weitere Informationen finden Sie unter [Namespaces](#win32-file-namespaces).

-   Beenden Sie den Datei-oder Verzeichnisnamen nicht mit einem Leerzeichen oder einem bestimmten Zeitraum. Obwohl das zugrunde liegende Dateisystem solche Namen unterstützt, wird die Windows-Shell und die Benutzeroberfläche nicht unterstützt. Es ist jedoch zulässig, einen Zeitraum als erstes Zeichen eines Namens anzugeben. Beispiel: ". Temp".

### <a name="short-vs-long-names"></a>Kurze und lange Namen

Ein langer Dateiname wird als beliebiger Dateiname betrachtet, der den kurzen MS-DOS-Benennungs Konventionen (auch als *8,3* bezeichnet) überschreitet. Wenn Sie einen langen Dateinamen erstellen, erstellt Windows möglicherweise auch eine kurze 8,3-Form des Namens, die als *8,3-Alias* oder Kurzname bezeichnet wird, und speichert Sie auch auf dem Datenträger. Dieses 8,3-Aliasing kann abhängig vom jeweiligen Dateisystem aus Leistungsgründen entweder systemweit oder für ein bestimmtes Volume deaktiviert werden.

**Windows Server 2008, Windows Vista, Windows Server 2003 und Windows XP:** 8,3 Aliasing kann für angegebene Volumes erst ab Windows 7 und Windows Server 2008 R2 deaktiviert werden.

In vielen Dateisystemen enthält ein Dateiname eine Tilde (~) in jeder Komponente des Namens, die zu lang ist, um 8,3-Benennungs Regeln einzuhalten.

> [!Note]  
> Nicht alle Dateisysteme Folgen der Tilde-Ersetzungs Konvention, und Systeme können so konfiguriert werden, dass die 8,3-Alias Generierung deaktiviert wird, auch wenn Sie normalerweise unterstützt wird. Nehmen Sie daher nicht die Annahme, dass der 8,3-Alias bereits auf dem Datenträger vorhanden ist.

 

Beachten Sie die folgenden Optionen, um 8,3-Dateinamen, lange Dateinamen oder den vollständigen Pfad einer Datei vom System anzufordern:

-   Um die 8,3-Form eines langen Datei namens zu erhalten, verwenden Sie die [**GetShortPathName**](/windows/desktop/api/FileAPI/nf-fileapi-getshortpathnamew) -Funktion.
-   Um die lange Dateinamen Version eines Kurznamens zu erhalten, verwenden Sie die [**GetLongPathName**](/windows/desktop/api/FileAPI/nf-fileapi-getlongpathnamea) -Funktion.
-   Verwenden Sie die Funktion [**getfullpathname**](/windows/desktop/api/FileAPI/nf-fileapi-getfullpathnamea) , um den vollständigen Pfad zu einer Datei zu erhalten.

Auf neueren Dateisystemen wie NTFS, exFAT, UDFs und FAT32 speichert Windows die langen Dateinamen auf einem Datenträger in Unicode. Dies bedeutet, dass der ursprüngliche lange Dateiname immer beibehalten wird. Dies gilt auch dann, wenn ein langer Dateiname erweiterte Zeichen enthält, unabhängig von der Codepage, die während eines Lese-oder Schreibvorgangs für einen Datenträger aktiv ist.

Dateien, die lange Dateinamen verwenden, können zwischen den NTFS-Dateisystem Partitionen und Windows FAT-Dateisystem Partitionen kopiert werden, ohne dass die Dateinamen Informationen verloren gehen. Dies gilt möglicherweise nicht für das ältere DOS-FAT und einige Arten von CDFS-Dateisystemen (CD-ROM), abhängig vom tatsächlichen Dateinamen. In diesem Fall wird nach Möglichkeit der kurze Dateiname ersetzt.

## <a name="paths"></a>Paths

Der *Pfad* zu einer angegebenen Datei besteht aus einer oder mehreren *Komponenten*, die durch ein Sonderzeichen (einen umgekehrten Schrägstrich) getrennt sind, wobei jede Komponente in der Regel ein Verzeichnisname oder Dateiname ist, jedoch mit einigen bedeutenden Ausnahmen, die im folgenden erläutert werden. Es ist oftmals wichtig, dass die Interpretation eines Pfads für den Anfang oder das *Präfix* des Pfads aussieht. Dieses Präfix bestimmt den *Namespace* , den der Pfad verwendet, und zusätzlich die Sonderzeichen, die an der Position innerhalb des Pfads verwendet werden, einschließlich des letzten Zeichens.

Wenn eine Komponente eines Pfades ein Dateiname ist, muss es sich um die letzte Komponente handeln.

Jede Komponente eines Pfads wird auch durch die maximale Länge beschränkt, die für ein bestimmtes Dateisystem angegeben wird. Im Allgemeinen werden diese Regeln in zwei Kategorien unterteilt: *Short* und *Long*. Beachten Sie, dass Verzeichnisnamen vom Dateisystem als spezieller Dateityp gespeichert werden, aber Benennungs Regeln für Dateien auch für Verzeichnisnamen gelten. Zusammenfassend gesagt: ein Pfad ist einfach die Zeichen folgen Darstellung der Hierarchie zwischen allen Verzeichnissen, die für einen bestimmten Datei-oder Verzeichnisnamen vorhanden sind.

### <a name="fully-qualified-vs-relative-paths"></a>Voll qualifizierte und relative Pfade

Für Windows-API-Funktionen, die Dateien bearbeiten, können Dateinamen häufig relativ zum aktuellen Verzeichnis sein, während für einige APIs ein voll qualifizierter Pfad erforderlich ist. Ein Dateiname ist relativ zum aktuellen Verzeichnis, wenn er nicht mit einem der folgenden Schritte beginnt:

-   Ein UNC-Name eines beliebigen Formats, das immer mit zwei umgekehrten Schrägstrichen (" \\ \\ ") beginnt. Weitere Informationen finden Sie im nächsten Abschnitt.
-   Ein Datenträger Kenn Zeichner mit einem umgekehrten Schrägstrich, z. b. "C: \\ " oder "d: \\ ".
-   Ein einzelner umgekehrter Schrägstrich, z \\ . b. "Directory" oder " \\file.txt". Dies wird auch als *absoluter Pfad* bezeichnet.

Wenn ein Dateiname nur mit einem Datenträger Kenn Zeichner, aber nicht mit dem umgekehrten Schrägstrich hinter dem Doppelpunkt beginnt, wird er als relativer Pfad zum aktuellen Verzeichnis auf dem Laufwerk mit dem angegebenen Buchstaben interpretiert. Beachten Sie, dass das aktuelle Verzeichnis möglicherweise das Stammverzeichnis ist oder nicht das Stammverzeichnis ist, je nachdem, was während des letzten "Change Directory"-Vorgangs auf diesem Datenträger festgelegt wurde. Beispiele für dieses Format:

-   "C:tmp.txt" verweist auf eine Datei mit dem Namen "tmp.txt" im aktuellen Verzeichnis auf Laufwerk C.
-   "C:TEMPDIR \\tmp.txt" verweist auf eine Datei in einem Unterverzeichnis auf das aktuelle Verzeichnis auf Laufwerk C.

Ein Pfad wird auch als relativ bezeichnet, wenn er "Doppelte Punkte" enthält; Das heißt, zwei Zeiträume in einer Komponente des Pfads. Dieser spezielle Spezifizierer wird verwendet, um das Verzeichnis oberhalb des aktuellen Verzeichnisses anzugeben, das auch als "übergeordnetes Verzeichnis" bezeichnet wird. Beispiele für dieses Format:

-   "..\\tmp.txt "gibt eine Datei mit dem Namen tmp.txt an, die sich im übergeordneten Element des aktuellen Verzeichnisses befindet.
-   "..\\..\\tmp.txt "gibt eine Datei an, die zwei Verzeichnisse oberhalb des aktuellen Verzeichnisses ist.
-   "..\\ TEMPDIR ( \\tmp.txt "gibt eine Datei mit dem Namen tmp.txt an, die sich in einem Verzeichnis namens TEMPDIR (befindet, das ein Peer Verzeichnis für das aktuelle Verzeichnis ist.

Relative Pfade können beide Beispiel Typen kombinieren, z. b. "c:.. \\tmp.txt ". Dies ist hilfreich, da das System zwar das aktuelle Laufwerk mit dem aktuellen Verzeichnis dieses Laufwerks nachverfolgt, aber auch die aktuellen Verzeichnisse in den einzelnen Laufwerk Buchstaben nachverfolgt (wenn Ihr System mehr als eins hat), unabhängig davon, welcher Laufwerks Kenn Zeichner als Aktuelles Laufwerk festgelegt ist.

### <a name="maximum-path-length-limitation"></a>Maximale Pfadlängen Beschränkung


In Editionen von Windows vor Windows 10, Version 1607, ist die maximale Länge für einen Pfad **Max \_ path**, der als 260 Zeichen definiert ist. In neueren Versionen von Windows ist das Ändern eines Registrierungsschlüssels oder des Gruppenrichtlinie Tools erforderlich, um das Limit zu entfernen. Ausführliche Informationen finden Sie unter [Maximale Pfadlängen Beschränkung](./maximum-file-path-limitation.md) .


## <a name="namespaces"></a>Namespaces

Es gibt zwei Hauptkategorien von Namespace Konventionen, die in den Windows-APIs verwendet werden, die häufig als *NT-Namespaces* und *Win32-Namespaces* bezeichnet werden. Der NT-Namespace wurde als Namespace der untersten Ebene entworfen, auf dem andere Subsysteme und Namespaces vorhanden sein können, einschließlich des Win32-Subsysteme und der Win32-Namespaces. POSIX ist ein weiteres Beispiel für ein Subsystem in Windows, das auf dem NT-Namespace aufbaut. In früheren Versionen von Windows wurden außerdem einige vordefinierte oder reservierte Namen für bestimmte Geräte definiert, wie z. b. Kommunikationsports (serielle und parallele Ports) und die Standard Anzeige Konsole als Teil des Namens NT-Geräte Namespace, und werden in aktuellen Versionen von Windows aus Gründen der Abwärtskompatibilität weiterhin unterstützt.

### <a name="win32-file-namespaces"></a>Win32-Dateinamespaces

Die Präfixen und Konventionen für den Win32-Namespace werden in diesem Abschnitt und im folgenden Abschnitt mit Beschreibungen der Verwendungsweise zusammengefasst. Beachten Sie, dass diese Beispiele für die Verwendung mit den Funktionen der Windows-API gedacht sind und nicht alle mit Windows Shell-Anwendungen wie Windows Explorer funktionieren. Aus diesem Grund gibt es eine größere Bandbreite an möglichen Pfaden, als normalerweise in Windows Shell-Anwendungen verfügbar sind, und Windows-Anwendungen, die diese Vorteile nutzen, können mit diesen Namespace Konventionen entwickelt werden.

Bei Datei-e/ \\ \\ \\ a weist das Präfix "?" einer Pfad Zeichenfolge den Windows-APIs an, die gesamte Zeichen folgen Verarbeitung zu deaktivieren und die Zeichenfolge direkt an das Dateisystem zu senden. Wenn das Dateisystem z. b. große Pfade und Dateinamen unterstützt, können Sie die **maximalen \_ Pfad** Limits überschreiten, die andernfalls von den Windows-APIs erzwungen werden. Weitere Informationen zur normalen maximalen Pfad Beschränkung finden Sie im vorherigen Abschnitt [Maximale Pfadlängen Beschränkung](#maximum-path-length-limitation).

Da die automatische Erweiterung der Pfad Zeichenfolge deaktiviert wird, \\ \\ lässt das \\ Präfix "?" auch die Verwendung von ".." und "." in den Pfadnamen zu. Dies kann hilfreich sein, wenn Sie versuchen, Vorgänge für eine Datei auszuführen, die diese anderweitig reservierten relativen pfadspezifiziererer als Teil des voll qualifizierten Pfads verwenden.

Viele, aber nicht alle Datei-e/a-APIs unterstützen " \\ \\ ? \\ ". Sie sollten sich das Referenz Thema für jede API ansehen, um sicher zu sein. 

Beachten Sie, dass Unicode-APIs verwendet werden sollten, um sicherzustellen, dass das \\ \\ \\ Präfix "?" den **maximalen \_ Pfad** überschreiten kann. 

### <a name="win32-device-namespaces"></a>Win32-Geräte Namespaces

Mit dem \\ \\ \\ Präfix "." wird anstelle des Win32-Datei Namespace auf den Win32-Geräte Namespace zugegriffen. Auf diese Weise wird der Zugriff auf physische Datenträger und Volumes direkt erreicht, ohne das Dateisystem durchlaufen zu müssen, wenn die API diese Art von Zugriff unterstützt. Sie können auf viele andere Geräte als Datenträger auf diese Weise zugreifen (z. b. mithilfe der Funktionen " [**fiatefile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) " und " [**definedosdevice**](/windows/desktop/api/FileAPI/nf-fileapi-definedosdevicew) ").

Wenn Sie z. b. den Port 1 der seriellen Kommunikation des Systems öffnen möchten, können Sie "COM1" im Aufrufen der Funktion " [**deatefile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) " verwenden. Dies funktioniert, weil COM1 – COM9 Teil der reservierten Namen im NT-Namespace ist, obwohl die Verwendung des \\ \\ \\ Präfix "." auch mit diesen Gerätenamen funktioniert. Wenn Sie einen 100-Port für eine serielle Erweiterungs Platine installiert haben und COM56 öffnen möchten, können Sie ihn im Vergleich nicht mit "COM56" öffnen, da es keinen vordefinierten NT-Namespace für COM56 gibt. Sie müssen es mit "Öffnen \\ \\ . \\ COM56 ", weil" \\ \\ . \\ "direkt in den Geräte Namespace wechselt, ohne zu versuchen, einen vordefinierten Alias zu suchen.

Ein weiteres Beispiel für die [**Verwendung des Win32**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) -Geräte Namespace ist die Verwendung der Funktion "-Funktion" mit " \\ \\ . \\ PhysicalDisk *X*"(wobei *x* ein gültiger ganzzahliger Wert ist) oder" \\ \\ . \\ Cdrom *X*". Dies ermöglicht es Ihnen, direkt auf diese Geräte zuzugreifen und das Dateisystem zu umgehen. Dies funktioniert, weil diese Gerätenamen vom System erstellt werden, während diese Geräte aufgelistet werden, und einige Treiber auch andere Aliase im System erstellen. Beispielsweise verfügt der Gerätetreiber, der den Namen "C: \\ " implementiert, über einen eigenen Namespace, der auch das Dateisystem ist.

APIs, [**die die Funktion**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) "." durchlaufen, funktionieren in der Regel mit dem \\ \\ Präfix ".", da "" als \\ Funktion zum Öffnen von Dateien und Geräten verwendet **wird** . Dies hängt von den Parametern ab, die Sie verwenden.

Wenn Sie mit Windows-API-Funktionen arbeiten, sollten Sie das \\ \\ Präfix "." verwenden, \\ um nur auf Geräte und nicht auf Dateien zuzugreifen.

Die meisten APIs unterstützen " \\ \\ ." nicht. \\ nur die APIs, die für die Arbeit mit dem Geräte Namespace entworfen wurden, werden Sie erkennen. Überprüfen Sie immer das Referenz Thema für jede API, um sicher zu sein.

### <a name="nt-namespaces"></a>NT-Namespaces

Es gibt auch APIs, die die Verwendung der NT-Namespace Konvention ermöglichen, aber der Windows-Objekt-Manager macht dies in den meisten Fällen unnötig. Um dies zu veranschaulichen, ist es hilfreich, die Windows-Namespaces im Systemobjekt Katalog mithilfe des Windows Sysinternals [WinObj](/sysinternals/downloads/winobj) -Tools zu durchsuchen. Wenn Sie dieses Tool ausführen, sehen Sie, dass der NT-Namespace beginnend mit dem Stammverzeichnis oder "" angezeigt wird \\ . Der Unterordner mit dem Namen "Global?" Gibt an, wo sich der Win32-Namespace befindet. Benannte Geräte Objekte befinden sich im NT-Namespace innerhalb des Unterverzeichnisses "Device". Hier finden Sie möglicherweise auch serial0 und Serial1, die Geräte Objekte, die die ersten beiden com-Ports darstellen, wenn Sie auf Ihrem System vorhanden sind. Ein Geräte Objekt, das ein Volume darstellt, wäre etwa "HarddiskVolume1", obwohl das numerische Suffix variieren kann. Der Name "DR0" im Unterverzeichnis "Harddisk0" ist ein Beispiel für das Geräte Objekt, das einen Datenträger darstellt, usw.

Um diese Geräte Objekte für Windows-Anwendungen zugänglich zu machen, erstellen die Gerätetreiber einen symbolischen Link (symlink) im Win32-Namespace ("Global??") zu den jeweiligen Geräte Objekten. Beispielsweise COM0 und COM1 unter dem "Global??" Unterverzeichnis sind einfach Symlinks zu serial0 und Serial1, "C:" ist ein symlink zu HarddiskVolume1, "Physicaldrive0" ist ein symlink zu DR0 usw. Ohne Symlink ist das angegebene Gerät "xxx" für keine Windows-Anwendung verfügbar, die Win32-Namespace Konventionen verwendet, wie zuvor beschrieben. Allerdings kann ein Handle für dieses Gerät mithilfe von APIs geöffnet werden, die den absoluten Pfad des NT-Namespace im Format " \\ Gerät \\ xxx" unterstützen.

Durch das Hinzufügen von Unterstützung für mehrere Benutzer über terminaldienstedienste und virtuelle Computer ist die Virtualisierung des systemweiten Stamm Geräts im Win32-Namespace noch weiter erforderlich. Dies wurde erreicht, indem der Symlink mit dem Namen "globalroot" dem Win32-Namespace hinzugefügt wurde, den Sie im "Global?" anzeigen können. das Unterverzeichnis des zuvor beschriebenen WinObj-Browser Tools, auf das über den Pfad \\ \\ \\ zugegriffen werden kann. Globalroot ". Dieses Präfix stellt sicher, dass der folgende Pfad den wahren Stammpfad des Systemobjekt-Managers und keinen Sitzungs abhängigen Pfad untersucht.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Vergleich der Datei System Funktionen](filesystem-functionality-comparison.md)
</dt> </dl>

 

 