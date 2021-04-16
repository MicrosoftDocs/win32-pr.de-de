---
description: Zusätzlich zu der Swapkette, die über die IDirect3DDevice9-Schnittstelle gehört und manipuliert wird, kann eine Anwendung zusätzliche Austausch Ketten erstellen, um mehrere Ansichten desselben Geräts darzustellen.
ms.assetid: 4fc09b9c-7adb-4f5d-80e0-2d39bc10420e
title: Darstellung mehrerer Ansichten im Fenstermodus (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 039b02c487e06c7464dc8163c719371dc2b23706
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104522768"
---
# <a name="presenting-multiple-views-in-windowed-mode-direct3d-9"></a>Darstellung mehrerer Ansichten im Fenstermodus (Direct3D 9)

Zusätzlich zu der Swapkette, die über die [**IDirect3DDevice9**](/windows/desktop/api) -Schnittstelle gehört und manipuliert wird, kann eine Anwendung zusätzliche Austausch Ketten erstellen, um mehrere Ansichten desselben Geräts darzustellen. Die Anwendung erstellt in der Regel eine Austausch Kette pro Ansicht mithilfe der [**IDirect3DDevice9:: forateadditionalswapchain**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createadditionalswapchain) -Methode und ordnet jede Swapkette einem bestimmten Fenster zu. Die Anwendung rendert Bilder in den backpuffern jeder SwapChain und zeigt Sie dann einzeln an.

Jeweils nur eine SwapChain kann auf jedem Adapter voll Bildschirm sein.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Programmiertipps](programming-tips.md)
</dt> </dl>

 

 
