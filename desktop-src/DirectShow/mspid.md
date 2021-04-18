---
description: Beachten Sie, dass diese API veraltet ist. Diese sollten von neuen Anwendungen nicht verwendet werden. Der mspid-Datentyp identifiziert den Zweck eines Medien Dampfes.
ms.assetid: 83a84eb7-a72c-4ca7-b152-8cc81a5bfdaf
title: Mspid (mmstream. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8464882aa018a373345f15c0a5639107d9beebf9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365712"
---
# <a name="mspid"></a><span data-ttu-id="18524-105">Mspid</span><span class="sxs-lookup"><span data-stu-id="18524-105">MSPID</span></span>

> [!Note]  
> <span data-ttu-id="18524-106">Diese API ist veraltet.</span><span class="sxs-lookup"><span data-stu-id="18524-106">This API is deprecated.</span></span> <span data-ttu-id="18524-107">Diese sollten von neuen Anwendungen nicht verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="18524-107">New applications should not use it.</span></span>

 

<span data-ttu-id="18524-108">Der **mspid-** Datentyp identifiziert den Zweck eines Medien Dampfes.</span><span class="sxs-lookup"><span data-stu-id="18524-108">The **MSPID** data type identifies the purpose of a media steam.</span></span>


```C++
typedef GUID MSPID;
typedef REFGUID REFMSPID;
```



## <a name="remarks"></a><span data-ttu-id="18524-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="18524-109">Remarks</span></span>

<span data-ttu-id="18524-110">**Mspid** ist einfach eine typedef für GUID.</span><span class="sxs-lookup"><span data-stu-id="18524-110">**MSPID** is simply a typedef for GUID.</span></span> <span data-ttu-id="18524-111">Die folgenden mspids sind definiert.</span><span class="sxs-lookup"><span data-stu-id="18524-111">The following MSPIDs are defined.</span></span>



| <span data-ttu-id="18524-112">Wert</span><span class="sxs-lookup"><span data-stu-id="18524-112">Value</span></span>               | <span data-ttu-id="18524-113">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="18524-113">Description</span></span>           |
|---------------------|-----------------------|
| <span data-ttu-id="18524-114">Mspid \_ primaryvideo</span><span class="sxs-lookup"><span data-stu-id="18524-114">MSPID\_PrimaryVideo</span></span> | <span data-ttu-id="18524-115">Primärer Videostream.</span><span class="sxs-lookup"><span data-stu-id="18524-115">Primary video stream.</span></span> |
| <span data-ttu-id="18524-116">Mspid \_ primaryaudio</span><span class="sxs-lookup"><span data-stu-id="18524-116">MSPID\_PrimaryAudio</span></span> | <span data-ttu-id="18524-117">Primärer Audiodatenstrom.</span><span class="sxs-lookup"><span data-stu-id="18524-117">Primary audio stream.</span></span> |



 

<span data-ttu-id="18524-118">Der **refmspid-** Typ definiert einen Verweis auf eine **mspid**.</span><span class="sxs-lookup"><span data-stu-id="18524-118">The **REFMSPID** type defines a reference to an **MSPID**.</span></span>

## <a name="requirements"></a><span data-ttu-id="18524-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="18524-119">Requirements</span></span>



| <span data-ttu-id="18524-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="18524-120">Requirement</span></span> | <span data-ttu-id="18524-121">Wert</span><span class="sxs-lookup"><span data-stu-id="18524-121">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="18524-122">Header</span><span class="sxs-lookup"><span data-stu-id="18524-122">Header</span></span><br/> | <dl> <span data-ttu-id="18524-123"><dt>Mmstream. h</dt></span><span class="sxs-lookup"><span data-stu-id="18524-123"><dt>Mmstream.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="18524-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="18524-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="18524-125">Multimedia-streamingdatentypen</span><span class="sxs-lookup"><span data-stu-id="18524-125">Multimedia Streaming Data Types</span></span>](multimedia-streaming-data-types.md)
</dt> </dl>

 

 




