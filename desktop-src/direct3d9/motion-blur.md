---
description: Sie können die wahrgenommene Geschwindigkeit eines Objekts in einer 3D-Szene verbessern, indem Sie das Objekt unscharf machen und eine unscharfe Spur von Objektbildern hinter dem Objekt lassen. Direct3D-Anwendungen erreichen dies, indem sie das Objekt mehrmals pro Frame rendern.
ms.assetid: 8b1a1f0d-5857-4ab4-828c-8ca7c17a4890
title: Bewegungsunschärfe (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3daa0b35a0c375cc798b619f18f1e363001050de4dcc950e6c6828a7d365801
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119628320"
---
# <a name="motion-blur-direct3d-9"></a>Bewegungsunschärfe (Direct3D 9)

Sie können die wahrgenommene Geschwindigkeit eines Objekts in einer 3D-Szene verbessern, indem Sie das Objekt unscharf machen und eine unscharfe Spur von Objektbildern hinter dem Objekt lassen. Direct3D-Anwendungen erreichen dies, indem sie das Objekt mehrmals pro Frame rendern.

Denken Sie daran, dass Direct3D-Anwendungen Szenen in der Regel in einem Off-Screen-Puffer rendern. Der Inhalt des Puffers wird auf dem Bildschirm angezeigt, wenn die Anwendung die [**IDirect3DDevice9::P resent-Methode**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present) aufruft. Ihre Direct3D-Anwendung kann das Objekt mehrmals in einer Szene rendern, bevor der Frame auf dem Bildschirm angezeigt wird.

Programmgesteuert ruft Ihre Anwendung mehrere Aufrufe einer DrawPrimitive-Methode auf und überträgt wiederholt das gleiche 3D-Objekt. Vor jedem Aufruf wird die Position des Objekts leicht aktualisiert, wodurch eine Reihe von unscharfen Objektbildern auf der Zielrenderingoberfläche erzeugt wird. Wenn das Objekt über eine oder mehrere Texturen verfügt, kann Ihre Anwendung den Bewegungsunschärfeeffekt verbessern, indem das erste Bild des Objekts mit allen Texturen nahezu transparent gerendert wird. Jedes Mal, wenn das Objekt gerendert wird, nimmt die Transparenz der Textur des Objekts ab. Wenn Ihre Anwendung das Objekt an seiner endgültigen Position rendert, sollte sie die Texturen des Objekts ohne Transparenz rendern. Die Ausnahme ist, wenn Sie bewegungsunschärfer zu einem anderen Effekt hinzufügen, der Texturtransparenz erfordert. In jedem Fall sollte das Anfangsbild des Objekts im Frame am transparentesten sein. Das endgültige Image sollte am wenigsten transparent sein.

Nachdem Ihre Anwendung die Reihe von Objektbildern auf der Zielrenderingoberfläche gerendert und den Rest der Szene gerendert hat, sollte sie die [**IDirect3DDevice9::P resent-Methode**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present) aufrufen, um den Frame auf dem Bildschirm anzuzeigen.

Wenn Ihre Anwendung den Effekt simuliert, dass sich der Benutzer mit hoher Geschwindigkeit durch eine Szene bewegt, kann dies der gesamten Szene bewegungsunschärfer werden. In diesem Fall rendert Ihre Anwendung die gesamte Szene mehrmals pro Frame. Jedes Mal, wenn die Szene gerendert wird, muss Ihre Anwendung den Blickpunkt leicht bewegen. Wenn die Szene sehr komplex ist, kann der Benutzer eine sichtbare Leistungsbeeinträchtigung sehen, da die Beschleunigung aufgrund der zunehmenden Anzahl von Szenenrenderings pro Frame erhöht wird.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Antialiasing](antialiasing.md)
</dt> </dl>

 

 
