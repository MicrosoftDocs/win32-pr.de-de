---
description: Die Anwendung kann mit dem Schablonen Puffer 2D-oder 3D-Bilder in eine 3D-Szene zusammensetzen.
ms.assetid: 9233d15d-fa99-41a2-a253-22f5ae5bf788
title: Zusammensetzung (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01bca61559d2773bd1e4f7dc345e9ad4c1fb6fcb
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106344229"
---
# <a name="compositing-direct3d-9"></a>Zusammensetzung (Direct3D 9)

Die Anwendung kann mit dem Schablonen Puffer 2D-oder 3D-Bilder in eine 3D-Szene zusammensetzen. Eine Maske im Schablone-Puffer wird verwendet, um einen Bereich der Renderingzieloberfläche zu okzieren. Gespeicherte 2D-Informationen, wie z. b. Text oder Bitmaps, können dann in den Bereich "okded" geschrieben werden. Alternativ kann die Anwendung zusätzliche 3D-primitive in den mit der Schablone maskierten Bereich der Renderingzieloberfläche rendern. Sie kann sogar eine ganze Szene darstellen.

Spiele sind häufig mehrere 3D-Szenen zusammengesetzt. Beispielsweise wird bei Fahr spielen in der Regel eine Spiegelung der Rückseite angezeigt. Die Spiegel Datenbank enthält die Ansicht der 3D-Szene hinter dem Treiber. Es handelt sich im Wesentlichen um eine zweite 3D-Szene, die mit der vorwärts Ansicht des Treibers zusammengesetzt wird

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Techniken für Schablonen Puffer](stencil-buffer-techniques.md)
</dt> </dl>

 

 



