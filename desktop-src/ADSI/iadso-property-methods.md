---
title: Iadso-Eigenschaften Methoden (IADs. h)
description: Mit den Eigenschafts Methoden der iadso-Schnittstelle werden die in der folgenden Tabelle beschriebenen Eigenschaften angezeigt oder festgelegt. Weitere Informationen finden Sie unter Interface Property Methods.
ms.assetid: d4bc1d29-98de-462d-b59c-2bc2641c25a0
ms.tgt_platform: multiple
keywords:
- Iadso-Eigenschaften Methoden ADSI
topic_type:
- apiref
api_name:
- IADsO Property Methods
- IADsO.Description
- IADsO.get_Description
- IADsO.put_Description
- IADsO.FaxNumber
- IADsO.get_FaxNumber
- IADsO.put_FaxNumber
- IADsO.LocalityName
- IADsO.get_LocalityName
- IADsO.put_LocalityName
- IADsO.PostalAddress
- IADsO.get_PostalAddress
- IADsO.put_PostalAddress
- IADsO.TelephoneNumber
- IADsO.get_TelephoneNumber
- IADsO.put_TelephoneNumber
- IADsO.SeeAlso
- IADsO.get_SeeAlso
- IADsO.put_SeeAlso
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 09840cf62d6883eb4f5ca326998b697a34698c90
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742688"
---
# <a name="iadso-property-methods"></a><span data-ttu-id="d8a46-105">Iadso-Eigenschaften Methoden</span><span class="sxs-lookup"><span data-stu-id="d8a46-105">IADsO Property Methods</span></span>

<span data-ttu-id="d8a46-106">Mit den Eigenschafts Methoden der [**iadso**](/windows/desktop/api/Iads/nn-iads-iadso) -Schnittstelle werden die in der folgenden Tabelle beschriebenen Eigenschaften angezeigt oder festgelegt.</span><span class="sxs-lookup"><span data-stu-id="d8a46-106">The property methods of the [**IADsO**](/windows/desktop/api/Iads/nn-iads-iadso) interface get or set the properties described in the following table.</span></span> <span data-ttu-id="d8a46-107">Weitere Informationen finden Sie unter [Interface Property Methods](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="d8a46-107">For more information, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="d8a46-108">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="d8a46-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="d8a46-109">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d8a46-109">**Description**</span></span>
<span data-ttu-id="d8a46-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="d8a46-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="d8a46-111">Die Beschreibung der Organisation.</span><span class="sxs-lookup"><span data-stu-id="d8a46-111">The description of the organization.</span></span>

<dt>

<span data-ttu-id="d8a46-112">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="d8a46-112">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="d8a46-113">Skript Datentyp: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="d8a46-113">Scripting data type: **BSTR**</span></span>
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

<span data-ttu-id="d8a46-114">**Faxnummer**</span><span class="sxs-lookup"><span data-stu-id="d8a46-114">**FaxNumber**</span></span>
<span data-ttu-id="d8a46-115"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="d8a46-115"></dt> <dd> <dl></span></span>

<span data-ttu-id="d8a46-116">Die Faxnummer (Fax) der Organisation.</span><span class="sxs-lookup"><span data-stu-id="d8a46-116">The facsimile (fax) number of the organization.</span></span>

<dt>

<span data-ttu-id="d8a46-117">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="d8a46-117">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="d8a46-118">Skript Datentyp: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="d8a46-118">Scripting data type: **BSTR**</span></span>
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

<span data-ttu-id="d8a46-119">**Localityname**</span><span class="sxs-lookup"><span data-stu-id="d8a46-119">**LocalityName**</span></span>
<span data-ttu-id="d8a46-120"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="d8a46-120"></dt> <dd> <dl></span></span>

<span data-ttu-id="d8a46-121">Der Name des Orts, an dem sich die Organisation befindet.</span><span class="sxs-lookup"><span data-stu-id="d8a46-121">The name of the place in which the organization is located.</span></span>

<dt>

<span data-ttu-id="d8a46-122">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="d8a46-122">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="d8a46-123">Skript Datentyp: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="d8a46-123">Scripting data type: **BSTR**</span></span>
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

<span data-ttu-id="d8a46-124">**PostalAddress**</span><span class="sxs-lookup"><span data-stu-id="d8a46-124">**PostalAddress**</span></span>
<span data-ttu-id="d8a46-125"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="d8a46-125"></dt> <dd> <dl></span></span>

<span data-ttu-id="d8a46-126">Die Postanschrift der Organisation.</span><span class="sxs-lookup"><span data-stu-id="d8a46-126">The postal address of the organization.</span></span>

<dt>

<span data-ttu-id="d8a46-127">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="d8a46-127">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="d8a46-128">Skript Datentyp: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="d8a46-128">Scripting data type: **BSTR**</span></span>
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

<span data-ttu-id="d8a46-129">**SeeAlso**</span><span class="sxs-lookup"><span data-stu-id="d8a46-129">**SeeAlso**</span></span>
<span data-ttu-id="d8a46-130"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="d8a46-130"></dt> <dd> <dl></span></span>

<span data-ttu-id="d8a46-131">Ein Array von ADsPath-Namen anderer ADSI-Objekte, die für dieses Objekt relevant sein können.</span><span class="sxs-lookup"><span data-stu-id="d8a46-131">An array of ADsPath names of other ADSI objects which may be relevant to this object.</span></span>

<dt>

<span data-ttu-id="d8a46-132">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="d8a46-132">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="d8a46-133">Skript Datentyp: **Variant**</span><span class="sxs-lookup"><span data-stu-id="d8a46-133">Scripting data type: **VARIANT**</span></span>
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

<span data-ttu-id="d8a46-134">**TelephoneNumber**</span><span class="sxs-lookup"><span data-stu-id="d8a46-134">**TelephoneNumber**</span></span>
<span data-ttu-id="d8a46-135"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="d8a46-135"></dt> <dd> <dl></span></span>

<span data-ttu-id="d8a46-136">Die Telefonnummer der Organisation.</span><span class="sxs-lookup"><span data-stu-id="d8a46-136">The telephone number of the organization.</span></span>

<dt>

<span data-ttu-id="d8a46-137">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="d8a46-137">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="d8a46-138">Skript Datentyp: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="d8a46-138">Scripting data type: **BSTR**</span></span>
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

 

## <a name="examples"></a><span data-ttu-id="d8a46-139">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d8a46-139">Examples</span></span>

<span data-ttu-id="d8a46-140">Im folgenden Codebeispiel wird die Beschreibung einer bestimmten Organisation angezeigt.</span><span class="sxs-lookup"><span data-stu-id="d8a46-140">The following code example displays the description of a given organization.</span></span> <span data-ttu-id="d8a46-141">Dabei wird davon ausgegangen, dass der zugrunde liegende Verzeichnisdienst das Gruppieren von Verzeichnis Objekten nach Organisation unter</span><span class="sxs-lookup"><span data-stu-id="d8a46-141">It assumes the underlying directory service supports grouping directory objects by organization.</span></span>


```VB
Dim dom As IADsContainer
Dim dso As IADsOpenDSObject
Dim szUsername As String
Dim szPassword As String
On Error GoTo Cleanup

' Insert code to securely retrieve the user name and password
 
Set dso = GetObject("LDAP:")
Set dom = dso.OpenDSObject("LDAP://adsrv1/dc=Fabrikam, dc=Com", _
                           szUsername, szPassword,1)
dom.Filter = Array("organization")
For Each o In dom
    MsgBox "Fax number of " & o.Name & " : " & o.Description
Next

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If

    Set dom = Nothing
    Set dso = Nothing
```



## <a name="requirements"></a><span data-ttu-id="d8a46-142">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d8a46-142">Requirements</span></span>



| <span data-ttu-id="d8a46-143">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d8a46-143">Requirement</span></span> | <span data-ttu-id="d8a46-144">Wert</span><span class="sxs-lookup"><span data-stu-id="d8a46-144">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d8a46-145">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d8a46-145">Minimum supported client</span></span><br/> | <span data-ttu-id="d8a46-146">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d8a46-146">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="d8a46-147">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d8a46-147">Minimum supported server</span></span><br/> | <span data-ttu-id="d8a46-148">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d8a46-148">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="d8a46-149">Header</span><span class="sxs-lookup"><span data-stu-id="d8a46-149">Header</span></span><br/>                   | <dl> <span data-ttu-id="d8a46-150"><dt>IADs. h</dt></span><span class="sxs-lookup"><span data-stu-id="d8a46-150"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="d8a46-151">DLL</span><span class="sxs-lookup"><span data-stu-id="d8a46-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d8a46-152"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d8a46-152"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="d8a46-153">IID</span><span class="sxs-lookup"><span data-stu-id="d8a46-153">IID</span></span><br/>                      | <span data-ttu-id="d8a46-154">IID \_ iadso ist als A1CD2DC6-Effe-11CF-8ABC-00C04FD8D503 definiert.</span><span class="sxs-lookup"><span data-stu-id="d8a46-154">IID\_IADsO is defined as A1CD2DC6-EFFE-11CF-8ABC-00C04FD8D503</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="d8a46-155">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d8a46-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d8a46-156">**Iadso**</span><span class="sxs-lookup"><span data-stu-id="d8a46-156">**IADsO**</span></span>](/windows/desktop/api/Iads/nn-iads-iadso)
</dt> <dt>

[<span data-ttu-id="d8a46-157">Schnittstelleneigenschaften Methoden</span><span class="sxs-lookup"><span data-stu-id="d8a46-157">Interface Property Methods</span></span>](interface-property-methods.md)
</dt> </dl>

 

 





