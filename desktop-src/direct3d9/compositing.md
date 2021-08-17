---
description: Ihre Anwendung kann den Schablonenpuffer verwenden, um 2D- oder 3D-Bilder in einer 3D-Szene zusammenzufügen.
ms.assetid: 9233d15d-fa99-41a2-a253-22f5ae5bf788
title: Compositing (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9dd6d11f98a5913c32d8f71385ce9b15ab5e7047c4db8394d5b0decee87f7f7d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119123387"
---
# <a name="compositing-direct3d-9"></a>Compositing (Direct3D 9)

Ihre Anwendung kann den Schablonenpuffer verwenden, um 2D- oder 3D-Bilder in einer 3D-Szene zusammenzufügen. Eine Maske im Schablonenpuffer wird verwendet, um einen Bereich der Renderingzieloberfläche auszublenden. Gespeicherte 2D-Informationen, z. B. Text oder Bitmaps, können dann in den verdeckten Bereich geschrieben werden. Alternativ kann Ihre Anwendung zusätzliche 3D-Primitive in den schablonenmaskierten Bereich der Renderingzieloberfläche rendern. Es kann sogar eine ganze Szene rendern.

Spiele kombinierten häufig mehrere 3D-Szenen. Beispielsweise zeigen Fahrspiele in der Regel einen Rückspiegel an. Der Spiegel enthält die Ansicht der 3D-Szene hinter dem Treiber. Es handelt sich im Wesentlichen um eine zweite 3D-Szene, die mit der Vorwärtsansicht des Treibers zusammengesetzt ist.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Schablonenpuffertechniken](stencil-buffer-techniques.md)
</dt> </dl>

 

 



