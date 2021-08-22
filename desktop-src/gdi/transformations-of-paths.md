---
description: Pfade werden mithilfe von logischen Einheiten und aktuellen Transformationen definiert.
ms.assetid: a5a426ec-25e8-4fe1-985c-d078227e8aba
title: Transformationen von Pfaden
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7561cc1544a49555eaad4d58cf06d29a4763b6cd40528452c68cea551c99af34
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119889000"
---
# <a name="transformations-of-paths"></a>Transformationen von Pfaden

Pfade werden mithilfe von logischen Einheiten und aktuellen Transformationen definiert. (Wenn die [**SetWorldTransform-Funktion**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform) aufgerufen wurde, sind die logischen Einheiten Welteinheiten, andernfalls sind die logischen Einheiten Seiteneinheiten.) Eine Anwendung kann weltliche Transformationen verwenden, um die Linien und Bézierkurven, die einen Pfad definieren, zu skalieren, zu drehen, zu verzerren, zu übersetzen und widerzuspiegeln.

> [!Note]  
> Eine Welttransformation innerhalb einer Pfadklammer wirkt sich nur auf die Linien und Kurven aus, die nach dem Festlegen der Transformation gezeichnet wurden. Sie hat keine Auswirkungen auf die Linien und Kurven, die vor dem Festlegen gezeichnet wurden. Eine Beschreibung der Welttransformation finden Sie unter [Koordinatenräume und Transformationen.](coordinate-spaces-and-transformations.md)

 

Eine Anwendung kann auch [**SetWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform) verwenden, um die Form des Stifts zu umranden, der zum Umranden eines Pfads verwendet wird, wenn der Stift ein geometrischer Stift ist. Eine Beschreibung der geometrischen Stifte finden Sie unter [Stifte.](pens.md)

 

 



