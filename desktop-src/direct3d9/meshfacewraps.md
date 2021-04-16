---
description: Wird verwendet, um die Textur Topologie der einzelnen Gesichter in einem Umbruch zu definieren. Der Wert des nfacewrapvalues-Members sollte gleich der Anzahl der Gesichter in einem Mesh sein.
ms.assetid: f4aa356c-8f91-462f-9fc7-869b186b6c27
title: Meshfacewrapper
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e9ba55db3dc2c0733d66f5a9e4589937258324b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104520483"
---
# <a name="meshfacewraps"></a><span data-ttu-id="dd04e-104">Meshfacewrapper</span><span class="sxs-lookup"><span data-stu-id="dd04e-104">MeshFaceWraps</span></span>

<span data-ttu-id="dd04e-105">Wird verwendet, um die Textur Topologie der einzelnen Gesichter in einem Umbruch zu definieren.</span><span class="sxs-lookup"><span data-stu-id="dd04e-105">Used to define the texture topology of each face in a wrap.</span></span> <span data-ttu-id="dd04e-106">Der Wert des nfacewrapvalues-Members sollte gleich der Anzahl der Gesichter in einem Mesh sein.</span><span class="sxs-lookup"><span data-stu-id="dd04e-106">The value of the nFaceWrapValues member should be equal to the number of faces in a mesh.</span></span>

``` syntax
template MeshFaceWraps
{
    < ED1EC5C0-C0A8-11D0-941C-0080C80CFA7B >
    DWORD nFaceWrapValues;
    array Boolean2d faceWrapValues[nFaceWrapValues];
} 
```

<span data-ttu-id="dd04e-107">Diese Vorlage wird nicht mehr verwendet.</span><span class="sxs-lookup"><span data-stu-id="dd04e-107">This template is no longer used.</span></span>

## <a name="see-also"></a><span data-ttu-id="dd04e-108">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="dd04e-108">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dd04e-109">Vorlagen</span><span class="sxs-lookup"><span data-stu-id="dd04e-109">Templates</span></span>](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



