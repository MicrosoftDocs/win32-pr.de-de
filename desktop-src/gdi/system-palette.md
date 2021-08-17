---
description: Das System verwaltet eine Systempalette für jedes Gerät, das Paletten verwendet.
ms.assetid: 4c93ce8c-6b3a-4016-bb47-786c25b93374
title: Systempalette
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e540bd4068989a3c457568c2451dbc91f77755065f3bc70af03f9577fcebee9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117698132"
---
# <a name="system-palette"></a>Systempalette

Das System verwaltet eine *Systempalette für* jedes Gerät, das Paletten verwendet. Die Systempalette enthält die Farbwerte für alle Farben, die derzeit vom Gerät angezeigt oder gezeichnet werden können. Anwendungen können nicht nur den Inhalt der Systempalette anzeigen, sondern können nicht direkt auf die Systempalette zugreifen. Stattdessen hat das System die vollständige Kontrolle über die Systempalette und lässt den Zugriff nur über die Verwendung logischer Paletten zu.

Eine Anwendung kann den Inhalt der Systempalette mithilfe der [**GetSystemPaletteEntries-Funktion**](/windows/desktop/api/Wingdi/nf-wingdi-getsystempaletteentries) anzeigen. Diese Funktion ruft den Inhalt eines oder mehrere Einträge bis zur Gesamtzahl der Einträge in der Systempalette ab. Der Gesamtwert entspricht immer der Zahl, die von der [**GetDeviceCaps-Funktion**](/windows/desktop/api/Wingdi/nf-wingdi-getdevicecaps) für den SIZEPALETTE-Wert zurückgegeben wird, und entspricht der maximalen Größe für jede bestimmte logische Palette.

Obwohl Anwendungen die Farben in der Systempalette nicht direkt ändern können, können sie änderungen verursachen, wenn logische Paletten realisiert werden. Um eine Palette zu realisieren, überprüft das System jede angeforderte Farbe und versucht, einen Eintrag in der Systempalette zu finden, der eine genaue Übereinstimmung enthält. Wenn das System eine übereinstimmende Farbe findet, ordnet es den logischen Palettenindex dem entsprechenden Systempalettenindex zu. Wenn das System keine genaue Übereinstimmung findet, kopiert es die angeforderte Farbe in einen nicht verwendeten Systempaletteneintrag, bevor die Indizes zuordnungsweise erstellt werden. Wenn alle Systempaletteneinträge verwendet werden, ordnet das System den logischen Palettenindex dem Systempaletteneintrag zu, dessen Farbe der angeforderten Farbe am besten entspricht. Nachdem diese Zuordnung festgelegt wurde, können Anwendungen sie nicht überschreiben. Beispielsweise können Anwendungen keine Systempalettenindizes verwenden, um Farben anzugeben. nur logische Palettenindizes sind zulässig.

Anwendungen können die Zuordnung von Indizes ändern, indem sie das **peFlags-Element** der [**PALETTEENTRY-Struktur**](/previous-versions//dd162769(v=vs.85)) beim Erstellen der logischen Palette auf ausgewählte Werte festlegen. Das PC NOCOLLAPSE-Flag z. B. leitet das System an, die angeforderte Farbe sofort in einen nicht verwendeten Systempaletteneintrag zu kopieren, unabhängig davon, ob ein Systempaletteneintrag diese Farbe bereits \_ enthält. Außerdem weist das PC EXPLICIT-Flag das System an, den logischen Palettenindex einem \_ explizit angegebenen Systempalettenindex zu zuordnen. (Die Anwendung gibt den Systempalettenindex im niedrig geordneten Wort der **PALETTEENTRY-Struktur** an.)

Paletten können entweder als Hintergrundpalette oder als Vordergrundpalette realisiert werden, indem **SIE TRUE** bzw. **FALSE** für den *bForceBackground-Parameter* in der [**SelectPalette-Funktion**](/windows/desktop/api/Wingdi/nf-wingdi-selectpalette) angeben. Es kann immer nur eine Vordergrundpalette im System gleichzeitig geben. Wenn das Fenster das derzeit aktive Fenster oder ein absteigender Teil des derzeit aktiven Fensters ist, kann eine Vordergrundpalette realisiert werden. Andernfalls wird die Palette als Hintergrundpalette unabhängig vom Wert des *bForceBackground-Parameters* realisiert. Die kritische Eigenschaft einer Vordergrundpalette ist, dass sie alle Einträge (mit Ausnahme der statischen Einträge) in der Systempalette überschreiben kann, wenn sie erkannt wird. Das System erreicht dies, indem alle Einträge, die in der Systempalette nicht statisch sind, vor der Umsetzung einer Vordergrundpalette als nicht verwendet markiert werden, wodurch alle verwendeten Einträge beseitigt werden. Für eine Hintergrundpalette wird in der Systempalette keine Vorverarbeitung ausgeführt. Die Vordergrundpalette legt alle möglichen nicht statischen Farben fest. Hintergrundpaletten können nur festlegen, was offen bleibt und auf eine Art first-come, first-serve priorisiert wird. In der Regel verwenden Anwendungen Hintergrundpaletten für untergeordnete Fenster, die ihre eigenen individuellen Paletten realisieren. Dadurch wird die Anzahl der Änderungen an der Systempalette minimiert.

Ein nicht verwendeter Systempaletteneintrag ist ein Eintrag, der nicht reserviert ist und keine statische Farbe enthält. Reservierte Einträge werden explizit mit dem WERT FÜR \_ RESERVIERTE PCs gekennzeichnet. Diese Einträge werden erstellt, wenn eine Anwendung eine logische Palette für die Palettenanimation realisiert. Statische Farbeinträge werden vom System erstellt und entsprechen den Farben in der Standardpalette. Die [**GetDeviceCaps-Funktion**](/windows/desktop/api/Wingdi/nf-wingdi-getdevicecaps) kann verwendet werden, um den NUMRESERVED-Wert abzurufen, der die Anzahl von Systempaletteneinträgen angibt, die für statische Farben reserviert sind.

Da die Systempalette über eine begrenzte Anzahl von Einträgen verfügt, kann sich das Auswählen und Realisieren einer logischen Palette für ein bestimmtes Gerät auf die Farben auswirken, die anderen logischen Paletten für dasselbe Gerät zugeordnet sind. Diese Farbänderungen sind besonders drastisch, wenn sie auf der Anzeige auftreten. Eine Anwendung kann sicherstellen, dass für die aktuell ausgewählte logische Palette angemessene Farben verwendet werden, indem sie die Palette vor jeder Verwendung zurücksetzen. Eine Anwendung setzt die Palette zurück, indem sie die [**Funktionen UnrealizeObject**](/windows/desktop/api/Wingdi/nf-wingdi-unrealizeobject) und [**RealizePalette**](/windows/desktop/api/Wingdi/nf-wingdi-realizepalette) aufruft. Die Verwendung dieser Funktionen bewirkt, dass das System die Farben in der logischen Palette den angemessenen Farben in der Systempalette neu zuweise.

 

 
