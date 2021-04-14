---
title: Iadsfileservice-Eigenschaften Methoden (IADs. h)
description: Mit den Eigenschafts Methoden der iadsfileservice-Schnittstelle werden die in der folgenden Tabelle beschriebenen Eigenschaften angezeigt oder festgelegt. Weitere Informationen finden Sie unter Interface Property Methods.
ms.assetid: 1455df61-9218-450b-b956-1cf127364f24
ms.tgt_platform: multiple
keywords:
- Iadsfileservice-Eigenschaften Methoden ADSI
topic_type:
- apiref
api_name:
- IADsFileService Property Methods
- IADsFileService.Description
- IADsFileService.get_Description
- IADsFileService.put_Description
- IADsFileService.MaxUserCount
- IADsFileService.get_MaxUserCount
- IADsFileService.put_MaxUserCount
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e1f3a46b37522bbdce6e99b969811e2909c8ecc9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518461"
---
# <a name="iadsfileservice-property-methods"></a><span data-ttu-id="31539-105">Iadsfileservice-Eigenschaften Methoden</span><span class="sxs-lookup"><span data-stu-id="31539-105">IADsFileService Property Methods</span></span>

<span data-ttu-id="31539-106">Mit den Eigenschafts Methoden der [**iadsfileservice**](/windows/desktop/api/Iads/nn-iads-iadsfileservice) -Schnittstelle werden die in der folgenden Tabelle beschriebenen Eigenschaften angezeigt oder festgelegt.</span><span class="sxs-lookup"><span data-stu-id="31539-106">The property methods of the [**IADsFileService**](/windows/desktop/api/Iads/nn-iads-iadsfileservice) interface get or set the properties described in the following table.</span></span> <span data-ttu-id="31539-107">Weitere Informationen finden Sie unter [Interface Property Methods](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="31539-107">For more information, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="31539-108">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="31539-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="31539-109">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="31539-109">**Description**</span></span>
<span data-ttu-id="31539-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="31539-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="31539-111">Die Beschreibung des Datei Dienstanbieter.</span><span class="sxs-lookup"><span data-stu-id="31539-111">The description of the file service.</span></span>

<dt>

<span data-ttu-id="31539-112">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="31539-112">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="31539-113">Skript Datentyp: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="31539-113">Scripting data type: **BSTR**</span></span>
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

<span data-ttu-id="31539-114">**MaxUserCount**</span><span class="sxs-lookup"><span data-stu-id="31539-114">**MaxUserCount**</span></span>
<span data-ttu-id="31539-115"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="31539-115"></dt> <dd> <dl></span></span>

<span data-ttu-id="31539-116">Die maximal zulässige Anzahl von Benutzern, die für den Dienst zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="31539-116">The maximum number of users allowed on the service at any time.</span></span>

<dt>

<span data-ttu-id="31539-117">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="31539-117">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="31539-118">Skript Datentyp: **Long**</span><span class="sxs-lookup"><span data-stu-id="31539-118">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_MaxUserCount(
  [out] LONG* plMaxUserCount
);
HRESULT put_MaxUserCount(
  [in] LONG lMaxUserCount
);
```


</dt> </dl> </dd> </dl>

 

## <a name="remarks"></a><span data-ttu-id="31539-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="31539-119">Remarks</span></span>

<span data-ttu-id="31539-120">Sie müssen den Datei Dienst durchlaufen, um auf Dateifreigaben, Sitzungen und Ressourcen auf einem Computer zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="31539-120">You must go through the file service to access file shares, sessions, and resources on a computer.</span></span>

## <a name="examples"></a><span data-ttu-id="31539-121">Beispiele</span><span class="sxs-lookup"><span data-stu-id="31539-121">Examples</span></span>

<span data-ttu-id="31539-122">Im folgenden Codebeispiel wird eine Beschreibung für geschrieben und das Benutzerlimit des Datei Dienstanbieter überprüft.</span><span class="sxs-lookup"><span data-stu-id="31539-122">The following code example writes a description for and check the user limit of the file service.</span></span>


```VB
Dim fs As IADsFileService
On Error GoTo Cleanup

' Bind to a file service object on "myComputer" in the local domain.
Set fs = GetObject("WinNT://myComputer/LanmanServer")

fs.Description = "WinNT file service."
n = fs.MaxUserCount
If n = -1 Then
   MsgBox "No limit has been imposed on number of users allowed."
Else
   MsgBox n & " users are allowed."
End If

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set fs = Nothing
```



<span data-ttu-id="31539-123">Im folgenden Codebeispiel wird eine Beschreibung für geschrieben und das Benutzerlimit für ein Datei Dienst Objekt überprüft.</span><span class="sxs-lookup"><span data-stu-id="31539-123">The following code example writes a description for and check the user limit on a file service object.</span></span>


```C++
HRESULT CheckFileService()
{
    IADsFileService *pFs = NULL;
    LPWSTR adsPath = L"WinNT://myComputer/LanmanServer";
    HRESULT hr = S_OK;
    long count = 0;

    hr = ADsGetObject(adsPath, IID_IADsFileService, (void**)&pFs)
    if(FAILED(hr)) {goto Cleanup;}

    hr = pFs->put_Description(CComBSTR("WinNT File Service"));
    if(FAILED(hr)) {goto Cleanup;}

    hr = pFs->SetInfo();
    if(FAILED(hr)) {goto Cleanup;}

    hr = pFs->get_MaxUserCount(&count);
    if(FAILED(hr)) {goto Cleanup;}

    if(count == -1) {
        printf("No limit has been imposed on the number of users.\n");
    } 
    else {
        printf("Number of allowed users are %d\n",count);
    }

Cleanup:
    if(pFs) pFs->Release();
    return S_OK;
}
```



## <a name="requirements"></a><span data-ttu-id="31539-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="31539-124">Requirements</span></span>



| <span data-ttu-id="31539-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="31539-125">Requirement</span></span> | <span data-ttu-id="31539-126">Wert</span><span class="sxs-lookup"><span data-stu-id="31539-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="31539-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="31539-127">Minimum supported client</span></span><br/> | <span data-ttu-id="31539-128">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="31539-128">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="31539-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="31539-129">Minimum supported server</span></span><br/> | <span data-ttu-id="31539-130">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="31539-130">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="31539-131">Header</span><span class="sxs-lookup"><span data-stu-id="31539-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="31539-132"><dt>IADs. h</dt></span><span class="sxs-lookup"><span data-stu-id="31539-132"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="31539-133">DLL</span><span class="sxs-lookup"><span data-stu-id="31539-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="31539-134"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="31539-134"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="31539-135">IID</span><span class="sxs-lookup"><span data-stu-id="31539-135">IID</span></span><br/>                      | <span data-ttu-id="31539-136">IID \_ iadsfileservice ist als A89D1900-31CA-11CF-A98A-00AA006BC149 definiert.</span><span class="sxs-lookup"><span data-stu-id="31539-136">IID\_IADsFileService is defined as A89D1900-31CA-11CF-A98A-00AA006BC149</span></span><br/>      |



## <a name="see-also"></a><span data-ttu-id="31539-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="31539-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="31539-138">**Iadsservice**</span><span class="sxs-lookup"><span data-stu-id="31539-138">**IADsService**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsservice)
</dt> <dt>

[<span data-ttu-id="31539-139">**Iadsfileservice**</span><span class="sxs-lookup"><span data-stu-id="31539-139">**IADsFileService**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsfileservice)
</dt> <dt>

[<span data-ttu-id="31539-140">**Iadsfileserviceoperations**</span><span class="sxs-lookup"><span data-stu-id="31539-140">**IADsFileServiceOperations**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsfileserviceoperations)
</dt> <dt>

[<span data-ttu-id="31539-141">**Iadsserviceoperations**</span><span class="sxs-lookup"><span data-stu-id="31539-141">**IADsServiceOperations**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsserviceoperations)
</dt> <dt>

[<span data-ttu-id="31539-142">Schnittstelleneigenschaften Methoden</span><span class="sxs-lookup"><span data-stu-id="31539-142">Interface Property Methods</span></span>](interface-property-methods.md)
</dt> </dl>

 

 





