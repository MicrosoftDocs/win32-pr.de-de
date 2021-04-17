---
description: Ruft die Versionsnummer des Ereignis Systems ab.
ms.assetid: 6355f1b3-e1e7-435f-9795-d92464e004ae
title: 'IEventSystem2:: GetVersion-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEventSystem2.GetVersion
api_type:
- COM
api_location: ''
ms.openlocfilehash: 2c75538d9fd71cb8ee81e454249fd5116ccd090c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483870"
---
# <a name="ieventsystem2getversion-method"></a><span data-ttu-id="32d6d-103">IEventSystem2:: GetVersion-Methode</span><span class="sxs-lookup"><span data-stu-id="32d6d-103">IEventSystem2::GetVersion method</span></span>

<span data-ttu-id="32d6d-104">Ruft die Versionsnummer des Ereignis Systems ab.</span><span class="sxs-lookup"><span data-stu-id="32d6d-104">Retrieves the version number of the event system.</span></span>

## <a name="syntax"></a><span data-ttu-id="32d6d-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="32d6d-105">Syntax</span></span>


```C++
HRESULT GetVersion(
  [out] int *pnVersion
);
```



## <a name="parameters"></a><span data-ttu-id="32d6d-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="32d6d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="32d6d-107">*pnVersion* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="32d6d-107">*pnVersion* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="32d6d-108">Die Versionsnummer des Ereignis Systems.</span><span class="sxs-lookup"><span data-stu-id="32d6d-108">The version number of the event system.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="32d6d-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="32d6d-109">Return value</span></span>

<span data-ttu-id="32d6d-110">Diese Methode kann die Standard Rückgabewerte e \_ invalidArg, e \_ outo fmemory, e \_ unerwartet, e \_ Fail und S OK \_ zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="32d6d-110">This method can return the standard return values E\_INVALIDARG, E\_OUTOFMEMORY, E\_UNEXPECTED, E\_FAIL, and S\_OK.</span></span>

## <a name="requirements"></a><span data-ttu-id="32d6d-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="32d6d-111">Requirements</span></span>



| <span data-ttu-id="32d6d-112">Anforderung</span><span class="sxs-lookup"><span data-stu-id="32d6d-112">Requirement</span></span> | <span data-ttu-id="32d6d-113">Wert</span><span class="sxs-lookup"><span data-stu-id="32d6d-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="32d6d-114">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="32d6d-114">Minimum supported client</span></span><br/> | <span data-ttu-id="32d6d-115">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="32d6d-115">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="32d6d-116">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="32d6d-116">Minimum supported server</span></span><br/> | <span data-ttu-id="32d6d-117">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="32d6d-117">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="32d6d-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="32d6d-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="32d6d-119">**IEventSystem2**</span><span class="sxs-lookup"><span data-stu-id="32d6d-119">**IEventSystem2**</span></span>](ieventsystem2.md)
</dt> </dl>

 

 




