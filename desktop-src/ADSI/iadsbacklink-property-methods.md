---
title: Iadsbacklink-Eigenschaften Methoden (IADs. h)
description: Die-Eigenschaften Methode der iadsbacklink-Schnittstelle legt die-Eigenschaft fest, die in der folgenden Tabelle beschrieben wird. Weitere Informationen finden Sie unter Interface Property Methods.
ms.assetid: 0a66fa6d-1bf5-4ff0-8bbd-625a69cf9594
ms.tgt_platform: multiple
keywords:
- Iadsbacklink-Eigenschaften Methoden ADSI
topic_type:
- apiref
api_name:
- IADsBackLink Property Methods
- IADsBackLink.RemoteID
- IADsBackLink.get_RemoteID
- IADsBackLink.put_RemoteID
- IADsBackLink.ObjectName
- IADsBackLink.get_ObjectName
- IADsBackLink.put_ObjectName
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1c2220fff3a18b0822c0167b387ec10c324d95aa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105158"
---
# <a name="iadsbacklink-property-methods"></a><span data-ttu-id="fafa7-105">Iadsbacklink-Eigenschaften Methoden</span><span class="sxs-lookup"><span data-stu-id="fafa7-105">IADsBackLink Property Methods</span></span>

<span data-ttu-id="fafa7-106">Die-Eigenschaften Methode der [**iadsbacklink**](/windows/desktop/api/Iads/nn-iads-iadsbacklink) -Schnittstelle legt die-Eigenschaft fest, die in der folgenden Tabelle beschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="fafa7-106">The property method of the [**IADsBackLink**](/windows/desktop/api/Iads/nn-iads-iadsbacklink) interface sets the property described in the following table.</span></span> <span data-ttu-id="fafa7-107">Weitere Informationen finden Sie unter [Interface Property Methods](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="fafa7-107">For more information, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="fafa7-108">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="fafa7-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="fafa7-109">**ObjectName**</span><span class="sxs-lookup"><span data-stu-id="fafa7-109">**ObjectName**</span></span>
<span data-ttu-id="fafa7-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="fafa7-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="fafa7-111">Der Name eines Objekts, an das das **Backlinkattribut** angefügt ist.</span><span class="sxs-lookup"><span data-stu-id="fafa7-111">The name of an object the **Back Link** attribute is attached to.</span></span>

<dt>

<span data-ttu-id="fafa7-112">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="fafa7-112">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="fafa7-113">Skript Datentyp: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="fafa7-113">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_ObjectName(
  [out] BSTR* retval
);
HRESULT put_ObjectName(
  [in] BSTR bstrSubjectName
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="fafa7-114">**RemoteID**</span><span class="sxs-lookup"><span data-stu-id="fafa7-114">**RemoteID**</span></span>
<span data-ttu-id="fafa7-115"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="fafa7-115"></dt> <dd> <dl></span></span>

<span data-ttu-id="fafa7-116">Der Bezeichner des Remote Servers, der einen externen Verweis auf das durch **objectName** angegebene Objekt erfordert.</span><span class="sxs-lookup"><span data-stu-id="fafa7-116">The identifier of the remote server that requires an external reference of the object specified by **ObjectName**.</span></span>

<dt>

<span data-ttu-id="fafa7-117">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="fafa7-117">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="fafa7-118">Skript Datentyp: **Long**</span><span class="sxs-lookup"><span data-stu-id="fafa7-118">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_RemoteID(
  [out] LONG* retVal
);
HRESULT put_RemoteID(
  [in] LONG bstrProtectedAttrName
);
```


</dt> </dl> </dd> </dl>

 

## <a name="requirements"></a><span data-ttu-id="fafa7-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fafa7-119">Requirements</span></span>



| <span data-ttu-id="fafa7-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fafa7-120">Requirement</span></span> | <span data-ttu-id="fafa7-121">Wert</span><span class="sxs-lookup"><span data-stu-id="fafa7-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fafa7-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="fafa7-122">Minimum supported client</span></span><br/> | <span data-ttu-id="fafa7-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="fafa7-123">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="fafa7-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="fafa7-124">Minimum supported server</span></span><br/> | <span data-ttu-id="fafa7-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="fafa7-125">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="fafa7-126">Header</span><span class="sxs-lookup"><span data-stu-id="fafa7-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="fafa7-127"><dt>IADs. h</dt></span><span class="sxs-lookup"><span data-stu-id="fafa7-127"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="fafa7-128">DLL</span><span class="sxs-lookup"><span data-stu-id="fafa7-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fafa7-129"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fafa7-129"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="fafa7-130">IID</span><span class="sxs-lookup"><span data-stu-id="fafa7-130">IID</span></span><br/>                      | <span data-ttu-id="fafa7-131">IID \_ iadsbacklink ist als FD1302BD-4080-11d1-A3AC-00C04FB950DC definiert.</span><span class="sxs-lookup"><span data-stu-id="fafa7-131">IID\_IADsBackLink is defined as FD1302BD-4080-11D1-A3AC-00C04FB950DC</span></span><br/>         |



## <a name="see-also"></a><span data-ttu-id="fafa7-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fafa7-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fafa7-133">**IADsBackLink**</span><span class="sxs-lookup"><span data-stu-id="fafa7-133">**IADsBackLink**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsbacklink)
</dt> <dt>

[<span data-ttu-id="fafa7-134">**anzeigen ( \_ Backlink)**</span><span class="sxs-lookup"><span data-stu-id="fafa7-134">**ADS\_BACKLINK**</span></span>](/windows/win32/api/iads/ns-iads-ads_backlink)
</dt> </dl>

 

 





