---
description: Seitenumkehrung ist bei Multimedia-, Animations- und Spielsoftware von entscheidender Bedeutung. sie entspricht der Art und Weise, wie Sie Animationen mit einem Papierpad erstellen können.
ms.assetid: b6824962-c7cb-4e7f-8731-2971b0d9a2b0
title: Seitenumkehrung und Zurückpufferung (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 134f1797300a838e453abf6811ae35b8f576e46c89ca0e929d2326b43ffea274
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119746930"
---
# <a name="page-flipping-and-back-buffering-direct3d-9"></a>Seitenumkehrung und Zurückpufferung (Direct3D 9)

Seitenumkehrung ist bei Multimedia-, Animations- und Spielsoftware von entscheidender Bedeutung. sie entspricht der Art und Weise, wie Sie Animationen mit einem Papierpad erstellen können. Auf jeder Seite ändert der Interpret die Figur geringfügig, sodass die Zeichnung animiert wird, wenn Sie schnell zwischen den Blättern blättern.

Das Seitenkippen in der Software ähnelt diesem Prozess. Direct3D implementiert Seitenumkehrfunktionen über eine Austauschkette, die eine Eigenschaft des Geräts ist. Zunächst richten Sie eine Reihe von Direct3D-Puffern ein, die so auf den Bildschirm kippen, wie das Papier des Interpreten auf die nächste Seite kippt. Der erste Puffer wird als Farbfrontpuffer bezeichnet. Die Puffer, die sich dahinter befinden, werden als Backpuffer bezeichnet. Ihre Anwendung schreibt in einen Hintergrundpuffer und kippt dann den Farb-Frontpuffer, sodass der Hintergrundpuffer auf dem Bildschirm angezeigt wird. Während das System das Bild anzeigt, schreibt Ihre Software wieder in einen Hintergrundpuffer. Der Prozess wird fortgesetzt, solange Sie sich animieren, sodass Sie Bilder effizient animieren können.

Direct3D erleichtert das Einrichten von Seitenumkehrschemas – von einem einfachen doppelt gepufferten Schema (ein Farb-Frontpuffer mit einem Hintergrundpuffer) bis hin zu komplexeren Schemas mit zusätzlichen Hintergrundpuffern.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Direct3D-Oberflächen](direct3d-surfaces.md)
</dt> <dt>

[Was ist eine Austauschkette? (Direct3D 9)](what-is-a-swap-chain-.md)
</dt> </dl>

 

 



