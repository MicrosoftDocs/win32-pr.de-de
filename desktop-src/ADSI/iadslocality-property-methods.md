---
title: Iadslolichkeit-Eigenschaften Methoden (IADs. h)
description: Mit den Methoden der iadsloalität-Schnittstelle werden die in diesem Thema beschriebenen Eigenschaften gelesen und geschrieben. Weitere Informationen finden Sie unter Interface Property Methods.
ms.assetid: 5d1cea40-62fb-49d4-857f-4563e9db7f51
ms.tgt_platform: multiple
keywords:
- Iadslolichkeit-Eigenschaften Methoden ADSI
topic_type:
- apiref
api_name:
- IADsLocality Property Methods
- IADsLocality.Description
- IADsLocality.get_Description
- IADsLocality.put_Description
- IADsLocality.LocalityName
- IADsLocality.get_LocalityName
- IADsLocality.put_LocalityName
- IADsLocality.PostalAddress
- IADsLocality.get_PostalAddress
- IADsLocality.put_PostalAddress
- IADsLocality.SeeAlso
- IADsLocality.get_SeeAlso
- IADsLocality.put_SeeAlso
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 34023f0af5365deb4f023d53a843dcf688c40afd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956909"
---
# <a name="iadslocality-property-methods"></a><span data-ttu-id="1e2ea-105">Iadslolichkeit-Eigenschaften Methoden</span><span class="sxs-lookup"><span data-stu-id="1e2ea-105">IADsLocality Property Methods</span></span>

<span data-ttu-id="1e2ea-106">Mit den Methoden der [**iadsloalität**](/windows/desktop/api/Iads/nn-iads-iadslocality) -Schnittstelle werden die in diesem Thema beschriebenen Eigenschaften gelesen und geschrieben.</span><span class="sxs-lookup"><span data-stu-id="1e2ea-106">The methods of the [**IADsLocality**](/windows/desktop/api/Iads/nn-iads-iadslocality) interface read and write the properties described in this topic.</span></span> <span data-ttu-id="1e2ea-107">Weitere Informationen finden Sie unter [Interface Property Methods](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="1e2ea-107">For more information, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="1e2ea-108">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="1e2ea-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="1e2ea-109">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="1e2ea-109">**Description**</span></span>
<span data-ttu-id="1e2ea-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="1e2ea-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="1e2ea-111">Gibt den Text an, der den Ort beschreibt.</span><span class="sxs-lookup"><span data-stu-id="1e2ea-111">Indicates the text that describes the locality.</span></span>

<dt>

<span data-ttu-id="1e2ea-112">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="1e2ea-112">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="1e2ea-113">Skript Datentyp: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="1e2ea-113">Scripting data type: **BSTR**</span></span>
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

<span data-ttu-id="1e2ea-114">**Localityname**</span><span class="sxs-lookup"><span data-stu-id="1e2ea-114">**LocalityName**</span></span>
<span data-ttu-id="1e2ea-115"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="1e2ea-115"></dt> <dd> <dl></span></span>

<span data-ttu-id="1e2ea-116">Gibt den Namen der geografischen Region an, wie durch dieses lokalisiererobjekt dargestellt.</span><span class="sxs-lookup"><span data-stu-id="1e2ea-116">Indicates the name of the geographical region as represented by this locality object.</span></span>

<dt>

<span data-ttu-id="1e2ea-117">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="1e2ea-117">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="1e2ea-118">Skript Datentyp: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="1e2ea-118">Scripting data type: **BSTR**</span></span>
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

<span data-ttu-id="1e2ea-119">**PostalAddress**</span><span class="sxs-lookup"><span data-stu-id="1e2ea-119">**PostalAddress**</span></span>
<span data-ttu-id="1e2ea-120"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="1e2ea-120"></dt> <dd> <dl></span></span>

<span data-ttu-id="1e2ea-121">Gibt die Haupt Postadresse der Lokalität an.</span><span class="sxs-lookup"><span data-stu-id="1e2ea-121">Indicates the main postal address of the locality.</span></span>

<dt>

<span data-ttu-id="1e2ea-122">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="1e2ea-122">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="1e2ea-123">Skript Datentyp: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="1e2ea-123">Scripting data type: **BSTR**</span></span>
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

<span data-ttu-id="1e2ea-124">**SeeAlso**</span><span class="sxs-lookup"><span data-stu-id="1e2ea-124">**SeeAlso**</span></span>
<span data-ttu-id="1e2ea-125"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="1e2ea-125"></dt> <dd> <dl></span></span>

<span data-ttu-id="1e2ea-126">Gibt ein Array von ADsPath-Namen der Verzeichnisobjekte an, die für dieses-Objekt relevant sind.</span><span class="sxs-lookup"><span data-stu-id="1e2ea-126">Indicates an array of ADsPath names of directory objects relevant to this object.</span></span>

<dt>

<span data-ttu-id="1e2ea-127">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="1e2ea-127">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="1e2ea-128">Skript Datentyp: **Variant**</span><span class="sxs-lookup"><span data-stu-id="1e2ea-128">Scripting data type: **VARIANT**</span></span>
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


</dt> </dl> </dd> </dl>

 

## <a name="examples"></a><span data-ttu-id="1e2ea-129">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1e2ea-129">Examples</span></span>

<span data-ttu-id="1e2ea-130">Im folgenden Codebeispiel werden die Lokalisierungsdaten eines Container Objekts angezeigt.</span><span class="sxs-lookup"><span data-stu-id="1e2ea-130">The following code example displays the locality data of a container object.</span></span> <span data-ttu-id="1e2ea-131">Dabei wird davon ausgegangen, dass ein Lokalisier Objekt mit dem Namen "mylokalität" für das Container Objekt erstellt und die Eigenschaften festgelegt wurden.</span><span class="sxs-lookup"><span data-stu-id="1e2ea-131">It assumes that a locality object, named "myLocality", has been created for the container object and the properties have been set.</span></span>


```VB
Dim dom As IADsContainer
Dim loc As IADsLocality
On Error GoTo Cleanup
 
Set dom = getObject("LDAP://adsrv1/dc=Fabrikam, dc=Com")
Set loc = dom.GetObject("locality","L=myLocality")
Debug.Print loc.Name
Debug.Print loc.LocalityName
Debug.Print loc.Description
Debug.Print loc.PostalAddress
Debug.Print loc.SeeAlso

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set dom = Nothing
    Set loc = Nothing
```



## <a name="requirements"></a><span data-ttu-id="1e2ea-132">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1e2ea-132">Requirements</span></span>



| <span data-ttu-id="1e2ea-133">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1e2ea-133">Requirement</span></span> | <span data-ttu-id="1e2ea-134">Wert</span><span class="sxs-lookup"><span data-stu-id="1e2ea-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1e2ea-135">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1e2ea-135">Minimum supported client</span></span><br/> | <span data-ttu-id="1e2ea-136">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1e2ea-136">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="1e2ea-137">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1e2ea-137">Minimum supported server</span></span><br/> | <span data-ttu-id="1e2ea-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1e2ea-138">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="1e2ea-139">Header</span><span class="sxs-lookup"><span data-stu-id="1e2ea-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="1e2ea-140"><dt>IADs. h</dt></span><span class="sxs-lookup"><span data-stu-id="1e2ea-140"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="1e2ea-141">DLL</span><span class="sxs-lookup"><span data-stu-id="1e2ea-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1e2ea-142"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1e2ea-142"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="1e2ea-143">IID</span><span class="sxs-lookup"><span data-stu-id="1e2ea-143">IID</span></span><br/>                      | <span data-ttu-id="1e2ea-144">IID \_ iadslolichkeit ist als A05E03A2-Effe-11CF-8ABC-00C04FD8D503 definiert.</span><span class="sxs-lookup"><span data-stu-id="1e2ea-144">IID\_IADsLocality is defined as A05E03A2-EFFE-11CF-8ABC-00C04FD8D503</span></span><br/>         |



## <a name="see-also"></a><span data-ttu-id="1e2ea-145">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1e2ea-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1e2ea-146">**IADs**</span><span class="sxs-lookup"><span data-stu-id="1e2ea-146">**IADs**</span></span>](/windows/desktop/api/Iads/nn-iads-iads)
</dt> <dt>

[<span data-ttu-id="1e2ea-147">**Iadsloalität**</span><span class="sxs-lookup"><span data-stu-id="1e2ea-147">**IADsLocality**</span></span>](/windows/desktop/api/Iads/nn-iads-iadslocality)
</dt> <dt>

[<span data-ttu-id="1e2ea-148">Schnittstelleneigenschaften Methoden</span><span class="sxs-lookup"><span data-stu-id="1e2ea-148">Interface Property Methods</span></span>](interface-property-methods.md)
</dt> </dl>

 

 





