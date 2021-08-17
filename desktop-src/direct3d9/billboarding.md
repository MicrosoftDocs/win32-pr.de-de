---
description: Beim Erstellen von 3D-Szenen kann eine Anwendung manchmal Leistungsvorteile erzielen, indem 2D-Objekte so gerendert werden, dass sie als 3D-Objekte erscheinen. Dies ist die Grundidee hinter der Technik des -Tafelns.
ms.assetid: 6637a9ce-6731-4f60-8b76-854e86b10bdd
title: Beschriftung (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02624a3172df7a36f4d38bb2bc6d613ded26faab8ac6d4f4b37668f0868cd16c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119123407"
---
# <a name="billboarding-direct3d-9"></a>Beschriftung (Direct3D 9)

Beim Erstellen von 3D-Szenen kann eine Anwendung manchmal Leistungsvorteile erzielen, indem 2D-Objekte so gerendert werden, dass sie als 3D-Objekte erscheinen. Dies ist die Grundidee hinter der Technik des -Tafelns.

Ein Schild im normalen Sinn des Worts ist ein Schild entlang einer Straße. Microsoft Direct3D-Anwendungen können diese Art von Tafel erstellen und rendern, indem sie einen rechteckigen Vollbildkörper definieren und eine Textur darauf anwenden. Das Aufhüren im spezielleren Sinn von 3D-Grafiken ist eine Erweiterung dieser. Ziel ist es, 2D-Objekte als 3D-Objekte zu verwenden. Die Technik besteht in der Anwendung einer Textur, die das Bild des Objekts enthält, auf einen rechteckigen Primitiven. Das Primitiv wird so gedreht, dass es immer dem Benutzer gegenüber steht. Es spielt keine Rolle, ob das Bild des Objekts nicht rechteckig ist. Teile der Tafel können transparent gemacht werden, sodass die Teile des Bilds, die Sie nicht sehen möchten, nicht sichtbar sind.

Viele Spiele verwenden Diebung für animierte Sprites. Wenn sich der Benutzer beispielsweise durch ein 3D-3D-2016 bewegt, werden ihm möglicherweise Bzw. Belohnungen angezeigt, die bzw. die er erhalten kann. Hierbei handelt es sich in der Regel um 2D-Bilder, die auf einem rechteckigen Primitiv strukturiert sind. In Spielen werden häufig Bilder von Bäumen, Sträuchen und Clouds gerendert.

Wenn ein Bild auf ein Schild angewendet wird, muss das rechteckige Primitiv zuerst gedreht werden, damit das resultierende Bild dem Benutzer angezeigt wird. Ihre Anwendung muss sie dann in die Position übersetzen. Die Anwendung kann dann eine Textur auf den Primitiven anwenden.

Die Überschlagung funktioniert am besten für symmetrische Objekte, insbesondere für Objekte, die entlang der vertikalen Achse symmetrisch sind. Außerdem ist es erforderlich, dass sich die Höhe des Blickpunkts nicht zu stark erhöht. Wenn der Benutzer das von oben gezeigte -Objekt anzeigen darf, wird deutlich, dass das Objekt 2D und nicht 3D ist.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Alphabeispiele](alpha-examples.md)
</dt> </dl>

 

 



