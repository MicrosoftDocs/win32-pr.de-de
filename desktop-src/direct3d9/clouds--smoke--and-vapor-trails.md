---
description: Cloud-, Qualm- und Tafelpfade können alle durch eine Erweiterung der Qualmtechnik erstellt werden.
ms.assetid: c5607327-de46-4241-a01a-4adfe0bbf6fb
title: Clouds, Smoke und Trail Trail (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 09da27ec1ba8f6ad8beb3c9a847226ffe63f1059c0b28dfe71e0d0582d56645f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118097160"
---
# <a name="clouds-smoke-and-vapor-trails-direct3d-9"></a>Clouds, Smoke und Trail Trail (Direct3D 9)

Cloud-, Qualm- und Tafelpfade können alle durch eine Erweiterung der Qualmtechnik erstellt werden. Weitere [Informationen finden Sie unterIng (Direct3D 9).](billboarding.md) Durch Drehen der Achse auf zwei Achsen anstelle einer kann Ihre Anwendung es dem Benutzer ermöglichen, ein Schild aus einem beliebigen Winkel zu sehen. In der Regel rotiert eine Anwendung die Tafel auf der horizontalen und vertikalen Achse.

Um eine einfache Wolke zu erstellen, kann Ihre Anwendung ein rechteckiges Primitiv auf einer oder zwei Achsen drehen, sodass das Primitiv dem Benutzer gegenüber steht. Eine cloudbasierte Textur kann dann mit Transparenz auf das Primitiv angewendet werden. Weitere Informationen zum Anwenden transparenter Texturen auf Primitive finden Sie unter [Texturmischung (Direct3D 9).](texture-blending.md) Sie können die Cloud animieren, indem Sie im Laufe der Zeit eine Reihe von Texturen anwenden.

Eine Anwendung kann komplexere Clouds erstellen, indem sie sie aus einer Gruppe primitiver Typen bildet. Jeder Teil der Cloud ist ein rechteckiger Grundtyp. Die Primitive können im Laufe der Zeit unabhängig voneinander verschoben werden, um das Erscheinungsbild eines dynamischen Erscheinungsbilds zu erhalten. Die folgende Abbildung zeigt dieses Konzept.

![Abbildung von Primitiven, die komplexere Clouds bilden](images/cloud.png)

Das Erscheinungsbild von Qualm wird ähnlich wie bei Clouds angezeigt. In der Regel sind mehrere Tafeln erforderlich, z. B. komplexe Clouds. In der Regel wird im Laufe der Zeit Eine Qualm geräuchert und steigt, sodass sich die Tafeln, aus denen die Qualmwolke besteht, entsprechend bewegen müssen. Möglicherweise müssen Sie weitere Tafeln hinzufügen, wenn die Pflaume zu- und verteilt wird.

Bei einem 20-0-Pfad handelt es sich um eine Qualmwolke, die nicht steigt. Wie bei einer Brandwolke wird sie jedoch im Laufe der Zeit verteilt. Die folgende Abbildung zeigt die Technik der Verwendung von Schilden zum Simulieren eines Tafelpfads.

![Abbildung von Tafeln, die einen Tafelpfad simulieren](images/vapor.png)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Alphabeispiele](alpha-examples.md)
</dt> </dl>

 

 



