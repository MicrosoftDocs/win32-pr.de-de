---
description: Clouds, Rauch und dampfpfade können alle durch eine Erweiterung der Methode zum abboarding erstellt werden.
ms.assetid: c5607327-de46-4241-a01a-4adfe0bbf6fb
title: Clouds, Rauch und Dampfwege (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f60bce89e23b2b2aab7affbb6947cab4d11c33ed
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104571222"
---
# <a name="clouds-smoke-and-vapor-trails-direct3d-9"></a>Clouds, Rauch und Dampfwege (Direct3D 9)

Clouds, Rauch und dampfpfade können alle durch eine Erweiterung der Methode zum abboarding erstellt werden. Siehe [fakboardingvorgang (Direct3D 9)](billboarding.md). Durch das Drehen des Billboard auf zwei Achsen anstelle eines solchen kann die Anwendung es dem Benutzer ermöglichen, ein Billboard aus beliebigen Winkeln anzuzeigen. In der Regel dreht eine Anwendung das Billboard auf den horizontalen und vertikalen Achsen.

Um eine einfache Cloud zu erstellen, kann die Anwendung ein rechteckiges primitiv auf einer oder zwei Achsen Drehen, sodass der primitive dem Benutzer angezeigt wird. Eine cloudähnliche Textur kann dann mit Transparenz auf die primitive angewendet werden. Ausführliche Informationen zum Anwenden transparenter Texturen auf primitive finden Sie unter [Textur blending (Direct3D 9)](texture-blending.md). Sie können die Cloud animieren, indem Sie im Laufe der Zeit eine Reihe von Texturen anwenden.

Eine Anwendung kann komplexere Clouds erstellen, indem Sie Sie aus einer Gruppe von primitiven bilden. Jeder Teil der Cloud ist ein rechteckiges primitiv. Die primitiven können im Laufe der Zeit unabhängig verschoben werden, um die Darstellung eines dynamischen Mist zu gestalten. In der folgenden Abbildung wird dieses Konzept veranschaulicht.

![Abbildung von primitiven, die komplexere Clouds bilden](images/cloud.png)

Das Aussehen von Rauch wird ähnlich wie Clouds angezeigt. Es sind in der Regel mehrere Billboards erforderlich, z.b. komplexe Clouds. In der Regel wird ein Rauch angezeigt, der sich im Laufe der Zeit befindet, sodass die Plakate, aus denen sich die Rauch-Plume bilden, entsprechend verschoben werden Möglicherweise müssen Sie weitere Billboards hinzufügen, wenn Plume ansteigt und verteilt wird.

Ein dampfpfad ist ein Rauch-Plume, der nicht steigt. Wie eine Rauch-Plume wird Sie jedoch über einen Zeitraum verteilt. In der folgenden Abbildung wird veranschaulicht, wie Sie mithilfe von Billboards einen dampfpfad simulieren.

![Abbildung von Plakatwänden, die einen Dampf Pfad simulieren](images/vapor.png)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Alpha Beispiele](alpha-examples.md)
</dt> </dl>

 

 



