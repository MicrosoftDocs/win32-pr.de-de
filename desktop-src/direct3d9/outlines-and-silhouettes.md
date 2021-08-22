---
description: Sie können den Schablonenpuffer für abstraktere Effekte wie Lining und Silhouetting verwenden.
ms.assetid: 8b9cd2b3-c1bf-4ac9-aae5-7fc0c9e049ff
title: Konturen und Gliederungen (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45b5fcf26b3f3cbbe6e051e1a7d8517cc6d69044beb6eaed7f54baef3509a748
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119563410"
---
# <a name="outlines-and-silhouettes-direct3d-9"></a>Konturen und Gliederungen (Direct3D 9)

Sie können den Schablonenpuffer für abstraktere Effekte wie Lining und Silhouetting verwenden.

Wenn Ihre Anwendung eine Schablonenmaske auf das Bild eines Primitivs wendet, das dieselbe Form, aber etwas kleiner ist, enthält das resultierende Bild nur die Kontur des Primitivs. Die Anwendung kann dann den mit Schablonen maskierten Bereich des Bilds mit einer Volltonfarbe füllen, was dem Primitiv ein einbettes Aussehen gibt.

Wenn die Schablonenmaske die gleiche Größe und Form wie die primitive Maske hat, die Sie rendern, enthält das resultierende Bild eine Lücke, in der sich das Primitive befinden sollte. Ihre Anwendung kann dann die Lücke mit Schwarz füllen, um eine Primprimitive zu erzeugen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Schablonenpuffertechniken](stencil-buffer-techniques.md)
</dt> </dl>

 

 



