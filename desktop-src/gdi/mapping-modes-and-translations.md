---
description: Die Mapping-Modi werden in der folgenden Tabelle beschrieben.
ms.assetid: 02bc45d1-2921-48bc-a066-2314765b6531
title: Mapping-Modi und-Übersetzungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 219bfe2f587ef9bc66f53d6f08404a0448180512
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215192"
---
# <a name="mapping-modes-and-translations"></a>Mapping-Modi und-Übersetzungen

Die Mapping-Modi werden in der folgenden Tabelle beschrieben.



| Mapping-Modus    | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                |
|-----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| MM- \_ anisotrope | Jede Einheit im Seiten Raum wird einer anwendungsspezifischen Einheit im Gerätespeicher zugeordnet. Die Achse ist möglicherweise gleichmäßig skaliert (z. b. kann es vorkommen, dass ein im Raum gezeichneter Kreis eine Ellipse ist, wenn Sie auf einem bestimmten Gerät dargestellt wird). Die Ausrichtung der Achse wird auch von der Anwendung angegeben.                  |
| MM- \_ hienglish   | Jede Einheit im Seiten Raum wird im Gerätebereich 0,001 Zoll zugeordnet. Der Wert von x wird von links nach rechts vergrößert. Der Wert von y wird von unten nach oben vergrößert.                                                                                                                                                                 |
| MM- \_ himetrik    | Jede Einheit im Seiten Raum wird im Geräteraum 0,01 Millimeter zugeordnet. Der Wert von x wird von links nach rechts vergrößert. Der Wert von y wird von unten nach oben vergrößert.                                                                                                                                                            |
| MM- \_ isotrope   | Jede Einheit im Seitenbereich wird einer Anwendungs definierten Einheit im Gerätespeicher zugeordnet. Die Achsen sind immer gleichmäßig skaliert. Die Ausrichtung der Achsen kann von der Anwendung angegeben werden.                                                                                                                                     |
| MM- \_ loenglish   | Jede Einheit im Seiten Raum wird im Gerätebereich 0,01 Zoll zugeordnet. Der Wert von x wird von links nach rechts vergrößert. Der Wert von y wird von unten nach oben vergrößert.                                                                                                                                                                  |
| MM- \_ lometrisch    | Jede Einheit im Seiten Raum wird im Geräteraum 0,1 Millimeter zugeordnet. Der Wert von x wird von links nach rechts vergrößert. Der Wert von y wird von unten nach oben vergrößert.                                                                                                                                                             |
| MM- \_ Text        | Jede Einheit im Seiten Raum ist einem Pixel zugeordnet. Das heißt, es wird keine Skalierung ausgeführt. Wenn keine Übersetzung aktiviert ist (Dies ist die Standardeinstellung), entspricht der Seitenbereich im mm- \_ Text-Mapping-Modus dem physischen Speicherplatz. Der Wert von x wird von links nach rechts vergrößert. Der Wert von y wird von oben nach unten vergrößert. |
| MM- \_ Twips       | Jede Einheit im Seiten Raum wird einem 20. Punkt eines Drucker Punkts (1/1440 Zoll) zugeordnet. Der Wert von x wird von links nach rechts vergrößert. Der Wert von y wird von unten nach oben vergrößert.                                                                                                                                           |



 

Um einen Zuordnungs Modus festzulegen, müssen Sie die [**setmapmode**](/windows/desktop/api/Wingdi/nf-wingdi-setmapmode) -Funktion aufrufen. Rufen Sie den aktuellen Zuordnungs Modus für einen DC ab, indem Sie die [**getmapmode**](/windows/desktop/api/Wingdi/nf-wingdi-getmapmode) -Funktion aufrufen.

Die Transformationen zwischen Seiten Raum und Geräteraum bestehen aus Werten, die von den Punkten berechnet werden, die durch das Fenster und den Viewport angegeben werden. In diesem Kontext bezieht sich das Fenster auf das logische Koordinatensystem des Seiten Raums, während der Viewport auf das Geräte Koordinatensystem des geräteraums verweist. Das Fenster und der Viewport bestehen jeweils aus einem Ursprung, einem horizontalen ("x") Block und einem vertikalen ("y") Wertebereich). Die Fenster Parameter befinden sich in logischen Koordinaten. der Viewport in Geräte Koordinaten (Pixel). Das System kombiniert die Ursprünge und Blöcke sowohl aus dem Fenster als auch aus dem Viewport, um die Transformation zu erstellen. Dies bedeutet, dass im Fenster und Viewport jeweils die Hälfte der Faktoren angegeben ist, die zum Definieren der Transformation erforderlich sind, mit der Punkte im Seiten Raum dem Gerätespeicher zugeordnet werden. Folglich ordnet das System den Fenster Ursprung dem Viewportursprung zu, und das Fenster wird wie in der folgenden Abbildung dargestellt an die viewportblöcke erweitert.

![Darstellung eines Fenster Ursprungs im Seitenbereich und eines Standpunkt Ursprungs im Geräteraum](images/cstrn-15.png)

Die Blöcke "Fenster" und "Viewport" legen ein Verhältnis oder einen Skalierungsfaktor fest, der im Seiten Raum zu den Transformationen für den Geräteraum verwendet wird. Für die sechs vordefinierten mappingmodi (mm \_ hienglish, mm \_ loenglish, mm \_ HIMETRIC, mm \_ lometrisch, mm \_ Text und mm \_ Twips) werden die Blöcke vom System festgelegt, wenn [**setmapmode**](/windows/desktop/api/Wingdi/nf-wingdi-setmapmode) aufgerufen wird. Sie können nicht geändert werden. Die anderen beiden Karten Modi (mm \_ ISOTROPIC und mm \_ anisotrope) erfordern, dass die Blöcke angegeben werden. Dies erfolgt durch Aufrufen von **setmapmode** , um den entsprechenden Modus festzulegen, und dann die Funktionen [**setwindowextex**](/windows/desktop/api/Wingdi/nf-wingdi-setwindowextex) und [**setviewportextex**](/windows/desktop/api/Wingdi/nf-wingdi-setviewportextex) aufrufen, um die Blöcke anzugeben. Im x- \_ isotrope-Mapping-Modus ist es wichtig, **setwindowextex** vor dem Aufrufen von **setviewportextex** aufzurufen.

Mit den Fenstern "Fenster" und "Viewport" wird die Übersetzung festgelegt, die im Seiten Raum zu den Transformationen für den Geräteraum Legen Sie die Fenster-und viewportursprünge mithilfe der Funktionen [**setwindoworgex**](/windows/desktop/api/Wingdi/nf-wingdi-setwindoworgex) und [**setviewportorgex**](/windows/desktop/api/Wingdi/nf-wingdi-setviewportorgex) fest. Die Ursprünge sind unabhängig von den Blöcken, und eine Anwendung kann Sie unabhängig vom aktuellen Zuordnungsmodus festlegen. Das Ändern eines Zuordnungsmodus wirkt sich nicht auf die aktuell festgelegten Ursprünge aus (obwohl sich dies auf die Blöcke auswirken kann). Ursprünge werden in absoluten Einheiten angegeben, die der aktuelle Mapping-Modus nicht beeinträchtigt. Verwenden Sie zum Ändern der Ursprünge die Funktionen [**offsetwindoworgex**](/windows/desktop/api/Wingdi/nf-wingdi-offsetwindoworgex) und [**offsetviewportorgex**](/windows/desktop/api/Wingdi/nf-wingdi-offsetviewportorgex) .

Die folgende Formel zeigt das mathematische Zeichen, das beim Umrechnen eines Punkts von der Seite in den Gerätebereich beteiligt ist.

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

Dieselbe Gleichung mit y, die x ersetzt, transformiert den y-Komponenten Wert eines Punkts.

Die Formel gibt zuerst den Punkt aus dem Koordinaten Ursprung aus. Dieser Wert, der nicht mehr durch den Ursprung verzerrt ist, wird dann durch das Verhältnis der Blöcke in das Zielkoordinaten System skaliert. Schließlich wird der skalierte Wert durch den Ziel Ursprung auf seine endgültige Zuordnung versetzt.

Die [**lptodp**](/windows/desktop/api/Wingdi/nf-wingdi-lptodp) -und [**dptolp**](/windows/desktop/api/Wingdi/nf-wingdi-dptolp) -Funktionen können verwendet werden, um von logischen Punkten zu gerätepunkten bzw. von gerätepunkten zu logischen Punkten zu konvertieren.

 

 



