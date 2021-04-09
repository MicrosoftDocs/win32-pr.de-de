---
description: Definiert die verschiedenen bereit Zustände der Medienquellen Erweiterung.
ms.assetid: 7455B92F-CC2D-4743-935D-F5EBFD834397
title: MF_MSE_READY-Enumeration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MF_MSE_READY
api_type:
- HeaderDef
api_location:
- mfmediaengine.h
ms.openlocfilehash: bff2155a2cb2cb21d4c25d868f95472f47f15b1a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103865584"
---
# <a name="mf_mse_ready-enumeration"></a><span data-ttu-id="6cc85-103">MF- \_ MSE- \_ Ready-Enumeration</span><span class="sxs-lookup"><span data-stu-id="6cc85-103">MF\_MSE\_READY enumeration</span></span>

<span data-ttu-id="6cc85-104">Definiert die verschiedenen bereit Zustände der Medienquellen Erweiterung.</span><span class="sxs-lookup"><span data-stu-id="6cc85-104">Defines the different ready states of the Media Source Extension.</span></span>

## <a name="syntax"></a><span data-ttu-id="6cc85-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="6cc85-105">Syntax</span></span>


```C++
typedef enum _MF_MSE_READY { 
  MF_MSE_READY_CLOSED  = 1,
  MF_MSE_READY_OPEN    = 2,
  MF_MSE_READY_ENDED   = 3
} MF_MSE_READY;
```



## <a name="constants"></a><span data-ttu-id="6cc85-106">Konstanten</span><span class="sxs-lookup"><span data-stu-id="6cc85-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="6cc85-107"><span id="MF_MSE_READY_CLOSED"></span><span id="mf_mse_ready_closed"></span>**MF- \_ MSE \_ Ready \_ geschlossen**</span><span class="sxs-lookup"><span data-stu-id="6cc85-107"><span id="MF_MSE_READY_CLOSED"></span><span id="mf_mse_ready_closed"></span>**MF\_MSE\_READY\_CLOSED**</span></span>
</dt> <dd>

<span data-ttu-id="6cc85-108">Die Medienquelle ist geschlossen.</span><span class="sxs-lookup"><span data-stu-id="6cc85-108">The media source is closed.</span></span>

</dd> <dt>

<span data-ttu-id="6cc85-109"><span id="MF_MSE_READY_OPEN"></span><span id="mf_mse_ready_open"></span>**MF- \_ MSE \_ bereit \_**</span><span class="sxs-lookup"><span data-stu-id="6cc85-109"><span id="MF_MSE_READY_OPEN"></span><span id="mf_mse_ready_open"></span>**MF\_MSE\_READY\_OPEN**</span></span>
</dt> <dd>

<span data-ttu-id="6cc85-110">Die Medienquelle ist geöffnet.</span><span class="sxs-lookup"><span data-stu-id="6cc85-110">The media source is open.</span></span>

</dd> <dt>

<span data-ttu-id="6cc85-111"><span id="MF_MSE_READY_ENDED"></span><span id="mf_mse_ready_ended"></span>**MF- \_ MSE- \_ Ready \_ beendet**</span><span class="sxs-lookup"><span data-stu-id="6cc85-111"><span id="MF_MSE_READY_ENDED"></span><span id="mf_mse_ready_ended"></span>**MF\_MSE\_READY\_ENDED**</span></span>
</dt> <dd>

<span data-ttu-id="6cc85-112">Die Medienquelle wurde beendet.</span><span class="sxs-lookup"><span data-stu-id="6cc85-112">The media source is ended.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6cc85-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6cc85-113">Requirements</span></span>



| <span data-ttu-id="6cc85-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6cc85-114">Requirement</span></span> | <span data-ttu-id="6cc85-115">Wert</span><span class="sxs-lookup"><span data-stu-id="6cc85-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="6cc85-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6cc85-116">Minimum supported client</span></span><br/> | <span data-ttu-id="6cc85-117">\[Nur Desktop-Apps Windows 8.1\]</span><span class="sxs-lookup"><span data-stu-id="6cc85-117">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="6cc85-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6cc85-118">Minimum supported server</span></span><br/> | <span data-ttu-id="6cc85-119">Nur Windows Server 2012 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6cc85-119">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="6cc85-120">IDL</span><span class="sxs-lookup"><span data-stu-id="6cc85-120">IDL</span></span><br/>                      | <dl> <span data-ttu-id="6cc85-121"><dt>MF mediaengine. idl</dt></span><span class="sxs-lookup"><span data-stu-id="6cc85-121"><dt>Mfmediaengine.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6cc85-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6cc85-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6cc85-123">Media Foundation Enumerationen</span><span class="sxs-lookup"><span data-stu-id="6cc85-123">Media Foundation Enumerations</span></span>](media-foundation-enumerations.md)
</dt> </dl>

 

 




