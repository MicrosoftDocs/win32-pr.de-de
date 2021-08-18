---
title: Text (Windows Media Player SDK)
description: Text
ms.assetid: 8c10cefb-d0d0-4214-8712-d171a76de95d
keywords:
- Windows Media Player Mobile Skins, Text
- Skins, Text
- Referenz für Skins, Text
- Text in Skins,About
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55027415222516e72df61afab01a14cceb503528467bf329264014c94bf31ed7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118118098"
---
# <a name="text-windows-media-player-sdk"></a>Text (Windows Media Player SDK)

Sie können ein oder mehrere Textanzeigefelder in Ihrer Skin verwenden. Jedes Textanzeigefeld, das Sie verwenden, muss in der Skindefinitionsdatei definiert werden. Wenn Sie in diesem Abschnitt kein Textanzeigefeld definieren, kann Ihr Skin es nicht verwenden.

Der Abschnitt Text der Skindefinitionsdatei beginnt mit dieser Zeile:


```C++
[ Text ]

```



Anschließend müssen Sie eine oder mehrere Zeilen hinzufügen, die Informationen zu den einzelnen Textanzeigefeldern in Ihrer Skin enthalten.


```C++
    Time         180,46,50,30   Right    Tahoma,16,N     255,255,255

```



Sie können die folgende Vorlage für den Abschnitt Text Ihrer Skindefinitionsdatei verwenden:


```C++
//  <Type>       <Location>     <Align> <Font>          <Color>
//  ------       ----------     ------- ------          -------

```



Sie müssen die in der vorherigen Vorlage gezeigte Reihenfolge für Textanzeigefeldinformationen für jede Zeile im Abschnitt Text verwenden. Jeder Teil der Zeile ist erforderlich. In den folgenden Abschnitten wird jedes Element ausführlich beschrieben.

1.  [Texttyp](text-type.md)
2.  [Textposition](text-location.md)
3.  [Textausrichtung](text-alignment.md)
4.  [Textschriftart](text-font.md)
5.  [Textfarbe](text-color.md)

Ein Beispiel für Textcode finden Sie im [Abschnitt Beispieltext](sample-text-section.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Skin-Referenz**](skin-reference.md)
</dt> </dl>

 

 




