---
description: Nachdem Sie einen Tiefenpuffer erstellt haben, wie unter Erstellen eines Tiefenpuffers (Direct3D 9) beschrieben, aktivieren Sie die Tiefenpufferung, indem Sie die IDirect3DDevice9::SetRenderState-Methode aufrufen.
ms.assetid: a3c972dd-3630-4d21-a22b-64a68e9acd19
title: Aktivieren der Tiefenpufferung (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e495b06e6c7d10890393f563c67053294010515e32a2eeb984abb371b8158231
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118095095"
---
# <a name="enabling-depth-buffering-direct3d-9"></a>Aktivieren der Tiefenpufferung (Direct3D 9)

Nachdem Sie einen Tiefenpuffer erstellt haben, wie unter Erstellen eines Tiefenpuffers [(Direct3D 9)](creating-a-depth-buffer.md)beschrieben, aktivieren Sie die Tiefenpufferung, indem Sie die [**IDirect3DDevice9::SetRenderState-Methode**](/windows/desktop/api) aufrufen. Legen Sie den D3DRS \_ ZENABLE-Renderzustand fest, um die Tiefenpufferung zu aktivieren. Verwenden Sie den D3D WIE TRUE-Member des \_ [**enumerierten D3DUFFERTYPE-Typs**](./d3dzbuffertype.md) (oder **TRUE),** um Z-Pufferung zu aktivieren, D3D WIE USEW zum Aktivieren der \_ W-Pufferung oder D3D WIE \_ FALSE (oder **FALSE),** um die Tiefenpufferung zu deaktivieren.

> [!Note]  
> Um die W-Pufferung zu verwenden, muss Ihre Anwendung auch dann eine konforme Projektionsmatrix festlegen, wenn die Direct3D-Transformationspipeline nicht verwendet wird. Informationen zum Bereitstellen einer geeigneten Projektionsmatrix finden Sie unter [Eine W-freundliche Projektionsmatrix.](projection-transform.md)

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Tiefenpuffer](depth-buffers.md)
</dt> </dl>

 

 
