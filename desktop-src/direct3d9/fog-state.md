---
description: Effekteffekte können einer 3D-Szene mehr Realismus verleihen.
ms.assetid: 26fe4f7c-7bb3-4a52-b539-5de2b11256e9
title: Zustand "State" (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 84004b8f261f9a6dc4c9b800ba5baa1f9a3c3e528db2b94e86286c3752414729
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119564240"
---
# <a name="fog-state-direct3d-9"></a>Zustand "State" (Direct3D 9)

Effekteffekte können einer 3D-Szene mehr Realismus verleihen. Sie können Effekteffekte für mehr als die Simulation von Häufungseffekten verwenden. Sie können auch die Klarheit einer Szene mit Entfernung verringern. Dies spiegelt wider, was in der realen Welt geschieht. wenn Objekte vom Benutzer entfernt werden, sind ihre Details weniger eindeutig.

Weitere Informationen zur Verwendung von "computers" in Ihrer Anwendung finden Sie unter [Überfall (Direct3D 9).](fog.md)

Eine C++-Anwendung steuert die Steuerung von Geräterenderingzuständen. Der [**D3DRENDERSTATETYPE-Enumerationstyp**](./d3drenderstatetype.md) enthält Zustände, um zu steuern, ob Pixel( Tabelle) oder Scheitelpunkt-Knoten verwendet werden, um welche Farbe es sich handelt, um die vom System angewendete Formel und die Parameter der Formel.

Sie aktivieren die Belegung, indem Sie den \_ D3DRS-RENDERZUSTAND FÜR DEN RENDER AUF **TRUE** festlegen. Die Farbtonfarbe kann mithilfe des D3DRS-RENDERzustandsCOLOR auf einen beliebigen Farbwert festgelegt \_ werden. Die Alphakomponente der Farbtonfarbe wird ignoriert.

Die Renderzustände D3DRS \_ SHADETABLEMODE und D3DRSTEXMODE \_ steuern die Formel, die für Berechnungen von Formeln angewendet wird, und steuern indirekt, welcher Typ von Licht angewendet wird. Beide Renderzustände können auf einen Member des [**D3DFOGMODE-Enumerationstyps**](./d3dfogmode.md) festgelegt werden. Wenn Sie entweder den Renderzustand auf D3DFOG NONE festlegen, wird der \_ Pixel- bzw. Scheitelpunktverschluss deaktiviert. Wenn beide Renderzustände auf gültige Modi festgelegt sind, wendet das System nur Pixeleffekteffekte an.

Die Renderzustände D3DRS \_ ADRSTART und D3DRS( \_ D3DRS) steuern Formelparameter der Formel für den D3DFOG \_ LINEAR-Modus. Der \_ D3DRS-RENDERZUSTANDSsteuert die Dichte der Verzweigungen in den exponentiellen Verzweigungsmodi.

Weitere Informationen finden Sie unter Parameter für [Metriken (Direct3D 9).](fog-parameters.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Renderzustände](render-states.md)
</dt> </dl>

 

 
