---
description: In der folgenden Tabelle sind die wichtigsten Schriftartmetriken für Anwendungen angegeben, die portable Dokumente erfordern, sowie die Funktionen, die es einer Anwendung ermöglichen, sie abzurufen.
ms.assetid: 61f6d244-7397-42af-af58-0ab9d07bf19e
title: Metriken für portable Dokumente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3762846e6d8280c2680f47f3cb32cd847ea4e664dab47a8a0995f5505c393da3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119558500"
---
# <a name="metrics-for-portable-documents"></a>Metriken für portable Dokumente

In der folgenden Tabelle sind die wichtigsten Schriftartmetriken für Anwendungen angegeben, die portable Dokumente erfordern, sowie die Funktionen, die es einer Anwendung ermöglichen, sie abzurufen.



| Funktion                                               | Metrik                | Verwendung                                                                                                          |
|--------------------------------------------------------|-----------------------|--------------------------------------------------------------------------------------------------------------|
| [**EnumFontFamilies**](/windows/desktop/api/Wingdi/nf-wingdi-enumfontfamiliesa)           | **ntmSizeEM**         | Abrufen von Entwurfsmetriken; Konvertierung in Gerätemetriken.                                                   |
| [**GetCharABCWidths**](/windows/desktop/api/Wingdi/nf-wingdi-getcharabcwidthsa)           | **ABCWidths**         | Genaue Platzierung von Zeichen am Anfang und Ende von Rändern, Bildgrenzen und anderen Textumbrüchen. |
| [**GetCharWidth32**](/windows/desktop/api/Wingdi/nf-wingdi-getcharwidth32a)               | **AdvanceWidths**     | Platzierung von Zeichen in einer Zeile.                                                                           |
| [**GetOutlineTextMetrics**](/windows/desktop/api/Wingdi/nf-wingdi-getoutlinetextmetricsa) | **otmfsType**         | Schriftart-Einbettungsbits.                                                                                         |
|                                                        | **otmsCharS aber auch** | Y-Komponente für die Steigung des Cursors für kursale Schriftarten.                                                            |
|                                                        | **otmsCharSrun**  | X-Komponente für die Steigung des Cursors für kursale Schriftarten.                                                            |
|                                                        | **otmAscent**         | Zeilenabstand.                                                                                                |
|                                                        | **otmDescent**        | Zeilenabstand.                                                                                                |
|                                                        | **otmLineGap**        | Zeilenabstand.                                                                                                |
|                                                        | **otmpFamilyName**    | Schriftartidentifikation.                                                                                         |
|                                                        | **otmpStyleName**     | Schriftartidentifikation.                                                                                         |
|                                                        | **otmpFullName**      | Schriftartidentifikation (in der Regel Familien- und Stilname).                                                      |



 

Die **Member otmsCharSmetric ,** **otmsCharSillaRun**, **otmAscent**, **otmDescent** und **otmLineGap** der [OUTLINETEXTMETRIC-Struktur](/windows/desktop/api/Wingdi/ns-wingdi-outlinetextmetrica) werden skaliert oder transformiert, um dem aktuellen Gerätemodus und der physischen Höhe zu entsprechen (wie im **tmHeight-Member** der [NEWTEXTMETRIC-Struktur](/windows/win32/api/wingdi/ns-wingdi-newtextmetrica) angegeben).

Die Schriftartidentifikation ist in diesen Fällen wichtig, wenn eine Anwendung dieselbe Schriftart auswählen muss, z. B. wenn ein Dokument erneut geöffnet oder in ein anderes Betriebssystem verschoben wird. Die Schriftartzuordnung wählt immer die richtige Schriftart aus, wenn eine Anwendung eine Schriftart mit vollständigem Namen an fordert. Die Familien- und Stilnamen stellen Eingaben für das Standardschriftfeld zur Verfügung, das sicherstellt, dass die Auswahlleisten ordnungsgemäß platziert werden.

Mit **den Werten otmsCharS font Und** **otmsCharSschlussRun** wird eine nahe Näherung des wichtigsten italischen Winkels der Schriftart erzeugt. Bei typischen romanischen **Schriftarten ist otmsCharS aber** 1 und **otmsCharSrun** 0. Bei italischen Schriftarten versuchen die Werte, den Sinus und den Kosinus des italischen Hauptwinkels der Schriftart (gegen den Uhrzeigersinn über vertikal hinaus) zu ungefähren. Beachten Sie, dass der italische Winkel für aufrechte Schriftarten 0 ist. Da diese Werte nicht in Entwurfseinheiten ausgedrückt werden, sollten sie nicht in Geräteeinheiten konvertiert werden.

Die Metriken für Zeichenplatzierung und Zeilenabstand ermöglichen es einer Anwendung, geräteunabhängige Zeilenumbrüche zu berechnen, die auf Bildschirmen, Druckern, Typen und sogar Plattformen portierbar sind.

**So führen Sie ein geräteunabhängiges Seitenlayout aus**

1.  Normalisieren Sie alle Entwurfsmetriken auf einen allgemeinen UHR-Wert (Ultra High Resolution), z. B. 65.536 DPI; Dadurch werden Rundungsfehler verhindert.
2.  Berechnen von Zeilenumbrüchen basierend auf UHR-Metriken und physischer Seitenbreite; dies ergibt einen Ausgangspunkt und einen Endpunkt einer Zeile innerhalb des Textstreams.
3.  Berechnen Sie die Geräteseitenbreite in Geräteeinheiten (z. B. Pixel).
4.  Passen Sie jede Textzeile in die Breite der Geräteseite ein, indem Sie die in Schritt 2 berechneten Zeilenumbrüche verwenden.
5.  Berechnen von Seitenumbrüchen mithilfe von UHR-Metriken und der physischen Seitenlänge; Dies ergibt die Anzahl der Zeilen pro Seite.
6.  Berechnen Sie die Linienhöhen in Geräteeinheiten.
7.  Passen Sie die Textzeilen auf die Seite an, indem Sie die Zeilen pro Seite aus Schritt 5 und die Zeilenhöhen aus Schritt 6 verwenden.

Wenn alle Anwendungen diese Techniken übernehmen, können Entwickler praktisch garantieren, dass Dokumente, die von einer Anwendung in eine andere verschoben wurden, ihre ursprüngliche Darstellung und ihr ursprüngliches Format beibehalten.

 

 



