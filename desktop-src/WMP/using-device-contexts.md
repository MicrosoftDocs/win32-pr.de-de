---
title: Verwenden von Geräte Kontexten
description: Verwenden von Geräte Kontexten
ms.assetid: 2e8de313-6218-4401-a578-73140e7fdae1
keywords:
- Visualisierungen, Gerätekontext
- benutzerdefinierte Visualisierungen, Gerätekontext
- Visualisierungen, Rendering-Funktion
- benutzerdefinierte Visualisierungen, Rendering-Funktion
- Funktion "Rendering", Gerätekontext
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08c315d5004565644750f4adcd099fc165e81575
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310308"
---
# <a name="using-device-contexts"></a>Verwenden von Geräte Kontexten

Der Gerätekontext ist ein Standard Handle für einen Gerätekontext. Sie benötigen dies für viele Zeichnungsfunktionen, damit Microsoft Windows weiß, welches Fenster gezeichnet werden soll. Um z. b. ein Rechteck zu zeichnen, müssen Sie den Gerätekontext angeben.


```C++
HDC hdc;
::Rectangle( hdc, 1, 1, 100, 100 );

```



Der Gerätekontext wird durch die Funktion " **Rendering** " von Windows Media Player angegeben. Wenn das Plug-in mithilfe eines Fensters gerendert wird, müssen Sie den Gerätekontext dieses Fensters verwenden. Verwenden Sie diesen Gerätekontext für ein beliebiges Zeichnungs Tool, das einen Gerätekontext erfordert.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Implementieren von Rendering**](implementing-render.md)
</dt> </dl>

 

 




