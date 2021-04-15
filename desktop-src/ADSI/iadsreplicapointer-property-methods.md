---
title: Iadsreplicapointer-Eigenschaften Methoden (IADs. h)
description: Die-Eigenschaften Methode der iadsreplicapointer-Schnittstelle legt die-Eigenschaft fest, die in der folgenden Tabelle beschrieben wird. Weitere Informationen finden Sie unter Interface Property Methods.
ms.assetid: fc520ea4-b2c2-44c0-8bec-25f8d4a77074
ms.tgt_platform: multiple
keywords:
- Iadsreplicapointer-Eigenschaften Methoden ADSI
topic_type:
- apiref
api_name:
- IADsReplicaPointer Property Methods
- IADsReplicaPointer.ServerName
- IADsReplicaPointer.get_ServerName
- IADsReplicaPointer.put_ServerName
- IADsReplicaPointer.ReplicaType
- IADsReplicaPointer.get_ReplicaType
- IADsReplicaPointer.put_ReplicaType
- IADsReplicaPointer.ReplicaNumber
- IADsReplicaPointer.get_ReplicaNumber
- IADsReplicaPointer.put_ReplicaNumber
- IADsReplicaPointer.Count
- IADsReplicaPointer.get_Count
- IADsReplicaPointer.put_Count
- IADsReplicaPointer.ReplicaAddressHints
- IADsReplicaPointer.get_ReplicaAddressHints
- IADsReplicaPointer.put_ReplicaAddressHints
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 044d5a5f1b87d42accb7e8e6e6c83eeda69eb5e0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517663"
---
# <a name="iadsreplicapointer-property-methods"></a><span data-ttu-id="9d36e-105">Iadsreplicapointer-Eigenschaften Methoden</span><span class="sxs-lookup"><span data-stu-id="9d36e-105">IADsReplicaPointer Property Methods</span></span>

<span data-ttu-id="9d36e-106">Die-Eigenschaften Methode der [**iadsreplicapointer**](/windows/desktop/api/Iads/nn-iads-iadsreplicapointer) -Schnittstelle legt die-Eigenschaft fest, die in der folgenden Tabelle beschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="9d36e-106">The property method of the [**IADsReplicaPointer**](/windows/desktop/api/Iads/nn-iads-iadsreplicapointer) interface sets the property described in the following table.</span></span> <span data-ttu-id="9d36e-107">Weitere Informationen finden Sie unter [Interface Property Methods](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="9d36e-107">For more information, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="9d36e-108">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="9d36e-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="9d36e-109">**Count**</span><span class="sxs-lookup"><span data-stu-id="9d36e-109">**Count**</span></span>
<span data-ttu-id="9d36e-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="9d36e-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="9d36e-111">Die Anzahl vorhandener Replikate.</span><span class="sxs-lookup"><span data-stu-id="9d36e-111">The number of existing replicas.</span></span>

<dt>

<span data-ttu-id="9d36e-112">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="9d36e-112">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="9d36e-113">Skript Datentyp: **Long**</span><span class="sxs-lookup"><span data-stu-id="9d36e-113">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Count(
  [out] LONG* retval
);
HRESULT put_Count(
  [in] LONG lnCount
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="9d36e-114">**Replicaadresssshints**</span><span class="sxs-lookup"><span data-stu-id="9d36e-114">**ReplicaAddressHints**</span></span>
<span data-ttu-id="9d36e-115"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="9d36e-115"></dt> <dd> <dl></span></span>

<span data-ttu-id="9d36e-116">Eine Netzwerkadresse, die als wahrscheinlichste Verweis auf einen Knoten vorgeschlagen wird, der zum Namen Server führt.</span><span class="sxs-lookup"><span data-stu-id="9d36e-116">A network address suggested as a likely reference to a node leading to the name server.</span></span>

<dt>

<span data-ttu-id="9d36e-117">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="9d36e-117">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="9d36e-118">Skript Datentyp: **Variant**</span><span class="sxs-lookup"><span data-stu-id="9d36e-118">Scripting data type: **VARIANT**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_ReplicaAddressHints(
  [out] VARIANT* retval
);
HRESULT put_ReplicaAddressHints(
  [in] VARIANT vReplicaAddressHints
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="9d36e-119">**Replikannummer**</span><span class="sxs-lookup"><span data-stu-id="9d36e-119">**ReplicaNumber**</span></span>
<span data-ttu-id="9d36e-120"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="9d36e-120"></dt> <dd> <dl></span></span>

<span data-ttu-id="9d36e-121">ID des Replikats.</span><span class="sxs-lookup"><span data-stu-id="9d36e-121">Identification number of the replica.</span></span>

<dt>

<span data-ttu-id="9d36e-122">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="9d36e-122">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="9d36e-123">Skript Datentyp: **Long**</span><span class="sxs-lookup"><span data-stu-id="9d36e-123">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_ReplicaNumber(
  [out] LONG* retval
);
HRESULT put_ReplicaNumber(
  [in] LONG lnReplicaNumber
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="9d36e-124">**Replialisier Type**</span><span class="sxs-lookup"><span data-stu-id="9d36e-124">**ReplicaType**</span></span>
<span data-ttu-id="9d36e-125"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="9d36e-125"></dt> <dd> <dl></span></span>

<span data-ttu-id="9d36e-126">Typ des Replikats (Master, Sekundär oder schreibgeschützt)</span><span class="sxs-lookup"><span data-stu-id="9d36e-126">Type of replica (master, secondary, or read-only.)</span></span>

<dt>

<span data-ttu-id="9d36e-127">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="9d36e-127">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="9d36e-128">Skript Datentyp: **Long**</span><span class="sxs-lookup"><span data-stu-id="9d36e-128">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_ReplicaType(
  [out] LONG* retval
);
HRESULT put_ReplicaType(
  [in] LONG lnType
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="9d36e-129">**ServerName**</span><span class="sxs-lookup"><span data-stu-id="9d36e-129">**ServerName**</span></span>
<span data-ttu-id="9d36e-130"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="9d36e-130"></dt> <dd> <dl></span></span>

<span data-ttu-id="9d36e-131">Name des Namen Servers, der das Replikat enthält.</span><span class="sxs-lookup"><span data-stu-id="9d36e-131">Name of the name server holding the replica.</span></span>

<dt>

<span data-ttu-id="9d36e-132">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="9d36e-132">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="9d36e-133">Skript Datentyp: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="9d36e-133">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_ServerName(
  [out] BSTR* retVal
);
HRESULT put_ServerName(
  [in] BSTR bstrServerName
);
```


</dt> </dl> </dd> </dl>

 

## <a name="requirements"></a><span data-ttu-id="9d36e-134">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9d36e-134">Requirements</span></span>



| <span data-ttu-id="9d36e-135">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9d36e-135">Requirement</span></span> | <span data-ttu-id="9d36e-136">Wert</span><span class="sxs-lookup"><span data-stu-id="9d36e-136">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9d36e-137">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9d36e-137">Minimum supported client</span></span><br/> | <span data-ttu-id="9d36e-138">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9d36e-138">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="9d36e-139">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9d36e-139">Minimum supported server</span></span><br/> | <span data-ttu-id="9d36e-140">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9d36e-140">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="9d36e-141">Header</span><span class="sxs-lookup"><span data-stu-id="9d36e-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="9d36e-142"><dt>IADs. h</dt></span><span class="sxs-lookup"><span data-stu-id="9d36e-142"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="9d36e-143">DLL</span><span class="sxs-lookup"><span data-stu-id="9d36e-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9d36e-144"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9d36e-144"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="9d36e-145">IID</span><span class="sxs-lookup"><span data-stu-id="9d36e-145">IID</span></span><br/>                      | <span data-ttu-id="9d36e-146">IID \_ iadsreplicapointer ist als F60FB803-4080-11d1-A3AC-00C04FB950DC definiert.</span><span class="sxs-lookup"><span data-stu-id="9d36e-146">IID\_IADsReplicaPointer is defined as F60FB803-4080-11D1-A3AC-00C04FB950DC</span></span><br/>   |



## <a name="see-also"></a><span data-ttu-id="9d36e-147">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9d36e-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9d36e-148">**IADsReplicaPointer**</span><span class="sxs-lookup"><span data-stu-id="9d36e-148">**IADsReplicaPointer**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsreplicapointer)
</dt> <dt>

[<span data-ttu-id="9d36e-149">**ADS \_ replicapointer**</span><span class="sxs-lookup"><span data-stu-id="9d36e-149">**ADS\_REPLICAPOINTER**</span></span>](/windows/win32/api/iads/ns-iads-ads_replicapointer)
</dt> </dl>

 

 





