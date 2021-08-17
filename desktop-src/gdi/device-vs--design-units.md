---
description: Eine Anwendung kann Schriftartmetriken für eine physische Schriftart nur abrufen, nachdem die Schriftart in einem Gerätekontext ausgewählt wurde.
ms.assetid: 3eaabc8b-e244-4b65-918b-a20043afa535
title: Geräte- und Entwurfseinheiten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 456ac0ed7ad02ced5390201000fbc76217b8c579116bf36b356b13880d5d0158
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119354410"
---
# <a name="device-vs-design-units"></a>Geräte- und Entwurfseinheiten

Eine Anwendung kann Schriftartmetriken für eine physische Schriftart nur abrufen, nachdem die Schriftart in einem Gerätekontext ausgewählt wurde. Wenn eine Schriftart in einem Gerätekontext ausgewählt wird, wird sie für das Gerät skaliert. Die für das Gerät spezifischen Schriftartmetriken werden als Geräteeinheiten bezeichnet.

Portable Metriken in Schriftarten werden als Entwurfseinheiten bezeichnet. Um auf ein angegebenes Gerät angewendet zu werden, müssen Entwurfseinheiten in Geräteeinheiten konvertiert werden. Verwenden Sie die folgende Formel, um Entwurfseinheiten in Geräteeinheiten zu konvertieren.

*DeviceUnits* = (*DesignUnits* / *unitsPerEm*) \* (*PointSize*/72) \* *DeviceResolution*

Die Variablen in dieser Formel haben die folgende Bedeutung.



| Variable           | BESCHREIBUNG                                                                                                                                                                |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *DeviceUnits*      | Gibt die in Geräteeinheiten konvertierte *Schriftartmetrik DesignUnits* an. Dieser Wert befindet sich in den gleichen Einheiten wie der für *DeviceResolution* angegebene Wert.                          |
| *DesignUnits*      | Gibt die Schriftartmetrik an, die in Geräteeinheiten konvertiert werden soll. Dieser Wert kann eine beliebige Schriftartmetrik sein, einschließlich der Breite eines Zeichens oder des aufsteigenden Werts für eine ganze Schriftart. |
| *unitsPerEm*       | Gibt die Quadratgröße em für die Schriftart an.                                                                                                                                 |
| *PointSize*        | Gibt den Schriftgrad in Punkten an. (Ein Punkt entspricht 1/72 Zoll.)                                                                                                 |
| *DeviceResolution* | Gibt die Anzahl der Geräteeinheiten (Pixel) pro Zoll an. Typische Werte können 300 für einen Drucker oder 96 für einen VGA-Bildschirm sein.                                                |



 

Diese Formel sollte nicht verwendet werden, um Geräteeinheiten zurück in Entwurfseinheiten zu konvertieren. Geräteeinheiten werden immer auf das nächste Pixel gerundet. Der weitergegebene Round-Off-Fehler kann sehr groß werden, insbesondere wenn eine Anwendung mit Bildschirmgrößen arbeitet.

Um Entwurfseinheiten anzufordern, erstellen Sie eine logische Schriftart, deren Höhe als *unitsPerEm* angegeben ist. Anwendungen können den Wert für *unitsPerEm abrufen,* indem sie die [**EnumFontFamilies-Funktion**](/windows/desktop/api/Wingdi/nf-wingdi-enumfontfamiliesa) aufrufen und den **ntmSizeEM-Member** der [**NEWTEXTMETRIC-Struktur**](/windows/win32/api/wingdi/ns-wingdi-newtextmetrica) überprüfen.

 

 



