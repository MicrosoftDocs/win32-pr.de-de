---
description: 'Nachdem Sie einen tiefen Puffer erstellt haben, wie unter Erstellen eines tiefen Puffers (Direct3D 9) beschrieben, aktivieren Sie die Tiefe Pufferung durch Aufrufen der Methode IDirect3DDevice9:: settrenderstate.'
ms.assetid: a3c972dd-3630-4d21-a22b-64a68e9acd19
title: Aktivieren der tiefen Pufferung (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 935d4f2e1db164a3aac2a39627be88d71887cc14
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104341428"
---
# <a name="enabling-depth-buffering-direct3d-9"></a><span data-ttu-id="ee0d8-103">Aktivieren der tiefen Pufferung (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="ee0d8-103">Enabling Depth Buffering (Direct3D 9)</span></span>

<span data-ttu-id="ee0d8-104">Nachdem Sie einen tiefen Puffer erstellt haben, wie unter [Erstellen eines tiefen Puffers (Direct3D 9)](creating-a-depth-buffer.md)beschrieben, aktivieren Sie die Tiefe Pufferung durch Aufrufen der Methode [**IDirect3DDevice9:: settrenderstate**](/windows/desktop/api) .</span><span class="sxs-lookup"><span data-stu-id="ee0d8-104">After you create a depth buffer, as described in [Creating a Depth Buffer (Direct3D 9)](creating-a-depth-buffer.md), you enable depth buffering by calling the [**IDirect3DDevice9::SetRenderState**](/windows/desktop/api) method.</span></span> <span data-ttu-id="ee0d8-105">Legen Sie den D3DRS \_ zenable-renderzustand so fest, dass tiefe Pufferung aktiviert wird.</span><span class="sxs-lookup"><span data-stu-id="ee0d8-105">Set the D3DRS\_ZENABLE render state to enable depth-buffering.</span></span> <span data-ttu-id="ee0d8-106">Verwenden Sie den D3DZB \_ true-Member des [**D3DZBUFFERTYPE**](./d3dzbuffertype.md) -Enumerationstyps (oder **true**), um z-Pufferung zu aktivieren, D3DZB \_ usew, um w-buffereing zu aktivieren, oder D3DZB \_ false (oder **false**), um die tiefen Pufferung zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="ee0d8-106">Use the D3DZB\_TRUE member of the [**D3DZBUFFERTYPE**](./d3dzbuffertype.md) enumerated type (or **TRUE**) to enable z-buffering, D3DZB\_USEW to enable w-buffering, or D3DZB\_FALSE (or **FALSE**) to disable depth buffering.</span></span>

> [!Note]  
> <span data-ttu-id="ee0d8-107">Um w-buffereing zu verwenden, muss die Anwendung eine konforme Projektions Matrix festlegen, auch wenn Sie die Direct3D-Transformations Pipeline nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="ee0d8-107">To use w-buffering, your application must set a compliant projection matrix even if it doesn't use the Direct3D transformation pipeline.</span></span> <span data-ttu-id="ee0d8-108">Weitere Informationen zum Bereitstellen einer geeigneten Projektions Matrix finden Sie in der [W-freundlichen Projektions Matrix](projection-transform.md) .</span><span class="sxs-lookup"><span data-stu-id="ee0d8-108">For information about providing an appropriate projection matrix, see [A W-Friendly Projection Matrix](projection-transform.md)</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="ee0d8-109">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="ee0d8-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ee0d8-110">Tiefen Puffer</span><span class="sxs-lookup"><span data-stu-id="ee0d8-110">Depth Buffers</span></span>](depth-buffers.md)
</dt> </dl>

 

 
