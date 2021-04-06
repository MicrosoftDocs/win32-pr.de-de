---
title: Iadsnetaddress-Eigenschaften Methoden (IADs. h)
description: Die-Eigenschaften Methode der iadsnetaddress-Schnittstelle legt die-Eigenschaft fest, die in der folgenden Tabelle beschrieben wird. Weitere Informationen finden Sie unter Interface Property Methods.
ms.assetid: 1da493d6-5660-4054-8d28-89db0b56f30f
ms.tgt_platform: multiple
keywords:
- Iadsnetaddress-Eigenschaften Methoden ADSI
topic_type:
- apiref
api_name:
- IADsNetAddress Property Methods
- IADsNetAddress.AddressType
- IADsNetAddress.get_AddressType
- IADsNetAddress.put_AddressType
- IADsNetAddress.Address
- IADsNetAddress.get_Address
- IADsNetAddress.put_Address
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 073033c703db8eaa55b05058d6d2bbc3d3167f4b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742689"
---
# <a name="iadsnetaddress-property-methods"></a><span data-ttu-id="ece19-105">Iadsnetaddress-Eigenschaften Methoden</span><span class="sxs-lookup"><span data-stu-id="ece19-105">IADsNetAddress Property Methods</span></span>

<span data-ttu-id="ece19-106">Die-Eigenschaften Methode der [**iadsnetaddress**](/windows/desktop/api/Iads/nn-iads-iadsnetaddress) -Schnittstelle legt die-Eigenschaft fest, die in der folgenden Tabelle beschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="ece19-106">The property method of the [**IADsNetAddress**](/windows/desktop/api/Iads/nn-iads-iadsnetaddress) interface sets the property described in the following table.</span></span> <span data-ttu-id="ece19-107">Weitere Informationen finden Sie unter [Interface Property Methods](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="ece19-107">For more information, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="ece19-108">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="ece19-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="ece19-109">**Adresse**</span><span class="sxs-lookup"><span data-stu-id="ece19-109">**Address**</span></span>
<span data-ttu-id="ece19-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="ece19-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="ece19-111">Eine Netzwerkadresse.</span><span class="sxs-lookup"><span data-stu-id="ece19-111">A network address.</span></span>

<dt>

<span data-ttu-id="ece19-112">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="ece19-112">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="ece19-113">Skript Datentyp: **Variant**</span><span class="sxs-lookup"><span data-stu-id="ece19-113">Scripting data type: **VARIANT**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Address(
  [out] VARIANT* retval
);
HRESULT put_Address(
  [in] VARIANT vAddress
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="ece19-114">**Adresstyp**</span><span class="sxs-lookup"><span data-stu-id="ece19-114">**AddressType**</span></span>
<span data-ttu-id="ece19-115"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="ece19-115"></dt> <dd> <dl></span></span>

<span data-ttu-id="ece19-116">Ein Typ von Kommunikationsprotokollen.</span><span class="sxs-lookup"><span data-stu-id="ece19-116">A type of communication protocols.</span></span>

<dt>

<span data-ttu-id="ece19-117">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="ece19-117">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="ece19-118">Skript Datentyp: **Long**</span><span class="sxs-lookup"><span data-stu-id="ece19-118">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_AddressType(
  [out] LONG* retVal
);
HRESULT put_AddressType(
  [in] LONG lnAddressType
);
```


</dt> </dl> </dd> </dl>

 

## <a name="requirements"></a><span data-ttu-id="ece19-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ece19-119">Requirements</span></span>



| <span data-ttu-id="ece19-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ece19-120">Requirement</span></span> | <span data-ttu-id="ece19-121">Wert</span><span class="sxs-lookup"><span data-stu-id="ece19-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ece19-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ece19-122">Minimum supported client</span></span><br/> | <span data-ttu-id="ece19-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ece19-123">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="ece19-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ece19-124">Minimum supported server</span></span><br/> | <span data-ttu-id="ece19-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ece19-125">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="ece19-126">Header</span><span class="sxs-lookup"><span data-stu-id="ece19-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="ece19-127"><dt>IADs. h</dt></span><span class="sxs-lookup"><span data-stu-id="ece19-127"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="ece19-128">DLL</span><span class="sxs-lookup"><span data-stu-id="ece19-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ece19-129"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ece19-129"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="ece19-130">IID</span><span class="sxs-lookup"><span data-stu-id="ece19-130">IID</span></span><br/>                      | <span data-ttu-id="ece19-131">IID \_ iadsnetaddress ist als B21A50A9-4080-11d1-A3AC-00C04FB950DC definiert.</span><span class="sxs-lookup"><span data-stu-id="ece19-131">IID\_IADsNetAddress is defined as B21A50A9-4080-11D1-A3AC-00C04FB950DC</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="ece19-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ece19-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ece19-133">**IADsNetAddress**</span><span class="sxs-lookup"><span data-stu-id="ece19-133">**IADsNetAddress**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsnetaddress)
</dt> <dt>

[<span data-ttu-id="ece19-134">**ADS- \_ netaddress**</span><span class="sxs-lookup"><span data-stu-id="ece19-134">**ADS\_NETADDRESS**</span></span>](/windows/win32/api/iads/ns-iads-ads_netaddress)
</dt> </dl>

 

 





