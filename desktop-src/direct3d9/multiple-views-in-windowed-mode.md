---
description: Zusätzlich zur Swapkette, die im Besitz des Direct3DDevice-Objekts ist und über das Direct3DDevice-Objekt bearbeitet wird, kann eine Anwendung die IDirect3DDevice9::CreateAdditionalSwapChain-Methode verwenden, um zusätzliche Austauschketten zu erstellen, um mehrere Ansichten vom gleichen Gerät aus darzustellen.
ms.assetid: f0d01dfb-d1de-4d16-8c64-4ae56d7fed06
title: Mehrere Ansichten im Fenstermodus (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e2784a4f2bd855293e427aa9297d2e5725a74a3f5bce52b4b53cdf3d9081062
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120069020"
---
# <a name="multiple-views-in-windowed-mode-direct3d-9"></a>Mehrere Ansichten im Fenstermodus (Direct3D 9)

Zusätzlich zur Swapkette, die im Besitz des Direct3DDevice-Objekts ist und über das Direct3DDevice-Objekt bearbeitet wird, kann eine Anwendung die [**IDirect3DDevice9::CreateAdditionalSwapChain-Methode**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createadditionalswapchain) verwenden, um zusätzliche Austauschketten zu erstellen, um mehrere Ansichten vom gleichen Gerät aus darzustellen.

In der Regel erstellt die Anwendung eine Swapkette pro Sicht und ordnet jede Swapkette einer bestimmten Sicht zu. Die Anwendung rendert Bilder in den Hintergrundpuffern jeder Swapkette und verwendet dann die [**IDirect3DDevice9::P resent-Methode,**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present) um sie einzeln darzustellen. Beachten Sie, dass auf jedem Adapter jeweils nur eine Swapkette im Vollbildmodus angezeigt werden kann.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Darstellen einer Szene](presenting-a-scene.md)
</dt> </dl>

 

 
