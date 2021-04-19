---
title: Iadsou-Eigenschaften Methoden (IADs. h)
description: Mit den Eigenschafts Methoden der iadsou-Schnittstelle werden die in der folgenden Tabelle aufgeführten Eigenschaften angezeigt oder festgelegt. Weitere Informationen finden Sie unter Interface Property Methods.
ms.assetid: 8cb84972-733b-47ca-8647-1b7a85c97021
ms.tgt_platform: multiple
keywords:
- Iadsou-Eigenschaften Methoden ADSI
topic_type:
- apiref
api_name:
- IADsOU Property Methods
- IADsOU.BusinessCategory
- IADsOU.get_BusinessCategory
- IADsOU.put_BusinessCategory
- IADsOU.Description
- IADsOU.get_Description
- IADsOU.put_Description
- IADsOU.FaxNumber
- IADsOU.get_FaxNumber
- IADsOU.put_FaxNumber
- IADsOU.LocalityName
- IADsOU.get_LocalityName
- IADsOU.put_LocalityName
- IADsOU.PostalAddress
- IADsOU.get_PostalAddress
- IADsOU.put_PostalAddress
- IADsOU.TelephoneNumber
- IADsOU.get_TelephoneNumber
- IADsOU.put_TelephoneNumber
- IADsOU.SeeAlso
- IADsOU.get_SeeAlso
- IADsOU.put_SeeAlso
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a0ce30fad6a690a26a8e16b817b77b129dee25f1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106342854"
---
# <a name="iadsou-property-methods"></a><span data-ttu-id="6727b-105">Iadsou-Eigenschaften Methoden</span><span class="sxs-lookup"><span data-stu-id="6727b-105">IADsOU Property Methods</span></span>

<span data-ttu-id="6727b-106">Mit den Eigenschafts Methoden der [**iadsou**](/windows/desktop/api/Iads/nn-iads-iadsou) -Schnittstelle werden die in der folgenden Tabelle aufgeführten Eigenschaften angezeigt oder festgelegt.</span><span class="sxs-lookup"><span data-stu-id="6727b-106">The property methods of the [**IADsOU**](/windows/desktop/api/Iads/nn-iads-iadsou) interface get or set the properties listed in the following table.</span></span> <span data-ttu-id="6727b-107">Weitere Informationen finden Sie unter [Interface Property Methods](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="6727b-107">For more information, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="6727b-108">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="6727b-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="6727b-109">**Businesscategory**</span><span class="sxs-lookup"><span data-stu-id="6727b-109">**BusinessCategory**</span></span>
<span data-ttu-id="6727b-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="6727b-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="6727b-111">Eine Zeichenfolge, die die allgemeine Geschäftsfunktion oder die von der Organisationseinheit ausgeführten Funktionen enthält, z. b. "Accounting".</span><span class="sxs-lookup"><span data-stu-id="6727b-111">A string that contains the general business function or functions performed by the organizational unit, for example "Accounting".</span></span>

<dt>

<span data-ttu-id="6727b-112">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="6727b-112">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="6727b-113">Skript Datentyp: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="6727b-113">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_BusinessCategory(
  [out] BSTR* pbstrBusinessCategory
);
HRESULT put_BusinessCategory(
  [in] BSTR bstrBusinessCategory
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="6727b-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="6727b-114">**Description**</span></span>
<span data-ttu-id="6727b-115"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="6727b-115"></dt> <dd> <dl></span></span>

<span data-ttu-id="6727b-116">Eine Zeichenfolge, die eine Textbeschreibung der Organisationseinheit enthält.</span><span class="sxs-lookup"><span data-stu-id="6727b-116">A string that contains a textual description of the organizational unit.</span></span>

<dt>

<span data-ttu-id="6727b-117">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="6727b-117">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="6727b-118">Skript Datentyp: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="6727b-118">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Description(
  [out] BSTR* pbstrDescription
);
HRESULT put_Description(
  [in] BSTR bstrDescription
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="6727b-119">**Faxnummer**</span><span class="sxs-lookup"><span data-stu-id="6727b-119">**FaxNumber**</span></span>
<span data-ttu-id="6727b-120"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="6727b-120"></dt> <dd> <dl></span></span>

<span data-ttu-id="6727b-121">Eine Zeichenfolge, die die Faxnummer der Organisationseinheit enthält.</span><span class="sxs-lookup"><span data-stu-id="6727b-121">A string that contains the facsimile number of the organizational unit.</span></span>

<dt>

<span data-ttu-id="6727b-122">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="6727b-122">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="6727b-123">Skript Datentyp: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="6727b-123">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_FaxNumber(
  [out] BSTR* pbstrFaxNumber
);
HRESULT put_FaxNumber(
  [in] BSTR bstrFaxNumber
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="6727b-124">**Localityname**</span><span class="sxs-lookup"><span data-stu-id="6727b-124">**LocalityName**</span></span>
<span data-ttu-id="6727b-125"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="6727b-125"></dt> <dd> <dl></span></span>

<span data-ttu-id="6727b-126">Eine Zeichenfolge, die den Namen des geografischen Bereichs der Organisationseinheit enthält.</span><span class="sxs-lookup"><span data-stu-id="6727b-126">A string that contains the name of the geographic region of the organizational unit.</span></span>

<dt>

<span data-ttu-id="6727b-127">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="6727b-127">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="6727b-128">Skript Datentyp: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="6727b-128">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_LocalityName(
  [out] BSTR* pbstrLocalityName
);
HRESULT put_LocalityName(
  [in] BSTR bstrLocalityName
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="6727b-129">**PostalAddress**</span><span class="sxs-lookup"><span data-stu-id="6727b-129">**PostalAddress**</span></span>
<span data-ttu-id="6727b-130"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="6727b-130"></dt> <dd> <dl></span></span>

<span data-ttu-id="6727b-131">Eine Zeichenfolge, die die Postanschrift der Organisationseinheit enthält.</span><span class="sxs-lookup"><span data-stu-id="6727b-131">A string that contains the postal address of the organizational unit.</span></span>

<dt>

<span data-ttu-id="6727b-132">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="6727b-132">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="6727b-133">Skript Datentyp: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="6727b-133">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_PostalAddress(
  [out] BSTR* pbstrPostalAddress
);
HRESULT put_PostalAddress(
  [in] BSTR bstrPostalAddress
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="6727b-134">**SeeAlso**</span><span class="sxs-lookup"><span data-stu-id="6727b-134">**SeeAlso**</span></span>
<span data-ttu-id="6727b-135"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="6727b-135"></dt> <dd> <dl></span></span>

<span data-ttu-id="6727b-136">Ein Array von Zeichen folgen, das die Distinguished Names von anderen Verzeichnis Objekten enthält, die für dieses Objekt relevant sein können.</span><span class="sxs-lookup"><span data-stu-id="6727b-136">An array of strings that contains the distinguished names of other directory objects which may be relevant to this object.</span></span>

<dt>

<span data-ttu-id="6727b-137">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="6727b-137">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="6727b-138">Skript Datentyp: **Variant**</span><span class="sxs-lookup"><span data-stu-id="6727b-138">Scripting data type: **VARIANT**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_SeeAlso(
  [out] VARIANT* pvSeeAlso
);
HRESULT put_SeeAlso(
  [in] VARIANT vSeeAlso
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="6727b-139">**TelephoneNumber**</span><span class="sxs-lookup"><span data-stu-id="6727b-139">**TelephoneNumber**</span></span>
<span data-ttu-id="6727b-140"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="6727b-140"></dt> <dd> <dl></span></span>

<span data-ttu-id="6727b-141">Eine Zeichenfolge, die die Telefonnummer der Organisationseinheit enthält.</span><span class="sxs-lookup"><span data-stu-id="6727b-141">A string that contains the telephone number of the organizational unit.</span></span>

<dt>

<span data-ttu-id="6727b-142">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="6727b-142">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="6727b-143">Skript Datentyp: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="6727b-143">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_TelephoneNumber(
  [out] BSTR* pbstrTelephoneNumber
);
HRESULT put_TelephoneNumber(
  [in] BSTR bstrTelephoneNumber
);
```


</dt> </dl> </dd> </dl>

 

## <a name="examples"></a><span data-ttu-id="6727b-144">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6727b-144">Examples</span></span>

<span data-ttu-id="6727b-145">Im folgenden Codebeispiel werden die **businesscategory** und die **Beschreibung** aller Organisationseinheiten in einem Container angezeigt.</span><span class="sxs-lookup"><span data-stu-id="6727b-145">The following code example displays the **BusinessCategory** and **Description** of all organization units in a container.</span></span> <span data-ttu-id="6727b-146">Dabei wird davon ausgegangen, dass der zugrunde liegende Verzeichnisdienst das Gruppieren von Verzeichnis Objekten nach Organisationseinheit unterstützt.</span><span class="sxs-lookup"><span data-stu-id="6727b-146">It assumes that the underlying directory service supports grouping of directory objects by organization unit.</span></span>


```VB
Dim dom As IADsContainer
Dim ou As IADsOU

' Bind to the container.
Set dom = GetObject("LDAP://server1/domain1")

' Filter out all objects that are not of class "organizationalUnit".
dom.filter = Array("organizationalUnit")

' Enumerate the organizational units in the container and display  
' the BusinessCategory and Description properties of each OU.
For Each ou In dom
    MsgBox ou.BusinessCategory & ": " & ou.Description
Next
```



## <a name="requirements"></a><span data-ttu-id="6727b-147">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6727b-147">Requirements</span></span>



| <span data-ttu-id="6727b-148">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6727b-148">Requirement</span></span> | <span data-ttu-id="6727b-149">Wert</span><span class="sxs-lookup"><span data-stu-id="6727b-149">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6727b-150">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6727b-150">Minimum supported client</span></span><br/> | <span data-ttu-id="6727b-151">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6727b-151">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="6727b-152">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6727b-152">Minimum supported server</span></span><br/> | <span data-ttu-id="6727b-153">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6727b-153">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="6727b-154">Header</span><span class="sxs-lookup"><span data-stu-id="6727b-154">Header</span></span><br/>                   | <dl> <span data-ttu-id="6727b-155"><dt>IADs. h</dt></span><span class="sxs-lookup"><span data-stu-id="6727b-155"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="6727b-156">DLL</span><span class="sxs-lookup"><span data-stu-id="6727b-156">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6727b-157"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6727b-157"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="6727b-158">IID</span><span class="sxs-lookup"><span data-stu-id="6727b-158">IID</span></span><br/>                      | <span data-ttu-id="6727b-159">IID \_ iadsou ist als A2F733B8-Effe-11CF-8ABC-00C04FD8D503 definiert.</span><span class="sxs-lookup"><span data-stu-id="6727b-159">IID\_IADsOU is defined as A2F733B8-EFFE-11CF-8ABC-00C04FD8D503</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="6727b-160">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6727b-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6727b-161">**Iadsou**</span><span class="sxs-lookup"><span data-stu-id="6727b-161">**IADsOU**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsou)
</dt> <dt>

[<span data-ttu-id="6727b-162">Schnittstelleneigenschaften Methoden</span><span class="sxs-lookup"><span data-stu-id="6727b-162">Interface Property Methods</span></span>](interface-property-methods.md)
</dt> </dl>

 

 





