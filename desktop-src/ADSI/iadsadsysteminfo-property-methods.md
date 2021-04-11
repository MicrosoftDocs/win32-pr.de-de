---
title: IADsADSystemInfo-Eigenschaften Methoden (IADs. h)
description: Mit den Eigenschafts Methoden der IADsADSystemInfo-Schnittstelle werden die in der folgenden Tabelle beschriebenen Eigenschaften angezeigt oder festgelegt. Weitere Informationen finden Sie unter Interface Property Methods.
ms.assetid: 1cdaa610-4341-4825-b2f9-dd495a9147ff
ms.tgt_platform: multiple
keywords:
- IADsADSystemInfo-Eigenschaften Methoden ADSI
topic_type:
- apiref
api_name:
- IADsADSystemInfo Property Methods
- IADsADSystemInfo.UserName
- IADsADSystemInfo.get_UserName
- IADsADSystemInfo.ComputerName
- IADsADSystemInfo.get_ComputerName
- IADsADSystemInfo.SiteName
- IADsADSystemInfo.get_SiteName
- IADsADSystemInfo.DomainShortName
- IADsADSystemInfo.get_DomainShortName
- IADsADSystemInfo.DomainDNSName
- IADsADSystemInfo.get_DomainDNSName
- IADsADSystemInfo.ForestDNSName
- IADsADSystemInfo.get_ForestDNSName
- IADsADSystemInfo.PDCRoleOwner
- IADsADSystemInfo.get_PDCRoleOwner
- IADsADSystemInfo.SchemaRoleOwner
- IADsADSystemInfo.get_SchemaRoleOwner
- IADsADSystemInfo.IsNativeMode
- IADsADSystemInfo.get_IsNativeMode
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d8dba53dfda4bb8f4dd3290cb2737cdeb4e8a6d3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105165"
---
# <a name="iadsadsysteminfo-property-methods"></a><span data-ttu-id="88fb4-105">IADsADSystemInfo-Eigenschaften Methoden</span><span class="sxs-lookup"><span data-stu-id="88fb4-105">IADsADSystemInfo Property Methods</span></span>

<span data-ttu-id="88fb4-106">Mit den Eigenschafts Methoden der [**IADsADSystemInfo**](/windows/desktop/api/Iads/nn-iads-iadsadsysteminfo) -Schnittstelle werden die in der folgenden Tabelle beschriebenen Eigenschaften angezeigt oder festgelegt.</span><span class="sxs-lookup"><span data-stu-id="88fb4-106">The property methods of the [**IADsADSystemInfo**](/windows/desktop/api/Iads/nn-iads-iadsadsysteminfo) interface get or set the properties described in the following table.</span></span> <span data-ttu-id="88fb4-107">Weitere Informationen finden Sie unter [Interface Property Methods](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="88fb4-107">For more information, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="88fb4-108">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="88fb4-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="88fb4-109">**Computername**</span><span class="sxs-lookup"><span data-stu-id="88fb4-109">**ComputerName**</span></span>
<span data-ttu-id="88fb4-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="88fb4-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="88fb4-111">Ruft den Distinguished Name des lokalen Computers ab.</span><span class="sxs-lookup"><span data-stu-id="88fb4-111">Retrieves the distinguished name of the local computer.</span></span>

<dt>

<span data-ttu-id="88fb4-112">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="88fb4-112">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="88fb4-113">Skript Datentyp: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="88fb4-113">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_ComputerName(
  [out] BSTR* pbstrComputer
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="88fb4-114">**DomainDNSName**</span><span class="sxs-lookup"><span data-stu-id="88fb4-114">**DomainDNSName**</span></span>
<span data-ttu-id="88fb4-115"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="88fb4-115"></dt> <dd> <dl></span></span>

<span data-ttu-id="88fb4-116">Ruft den DNS-Namen der Domäne des lokalen Computers ab, z. b. "domainname.CompanyName.com".</span><span class="sxs-lookup"><span data-stu-id="88fb4-116">Retrieves the DNS name of the local computer's domain, such as "domainName.companyName.com".</span></span>

<dt>

<span data-ttu-id="88fb4-117">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="88fb4-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="88fb4-118">Skript Datentyp: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="88fb4-118">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_DomainDNSName(
  [out] BSTR* pbstr
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="88fb4-119">**Domainshortname**</span><span class="sxs-lookup"><span data-stu-id="88fb4-119">**DomainShortName**</span></span>
<span data-ttu-id="88fb4-120"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="88fb4-120"></dt> <dd> <dl></span></span>

<span data-ttu-id="88fb4-121">Ruft den Kurznamen der Domäne des lokalen Computers ab, z. b. "Domänen Name".</span><span class="sxs-lookup"><span data-stu-id="88fb4-121">Retrieves the short name of the local computer's domain, such as "domainName".</span></span>

<dt>

<span data-ttu-id="88fb4-122">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="88fb4-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="88fb4-123">Skript Datentyp: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="88fb4-123">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_DomainShortName(
  [out] BSTR* pbstrDSN
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="88fb4-124">**ForestDNSName**</span><span class="sxs-lookup"><span data-stu-id="88fb4-124">**ForestDNSName**</span></span>
<span data-ttu-id="88fb4-125"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="88fb4-125"></dt> <dd> <dl></span></span>

<span data-ttu-id="88fb4-126">Ruft den DNS-Namen der Gesamtstruktur des lokalen Computers ab.</span><span class="sxs-lookup"><span data-stu-id="88fb4-126">Retrieves the DNS name of the local computer's forest.</span></span>

<dt>

<span data-ttu-id="88fb4-127">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="88fb4-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="88fb4-128">Skript Datentyp: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="88fb4-128">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_ForestDNSName(
  [out] BSTR* pbstr
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="88fb4-129">**Isnativemode**</span><span class="sxs-lookup"><span data-stu-id="88fb4-129">**IsNativeMode**</span></span>
<span data-ttu-id="88fb4-130"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="88fb4-130"></dt> <dd> <dl></span></span>

<span data-ttu-id="88fb4-131">Bestimmt, ob sich die Domäne des lokalen Computers im einheitlichen oder gemischten Modus befindet.</span><span class="sxs-lookup"><span data-stu-id="88fb4-131">Determines whether the local computer's domain is in native or mixed mode.</span></span>

<dt>

<span data-ttu-id="88fb4-132">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="88fb4-132">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="88fb4-133">Skript Datentyp: **bool**</span><span class="sxs-lookup"><span data-stu-id="88fb4-133">Scripting data type: **BOOL**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_IsNativeMode(
  [out] BOOL* pvBool
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="88fb4-134">**PdcRoleOwner**</span><span class="sxs-lookup"><span data-stu-id="88fb4-134">**PDCRoleOwner**</span></span>
<span data-ttu-id="88fb4-135"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="88fb4-135"></dt> <dd> <dl></span></span>

<span data-ttu-id="88fb4-136">Ruft den Distinguished Name des Verzeichnisdienst-Agent-Objekts (DSA) für den Domänen Controller ab, der die Rolle des primären Domänen Controllers in der Domäne des lokalen Computers besitzt.</span><span class="sxs-lookup"><span data-stu-id="88fb4-136">Retrieves the distinguished name of the directory service agent (DSA) object for the DC that owns the primary domain controller role in the local computer's domain.</span></span>

<dt>

<span data-ttu-id="88fb4-137">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="88fb4-137">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="88fb4-138">Skript Datentyp: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="88fb4-138">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_PDCRoleOwner(
  [out] BSTR* pbstr
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="88fb4-139">**SchemaRoleOwner**</span><span class="sxs-lookup"><span data-stu-id="88fb4-139">**SchemaRoleOwner**</span></span>
<span data-ttu-id="88fb4-140"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="88fb4-140"></dt> <dd> <dl></span></span>

<span data-ttu-id="88fb4-141">Ruft den Distinguished Name des Verzeichnisdienst-Agent-Objekts (DSA) für den Domänen Controller ab, der die Schema Master Rolle in der Gesamtstruktur des lokalen Computers besitzt.</span><span class="sxs-lookup"><span data-stu-id="88fb4-141">Retrieves the distinguished name of the directory service agent (DSA) object for the DC that owns the schema master role in the local computer's forest.</span></span>

<dt>

<span data-ttu-id="88fb4-142">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="88fb4-142">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="88fb4-143">Skript Datentyp: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="88fb4-143">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_SchemaRoleOwner(
  [out] BSTR* pbstr
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="88fb4-144">**Sitename**</span><span class="sxs-lookup"><span data-stu-id="88fb4-144">**SiteName**</span></span>
<span data-ttu-id="88fb4-145"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="88fb4-145"></dt> <dd> <dl></span></span>

<span data-ttu-id="88fb4-146">Ruft den Standortnamen des lokalen Computers ab.</span><span class="sxs-lookup"><span data-stu-id="88fb4-146">Retrieves the site name of the local computer.</span></span>

<dt>

<span data-ttu-id="88fb4-147">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="88fb4-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="88fb4-148">Skript Datentyp: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="88fb4-148">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_SiteName(
  [out] BSTR* pbstrSite
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="88fb4-149">**UserName**</span><span class="sxs-lookup"><span data-stu-id="88fb4-149">**UserName**</span></span>
<span data-ttu-id="88fb4-150"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="88fb4-150"></dt> <dd> <dl></span></span>

<span data-ttu-id="88fb4-151">Ruft den Active Directory Distinguished Name des aktuellen Benutzers ab, der der angemeldete Benutzer ist, oder der Benutzer, der vom aufrufenden Thread angenommen wird.</span><span class="sxs-lookup"><span data-stu-id="88fb4-151">Retrieves the Active Directory distinguished name of the current user, which is the logged-on user or the user impersonated by the calling thread.</span></span>

<dt>

<span data-ttu-id="88fb4-152">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="88fb4-152">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="88fb4-153">Skript Datentyp: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="88fb4-153">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_UserName(
  [out] BSTR* pbstrUser
);
```


</dt> </dl> </dd> </dl>

 

## <a name="examples"></a><span data-ttu-id="88fb4-154">Beispiele</span><span class="sxs-lookup"><span data-stu-id="88fb4-154">Examples</span></span>

<span data-ttu-id="88fb4-155">Im folgenden C++-Codebeispiel werden die Windows-Systeminformationen abgerufen.</span><span class="sxs-lookup"><span data-stu-id="88fb4-155">The following C++ code example retrieves the Windows system information.</span></span> <span data-ttu-id="88fb4-156">Aus Gründen der Übersichtlichkeit wird die Fehlerüberprüfung ausgelassen.</span><span class="sxs-lookup"><span data-stu-id="88fb4-156">For brevity, error checking is omitted.</span></span>


```C++
#include <activeds.h>
#include <stdio.h>
 
int main()
{
   HRESULT hr;
 
   hr = CoInitialize(NULL);
 
    IADsADSystemInfo *pSys;
    hr = CoCreateInstance(CLSID_ADSystemInfo,
                          NULL,
                          CLSCTX_INPROC_SERVER,
                          IID_IADsADSystemInfo,
                          (void**)&pSys);
 
   BSTR bstr;
   hr = pSys->get_UserName(&bstr);
   if (SUCCEEDED(hr)) {
      printf("User: %S\n", bstr);
      SysFreeString(bstr);
   }
 
   hr = pSys->get_ComputerName(&bstr);
   if (SUCCEEDED(hr)) {
      printf("Computer: %S\n", bstr);
      SysFreeString(bstr);
   }
 
   hr = pSys->get_DomainDNSName(&bstr);
   if (SUCCEEDED(hr)) {
      printf("Domain: %S\n", bstr);
      SysFreeString(bstr);
   }
 
   hr = pSys->get_PDCRoleOwner(&bstr);
   if (SUCCEEDED(hr)) {
      printf("PDC Role owner: %S\n", bstr);
      SysFreeString(bstr);
   }
 
   if(pSys) {
      pSys->Release();
   }
 
   CoUninitialize();
   return 0;
}
```



<span data-ttu-id="88fb4-157">Im folgenden Visual Basic Codebeispiel werden die Windows-Systeminformationen abgerufen.</span><span class="sxs-lookup"><span data-stu-id="88fb4-157">The following Visual Basic code example retrieves the Windows system information.</span></span>


```VB
Dim sys As New ADSystemInfo
Debug.print "User: " & sys.UserName
Debug.print "Computer: " & sys.ComputerName
Debug.print "Domain: " & sys.DomainDNSName
Debug.print "PDC Role Owner: " & sys.PDCRoleOwner
```



<span data-ttu-id="88fb4-158">Im folgenden VBScript/ASP-Codebeispiel werden die Windows-Systeminformationen abgerufen.</span><span class="sxs-lookup"><span data-stu-id="88fb4-158">The following VBScript/ASP code example retrieves the Windows system information.</span></span>


```VB
<%
Dim sys
Set sys = CreateObject("ADSystemInfo")
Response.Write "User: " & sys.UserName
Response.Write "Computer: " & sys.ComputerName
Response.Write "Domain: " & sys.DomainDNSName
Response.Write "PDC Role Owner: " & sys.PDCRoleOwner
%>
```



## <a name="requirements"></a><span data-ttu-id="88fb4-159">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="88fb4-159">Requirements</span></span>



| <span data-ttu-id="88fb4-160">Anforderung</span><span class="sxs-lookup"><span data-stu-id="88fb4-160">Requirement</span></span> | <span data-ttu-id="88fb4-161">Wert</span><span class="sxs-lookup"><span data-stu-id="88fb4-161">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="88fb4-162">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="88fb4-162">Minimum supported client</span></span><br/> | <span data-ttu-id="88fb4-163">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="88fb4-163">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="88fb4-164">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="88fb4-164">Minimum supported server</span></span><br/> | <span data-ttu-id="88fb4-165">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="88fb4-165">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="88fb4-166">Header</span><span class="sxs-lookup"><span data-stu-id="88fb4-166">Header</span></span><br/>                   | <dl> <span data-ttu-id="88fb4-167"><dt>IADs. h</dt></span><span class="sxs-lookup"><span data-stu-id="88fb4-167"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="88fb4-168">DLL</span><span class="sxs-lookup"><span data-stu-id="88fb4-168">DLL</span></span><br/>                      | <dl> <span data-ttu-id="88fb4-169"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="88fb4-169"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="88fb4-170">IID</span><span class="sxs-lookup"><span data-stu-id="88fb4-170">IID</span></span><br/>                      | <span data-ttu-id="88fb4-171">IID \_ IADsADSystemInfo ist als 5bb11929-afd1-11d2-9cb9-0000f87a369e definiert.</span><span class="sxs-lookup"><span data-stu-id="88fb4-171">IID\_IADsADSystemInfo is defined as 5BB11929-AFD1-11D2-9CB9-0000F87A369E</span></span><br/>     |



## <a name="see-also"></a><span data-ttu-id="88fb4-172">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="88fb4-172">See also</span></span>

<dl> <dt>

[<span data-ttu-id="88fb4-173">**IADsADSystemInfo**</span><span class="sxs-lookup"><span data-stu-id="88fb4-173">**IADsADSystemInfo**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsadsysteminfo)
</dt> <dt>

[<span data-ttu-id="88fb4-174">**CoCreateInstance**</span><span class="sxs-lookup"><span data-stu-id="88fb4-174">**CoCreateInstance**</span></span>](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance)
</dt> </dl>

 

