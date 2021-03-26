---
description: In der folgenden Tabelle sind die wichtigsten Schriftart Metriken für Anwendungen aufgeführt, für die Portable Dokumente und die Funktionen erforderlich sind, mit denen eine Anwendung diese abrufen kann.
ms.assetid: 61f6d244-7397-42af-af58-0ab9d07bf19e
title: Metriken für Portable Dokumente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c840b1b8e8014086b97098a44890f170a6bd11d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104978553"
---
# <a name="metrics-for-portable-documents"></a>Metriken für Portable Dokumente

In der folgenden Tabelle sind die wichtigsten Schriftart Metriken für Anwendungen aufgeführt, für die Portable Dokumente und die Funktionen erforderlich sind, mit denen eine Anwendung diese abrufen kann.



| Funktion                                               | Metrik                | Verwendung                                                                                                          |
|--------------------------------------------------------|-----------------------|--------------------------------------------------------------------------------------------------------------|
| [**EnumFontFamilies**](/windows/desktop/api/Wingdi/nf-wingdi-enumfontfamiliesa)           | **ntmsizeem**         | Abrufen von Entwurfs Metriken Konvertierung in gerätemetriken.                                                   |
| [**Getcharabcbreiten**](/windows/desktop/api/Wingdi/nf-wingdi-getcharabcwidthsa)           | **Abcbreiten**         | Genaue Platzierung von Zeichen am Anfang und Ende von Rändern, Bild Begrenzungen und anderen Text Umbrüchen. |
| [**GetCharWidth32**](/windows/desktop/api/Wingdi/nf-wingdi-getcharwidth32a)               | **Advancebreiten**     | Platzierung von Zeichen in einer Zeile.                                                                           |
| [**Getoutlinetextmetrics**](/windows/desktop/api/Wingdi/nf-wingdi-getoutlinetextmetricsa) | **otmf sType**         | Schriftart: Einbettungs Bits.                                                                                         |
|                                                        | **otmscharsloperise** | Y-Komponente für die Steigung des Cursors für kursiv Schriftarten.                                                            |
|                                                        | **otmscharsloperun**  | X-Komponente für die Steigung des Cursors für kursiv Schriftarten.                                                            |
|                                                        | **otmascent**         | Zeilenabstand.                                                                                                |
|                                                        | **otmdescent**        | Zeilenabstand.                                                                                                |
|                                                        | **otmlinegap**        | Zeilenabstand.                                                                                                |
|                                                        | **otmpfamilyname**    | Schriftart Identifikation.                                                                                         |
|                                                        | **otmpstylename**     | Schriftart Identifikation.                                                                                         |
|                                                        | **otmpfullname**      | Schriftart Identifikation (normalerweise Familie-und Stilname).                                                      |



 

Die **otmscharsloperise**-, **otmscharsloperun**-, **otmascent**-, **otmdescent**-und **otmlinegap** -Member der [outlinetextmetric](/windows/desktop/api/Wingdi/ns-wingdi-outlinetextmetrica) -Struktur werden skaliert oder transformiert, sodass Sie dem aktuellen Geräte Modus und der physischen Höhe entsprechen (wie im **tmheight** -Member der [newtextmetric](/windows/win32/api/wingdi/ns-wingdi-newtextmetrica) -Struktur angegeben).

Die Schriftart Identifizierung ist in diesen Fällen wichtig, wenn eine Anwendung dieselbe Schriftart auswählen muss, z. b. Wenn ein Dokument erneut geöffnet oder in ein anderes Betriebssystem verschoben wird. Der Schriftart-Mapper wählt immer die richtige Schriftart aus, wenn eine Anwendung eine Schriftart nach vollständigem Namen anfordert. Die Familien-und Format Namen geben Eingaben für das Standard Dialogfeld Schriftart an, mit dem sichergestellt wird, dass die Auswahl leisten ordnungsgemäß platziert werden.

Die **otmscharsloperise** -und **otmscharsloperun-** Werte werden verwendet, um eine nahe Näherung des haupkursiv formatieren Winkels der Schriftart zu erhalten. Für typische römische Schriftarten ist **otmscharsloperise** 1, und **otmscharsloperun** ist 0 (null). Bei kursiv Formatierbaren Schriftarten versuchen die Werte, den Sinus und Kosinus des haupkursiv kursiv Winkels der Schriftart (in der vertikalen gegen den Uhrzeigersinn) zu nähern; Beachten Sie, dass der kursiv stehende Winkel für aufrufte Schriftarten 0 ist. Da diese Werte nicht in Entwurfs Einheiten ausgedrückt werden, sollten Sie nicht in Geräte Einheiten konvertiert werden.

Mit den Metriken für Zeichen Platzierung und Zeilenabstand kann eine Anwendung geräteunabhängige Zeilenumbrüche berechnen, die über Bildschirme, Drucker, typesetters und sogar Plattformen hinweg portabel sind.

**So führen Sie ein Geräte unabhängiges Seitenlayout durch**

1.  Normalisieren Sie alle Entwurfs Metriken auf einen allgemeinen Wert für eine extrem hohe Auflösung (z. b. 65.536 dpi). Dies verhindert einen roundoff-Fehler.
2.  Compute-Zeilenumbrüche auf der Grundlage von Uhr-Metriken und physischer Seitenbreite; Dies ergibt einen Ausgangspunkt und einen Endpunkt einer Zeile innerhalb des Text Stroms.
3.  Berechnen Sie die Breite der Geräteseite in Geräte Einheiten (z. b. Pixel).
4.  Passen Sie jede Textzeile mithilfe der in Schritt 2 berechneten Zeilenumbrüche in die Seitenbreite des Geräts an.
5.  Berechnen Sie Seitenumbrüche mithilfe von "Uhr"-Metriken und der physischen Seitenlänge. Dies ergibt die Anzahl der Zeilen pro Seite.
6.  Berechnen Sie die Linien Höhen in den Geräte Einheiten.
7.  Passen Sie die Textzeilen auf die Seite an. verwenden Sie dabei die Zeilen pro Seite aus Schritt 5 und die Zeilenhöhe aus Schritt 6.

Wenn alle Anwendungen diese Verfahren übernehmen, können Entwickler praktisch garantieren, dass Dokumente, die von einer Anwendung in eine andere verschoben werden, ihre ursprüngliche Darstellung und ihr ursprüngliches Format beibehalten.

 

 



