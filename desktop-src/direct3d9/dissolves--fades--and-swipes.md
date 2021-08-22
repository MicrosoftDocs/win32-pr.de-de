---
description: Anwendungen verwenden zunehmend Sondereffekte, die häufig in Filmen und Videos verwendet werden, wie z. B. Wisch- und Wischabblendungen.
ms.assetid: 6203922f-9594-4e5c-9baa-8b27ac30978f
title: Besen, Ausblenden und Wischen (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc6d6df834ad19fa4b00b6e4706d0884227bc4af33c6a25ec09cba14757e1248
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119607460"
---
# <a name="dissolves-fades-and-swipes-direct3d-9"></a>Besen, Ausblenden und Wischen (Direct3D 9)

Anwendungen verwenden zunehmend Sondereffekte, die häufig in Filmen und Videos verwendet werden, wie z. B. Wisch- und Wischabblendungen.

In einer Ungnabfolge wird ein Bild schrittweise durch ein anderes in einer reibungslosen Sequenz von Frames ersetzt. Obwohl Direct3D Methoden zur Verwendung mehrerer Texturmischungen bietet, um den gleichen Effekt zu erzielen, können Anwendungen, die den Schablonenpuffer für Läufe verwenden, Texturmischungsfunktionen für andere Effekte verwenden, während sie eine Ungnurung erzielen.

Wenn Ihre Anwendung eine Unterschiedliche ausführt, muss sie zwei verschiedene Bilder rendern. Er verwendet den Schablonenpuffer, um zu steuern, welche Pixel von jedem Bild auf die Renderingzieloberfläche gezeichnet werden. Sie können eine Reihe von Schablonenmasken definieren und sie auf nachfolgenden Frames in den Schablonenpuffer kopieren. Alternativ können Sie eine Basis-Schablonenmaske für den ersten Frame definieren und inkrementell ändern.

Am Anfang der Maske legt Ihre Anwendung die Schablonenfunktion und die Schablonenmaske so fest, dass die meisten Pixel aus dem Startbild den Schablonentest bestehen. Die meisten Pixel aus dem Endbild sollten den Schablonentest nicht bestehen. Bei aufeinander folgenden Frames wird die Schablonenmaske aktualisiert, sodass immer weniger Pixel im Startbild den Test bestehen. Im Verlauf der Frames wird der Test immer weniger Pixel im Endbild fehlschlagen. Auf diese Weise kann Ihre Anwendung eine Tränkung mit beliebigen Mustern durchführen.

Das Ein- oder Ausfadieren ist ein Sonderfall der Auflösung. Beim Einfendern wird der Schablonenpuffer verwendet, um von einem schwarz-weißen Bild zu einem Rendering einer 3D-Szene zu werden. Das Verfängnen ist das Gegenteil. Ihre Anwendung beginnt mit dem Rendern einer 3D-Szene und ist schwarz oder weiß. Das Ausblenden kann mit einem beliebigen Muster erfolgen, das Sie verwenden möchten.

Direct3D-Anwendungen verwenden ein ähnliches Verfahren für Wischen. Wenn eine Anwendung z. B. einen Wisch von links nach rechts ausführt, scheint das Endbild allmählich von links nach rechts über das Startbild zu gleiten. Wie bei einer Brille müssen Sie eine Reihe von Schablonenmasken definieren, die in aufeinanderfolgende Frames in den Schablonenpuffer geladen werden, oder die Start-Schablonenmaske nacheinander ändern. Die Schablonenmasken werden verwendet, um das Schreiben von Pixeln aus dem Startbild zu deaktivieren und das Schreiben von Pixeln aus dem Endbild zu ermöglichen.

Ein Wischen ist etwas komplexer als eine Wischung, da Ihre Anwendung Pixel aus dem Endbild in umgekehrter Reihenfolge der Wischung lesen muss. Das heißt, wenn sich der Wisch von links nach rechts bewegt, muss Ihre Anwendung Pixel aus dem Endbild von rechts nach links lesen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Schablonenpuffertechniken](stencil-buffer-techniques.md)
</dt> </dl>

 

 



