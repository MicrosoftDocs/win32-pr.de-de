---
title: Iadstimestamp-Eigenschaften Methoden (IADs. h)
description: Die Property-Methode der iadstimestamp-Schnittstelle legt die in der folgenden Tabelle beschriebene Eigenschaft fest. Weitere Informationen finden Sie unter Interface Property Methods.
ms.assetid: 0f00d270-3c11-4c60-95b3-178130e31caa
ms.tgt_platform: multiple
keywords:
- Iadstimestamp-Eigenschaften Methoden ADSI
topic_type:
- apiref
api_name:
- IADsTimestamp Property Methods
- IADsTimestamp.WholeSeconds
- IADsTimestamp.get_WholeSeconds
- IADsTimestamp.put_WholeSeconds
- IADsTimestamp.EventID
- IADsTimestamp.get_EventID
- IADsTimestamp.put_EventID
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a77db7a6a3b3814cd10beca5da5e3166ab1b61a2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476347"
---
# <a name="iadstimestamp-property-methods"></a><span data-ttu-id="91c7b-105">Iadstimestamp-Eigenschaften Methoden</span><span class="sxs-lookup"><span data-stu-id="91c7b-105">IADsTimestamp Property Methods</span></span>

<span data-ttu-id="91c7b-106">Die Property-Methode der [**iadstimestamp**](/windows/desktop/api/Iads/nn-iads-iadstimestamp) -Schnittstelle legt die in der folgenden Tabelle beschriebene Eigenschaft fest.</span><span class="sxs-lookup"><span data-stu-id="91c7b-106">The property method of the [**IADsTimestamp**](/windows/desktop/api/Iads/nn-iads-iadstimestamp) interface sets the property described in the following table.</span></span> <span data-ttu-id="91c7b-107">Weitere Informationen finden Sie unter [Interface Property Methods](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="91c7b-107">For more information, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="91c7b-108">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="91c7b-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="91c7b-109">**EventID**</span><span class="sxs-lookup"><span data-stu-id="91c7b-109">**EventID**</span></span>
<span data-ttu-id="91c7b-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="91c7b-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="91c7b-111">Ein Ereignisbezeichner.</span><span class="sxs-lookup"><span data-stu-id="91c7b-111">An event identifier.</span></span>

<dt>

<span data-ttu-id="91c7b-112">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="91c7b-112">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="91c7b-113">Skript Datentyp: **Long**</span><span class="sxs-lookup"><span data-stu-id="91c7b-113">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_EventID(
  [out] LONG* retval
);
HRESULT put_EventID(
  [in] LONG lnEventID
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="91c7b-114">**Großhandels-econds**</span><span class="sxs-lookup"><span data-stu-id="91c7b-114">**WholeSeconds**</span></span>
<span data-ttu-id="91c7b-115"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="91c7b-115"></dt> <dd> <dl></span></span>

<span data-ttu-id="91c7b-116">Anzahl von Sekunden, wobei der Wert 0 (null) 12:00 Uhr, Januar 1970, UTC ist.</span><span class="sxs-lookup"><span data-stu-id="91c7b-116">Number of seconds with zero value being 12:00 AM, January 1970, UTC.</span></span>

<dt>

<span data-ttu-id="91c7b-117">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="91c7b-117">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="91c7b-118">Skript Datentyp: **Long**</span><span class="sxs-lookup"><span data-stu-id="91c7b-118">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_WholeSeconds(
  [out] LONG* retVal
);
HRESULT put_WholeSeconds(
  [in] LONG lnWholeSeconds
);
```


</dt> </dl> </dd> </dl>

 

## <a name="requirements"></a><span data-ttu-id="91c7b-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="91c7b-119">Requirements</span></span>



| <span data-ttu-id="91c7b-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="91c7b-120">Requirement</span></span> | <span data-ttu-id="91c7b-121">Wert</span><span class="sxs-lookup"><span data-stu-id="91c7b-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="91c7b-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="91c7b-122">Minimum supported client</span></span><br/> | <span data-ttu-id="91c7b-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="91c7b-123">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="91c7b-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="91c7b-124">Minimum supported server</span></span><br/> | <span data-ttu-id="91c7b-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="91c7b-125">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="91c7b-126">Header</span><span class="sxs-lookup"><span data-stu-id="91c7b-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="91c7b-127"><dt>IADs. h</dt></span><span class="sxs-lookup"><span data-stu-id="91c7b-127"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="91c7b-128">DLL</span><span class="sxs-lookup"><span data-stu-id="91c7b-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="91c7b-129"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="91c7b-129"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="91c7b-130">IID</span><span class="sxs-lookup"><span data-stu-id="91c7b-130">IID</span></span><br/>                      | <span data-ttu-id="91c7b-131">IID \_ iadstimestamp ist als B2F5A901-4080-11d1-A3AC-00C04FB950DC definiert.</span><span class="sxs-lookup"><span data-stu-id="91c7b-131">IID\_IADsTimestamp is defined as B2F5A901-4080-11D1-A3AC-00C04FB950DC</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="91c7b-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="91c7b-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="91c7b-133">**IADsTimestamp**</span><span class="sxs-lookup"><span data-stu-id="91c7b-133">**IADsTimestamp**</span></span>](/windows/desktop/api/Iads/nn-iads-iadstimestamp)
</dt> <dt>

[<span data-ttu-id="91c7b-134">**Werbe \_ Zeitstempel**</span><span class="sxs-lookup"><span data-stu-id="91c7b-134">**ADS\_TIMESTAMP**</span></span>](/windows/win32/api/iads/ns-iads-ads_timestamp)
</dt> </dl>

 

 





