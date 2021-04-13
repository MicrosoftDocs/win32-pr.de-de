---
title: Automatisches Abschneiden
description: Automatisches Abschneiden
ms.assetid: 9107ee47-52aa-48c8-b141-c821f93fda45
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71fb39f3a9f15ed6e1e96493ed2cbdd62db40403
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310676"
---
# <a name="automatic-clipping"></a>Automatisches Abschneiden

Es wird dringend empfohlen, dass ein ActiveX-Steuerelement Container das automatische Abschneiden seiner Steuerelemente unterstützt. Dies führt für die meisten Steuerelemente zu einem effizienteren Betrieb. Wenn Automatisches Abschneiden unterstützt wird, muss die autoclip Ambient-Eigenschaft unterstützt werden und den Wert **true** aufweisen.

Das automatische Abschneiden ist die Fähigkeit eines Containers sicherzustellen, dass die gezeichnete Ausgabe eines Steuer Elements nur in den aktuellen Clippingbereich des Containers übergeht. In einem Container, der das automatische Clipping unterstützt, kann ein Steuerelement ohne Rücksicht auf den Ausschneide Bereich zeichnen, da der Container automatisch alle Zeichnungen Ausschneide, die außerhalb des Bereichs des Steuer Elements auftreten. Wenn ein Container das automatische Abschneiden nicht unterstützt, wird von cdk-generierten Steuerelementen ein zusätzliches übergeordnetes Fenster erstellt, wenn ein Clippingbereich außerhalb von NULL übergeben wird.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Container](containers.md)
</dt> </dl>

 

 




