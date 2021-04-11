---
description: Beschreibt Überlegungen zur Anwendungssteuerung der Datei Pufferung, auch bekannt als nicht gepufferte Dateieingabe/-Ausgabe (e/a).
ms.assetid: ae1e5d0f-9b55-4aae-8402-b9c8e33d9363
title: Dateipufferung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a44f6724622b2c3116fa24a6109efb6c0d9f1d9f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218014"
---
# <a name="file-buffering"></a>Dateipufferung

In diesem Thema werden die verschiedenen Überlegungen zur Anwendungssteuerung der Datei Pufferung behandelt, auch bekannt als nicht gepufferte Dateieingabe/-Ausgabe (e/a). Die Datei Pufferung wird in der Regel vom System im Hintergrund verarbeitet und als Teil der Zwischenspeicherung von [Dateien](file-caching.md) innerhalb des Windows-Betriebssystems betrachtet, sofern nicht anders angegeben. Obwohl *die Begriffe zwischen* Speicherung und *Pufferung* manchmal synonym verwendet werden, wird in diesem Thema der Begriff *Pufferung* speziell in dem Kontext erläutert, in dem erläutert wird, wie mit Daten interagiert wird, die nicht vom System zwischengespeichert (gepuffert) werden, da Sie ansonsten größtenteils nicht direkt von der direkten Steuerung der Benutzermodusanwendungen betroffen sind.

Beim Öffnen oder Erstellen einer Datei mit der [**Funktion "**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) -Funktion" kann **das \_ Dateiflag " \_ kein \_ pufferungsflag** " angegeben werden, um das Zwischenspeichern von Daten, die aus der Datei gelesen oder in die Datei geschrieben werden, zu deaktivieren. Obwohl dies eine umfassende und direkte Kontrolle über die Daten-e/a-Pufferung bietet, müssen im Fall von Dateien und ähnlichen Geräten Daten Ausrichtungs Anforderungen berücksichtigt werden.

> [!Note]  
> Diese Ausrichtungs Informationen gelten für e/a-Vorgänge auf Geräten wie Dateien, die Suchvorgänge unterstützen, und das Konzept von Datei Positions Zeigern (oder *Offsets*). Bei Geräten, die nicht suchen, z. b. Named Pipes oder Kommunikationsgeräte, ist für das Ausschalten der Pufferung möglicherweise keine bestimmte Ausrichtung erforderlich. Alle Einschränkungen oder Effizienz, die in diesem Fall durch die Ausrichtung erzielt werden können, sind von der zugrunde liegenden Technologie abhängig.

 

In einem einfachen Beispiel öffnet die Anwendung eine Datei für den Schreibzugriff mit dem **\_ Dateiflag \_ kein \_ pufferungsflag** und führt dann einen Aufrufen der Funktion "Write [**File**](/windows/desktop/api/FileAPI/nf-fileapi-writefile) " mithilfe eines Daten Puffers aus, der in der Anwendung definiert ist. Dieser lokale Puffer ist in diesen Fällen tatsächlich der einzige Datei Puffer, der für diesen Vorgang vorhanden ist. Aufgrund des physischen Datenträger Layouts, des Dateisystem-Speicher Layouts und der Dateizeiger-Positions Nachverfolgung auf Systemebene schlägt dieser Schreibvorgang fehl, es sei denn, die lokal definierten Datenpuffer erfüllen bestimmte Ausrichtungs Kriterien, die im folgenden Abschnitt erläutert werden.

> [!Note]  
> Bei der Erörterung der Zwischenspeicherung wird das Zwischenspeichern von Hardware auf dem physischen Datenträger selbst nicht berücksichtigt, da es in jedem Fall nicht unbedingt innerhalb der direkten Kontrolle des Systems ist. Dies hat keine Auswirkung auf die in diesem Thema angegebenen Anforderungen.

 

Weitere Informationen darüber, wie **das \_ Dateiflag \_ keine \_ Pufferung** mit anderen Cache bezogenen Flags interagiert, finden Sie unter " [**kreatefile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea)".

## <a name="alignment-and-file-access-requirements"></a>Anforderungen an Ausrichtung und Dateizugriff

Wie bereits erwähnt, muss eine Anwendung bestimmte Anforderungen erfüllen, wenn Sie mit Dateien arbeiten, die mit dem **\_ Dateiflag \_ keine \_ Pufferung** geöffnet wurden. Es gelten die folgenden Besonderheiten:

-   Datei zugriffsgrößen, einschließlich des optionalen Dateioffsets in der [**über**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) Lapp enden Struktur, müssen für eine Anzahl von Bytes sein, bei der es sich um ein ganzzahliges Vielfaches der volumesektorgröße handelt. Wenn die Sektorgröße z. b. 512 Bytes beträgt, kann eine Anwendung Lese-und Schreibvorgänge von 512, 1.024, 1.536 oder 2.048 bytes, jedoch nicht von 335, 981 oder 7.171 bytes anfordern.
-   Datei Zugriffs Puffer-Adressen für Lese-und Schreibvorgänge sollten physisch sektororientiert sein, was bedeutet, dass Adressen im Arbeitsspeicher ausgerichtet sind, bei denen es sich um ganzzahlige Vielfache der physischen Sektorgröße des Volumes handelt. Abhängig vom Datenträger wird diese Anforderung möglicherweise nicht erzwungen.

Anwendungsentwickler sollten die neuen Typen von Speichergeräten notieren, die auf dem Markt mit einer physischen Medien Sektorgröße von 4.096 Bytes eingeführt werden. Der Branchen Name für diese Geräte ist "Erweitertes Format". Da es möglicherweise Kompatibilitätsprobleme bei der direkten Einführung von 4.096 Bytes als Einheit der Adressierung für das Medium gibt, besteht eine temporäre Kompatibilitäts Lösung darin, Geräte einzuführen, die ein reguläres 512-Byte-sektorspeichergerät emulieren, aber über standardmäßige ATA-und SCSI-Befehle Informationen über die tatsächliche Sektorgröße bereitstellen.

Aufgrund dieser Emulation gibt es im Wesentlichen zwei Sektorgrößen, die Entwickler verstehen müssen:

-   Logischer Sektor: die Einheit, die für die logische Block Adressierung für das Medium verwendet wird. Wir können uns dies auch als kleinste Schreibeinheit vorstellen, die der Speicher annehmen kann. Dies ist die "Emulation".
-   Physischer Sektor: die Einheit, für die Lese-und Schreibvorgänge auf dem Gerät in einem einzelnen Vorgang abgeschlossen werden. Dies ist die Einheit des atomaren Schreibzugriffs und die nicht gepufferte e/a, die für die optimale Leistung und Zuverlässigkeit von Merkmalen ausgerichtet werden muss.

Die meisten aktuellen Windows-APIs, wie z. b. [**IOCTL \_ Disk \_ get \_ Drive \_ Geometry**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_disk_get_drive_geometry) und [**GetDiskFreeSpace**](/windows/desktop/api/FileAPI/nf-fileapi-getdiskfreespacea), geben die logische Sektorgröße zurück, aber die physische Sektorgröße kann über den [**IOCTL \_ Storage \_ Query- \_ Eigenschafts**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_query_property) Steuerungs Code abgerufen werden, wobei die relevanten Informationen im **bytesperphysicalsektor-** Member in der-Struktur der [**Speicher \_ Zugriffs \_ Ausrichtung \_**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_access_alignment_descriptor) angezeigt werden. Ein Beispiel finden Sie im Beispielcode unter [**Speicher \_ Zugriffs- \_ Ausrichtungs \_ Deskriptor**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_access_alignment_descriptor). Microsoft empfiehlt dringend, dass Entwickler nicht gepufferte e/a-Vorgänge an die physische Sektorgröße ausrichten, wie vom Steuercode der **IOCTL \_ Storage \_ Query- \_ Eigenschaft** gemeldet, um sicherzustellen, dass Ihre Anwendungen für diesen Sektorgrößen Übergang vorbereitet werden.

**Windows Server 2003 und Windows XP:** Die [**\_ \_ \_ deskriptorstruktur der Speicherzugriffs Ausrichtung**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_access_alignment_descriptor) ist nicht verfügbar. Es wurde mit Windows Vista und Windows Server 2008 eingeführt.

Da Puffer Adressen für Lese-und Schreibvorgänge sektororientiert sein müssen, muss die Anwendung direkt steuern können, wie diese Puffer zugewiesen werden. Eine Möglichkeit, Puffer in Sektoren auszurichten, ist die Verwendung der [**VirtualAlloc**](/windows/desktop/api/memoryapi/nf-memoryapi-virtualalloc) -Funktion, um die Puffer zuzuordnen. Beachten Sie Folgendes:

-   [**Virtualbelegc**](/windows/desktop/api/memoryapi/nf-memoryapi-virtualalloc) ordnet Arbeitsspeicher zu, bei dem es sich um ganzzahlige Vielfache der Seitengröße des Systems handelt. Die Seitengröße beträgt 4.096 Bytes auf x64-und x86-oder 8.192-Bytes für Itanium-basierte Systeme. Weitere Informationen finden Sie unter der [**GetSystemInfo**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getsysteminfo) -Funktion.
-   Die Sektorgröße beträgt in der Regel 512 bis 4.096 Bytes für direkt Zugriff auf Speichergeräte (Festplatten) und 2.048 Bytes für CD-ROMs.
-   Sowohl die Seiten-als auch die Sektorgröße sind die Kräfte 2.

In den meisten Fällen wird der Seiten basierte Speicher auch sektororientiert, da der Fall, in dem die Sektorgröße größer ist als die Seitengröße, selten vorkommt.

Eine weitere Möglichkeit zum Abrufen von manuell ausgerichteten Speicher Puffern ist die Verwendung der [ \_ ausgerichteten \_ malloc](/cpp/c-runtime-library/reference/aligned-malloc?view=vs-2019) -Funktion aus der C-Run-Time-Bibliothek. Ein Beispiel für die manuelle Steuerung der Puffer Ausrichtung finden Sie im C++-Sprachcode Beispiel im Beispielcode Abschnitt von " [**Write File**](/windows/desktop/api/FileAPI/nf-fileapi-writefile)".

 

 
