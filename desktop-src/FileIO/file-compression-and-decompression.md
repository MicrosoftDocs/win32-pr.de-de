---
description: Das NTFS-Dateisystem verwendet Lempel-Ziv Komprimierung, bei der es sich um einen Verlust losen Komprimierungs Algorithmus handelt.
ms.assetid: 35a9fb47-5a73-479c-8fe0-5a2b07705536
title: Dateikomprimierung und-Dekomprimierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73d1aa9d8d3540eff85413c03358fd1ba7e21300
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106364225"
---
# <a name="file-compression-and-decompression"></a>Dateikomprimierung und-Dekomprimierung

Die NTFS-Dateisystemvolumes unterstützen die Dateikomprimierung auf einer einzelnen Datei Basis. Der vom NTFS-Dateisystem verwendete Datei Komprimierungs Algorithmus ist Lempel-Ziv Komprimierung. Dies ist ein *verlustfreier* Komprimierungs Algorithmus. Dies bedeutet, dass beim Komprimieren und Dekomprimieren der Datei keine Daten verloren gehen, und nicht im *Gegensatz zu* Verlusts-Komprimierungs Algorithmen wie JPEG, bei denen bei der Datenkomprimierung und-Dekomprimierung einige Daten verloren gehen.

Durch die Datenkomprimierung wird die Größe einer Datei reduziert, indem redundante Daten minimiert werden. In einer Textdatei können redundante Daten häufig vorkommen, z. b. das Leerzeichen oder allgemeine Vokale, wie z. b. Buchstaben e und a. Es kann sich auch um häufig auftretende Zeichen folgen handeln. Durch die Datenkomprimierung wird eine komprimierte Version einer Datei erstellt, indem diese redundante Daten minimiert werden.

Jeder Typ von Daten Komprimierungs Algorithmus minimiert redundante Daten auf eindeutige Weise. Der *Huffman-Codierungs Algorithmus* weist z. b. Zeichen in einer Datei anhand der Häufigkeit, mit der diese Zeichen auftreten, einen Code zu. Ein anderer Komprimierungs Algorithmus, der als *Lauflängen Codierung* bezeichnet wird, generiert einen zweiteiligen Wert für wiederholte Zeichen: der erste Teil gibt an, wie oft das Zeichen wiederholt wird, und der zweite Teil gibt das Zeichen an. Ein anderer Komprimierungs Algorithmus, der als *Lempel-Ziv-Algorithmus* bezeichnet wird, konvertiert Zeichen folgen variabler Länge in Codes mit fester Länge, die weniger Speicherplatz als die ursprünglichen Zeichen folgen verbrauchen.

## <a name="the-ntfs-file-system-file-compression"></a>Dateikomprimierung des NTFS-Dateisystems

Auf dem NTFS-Dateisystem wird die Komprimierung transparent ausgeführt. Dies bedeutet, dass Sie ohne Änderungen an vorhandenen Anwendungen verwendet werden kann. Die komprimierten Bytes der Datei sind für Anwendungen nicht zugänglich. Es werden nur die unkomprimierten Daten angezeigt. Daher können Anwendungen, die eine komprimierte Datei öffnen, so funktionieren, als wäre sie nicht komprimiert. Diese Dateien können jedoch nicht in ein anderes Dateisystem kopiert werden.

Wenn Sie eine Datei mit einer Größe von mehr als 30 Gigabyte komprimieren, wird die Komprimierung möglicherweise nicht erfolgreich ausgeführt.

In den folgenden Themen wird die Dateikomprimierung des NTFS-Dateisystems identifiziert:

-   [Komprimierungs Attribut](compression-attribute.md)
-   [Komprimierungs Status](compression-state.md)
-   [Abrufen der Größe einer komprimierten Datei](obtaining-the-size-of-a-compressed-file.md)

## <a name="file-compression-and-decompression-libraries"></a>Dateien zum Komprimieren und Dekomprimieren von Dateien

Die Dateien für die Dateikomprimierung und-Dekomprimierung nehmen eine vorhandene Datei oder Dateien an und erstellen eine Datei oder Dateien, die komprimierte Versionen der Originalversionen sind. Die Komprimierung ist ebenfalls verlustfrei, aber die Komprimierung ist für Anwendungen nicht transparent. Eine Anwendung kann nur für solche Dateien mit Unterstützung einer Datei Komprimierungs Bibliothek verwendet werden. Darüber hinaus können Sie für solche Dateien nur eine komprimierte Datei aus einem Original erstellen und die ursprünglichen Daten der dekomprimierten Version wiederherstellen. Die Bearbeitung wird in der Regel nicht unterstützt, und die Suche ist begrenzt, wenn Sie überhaupt unterstützt wird

In der Regel Ruft eine Anwendung Funktionen in Lz32.dll auf, um mit Compress.exe komprimierte Daten zu dekomprimieren. Die Funktionen können auch Dateien verarbeiten, ohne zu versuchen, Sie zu dekomprimieren.

Sie können die Funktionen in Lz32.dll verwenden, um einzelne oder mehrere Dateien zu dekomprimieren. Sie können Sie auch verwenden, um komprimierte Dateien zu einem Teil gleichzeitig zu dekomprimieren.

In den folgenden Themen wird die Datei Dekomprimierung identifiziert, die von den Funktionen in Lz32.dll bereitgestellt wird:

-   [Dekomprimieren einer einzelnen Datei](decompressing-a-single-file.md)
-   [Dekomprimieren mehrerer Dateien](decompressing-multiple-files.md)
-   [Lesen aus komprimierten Dateien](reading-from-compressed-files.md)

## <a name="cabinets"></a>Schrank

Schränke werden von einer Komprimierungs Bibliothek erstellt, die Funktionen wie die Datenträger Aufteilung und die Komprimierung mit mehreren Dateien unterstützt. Weitere Informationen finden Sie unter CAB Software Development Kit: [https://msdn.microsoft.com/library/dncabsdk/html/cabdl.asp](/previous-versions/ms974336(v=msdn.10)) .

## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                                                             | BESCHREIBUNG                                                                                                                              |
|---------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| [Komprimierungs Attribut](compression-attribute.md)<br/>                                     | Auf einem NTFS-Dateisystem Volume weist jede Datei und jedes Verzeichnis ein *Komprimierungs Attribut* auf.<br/>                                         |
| [Komprimierungs Status](compression-state.md)<br/>                                             | Jede Datei und jedes Verzeichnis auf einem Volume, das die Komprimierung für einzelne Dateien und Verzeichnisse unterstützt, hat einen *Komprimierungs Status*.<br/> |
| [Abrufen der Größe einer komprimierten Datei](obtaining-the-size-of-a-compressed-file.md)<br/> | Verwenden Sie die getcompressedfilesize-Funktion, um die komprimierte Größe einer Datei zu erhalten.<br/>                                               |
| [Dekomprimieren einer einzelnen Datei](decompressing-a-single-file.md)<br/>                         | Eine Anwendung kann eine einzelne komprimierte Datei dekomprimieren, indem Sie die lzopenfile-, lzcopy-und lzclose-Funktionen verwendet.<br/>                |
| [Dekomprimieren mehrerer Dateien](decompressing-multiple-files.md)<br/>                       | Eine Anwendung kann mehrere Dateien mithilfe der Funktionen lzopenfile, lzcopy und lzclose dekomprimieren.<br/>                          |
| [Lesen aus komprimierten Dateien](reading-from-compressed-files.md)<br/>                     | Eine Anwendung kann eine komprimierte Datei Teil Weise dekomprimieren, indem Sie die lzseek-und lzread-Funktionen verwendet.<br/>                 |



 

 

