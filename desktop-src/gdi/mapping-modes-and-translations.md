---
description: Die Zuordnungsmodi werden in der folgenden Tabelle beschrieben.
ms.assetid: 02bc45d1-2921-48bc-a066-2314765b6531
title: Zuordnungsmodi und Übersetzungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 242ba699a8ec7289495cbcdff33e940460b20bcabffa373d5c792b1aee0fe9d2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118760146"
---
# <a name="mapping-modes-and-translations"></a>Zuordnungsmodi und Übersetzungen

Die Zuordnungsmodi werden in der folgenden Tabelle beschrieben.



| Zuordnungsmodus    | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                |
|-----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| MM \_ ANISOTROPIC | Jede Einheit im Seitenbereich wird einer anwendungsspezifischen Einheit im Gerätebereich zugeordnet. Die Achse kann gleich skaliert werden (z. B. kann ein Kreis, der im Raum gezeichnet wird, eine Ellipse sein, wenn er auf einem bestimmten Gerät dargestellt wird). Die Ausrichtung der Achse wird auch von der Anwendung angegeben.                  |
| MM \_ HIENGLISH   | Jede Einheit im Seitenbereich wird 0,001 Zoll im Gerätebereich zugeordnet. Der Wert von x erhöht sich von links nach rechts. Der Wert von y erhöht sich von unten nach oben.                                                                                                                                                                 |
| MM \_ HIMETRIC    | Jede Einheit im Seitenbereich wird 0,01 Millimeter im Gerätebereich zugeordnet. Der Wert von x erhöht sich von links nach rechts. Der Wert von y erhöht sich von unten nach oben.                                                                                                                                                            |
| MM \_ ISOTROPIC   | Jede Einheit im Seitenbereich wird einer anwendungsdefinierten Einheit im Gerätebereich zugeordnet. Die Achsen sind immer gleich skaliert. Die Ausrichtung der Achsen kann von der Anwendung angegeben werden.                                                                                                                                     |
| MM \_ LOENGLISH   | Jede Einheit im Seitenbereich wird 0,01 Zoll im Gerätebereich zugeordnet. Der Wert von x erhöht sich von links nach rechts. Der Wert von y erhöht sich von unten nach oben.                                                                                                                                                                  |
| MM \_ LOMETRIC    | Jede Einheit im Seitenbereich wird 0,1 Millimeter im Gerätebereich zugeordnet. Der Wert von x erhöht sich von links nach rechts. Der Wert von y erhöht sich von unten nach oben.                                                                                                                                                             |
| MM \_ TEXT        | Jede Einheit im Seitenbereich wird einem Pixel zugeordnet. Das heißt, es wird keine Skalierung durchgeführt. Wenn keine Übersetzung wirksam ist (dies ist die Standardeinstellung), entspricht der Seitenraum im \_ MM-Textzuordnungsmodus dem physischen Geräteraum. Der Wert von x erhöht sich von links nach rechts. Der Wert von y erhöht sich von oben nach unten. |
| MM \_ TWIPS       | Jede Einheit im Seitenbereich wird einem 1/1440-Zoll-Punkt eines Druckers zugeordnet. Der Wert von x erhöht sich von links nach rechts. Der Wert von y erhöht sich von unten nach oben.                                                                                                                                           |



 

Rufen Sie zum Festlegen eines Zuordnungsmodus die [**Funktion SetMapMode**](/windows/desktop/api/Wingdi/nf-wingdi-setmapmode) auf. Rufen Sie den aktuellen Zuordnungsmodus für einen DC ab, indem Sie die [**GetMapMode-Funktion**](/windows/desktop/api/Wingdi/nf-wingdi-getmapmode) aufrufen.

Die Transformationen zwischen Seitenbereich und Gerätebereich bestehen aus Werten, die aus den punkten berechnet werden, die vom Fenster und Viewport angegeben werden. In diesem Kontext bezieht sich das Fenster auf das logische Koordinatensystem des Seitenbereichs, während der Viewport auf das Gerätekoordinatensystem des Geräteraums verweist. Das Fenster und der Viewport bestehen jeweils aus einem Ursprung, einem horizontalen ("x") Und einem vertikalen ("y") Ausdungszeichen). Die Fensterparameter befinden sich in logischen Koordinaten. der Viewport in Gerätekoordinaten (Pixel). Das System kombiniert die Ursprünge und Ausdrungen aus dem Fenster und dem Viewport, um die Transformation zu erstellen. Dies bedeutet, dass das Fenster und der Viewport jeweils die Hälfte der Faktoren angeben, die zum Definieren der Transformation erforderlich sind, die zum Zuordnen von Punkten im Seitenbereich zum Gerätebereich verwendet wird. Daher ordnet das System den Ursprung des Fensters dem Viewport-Ursprung und die Fensterdungen den Viewport-Bereichen zu, wie in der folgenden Abbildung dargestellt.

![Abbildung eines Fensteranfangs im Seitenbereich und eines Blickpunkts im Geräteraum](images/cstrn-15.png)

Die Fenster- und Viewport-Erweiterungen stellen ein Verhältnis oder einen Skalierungsfaktor für die Transformationen zwischen Seitenbereich und Gerätebereich dar. Für die sechs vordefinierten \_ Zuordnungsmodi (MM HIENGLISH, MM \_ LOENGLISH, MM \_ HIMETRIC, MM \_ LOMETRIC, MM \_ TEXT und MM \_ TWIPS) [](/windows/desktop/api/Wingdi/nf-wingdi-setmapmode) werden die Werte vom System festgelegt, wenn SetMapMode aufgerufen wird. Sie können nicht geändert werden. Die anderen beiden Zuordnungsmodi (MM \_ ISOTROPIC und MM \_ ANISOTROPIC) erfordern, dass die Werte in Dendungen angegeben werden. Rufen Sie hierzu **SetMapMode** auf, um den entsprechenden Modus festzulegen, und rufen Sie dann die [**Funktionen SetWindowExtEx**](/windows/desktop/api/Wingdi/nf-wingdi-setwindowextex) und [**SetViewportExtEx**](/windows/desktop/api/Wingdi/nf-wingdi-setviewportextex) auf, um die Werte zu bestimmen. Im MM-ISOTROPIC-Zuordnungsmodus ist es \_ wichtig, **SetWindowExtEx auf** aufruft, bevor **SetViewportExtEx aufruft.**

Die Fenster- und Viewport-Ursprünge richten die Übersetzung ein, die im Seitenbereich in Gerätebereichstransformationen verwendet wird. Legen Sie die Fenster- und Viewport-Ursprünge mithilfe der [**Funktionen SetWindowOrgEx**](/windows/desktop/api/Wingdi/nf-wingdi-setwindoworgex) und [**SetViewportOrgEx**](/windows/desktop/api/Wingdi/nf-wingdi-setviewportorgex) fest. Die Ursprünge sind unabhängig von den Extents, und eine Anwendung kann sie unabhängig vom aktuellen Zuordnungsmodus festlegen. Das Ändern eines Zuordnungsmodus wirkt sich nicht auf die aktuell festgelegten Ursprünge aus (obwohl es sich auf die Extent auswirken kann). Ursprünge werden in absoluten Einheiten angegeben, die der aktuelle Zuordnungsmodus nicht beeinflusst. Verwenden Sie zum Ändern der Ursprünge die [**Funktionen OffsetWindowOrgEx**](/windows/desktop/api/Wingdi/nf-wingdi-offsetwindoworgex) und [**OffsetViewportOrgEx.**](/windows/desktop/api/Wingdi/nf-wingdi-offsetviewportorgex)

Die folgende Formel zeigt die Mathematik, die bei der Konvertierung eines Punkts vom Seiten- in den Gerätebereich verwendet wird.

``` syntax
Dx = ((Lx - WOx) * VEx / WEx) + VOx 
```

Die folgenden Variablen sind beteiligt.

``` syntax
Dx     x value in device units 
Lx     x value in logical units (also known as page space units) 
WOx     window x origin 
VOx     viewport x origin 
WEx     window x-extent 
VEx     viewport x-extent 
```

Dieselbe Gleichung mit y, die x ersetzt, transformiert die y-Komponente eines Punkts.

Die Formel versetzt zuerst den Punkt von ihrem Koordinaten-Ursprung. Dieser Wert, der nicht mehr vom Ursprung voreingenommen wird, wird dann im Verhältnis der Werte in das Zielkoordinatensystem skaliert. Schließlich wird der skalierte Wert durch den Ursprungsziel zur endgültigen Zuordnung versetzt.

Die [**Funktionen LPtoDP**](/windows/desktop/api/Wingdi/nf-wingdi-lptodp) und [**DPtoLP**](/windows/desktop/api/Wingdi/nf-wingdi-dptolp) können zum Konvertieren von logischen Punkten in Gerätepunkte bzw. von Gerätepunkten in logische Punkte verwendet werden.

 

 



