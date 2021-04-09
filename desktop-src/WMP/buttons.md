---
title: Schaltflächen (Windows Media Player SDK)
description: Schaltflächen
ms.assetid: 1212e2d9-e8f8-45d8-8c7f-20865c9c9c94
keywords:
- Windows Media Player Mobile Skins, Schaltflächen Übersicht
- Skins, Schaltflächen Übersicht
- Verweis für Skins, Schaltflächen
- Schaltflächen in Skins, Info
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0f06eb2fe21ee18a24f92e92d4fa760e9c76887
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "104102758"
---
# <a name="buttons-windows-media-player-sdk"></a>Schaltflächen (Windows Media Player SDK)

Sie möchten eine oder mehrere Schaltflächen in der Skin verwenden, und jede Schaltfläche muss in der Skin-Definitionsdatei definiert werden. Wenn Sie in diesem Abschnitt keine Schaltfläche definieren, kann Sie von der Skin nicht verwendet werden.

Der Schaltflächen Abschnitt der Skin-Definitionsdatei beginnt mit der folgenden Zeile:


```C++
[ Buttons ]

```



Anschließend müssen Sie eine oder mehrere Zeilen hinzufügen, die Informationen zu den einzelnen Schaltflächen in der Skin enthalten. Eine typische Zeile könnte wie folgt lauten:


```C++
    PlayPause  2PushHit   84,99,67,67   Pushed @ 44,50    Disabled @ 44,50     0,255,255  Pushed @ 160,5      Pushed @ 160,98

```



Beachten Sie, dass dieser Code als eine Zeile typisiert werden muss, die mit "PLAYPAUSE" beginnt und mit "Pushvorgang @ 160, 98" endet.

Sie können die folgende Vorlage für den Schaltflächen Abschnitt Ihrer Skin-Definitionsdatei verwenden:


```C++
//  <Function> <Type>     <Location>     <Push Image Src> <Dis Image Src>    <Hit R,G,B> <Norm 2 Image Src> <Push 2 Image Src>
//  ---------- ------     ----------     ---------------- ---------------    ----------- ------------------ ------------------

```



Beachten Sie, dass diese als einzelne Zeilen eingegeben werden müssen, wobei der erste mit "// <Function> " beginnt und mit " &lt; Push 2 Image src &gt; " endet. Die zweite Zeile beginnt mit "//----------" und endet mit "------------------.".

Die Schaltflächen Informationen für jede Zeile im Schaltflächen Abschnitt müssen in der folgenden Reihenfolge angezeigt werden. Nur die ersten sechs Teile der Zeile sind erforderlich. Sekundäre Images sind nur enthalten, wenn Sie benötigt werden.

1.  [Button-Funktion](button-function.md)
2.  [Schalt Flächentyp](button-type.md)
3.  [Schaltflächen Position](button-location.md)
4.  [Bildquelle mit pushübertragung](pushed-image-source.md)
5.  [Bildquelle für deaktivierte Schaltfläche](image-source-for-disabled-button.md)
6.  [RGB-Farbe](hit-rgb-color.md)
7.  [Normale sekundäre Image Quelle](normal-secondary-image-source.md)
8.  [Normale tertiäre Image Quelle](normal-tertiary-image-source.md)
9.  [Quelle für das sekundäre Image](pushed-secondary-image-source.md)
10. [Quelle für tertiäres Image übermittelt](pushed-tertiary-image-source.md)

Ein Beispiel für einen Schaltflächen Code finden Sie im [Abschnitt Sample Button](sample-button-section.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Skin-Referenz**](skin-reference.md)
</dt> </dl>

 

 




