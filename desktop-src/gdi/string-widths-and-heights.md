---
description: Zusätzlich zum Abrufen von Daten mit Zeichenbreite für einzelne Zeichen müssen Anwendungen auch die Breite und Höhe ganzer Zeichenfolgen berechnen.
ms.assetid: 0c1d9142-258a-447f-8950-8d684645383b
title: Zeichenfolgenbreiten und -höhen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d5a9ee485cbc163cc7cbb9dbd296f15db0e9e622f4be6ad8dcb251b583099f8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119778820"
---
# <a name="string-widths-and-heights"></a>Zeichenfolgenbreiten und -höhen

Zusätzlich zum Abrufen von Daten mit Zeichenbreite für einzelne Zeichen müssen Anwendungen auch die Breite und Höhe ganzer Zeichenfolgen berechnen. Zwei Funktionen rufen Zeichenfolgenbreiten- und Höhenmessungen ab: [**GetTextExtentPoint32**](/windows/desktop/api/Wingdi/nf-wingdi-gettextextentpoint32a)und [**GetTabbedTextExtent.**](/windows/desktop/api/Winuser/nf-winuser-gettabbedtextextenta) Wenn die Zeichenfolge keine Tabstoppzeichen enthält, kann eine Anwendung die **GetTextExtentPoint32-Funktion** verwenden, um die Breite und Höhe einer angegebenen Zeichenfolge abzurufen. Wenn die Zeichenfolge Tabstoppzeichen enthält, sollte eine Anwendung die GetTabbedTextExtent-Funktion aufrufen.

Anwendungen können die [**GetTextExtentExPoint-Funktion**](/windows/desktop/api/Wingdi/nf-wingdi-gettextextentexpointa) für Zeilenumbruchvorgänge verwenden. Diese Funktion gibt die Anzahl der Zeichen aus einer angegebenen Zeichenfolge zurück, die in ein angegebenes Leerzeichen passen.

## <a name="font-ascenders-and-descenders"></a>Aufsteigende Und Nachfolger von Schriftarten

Einige Anwendungen bestimmen den Zeilenabstand zwischen Textzeilen unterschiedlicher Größe mithilfe des maximalen Auf- und Absteigens einer Schriftart. Eine Anwendung kann diese Werte abrufen, indem sie die [**GetTextMetrics-Funktion aufruft**](/windows/desktop/api/Wingdi/nf-wingdi-gettextmetrics) und dann die **TmAscent-** und **tmDescent-Member** von [**TEXTMETRIC**](/windows/win32/api/wingdi/ns-wingdi-textmetrica)überprüft.

Der maximale Anstieg und der Abstieg unterscheiden sich vom typografischen Anstieg und dem Abstieg. In TrueType- und OpenType-Schriftarten sind der typografische Anstieg und der Abstieg in der Regel der Anfang des f-Glyphes und der untere Rand des Glyphen. Eine Anwendung kann den typografischen Aufsteigend- und Nachfolger für eine TrueType- oder OpenType-Schriftart abrufen, indem sie die [**GetOutlineTextMetrics-Funktion**](/windows/desktop/api/Wingdi/nf-wingdi-getoutlinetextmetricsa) aufruft und die Werte in den **Membern otmMacAscent** und **otmMacDescent** der [**OUTLINETEXTMETRIC-Struktur**](/windows/desktop/api/Wingdi/ns-wingdi-outlinetextmetrica) überprüft.

Die folgende Abbildung zeigt den Unterschied zwischen den vertikalen Textmetrikwerten, die in den Strukturen [**NEWTEXTMETRIC**](/windows/win32/api/wingdi/ns-wingdi-newtextmetrica) und [**OUTLINETEXTMETRIC**](/windows/win32/api/wingdi/ns-wingdi-outlinetextmetrica) zurückgegeben werden. (Die Namen, die mit otm beginnen, sind Member der **OUTLINETEXTMETRIC-Struktur.)**

![Abbildung, die zeigt, wie Textmetrikwerte mit Werten für Konturtextmetriken gegenüber stehen](images/csftx-03.png)

## <a name="font-dimensions"></a>Schriftabmessungen

Eine Anwendung kann die physischen Dimensionen einer TrueType- oder OpenType-Schriftart abrufen, indem sie die [**GetOutlineTextMetrics-Funktion aufruft.**](/windows/desktop/api/Wingdi/nf-wingdi-getoutlinetextmetricsa) Eine Anwendung kann die physischen Dimensionen einer beliebigen anderen Schriftart abrufen, indem sie die [**GetTextMetrics-Funktion aufruft.**](/windows/desktop/api/Wingdi/nf-wingdi-gettextmetrics) Um die Dimensionen eines Ausgabegeräts zu bestimmen, kann eine Anwendung die [**GetDeviceCaps-Funktion**](/windows/desktop/api/Wingdi/nf-wingdi-getdevicecaps) aufrufen. **GetDeviceCaps** gibt sowohl physische als auch logische Dimensionen zurück.

Ein logischer Zoll ist ein Measure, das das System verwendet, um lesbare Schriftarten auf dem Bildschirm darzustellen, und ist ungefähr 30 bis 40 Prozent größer als ein physischer Zoll. Die Verwendung logischer Zolls schließt eine genaue Übereinstimmung zwischen der Ausgabe des Bildschirms und des Druckers aus. Entwickler sollten beachten, dass der Text auf einem Bildschirm nicht einfach eine skalierte Version des Texts ist, die auf der Seite angezeigt wird, insbesondere wenn Grafiken in den Text integriert werden.

 

 
