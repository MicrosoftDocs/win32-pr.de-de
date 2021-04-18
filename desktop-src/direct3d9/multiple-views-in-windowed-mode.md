---
description: Neben der Swapkette, die im Besitz des Direct3DDevice-Objekts ist, kann eine Anwendung die IDirect3DDevice9::-Methode verwenden, um zusätzliche Austausch Ketten zu erstellen, um mehrere Ansichten desselben Geräts darzustellen.
ms.assetid: f0d01dfb-d1de-4d16-8c64-4ae56d7fed06
title: Mehrere Ansichten im Fenstermodus (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed750472d1816c0365298630cfb426982743b11a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106338859"
---
# <a name="multiple-views-in-windowed-mode-direct3d-9"></a>Mehrere Ansichten im Fenstermodus (Direct3D 9)

Neben der Swapkette, die im Besitz des Direct3DDevice-Objekts ist, kann eine Anwendung die [**IDirect3DDevice9::**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createadditionalswapchain) -Methode verwenden, um zusätzliche Austausch Ketten zu erstellen, um mehrere Ansichten desselben Geräts darzustellen.

In der Regel erstellt die Anwendung eine austauschkette pro Ansicht und ordnet jede Austausch Kette einer bestimmten Ansicht zu. Die Anwendung rendert Bilder in den backpuffern jeder SwapChain und verwendet dann die [**IDirect3DDevice9::P Resent**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present) -Methode, um Sie einzeln darzustellen. Beachten Sie, dass auf jedem Adapter jeweils nur eine SwapChain auf dem Bildschirm angezeigt werden kann.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Präsentieren einer Szene](presenting-a-scene.md)
</dt> </dl>

 

 
