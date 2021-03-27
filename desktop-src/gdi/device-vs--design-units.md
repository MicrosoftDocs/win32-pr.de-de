---
description: Eine Anwendung kann Schriftart Metriken nur für eine physische Schriftart abrufen, nachdem die Schriftart in einem Gerätekontext ausgewählt wurde.
ms.assetid: 3eaabc8b-e244-4b65-918b-a20043afa535
title: Geräte im Vergleich zu Entwurfs Einheiten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9fb52a671727a2fa84d5514b469be5bd320f3318
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863660"
---
# <a name="device-vs-design-units"></a>Geräte im Vergleich zu Entwurfs Einheiten

Eine Anwendung kann Schriftart Metriken nur für eine physische Schriftart abrufen, nachdem die Schriftart in einem Gerätekontext ausgewählt wurde. Wenn eine Schriftart in einen Gerätekontext ausgewählt wird, wird Sie für das Gerät skaliert. Die für das Gerät spezifischen Schriftart Metriken werden als Geräte Einheiten bezeichnet.

Portable Metriken in Schriftarten werden als Entwurfs Einheiten bezeichnet. Entwurfs Einheiten müssen in Geräte Einheiten konvertiert werden, damit Sie auf ein bestimmtes Gerät angewendet werden können. Verwenden Sie die folgende Formel, um Entwurfs Einheiten in Geräte Einheiten zu konvertieren.

*Deviceunits* = (*designunits* / *unitsperem*) \* (*pointsize*/72) \* *deviceresolution*

Die Variablen in dieser Formel haben folgende Bedeutungen.



| Variable           | BESCHREIBUNG                                                                                                                                                                |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *Deviceunits*      | Gibt die in Geräte Einheiten konvertierte Schriftart Metrik " *designunits* " an. Dieser Wert befindet sich in den gleichen Einheiten wie der für *deviceresolution* angegebene Wert.                          |
| *Design Units*      | Gibt die Schriftart Metrik an, die in Geräte Einheiten konvertiert werden soll. Bei diesem Wert kann es sich um eine beliebige Schriftart Metrik handeln, einschließlich der Breite eines Zeichens oder des aufsteigenden Werts für eine ganze Schriftart. |
| *unitsperem*       | Gibt die EM-Quadrat Größe für die Schriftart an.                                                                                                                                 |
| *PointSize*        | Gibt die Schriftgröße in Punkt an. (Ein Punkt ist gleich 1/72 Zoll.)                                                                                                 |
| *Deviceresolution* | Gibt die Anzahl der Geräte Einheiten (Pixel) pro Zoll an. Typische Werte können 300 für einen Laserdrucker oder 96 für einen VGA-Bildschirm sein.                                                |



 

Diese Formel sollte nicht verwendet werden, um Geräte Einheiten zurück in Entwurfs Einheiten zu konvertieren. Geräte Einheiten werden immer auf das nächste Pixel gerundet. Der weitergaberoundfehler kann sehr groß werden, insbesondere dann, wenn eine Anwendung mit Bildschirmgrößen arbeitet.

Um Entwurfs Einheiten anzufordern, erstellen Sie eine logische Schriftart, deren Höhe als *unitsperem* angegeben wird. Anwendungen können den Wert für *unitsperem* abrufen, indem Sie die Funktion " [**EnumFontFamilies**](/windows/desktop/api/Wingdi/nf-wingdi-enumfontfamiliesa) " aufrufen und den **ntmsizeem** -Member der [**newtextmetric**](/windows/win32/api/wingdi/ns-wingdi-newtextmetrica) -Struktur überprüfen.

 

 



