---
title: Album Kunst
description: Album Kunst
ms.assetid: a5996232-e1ee-41ae-a6ca-f841321644fe
keywords:
- Windows Media Player Mobile Skins, Albumkunst
- Skins, Albumkunst
- Referenz für Skins, Albumkunst
- kunstdateien für Skins, Albumkunst
- Albumkunst in Skins
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0974f8683da98469e75a4472d086dcb1a244c75
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106342045"
---
# <a name="album-art"></a>Album Kunst

Wenn Sie ein Skin für Windows Media Player 10 Mobile oder höher erstellen, empfiehlt es sich, albumgrafiken anzuzeigen, die sich auf das aktuell wiedergegebene Medien Element beziehen. Wenn Sie Ihre Skin entwerfen, sollten Sie Platz im Hintergrundbild reservieren, um die Albumkunst zu enthalten.

Der Abschnitt "Album-Art" der Skin-Definitionsdatei muss mit der folgenden Zeile beginnen:


```C++
[ Album Art ]

```



Anschließend müssen Sie Informationen hinzufügen, die den Speicherort und die Größe der albumgrafiken in der Skin angeben. Sie müssen vier positive ganze Zahlen eingeben, getrennt durch Kommas, die die linke, obere, Breite und Höhe der Art des Albums in Pixel relativ zum Hintergrundbild definieren. Im folgenden Beispiel wird gezeigt, wie Dimensionen angegeben werden:


```C++
//  <Location>
//  ----------
   5,37,230,155

```



Wenn Sie planen, einen Video Abschnitt in der Skin einzuschließen, können Sie die gleiche Größe und den gleichen Speicherort für Ihre Albumkunst verwenden, um Platz zu sparen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Skin-Referenz**](skin-reference.md)
</dt> </dl>

 

 




