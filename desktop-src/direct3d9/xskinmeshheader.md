---
description: Diese Vorlage wird nur in Netzen, die exportierte skinsinformationen enthalten, pro Mesh instanziiert. Der Zweck dieser Vorlage besteht darin, Informationen über die Art der exportierten Informationen zu den zu exportierenden Informationen bereitzustellen.
ms.assetid: 95a4fa45-63d1-4931-9c91-b26807d2b043
title: Xskinmeshheader
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 306f8c183086846fca020040af00b9ccef2665cc
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104392785"
---
# <a name="xskinmeshheader"></a><span data-ttu-id="103cb-104">Xskinmeshheader</span><span class="sxs-lookup"><span data-stu-id="103cb-104">XSkinMeshHeader</span></span>

<span data-ttu-id="103cb-105">Diese Vorlage wird nur in Netzen, die exportierte skinsinformationen enthalten, pro Mesh instanziiert.</span><span class="sxs-lookup"><span data-stu-id="103cb-105">This template is instantiated on a per-mesh basis only in meshes that contain exported skinning information.</span></span> <span data-ttu-id="103cb-106">Der Zweck dieser Vorlage besteht darin, Informationen über die Art der exportierten Informationen zu den zu exportierenden Informationen bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="103cb-106">The purpose of this template is to provide information about the nature of the skinning information that was exported.</span></span>

``` syntax
template XSkinMeshHeader 
{ 
    < 3CF169CE-FF7C-44ab-93C0-F78F62D172E2 >  
    WORD nMaxSkinWeightsPerVertex; 
    WORD nMaxSkinWeightsPerFace; 
    WORD nBones; 
}
```

<span data-ttu-id="103cb-107">Hierbei gilt:</span><span class="sxs-lookup"><span data-stu-id="103cb-107">Where:</span></span>

-   <span data-ttu-id="103cb-108">nmaxskinweightspervertex: maximale Anzahl von Transformationen, die einen Scheitelpunkt im Mesh beeinflussen.</span><span class="sxs-lookup"><span data-stu-id="103cb-108">nMaxSkinWeightsPerVertex - Maximum number of transforms that affect a vertex in the mesh.</span></span>
-   <span data-ttu-id="103cb-109">nmaxskinweightsperface: maximale Anzahl eindeutiger Transformationen, die die drei Scheitel Punkte beliebiger Gesichter beeinflussen.</span><span class="sxs-lookup"><span data-stu-id="103cb-109">nMaxSkinWeightsPerFace - Maximum number of unique transforms that affect the three vertices of any face.</span></span>
-   <span data-ttu-id="103cb-110">nbones: die Anzahl der Knochen, die die Scheitel Punkte in diesem Mesh beeinflussen.</span><span class="sxs-lookup"><span data-stu-id="103cb-110">nBones - Number of bones that affect vertices in this mesh.</span></span>

## <a name="see-also"></a><span data-ttu-id="103cb-111">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="103cb-111">See also</span></span>

<dl> <dt>

[<span data-ttu-id="103cb-112">Vorlagen</span><span class="sxs-lookup"><span data-stu-id="103cb-112">Templates</span></span>](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



