---
description: Sie können die wahrgenommene Geschwindigkeit eines Objekts in einer 3D-Szene verbessern, indem Sie das Objekt verwischen und eine unscharfe Spur von Objektbildern hinter dem Objekt hinterlassen. Direct3D-Anwendungen erreichen dies, indem Sie das Objekt mehrmals pro Frame rendern.
ms.assetid: 8b1a1f0d-5857-4ab4-828c-8ca7c17a4890
title: Bewegungsunschärfe (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fccb5c00d1208041afc31d4afe1cf0c7a5425037
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104521920"
---
# <a name="motion-blur-direct3d-9"></a>Bewegungsunschärfe (Direct3D 9)

Sie können die wahrgenommene Geschwindigkeit eines Objekts in einer 3D-Szene verbessern, indem Sie das Objekt verwischen und eine unscharfe Spur von Objektbildern hinter dem Objekt hinterlassen. Direct3D-Anwendungen erreichen dies, indem Sie das Objekt mehrmals pro Frame rendern.

Erinnern Sie sich daran, dass Direct3D-Anwendungen in der Regel Szenen in einem Offline-Puffer darstellen. Der Inhalt des Puffers wird auf dem Bildschirm angezeigt, wenn die Anwendung die [**IDirect3DDevice9::P Resent**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present) -Methode aufruft. Ihre Direct3D-Anwendung kann das Objekt mehrmals in eine Szene Rendering, bevor der Frame auf dem Bildschirm angezeigt wird.

Programm gesteuert führt Ihre Anwendung mehrere Aufrufe an eine drawprimitive-Methode durch und übergibt dabei wiederholt dasselbe 3D-Objekt. Vor jedem-Rückruf wird die Position des-Objekts geringfügig aktualisiert, und es wird eine Reihe von unscharfen Objektbildern auf der Ziel Rendering-Oberfläche erzeugt. Wenn das-Objekt über eine oder mehrere Texturen verfügt, kann die Anwendung den Bewegungs weich Effekt verbessern, indem das erste Bild des Objekts mit allen zugehörigen Texturen nahezu transparent gerendert wird. Jedes Mal, wenn das Objekt gerendert wird, sinkt die Transparenz der Textur des Objekts. Wenn die Anwendung das Objekt an der endgültigen Position rendert, sollte Sie die Texturen des Objekts ohne Transparenz rendern. Die Ausnahme besteht darin, dass Sie Bewegungsunschärfe einem anderen Effekt hinzufügen, der Textur Transparenz erfordert. In jedem Fall sollte das erste Bild des Objekts im Frame transparent sein. Das endgültige Bild sollte am wenigsten transparent sein.

Nachdem die Anwendung die Reihe von Objektbildern auf der Ziel Rendering-Oberfläche gerendert und den Rest der Szene gerendert hat, sollte Sie die [**IDirect3DDevice9::P Resent**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present) -Methode aufrufen, um den Frame auf dem Bildschirm anzuzeigen.

Wenn Ihre Anwendung die Auswirkung des Benutzers auf eine hohe Geschwindigkeit simuliert, kann der Benutzer der gesamten Szene Bewegungsunschärfe hinzufügen. In diesem Fall wird die gesamte Szene von Ihrer Anwendung mehrmals pro Frame gerendert. Jedes Mal, wenn die Szene gerendert wird, muss die Anwendung den Standpunkt leicht verschieben. Wenn die Szene sehr komplex ist, wird dem Benutzer möglicherweise eine sichtbare Leistungsminderung angezeigt, da sich die Beschleunigung aufgrund der zunehmenden Anzahl von Szenen Renderings pro Frame vergrößert.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Antialiasing](antialiasing.md)
</dt> </dl>

 

 
