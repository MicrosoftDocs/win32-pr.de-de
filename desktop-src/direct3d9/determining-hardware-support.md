---
description: Direct3D bietet die folgenden Funktionen zum Bestimmen der Hardwareunterstützung.
ms.assetid: 63afa799-2c2c-432c-993e-dca8f7433d59
title: Bestimmen der Hardware Unterstützung (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc4fbc04343ede671d009054ac3782bbf2563109
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106338860"
---
# <a name="determining-hardware-support-direct3d-9"></a>Bestimmen der Hardware Unterstützung (Direct3D 9)

Direct3D bietet die folgenden Funktionen zum Bestimmen der Hardwareunterstützung.

-   [**IDirect3D9:: CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat)

    Wird verwendet, um zu überprüfen, ob ein Oberflächen Format als Textur verwendet werden kann, ob ein Oberflächen Format als Textur-und Renderziel verwendet werden kann oder ob ein Oberflächen Format als tiefen Schablone-Puffer verwendet werden kann. Außerdem wird diese Methode verwendet, um die Unterstützung für tiefe Puffer Formate und die Unterstützung für die Unterstützung von tiefen Schablonen Puffer zu überprüfen.

-   [**IDirect3D9:: checkabvicetype**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdevicetype)

    Wird verwendet, um zu überprüfen, ob das Gerät eine Hardwarebeschleunigung durchführen kann, ob ein Gerät eine Swapkette für die Präsentation erstellen oder ob ein Gerät in das aktuelle Anzeige Format renderfähig ist.

-   [**IDirect3D9:: checkdepthstencilmatch**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdepthstencilmatch)

    Wird verwendet, um zu überprüfen, ob ein tiefen Schablone-Puffer Format mit einem renderzielformat kompatibel ist. Beachten Sie, dass die Anwendung vor dem Aufruf dieser Methode [**IDirect3D9:: CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat) sowohl für das tiefen-Schablone-als auch das renderzielformat aufrufen sollte.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Direct3D-Geräte](direct3d-devices.md)
</dt> </dl>

 

 
