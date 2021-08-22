---
description: Das NTFS-Dateisystem verwendet Lempel-Ziv Komprimierung, bei der es sich um einen verlustlosen Komprimierungsalgorithmus handelt.
ms.assetid: 35a9fb47-5a73-479c-8fe0-5a2b07705536
title: Dateikomprimierung und Dekomprimierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f61c19449d1bfb31dfdd6e55e8c5ffa204bda36af597c43204693c55b13254e5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119927800"
---
# <a name="file-compression-and-decompression"></a>Dateikomprimierung und Dekomprimierung

Die NTFS-Dateisystemvolumes unterstützen die Dateikomprimierung auf Einzeldateibasis. Der vom NTFS-Dateisystem verwendete Dateikomprimierungsalgorithmus ist Lempel-Ziv Komprimierung. Dies  ist ein verlustfreier Komprimierungsalgorithmus, der bedeutet, dass beim Komprimieren  und Dekomprimieren der Datei keine Daten verloren gehen, im Gegensatz zu verlustbehafteten Komprimierungsalgorithmen wie JPEG, bei denen einige Daten bei jeder Datenkomprimierung und Dekomprimierung verloren gehen.

Die Datenkomprimierung reduziert die Größe einer Datei, indem redundante Daten minimiert werden. In einer Textdatei können redundante Daten häufig vorkommende Zeichen sein, z. B. das Leerzeichen oder allgemeine Vokale, z. B. die Buchstaben e und a; es kann auch häufig vorkommende Zeichenfolgen sein. Die Datenkomprimierung erstellt eine komprimierte Version einer Datei, indem diese redundanten Daten minimiert werden.

Jeder Typ von Datenkomprimierungsalgorithmus minimiert redundante Daten auf einzigartige Weise. Beispielsweise weist der *Huffman-Codierungsalgorithmus* Zeichen in einer Datei basierend darauf, wie häufig diese Zeichen auftreten, einen Code zu. Ein anderer Komprimierungsalgorithmus, der als Codierung der Ausführungslänge bezeichnet *wird,* generiert einen zweiteilige Wert für wiederholte Zeichen: Der erste Teil gibt an, wie oft das Zeichen wiederholt wird, und der zweite Teil identifiziert das Zeichen. Ein weiterer Komprimierungsalgorithmus, der *auch als Algorithmus Fürpel-Ziv* bezeichnet wird, konvertiert Zeichenfolgen variabler Länge in Codes fester Länge, die weniger Speicherplatz als die ursprünglichen Zeichenfolgen verbrauchen.

## <a name="the-ntfs-file-system-file-compression"></a>Die NTFS-Dateisystemdateikomprimierung

Im NTFS-Dateisystem erfolgt die Komprimierung transparent. Dies bedeutet, dass es ohne Änderungen an vorhandenen Anwendungen verwendet werden kann. Die komprimierten Bytes der Datei sind für Anwendungen nicht zugänglich. sie sehen nur die unkomprimierten Daten. Daher können Anwendungen, die eine komprimierte Datei öffnen, damit arbeiten, als wäre sie nicht komprimiert. Diese Dateien können jedoch nicht in ein anderes Dateisystem kopiert werden.

Wenn Sie eine Datei komprimieren, die größer als 30 Gigabyte ist, ist die Komprimierung möglicherweise nicht erfolgreich.

In den folgenden Themen wird die NTFS-Dateisystemdateikomprimierung identifiziert:

-   [Komprimierungsattribut](compression-attribute.md)
-   [Komprimierungsstatus](compression-state.md)
-   [Abrufen der Größe einer komprimierten Datei](obtaining-the-size-of-a-compressed-file.md)

## <a name="file-compression-and-decompression-libraries"></a>Dateikomprimierungs- und Dekomprimierungsbibliotheken

Die Dateikomprimierungs- und Dekomprimierungsbibliotheken verwenden eine oder mehrere vorhandene Dateien und erzeugen eine oder mehrere Dateien, bei denen es sich um komprimierte Versionen der Originaldateien handelt. Die Komprimierung ist ebenfalls verlustfrei, aber die Komprimierung ist für Anwendungen nicht transparent. Eine Anwendung kann solche Dateien nur mithilfe einer Dateikomprimierungsbibliothek verwenden. Darüber hinaus sind die einzigen Vorgänge, die Sie für solche Dateien ausführen können, das Erstellen einer komprimierten Datei aus einem Original und das Wiederherstellen der ursprünglichen Daten aus der dekomprimierten Version. Die Bearbeitung wird in der Regel nicht unterstützt, und die Suchfunktionen sind eingeschränkt, wenn sie überhaupt unterstützt werden.

In der Regel ruft eine Anwendung Funktionen in Lz32.dll, um Daten zu dekomprimieren, die mithilfe von Compress.exe. Die Funktionen können auch Dateien verarbeiten, ohne zu versuchen, sie zu dekomprimieren.

Sie können die Funktionen in Lz32.dll, um einzelne oder mehrere Dateien zu dekomprimieren. Sie können sie auch verwenden, um komprimierte Dateien nach und nach zu dekomprimieren.

In den folgenden Themen wird die Dateidekomprimierung identifiziert, die von den Funktionen in Lz32.dll:

-   [Dekomprimieren einer einzelnen Datei](decompressing-a-single-file.md)
-   [Dekomprimieren mehrerer Dateien](decompressing-multiple-files.md)
-   [Lesen aus komprimierten Dateien](reading-from-compressed-files.md)

## <a name="cabinets"></a>Schränke

Schränken werden von einer Komprimierungsbibliothek erstellt, die Features wie Datenträgerübergreifende und Multidateikomprimierung unterstützt. Weitere Informationen finden Sie im Cabinet Software Development Kit: [https://msdn.microsoft.com/library/dncabsdk/html/cabdl.asp](/previous-versions/ms974336(v=msdn.10)) .

## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                                                             | Beschreibung                                                                                                                              |
|---------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| [Komprimierungsattribut](compression-attribute.md)<br/>                                     | Auf einem NTFS-Dateisystem-Volume verfügt jede Datei und jedes Verzeichnis über das *Komprimierungsattribut*.<br/>                                         |
| [Komprimierungsstatus](compression-state.md)<br/>                                             | Jede Datei und jedes Verzeichnis auf einem Volume, das die Komprimierung für einzelne Dateien und Verzeichnisse unterstützt, hat den *Komprimierungsstatus*.<br/> |
| [Abrufen der Größe einer komprimierten Datei](obtaining-the-size-of-a-compressed-file.md)<br/> | Um die komprimierte Größe einer Datei zu erhalten, verwenden Sie die GetCompressedFileSize-Funktion.<br/>                                               |
| [Dekomprimieren einer einzelnen Datei](decompressing-a-single-file.md)<br/>                         | Eine Anwendung kann eine einzelne komprimierte Datei mithilfe der Funktionen LZOpenFile, LZCopy und LZClose dekomprimieren.<br/>                |
| [Dekomprimieren mehrerer Dateien](decompressing-multiple-files.md)<br/>                       | Eine Anwendung kann mehrere Dateien mithilfe der Funktionen LZOpenFile, LZCopy und LZClose dekomprimieren.<br/>                          |
| [Lesen aus komprimierten Dateien](reading-from-compressed-files.md)<br/>                     | Eine Anwendung kann eine komprimierte Datei mithilfe der Funktionen LZSeek und LZRead nach und nach dekomprimieren.<br/>                 |



 

 

