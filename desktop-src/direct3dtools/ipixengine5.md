---
description: Erweiterungen der IPixEngine4-Schnittstelle mit Ergänzungen zum Anzeigen von Texturen.
MS-HAID: vspixengine.IPixEngine5
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: IPixEngine5-Schnittstelle
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 8995B617-6830-4A07-8C83-B5925E033967
api_name:
- IPixEngine5
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 300ed31eae5d8ff4009f28691c5348db7cd89d6e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104521384"
---
# <a name="span-idvspixengineipixengine5spanipixengine5-interface"></a><span data-ttu-id="47c19-103"><span id="vspixengine.ipixengine5"></span>IPixEngine5-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="47c19-103"><span id="vspixengine.ipixengine5"></span>IPixEngine5 interface</span></span>

<span data-ttu-id="47c19-104">Erweiterungen der IPixEngine4-Schnittstelle mit Ergänzungen zum Anzeigen von Texturen.</span><span class="sxs-lookup"><span data-stu-id="47c19-104">Extensions to the IPixEngine4 interface containing additions for viewing textures.</span></span>

## <a name="members"></a><span data-ttu-id="47c19-105">Member</span><span class="sxs-lookup"><span data-stu-id="47c19-105">Members</span></span>

<span data-ttu-id="47c19-106">Die **IPixEngine5** -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="47c19-106">The **IPixEngine5** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="47c19-107">**IPixEngine5** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="47c19-107">**IPixEngine5** also has these types of members:</span></span>

-   [<span data-ttu-id="47c19-108">Methoden</span><span class="sxs-lookup"><span data-stu-id="47c19-108">Methods</span></span>](#methods)

### <a name="span-idmethodsspanmethods"></a><span data-ttu-id="47c19-109"><span id="methods"></span>Methoden</span><span class="sxs-lookup"><span data-stu-id="47c19-109"><span id="methods"></span>Methods</span></span>

<span data-ttu-id="47c19-110">Die **IPixEngine5** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="47c19-110">The **IPixEngine5** interface has these methods.</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th style="text-align: left;"><span data-ttu-id="47c19-111">Methode</span><span class="sxs-lookup"><span data-stu-id="47c19-111">Method</span></span></th><th style="text-align: left;"><span data-ttu-id="47c19-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="47c19-112">Description</span></span></th></tr></thead><tbody><tr class="odd"><td style="text-align: left;"><span data-ttu-id="47c19-113"><a href="/windows/desktop/direct3dtools/ipixengine5-freetextureasync-uint-ipixengine5callbacks-ptr-dword-dword"><strong>"Fretextureasync"</strong></a></span><span class="sxs-lookup"><span data-stu-id="47c19-113"><a href="/windows/desktop/direct3dtools/ipixengine5-freetextureasync-uint-ipixengine5callbacks-ptr-dword-dword"><strong>FreeTextureAsync</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="47c19-114">Gibt eine Textur frei und benachrichtigt den Host asynchron.</span><span class="sxs-lookup"><span data-stu-id="47c19-114">Frees a texture and notifies the host asynchronously.</span></span></p></td></tr><tr class="even"><td style="text-align: left;"><span data-ttu-id="47c19-115"><a href="/windows/desktop/direct3dtools/ipixengine5-loadhistogramasync-uint-pixenginetexturesliceindex-int-bstr-ipixengine5callbacks-ptr-dword-dword"><strong>Loadhistogrammasync</strong></a></span><span class="sxs-lookup"><span data-stu-id="47c19-115"><a href="/windows/desktop/direct3dtools/ipixengine5-loadhistogramasync-uint-pixenginetexturesliceindex-int-bstr-ipixengine5callbacks-ptr-dword-dword"><strong>LoadHistogramAsync</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="47c19-116">Eine asynchrone Anforderung zum Laden von Histogrammdaten.</span><span class="sxs-lookup"><span data-stu-id="47c19-116">An asynchronous request to load histogram data.</span></span></p></td></tr><tr class="odd"><td style="text-align: left;"><span data-ttu-id="47c19-117"><a href="/windows/desktop/direct3dtools/ipixengine5-loadtexturefromfileasync-bstr-bstr-ipixengine5callbacks-ptr-dword-dword"><strong>Loadtexturefromfileasync</strong></a></span><span class="sxs-lookup"><span data-stu-id="47c19-117"><a href="/windows/desktop/direct3dtools/ipixengine5-loadtexturefromfileasync-bstr-bstr-ipixengine5callbacks-ptr-dword-dword"><strong>LoadTextureFromFileAsync</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="47c19-118">Lädt eine Textur aus einer Datei und benachrichtigt den Host beim Abschluss asynchron.</span><span class="sxs-lookup"><span data-stu-id="47c19-118">Loads a texture from a file and notifies the host asynchronously when it completes.</span></span></p></td></tr><tr class="even"><td style="text-align: left;"><span data-ttu-id="47c19-119"><a href="/windows/desktop/direct3dtools/ipixengine5-loadtexturesliceasync-uint-pixenginetexturesliceindex-int-bstr-ipixengine5callbacks-ptr-dword-dword"><strong>Loadtexturesliceasync</strong></a></span><span class="sxs-lookup"><span data-stu-id="47c19-119"><a href="/windows/desktop/direct3dtools/ipixengine5-loadtexturesliceasync-uint-pixenginetexturesliceindex-int-bstr-ipixengine5callbacks-ptr-dword-dword"><strong>LoadTextureSliceAsync</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="47c19-120">Lädt einen Textur Slice und benachrichtigt den Host beim Abschluss asynchron.</span><span class="sxs-lookup"><span data-stu-id="47c19-120">Loads a texture slice and notifies the host asynchrnously when it completes.</span></span></p></td></tr><tr class="odd"><td style="text-align: left;"><span data-ttu-id="47c19-121"><a href="/windows/desktop/direct3dtools/ipixengine5-readtexelvalueasync-uint-pixenginetexturesliceindex-int-int-int-ipixengine5callbacks-ptr-dword-dword"><strong>"Read texelvalueasync"</strong></a></span><span class="sxs-lookup"><span data-stu-id="47c19-121"><a href="/windows/desktop/direct3dtools/ipixengine5-readtexelvalueasync-uint-pixenginetexturesliceindex-int-int-int-ipixengine5callbacks-ptr-dword-dword"><strong>ReadTexelValueAsync</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="47c19-122">Liest einen Texel-Wert und gibt das Ergebnis asynchron an den Host zurück.</span><span class="sxs-lookup"><span data-stu-id="47c19-122">Reads a texel value and returns the result to the host asynchrnously.</span></span></p></td></tr><tr class="even"><td style="text-align: left;"><span data-ttu-id="47c19-123"><a href="/previous-versions/windows/desktop/legacy/mt432769(v=vs.85)"><strong>Rendertextureasync</strong></a></span><span class="sxs-lookup"><span data-stu-id="47c19-123"><a href="/previous-versions/windows/desktop/legacy/mt432769(v=vs.85)"><strong>RenderTextureAsync</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="47c19-124">Rendert eine Textur in eine Datei und gibt das Ergebnis asynchron an den Host zurück.</span><span class="sxs-lookup"><span data-stu-id="47c19-124">Renders a texture to a file and returns the result to the host asynchrnously.</span></span></p></td></tr><tr class="odd"><td style="text-align: left;"><span data-ttu-id="47c19-125"><a href="/windows/desktop/direct3dtools/ipixengine5-savetextureasync-uint-bstr-ipixengine5callbacks-ptr-dword-dword"><strong>Savetextureasync</strong></a></span><span class="sxs-lookup"><span data-stu-id="47c19-125"><a href="/windows/desktop/direct3dtools/ipixengine5-savetextureasync-uint-bstr-ipixengine5callbacks-ptr-dword-dword"><strong>SaveTextureAsync</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="47c19-126">Speichert eine Textur.</span><span class="sxs-lookup"><span data-stu-id="47c19-126">Saves a texture.</span></span></p></td></tr></tbody></table>

 

## <a name="requirements"></a><span data-ttu-id="47c19-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="47c19-127">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="47c19-128">Header</span><span class="sxs-lookup"><span data-stu-id="47c19-128">Header</span></span></p></td><td><span data-ttu-id="47c19-129">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="47c19-129">Vspixengine.h</span></span></td></tr></tbody></table>

 

 
