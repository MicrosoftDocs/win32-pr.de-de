---
title: Lauschende Attribute
description: Lauschende Attribute
ms.assetid: 51b10507-5c2e-49ca-b560-6db6a1a7ee87
keywords:
- Windows Media Player skins,listening attributes
- Skins, lauschende Attribute
- Referenz für Skins, Lauschen von Attributen
- Lauschende Attribute
- Attribute, lauschend
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8cceb9a8721995c494b5e4366291353376a2569c045e41eb41c1418e2f4d5ea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118996410"
---
# <a name="listening-attributes"></a>Lauschende Attribute

Ein lauschende Attribut wird verwendet, um ein Attribut mit einem anderen zu verbinden, sodass sich sein Wert jedes Mal ändert, wenn sich der Wert des anderen Attributs ändert.

Das lauschende **Attribut wmpprop:** ist am nützlichsten. Wenn der Wert eines Attributs als **wmpprop:** eines zweiten Attributs angegeben wird, wird der erste Wert automatisch aktualisiert, um bei jeder Änderung des zweiten Werts den zweiten Wert widerzuenkennen.

**Beispiel:**


```C++
<TEXT
  value="wmpprop:mySlider.value"
/>

```



Auf diese Weise kann der Wert von mySlider, der durch die Position des Schieberegler-Steuerelements angezeigt wird, auch als Zahl in einem Textfeld angezeigt werden.

Die beiden anderen Lauschattribute **wmpenabled:** und **wmpdisabled:** können  verwendet werden, um das aktivierte Attribut eines Steuerelements abhängig davon zu ändern, ob seine Funktionalität derzeit im Player verfügbar ist. Diese Attribute können nur auf Methoden des **Controls-Objekts** lauschen.

**Beispiel:**


```C++
<BUTTON 
  id="play" 
  enabled="wmpenabled:player.controls.play"
/>

```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**verschiedene gefährliche Stoffe**](miscellaneous.md)
</dt> </dl>

 

 




