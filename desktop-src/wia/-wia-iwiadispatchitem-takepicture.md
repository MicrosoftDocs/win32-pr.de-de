---
description: Die takepicture-Methode des Item-Objekts bewirkt, dass ein digitales Kamera Gerät ein Bild annimmt und ein Element Objekt zurückgibt, das das resultierende Bild darstellt. Diese Methode gilt nur für digitale Kamerageräte.
ms.assetid: d181048e-21ef-4fcc-a50a-5ba44bbde72e
title: Item. takepicture-Methode (WiaVideo. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Item.TakePicture
api_type:
- COM
api_location:
- Wiascr.dll
ms.openlocfilehash: fd07f7ccd4f2c65c2d911dabdd0ca829dc241765
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959819"
---
# <a name="itemtakepicture-method"></a><span data-ttu-id="4671d-104">Item. takepicture-Methode</span><span class="sxs-lookup"><span data-stu-id="4671d-104">Item.TakePicture method</span></span>

<span data-ttu-id="4671d-105">Die **takepicture** -Methode des [**Item**](-wia-item.md) -Objekts bewirkt, dass ein digitales Kamera Gerät ein Bild annimmt und ein **Element** Objekt zurückgibt, das das resultierende Bild darstellt.</span><span class="sxs-lookup"><span data-stu-id="4671d-105">The **TakePicture** method of the [**Item**](-wia-item.md) object causes a digital camera device to take a picture and returns an **Item** object that represents the resulting image.</span></span> <span data-ttu-id="4671d-106">Diese Methode gilt nur für digitale Kamerageräte.</span><span class="sxs-lookup"><span data-stu-id="4671d-106">This method applies only to digital camera devices.</span></span>

## <a name="syntax"></a><span data-ttu-id="4671d-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="4671d-107">Syntax</span></span>


```JScript
retVal = Item.TakePicture()
```



## <a name="parameters"></a><span data-ttu-id="4671d-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="4671d-108">Parameters</span></span>

<span data-ttu-id="4671d-109">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="4671d-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="4671d-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4671d-110">Return value</span></span>

<span data-ttu-id="4671d-111">Typ: **iwiadispatchitem**</span><span class="sxs-lookup"><span data-stu-id="4671d-111">Type: **IWiaDispatchItem**</span></span>

<span data-ttu-id="4671d-112">Ein [**Element**](-wia-item.md) Objekt, das das Bild darstellt, das von dieser Methode erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="4671d-112">An [**Item**](-wia-item.md) object that represents the image that this method creates.</span></span>

## <a name="requirements"></a><span data-ttu-id="4671d-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4671d-113">Requirements</span></span>



| <span data-ttu-id="4671d-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4671d-114">Requirement</span></span> | <span data-ttu-id="4671d-115">Wert</span><span class="sxs-lookup"><span data-stu-id="4671d-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4671d-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="4671d-116">Minimum supported client</span></span><br/> | <span data-ttu-id="4671d-117">Windows 2000 Professional, Windows XP \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4671d-117">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="4671d-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="4671d-118">Minimum supported server</span></span><br/> | <span data-ttu-id="4671d-119">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4671d-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="4671d-120">Header</span><span class="sxs-lookup"><span data-stu-id="4671d-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="4671d-121"><dt>WiaVideo. h</dt></span><span class="sxs-lookup"><span data-stu-id="4671d-121"><dt>Wiavideo.h</dt></span></span> </dl>                         |
| <span data-ttu-id="4671d-122">DLL</span><span class="sxs-lookup"><span data-stu-id="4671d-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4671d-123"><dt>Wiascr.dll (Version 4,90 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="4671d-123"><dt>Wiascr.dll (version 4.90 or later)</dt></span></span> </dl> |



 

 




