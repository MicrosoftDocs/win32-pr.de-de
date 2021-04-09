---
description: Rückrufe, die zum Anzeigen von Texturen verwendet werden.
MS-HAID: vspixengine.IPixEngine5Callbacks
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: IPixEngine5Callbacks-Schnittstelle
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: F87F00ED-C816-49A3-926B-28E3C8330EA2
api_name:
- IPixEngine5Callbacks
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 80f00a0d7e2e3478114d94480e01e31add63ef90
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104124723"
---
# <a name="span-idvspixengineipixengine5callbacksspanipixengine5callbacks-interface"></a><span data-ttu-id="91289-103"><span id="vspixengine.ipixengine5callbacks"></span>IPixEngine5Callbacks-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="91289-103"><span id="vspixengine.ipixengine5callbacks"></span>IPixEngine5Callbacks interface</span></span>

<span data-ttu-id="91289-104">Rückrufe, die zum Anzeigen von Texturen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="91289-104">Callbacks used for viewing textures.</span></span>

## <a name="members"></a><span data-ttu-id="91289-105">Member</span><span class="sxs-lookup"><span data-stu-id="91289-105">Members</span></span>

<span data-ttu-id="91289-106">Die **IPixEngine5Callbacks** -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="91289-106">The **IPixEngine5Callbacks** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="91289-107">**IPixEngine5Callbacks** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="91289-107">**IPixEngine5Callbacks** also has these types of members:</span></span>

-   [<span data-ttu-id="91289-108">Methoden</span><span class="sxs-lookup"><span data-stu-id="91289-108">Methods</span></span>](#methods)

### <a name="span-idmethodsspanmethods"></a><span data-ttu-id="91289-109"><span id="methods"></span>Methoden</span><span class="sxs-lookup"><span data-stu-id="91289-109"><span id="methods"></span>Methods</span></span>

<span data-ttu-id="91289-110">Die **IPixEngine5Callbacks** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="91289-110">The **IPixEngine5Callbacks** interface has these methods.</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th style="text-align: left;"><span data-ttu-id="91289-111">Methode</span><span class="sxs-lookup"><span data-stu-id="91289-111">Method</span></span></th><th style="text-align: left;"><span data-ttu-id="91289-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="91289-112">Description</span></span></th></tr></thead><tbody><tr class="odd"><td style="text-align: left;"><span data-ttu-id="91289-113"><a href="/windows/desktop/direct3dtools/ipixengine5callbacks-freetexturecomplete"><strong>Freitexturecomplete</strong></a></span><span class="sxs-lookup"><span data-stu-id="91289-113"><a href="/windows/desktop/direct3dtools/ipixengine5callbacks-freetexturecomplete"><strong>FreeTextureComplete</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="91289-114">Eine Rückruffunktion, die verwendet wird, um den Host zu benachrichtigen, wenn eine Textur freigegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="91289-114">A callback function used to notify the host when a texture has been freed.</span></span></p></td></tr><tr class="even"><td style="text-align: left;"><span data-ttu-id="91289-115"><a href="/windows/desktop/direct3dtools/ipixengine5callbacks-loadhistogramcomplete-pixenginehistogram-ptr"><strong>Loadhistogrammcomplete</strong></a></span><span class="sxs-lookup"><span data-stu-id="91289-115"><a href="/windows/desktop/direct3dtools/ipixengine5callbacks-loadhistogramcomplete-pixenginehistogram-ptr"><strong>LoadHistogramComplete</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="91289-116">Eine Rückruffunktion, die verwendet wird, um den Host zu benachrichtigen, wenn eine histogrammauslastung abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="91289-116">A callback function used to notify the host when a histogram load has been completed.</span></span></p></td></tr><tr class="odd"><td style="text-align: left;"><span data-ttu-id="91289-117"><a href="/previous-versions/windows/desktop/legacy/mt432759(v=vs.85)"><strong>Loadtexturefromfilecomplete</strong></a></span><span class="sxs-lookup"><span data-stu-id="91289-117"><a href="/previous-versions/windows/desktop/legacy/mt432759(v=vs.85)"><strong>LoadTextureFromFileComplete</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="91289-118">Eine Rückruffunktion, die verwendet wird, um den Host zu benachrichtigen, wenn ein Textur Ladevorgang abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="91289-118">A callback function used to notify the host when a texture load has been completed.</span></span></p></td></tr><tr class="even"><td style="text-align: left;"><span data-ttu-id="91289-119"><a href="/windows/desktop/direct3dtools/ipixengine5callbacks-loadtextureslicecomplete-pixenginetextureslicedescriptor-pixenginehistogram-ptr"><strong>Loadtextureslicecomplete</strong></a></span><span class="sxs-lookup"><span data-stu-id="91289-119"><a href="/windows/desktop/direct3dtools/ipixengine5callbacks-loadtextureslicecomplete-pixenginetextureslicedescriptor-pixenginehistogram-ptr"><strong>LoadTextureSliceComplete</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="91289-120">Eine Rückruffunktion, die verwendet wird, um den Host zu benachrichtigen, wenn ein Textur Slice geladen wurde.</span><span class="sxs-lookup"><span data-stu-id="91289-120">A callback function used to notify the host when a texture slice load has been completed.</span></span></p></td></tr><tr class="odd"><td style="text-align: left;"><span data-ttu-id="91289-121"><a href="/windows/desktop/direct3dtools/ipixengine5callbacks-readtexelvaluecomplete-uint-bstr-arr-double-arr"><strong>"Read texelvaluecomplete"</strong></a></span><span class="sxs-lookup"><span data-stu-id="91289-121"><a href="/windows/desktop/direct3dtools/ipixengine5callbacks-readtexelvaluecomplete-uint-bstr-arr-double-arr"><strong>ReadTexelValueComplete</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="91289-122">Eine Rückruffunktion, die verwendet wird, um den Host zu benachrichtigen, wenn ein Texttyp gelesen wurde.</span><span class="sxs-lookup"><span data-stu-id="91289-122">A callback function used to notify the host when a texel value read has been completed.</span></span></p></td></tr><tr class="even"><td style="text-align: left;"><span data-ttu-id="91289-123"><a href="/windows/desktop/direct3dtools/ipixengine5callbacks-rendertexturecomplete"><strong>Rendertexturecomplete</strong></a></span><span class="sxs-lookup"><span data-stu-id="91289-123"><a href="/windows/desktop/direct3dtools/ipixengine5callbacks-rendertexturecomplete"><strong>RenderTextureComplete</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="91289-124">Eine Rückruffunktion, die verwendet wird, um den Host zu benachrichtigen, wenn ein Textur Rendering abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="91289-124">A callback function used to notify the host when a texture render has been completed.</span></span></p></td></tr><tr class="odd"><td style="text-align: left;"><span data-ttu-id="91289-125"><a href="/windows/desktop/direct3dtools/ipixengine5callbacks-savetexturecomplete"><strong>Savetexturecomplete</strong></a></span><span class="sxs-lookup"><span data-stu-id="91289-125"><a href="/windows/desktop/direct3dtools/ipixengine5callbacks-savetexturecomplete"><strong>SaveTextureComplete</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="91289-126">Eine Rückruffunktion, die verwendet wird, um den Host zu benachrichtigen, wenn das Speichern einer Textur abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="91289-126">A callback function used to notify the host when saving a texture has been completed.</span></span></p></td></tr></tbody></table>

 

## <a name="requirements"></a><span data-ttu-id="91289-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="91289-127">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="91289-128">Header</span><span class="sxs-lookup"><span data-stu-id="91289-128">Header</span></span></p></td><td><span data-ttu-id="91289-129">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="91289-129">Vspixengine.h</span></span></td></tr></tbody></table>

 

 
