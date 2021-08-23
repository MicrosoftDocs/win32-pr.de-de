---
description: Medienparameter
ms.assetid: 48b2bc2e-897d-4aa9-8a50-c2855a17dca5
title: Medienparameter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37cf7229cac3deb5b31a6c6879fd3b5896e5f4098a4cce64ac42d19970f5c569
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119584340"
---
# <a name="media-parameters"></a>Medienparameter

Medienparameter ermöglichen es einer Anwendung, die Eigenschaften eines Objekts so zu konfigurieren, dass sie sich im Laufe der Zeit auf mathematische deterministische Weise ändern.

Angenommen, ein Tontechniker mischen ein digitales Masterband und möchte eine geringfügige Verzögerung auf einen Bänderabschnitt anwenden, um den Sound zu füllen. Der Effekt ist jarring, wenn die Verzögerung plötzlich einschneidet. Stattdessen sollte der Effekt zu 100 Prozent (ohne Verzögerung) beginnen, und die Versheiterungs-/Regenmischung sollte schrittweise zunehmen, bis sie das gewünschte Niveau erreicht. Darüber hinaus sollte dieser Übergang einer reibungslosen Kurve oder einem linearen Fortschritt folgen. Zur Unterstützung dieses Szenarios kann ein DMO die folgenden Schnittstellen verfügbar machen:

-   [**IMediaParamInfo enthält**](/previous-versions/windows/desktop/api/Medparam/nn-medparam-imediaparaminfo) Methoden zum Entdecken von Informationen zu den unterstützten Eigenschaften. In der Regel wird der Client diese Methoden aufrufen, bevor er mit dem Streamen von Daten beginnt.
-   [**IMediaParams enthält**](/previous-versions/windows/desktop/api/Medparam/nn-medparam-imediaparams) Methoden zum Festlegen der Kurven, denen ein Parameter während des Streamings folgt.

Diese Schnittstellen sind in erster Linie für DMOs konzipiert, aber jedes Objekt kann sie unterstützen. In diesem Abschnitt bezieht sich der Begriff *parameter* auf jede Eigenschaft, die diese beiden Schnittstellen unterstützt.

Dieser Abschnitt enthält die folgenden Themen:

-   [Parameterkurven](parameter-curves.md)
-   [Parameterinformationen](parameter-information.md)
-   [Umschlagsegmente](envelope-segments.md)
-   [Berechnen von Parameterwerten](calculating-parameter-values.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[DirectX-Medienobjekte](directx-media-objects.md)
</dt> </dl>

 

 



