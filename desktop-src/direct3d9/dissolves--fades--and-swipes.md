---
description: Anwendungen nutzen zunehmend besondere Effekte, die häufig in Filmen und Videos verwendet werden, wie z. b. das Auflösen, wischen und durchlaufen von Anwendungen.
ms.assetid: 6203922f-9594-4e5c-9baa-8b27ac30978f
title: Wird aufgelöst, ausgeblendet und durch Schwenken (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2ad837ea846ca43d61102ce426d415270d2f27f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103746857"
---
# <a name="dissolves-fades-and-swipes-direct3d-9"></a>Wird aufgelöst, ausgeblendet und durch Schwenken (Direct3D 9)

Anwendungen nutzen zunehmend besondere Effekte, die häufig in Filmen und Videos verwendet werden, wie z. b. das Auflösen, wischen und durchlaufen von Anwendungen.

In einer Auflösung wird ein Bild nach und nach durch einen anderen in einer glatten Sequenz von Frames ersetzt. Obwohl Direct3D Methoden zur Verwendung mehrerer Textur Mischungs Funktionen bereitstellt, um denselben Effekt zu erzielen, können Anwendungen, die den Schablonen Puffer für die Auflösung verwenden, Textur Mischungs Funktionen für andere Effekte verwenden, während Sie eine Auflösung durchführen.

Wenn Ihre Anwendung eine Auflösung durchführt, muss Sie zwei unterschiedliche Bilder darstellen. Er verwendet den Schablonen Puffer, um zu steuern, welche Pixel aus jedem Bild auf die Renderingzieloberfläche gezeichnet werden. Sie können eine Reihe von Schablone-Masken definieren und diese bei aufeinander folgenden Frames in den Schablonen Puffer kopieren. Alternativ können Sie eine Basis Schablonen Maske für den ersten Frame definieren und inkrementell ändern.

Am Anfang der Auflösung legt ihre Anwendung die Schablone-und Schablonen Maske fest, sodass die meisten Pixel aus dem Startimage den Schablonen Test bestehen. Die meisten Pixel des endbilds sollten den Schablonen Test nicht bestanden haben. Bei aufeinander folgenden Frames wird die Schablonen Maske so aktualisiert, dass weniger und weniger Pixel im Start Abbild den Test bestehen. Während der Fortschritt des Frames schlägt weniger und weniger der Pixel im Endbild bei dem Test fehl. Auf diese Weise kann die Anwendung mithilfe beliebiger Auflösungs Muster aufgelöst werden.

Das Ausblenden oder Auschecken ist ein Sonderfall der Auflösung. Beim Ausblenden wird der Schablone-Puffer verwendet, um von einem schwarzen oder weißen Bild zu einem Rendering einer 3D-Szene zu lösen. Das Ausblenden ist das Gegenteil, Ihre Anwendung beginnt mit einem Rendering einer 3D-Szene und wird in schwarz oder weiß aufgelöst. Das ausblenden kann mithilfe eines beliebigen Musters erfolgen, das Sie verwenden möchten.

Direct3D-Anwendungen verwenden eine ähnliche Methode für das Schwenken. Wenn eine Anwendung z. b. einen Schwenk von links nach rechts durchführt, wird das Ende Bild nach dem Start Bild von links nach rechts angezeigt. Wie bei einer Auflösung müssen Sie eine Reihe von Schablone-Masken definieren, die bei aufeinander folgenden Frames in den Schablonen Puffer geladen werden, oder die Anfangs Schablone-Maske nacheinander ändern. Die Schablonen Masken werden verwendet, um das Schreiben von Pixeln aus dem Startbild zu deaktivieren und das Schreiben von Pixeln aus dem Endbild zu aktivieren.

Ein Schwenk ist etwas komplexer als eine Auflösung, in der die Anwendung Pixel aus dem Endbild in umgekehrter Reihenfolge des Schwenken lesen muss. Das heißt, wenn der schwenkvorgang von links nach rechts verschoben wird, muss die Anwendung Pixel aus dem Endbild von rechts nach links lesen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Techniken für Schablonen Puffer](stencil-buffer-techniques.md)
</dt> </dl>

 

 



