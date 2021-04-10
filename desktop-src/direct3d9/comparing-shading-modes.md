---
description: Im Flatshading-Modus wird die folgende Pyramide mit einem Spitzen Rand zwischen angrenzenden Gesichtern angezeigt. Im Modus "Gouraud-Schattierung" werden Schattierungs Werte jedoch über den gesamten Rand hinweg interpoliert, und die endgültige Darstellung ist eine gekrümmte Oberfläche.
ms.assetid: efcaf3f7-b474-4719-adde-10096e296b9f
title: Vergleichen von Schattierungs Modi (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b275f18aa7283a8109db5d6709595cff0ddd09be
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127777"
---
# <a name="comparing-shading-modes-direct3d-9"></a>Vergleichen von Schattierungs Modi (Direct3D 9)

Im Flatshading-Modus wird die folgende Pyramide mit einem Spitzen Rand zwischen angrenzenden Gesichtern angezeigt. Im Modus "Gouraud-Schattierung" werden Schattierungs Werte jedoch über den gesamten Rand hinweg interpoliert, und die endgültige Darstellung ist eine gekrümmte Oberfläche.

![Abbildung einer Pyramide mit Spitzen Kanten und Pfeilen, die auf das Gesicht "normale" zeigen](images/shade2.png)

Die Schattierung von Gouraud-Schattierungen ist eine realistischere Oberfläche als flache Schattierung. Ein Gesicht im Flatshading-Modus ist eine einheitliche Farbe, aber die Schattierung von Gouraud ermöglicht, dass das Licht besser auf ein Gesicht fällt. Dieser Effekt ist besonders offensichtlich, wenn eine Punktquelle in der Nähe vorhanden ist.

Durch die Schattierung von Gouraud werden die Spitzen Ränder zwischen Polygonen, die mit flacher Schattierung sichtbar sind, glätten. Allerdings kann dies zu Mach-Bändern führen, bei denen es sich um Farb-oder Lichtbänder handelt, die nicht nahtlos über angrenzende Polygone gemischt werden. Die Anwendung kann die Darstellung von Mach-Bändern verringern, indem die Anzahl der Polygone in einem Objekt erhöht wird, die Bildschirmauflösung erhöht oder die Farbtiefe der Anwendung erhöht wird.

Bei der Schattierung von Gouraud können einige Details übersehen werden. Beispielsweise ist in der folgenden Abbildung ein Spotlight vollständig in einem Polygon Gesicht enthalten.

![Abbildung eines Spotlight in einem Polygon Gesicht](images/gouraud.png)

In diesem Fall würde die Schattierung von Gouraud, die zwischen Scheitel Punkten interpoliert, das Spotlight vollständig übersehen. das Gesicht würde so gerendert werden, als wäre der Spotlight nicht vorhanden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Schattierung](shading.md)
</dt> </dl>

 

 



