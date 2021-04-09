---
description: Medien Parameter
ms.assetid: 48b2bc2e-897d-4aa9-8a50-c2855a17dca5
title: Medien Parameter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce9276a3d38b9176458299bfd1a47057cac6236e
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "103869472"
---
# <a name="media-parameters"></a>Medien Parameter

Mithilfe von Medien Parametern kann eine Anwendung die Eigenschaften eines Objekts so konfigurieren, dass Sie sich im Laufe der Zeit auf mathematisch deterministische Weise ändern.

Nehmen wir beispielsweise an, dass ein Sound Techniker ein digitales Master Band vermischt und eine geringfügige Verzögerung auf einen Vokal Abschnitt anwenden möchte, um den Sound auszufüllen. Der Effekt wird als jarringvorgang verwendet, wenn die Verzögerung plötzlich reduziert wird. Stattdessen sollte der Effekt 100 Prozent trocken (keine Verzögerung) beginnen, und die nasse/trockene Mischung sollte allmählich erhöht werden, bis die gewünschte Ebene erreicht wird. Außerdem sollte dieser Übergang eine glatte Kurve oder eine lineare Fortsetzung nach sich ziehen. Zur Unterstützung dieses Szenarios kann ein DMO die folgenden Schnittstellen verfügbar machen:

-   [**Imediaparaminfo**](/previous-versions/windows/desktop/api/Medparam/nn-medparam-imediaparaminfo) enthält Methoden zum Ermitteln von Informationen zu den unterstützten Eigenschaften. In der Regel ruft der Client diese Methoden auf, bevor er mit dem Streamen von Daten beginnt.
-   [**Imediaparams**](/previous-versions/windows/desktop/api/Medparam/nn-medparam-imediaparams) enthalten Methoden zum Festlegen der Kurven, die ein Parameter beim Streaming befolgt.

Diese Schnittstellen sind hauptsächlich für DMOS konzipiert, aber jedes Objekt kann Sie unterstützen. In diesem Abschnitt bezieht sich der Begriffs *Parameter* auf eine beliebige Eigenschaft, die diese beiden Schnittstellen unterstützt.

Dieser Abschnitt enthält die folgenden Themen:

-   [Parameter Kurven](parameter-curves.md)
-   [Parameter Informationen](parameter-information.md)
-   [Umschlag Segmente](envelope-segments.md)
-   [Berechnen von Parameter Werten](calculating-parameter-values.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[DirectX-Medienobjekte](directx-media-objects.md)
</dt> </dl>

 

 



