---
description: Direct3D-Anwendungen verwenden die-Verwendung, um zu steuern, welche Pixel von einem bestimmten primitiven Bild auf die Renderingzieloberfläche gezeichnet werden. Anwendungen wenden die Abbilder von primitiven an, damit Coplanar-Polygone ordnungsgemäß wieder hergestellt werden können.
ms.assetid: 0d57983c-c8f3-4095-9495-a3ec5d280bda
title: Wird abgebrochen (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5606bdbc798d8b1e834aff53b04984f659af650
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104123877"
---
# <a name="decaling-direct3d-9"></a>Wird abgebrochen (Direct3D 9)

Direct3D-Anwendungen verwenden die-Verwendung, um zu steuern, welche Pixel von einem bestimmten primitiven Bild auf die Renderingzieloberfläche gezeichnet werden. Anwendungen wenden die Abbilder von primitiven an, damit Coplanar-Polygone ordnungsgemäß wieder hergestellt werden können.

Wenn beispielsweise Reifen Markierungen und gelbe Linien auf eine Straßenebene angewendet werden, sollten die Markierungen direkt auf der Straße angezeigt werden. Die z-Werte der Markierungen und der Straße sind jedoch identisch. Daher erzeugt der tiefen Puffer möglicherweise keine saubere Trennung zwischen den beiden. Einige Pixel im Hintergrundtyp können über dem Front-primitiv und umgekehrt gerendert werden. Das resultierende Bild wird angezeigt, um von Frame zu Rahmen zu vershicheln. Dieser Effekt heißt *z-Fighting* oder *Flimmern*.

Um dieses Problem zu beheben, verwenden Sie eine Schablone, um den Abschnitt des hintergrundprimitivs zu maskieren, in dem die Client Zugriffslizenz angezeigt wird. Deaktivieren Sie die z-Pufferung, und Renderern Sie das Bild des Front-Primitivs in den maskierten Bereich der Renderziel-Oberfläche.

Obwohl mehrere Textur Mischungs Möglichkeiten verwendet werden können, um dieses Problem zu lösen, schränkt dies die Anzahl anderer spezieller Effekte ein, die Ihre Anwendung erzeugen kann. Wenn Sie den Schablonen Puffer zum Anwenden von Decals verwenden, werden Textur Mischungs Phasen für andere Effekte freigegeben.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Techniken für Schablonen Puffer](stencil-buffer-techniques.md)
</dt> </dl>

 

 



