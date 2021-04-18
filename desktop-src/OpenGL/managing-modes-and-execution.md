---
title: Verwalten von Modi und Ausführung
description: Verwalten von Modi und Ausführung
ms.assetid: 6a1ecc42-194a-4d8f-94f6-fd59696d87cf
keywords:
- OpenGL, Modi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 427e04b856c79c9adfdfebf4061f7e96f09db835
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106340820"
---
# <a name="managing-modes-and-execution"></a>Verwalten von Modi und Ausführung

Die Auswirkung vieler OpenGL-Funktionen hängt davon ab, ob ein bestimmter Modus wirksam ist. Die Funktionen " [**glEnable**](glenable.md) " und " [**gldeaktivieren**](gldisable.md) " legen solche Modi fest. " [**glisenabled**](glisenabled.md) " bestimmt, ob ein bestimmter Modus festgelegt ist.

Sie können die Ausführung von zuvor ausgestellten OpenGL-Funktionen mit [**glfinish**](glfinish.md)steuern, wodurch alle Funktionen beendet werden, oder [**glflush**](glflush.md), wodurch sichergestellt wird, dass alle diese Funktionen innerhalb einer begrenzten Zeit abgeschlossen werden.

In einer bestimmten Implementierung von OpenGL können Sie möglicherweise bestimmte Verhalten mit Hinweisen mithilfe von [**glhint**](glhint.md)steuern. Solche Verhalten sind die Qualität der Farb-und Texturkoordinaten interpolung. die Genauigkeit von Nebel Berechnungen; und die Stichproben Qualität von Antialiasing Punkten, Linien oder Polygonen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Modi und Ausführungs Verweis](modes-and-execution-reference.md)
</dt> </dl>

 

 




