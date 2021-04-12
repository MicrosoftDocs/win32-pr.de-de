---
title: Iadsacl-Eigenschafts Methoden (IADs. h)
description: Die-Eigenschaften Methode der iadsacl-Schnittstelle legt die-Eigenschaft fest, die in der folgenden Tabelle beschrieben wird. Weitere Informationen finden Sie unter Interface Property Methods.
ms.assetid: eb4786d7-d366-4924-8255-dc28ea47a246
ms.tgt_platform: multiple
keywords:
- Iadsacl-Eigenschafts Methoden ADSI
topic_type:
- apiref
api_name:
- IADsAcl Property Methods
- IADsAcl.ProtectedAttrName
- IADsAcl.get_ProtecteAttrName
- IADsAcl.put_ProtectedAttrName
- IADsAcl.SubjectName
- IADsAcl.get_SubjectName
- IADsAcl.put_SubjectName
- IADsAcl.Privileges
- IADsAcl.get_Privileges
- IADsAcl.put_Privileges
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b9d8afb1ba3cbf7749ad8e3d14fa970662715909
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478126"
---
# <a name="iadsacl-property-methods"></a><span data-ttu-id="423e8-105">Iadsacl-Eigenschaften Methoden</span><span class="sxs-lookup"><span data-stu-id="423e8-105">IADsAcl Property Methods</span></span>

<span data-ttu-id="423e8-106">Die-Eigenschaften Methode der [**iadsacl**](/windows/desktop/api/Iads/nn-iads-iadsacl) -Schnittstelle legt die-Eigenschaft fest, die in der folgenden Tabelle beschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="423e8-106">The property method of the [**IADsAcl**](/windows/desktop/api/Iads/nn-iads-iadsacl) interface sets the property described in the following table.</span></span> <span data-ttu-id="423e8-107">Weitere Informationen finden Sie unter [Interface Property Methods](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="423e8-107">For more information, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="423e8-108">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="423e8-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="423e8-109">**Berechtigungen**</span><span class="sxs-lookup"><span data-stu-id="423e8-109">**Privileges**</span></span>
<span data-ttu-id="423e8-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="423e8-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="423e8-111">Berechtigungseinstellungen.</span><span class="sxs-lookup"><span data-stu-id="423e8-111">Privilege settings.</span></span>

<dt>

<span data-ttu-id="423e8-112">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="423e8-112">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="423e8-113">Skript Datentyp: **Long**</span><span class="sxs-lookup"><span data-stu-id="423e8-113">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Privileges(
  [out] LONG* retval
);
HRESULT put_Privileges(
  [in] LONG lnPrivileges
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="423e8-114">**Protectedattrname**</span><span class="sxs-lookup"><span data-stu-id="423e8-114">**ProtectedAttrName**</span></span>
<span data-ttu-id="423e8-115"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="423e8-115"></dt> <dd> <dl></span></span>

<span data-ttu-id="423e8-116">Name eines geschützten Attributs.</span><span class="sxs-lookup"><span data-stu-id="423e8-116">Name of a protected attribute.</span></span>

<dt>

<span data-ttu-id="423e8-117">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="423e8-117">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="423e8-118">Skript Datentyp: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="423e8-118">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_ProtecteAttrName(
  [out] BSTR* retVal
);
HRESULT put_ProtectedAttrName(
  [in] BSTR bstrProtectedAttrName
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="423e8-119">**SubjectName**</span><span class="sxs-lookup"><span data-stu-id="423e8-119">**SubjectName**</span></span>
<span data-ttu-id="423e8-120"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="423e8-120"></dt> <dd> <dl></span></span>

<span data-ttu-id="423e8-121">Der Name des Subjekts.</span><span class="sxs-lookup"><span data-stu-id="423e8-121">Name of the subject.</span></span>

<dt>

<span data-ttu-id="423e8-122">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="423e8-122">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="423e8-123">Skript Datentyp: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="423e8-123">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_SubjectName(
  [out] BSTR* retval
);
HRESULT put_SubjectName(
  [in] BSTR bstrSubjectName
);
```


</dt> </dl> </dd> </dl>

 

## <a name="requirements"></a><span data-ttu-id="423e8-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="423e8-124">Requirements</span></span>



| <span data-ttu-id="423e8-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="423e8-125">Requirement</span></span> | <span data-ttu-id="423e8-126">Wert</span><span class="sxs-lookup"><span data-stu-id="423e8-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="423e8-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="423e8-127">Minimum supported client</span></span><br/> | <span data-ttu-id="423e8-128">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="423e8-128">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="423e8-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="423e8-129">Minimum supported server</span></span><br/> | <span data-ttu-id="423e8-130">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="423e8-130">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="423e8-131">Header</span><span class="sxs-lookup"><span data-stu-id="423e8-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="423e8-132"><dt>IADs. h</dt></span><span class="sxs-lookup"><span data-stu-id="423e8-132"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="423e8-133">DLL</span><span class="sxs-lookup"><span data-stu-id="423e8-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="423e8-134"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="423e8-134"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="423e8-135">IID</span><span class="sxs-lookup"><span data-stu-id="423e8-135">IID</span></span><br/>                      | <span data-ttu-id="423e8-136">IID \_ iadsacl ist als 8452d3ab-0869-11d1-a377-00c04b950 DC definiert.</span><span class="sxs-lookup"><span data-stu-id="423e8-136">IID\_IADsAcl is defined as 8452D3AB-0869-11D1-A377-00C04FB950DC</span></span><br/>              |



## <a name="see-also"></a><span data-ttu-id="423e8-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="423e8-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="423e8-138">**IADsAcl**</span><span class="sxs-lookup"><span data-stu-id="423e8-138">**IADsAcl**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsacl)
</dt> </dl>

 

 





