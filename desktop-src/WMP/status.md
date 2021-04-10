---
title: Status (Windows Media Player SDK)
description: Status
ms.assetid: b8d6d026-819c-4889-a894-c82fe81ec922
keywords:
- Windows Media Player Mobile Skins, Statusanzeige
- Skins, Statusanzeige
- Verweis für Skins, Statusanzeige
- Statusanzeige in Skins, Info
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f6f1cd9e0df209d6a37ed880765fd607e939765
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "104039929"
---
# <a name="status-windows-media-player-sdk"></a>Status (Windows Media Player SDK)

Möglicherweise möchten Sie eine Statusanzeige in der Skin verwenden. Wenn dies der Fall ist, muss das Status-Element in der Skin-Definitionsdatei definiert werden. Als Alternative können Sie diese Informationen auch mithilfe des Status-Attributs im Text-Element anzeigen.

Der Status Abschnitt der Skin-Definitionsdatei beginnt mit der folgenden Zeile:


```C++
[ Status ]

```



Anschließend müssen Sie eine oder mehrere Zeilen hinzufügen, die Informationen über die Statusanzeige in der Skin enthalten.


```C++
    On           45,193,120,13    Left    Tahoma,8,B        0,255,  0

```



Sie können die folgende Vorlage für den Status Abschnitt Ihrer Skin-Definitionsdatei verwenden:


```C++
//  <Item>       <Location>     <Align>  <Font>          <Color>
//  ------       ----------     -------  ------          -------

```



Sie müssen die in der vorangehenden Vorlage gezeigte Reihenfolge für Statusanzeige Informationen für jede Zeile im Abschnitt Status verwenden. Jeder Teil der Zeile ist erforderlich. In den folgenden Abschnitten werden die einzelnen Elemente beschrieben:

-   [Angezeigter Status](status-item.md)
-   [Status Speicherort](status-location.md)
-   [Status Ausrichtung](status-alignment.md)
-   [Status Schriftart](status-font.md)
-   [Status Farbe](status-color.md)

Ein Beispiel für einen Statuscode finden Sie im [Abschnitt Sample Status](sample-status-section.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Skin-Referenz**](skin-reference.md)
</dt> </dl>

 

 




