---
title: Prämultiplizieren von Effekten
description: Verwenden Sie diesen Effekt, um ein Bild von einem nicht multiplizierten Alpha in ein prämultipliziertes Alpha zu konvertieren.
ms.assetid: 8A5F55C6-3AC7-48B4-87D8-C19D8B4EA0DD
keywords:
- prämultiplizieren von Effekten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a01a8a9ba005ed688a96254856897b3514f05fd5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956784"
---
# <a name="premultiply-effect"></a><span data-ttu-id="a9fac-104">Prämultiplizieren von Effekten</span><span class="sxs-lookup"><span data-stu-id="a9fac-104">Premultiply effect</span></span>

<span data-ttu-id="a9fac-105">Verwenden Sie diesen Effekt, um ein Bild von einem nicht multiplizierten Alpha in ein prämultipliziertes Alpha zu konvertieren.</span><span class="sxs-lookup"><span data-stu-id="a9fac-105">Use this effect to convert an image from unpremultiplied alpha to premultiplied alpha.</span></span> <span data-ttu-id="a9fac-106">Der Effekt ersetzt jedes Eingabe Pixel `P = {R, G, B, A}` durch `P' = {R*A, G*A, B*A, A}` in der Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="a9fac-106">The effect replaces each input pixel `P = {R, G, B, A}` with `P' = {R*A, G*A, B*A, A}` in the output.</span></span>

<span data-ttu-id="a9fac-107">Dieser Effekt hat keine Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="a9fac-107">This effect has no properties.</span></span>

<span data-ttu-id="a9fac-108">Die CLSID für diesen Effekt ist CLSID \_ D2D1Premultiply.</span><span class="sxs-lookup"><span data-stu-id="a9fac-108">The CLSID for this effect is CLSID\_D2D1Premultiply.</span></span>

## <a name="output-bitmap"></a><span data-ttu-id="a9fac-109">Ausgabe Bitmap</span><span class="sxs-lookup"><span data-stu-id="a9fac-109">Output bitmap</span></span>

<span data-ttu-id="a9fac-110">Die Größe der Ausgabe Bitmap entspricht der Größe der Eingabe Bitmap.</span><span class="sxs-lookup"><span data-stu-id="a9fac-110">The output bitmap size is the same as the input bitmap size.</span></span>

## <a name="requirements"></a><span data-ttu-id="a9fac-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a9fac-111">Requirements</span></span>



| <span data-ttu-id="a9fac-112">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a9fac-112">Requirement</span></span> | <span data-ttu-id="a9fac-113">Wert</span><span class="sxs-lookup"><span data-stu-id="a9fac-113">Value</span></span> |
|--------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="a9fac-114">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a9fac-114">Minimum supported client</span></span> | <span data-ttu-id="a9fac-115">Windows 8 und Platt Form Update für Windows 7 \[ -Desktop-Apps für \| Windows Store-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a9fac-115">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="a9fac-116">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a9fac-116">Minimum supported server</span></span> | <span data-ttu-id="a9fac-117">Windows 8 und Platt Form Update für Windows 7 \[ -Desktop-Apps für \| Windows Store-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a9fac-117">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="a9fac-118">Header</span><span class="sxs-lookup"><span data-stu-id="a9fac-118">Header</span></span>                   | <span data-ttu-id="a9fac-119">d2d1effects. h</span><span class="sxs-lookup"><span data-stu-id="a9fac-119">d2d1effects.h</span></span>                                                                      |
| <span data-ttu-id="a9fac-120">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="a9fac-120">Library</span></span>                  | <span data-ttu-id="a9fac-121">d2d1. lib, dxguid. lib</span><span class="sxs-lookup"><span data-stu-id="a9fac-121">d2d1.lib, dxguid.lib</span></span>                                                               |



 

## <a name="related-topics"></a><span data-ttu-id="a9fac-122">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="a9fac-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a9fac-123">**ID2D1Effect**</span><span class="sxs-lookup"><span data-stu-id="a9fac-123">**ID2D1Effect**</span></span>](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

 
