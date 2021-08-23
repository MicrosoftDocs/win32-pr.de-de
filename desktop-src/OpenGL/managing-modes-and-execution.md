---
title: Verwalten von Modi und Ausführung
description: Verwalten von Modi und Ausführung
ms.assetid: 6a1ecc42-194a-4d8f-94f6-fd59696d87cf
keywords:
- OpenGL, Modi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec448fa94c8ed0983be68f8aa1dbbef0974d2e040c4f68b002b026b300406981
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119553980"
---
# <a name="managing-modes-and-execution"></a>Verwalten von Modi und Ausführung

Die Auswirkung vieler OpenGL-Funktionen hängt davon ab, ob ein bestimmter Modus aktiviert ist. Die [**Funktionen glEnable**](glenable.md) und [**glDisable**](gldisable.md) legen solche Modi fest. [**glIsEnabled**](glisenabled.md) bestimmt, ob ein bestimmter Modus festgelegt ist.

Sie können die Ausführung von zuvor ausgegebenen OpenGL-Funktionen mit [**glFinish**](glfinish.md)steuern, wodurch der Abschluss aller dieser Funktionen erzwingt wird, oder [**glFlush,**](glflush.md)wodurch sichergestellt wird, dass alle diese Funktionen in einer begrenzten Zeit abgeschlossen werden.

In einer bestimmten Implementierung von OpenGL können Sie möglicherweise bestimmte Verhaltensweisen mit Hinweisen steuern, indem Sie [**glHint verwenden.**](glhint.md) Solche Verhaltensweisen sind die Qualität der Farb- und Texturkoordinateninterpolation. Die Genauigkeit von Berechnungen von Berechnungen; und die Stichprobenqualität von Antialiasingpunkten, Linien oder Polygonen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Modi und Ausführungsreferenz](modes-and-execution-reference.md)
</dt> </dl>

 

 




