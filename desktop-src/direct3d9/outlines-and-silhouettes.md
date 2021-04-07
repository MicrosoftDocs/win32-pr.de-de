---
description: Sie können den Schablonen Puffer für abstraktere Effekte verwenden, z. b. Gliederung und Silhouette.
ms.assetid: 8b9cd2b3-c1bf-4ac9-aae5-7fc0c9e049ff
title: Kontur und Silhouetten (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46a282b650b96cdbb36dc252e1f31cb81d91f0bb
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103745536"
---
# <a name="outlines-and-silhouettes-direct3d-9"></a>Kontur und Silhouetten (Direct3D 9)

Sie können den Schablonen Puffer für abstraktere Effekte verwenden, z. b. Gliederung und Silhouette.

Wenn Ihre Anwendung eine Schablone-Maske auf das Bild eines primitiven anwendet, das dieselbe Form aufweist, aber etwas kleiner ist, enthält das resultierende Bild nur den Umriss des primitiven. Die Anwendung kann dann den Bereich der Schablone maskiert mit einer voll Tonfarbe ausfüllen, wodurch dem primitiven ein geprägte Bild angezeigt wird.

Wenn die Schablone-Maske dieselbe Größe und Form wie das primitive-Format aufweist, das Sie rendern, enthält das resultierende Bild eine Lücke, in der der primitive entsprechen sollte. Die Anwendung kann dann das Loch mit Black auffüllen, um eine Silhouette des primitiven zu schaffen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Techniken für Schablonen Puffer](stencil-buffer-techniques.md)
</dt> </dl>

 

 



