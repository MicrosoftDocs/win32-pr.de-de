---
description: Zeichnen von Text
ms.assetid: 8a06f659-4e08-4738-b7a9-956b599c1344
title: Zeichnen von Text (Windows-GDI)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7db44a756ff211bcae7605cb87bdac77005b34f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103754424"
---
# <a name="drawing-text-windows-gdi"></a>Zeichnen von Text (Windows-GDI)

Nachdem eine Anwendung die entsprechende Schriftart ausgewählt hat, legt die erforderlichen Text Formatierungsoptionen fest und berechnet die erforderlichen Zeichen breiten-und Höhenwerte für eine Text Zeichenfolge. Sie kann beginnen, Zeichen und Symbole zu zeichnen, indem Sie eine der Textausgabe Funktionen aufrufen:

-   [DrawText](/windows/desktop/api/Winuser/nf-winuser-drawtext)
-   [Drawtextex](/windows/desktop/api/Winuser/nf-winuser-drawtextexa)
-   [Exttextout](/windows/desktop/api/Wingdi/nf-wingdi-exttextouta)
-   [Polytextout](/windows/desktop/api/Wingdi/nf-wingdi-polytextouta)
-   [Tabbedtextout](/windows/desktop/api/Winuser/nf-winuser-tabbedtextouta)
-   [TextOut](/windows/desktop/api/Wingdi/nf-wingdi-textouta)

Wenn eine Anwendung eine dieser Funktionen aufruft, übergibt das Betriebssystem den Aufruf an die Grafik-Engine, die wiederum den Aufruf an den entsprechenden Gerätetreiber übergibt. Auf der Gerätetreiber Ebene werden alle diese Aufrufe von einem oder mehreren Aufrufen der eigenen [exttextout](/windows/desktop/api/Wingdi/nf-wingdi-exttextouta) -oder [TextOut](/windows/desktop/api/Wingdi/nf-wingdi-textouta) -Funktion des Treibers unterstützt. Eine Anwendung erreicht die schnellste Ausführung durch Aufrufen von [**exttextout**](/windows/win32/api/wingdi/nf-wingdi-exttextouta), die schnell in einen **exttextout** -Aufruf für das Gerät konvertiert werden kann. Es gibt jedoch Instanzen, wenn eine Anwendung eine der anderen drei Funktionen aufruft. um z. b. mehrere Textzeilen innerhalb der Rahmen eines angegebenen rechteckigen Bereichs zu zeichnen, ist es effizienter, [**DrawText**](/windows/win32/api/winuser/nf-winuser-drawtext)aufzurufen. Zum Erstellen einer Tabelle mit mehreren Spalten mit begründeten Textspalten ist es effizienter, [**tabbedtextout**](/windows/win32/api/winuser/nf-winuser-tabbedtextouta)aufzurufen.

 

 
