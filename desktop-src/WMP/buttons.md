---
title: Schaltflächen (Windows Media Player SDK)
description: Schaltflächen
ms.assetid: 1212e2d9-e8f8-45d8-8c7f-20865c9c9c94
keywords:
- Windows Media Player Mobile Skins, Übersicht über Schaltflächen
- Skins, Übersicht über Schaltflächen
- Referenz für Skins, Schaltflächen
- Schaltflächen in Skins, Informationen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96128c723c5b8bbac31c82a32060704bc892dfb7
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122885541"
---
# <a name="buttons-windows-media-player-sdk"></a>Schaltflächen (Windows Media Player SDK)

Sie sollten eine oder mehrere Schaltflächen in Ihrer Skin verwenden, und jede Schaltfläche muss in der Skindefinitionsdatei definiert werden. Wenn Sie in diesem Abschnitt keine Schaltfläche definieren, kann Ihre Skin sie nicht verwenden.

Der Abschnitt buttons der Skindefinitionsdatei beginnt mit dieser Zeile:


```C++
[ Buttons ]

```



Anschließend müssen Sie eine oder mehrere Zeilen hinzufügen, die Informationen zu den einzelnen Schaltflächen in Ihrer Skin enthalten. Eine typische Zeile kann sein:


```C++
    PlayPause  2PushHit   84,99,67,67   Pushed @ 44,50    Disabled @ 44,50     0,255,255  Pushed @ 160,5      Pushed @ 160,98

```



Beachten Sie, dass dieser Code als eine Zeile beginnend mit "PlayPause" und endend mit "Pushed @ 160,98" typiert werden sollte.

Sie können die folgende Vorlage für den Abschnitt Schaltfläche ihrer Skindefinitionsdatei verwenden:


```C++
//  <Function> <Type>     <Location>     <Push Image Src> <Dis Image Src>    <Hit R,G,B> <Norm 2 Image Src> <Push 2 Image Src>
//  ---------- ------     ----------     ---------------- ---------------    ----------- ------------------ ------------------

```



Beachten Sie auch hier, dass diese als einzelne Zeilen typiert werden sollten. Die erste beginnt mit "/ Funktion " und endet &lt; &gt; mit " Push &lt; 2 Image Src &gt; ". Die zweite Zeile beginnt mit "/ ----------" und endet mit "------------------."

Schaltflächeninformationen für jede Zeile im Abschnitt Schaltfläche müssen in der folgenden Reihenfolge angezeigt werden. Nur die ersten sechs Teile der Zeile sind erforderlich. Sekundäre Images sind nur enthalten, wenn sie benötigt werden.

1.  [Button-Funktion](button-function.md)
2.  [Schaltflächentyp](button-type.md)
3.  [Schaltflächenposition](button-location.md)
4.  [Pushed Image Source](pushed-image-source.md)
5.  [Bildquelle für deaktivierte Schaltfläche](image-source-for-disabled-button.md)
6.  [Rgb-Farbe treffen](hit-rgb-color.md)
7.  [Normale sekundäre Imagequelle](normal-secondary-image-source.md)
8.  [Normale, tertiäre Bildquelle](normal-tertiary-image-source.md)
9.  [Pushed Secondary Image Source](pushed-secondary-image-source.md)
10. [Pushed Tertiary Image Source](pushed-tertiary-image-source.md)

Ein Beispiel für Schaltflächencode finden Sie im [Abschnitt "Beispielschaltfläche".](sample-button-section.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Skin-Referenz**](skin-reference.md)
</dt> </dl>

 

 




