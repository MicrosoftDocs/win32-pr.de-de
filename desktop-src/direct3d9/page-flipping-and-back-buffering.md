---
description: Das Seiten kippen ist in Multimedia-, Animations-und Spielsoftware ein wichtiger Punkt. Dies entspricht der Art und Weise, wie Sie Animationen mit einem Papierblatt durchführen können.
ms.assetid: b6824962-c7cb-4e7f-8731-2971b0d9a2b0
title: Seiten kippen und zurück Pufferung (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3bffad581c5d4250c7f36980ba1f278a9f770912
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106345582"
---
# <a name="page-flipping-and-back-buffering-direct3d-9"></a>Seiten kippen und zurück Pufferung (Direct3D 9)

Das Seiten kippen ist in Multimedia-, Animations-und Spielsoftware ein wichtiger Punkt. Dies entspricht der Art und Weise, wie Sie Animationen mit einem Papierblatt durchführen können. Auf jeder Seite ändert der Künstler die Abbildung leicht, sodass das Zeichnen beim schnellen kippen zwischen den Blättern animiert erscheint.

Das Seiten kippen in Software ähnelt diesem Prozess. Direct3D implementiert die Seiten flippingfunktion über eine SwapChain, bei der es sich um eine Eigenschaft des Geräts handelt. Zuerst richten Sie eine Reihe von Direct3D-Puffern ein, die so auf den Bildschirm kippen, wie das Papier des Künstlers auf die nächste Seite gedreht wird. Der erste Puffer wird als Farben-Front-Puffer bezeichnet. Die Puffer dahinter werden als backpuffer bezeichnet. Die Anwendung schreibt in einen Hintergrund Puffer und flippt dann den Farben-Front-Puffer, sodass der Hintergrund Puffer auf dem Bildschirm angezeigt wird. Während das System das Abbild anzeigt, schreibt ihre Software erneut in einen Hintergrund Puffer. Der Prozess wird so lange fortgesetzt, wie Sie animieren, sodass Sie Bilder effizient animieren können.

Direct3D erleichtert das Einrichten von Seiten flippingschemas, von einem einfachen, doppelt gepufferten Schema (einem Farb-Front-Puffer mit einem Hintergrund Puffer) bis hin zu komplexeren Schemas mit zusätzlichen backpuffern.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Direct3D-Oberflächen](direct3d-surfaces.md)
</dt> <dt>

[Was ist eine austauschkette? (Direct3D 9)](what-is-a-swap-chain-.md)
</dt> </dl>

 

 



