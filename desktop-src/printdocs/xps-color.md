---
description: Eine-Struktur, die einen einzelnen Farbwert beschreibt.
ms.assetid: 710f3ef1-bbc3-416d-9faf-aa4a716007c2
title: XPS_COLOR (xpsobjectmodel. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 34c148c2a5452154bfe33b0c74d695fe78f0cdad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362662"
---
# <a name="xps_color"></a><span data-ttu-id="42118-103">XPS- \_ Farbe</span><span class="sxs-lookup"><span data-stu-id="42118-103">XPS\_COLOR</span></span>

<span data-ttu-id="42118-104">Eine-Struktur, die einen einzelnen Farbwert beschreibt.</span><span class="sxs-lookup"><span data-stu-id="42118-104">A structure that describes a single color value.</span></span>

``` syntax
typedef union switch (XPS_COLOR_TYPE colorType) value
{
    case XPS_COLOR_TYPE_SRGB:
        struct {
            byte alpha, red, green, blue;
        } sRGB;
    case XPS_COLOR_TYPE_SCRGB:
        struct {
            FLOAT alpha, red, green, blue;
        } scRGB;
    case XPS_COLOR_TYPE_CONTEXT:
        struct {
            byte channelCount;
            FLOAT channels[9];
        } context;
} XPS_COLOR;
```

## <a name="remarks"></a><span data-ttu-id="42118-105">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="42118-105">Remarks</span></span>

<span data-ttu-id="42118-106">Das Format der Struktur hängt vom Wert von *ColorType* ab.</span><span class="sxs-lookup"><span data-stu-id="42118-106">The structure's format depends on the value of *colorType*.</span></span>

<dl>

<span data-ttu-id="42118-107">[**XPS \_ - \_ Farbtyp \_ sRGB**](/previous-versions/windows/desktop/dd372944(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="42118-107">[**XPS\_COLOR\_TYPE\_SRGB**](/previous-versions/windows/desktop/dd372944(v=vs.85))</span></span>  
<span data-ttu-id="42118-108">[**XPS \_ - \_ Farbtyp \_ ScRGB**](/previous-versions/windows/desktop/dd372943(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="42118-108">[**XPS\_COLOR\_TYPE\_SCRGB**](/previous-versions/windows/desktop/dd372943(v=vs.85))</span></span>  
[<span data-ttu-id="42118-109">**XPS \_ - \_ Farbtyp \_ Kontext**</span><span class="sxs-lookup"><span data-stu-id="42118-109">**XPS\_COLOR\_TYPE\_CONTEXT**</span></span>](/windows/win32/api/xpsobjectmodel/ns-xpsobjectmodel-xps_color)  
</dl>

## <a name="requirements"></a><span data-ttu-id="42118-110">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="42118-110">Requirements</span></span>



| <span data-ttu-id="42118-111">Anforderung</span><span class="sxs-lookup"><span data-stu-id="42118-111">Requirement</span></span> | <span data-ttu-id="42118-112">Wert</span><span class="sxs-lookup"><span data-stu-id="42118-112">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="42118-113">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="42118-113">Minimum supported client</span></span><br/> | <span data-ttu-id="42118-114">Windows 7, Windows Vista mit SP2 und Platt Form Update für Windows Vista \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="42118-114">Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                          |
| <span data-ttu-id="42118-115">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="42118-115">Minimum supported server</span></span><br/> | <span data-ttu-id="42118-116">Windows Server 2008 R2, Windows Server 2008 mit SP2 und Platt Form Update für Windows Server 2008 \[ Desktop Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="42118-116">Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="42118-117">Header</span><span class="sxs-lookup"><span data-stu-id="42118-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="42118-118"><dt>Xpsobjectmodel. h</dt></span><span class="sxs-lookup"><span data-stu-id="42118-118"><dt>Xpsobjectmodel.h</dt></span></span> </dl>                                              |
| <span data-ttu-id="42118-119">IDL</span><span class="sxs-lookup"><span data-stu-id="42118-119">IDL</span></span><br/>                      | <dl> <span data-ttu-id="42118-120"><dt>Xpsobjectmodel. idl</dt></span><span class="sxs-lookup"><span data-stu-id="42118-120"><dt>XpsObjectModel.idl</dt></span></span> </dl>                                            |



## <a name="see-also"></a><span data-ttu-id="42118-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="42118-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="42118-122">XML Paper Specification</span><span class="sxs-lookup"><span data-stu-id="42118-122">XML Paper Specification</span></span>](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

