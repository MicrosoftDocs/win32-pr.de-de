---
description: Clouds, Feuer und Geländepfade können alle durch eine Erweiterung der Technik zur Vergrößerung erstellt werden.
ms.assetid: c5607327-de46-4241-a01a-4adfe0bbf6fb
title: Clouds, Smoke und Trails (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 09da27ec1ba8f6ad8beb3c9a847226ffe63f1059c0b28dfe71e0d0582d56645f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118097160"
---
# <a name="clouds-smoke-and-vapor-trails-direct3d-9"></a>Clouds, Smoke und Trails (Direct3D 9)

Clouds, Feuer und Geländepfade können alle durch eine Erweiterung der Technik zur Vergrößerung erstellt werden. Weitere Informationen finden Sie unter [Entzuge (Direct3D 9).](billboarding.md) Durch Drehen des Strahls auf zwei anstatt auf einer Achse kann Ihre Anwendung es dem Benutzer ermöglichen, einen Strahl aus einem beliebigen Winkel anzuzeigen. In der Regel rotiert eine Anwendung den Mittelpunkt auf der horizontalen und vertikalen Achse.

Um eine einfache Cloud zu erstellen, kann Ihre Anwendung ein rechteckiges Primitiv auf einer oder zwei Achsen drehen, sodass das Primitive dem Benutzer gegenübersteht. Eine cloudähnliche Textur kann dann transparent auf den Primitiven angewendet werden. Ausführliche Informationen zum Anwenden von transparenten Texturen auf Primitive finden Sie unter [Texturmischung (Direct3D 9).](texture-blending.md) Sie können die Cloud animieren, indem Sie im Laufe der Zeit eine Reihe von Texturen anwenden.

Eine Anwendung kann komplexere Clouds erstellen, indem sie sie aus einer Gruppe von Primitiven bildet. Jeder Teil der Cloud ist ein rechteckiger Primitiver. Die Primitiven können im Laufe der Zeit unabhängig verschoben werden, um ein dynamisches Erscheinungsbild zu erhalten. Die folgende Abbildung zeigt dieses Konzept.

![Abbildung von Primitiven, die komplexere Clouds bilden](images/cloud.png)

Die Darstellung des Feuers wird ähnlich wie bei Clouds angezeigt. In der Regel sind mehrere Bündel erforderlich, z. B. komplexe Clouds. In der Regel werden im Laufe der Zeit Qualmen abgerechnet und steigen, sodass sich die Leitungen, aus denen die Qualmwolken bilden, entsprechend bewegen müssen. Unter Umständen müssen Sie weitere Leitungen hinzufügen, wenn die Pflaume steigt und verteilt wird.

Ein Schluchtenpfad ist eine Feuerplaume, die nicht aufsteigt. Wie eine Feuerplaume verteilt sie sich jedoch im Laufe der Zeit. Die folgende Abbildung zeigt die Technik der Verwendung von Schildern, um einen Steigpfad zu simulieren.

![Abbildung von Schildern, die einen Laufpfad simulieren](images/vapor.png)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Alphabeispiele](alpha-examples.md)
</dt> </dl>

 

 



