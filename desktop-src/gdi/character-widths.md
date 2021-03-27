---
description: Anwendungen müssen Daten aus der Zeichenbreite abrufen, wenn Sie Aufgaben wie das Anpassen von Text Zeichenfolgen an die Seiten-oder Spaltenbreite ausführen.
ms.assetid: 0c84f5f9-71cd-4077-bc99-f23a393c1c4d
title: Zeichenbreite
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 950fbb7e6ad1e5f4ef12f2abd9e528ce3158a869
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863687"
---
# <a name="character-widths"></a>Zeichenbreite

Anwendungen müssen Daten aus der Zeichenbreite abrufen, wenn Sie Aufgaben wie das Anpassen von Text Zeichenfolgen an die Seiten-oder Spaltenbreite ausführen. Es gibt vier Funktionen, die eine Anwendung verwenden kann, um Daten mit Zeichenbreite abzurufen. Zwei dieser Funktionen rufen die Zeichen Vorlauf Breite ab, und zwei dieser Funktionen rufen tatsächliche Daten der Zeichenbreite ab.

Eine Anwendung kann die [GetCharWidth32](/windows/desktop/api/Wingdi/nf-wingdi-getcharwidth32a) -Funktion und die [getcharwidthfloat](/windows/desktop/api/Wingdi/nf-wingdi-getcharwidthfloata) -Funktion verwenden, um die voraus Breite für einzelne Zeichen oder Symbole in einer Text Zeichenfolge abzurufen. Die erweiterte Breite ist die Distanz, die der Cursor auf einer Videoanzeige oder der Druck Kopf auf einem Drucker vor dem Drucken des nächsten Zeichens in einer Text Zeichenfolge vor dem Drucken des nächsten Zeichens fortsetzen muss. Die [**GetCharWidth32**](/windows/win32/api/wingdi/nf-wingdi-getcharwidth32a) -Funktion gibt die erweiterte Breite als ganzzahligen Wert zurück. Wenn eine höhere Genauigkeit erforderlich ist, kann eine Anwendung die [**getcharwidthfloat**](/windows/win32/api/wingdi/nf-wingdi-getcharwidthfloata) -Funktion verwenden, um Werte für die Sekundenbruchteile abzurufen.

Eine Anwendung kann tatsächliche Daten der Zeichenbreite mithilfe der Funktionen [getcharabcwidth](/windows/desktop/api/Wingdi/nf-wingdi-getcharabcwidthsa) und [**getcharabcwidthsfloat**](/windows/desktop/api/Wingdi/nf-wingdi-getcharabcwidthsfloata) abrufen. Die **getcharabcwidthsfloat** -Funktion funktioniert mit allen Schriftarten. Die [**getcharabcbreiten**](/windows/win32/api/wingdi/nf-wingdi-getcharabcwidthsa) -Funktion funktioniert nur mit TrueType-und OpenType-Schriftarten. Weitere Informationen zu TrueType-und OpenType-Schriftarten finden Sie unter [Raster-, Vektor-, TrueType-und OpenType-Schriftarten](raster--vector--truetype--and-opentype-fonts.md).

Die folgende Abbildung zeigt die drei Komponenten einer Zeichenbreite:

![Darstellung der Abstände, b-Abstände und c-Abstände von zwei angrenzenden Zeichen](images/csftx-02.png)

Der Abstand ist die Breite, die der aktuellen Position vor dem Platzieren des Zeichens hinzugefügt wird. Der B-Abstand ist die Breite des Zeichens selbst. Der C-Abstand ist der Leerraum rechts vom Zeichen. Die gesamte Fortschritt Breite wird durch Berechnen der Summe von A + B + C festgelegt. Die Zeichen Zelle ist ein imaginäres Rechteck, das die einzelnen Zeichen oder Symbole in einer Schriftart umgibt. Da Zeichen die Zeichen Zelle überschreiten oder unterschreiten können, kann es sich bei den Schritten a und C um eine negative Zahl handeln.

 

 
