---
description: Der durch den D3DTADDRESS \_ Clamp-Member des D3DTEXTUREADDRESS-Enumerationstyps identifizierte Klemm Textur Adress Modus bewirkt, dass Direct3D die Texturkoordinaten an den \[ Bereich 0,0, 1,0, anklammert \] .
ms.assetid: 8efed38d-4c9f-4a8d-9d1b-af1c8df9292a
title: Einspannen des Textur Adress Modus (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 153ed1f044bacaec6b87420eb7df22a2557349a7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106344223"
---
# <a name="clamp-texture-address-mode-direct3d-9"></a>Einspannen des Textur Adress Modus (Direct3D 9)

Der durch den D3DTADDRESS \_ Clamp-Member des [**D3DTEXTUREADDRESS**](./d3dtextureaddress.md) -Enumerationstyps identifizierte Klemm Textur Adress Modus bewirkt, dass Direct3D die Texturkoordinaten an den \[ Bereich 0,0, 1,0, anklammert \] . Das heißt, Sie wendet die Textur einmal an und gibt dann die Farbe der edgepixel aus. Nehmen Sie beispielsweise an, dass Ihre Anwendung ein quadratisches primitiv erstellt und die Texturkoordinaten (0,0, 0,0), (0,0, 3.0), (3.0, 3.0) und (3.0, 0,0) den Scheitel Punkten des primitiven zuweist. Wenn Sie den Textur Adressierungs Modus auf D3DTADDRESS-Klammer festlegen, \_ wird die Textur einmal angewendet. Die Pixel Farben am oberen Rand der Spalten und das Ende der Zeilen werden auf den oberen bzw. rechten Rand des primitiven erweitert.

Die folgende Abbildung zeigt eine geklehte Textur.

![Abbildung einer Textur und einer geklamfferten Textur](images/clamp.png)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Textur Adressierungs Modi](texture-addressing-modes.md)
</dt> </dl>

 

 
