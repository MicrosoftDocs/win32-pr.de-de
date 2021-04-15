---
title: Lauschen von Attributen
description: Lauschen von Attributen
ms.assetid: 51b10507-5c2e-49ca-b560-6db6a1a7ee87
keywords:
- Windows Media Player Skins, lauschen von Attributen
- Skins, lauschen von Attributen
- Referenz für Skins, lauschen von Attributen
- lauschen von Attributen
- Attribute, lauschen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 349a549966f7fba5ea152f8f0bb002a92f6dfb8e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104515675"
---
# <a name="listening-attributes"></a>Lauschen von Attributen

Ein lauschen-Attribut wird verwendet, um ein Attribut mit einem anderen zu verbinden, sodass sich der Wert jedes Mal ändert, wenn sich der Wert des anderen Attributs ändert.

Das Abhör Attribut **wmpprop:** ist das nützlichste. Wenn der Wert eines Attributs als **wmpprop:** eines zweiten Attributs angegeben ist, wird der erste Wert automatisch aktualisiert, um den zweiten Wert jedes Mal widerzuspiegeln, wenn sich der zweite Wert ändert.

**Beispiel:**


```C++
<TEXT
  value="wmpprop:mySlider.value"
/>

```



Auf diese Weise kann der Wert von myslider, der durch die Position des Schieberegler-Steuer Elements angezeigt wird, auch als Zahl in einem Textfeld angezeigt werden.

Die beiden anderen Überwachungs Attribute **wmpaktivierte:** und **wmpdeaktivierte** Attribute können verwendet werden, um das **aktivierte** Attribut eines Steuer Elements zu ändern, je nachdem, ob seine Funktionalität aktuell im Player verfügbar ist. Diese Attribute können nur auf Methoden des Steuer Elements "Steuer **Elemente** " lauschen.

**Beispiel:**


```C++
<BUTTON 
  id="play" 
  enabled="wmpenabled:player.controls.play"
/>

```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Verschiedenes**](miscellaneous.md)
</dt> </dl>

 

 




