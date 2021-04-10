---
title: Einfache ADSI-Datentypen (IADs. h)
description: Mit Active Directory Service Interfaces (ADSI) werden die folgenden einfachen Datentypen definiert und verwendet.
ms.assetid: 0bd34f13-269f-4f5d-8a18-74577522e402
ms.tgt_platform: multiple
keywords:
- ADS_BOOLEAN
- ADS_CASE_EXACT_STRING
- ADS_CASE_IGNORE_STRING
- ADS_DN_STRING
- ADS_INTEGER
- ADS_LARGE_INTEGER
- ADS_NUMERIC_STRING
- ADS_OBJECT_CLASS
- ADS_PRINTABLE_STRING
- ADS_SEARCH_HANDLE
- ADS_UTC_TIME
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5530fda2ca1f4fe967eaf376b668a0bedc29c4b6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040246"
---
# <a name="adsi-simple-data-types"></a><span data-ttu-id="71ae3-114">Einfache ADSI-Datentypen</span><span class="sxs-lookup"><span data-stu-id="71ae3-114">ADSI Simple Data Types</span></span>

<span data-ttu-id="71ae3-115">Mit Active Directory Service Interfaces (ADSI) werden die folgenden einfachen Datentypen definiert und verwendet.</span><span class="sxs-lookup"><span data-stu-id="71ae3-115">Active Directory Service Interfaces (ADSI) defines and uses the following simple data types.</span></span>


```C++
typedef DWORD ADS_BOOLEAN, *PADS_BOOLEAN;
typedef LPWSTR ADS_CASE_EXACT_STRING, *PADS_CASE_EXACT_STRING;
typedef LPWSTR ADS_CASE_IGNORE_STRING, *PADS_CASE_IGNORE_STRING;
typedef LPWSTR ADS_DN_STRING, *PADS_DN_STRING;
typedef DWORD ADS_INTEGER, *PADS_INTEGER;
typedef LARGE_INTEGER ADS_LARGE_INTEGER, *PADS_LARGE_INTEGER;
typedef LPWSTR ADS_NUMERIC_STRING, *PADS_NUMERIC_STRING;
typedef LPWSTR ADS_OBJECT_CLASS, *PADS_OBJECT_CLASS;
typedef LPWSTR ADS_PRINTABLE_STRING, *PADS_PRINTABLE_STRING;
typedef HANDLE ADS_SEARCH_HANDLE, *PADS_SEARCH_HANDLE;
typedef SYSTEMTIME ADS_UTC_TIME, *PADS_UTC_TIME;
```



<dl> <dt>

<span data-ttu-id="71ae3-116">**ADS \_ boolescher Wert**</span><span class="sxs-lookup"><span data-stu-id="71ae3-116">**ADS\_BOOLEAN**</span></span>
</dt> <dd>

<span data-ttu-id="71ae3-117">DWORD</span><span class="sxs-lookup"><span data-stu-id="71ae3-117">DWORD</span></span>

</dd> <dt>

<span data-ttu-id="71ae3-118">**\_ \_ akdie exakte \_ Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="71ae3-118">**ADS\_CASE\_EXACT\_STRING**</span></span>
</dt> <dd>

<span data-ttu-id="71ae3-119">LPWSTR</span><span class="sxs-lookup"><span data-stu-id="71ae3-119">LPWSTR</span></span>

</dd> <dt>

<span data-ttu-id="71ae3-120">**ADS \_ - \_ \_ Zeichenfolge ignorieren**</span><span class="sxs-lookup"><span data-stu-id="71ae3-120">**ADS\_CASE\_IGNORE\_STRING**</span></span>
</dt> <dd>

<span data-ttu-id="71ae3-121">LPWSTR</span><span class="sxs-lookup"><span data-stu-id="71ae3-121">LPWSTR</span></span>

</dd> <dt>

<span data-ttu-id="71ae3-122">**ADS \_ DN- \_ Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="71ae3-122">**ADS\_DN\_STRING**</span></span>
</dt> <dd>

<span data-ttu-id="71ae3-123">LPWSTR</span><span class="sxs-lookup"><span data-stu-id="71ae3-123">LPWSTR</span></span>

</dd> <dt>

<span data-ttu-id="71ae3-124">**ADS- \_ Ganzzahl**</span><span class="sxs-lookup"><span data-stu-id="71ae3-124">**ADS\_INTEGER**</span></span>
</dt> <dd>

<span data-ttu-id="71ae3-125">DWORD</span><span class="sxs-lookup"><span data-stu-id="71ae3-125">DWORD</span></span>

</dd> <dt>

<span data-ttu-id="71ae3-126">**Werbung für \_ große \_ ganze Zahlen**</span><span class="sxs-lookup"><span data-stu-id="71ae3-126">**ADS\_LARGE\_INTEGER**</span></span>
</dt> <dd>

[<span data-ttu-id="71ae3-127">**große \_ ganze Zahl**</span><span class="sxs-lookup"><span data-stu-id="71ae3-127">**LARGE\_INTEGER**</span></span>](/windows/win32/api/winnt/ns-winnt-large_integer-r1)

</dd> <dt>

<span data-ttu-id="71ae3-128">**\_numerische \_ Zeichenfolge ADS**</span><span class="sxs-lookup"><span data-stu-id="71ae3-128">**ADS\_NUMERIC\_STRING**</span></span>
</dt> <dd>

<span data-ttu-id="71ae3-129">LPWSTR</span><span class="sxs-lookup"><span data-stu-id="71ae3-129">LPWSTR</span></span>

</dd> <dt>

<span data-ttu-id="71ae3-130">**ADS- \_ Objekt \_ Klasse**</span><span class="sxs-lookup"><span data-stu-id="71ae3-130">**ADS\_OBJECT\_CLASS**</span></span>
</dt> <dd>

<span data-ttu-id="71ae3-131">LPWSTR</span><span class="sxs-lookup"><span data-stu-id="71ae3-131">LPWSTR</span></span>

</dd> <dt>

<span data-ttu-id="71ae3-132">**\_Druck druckbare \_ Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="71ae3-132">**ADS\_PRINTABLE\_STRING**</span></span>
</dt> <dd>

<span data-ttu-id="71ae3-133">LPWSTR</span><span class="sxs-lookup"><span data-stu-id="71ae3-133">LPWSTR</span></span>

</dd> <dt>

<span data-ttu-id="71ae3-134">**ADS- \_ Such \_ handle**</span><span class="sxs-lookup"><span data-stu-id="71ae3-134">**ADS\_SEARCH\_HANDLE**</span></span>
</dt> <dd>

<span data-ttu-id="71ae3-135">HANDLE</span><span class="sxs-lookup"><span data-stu-id="71ae3-135">HANDLE</span></span>

</dd> <dt>

<span data-ttu-id="71ae3-136">**Anzeigen der \_ UTC- \_ Zeit**</span><span class="sxs-lookup"><span data-stu-id="71ae3-136">**ADS\_UTC\_TIME**</span></span>
</dt> <dd>

[<span data-ttu-id="71ae3-137">**System Time**</span><span class="sxs-lookup"><span data-stu-id="71ae3-137">**SYSTEMTIME**</span></span>](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime)

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="71ae3-138">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="71ae3-138">Remarks</span></span>

<span data-ttu-id="71ae3-139">Wenn ADSI ein Attribut liest, das im LDAP-Schema als **Integer** definiert wurde, wird die ganze Zahl immer als 32-Bit-Wert behandelt, und die Daten können abgeschnitten werden.</span><span class="sxs-lookup"><span data-stu-id="71ae3-139">When ADSI reads an attribute that has been defined as an **INTEGER** in the LDAP schema, it will always handle the integer as a 32-bit value and may truncate the data.</span></span> <span data-ttu-id="71ae3-140">Dies ist nur bei LDAP-Servern von Bedeutung, die ganzzahlige Werte beliebig groß sind.</span><span class="sxs-lookup"><span data-stu-id="71ae3-140">This is only a concern for LDAP servers that allow arbitrary sized integer values.</span></span> <span data-ttu-id="71ae3-141">Wenn das Attribut ein durch die Erweiterung des Schemas definiertes benutzerdefiniertes Attribut ist, kann dieses Problem vermieden werden, indem das benutzerdefinierte Attribut als Zeichenfolge definiert wird.</span><span class="sxs-lookup"><span data-stu-id="71ae3-141">If the attribute is a custom attribute defined by extending the schema, this problem can be avoided by defining the custom attribute as a string.</span></span>

## <a name="requirements"></a><span data-ttu-id="71ae3-142">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="71ae3-142">Requirements</span></span>



| <span data-ttu-id="71ae3-143">Anforderung</span><span class="sxs-lookup"><span data-stu-id="71ae3-143">Requirement</span></span> | <span data-ttu-id="71ae3-144">Wert</span><span class="sxs-lookup"><span data-stu-id="71ae3-144">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="71ae3-145">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="71ae3-145">Minimum supported client</span></span><br/> | <span data-ttu-id="71ae3-146">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="71ae3-146">Windows Vista</span></span><br/>                                                          |
| <span data-ttu-id="71ae3-147">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="71ae3-147">Minimum supported server</span></span><br/> | <span data-ttu-id="71ae3-148">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="71ae3-148">Windows Server 2008</span></span><br/>                                                    |
| <span data-ttu-id="71ae3-149">Header</span><span class="sxs-lookup"><span data-stu-id="71ae3-149">Header</span></span><br/>                   | <dl> <span data-ttu-id="71ae3-150"><dt>IADs. h</dt></span><span class="sxs-lookup"><span data-stu-id="71ae3-150"><dt>Iads.h</dt></span></span> </dl> |



 

