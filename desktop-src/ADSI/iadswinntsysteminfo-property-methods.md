---
title: Iadswinntsysteminfo-Eigenschaften Methoden (IADs. h)
description: Mit den Eigenschafts Methoden der iadswinntsysteminfo-Schnittstelle werden die in der folgenden Tabelle beschriebenen Eigenschaften angezeigt oder festgelegt. Weitere Informationen finden Sie unter Interface Property Methods.
ms.assetid: 5ba36851-3d03-4179-8cee-dbebe24b7c4e
ms.tgt_platform: multiple
keywords:
- Iadswinntsysteminfo-Eigenschaften Methoden ADSI
topic_type:
- apiref
api_name:
- IADsWinNTSystemInfo Property Methods
- IADsWinNTSystemInfo.UserName
- IADsWinNTSystemInfo.get_UserName
- IADsWinNTSystemInfo.ComputerName
- IADsWinNTSystemInfo.get_ComputerName
- IADsWinNTSystemInfo.DomainName
- IADsWinNTSystemInfo.get_DomainName
- IADsWinNTSystemInfo.PDC
- IADsWinNTSystemInfo.get_PDC
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5d647cf672032a4a06967ee034eb7b6430faf8dc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106337907"
---
# <a name="iadswinntsysteminfo-property-methods"></a><span data-ttu-id="49f71-105">Iadswinntsysteminfo-Eigenschaften Methoden</span><span class="sxs-lookup"><span data-stu-id="49f71-105">IADsWinNTSystemInfo Property Methods</span></span>

<span data-ttu-id="49f71-106">Mit den Eigenschafts Methoden der [**iadswinntsysteminfo**](/windows/desktop/api/Iads/nn-iads-iadswinntsysteminfo) -Schnittstelle werden die in der folgenden Tabelle beschriebenen Eigenschaften angezeigt oder festgelegt.</span><span class="sxs-lookup"><span data-stu-id="49f71-106">The property methods of the [**IADsWinNTSystemInfo**](/windows/desktop/api/Iads/nn-iads-iadswinntsysteminfo) interface get or set the properties described in the following table.</span></span> <span data-ttu-id="49f71-107">Weitere Informationen finden Sie unter [Interface Property Methods](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="49f71-107">For more information, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="49f71-108">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="49f71-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="49f71-109">**Computername**</span><span class="sxs-lookup"><span data-stu-id="49f71-109">**ComputerName**</span></span>
<span data-ttu-id="49f71-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="49f71-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="49f71-111">Der Name des Host Computers, auf dem die Anwendung ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="49f71-111">Name of the host computer where the application is running.</span></span>

<dt>

<span data-ttu-id="49f71-112">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="49f71-112">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="49f71-113">Skript Datentyp: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="49f71-113">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_ComputerName(
  [out] BSTR* pbstrComputer
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="49f71-114">**DomainName**</span><span class="sxs-lookup"><span data-stu-id="49f71-114">**DomainName**</span></span>
<span data-ttu-id="49f71-115"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="49f71-115"></dt> <dd> <dl></span></span>

<span data-ttu-id="49f71-116">Der Name der Domäne, zu der der Benutzer gehört.</span><span class="sxs-lookup"><span data-stu-id="49f71-116">Name of the domain to which the user belongs.</span></span>

<dt>

<span data-ttu-id="49f71-117">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="49f71-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="49f71-118">Skript Datentyp: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="49f71-118">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_DomainName(
  [out] BSTR* pbstrDomain
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="49f71-119">**PDC**</span><span class="sxs-lookup"><span data-stu-id="49f71-119">**PDC**</span></span>
<span data-ttu-id="49f71-120"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="49f71-120"></dt> <dd> <dl></span></span>

<span data-ttu-id="49f71-121">Der Name des primären Domänen Controllers, zu dem der Host Computer gehört.</span><span class="sxs-lookup"><span data-stu-id="49f71-121">Name of the primary domain controller to which the host computer belongs.</span></span>

<dt>

<span data-ttu-id="49f71-122">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="49f71-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="49f71-123">Skript Datentyp: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="49f71-123">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_PDC(
  [out] BSTR* pbstrPDC
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="49f71-124">**UserName**</span><span class="sxs-lookup"><span data-stu-id="49f71-124">**UserName**</span></span>
<span data-ttu-id="49f71-125"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="49f71-125"></dt> <dd> <dl></span></span>

<span data-ttu-id="49f71-126">Der Name des Benutzerkontos, unter dem das **winntsysteminfo** -Objekt erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="49f71-126">Name of the user account under which the **WinNTSystemInfo** object is created.</span></span>

<dt>

<span data-ttu-id="49f71-127">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="49f71-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="49f71-128">Skript Datentyp: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="49f71-128">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_UserName(
  [out] BSTR* pbstrUser
);
```


</dt> </dl> </dd> </dl>

 

## <a name="examples"></a><span data-ttu-id="49f71-129">Beispiele</span><span class="sxs-lookup"><span data-stu-id="49f71-129">Examples</span></span>

<span data-ttu-id="49f71-130">Im folgenden C/C++-Codebeispiel werden die WinNT-Systeminformationen abgerufen.</span><span class="sxs-lookup"><span data-stu-id="49f71-130">The following C/C++ code example retrieves the WinNT system information.</span></span> <span data-ttu-id="49f71-131">Aus Gründen der Übersichtlichkeit wird die Fehlerüberprüfung ausgelassen.</span><span class="sxs-lookup"><span data-stu-id="49f71-131">For brevity, error checking is omitted.</span></span>


```C++
#include <activeds.h>
#include <stdio.h>
 
int main()
{
   HRESULT hr;
 
   hr = CoInitialize(NULL);
 
    IADsWinNTSystemInfo *pNtSys;
    hr = CoCreateInstance(CLSID_WinNTSystemInfo,
                          NULL,
                          CLSCTX_INPROC_SERVER,
                          IID_IADsWinNTSystemInfo,
                          (void**)&pNTsys);
 
   BSTR bstr;
   hr = pNtSys->get_UserName(&bstr);
   if (SUCCEEDED(hr)) {
      printf("User: %S\n", bstr);
      SysFreeString(bstr);
   }
 
   hr = pNtSys->get_ComputerName(&bstr);
   if (SUCCEEDED(hr)) {
      printf("Computer: %S\n", bstr);
      SysFreeString(bstr);
   }
 
   hr = pNtSys->get_DomainName(&bstr);
   if (SUCCEEDED(hr)) {
      printf("Domain: %S\n", bstr);
      SysFreeString(bstr);
   }
 
   hr = pNtSys->get_PDC(&bstr);
   if (SUCCEEDED(hr)) {
      printf("PDC: %S\n", bstr);
      SysFreeString(bstr);
   }
 
   if(pNtSys) {
      pNtSys->Release();
   }
 
   CoUninitialize();
   return 0;
}
```



<span data-ttu-id="49f71-132">Im folgenden Visual Basic Codebeispiel werden die WinNT-Systeminformationen abgerufen.</span><span class="sxs-lookup"><span data-stu-id="49f71-132">The following Visual Basic code example retrieves the WinNT system information.</span></span>


```VB
Dim ntsys As New WinNTSystemInfo
Debug.print "User: " & ntsys.UserName
Debug.print "Computer: " & ntsys.ComputerName
Debug.print "Domain: " & ntsys.DomainName
Debug.print "PDC: " & ntsys.PDC
```



<span data-ttu-id="49f71-133">Im folgenden Codebeispiel für Visual Basic Scripting Edition/Active Server Pages werden die WinNT-Systeminformationen abgerufen.</span><span class="sxs-lookup"><span data-stu-id="49f71-133">The following Visual Basic Scripting Edition/Active Server Pages code example retrieves the WinNT system information.</span></span>


```VB
<%
Dim ntsys
Set ntsys = CreateObject("WinNTSystemInfo")
Response.Write "User: " & ntsys.UserName
Response.Write "Computer: " & ntsys.ComputerName
Response.Write "Domain: " & ntsys.DomainName
Response.Write "PDC: " & ntsys.PDC
%>
```



## <a name="requirements"></a><span data-ttu-id="49f71-134">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="49f71-134">Requirements</span></span>



| <span data-ttu-id="49f71-135">Anforderung</span><span class="sxs-lookup"><span data-stu-id="49f71-135">Requirement</span></span> | <span data-ttu-id="49f71-136">Wert</span><span class="sxs-lookup"><span data-stu-id="49f71-136">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="49f71-137">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="49f71-137">Minimum supported client</span></span><br/> | <span data-ttu-id="49f71-138">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="49f71-138">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="49f71-139">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="49f71-139">Minimum supported server</span></span><br/> | <span data-ttu-id="49f71-140">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="49f71-140">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="49f71-141">Header</span><span class="sxs-lookup"><span data-stu-id="49f71-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="49f71-142"><dt>IADs. h</dt></span><span class="sxs-lookup"><span data-stu-id="49f71-142"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="49f71-143">DLL</span><span class="sxs-lookup"><span data-stu-id="49f71-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="49f71-144"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="49f71-144"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="49f71-145">IID</span><span class="sxs-lookup"><span data-stu-id="49f71-145">IID</span></span><br/>                      | <span data-ttu-id="49f71-146">IID \_ iadswinntsysteminfo ist als 6c6d65dc-afd1-11d2-9cb9-0000f 87a369e definiert.</span><span class="sxs-lookup"><span data-stu-id="49f71-146">IID\_IADsWinNTSystemInfo is defined as 6C6D65DC-AFD1-11D2-9CB9-0000F87A369E</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="49f71-147">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="49f71-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="49f71-148">**Iadswinntsysteminfo**</span><span class="sxs-lookup"><span data-stu-id="49f71-148">**IADsWinNTSystemInfo**</span></span>](/windows/desktop/api/Iads/nn-iads-iadswinntsysteminfo)
</dt> </dl>

 

 





