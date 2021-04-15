---
description: Die folgende Tabelle zeigt, welche Wörter reserviert sind und nicht verwendet werden dürfen.
ms.assetid: 680211de-3f81-4ea7-b03e-741096b5dde0
title: Reservierte Wörter, Header und Kommentare
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2696aaf6e635f08124e28392d0a8faf63c39a85
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104520888"
---
# <a name="reserved-words-header-and-comments"></a>Reservierte Wörter, Header und Kommentare

Die folgende Tabelle zeigt, welche Wörter reserviert sind und nicht verwendet werden dürfen.



|                  |          |           |
|------------------|----------|-----------|
| ARRAY            | DWORD    | UCHAR     |
| BINARY           | GLEITKOMMAZAHL    | ULONGLONG |
| binäre \_ Ressource | SDWORD   | UNICODE   |
| CHAR             | STRING   | WORD      |
| CSTRING          | SWORD    |           |
| Double           | TEMPLATE |           |



 

Der Header variabler Länge ist obligatorisch und muss sich am Anfang des Datenstroms befinden. Der-Header enthält die folgenden Daten.



| type           | Erforderlich | Größe (in Bytes) | Wert | BESCHREIBUNG                  |
|----------------|----------|-----------------|-------|------------------------------|
| Magische Zahl   | x        | 4               | XOF   |                              |
| Versionsnummer | x        | 2               | 03    | Hauptversion 3              |
|                |          |                 | 03    | Neben Version 3              |
| Formattyp    | x        | 4               | txt   | Textdatei                    |
|                |          |                 | bin   | Binärdatei                  |
|                |          |                 | übernehmen  | Mit mszip komprimierte Textdatei   |
|                |          |                 | bzip-Datei  | Mit mszip komprimierte Binärdatei |
| Float-Größe     | x        | 0064            |       | 64-Bit-Gleit Komma Zahlen                |
|                | x        | "0032"          |       | 32-Bit-Gleit Komma Zahlen                |



 

Die Werte in der Tabelle werden durch Anführungszeichen getrennt, um die Anzahl der Zeichen in den einzelnen Werten aufzurufen. Solche mit 4 Bytes enthalten vier Zeichen, die mit 2 Bytes zwei Zeichen enthalten.

Kommentare sind nur in Textdateien anwendbar. Kommentare können an beliebiger Stelle im Datenstrom auftreten. Ein Kommentar beginnt mit einem doppelten Schrägstrich (//) im C++-Format oder einem Nummern Zeichen ( \# ). Der Kommentar wird bis zur nächsten neuen Zeile ausgeführt. Das folgende Beispiel zeigt gültige Kommentare.


```
#  This is a comment.
// This is another comment.
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Text Codierung](text-encoding.md)
</dt> </dl>

 

 



