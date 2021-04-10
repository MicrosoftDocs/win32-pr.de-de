---
title: Imageliststateflags (kommctrl. h)
description: Die folgenden Flags werden an die IImageList-Draw-Methode im fstate-Member von imagelistdrawparameams übergeben.
ms.assetid: a22b4acf-c290-44b2-9216-b006d0326236
topic_type:
- apiref
api_name:
- ILS_NORMAL
- ILS_GLOW
- ILS_SHADOW
- ILS_SATURATE
- ILS_ALPHA
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fea580294f54b6e2fc5c3e5b6aee1119811c22e8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040443"
---
# <a name="imageliststateflags"></a><span data-ttu-id="bbaa8-103">Imageliststateflags</span><span class="sxs-lookup"><span data-stu-id="bbaa8-103">IMAGELISTSTATEFLAGS</span></span>

<span data-ttu-id="bbaa8-104">Die folgenden Flags werden an die [**IImageList::D RAW**](/windows/desktop/api/CommonControls/nf-commoncontrols-iimagelist-draw) -Methode im **fstate** -Member von [**imagelistdrawparameams**](/windows/win32/api/commctrl/ns-commctrl-imagelistdrawparams)übergeben.</span><span class="sxs-lookup"><span data-stu-id="bbaa8-104">The following flags are passed to the [**IImageList::Draw**](/windows/desktop/api/CommonControls/nf-commoncontrols-iimagelist-draw) method in the **fState** member of [**IMAGELISTDRAWPARAMS**](/windows/win32/api/commctrl/ns-commctrl-imagelistdrawparams).</span></span>



| <span data-ttu-id="bbaa8-105">Konstante/Wert</span><span class="sxs-lookup"><span data-stu-id="bbaa8-105">Constant/value</span></span>                                                                                                                                                                                                             | <span data-ttu-id="bbaa8-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="bbaa8-106">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                   |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="ILS_NORMAL"></span><span id="ils_normal"></span><dl> <span data-ttu-id="bbaa8-107"><dt>**ILS \_ Normales**</dt> <dt>0x00000000</dt></span><span class="sxs-lookup"><span data-stu-id="bbaa8-107"><dt>**ILS\_NORMAL**</dt> <dt>0x00000000</dt></span></span> </dl>       | <span data-ttu-id="bbaa8-108">Der Bild Zustand wird nicht geändert.</span><span class="sxs-lookup"><span data-stu-id="bbaa8-108">The image state is not modified.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                   |
| <span id="ILS_GLOW"></span><span id="ils_glow"></span><dl> <span data-ttu-id="bbaa8-109"><dt>**ILS \_ Glanz**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="bbaa8-109"><dt>**ILS\_GLOW**</dt> <dt>0x00000001</dt></span></span> </dl>             | <span data-ttu-id="bbaa8-110">Wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="bbaa8-110">Not supported.</span></span> <br/>                                                                                                                                                                                                                                                                                                                                                                    |
| <span id="ILS_SHADOW"></span><span id="ils_shadow"></span><dl> <span data-ttu-id="bbaa8-111"><dt>**ILS \_ Schatten**</dt> <dt>0x00000002</dt></span><span class="sxs-lookup"><span data-stu-id="bbaa8-111"><dt>**ILS\_SHADOW**</dt> <dt>0x00000002</dt></span></span> </dl>       | <span data-ttu-id="bbaa8-112">Wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="bbaa8-112">Not supported.</span></span> <br/>                                                                                                                                                                                                                                                                                                                                                                    |
| <span id="ILS_SATURATE"></span><span id="ils_saturate"></span><dl> <span data-ttu-id="bbaa8-113"><dt>**ILS \_ Voll**</dt> ständig <dt>0x00000004</dt></span><span class="sxs-lookup"><span data-stu-id="bbaa8-113"><dt>**ILS\_SATURATE**</dt> <dt>0x00000004</dt></span></span> </dl> | <span data-ttu-id="bbaa8-114">Verringert die Farbsättigung des Symbols auf Graustufen.</span><span class="sxs-lookup"><span data-stu-id="bbaa8-114">Reduces the color saturation of the icon to grayscale.</span></span> <span data-ttu-id="bbaa8-115">Dies betrifft nur 32 bpp-Images.</span><span class="sxs-lookup"><span data-stu-id="bbaa8-115">This only affects 32bpp images.</span></span> <br/>                                                                                                                                                                                                                                                                                            |
| <span id="ILS_ALPHA"></span><span id="ils_alpha"></span><dl> <span data-ttu-id="bbaa8-116"><dt>**ILS \_ Alpha**</dt> <dt>0x00000008</dt></span><span class="sxs-lookup"><span data-stu-id="bbaa8-116"><dt>**ILS\_ALPHA**</dt> <dt>0x00000008</dt></span></span> </dl>          | <span data-ttu-id="bbaa8-117">Alpha blendet das Symbol aus.</span><span class="sxs-lookup"><span data-stu-id="bbaa8-117">Alpha blends the icon.</span></span> <span data-ttu-id="bbaa8-118">Alpha Blending steuert die Transparenz Ebene eines Symbols entsprechend dem Wert des Alphakanals.</span><span class="sxs-lookup"><span data-stu-id="bbaa8-118">Alpha blending controls the transparency level of an icon, according to the value of its alpha channel.</span></span> <span data-ttu-id="bbaa8-119">Der Wert des Alphakanals wird durch das **Frame** -Element in der [**imagelistdrawparameams**](/windows/win32/api/commctrl/ns-commctrl-imagelistdrawparams) -Methode angegeben.</span><span class="sxs-lookup"><span data-stu-id="bbaa8-119">The value of the alpha channel is indicated by the **frame** member in the [**IMAGELISTDRAWPARAMS**](/windows/win32/api/commctrl/ns-commctrl-imagelistdrawparams) method.</span></span> <span data-ttu-id="bbaa8-120">Der Alphakanal kann zwischen 0 und 255 liegen, wobei 0 vollständig transparent ist und 255 vollständig deckend ist.</span><span class="sxs-lookup"><span data-stu-id="bbaa8-120">The alpha channel can be from 0 to 255, with 0 being completely transparent, and 255 being completely opaque.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="bbaa8-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bbaa8-121">Requirements</span></span>



| <span data-ttu-id="bbaa8-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="bbaa8-122">Requirement</span></span> | <span data-ttu-id="bbaa8-123">Wert</span><span class="sxs-lookup"><span data-stu-id="bbaa8-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="bbaa8-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="bbaa8-124">Minimum supported client</span></span><br/> | <span data-ttu-id="bbaa8-125">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="bbaa8-125">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="bbaa8-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="bbaa8-126">Minimum supported server</span></span><br/> | <span data-ttu-id="bbaa8-127">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="bbaa8-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="bbaa8-128">Header</span><span class="sxs-lookup"><span data-stu-id="bbaa8-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="bbaa8-129"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="bbaa8-129"><dt>Commctrl.h</dt></span></span> </dl> |



 

