---
description: Direct3D-Anwendungen verwenden die Dekalierung, um zu steuern, welche Pixel von einem bestimmten primitiven Bild auf die Renderingzieloberfläche gezeichnet werden. Anwendungen wenden Abschärfungen auf die Bilder von Primitiven an, damit koplanare Polygone ordnungsgemäß gerendert werden können.
ms.assetid: 0d57983c-c8f3-4095-9495-a3ec5d280bda
title: Dekalierung (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e16b07eefcbf43bf2a3c71deb1a1073a656bb8d637696af71484a7a3e478ff8c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117910216"
---
# <a name="decaling-direct3d-9"></a>Dekalierung (Direct3D 9)

Direct3D-Anwendungen verwenden die Dekalierung, um zu steuern, welche Pixel von einem bestimmten primitiven Bild auf die Renderingzieloberfläche gezeichnet werden. Anwendungen wenden Abschärfungen auf die Bilder von Primitiven an, damit koplanare Polygone ordnungsgemäß gerendert werden können.

Wenn Sie z. B. Reifenmarkierungen und gelbe Linien auf eine Straße anwenden, sollten die Markierungen direkt über der Straße angezeigt werden. Die z-Werte der Markierungen und der Straße sind jedoch identisch. Daher erzeugt der Tiefenpuffer möglicherweise keine saubere Trennung zwischen den beiden. Einige Pixel im primitiven Hintergrundtyp werden möglicherweise über dem primitiven Anfang und umgekehrt gerendert. Das resultierende Bild scheint von Frame zu Frame zu schrumpfen. Dieser Effekt wird als *Z-Fighting oder* *Flimmering bezeichnet.*

Um dieses Problem zu beheben, verwenden Sie eine Schablone, um den Abschnitt des Hintergrundprimitiven zu maskieren, in dem die Decal angezeigt wird. Deaktivieren Sie die Z-Pufferung, und rendern Sie das Bild des primitiven Front-Primitivs im maskierten Bereich der Renderzieloberfläche.

Obwohl mehrere Texturmischungen verwendet werden können, um dieses Problem zu lösen, schränkt dies die Anzahl anderer Sondereffekte ein, die Ihre Anwendung erzeugen kann. Durch die Verwendung des Schablonenpuffers zum Anwenden von Decals werden Texturmischungsphasen für andere Effekte frei.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Schablonenpuffertechniken](stencil-buffer-techniques.md)
</dt> </dl>

 

 



