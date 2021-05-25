---
description: Die folgende Tabelle zeigt, welche Wörter reserviert sind und nicht verwendet werden dürfen.
ms.assetid: 680211de-3f81-4ea7-b03e-741096b5dde0
title: Reservierte Wörter, Header und Kommentare
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8879d0dbb518f92f0d8a6c38793ab315ae48b73e
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/24/2021
ms.locfileid: "110343655"
---
# <a name="reserved-words-header-and-comments"></a>Reservierte Wörter, Header und Kommentare

Die folgende Tabelle zeigt, welche Wörter reserviert sind und nicht verwendet werden dürfen.

| Reservierte Wörter | Reservierte Wörter | Reservierte Wörter|
|------------------|----------|-----------|
| ARRAY            | DWORD    | UCHAR     |
| BINARY           | GLEITKOMMAZAHL    | ULONGLONG |
| BINÄRE \_ RESSOURCE | SDWORD   | UNICODE   |
| CHAR             | STRING   | WORD      |
| Cstring          | SWORD    |           |
| Double           | TEMPLATE |           |



 

Der Header variabler Länge ist unerlangt und muss sich am Anfang des Datenstroms befindet. Der Header enthält die folgenden Daten.



| Typ           | Erforderlich | Größe (in Bytes) | Wert | BESCHREIBUNG                  |
|----------------|----------|-----------------|-------|------------------------------|
| Magic Number   | x        | 4               | Xof   |                              |
| Versionsnummer | x        | 2               | 03    | Hauptversion 3              |
|                |          |                 | 03    | Nebenversion 3              |
| Formattyp    | x        | 4               | txt   | Textdatei                    |
|                |          |                 | bin   | Binärdatei                  |
|                |          |                 | tzip  | Komprimierte MSZip-Textdatei   |
|                |          |                 | bzip  | Komprimierte MSZip-Binärdatei |
| Gleitkommagröße     | x        | 0064            |       | 64-Bit-Gleitkomma                |
|                | x        | "0032"          |       | 32-Bit-Gleitkomma                |



 

Die Werte in der Tabelle werden durch Anführungszeichen getrennt, um die Aufmerksamkeit auf die Anzahl der Zeichen in jedem Wert zu lenken. Die mit 4 Bytes enthalten vier Zeichen, die mit 2 Bytes zwei Zeichen.

Kommentare gelten nur in Textdateien. Kommentare können an einer beliebigen Stelle im Datenstrom auftreten. Ein Kommentar beginnt entweder mit doppelten Schrägstrichen (/) im C++-Stil oder mit einem Nummernzeichen ( \# ). Der Kommentar wird bis zur nächsten neuen Zeile ausgeführt. Das folgende Beispiel zeigt gültige Kommentare.


```
#  This is a comment.
// This is another comment.
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Textcodierung](text-encoding.md)
</dt> </dl>

 

 



