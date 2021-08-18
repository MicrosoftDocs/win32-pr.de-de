---
title: Automatisches Clipping
description: Automatisches Clipping
ms.assetid: 9107ee47-52aa-48c8-b141-c821f93fda45
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1dabc3fd7ece50250ee9e1fea89ff23dd23db533dfcc90d5a939ce1b563ce764
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118551236"
---
# <a name="automatic-clipping"></a>Automatisches Clipping

Es wird dringend empfohlen, dass ein ActiveX-Steuerelementcontainer das automatische Ausschneiden seiner Steuerelemente unterstützt. Dies führt zu einem effizienteren Betrieb für die meisten Steuerelemente. Wenn automatisches Clipping unterstützt wird, muss die AutoClip-Ambient-Eigenschaft unterstützt werden und den Wert **TRUE** aufweisen.

Automatisches Clipping ist die Fähigkeit eines Containers, sicherzustellen, dass die gezeichnete Ausgabe eines Steuerelements nur an den aktuellen Clippingbereich des Containers geht. In einem Container, der automatisches Clipping unterstützt, kann ein Steuerelement ohne Berücksichtigung seines Clippingbereichs zeichnen, da der Container automatisch alle Zeichnungen ausschneiden wird, die außerhalb des Bereichs des Steuerelements auftreten. Wenn ein Container keinen automatischen Clipping unterstützt, erstellen von CDK generierte Steuerelemente ein zusätzliches übergeordnetes Fenster, wenn ein Clippingbereich ungleich NULL übergeben wird.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Container](containers.md)
</dt> </dl>

 

 




