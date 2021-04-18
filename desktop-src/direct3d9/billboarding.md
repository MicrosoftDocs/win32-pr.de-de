---
description: Beim Erstellen von 3D-Szenen kann eine Anwendung manchmal Leistungsvorteile erzielen, indem 2D-Objekte auf eine Weise gerendert werden, die Sie als 3D-Objekte eingibt. Dies ist die grundlegende Idee hinter der Methode des fakboardingverfahrens.
ms.assetid: 6637a9ce-6731-4f60-8b76-854e86b10bdd
title: Fakboardingvorgang (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e287624ef8800f0b66941e826e211d044b7bf27
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106344230"
---
# <a name="billboarding-direct3d-9"></a>Fakboardingvorgang (Direct3D 9)

Beim Erstellen von 3D-Szenen kann eine Anwendung manchmal Leistungsvorteile erzielen, indem 2D-Objekte auf eine Weise gerendert werden, die Sie als 3D-Objekte eingibt. Dies ist die grundlegende Idee hinter der Methode des fakboardingverfahrens.

Ein Billboard im normalen Sinne des Worts ist ein Vorzeichen. Microsoft Direct3D-Anwendungen können diese Art von Billboard erstellen und Rendering, indem Sie ein rechteckiges Solid definieren und eine Textur darauf anwenden. Das Abgleichen von 3D-Grafiken ist eine Erweiterung dieser. Das Ziel besteht darin, 2D-Objekte als 3D-Objekte zu erstellen. Die Technik besteht darin, eine Textur mit dem Bild des Objekts auf ein rechteckiges primitiv anzuwenden. Die primitive wird so gedreht, dass Sie immer dem Benutzer angezeigt wird. Es spielt keine Rolle, ob das Bild des Objekts nicht rechteckig ist. Teile des Billboard können transparent gemacht werden, sodass die Teile des Billboard-Bilds, die Sie nicht sehen möchten, nicht sichtbar sind.

Viele Spiele verwenden die Abrechnungen für animierte Sprites. Wenn der Benutzer z. b. durch ein 3D-Maze bewegt wird, wird ihm möglicherweise Waffen oder Belohnungen angezeigt, die abgerufen werden können. Dabei handelt es sich in der Regel um 2D-Bilder, die auf einem rechteckigen primitiven Das Abgleichen von Abrechnungen wird häufig in Spielen zum Rendering von Bildern, Sträuchern und Clouds verwendet.

Wenn ein Bild auf ein Billboard angewendet wird, muss der rechteckige Primitive zuerst gedreht werden, damit das resultierende Bild dem Benutzer angezeigt wird. Die Anwendung muss Sie dann in die Position übersetzen. Die Anwendung kann dann eine Textur auf den primitiven anwenden.

Das Abgleichen von Abrechnungen eignet sich am besten für symmetrische Objekte, insbesondere für symmetrische Objekte entlang der vertikalen Achse. Außerdem ist es erforderlich, dass sich die Höhe des Standpunkts nicht zu stark vergrößert. Wenn der Benutzer die in der obigen Ansicht aufgeführten Daten anzeigen darf, ist es leicht erkennbar, dass es sich um ein 2D-Objekt und nicht um 3D handelt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Alpha Beispiele](alpha-examples.md)
</dt> </dl>

 

 



