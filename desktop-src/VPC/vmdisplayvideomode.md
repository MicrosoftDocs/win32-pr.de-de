---
title: Vmdisplayvideomode-Enumeration (vpccominterfaces. h)
description: Gibt den Videomodus für die Anzeige an.
ms.assetid: 9ffd1bb5-115d-4554-92c6-5dcf86f904a5
keywords:
- Vmdisplayvideomode-Enumeration virtueller PC
topic_type:
- apiref
api_name:
- VMDisplayVideoMode
api_location:
- VPCCOMInterfaces.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0b159a8c251c83643ae9897842b313ea9be567e4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476545"
---
# <a name="vmdisplayvideomode-enumeration"></a><span data-ttu-id="0703a-104">Vmdisplayvideomode-Enumeration</span><span class="sxs-lookup"><span data-stu-id="0703a-104">VMDisplayVideoMode enumeration</span></span>

<span data-ttu-id="0703a-105">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="0703a-105">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="0703a-106">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="0703a-106">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="0703a-107">Gibt den Videomodus für die Anzeige an.</span><span class="sxs-lookup"><span data-stu-id="0703a-107">Specifies the display video mode.</span></span>

## <a name="syntax"></a><span data-ttu-id="0703a-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="0703a-108">Syntax</span></span>


```C++
typedef enum  { 
  vmVideoMode_TextMode  = 0,
  vmVideoMode_CGAMode   = 1,
  vmVideoMode_VGAMode   = 2,
  vmVideoMode_SVGAMode  = 3
} VMDisplayVideoMode;
```



## <a name="constants"></a><span data-ttu-id="0703a-109">Konstanten</span><span class="sxs-lookup"><span data-stu-id="0703a-109">Constants</span></span>

<dl> <dt>

<span data-ttu-id="0703a-110"><span id="vmVideoMode_TextMode"></span><span id="vmvideomode_textmode"></span><span id="VMVIDEOMODE_TEXTMODE"></span>**vmvideomode- \_ TextMode**</span><span class="sxs-lookup"><span data-stu-id="0703a-110"><span id="vmVideoMode_TextMode"></span><span id="vmvideomode_textmode"></span><span id="VMVIDEOMODE_TEXTMODE"></span>**vmVideoMode\_TextMode**</span></span>
</dt> <dd>

<span data-ttu-id="0703a-111">Textmodus.</span><span class="sxs-lookup"><span data-stu-id="0703a-111">Text mode.</span></span>

</dd> <dt>

<span data-ttu-id="0703a-112"><span id="vmVideoMode_CGAMode"></span><span id="vmvideomode_cgamode"></span><span id="VMVIDEOMODE_CGAMODE"></span>**vmvideomode \_ cgamode**</span><span class="sxs-lookup"><span data-stu-id="0703a-112"><span id="vmVideoMode_CGAMode"></span><span id="vmvideomode_cgamode"></span><span id="VMVIDEOMODE_CGAMODE"></span>**vmVideoMode\_CGAMode**</span></span>
</dt> <dd>

<span data-ttu-id="0703a-113">CGA-Modus.</span><span class="sxs-lookup"><span data-stu-id="0703a-113">CGA mode.</span></span>

</dd> <dt>

<span data-ttu-id="0703a-114"><span id="vmVideoMode_VGAMode"></span><span id="vmvideomode_vgamode"></span><span id="VMVIDEOMODE_VGAMODE"></span>**vmvideomode \_ vgamode**</span><span class="sxs-lookup"><span data-stu-id="0703a-114"><span id="vmVideoMode_VGAMode"></span><span id="vmvideomode_vgamode"></span><span id="VMVIDEOMODE_VGAMODE"></span>**vmVideoMode\_VGAMode**</span></span>
</dt> <dd>

<span data-ttu-id="0703a-115">Der VGA-Modus.</span><span class="sxs-lookup"><span data-stu-id="0703a-115">VGA mode.</span></span>

</dd> <dt>

<span data-ttu-id="0703a-116"><span id="vmVideoMode_SVGAMode"></span><span id="vmvideomode_svgamode"></span><span id="VMVIDEOMODE_SVGAMODE"></span>**vmvideomode \_ svgamode**</span><span class="sxs-lookup"><span data-stu-id="0703a-116"><span id="vmVideoMode_SVGAMode"></span><span id="vmvideomode_svgamode"></span><span id="VMVIDEOMODE_SVGAMODE"></span>**vmVideoMode\_SVGAMode**</span></span>
</dt> <dd>

<span data-ttu-id="0703a-117">SVGA-Modus.</span><span class="sxs-lookup"><span data-stu-id="0703a-117">SVGA mode.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0703a-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0703a-118">Requirements</span></span>



| <span data-ttu-id="0703a-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0703a-119">Requirement</span></span> | <span data-ttu-id="0703a-120">Wert</span><span class="sxs-lookup"><span data-stu-id="0703a-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="0703a-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0703a-121">Minimum supported client</span></span><br/> | <span data-ttu-id="0703a-122">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0703a-122">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="0703a-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0703a-123">Minimum supported server</span></span><br/> | <span data-ttu-id="0703a-124">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="0703a-124">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="0703a-125">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="0703a-125">End of client support</span></span><br/>    | <span data-ttu-id="0703a-126">Windows 7</span><span class="sxs-lookup"><span data-stu-id="0703a-126">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="0703a-127">Produkt</span><span class="sxs-lookup"><span data-stu-id="0703a-127">Product</span></span><br/>                  | <span data-ttu-id="0703a-128">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="0703a-128">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="0703a-129">Header</span><span class="sxs-lookup"><span data-stu-id="0703a-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="0703a-130"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="0703a-130"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0703a-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0703a-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0703a-132">**Ivmdisplay:: videomode**</span><span class="sxs-lookup"><span data-stu-id="0703a-132">**IVMDisplay::VideoMode**</span></span>](ivmdisplay-videomode.md)
</dt> </dl>

 

