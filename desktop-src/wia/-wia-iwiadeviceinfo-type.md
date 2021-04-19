---
description: Ruft den Typ des Hardware Geräts für die Windows-Abbild Beschaffung (WIA) ab.
ms.assetid: 5f10bcd1-03a0-4cd9-8886-e1f957312c3b
title: DeviceInfo. Type-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DeviceInfo.Type
api_type:
- COM
api_location:
- Wiascr.dll
ms.openlocfilehash: 89a322890f035a1865c01be7c4bfb0bbab812fa7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347821"
---
# <a name="deviceinfotype-property"></a><span data-ttu-id="4161a-103">DeviceInfo. Type-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="4161a-103">DeviceInfo.Type property</span></span>

<span data-ttu-id="4161a-104">Ruft den Typ des Hardware Geräts für die Windows-Abbild Beschaffung (WIA) ab.</span><span class="sxs-lookup"><span data-stu-id="4161a-104">Retrieves the type of Windows Image Acquisition (WIA) hardware device.</span></span> <span data-ttu-id="4161a-105">Dabei sind folgende Werte möglich:</span><span class="sxs-lookup"><span data-stu-id="4161a-105">Possible values are:</span></span>

-   <span data-ttu-id="4161a-106">Digitalcamera</span><span class="sxs-lookup"><span data-stu-id="4161a-106">DigitalCamera</span></span>
-   <span data-ttu-id="4161a-107">Scanner</span><span class="sxs-lookup"><span data-stu-id="4161a-107">Scanner</span></span>
-   <span data-ttu-id="4161a-108">Streamingvideo</span><span class="sxs-lookup"><span data-stu-id="4161a-108">StreamingVideo</span></span>
-   <span data-ttu-id="4161a-109">Standard</span><span class="sxs-lookup"><span data-stu-id="4161a-109">Default</span></span>

<span data-ttu-id="4161a-110">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="4161a-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="4161a-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="4161a-111">Syntax</span></span>


```JScript
propVal = DeviceInfo.Type
```



## <a name="property-value"></a><span data-ttu-id="4161a-112">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="4161a-112">Property value</span></span>

<span data-ttu-id="4161a-113">Zeichenfolge, die das Gerät empfängt.</span><span class="sxs-lookup"><span data-stu-id="4161a-113">String that receives the device.</span></span>

## <a name="requirements"></a><span data-ttu-id="4161a-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4161a-114">Requirements</span></span>



| <span data-ttu-id="4161a-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4161a-115">Requirement</span></span> | <span data-ttu-id="4161a-116">Wert</span><span class="sxs-lookup"><span data-stu-id="4161a-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4161a-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="4161a-117">Minimum supported client</span></span><br/> | <span data-ttu-id="4161a-118">Windows 2000 Professional, Windows XP \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4161a-118">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="4161a-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="4161a-119">Minimum supported server</span></span><br/> | <span data-ttu-id="4161a-120">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4161a-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="4161a-121">DLL</span><span class="sxs-lookup"><span data-stu-id="4161a-121">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4161a-122"><dt>Wiascr.dll (Version 4,90 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="4161a-122"><dt>Wiascr.dll (version 4.90 or later)</dt></span></span> </dl> |



 

 




