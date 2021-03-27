---
description: Pfade werden mithilfe logischer Einheiten und aktueller Transformationen definiert.
ms.assetid: a5a426ec-25e8-4fe1-985c-d078227e8aba
title: Transformationen von Pfaden
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1eb2c033b5769a4edff29beba6cccbd80cfd26de
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980296"
---
# <a name="transformations-of-paths"></a>Transformationen von Pfaden

Pfade werden mithilfe logischer Einheiten und aktueller Transformationen definiert. (Wenn die [**setworldtransform**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform) -Funktion aufgerufen wurde, sind die logischen Einheiten Welteinheiten. andernfalls sind die logischen Einheiten Seiten Einheiten.) Eine Anwendung kann globale Transformationen verwenden, um die Linien und die Bézier-Kurven zu skalieren, zu drehen, zu scheren, zu übersetzen und wiederzugeben, die einen Pfad definieren.

> [!Note]  
> Eine globale Transformation innerhalb einer Pfad Klammer wirkt sich nur auf die Linien und Kurven aus, die nach dem Festlegen der Transformation gezeichnet wurden. Dies hat keine Auswirkung auf die Linien und Kurven, die gezeichnet wurden, bevor Sie festgelegt wurden. Eine Beschreibung der weltweiten Transformation finden Sie unter [Koordinaten Bereiche und Transformationen](coordinate-spaces-and-transformations.md).

 

Eine Anwendung kann auch [**setworldtransform**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform) verwenden, um die Form des Stifts zu gliedern, der verwendet wird, um einen Pfad zu gliedern, wenn der Stift ein geometrischer Stift ist. Eine Beschreibung der geometrischen Stifte finden Sie unter [Stifte](pens.md).

 

 



