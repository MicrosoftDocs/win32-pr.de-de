---
description: Anwendungen müssen Daten mit Zeichenbreite abrufen, wenn sie Aufgaben wie das Anpassen von Textzeichenfolgen an Seiten- oder Spaltenbreiten ausführen.
ms.assetid: 0c84f5f9-71cd-4077-bc99-f23a393c1c4d
title: Zeichenbreiten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 822ae01ea1ccd5a2a7ec118cb1b93211b1c2e5c0a215737a600d9450b8996117
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117888099"
---
# <a name="character-widths"></a>Zeichenbreiten

Anwendungen müssen Daten mit Zeichenbreite abrufen, wenn sie Aufgaben wie das Anpassen von Textzeichenfolgen an Seiten- oder Spaltenbreiten ausführen. Es gibt vier Funktionen, mit denen eine Anwendung Daten mit Zeichenbreite abrufen kann. Zwei dieser Funktionen rufen die Zeichenvorrückungsbreite ab, und zwei dieser Funktionen rufen tatsächliche Zeichenbreitendaten ab.

Eine Anwendung kann die Funktionen [GetCharWidth32](/windows/desktop/api/Wingdi/nf-wingdi-getcharwidth32a) und [GetCharWidthFloat](/windows/desktop/api/Wingdi/nf-wingdi-getcharwidthfloata) verwenden, um die Breite für einzelne Zeichen oder Symbole in einer Textzeichenfolge abzurufen. Die Vorbreite ist der Abstand, den der Cursor auf einer Videoanzeige oder den Druckkopf auf einem Drucker vor dem Drucken des nächsten Zeichens in einer Textzeichenfolge vorrücken muss. Die [**GetCharWidth32-Funktion**](/windows/win32/api/wingdi/nf-wingdi-getcharwidth32a) gibt die vorgezogene Breite als ganzzahligen Wert zurück. Wenn eine höhere Genauigkeit erforderlich ist, kann eine Anwendung die [**GetCharWidthFloat-Funktion**](/windows/win32/api/wingdi/nf-wingdi-getcharwidthfloata) verwenden, um Dezimalstellenwerte mit erweiterter Breite abzurufen.

Eine Anwendung kann tatsächliche Zeichenbreitendaten mithilfe der Funktionen [GetCharABCWidths](/windows/desktop/api/Wingdi/nf-wingdi-getcharabcwidthsa) und [**GetCharABCWidthsFloat**](/windows/desktop/api/Wingdi/nf-wingdi-getcharabcwidthsfloata) abrufen. Die **GetCharABCWidthsFloat-Funktion** funktioniert mit allen Schriftarten. Die [**GetCharABCWidths-Funktion**](/windows/win32/api/wingdi/nf-wingdi-getcharabcwidthsa) funktioniert nur mit TrueType- und OpenType-Schriftarten. Weitere Informationen zu TrueType- und OpenType-Schriftarten finden Sie unter [Raster-, Vector-, TrueType- und OpenType-Schriftarten.](raster--vector--truetype--and-opentype-fonts.md)

Die folgende Abbildung zeigt die drei Komponenten einer Zeichenbreite:

![Abbildung: Abstand, B-Abstand und C-Abstand von zwei angrenzenden Zeichen](images/csftx-02.png)

Der Abstand A ist die Breite, die der aktuellen Position hinzugefügt werden soll, bevor das Zeichen platziert wird. Der B-Abstand ist die Breite des Zeichens selbst. Der C-Abstand ist der Leerraum rechts neben dem Zeichen. Die gesamte Vorausbreite wird durch Berechnen der Summe von A+B+C bestimmt. Die Zeichenzelle ist ein imaginäres Rechteck, das jedes Zeichen oder Symbol in einer Schriftart umschließt. Da Zeichen die Zeichenzelle über- oder unterhängen können, kann es sich entweder um eine negative Zahl oder um beide Inkremente von A und C handeln.

 

 
