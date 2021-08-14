---
title: Testen des Pixelbesitzes
description: Der Pixelbesitztest bestimmt, ob der aktuelle OpenGL-Kontext das Pixel im Framepuffer besitzt, das einem bestimmten Fragment entspricht.
ms.assetid: aa9428a6-cc05-4df4-ba31-444f999006a8
keywords:
- OpenGL-Verarbeitungspipeline, Pixelbesitztest
- Pixelbesitztest OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12cfefe133b3951fa70d51736f664ec5a7cb9942c4c05f892115dd222013f294
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118936249"
---
# <a name="pixel-ownership-test"></a>Testen des Pixelbesitzes

Der Pixelbesitztest bestimmt, ob der aktuelle OpenGL-Kontext das Pixel im Framepuffer besitzt, das einem bestimmten Fragment entspricht. Wenn dies der Schritt ist, wird das Fragment mit dem nächsten Test fortgesetzt. Wenn dies nicht der Fall ist, bestimmt das Fenstersystem, ob das Fragment verworfen wird oder ob weitere Fragmentvorgänge mit diesem Fragment ausgeführt werden. Bei diesem Test steuert das Fenstersystem das Verhalten, wenn z. B. ein OpenGL-Fenster verdeckt wird.

 

 




