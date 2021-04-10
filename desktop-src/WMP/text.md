---
title: Text (Windows Media Player SDK)
description: Text
ms.assetid: 8c10cefb-d0d0-4214-8712-d171a76de95d
keywords:
- Windows Media Player Mobile Skins, Text
- Skins, Text
- Verweis für Skins, Text
- Text in Skins, Info
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c801d93698bc7a17eea34df71514dd88b485f0d9
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "103858614"
---
# <a name="text-windows-media-player-sdk"></a>Text (Windows Media Player SDK)

Möglicherweise möchten Sie ein oder mehrere Textanzeige Felder in der Skin verwenden. Jedes verwendete Textanzeige Feld muss in der Skin-Definitionsdatei definiert werden. Wenn Sie in diesem Abschnitt kein Textfeld für die Anzeige definieren, kann es von der Skin nicht verwendet werden.

Der Text Abschnitt der Skin-Definitionsdatei beginnt mit der folgenden Zeile:


```C++
[ Text ]

```



Sie müssen dann mindestens eine Zeile hinzufügen, die Informationen zu jedem der Textanzeige Felder in der Skin enthält.


```C++
    Time         180,46,50,30   Right    Tahoma,16,N     255,255,255

```



Sie können die folgende Vorlage für den Text Abschnitt der Skin-Definitionsdatei verwenden:


```C++
//  <Type>       <Location>     <Align> <Font>          <Color>
//  ------       ----------     ------- ------          -------

```



Sie müssen die in der vorangehenden Vorlage gezeigte Reihenfolge für Textanzeige Feldinformationen für jede Zeile im Textabschnitt verwenden. Jeder Teil der Zeile ist erforderlich. In den folgenden Abschnitten werden die einzelnen Elemente ausführlich beschrieben.

1.  [Texttyp](text-type.md)
2.  [Text Speicherort](text-location.md)
3.  [Text Ausrichtung](text-alignment.md)
4.  [Text Schriftart](text-font.md)
5.  [Textfarbe](text-color.md)

Ein Beispiel für Textcode finden Sie unter [Sample Text section](sample-text-section.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Skin-Referenz**](skin-reference.md)
</dt> </dl>

 

 




