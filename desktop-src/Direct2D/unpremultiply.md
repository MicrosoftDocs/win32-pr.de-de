---
title: Unvorhersehunmultiplizieren
description: Verwenden Sie diesen Effekt zum Konvertieren eines Bilds von einem prämultiplizierten Alpha in ein unvorhersehvielfaches alpha.
ms.assetid: A4FAF899-81DA-4BDA-98B4-DE63EC1664F5
keywords:
- unvorhersehunmultiplizieren
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5628ea646443a08abffa4549ad25147deb609acf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104392113"
---
# <a name="unpremultiply-effect"></a><span data-ttu-id="8a817-104">Unvorhersehunmultiplizieren</span><span class="sxs-lookup"><span data-stu-id="8a817-104">Unpremultiply effect</span></span>

<span data-ttu-id="8a817-105">Verwenden Sie diesen Effekt zum Konvertieren eines Bilds von einem prämultiplizierten Alpha in ein unvorhersehvielfaches alpha.</span><span class="sxs-lookup"><span data-stu-id="8a817-105">Use this effect to convert an image from premultiplied alpha to unpremultiplied alpha.</span></span> <span data-ttu-id="8a817-106">Der Effekt ersetzt jedes Eingabe Pixel `P = {R, G, B, A}` durch `P' = {R/A, G/A, B/A, A}` in der Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="8a817-106">The effect replaces each input pixel `P = {R, G, B, A}` with `P' = {R/A, G/A, B/A, A}` in the output.</span></span>

<span data-ttu-id="8a817-107">Dieser Effekt hat keine Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="8a817-107">This effect has no properties.</span></span>

<span data-ttu-id="8a817-108">Die CLSID für diesen Effekt ist CLSID \_ D2D1Unpremultiply.</span><span class="sxs-lookup"><span data-stu-id="8a817-108">The CLSID for this effect is CLSID\_D2D1Unpremultiply.</span></span>

## <a name="output-bitmap"></a><span data-ttu-id="8a817-109">Ausgabe Bitmap</span><span class="sxs-lookup"><span data-stu-id="8a817-109">Output bitmap</span></span>

<span data-ttu-id="8a817-110">Die Größe der Ausgabe Bitmap entspricht der Größe der Eingabe Bitmap.</span><span class="sxs-lookup"><span data-stu-id="8a817-110">The output bitmap size is the same as the input bitmap size.</span></span>

## <a name="requirements"></a><span data-ttu-id="8a817-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8a817-111">Requirements</span></span>



| <span data-ttu-id="8a817-112">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8a817-112">Requirement</span></span> | <span data-ttu-id="8a817-113">Wert</span><span class="sxs-lookup"><span data-stu-id="8a817-113">Value</span></span> |
|--------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="8a817-114">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="8a817-114">Minimum supported client</span></span> | <span data-ttu-id="8a817-115">Windows 8 und Platt Form Update für Windows 7 \[ -Desktop-Apps für \| Windows Store-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8a817-115">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="8a817-116">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="8a817-116">Minimum supported server</span></span> | <span data-ttu-id="8a817-117">Windows 8 und Platt Form Update für Windows 7 \[ -Desktop-Apps für \| Windows Store-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8a817-117">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="8a817-118">Header</span><span class="sxs-lookup"><span data-stu-id="8a817-118">Header</span></span>                   | <span data-ttu-id="8a817-119">d2d1effects. h</span><span class="sxs-lookup"><span data-stu-id="8a817-119">d2d1effects.h</span></span>                                                                      |
| <span data-ttu-id="8a817-120">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="8a817-120">Library</span></span>                  | <span data-ttu-id="8a817-121">d2d1. lib, dxguid. lib</span><span class="sxs-lookup"><span data-stu-id="8a817-121">d2d1.lib, dxguid.lib</span></span>                                                               |



 

## <a name="related-topics"></a><span data-ttu-id="8a817-122">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="8a817-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8a817-123">**ID2D1Effect**</span><span class="sxs-lookup"><span data-stu-id="8a817-123">**ID2D1Effect**</span></span>](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

 
