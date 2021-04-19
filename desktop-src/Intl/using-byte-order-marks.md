---
description: Stellen Sie immer eine Unicode-nur-Text-Datei mit einer Byte Reihenfolge-Markierung vor, die einer Anwendung mitteilt, dass die Datei in Byte sortiert ist.
ms.assetid: d9f1ef5c-6367-4183-9c07-01c73cb4debc
title: Verwenden von Byte Reihenfolge Markierungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b72d2ec366020f4c82c418e654e1c7fa0b4c8c1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106366497"
---
# <a name="using-byte-order-marks"></a>Verwenden von Byte Reihenfolge Markierungen

Stellen Sie immer eine Unicode-nur-Text-Datei mit einer Byte Reihenfolge-Markierung vor, die einer Anwendung mitteilt, dass die Datei in Byte sortiert ist. In der folgenden Tabelle sind die verfügbaren Byte-Reihenfolge Markierungen aufgeführt. Da der nur-Text-Unicode-Text eine Sequenz von 16-Bit-Codewerten ist, ist er für die beim Schreiben des Texts verwendete Byte Reihenfolge empfindlich.

> [!Note]  
> Eine Byte Reihenfolge Markierung ist kein Steuerzeichen, das die Byte Reihenfolge des Texts auswählt.

 



| Bytereihenfolge-Marke | BESCHREIBUNG           |
|-----------------|-----------------------|
| EF BB BF        | UTF-8                 |
| FF FE           | UTF-16, Little-d |
| FE FF           | UTF-16, Big-ddian    |
| FF FE 00 00     | UTF-32, Little-d |
| 00 00 FE FF     | UTF-32, Big-enddian    |



 

> [!Note]  
> Microsoft verwendet UTF-16, Little-Endian-Byte Reihenfolge.

 

Im Idealfall folgt der gesamte Unicode-Text nur einem Satz von Byte Reihenfolge Regeln. Dies ist jedoch nicht möglich, da sich die Mikroprozessoren bei der Platzierung des am wenigsten signifikanten Bytes unterscheiden. Intel-und MIPS-Prozessoren positionieren das am wenigsten signifikante Byte zuerst, während von den Motorola-Prozessoren (und allen Byte-umgekehrten Unicode-Dateien) die letzte Position angezeigt wird. Mit nur einem einzigen Satz von Byte Sortierregeln werden Benutzer von einem Typ von Mikroprozessor gezwungen, die Byte Reihenfolge jedes Mal auszutauschen, wenn eine nur-Text-Datei aus gelesen oder geschrieben wird, auch wenn die Datei nie auf ein anderes Betriebssystem auf der Grundlage eines anderen Mikroprozessors übertragen wird.

Der bevorzugte Ort zum Angeben der Byte Reihenfolge ist in einem Dateiheader, Textdateien haben jedoch keine Header. Daher hat Unicode ein Zeichen (u + FEFF) und ein nicht-Zeichen (u + FFFE) als Byte Reihenfolge Markierungen definiert. Sie sind Spiegel Byte Bilder zueinander.

Da die Sequenz U + FEFF am Anfang einer regulären nicht-Unicode-Textdatei sehr selten vorkommt, kann Sie als impliziter Marker oder eine Signatur dienen, um die Datei als Unicode-Datei zu identifizieren. Anwendungen, die sowohl Unicode-als auch nicht-Unicode-Textdateien lesen, sollten das vorhanden sein dieser Sequenz als Indikator verwenden, dass es sich bei der Datei höchstwahrscheinlich um eine Unicode-Datei handelt. Vergleichen Sie diese Technik mit der Verwendung des MS-DOS-markermarkers zum Beenden von Textdateien.

Wenn eine Anwendung am Anfang einer Textdatei U + FEFF findet, wird die Datei in der Regel als Unicode-Datei verarbeitet, obwohl Sie weitere heuristische Prüfungen zur Überprüfung durchführen kann. Eine solche Überprüfung kann so einfach wie das Testen sein, um herauszufinden, ob die Variation in den nieder wertigen Bytes deutlich höher ist als die Variation in den höherwertigen Bytes. Wenn z. b. ASCII-Text in Unicode-Text konvertiert wird, ist jedes zweite Byte 0. Außerdem kann die Überprüfung sowohl für den Zeilenvorschub als auch das Wagen Rücklauf Zeichen (u + 000A und U + 000D) sowie für die gerade oder ungerade Dateigröße einen starken Indikator für die Art der Datei bereitstellen.

Wenn eine Anwendung am Anfang einer Textdatei U + FFFE findet, wird Sie so interpretiert, dass die Datei eine Byte-umgekehrte Unicode-Datei ist. Die Anwendung kann entweder die Reihenfolge der Bytes austauschen oder den Benutzer darüber benachrichtigen, dass ein Fehler aufgetreten ist.

Da das Unicode-Byte Reihenfolge-Zeichen nicht in einer Codepage gefunden wird, wird es nicht mehr angezeigt, wenn Daten in ANSI konvertiert werden. Im Gegensatz zu anderen Unicode-Zeichen wird es beim Konvertieren nicht durch ein Standard Zeichen ersetzt. Wenn eine Byte Reihenfolge-Markierung in der Mitte einer Datei gefunden wird, wird Sie nicht als Unicode-Zeichen interpretiert und hat keine Auswirkung auf die Textausgabe.

> [!Note]  
> Der Unicode-Wert U + FFFF ist in nur-Text-Dateien unzulässig und kann nicht zwischen Anwendungen übermittelt werden. Es ist für die private Verwendung einer Anwendung reserviert.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden von Sonderzeichen in Unicode](using-special-characters-in-unicode.md)
</dt> </dl>

 

 



