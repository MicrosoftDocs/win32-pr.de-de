---
description: Definiert einen Koordinaten Rahmen oder &\# 0034; Frame des Verweises. &\# 0034; Die Frame Vorlage ist geöffnet und kann ein beliebiges-Objekt enthalten. Die D3DX Mesh-Ladefunktionen erkennen Mesh-, frametransformmatrix-und Frame-Vorlagen Instanzen als untergeordnete Objekte beim Laden einer Frame Instanz.
ms.assetid: vs|directx_sdk|~\frame.htm
title: Frame (Direct3D 9-Grafiken)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81cc9d02b1bcbc21cc299739d93272afcf110c92
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103860092"
---
# <a name="frame-direct3d-9-graphics"></a><span data-ttu-id="9ea9d-104">Frame (Direct3D 9-Grafiken)</span><span class="sxs-lookup"><span data-stu-id="9ea9d-104">Frame (Direct3D 9 Graphics)</span></span>

<span data-ttu-id="9ea9d-105">Definiert einen Koordinaten Rahmen oder "Frame of Reference".</span><span class="sxs-lookup"><span data-stu-id="9ea9d-105">Defines a coordinate frame, or "frame of reference."</span></span> <span data-ttu-id="9ea9d-106">Die Frame Vorlage ist geöffnet und kann ein beliebiges-Objekt enthalten.</span><span class="sxs-lookup"><span data-stu-id="9ea9d-106">The Frame template is open and can contain any object.</span></span> <span data-ttu-id="9ea9d-107">Die D3DX Mesh-Ladefunktionen erkennen [**Mesh**](mesh.md)-, [**frametransformmatrix**](frametransformmatrix.md)-und **Frame** -Vorlagen Instanzen als untergeordnete Objekte beim Laden einer **Frame** Instanz.</span><span class="sxs-lookup"><span data-stu-id="9ea9d-107">The D3DX mesh-loading functions recognize [**Mesh**](mesh.md), [**FrameTransformMatrix**](frametransformmatrix.md), and **Frame** template instances as child objects when loading a **Frame** instance.</span></span>

``` syntax
template Frame
{
    < 3D82AB46-62DA-11CF-AB39-0020AF71E433 >
    [...]           
} 
```

<span data-ttu-id="9ea9d-108">Die Frame-Vorlage erkennt untergeordnete **Frame** -und [**Gitter**](mesh.md) Knoten innerhalb eines Frames und kann benutzerdefinierte Vorlagen über eine Rückruffunktion erkennen.</span><span class="sxs-lookup"><span data-stu-id="9ea9d-108">The frame template recognizes child **Frame** and [**Mesh**](mesh.md) nodes inside a frame and can recognize user-defined templates through a callback function.</span></span>

## <a name="see-also"></a><span data-ttu-id="9ea9d-109">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9ea9d-109">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9ea9d-110">Vorlagen</span><span class="sxs-lookup"><span data-stu-id="9ea9d-110">Templates</span></span>](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



