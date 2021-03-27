---
description: Zusätzlich zum Abrufen von Daten mit Zeichenbreite für einzelne Zeichen müssen Anwendungen auch die Breite und Höhe ganzer Zeichen folgen berechnen.
ms.assetid: 0c1d9142-258a-447f-8950-8d684645383b
title: Zeichen folgen Breite und-Höhe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f57846d0588c518f445523361ae186e4b966bf93
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864327"
---
# <a name="string-widths-and-heights"></a>Zeichen folgen Breite und-Höhe

Zusätzlich zum Abrufen von Daten mit Zeichenbreite für einzelne Zeichen müssen Anwendungen auch die Breite und Höhe ganzer Zeichen folgen berechnen. Mit zwei Funktionen werden Zeichen folgen Breite und Höhenmessungen abgerufen: [**GetTextExtentPoint32**](/windows/desktop/api/Wingdi/nf-wingdi-gettextextentpoint32a)und [**gettabbedtextextent**](/windows/desktop/api/Winuser/nf-winuser-gettabbedtextextenta). Wenn die Zeichenfolge keine Tabulator Zeichen enthält, kann eine Anwendung die **GetTextExtentPoint32** -Funktion verwenden, um die Breite und Höhe einer angegebenen Zeichenfolge abzurufen. Wenn die Zeichenfolge Tabstopps enthält, sollte eine Anwendung die gettabbedtextextent-Funktion aufrufen.

Anwendungen können die [**GetTextExtentExPoint**](/windows/desktop/api/Wingdi/nf-wingdi-gettextextentexpointa) -Funktion für Wort Umbruch Vorgänge verwenden. Diese Funktion gibt die Anzahl von Zeichen aus einer angegebenen Zeichenfolge zurück, die in einen angegebenen Bereich passen.

## <a name="font-ascenders-and-descenders"></a>Schriftart und Nachfolger

Einige Anwendungen bestimmen den Zeilenabstand zwischen Textzeilen unterschiedlicher Größe mithilfe des maximalen Aufsteigers und des descender der Schriftart. Eine Anwendung kann diese Werte abrufen, indem Sie die [**GetTextMetrics**](/windows/desktop/api/Wingdi/nf-wingdi-gettextmetrics) -Funktion aufruft und dann die **tmascent** -und **tmdescent** -Member von [**TextMetric**](/windows/win32/api/wingdi/ns-wingdi-textmetrica)überprüft.

Die maximale Steigung und der Abstieg unterscheiden sich von der typografischen Besteigung und dem Abstieg. In TrueType-und OpenType-Schriftarten sind der typografische Aufstieg und der Abstieg in der Regel der obere Rand des f-Symbols und das Ende des g-Symbols. Eine Anwendung kann den typografische-Vorgänger und den unter Länge-Wert für eine TrueType-oder OpenType-Schriftart abrufen, indem die [**getoutlinetextmetrics**](/windows/desktop/api/Wingdi/nf-wingdi-getoutlinetextmetricsa) -Funktion aufgerufen und die Werte in den **otmmacascent** -und **otmmacdescent** -Elementen der [**outlinetextmetric**](/windows/desktop/api/Wingdi/ns-wingdi-outlinetextmetrica) -Struktur überprüft werden.

Die folgende Abbildung zeigt den Unterschied zwischen den in den Strukturen [**newtextmetric**](/windows/win32/api/wingdi/ns-wingdi-newtextmetrica) und [**outlinetextmetric**](/windows/win32/api/wingdi/ns-wingdi-outlinetextmetrica) zurückgegebenen vertikalen textmetrikwerten. (Die Namen, die mit OTM beginnen, sind Elemente der **outlinetextmetric** -Struktur.)

![Abbildung, die zeigt, wie Text Metrikwerte mit gliedertextmetrikwerten vergleichen](images/csftx-03.png)

## <a name="font-dimensions"></a>Schriftart Dimensionen

Eine Anwendung kann die physischen Dimensionen einer TrueType-oder OpenType-Schriftart abrufen, indem Sie die [**getoutlinetextmetrics**](/windows/desktop/api/Wingdi/nf-wingdi-getoutlinetextmetricsa) -Funktion aufrufen. Eine Anwendung kann die physischen Dimensionen jeder anderen Schriftart abrufen, indem Sie die [**GetTextMetrics**](/windows/desktop/api/Wingdi/nf-wingdi-gettextmetrics) -Funktion aufrufen. Um die Dimensionen eines Ausgabegeräts zu bestimmen, kann eine Anwendung die [**GetDeviceCaps**](/windows/desktop/api/Wingdi/nf-wingdi-getdevicecaps) -Funktion aufrufen. **Getde vicecaps** gibt sowohl physische als auch logische Dimensionen zurück.

Ein logischer Zoll ist ein Measure, das das System verwendet, um lesbare Schriftarten auf dem Bildschirm darzustellen, und ist ungefähr 30 bis 40 Prozent größer als ein physischer Zoll. Die Verwendung von logischen Zoll schließt eine genaue Entsprechung zwischen der Ausgabe des Bildschirms und des Druckers aus. Entwickler sollten sich bewusst sein, dass der Text auf einem Bildschirm nicht einfach eine skalierte Version des Texts ist, der auf der Seite angezeigt wird. Dies gilt insbesondere, wenn Grafiken in den Text eingebunden werden.

 

 
