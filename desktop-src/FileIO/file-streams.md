---
description: Im NTFS-Dateisystem enthalten Streams die Daten, die in eine Datei geschrieben werden, und die mehr Informationen über eine Datei als Attribute und Eigenschaften enthält.
ms.assetid: 41dda6f1-a6d1-4e76-94f3-a72f9e491bee
title: Datei Datenströme (lokale Dateisysteme)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a934a51225a886e3d5a7de4d9e1e91900fab460
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103755161"
---
# <a name="file-streams-local-file-systems"></a>Datei Datenströme (lokale Dateisysteme)

Ein Datenstrom ist eine Bytefolge. Im NTFS-Dateisystem enthalten Streams die Daten, die in eine Datei geschrieben werden, und die mehr Informationen über eine Datei als Attribute und Eigenschaften enthält. Beispielsweise können Sie einen Stream erstellen, der Such Schlüsselwörter enthält, oder die Identität des Benutzerkontos, mit dem eine Datei erstellt wird.

Jeder Datenstrom, der einer Datei zugeordnet ist, verfügt über eine eigene Zuordnungs Größe, tatsächliche Größe und gültige Daten Länge:

-   Bei der Zuordnungs Größe handelt es sich um die Menge an Speicherplatz, die für einen Datenstrom reserviert ist.
-   Die tatsächliche Größe ist die Anzahl der Bytes, die von einem Aufrufer verwendet werden.
-   Die gültige Daten Länge (VDL) ist die Anzahl der Bytes, die aus der Zuordnungs Größe für den Stream initialisiert werden.

Jeder Stream behält auch seinen eigenen Zustand für Komprimierung, Verschlüsselung und geringe Dichte. Das **file \_ Attribute \_ Sparse \_ File** -Attribut für die Datei wird im **dwfileattribute** -Member der [**Win32 \_ Find \_ Data**](/windows/desktop/api/MinWinBase/ns-minwinbase-win32_find_dataa) -Struktur festgelegt, die von der [**FindFirstFile**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfilea)-, der [**findfirstfileex**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfileexa)-Funktion und der [**FindNextFile**](/windows/desktop/api/FileAPI/nf-fileapi-findnextfilea) -Funktion zurückgegeben wird, wenn einer der Streams jemals eine geringe Dichte aufweist. " [**Getfileattribute**](/windows/desktop/api/FileAPI/nf-fileapi-getfileattributesa)", " [**getfileattributesex**](/windows/desktop/api/FileAPI/nf-fileapi-getfileattributesexa)", " [**getfileattributestransagiert**](/windows/desktop/api/WinBase/nf-winbase-getfileattributestransacteda)", " [**GetFileInformationByHandle**](/windows/desktop/api/FileAPI/nf-fileapi-getfileinformationbyhandle)" und " [**getfileinformationbylenker Ex**](/windows/desktop/api/WinBase/nf-winbase-getfileinformationbyhandleex) " geben den sparsezustand des standardmäßigen Datenstroms zurück, wenn kein Stream angegeben ist.

Einem Stream sind keine Datei Zeiten zugeordnet. Die Datei Zeiten für eine Datei werden aktualisiert, wenn ein beliebiger Stream in einer Datei aktualisiert wird.

Opportunistische Sperren werden pro Stream verwaltet. Freigabe Modi werden auch pro Stream verwaltet. Wenn für eine Datei der Lösch Zugriff angefordert wird, überprüft das Betriebssystem den Lösch Zugriff für alle geöffneten Streams in einer Datei. Wenn ein anderer Prozess einen Stream ohne die DELETE-Berechtigung der **Datei \_ Freigabe \_** geöffnet hat, können Sie die Datei für den Lösch Zugriff nicht öffnen.

Wenn eine zu kopierende Datei einen Datenstream aufweist und der Netzwerkredirector verwendet wird, kann die Datei nur kopiert werden, wenn der Client über die Berechtigung Lesen und die Berechtigung zum Lesen von Attributen verfügt.

## <a name="naming-conventions-for-streams"></a>Benennungs Konventionen für Streams

Wenn der vollständige Name eines Datenstroms in der Windows Shell-Befehlszeile angegeben ist, lautet der vollständige Name des Datenstroms "*filename*:*Stream Name*:*Stream Type*", wie im folgenden Beispiel gezeigt: "MyFile. dat: Stream1: $Data".

Alle Zeichen, die für einen Dateinamen zulässig sind, sind auch für den Datenstrom Namen zulässig, einschließlich Leerzeichen. Weitere Informationen finden Sie unter [Benennen einer Datei](naming-a-file.md). Der Streamtyp (auch als Attributtyp Code bezeichnet) ist für das NTFS-Dateisystem intern. Benutzer können daher keine neuen Streamtypen erstellen, aber Sie können vorhandene NTFS-Dateisystemtypen öffnen. Die Werte für den streamtypspezifizierer beginnen immer mit dem Dollarzeichen ($). Eine Liste der Streamtypen finden Sie unten.

Standardmäßig ist der Standarddaten Strom unbenannt. Um den standarddatenstream vollständig anzugeben, verwenden Sie "*filename*:: $Data", wobei $Data der Streamtyp ist. Dies entspricht "*filename*". Mithilfe der [Datei Benennungs Konventionen](naming-a-file.md)können Sie einen benannten Stream in der Datei erstellen. Beachten Sie, dass "$Data" ein gültiger Datenstrom Name ist. Beispielsweise wäre der vollständige Name eines Datenstroms mit dem Namen "$Data" in einer Datei namens "*Sample*" "*Sample*: $Data: $Data". Wenn Sie einen Stream mit dem Namen "Bar" in derselben Datei erstellt haben, lautet der vollständige Name "*Sample*: Bar: $Data".

Beim Erstellen und Verwenden von Dateien mit einem Zeichennamen wird dem Dateinamen ein Zeitraum vorangestellt, gefolgt von einem umgekehrten Schrägstrich (. \) oder verwenden Sie einen voll qualifizierten Pfadnamen. Der Grund hierfür ist, dass Windows Dateinamen mit einem Zeichen als Laufwerk Buchstaben behandelt. Wenn ein Laufwerk Buchstabe mit einem relativen Pfad angegeben ist, wird der Laufwerk Buchstabe vom Pfad getrennt. Wenn es Mehrdeutigkeiten gibt, ob ein Zeichen Name ein Laufwerk Buchstabe oder ein Dateiname ist, geht Windows davon aus, dass es sich um einen Laufwerk Buchstaben handelt, wenn die Zeichenfolge, die auf den Doppelpunkt folgt, ein gültiger Pfad ist, auch wenn der Laufwerk Buchstabe ungültig ist.

## <a name="stream-types"></a>Streamtypen

Im folgenden finden Sie die Liste der NTFS-Streamtypen, die auch als Attributtyp Codes bezeichnet werden. Einige der Streamtypen sind intern für NTFS und deren Format nicht dokumentiert.



| Streamtyp                | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|----------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| :: $Attribute \_ Liste         | Enthält eine Liste aller Attribute, aus denen die Datei besteht, und gibt an, wo sich die einzelnen Attribute befinden.                                                                                                                                                                                                                                                                                                                                          |
| :: $Bitmap                  | Eine Bitmap, die von Indizes verwendet wird, um den freien b-Struktur-Speicherplatz für ein Verzeichnis zu verwalten. Die b-Struktur wird in Blöcken von 4 KB (unabhängig von der Clustergröße) verwaltet und wird verwendet, um die Zuordnung dieser Blöcke zu verwalten. Dieser Streamtyp ist in jedem Verzeichnis vorhanden.                                                                                                                                                                                           |
| :: $Data                    | Datenstrom. Der Standarddaten Strom hat keinen Namen. Datenströme können mithilfe der Funktionen [**findfirststreamw**](/windows/desktop/api/fileapi/nf-fileapi-findfirststreamw) und [**findnextstreamw**](/windows/desktop/api/fileapi/nf-fileapi-findnextstreamw) aufgelistet werden.                                                                                                                                                                                                                                                |
| :: $EA                      | Enthält Daten zu erweiterten Attributen.|
| :: $EA \_ Informationen         | Enthält Support Informationen zu den erweiterten Attributen.                                                                                                                                                                                                                                                                                                                                                                                      |
| :: $file \_ Name              | Der Name der Datei in Unicode-Zeichen. Dies schließt den Kurznamen der Datei sowie alle fest Verknüpfungen ein.                                                                                                                                                                                                                                                                                                                                 |
| :: $Index \_ Zuordnung       | Der Streamtyp eines Verzeichnisses. Wird verwendet, um die Dateinamen Zuordnung für große Verzeichnisse zu implementieren. Dieser Stream stellt das Verzeichnis selbst dar und enthält alle Daten des Verzeichnisses. Änderungen an Streams dieses Typs werden im NTFS-Änderungs Journal protokolliert. Der Standarddaten Strom Name eines $Index \_ Zuordnungs Datenstrom Typs ist $I 30, sodass "*dirname*", "*dirname*:: $Index \_ Allocation" und "*dirname*: $I 30: $Index \_ Allocation" gleich sind. |
| : \_ : $Index Stamm             | Dieser Stream stellt den Stamm der b-Struktur eines Indexes dar. Dieser Streamtyp ist in jedem Verzeichnis vorhanden.                                                                                                                                                                                                                                                                                                                                           |
| :: $Logged \_ Utility- \_ Stream | Ähnlich wie:: $Data, aber Vorgänge werden im NTFS-Änderungs Journal protokolliert. Wird von EFS und [transaktionalem NTFS (TxF)](transactional-ntfs-portal.md)verwendet. Das Paar ":*streamName*: $*Streamtype*" für EFS ist ": $EFS: $Logged \_ Utility \_ Stream", und für TxF ist ": $TxF \_ Data: $Logged \_ Utility \_ Stream".                                                                                                                                                    |
| :: $Object- \_ ID              | Eine 16-Byte-ID, die verwendet wird, um die Datei für den Link Überwachungsdienst zu identifizieren.                                                                                                                                                                                                                                                                                                                                                                           |
| :: $REPARSE \_ Punkt          | Die Daten des Analyse [Punkts](reparse-points.md) .|



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden von Streams](using-streams.md)
</dt> </dl>

 

 



