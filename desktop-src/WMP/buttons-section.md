---
title: Schaltflächen Abschnitt
description: Schaltflächen Abschnitt
ms.assetid: fa413bb4-e04a-4e3d-9754-cd4c2d82de6e
keywords:
- Windows Media Player Mobile Skins, Schaltflächen Abschnitt
- Skins, Schaltflächen Abschnitt
- Erstellen von Skins, Schaltflächen Abschnitt
- Schreiben von Code für Skins, Schaltflächen (Abschnitt)
- Schaltflächen im Bereich "Skins", Schaltflächen
- Skin-Definitions Dateien, Schaltflächen Abschnitt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f994225154e3f4cc55070351c32c654d5ad616c1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037182"
---
# <a name="buttons-section"></a>Schaltflächen Abschnitt

Als nächstes müssen Sie die Schaltflächen definieren, die Sie verwenden werden:


```C++
[ Buttons ]

//  <Function> <Type>     <Location>     <Push Image Src>  <Dis Image Src>    <Hit R,G,B>  <Norm 2 Image Src>  <Push 2 Image Src>
//  ---------- ------     ----------     ----------------  ---------------    -----------  ------------------  ------------------
    PlayPause  2PushHit   100,20,110,100 Pushed @ 100,20   Disabled @ 100,20    0,255,255  Pushed @ 270,20     Pushed @ 270,130
    Stop       PushHit    20,20,45,45    Pushed @ 20,20    Disabled @ 20,20   255,255,  0
    Next       PushHit    20,80,45,45    Pushed @ 20,80    Disabled @ 20,80   255,  0,  0
    Prev       PushHit    20,140,45,45   Pushed @ 20,140   Disabled @ 20,130    0,  0,255

```



In diesem Abschnitt sind vier Schaltflächen definiert. Diese Zeilen können von der Seite, die Sie anzeigen, umschlossen werden, aber wenn Sie den Code eingeben, dürfen Sie keine Zeilen umschließen. Das heißt, jede Zeile muss abgeschlossen sein und mit einer Absatz Markierung enden.

> [!Note]  
> Schaltflächen Typen sind in Windows Media Player 10 Mobile oder höher als veraltet markiert. Geben Sie anstelle eines in der Skin-Datei deklarierten Schaltflächen Typs für jeden Typ "na" ein.

 

Für jede Schaltfläche müssen Sie die Funktion, den Typ, den Speicherort, die gedrückte Bildquelle, die deaktivierte Quelle und die Farbe (für die Schaltflächen "Treffer") definieren Außerdem müssen Sie für die Schaltfläche "PLAYPAUSE" die normalen und per pushübertragung übertragenen Bildquellen für den angehaltenen Zustand definieren.

Weitere Informationen zum Schaltflächen Abschnitt der Skin-Definitionsdatei finden Sie unter [Schalt](buttons.md) Flächen in der Skin-Referenz.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Schreiben des Codes**](writing-the-code.md)
</dt> </dl>

 

 




