---
description: Gibt den Typ des Tablettgeräts an, z. b. einen Stift, eine Maus oder einen Fingerabdruck-Digitalisierungs
ms.assetid: 4cca1e09-99c0-4357-a6ef-159bc8d17d57
title: TABLET_DEVICE_KIND-Enumeration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TABLET_DEVICE_KIND
api_type:
- NA
api_location: ''
ms.openlocfilehash: 18f691a2fa909ef28059a4788f4f8b4e184a61ee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106351129"
---
# <a name="tablet_device_kind-enumeration"></a><span data-ttu-id="be0d5-103">Tablet \_ Device \_ Kind-Enumeration</span><span class="sxs-lookup"><span data-stu-id="be0d5-103">TABLET\_DEVICE\_KIND enumeration</span></span>

<span data-ttu-id="be0d5-104">Gibt den Typ des Tablettgeräts an, z. b. einen Stift, eine Maus oder einen Fingerabdruck-Digitalisierungs</span><span class="sxs-lookup"><span data-stu-id="be0d5-104">Indicates the type of tablet device such as a pen, mouse or touch sensitive digitizer.</span></span>

## <a name="syntax"></a><span data-ttu-id="be0d5-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="be0d5-105">Syntax</span></span>


```C++
typedef enum _TABLET_DEVICE_KIND { 
  TABLET_DEVICE_MOUSE  = 0,
  TABLET_DEVICE_PEN,
  TABLET_DEVICE_TOUCH
} TABLET_DEVICE_KIND;
```



## <a name="constants"></a><span data-ttu-id="be0d5-106">Konstanten</span><span class="sxs-lookup"><span data-stu-id="be0d5-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="be0d5-107"><span id="TABLET_DEVICE_MOUSE"></span><span id="tablet_device_mouse"></span>**\_Tablettgerät- \_ Maus**</span><span class="sxs-lookup"><span data-stu-id="be0d5-107"><span id="TABLET_DEVICE_MOUSE"></span><span id="tablet_device_mouse"></span>**TABLET\_DEVICE\_MOUSE**</span></span>
</dt> <dd>

<span data-ttu-id="be0d5-108">Das Tablet ist eine Maus.</span><span class="sxs-lookup"><span data-stu-id="be0d5-108">The tablet is a mouse.</span></span> <span data-ttu-id="be0d5-109">Dies schließt Touchpads ein, die auf vielen Laptop Computern gefunden wurden.</span><span class="sxs-lookup"><span data-stu-id="be0d5-109">This includes touchpads found on many laptop computers.</span></span>

</dd> <dt>

<span data-ttu-id="be0d5-110"><span id="TABLET_DEVICE_PEN"></span><span id="tablet_device_pen"></span>**\_Tablettgerät \_ Stift**</span><span class="sxs-lookup"><span data-stu-id="be0d5-110"><span id="TABLET_DEVICE_PEN"></span><span id="tablet_device_pen"></span>**TABLET\_DEVICE\_PEN**</span></span>
</dt> <dd>

<span data-ttu-id="be0d5-111">Das Tablet verwendet einen elektromagnetischen Stift und Digitalisierer.</span><span class="sxs-lookup"><span data-stu-id="be0d5-111">The tablet utilizes an electromagnetic pen and digitizer.</span></span>

</dd> <dt>

<span data-ttu-id="be0d5-112"><span id="TABLET_DEVICE_TOUCH"></span><span id="tablet_device_touch"></span>**Tablet \_ Gerät \_ berühren**</span><span class="sxs-lookup"><span data-stu-id="be0d5-112"><span id="TABLET_DEVICE_TOUCH"></span><span id="tablet_device_touch"></span>**TABLET\_DEVICE\_TOUCH**</span></span>
</dt> <dd>

<span data-ttu-id="be0d5-113">Das Tablet verwendet einen Fingerabdruck der Fingereingabe.</span><span class="sxs-lookup"><span data-stu-id="be0d5-113">The tablet utilizes a touch sensitive digitizer.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="be0d5-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="be0d5-114">Requirements</span></span>



| <span data-ttu-id="be0d5-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="be0d5-115">Requirement</span></span> | <span data-ttu-id="be0d5-116">Wert</span><span class="sxs-lookup"><span data-stu-id="be0d5-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="be0d5-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="be0d5-117">Minimum supported client</span></span><br/> | <span data-ttu-id="be0d5-118">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="be0d5-118">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="be0d5-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="be0d5-119">Minimum supported server</span></span><br/> | <span data-ttu-id="be0d5-120">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="be0d5-120">None supported</span></span><br/>                                     |



## <a name="see-also"></a><span data-ttu-id="be0d5-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="be0d5-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="be0d5-122">**ITablet2:: getdevicekind-Methode**</span><span class="sxs-lookup"><span data-stu-id="be0d5-122">**ITablet2::GetDeviceKind Method**</span></span>](itablet2-getdevicekind.md)
</dt> </dl>

 

 




