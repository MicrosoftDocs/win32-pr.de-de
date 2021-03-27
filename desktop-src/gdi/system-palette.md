---
description: Das System verwaltet für jedes Gerät, das Paletten verwendet, eine Systempalette.
ms.assetid: 4c93ce8c-6b3a-4016-bb47-786c25b93374
title: System Palette
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d8738cf63eef0b77f2d184f2cf95b6550b81053
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104994575"
---
# <a name="system-palette"></a>System Palette

Das System verwaltet für jedes Gerät, das Paletten verwendet, eine *Systempalette* . Die Systempalette enthält die Farbwerte für alle Farben, die derzeit vom Gerät angezeigt oder gezeichnet werden können. Abgesehen von der Anzeige der Inhalte der Systempalette können Anwendungen nicht direkt auf die Systempalette zugreifen. Stattdessen verfügt das System über eine umfassende Kontrolle über die Systempalette und gestattet nur den Zugriff durch die Verwendung logischer Paletten.

Eine Anwendung kann den Inhalt der Systempalette mithilfe der [**getsystempaletteentries**](/windows/desktop/api/Wingdi/nf-wingdi-getsystempaletteentries) -Funktion anzeigen. Diese Funktion Ruft den Inhalt von mindestens einem Eintrag ab, bis zur Gesamtanzahl der Einträge in der Systempalette. Die Summe entspricht immer der Zahl, die von der [**getdebug**](/windows/desktop/api/Wingdi/nf-wingdi-getdevicecaps) -Funktion für den SIZEPALETTE-Wert zurückgegeben wird, und ist mit der maximalen Größe für eine beliebige logische Palette identisch.

Obwohl Anwendungen die Farben in der Systempalette nicht direkt ändern können, können Sie bei der Realisierung logischer Paletten Änderungen verursachen. Zum realisieren einer Palette überprüft das System jede angeforderte Farbe und versucht, einen Eintrag in der Systempalette zu finden, der eine genaue Entsprechung enthält. Wenn das System eine übereinstimmende Farbe findet, ordnet es den Index der logischen Palette dem entsprechenden System Palettenindex zu. Wenn das System keine genaue Entsprechung findet, wird die angeforderte Farbe in einen nicht verwendeten System Paletteneintrag kopiert, bevor die Indizes zugeordnet werden. Wenn alle Systempalette-Einträge verwendet werden, ordnet das System den Index der logischen Palette dem System Paletteneintrag zu, dessen Farbe am ehesten der angeforderten Farbe entspricht. Nachdem diese Zuordnung festgelegt wurde, können Anwendungen Sie nicht mehr überschreiben. Anwendungen können z. b. keine System palettenindizes zum Angeben von Farben verwenden. nur logische palettenindizes sind zulässig.

Anwendungen können die Zuordnung von Indizes ändern, indem Sie den Member " **Peer Flags** " der [**PaletteEntry**](/previous-versions//dd162769(v=vs.85)) -Struktur auf ausgewählte Werte festlegen, wenn Sie die logische Palette erstellen. Beispielsweise weist das Flag "PC \_ nocollapse" das System an, die angeforderte Farbe sofort in einen nicht verwendeten System Paletteneintrag zu kopieren, unabhängig davon, ob ein System Paletteneintrag diese Farbe bereits enthält. Außerdem weist das explizite PC- \_ Flag das System an, den logischen Palettenindex einem explizit gegebenen System Palettenindex zuzuordnen. (Die Anwendung gibt den System Palettenindex im nieder wertigen Wort der **PaletteEntry** -Struktur an.)

Paletten können entweder als Hintergrund Palette oder als Vordergrund Palette erkannt werden, indem " **true** " oder " **false** " für den Parameter " *bForceBackground* " in der [**SelectPalette**](/windows/desktop/api/Wingdi/nf-wingdi-selectpalette) -Funktion angegeben wird. Es darf jeweils nur eine Vordergrund Palette im System vorhanden sein. Wenn das Fenster das derzeit aktive Fenster oder ein Nachfolger des derzeit aktiven Fensters ist, kann es eine Vordergrund Palette erkennen. Andernfalls wird die Palette unabhängig vom Wert des *bForceBackground* -Parameters als Hintergrund Palette erkannt. Die Critical-Eigenschaft einer Vordergrund Palette ist, dass bei der Realisierung alle Einträge (außer den statischen Einträgen) in der Systempalette überschrieben werden können. Dies wird durch das System erreicht, indem alle Einträge, die in der Systempalette nicht statisch sind, vor der Realisierung einer Vordergrund Palette als nicht verwendet markiert werden. Dadurch werden alle verwendeten Einträge eliminiert. In der Systempalette erfolgt keine Vorverarbeitung für die Realisierung einer Hintergrund Palette. Die Vordergrund Palette legt alle möglichen nicht statischen Farben fest. Mit Hintergrund Paletten können nur die verbleibenden Elemente festgelegt werden, die in einer erstmaligen, erstmaligen Bereitstellung und priorisiert werden. In der Regel verwenden Anwendungen Hintergrund Paletten für untergeordnete Fenster, die ihre eigenen Paletten erkennen. Dadurch wird die Anzahl der Änderungen an der Systempalette minimiert.

Ein nicht verwendeter System Paletteneintrag ist ein Eintrag, der nicht reserviert ist und keine statische Farbe enthält. Reservierte Einträge werden explizit mit dem reservierten PC- \_ Wert markiert. Diese Einträge werden erstellt, wenn eine Anwendung eine logische Palette für die palettenanimation erkennt. Statische Farbeinträge werden vom System erstellt und entsprechen den Farben in der Standardpalette. Die [**gettovicecaps**](/windows/desktop/api/Wingdi/nf-wingdi-getdevicecaps) -Funktion kann zum Abrufen des numreserved-Werts verwendet werden, der die Anzahl der für statische Farben reservierten System Paletteneinträge angibt.

Da die Systempalette nur über eine begrenzte Anzahl von Einträgen verfügt, wirkt sich die Auswahl und das Erkennen einer logischen Palette für ein bestimmtes Gerät möglicherweise auf die Farben aus, die anderen logischen Paletten für das gleiche Gerät zugeordnet sind. Diese Farbänderungen sind besonders dramatisch, wenn Sie auf der Anzeige auftreten. Eine Anwendung kann sicherstellen, dass für die aktuell ausgewählte logische Palette sinnvolle Farben verwendet werden, indem Sie die Palette vor jeder Verwendung zurücksetzen. Eine Anwendung setzt die Palette zurück, indem Sie die Funktionen [**UnrealizeObject**](/windows/desktop/api/Wingdi/nf-wingdi-unrealizeobject) und [**RealizePalette**](/windows/desktop/api/Wingdi/nf-wingdi-realizepalette) aufruft. Die Verwendung dieser Funktionen bewirkt, dass das System die Farben in der logischen Palette den angemessenen Farben in der Systempalette zuordnet.

 

 
