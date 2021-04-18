---
title: Altersfreigabe
description: Altersfreigabe
ms.assetid: babc9db5-2782-4261-a571-acb7be4ea770
keywords:
- Windows Media Player Mobile Skins, BEWERTUNGEN
- Skins, BEWERTUNGEN
- Referenz für Skins, BEWERTUNGEN
- Bewertungen in Skins
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: edb90908c725fcb525e0be1547c27c588a4220c6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106337384"
---
# <a name="ratings"></a>Altersfreigabe

Wenn Sie ein Skin für Windows Media Player 10,1 Mobile erstellen, können Sie die Bewertung anzeigen, die Windows Media Audio-basierten, derzeit wiedergegebenen Inhalt zugeordnet ist. Die Bewertung wird als Stern mit einer Zahl angezeigt. Der Stern wird um eins bis fünf nummeriert, was die aktuelle Bewertung für diesen Inhalt anzeigt. Wenn der Inhalt nicht bewertet wird, wird der Stern mit 0 nummeriert.

Der bewertungsabschnitt der Skin-Definitionsdatei beginnt mit der folgenden Zeile:


```C++
[ Ratings ]

```



Anschließend müssen Sie eine Zeile hinzufügen, die Informationen über die Größe und den Speicherort Ihres Bewertungs Symbols in der Skin enthält.


```C++
147, 3, 22, 21       ratings96S.gif

```



Sie können die folgende Vorlage für den bewertungsabschnitt ihrer Skin-Definitionsdatei verwenden:


```C++
// <Location>           <Image>
// ---------------      --------------------
```



Sie können einem Medien Element auch über die Benutzeroberfläche in Windows Media Player 10,1 Mobile einen Bewertungs Wert zuweisen. wenn das Gerät das nächste Mal mit einem Computer synchronisiert wird, wird der neue Bewertungs Wert an das Medien Element weitergegeben, wenn es sich in der Windows Media Player 10-Bibliothek befindet.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Skin-Referenz**](skin-reference.md)
</dt> </dl>

 

 




