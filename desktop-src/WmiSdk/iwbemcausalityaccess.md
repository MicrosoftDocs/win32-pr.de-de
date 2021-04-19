---
description: Verfolgt die untergeordneten Anforderungen, die von einer übergeordneten Anforderung generiert werden.
ms.assetid: e1d98eae-6fc1-489b-aa8b-2e86bac5c65a
ms.tgt_platform: multiple
title: Iwbemkausalityaccess-Schnittstelle (wbemint. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWbemCausalityAccess
api_type:
- COM
api_location:
- Fastprox.dll
ms.openlocfilehash: db4c7a76b04b659cd467f7a4a7a9a8c1ba42721f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106359205"
---
# <a name="iwbemcausalityaccess-interface"></a><span data-ttu-id="552a5-103">Iwbemkausalityaccess-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="552a5-103">IWbemCausalityAccess interface</span></span>

<span data-ttu-id="552a5-104">Die **iwbemkausalityaccess** -Schnittstelle verfolgt die untergeordneten Anforderungen, die von einer übergeordneten Anforderung generiert werden.</span><span class="sxs-lookup"><span data-stu-id="552a5-104">The **IWbemCausalityAccess** interface keeps track of child requests that are generated from a parent request.</span></span> <span data-ttu-id="552a5-105">Sie können ein **iwbemkausalityaccess** -Objekt mit einer Abfrage Schnittstelle (Qi) für [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext)abrufen.</span><span class="sxs-lookup"><span data-stu-id="552a5-105">You can obtain an **IWbemCausalityAccess** object by using a query interface (QI) for [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext).</span></span> <span data-ttu-id="552a5-106">Jede Anforderung wird durch einen global eindeutigen Bezeichner (GUID) identifiziert und kann über eine übergeordnete Anforderung verfügen oder eine Top-Anforderung sein.</span><span class="sxs-lookup"><span data-stu-id="552a5-106">Each request is identified by a Globally Unique Identifier (GUID) and can have a parent request or can be a top request.</span></span> <span data-ttu-id="552a5-107">Eine GUID ist eine eindeutige 128-Bit-Zahl.</span><span class="sxs-lookup"><span data-stu-id="552a5-107">A GUID is a unique 128-bit number.</span></span> <span data-ttu-id="552a5-108">Beispiel: 5b2fc63a-8af4-44cb-960c-aefdced908d6.</span><span class="sxs-lookup"><span data-stu-id="552a5-108">For example, 5b2fc63a-8af4-44cb-960c-aefdced908d6.</span></span>

## <a name="members"></a><span data-ttu-id="552a5-109">Member</span><span class="sxs-lookup"><span data-stu-id="552a5-109">Members</span></span>

<span data-ttu-id="552a5-110">Die **iwbemkausalityaccess** -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="552a5-110">The **IWbemCausalityAccess** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="552a5-111">**Iwbemkausalityaccess** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="552a5-111">**IWbemCausalityAccess** also has these types of members:</span></span>

-   [<span data-ttu-id="552a5-112">Methoden</span><span class="sxs-lookup"><span data-stu-id="552a5-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="552a5-113">Methoden</span><span class="sxs-lookup"><span data-stu-id="552a5-113">Methods</span></span>

<span data-ttu-id="552a5-114">Die **iwbemkausalityaccess** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="552a5-114">The **IWbemCausalityAccess** interface has these methods.</span></span>



| <span data-ttu-id="552a5-115">Methode</span><span class="sxs-lookup"><span data-stu-id="552a5-115">Method</span></span>                                                    | <span data-ttu-id="552a5-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="552a5-116">Description</span></span>                                                                                                                                                             |
|:----------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="552a5-117">**GetRequestID**</span><span class="sxs-lookup"><span data-stu-id="552a5-117">**GetRequestId**</span></span>](iwbemcausalityaccess-getrequestid.md) | <span data-ttu-id="552a5-118">Gibt einen eindeutigen GUID-Bezeichner für eine Anforderung zurück.</span><span class="sxs-lookup"><span data-stu-id="552a5-118">Returns a unique GUID identifier for a request.</span></span><br/>                                                                                                              |
| [<span data-ttu-id="552a5-119">**Ischildof**</span><span class="sxs-lookup"><span data-stu-id="552a5-119">**IsChildOf**</span></span>](iwbemcausalityaccess-ischildof.md)       | <span data-ttu-id="552a5-120">Bestimmt, ob eine Anforderung ein untergeordnetes Element einer angegebenen übergeordneten Anforderung ist.</span><span class="sxs-lookup"><span data-stu-id="552a5-120">Determines if a request is a child of a specified parent request.</span></span> <span data-ttu-id="552a5-121">Eine übergeordnete Anforderung kann über mehrere untergeordnete Anforderungen verfügen, die jeweils durch einen eindeutigen GUID-Wert identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="552a5-121">A parent request can have multiple child requests, each identified by a unique GUID value.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="552a5-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="552a5-122">Requirements</span></span>



| <span data-ttu-id="552a5-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="552a5-123">Requirement</span></span> | <span data-ttu-id="552a5-124">Wert</span><span class="sxs-lookup"><span data-stu-id="552a5-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="552a5-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="552a5-125">Minimum supported client</span></span><br/> | <span data-ttu-id="552a5-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="552a5-126">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="552a5-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="552a5-127">Minimum supported server</span></span><br/> | <span data-ttu-id="552a5-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="552a5-128">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="552a5-129">Header</span><span class="sxs-lookup"><span data-stu-id="552a5-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="552a5-130"><dt>Wbemint. h</dt></span><span class="sxs-lookup"><span data-stu-id="552a5-130"><dt>Wbemint.h</dt></span></span> </dl>    |
| <span data-ttu-id="552a5-131">DLL</span><span class="sxs-lookup"><span data-stu-id="552a5-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="552a5-132"><dt>Fastprox.dll</dt></span><span class="sxs-lookup"><span data-stu-id="552a5-132"><dt>Fastprox.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="552a5-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="552a5-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="552a5-134">COM-API für WMI</span><span class="sxs-lookup"><span data-stu-id="552a5-134">COM API for WMI</span></span>](com-api-for-wmi.md)
</dt> </dl>

 

