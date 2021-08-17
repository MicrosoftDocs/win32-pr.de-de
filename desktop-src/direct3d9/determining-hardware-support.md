---
description: Direct3D stellt die folgenden Funktionen bereit, um die Hardwareunterstützung zu bestimmen.
ms.assetid: 63afa799-2c2c-432c-993e-dca8f7433d59
title: Bestimmen der Hardwareunterstützung (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42dda0aa1e1d5d75d2c8b6f0364c08daa836e7d2f0996252748bbb49b3d2a4a0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117730633"
---
# <a name="determining-hardware-support-direct3d-9"></a>Bestimmen der Hardwareunterstützung (Direct3D 9)

Direct3D stellt die folgenden Funktionen bereit, um die Hardwareunterstützung zu bestimmen.

-   [**IDirect3D9::CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat)

    Wird verwendet, um zu überprüfen, ob ein Oberflächenformat als Textur verwendet werden kann, ob ein Oberflächenformat als Textur und Renderziel verwendet werden kann oder ob ein Oberflächenformat als Tiefenschablonenpuffer verwendet werden kann. Darüber hinaus wird diese Methode verwendet, um die Unterstützung des Tiefenpufferformats und des Tiefenschablonenpufferformats zu überprüfen.

-   [**IDirect3D9::CheckDeviceType**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdevicetype)

    Wird verwendet, um die Fähigkeit eines Geräts zum Ausführen der Hardwarebeschleunigung, die Fähigkeit eines Geräts zum Erstellen einer Austauschkette für die Präsentation oder die Fähigkeit eines Geräts zum Rendern im aktuellen Anzeigeformat zu überprüfen.

-   [**IDirect3D9::CheckDepthStencilMatch**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdepthstencilmatch)

    Wird verwendet, um zu überprüfen, ob ein Tiefenschablonenpufferformat mit einem Renderzielformat kompatibel ist. Beachten Sie, dass die Anwendung vor dem Aufrufen dieser Methode [**IDirect3D9::CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat) sowohl für die Tiefenschablone als auch für das Renderzielformat aufrufen sollte.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Direct3D-Geräte](direct3d-devices.md)
</dt> </dl>

 

 
