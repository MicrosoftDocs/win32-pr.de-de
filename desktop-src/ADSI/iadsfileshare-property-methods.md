---
title: Iadsfileshare-Eigenschaften Methoden (IADs. h)
description: Mit den Eigenschafts Methoden der iadsfileshare-Schnittstelle werden die in der folgenden Tabelle beschriebenen Eigenschaften angezeigt oder festgelegt. Weitere Informationen finden Sie unter Interface Property Methods.
ms.assetid: c5a81c42-507f-4a68-b6f4-83097bd0fa01
ms.tgt_platform: multiple
keywords:
- Iadsfileshare-Eigenschaften Methoden ADSI
topic_type:
- apiref
api_name:
- IADsFileShare Property Methods
- IADsFileShare.CurrentUserCount
- IADsFileShare.get_CurrentUserCount
- IADsFileShare.Description
- IADsFileShare.get_Description
- IADsFileShare.put_Description
- IADsFileShare.HostComputer
- IADsFileShare.get_HostComputer
- IADsFileShare.put_HostComputer
- IADsFileShare.MaxUserCount
- IADsFileShare.get_MaxUserCount
- IADsFileShare.Path
- IADsFileShare.get_Path
- IADsFileShare.put_Path
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f38369a4054f1848d5e35ff8bdb2dda9e9423a87
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105140"
---
# <a name="iadsfileshare-property-methods"></a><span data-ttu-id="8b512-105">Iadsfileshare-Eigenschaften Methoden</span><span class="sxs-lookup"><span data-stu-id="8b512-105">IADsFileShare Property Methods</span></span>

<span data-ttu-id="8b512-106">Mit den Eigenschafts Methoden der [**iadsfileshare**](/windows/desktop/api/Iads/nn-iads-iadsfileshare) -Schnittstelle werden die in der folgenden Tabelle beschriebenen Eigenschaften angezeigt oder festgelegt.</span><span class="sxs-lookup"><span data-stu-id="8b512-106">The property methods of the [**IADsFileshare**](/windows/desktop/api/Iads/nn-iads-iadsfileshare) interface get or set the properties described in the following table.</span></span> <span data-ttu-id="8b512-107">Weitere Informationen finden Sie unter [Interface Property Methods](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="8b512-107">For more information, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="8b512-108">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="8b512-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="8b512-109">**Currentusercount**</span><span class="sxs-lookup"><span data-stu-id="8b512-109">**CurrentUserCount**</span></span>
<span data-ttu-id="8b512-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="8b512-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="8b512-111">Die Anzahl der Benutzer, die mit der Freigabe verbunden sind.</span><span class="sxs-lookup"><span data-stu-id="8b512-111">The number of users connected to the share.</span></span>

<dt>

<span data-ttu-id="8b512-112">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8b512-112">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8b512-113">Skript Datentyp: **Long**</span><span class="sxs-lookup"><span data-stu-id="8b512-113">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_CurrentUserCount(
  [out] LONG* plCurrentUserCount
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="8b512-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="8b512-114">**Description**</span></span>
<span data-ttu-id="8b512-115"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="8b512-115"></dt> <dd> <dl></span></span>

<span data-ttu-id="8b512-116">Die Beschreibung der Dateifreigabe.</span><span class="sxs-lookup"><span data-stu-id="8b512-116">The description of the file share.</span></span>

<dt>

<span data-ttu-id="8b512-117">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="8b512-117">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="8b512-118">Skript Datentyp: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="8b512-118">Scripting data type: **BSTR**</span></span>
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

<span data-ttu-id="8b512-119">**Host Computer**</span><span class="sxs-lookup"><span data-stu-id="8b512-119">**HostComputer**</span></span>
<span data-ttu-id="8b512-120"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="8b512-120"></dt> <dd> <dl></span></span>

<span data-ttu-id="8b512-121">Ein ADsPath-Verweis auf den Host Computer.</span><span class="sxs-lookup"><span data-stu-id="8b512-121">An ADsPath reference to the host computer.</span></span>

<dt>

<span data-ttu-id="8b512-122">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="8b512-122">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="8b512-123">Skript Datentyp: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="8b512-123">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_HostComputer(
  [out] BSTR* pbstrHostComputer
);
HRESULT put_HostComputer(
  [in] BSTR bstrHostComputer
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="8b512-124">**MaxUserCount**</span><span class="sxs-lookup"><span data-stu-id="8b512-124">**MaxUserCount**</span></span>
<span data-ttu-id="8b512-125"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="8b512-125"></dt> <dd> <dl></span></span>

<span data-ttu-id="8b512-126">Die maximale Anzahl von Benutzern, die gleichzeitig auf die Freigabe zugreifen dürfen.</span><span class="sxs-lookup"><span data-stu-id="8b512-126">The maximum number of users allowed to access the share at one time.</span></span>

<dt>

<span data-ttu-id="8b512-127">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8b512-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8b512-128">Skript Datentyp: **Long**</span><span class="sxs-lookup"><span data-stu-id="8b512-128">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_MaxUserCount(
  [out] LONG* plMaxUserCount
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="8b512-129">**Pfad**</span><span class="sxs-lookup"><span data-stu-id="8b512-129">**Path**</span></span>
<span data-ttu-id="8b512-130"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="8b512-130"></dt> <dd> <dl></span></span>

<span data-ttu-id="8b512-131">Der Dateisystempfad zum freigegebenen Verzeichnis.</span><span class="sxs-lookup"><span data-stu-id="8b512-131">The file system path to the shared directory.</span></span>

<dt>

<span data-ttu-id="8b512-132">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="8b512-132">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="8b512-133">Skript Datentyp: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="8b512-133">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Path(
  [out] BSTR* pbstrPath
);
HRESULT put_Path(
  [in] BSTR bstrPath
);
```


</dt> </dl> </dd> </dl>

 

## <a name="examples"></a><span data-ttu-id="8b512-134">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8b512-134">Examples</span></span>

<span data-ttu-id="8b512-135">Wenn Sie auf die Eigenschaften von Dateifreigaben auf einem Computer zugreifen möchten, müssen Sie zunächst eine Bindung an den "LanManServer" auf dem Computer herstellen.</span><span class="sxs-lookup"><span data-stu-id="8b512-135">To access the properties of file shares on a computer, you must first bind to the "LanmanServer" on the machine.</span></span> <span data-ttu-id="8b512-136">Im folgenden Codebeispiel wird gezeigt, wie Sie die Beschreibung und die maximale Anzahl zulässiger Benutzer für alle öffentlichen Dateifreigaben auf dem Computer (mit dem Namen "MyMachine") in der Standard Domäne einrichten.</span><span class="sxs-lookup"><span data-stu-id="8b512-136">The following code example shows how to set up the description and the maximum number of allowed users for all the public file shares on the computer, named as "myMachine", in the default domain.</span></span>


```VB
Dim fs As IADsFileService
Dim share As IADsFileShare
On Error GoTo Cleanup

Set fs = GetObject("WinNT://myMachine/LanmanServer")
If (fs.class = "FileService") Then
    For Each share In fs
        share.description = share.name & " is my working folder."
        share.MaxUserCount =  10
        share.SetInfo
    Next share
End if

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set fs = Nothing
    Set share = Nothing
```



<span data-ttu-id="8b512-137">Im folgenden Codebeispiel wird gezeigt, wie das vorhandene Verzeichnis "C: \\ MyFolder" als öffentliche Dateifreigabe erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="8b512-137">The following code example shows how to make the existing C:\\MyFolder directory a public file share.</span></span>


```VB
Dim fs As IADsFileShare
Dim cont As IADsContainer
On Error GoTo Cleanup
 
Set cont = GetObject("WinNT://yourDomain/yourMachineName/LanmanServer")
 
Set fs = cont.Create("FileShare", "Public")
Debug.Print fs.Class
fs.Path = "C:\MyFolder"
fs.SetInfo

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set cont = Nothing
    Set fs = Nothing
```



<span data-ttu-id="8b512-138">Im folgenden Codebeispiel wird das vorhandene Verzeichnis C: \\ MyFolder zu einer öffentlichen Dateifreigabe.</span><span class="sxs-lookup"><span data-stu-id="8b512-138">The following code example makes the existing C:\\MyFolder directory a public file share.</span></span>


```C++
IADsFileShare *pShare = NULL;
IADsContainer *pCont = NULL;
LPWSTR adsPath = L"WinNT://yourMachineName/LanmanServer";
HRESULT hr = S_OK;

hr = ADsGetObject(adsPath, IID_IADsContainer,(void**)&pCont);
if(FAILED(hr)) {goto Cleanup;}

hr = pCont->Create(CComBSTR("FileShare"), CComBSTR("Public"), (IDispatch**)&pShare);

if(FAILED(hr)) {goto Cleanup;}

hr = pShare->put_Path(CComBSTR("c:\\public"));

if(FAILED(hr)) {goto Cleanup;}

hr = pShare->SetInfo();

Cleanup:
    if(pCont) pCont->Release();
    if(pShare) pShare->Release();
```



## <a name="requirements"></a><span data-ttu-id="8b512-139">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8b512-139">Requirements</span></span>



| <span data-ttu-id="8b512-140">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8b512-140">Requirement</span></span> | <span data-ttu-id="8b512-141">Wert</span><span class="sxs-lookup"><span data-stu-id="8b512-141">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8b512-142">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="8b512-142">Minimum supported client</span></span><br/> | <span data-ttu-id="8b512-143">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8b512-143">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="8b512-144">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="8b512-144">Minimum supported server</span></span><br/> | <span data-ttu-id="8b512-145">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8b512-145">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="8b512-146">Header</span><span class="sxs-lookup"><span data-stu-id="8b512-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="8b512-147"><dt>IADs. h</dt></span><span class="sxs-lookup"><span data-stu-id="8b512-147"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="8b512-148">DLL</span><span class="sxs-lookup"><span data-stu-id="8b512-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8b512-149"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8b512-149"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="8b512-150">IID</span><span class="sxs-lookup"><span data-stu-id="8b512-150">IID</span></span><br/>                      | <span data-ttu-id="8b512-151">IID \_ iadsfileshare ist als EB6DCAF0-4B83-11CF-A995-00AA006BC149 definiert.</span><span class="sxs-lookup"><span data-stu-id="8b512-151">IID\_IADsFileShare is defined as EB6DCAF0-4B83-11CF-A995-00AA006BC149</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="8b512-152">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8b512-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8b512-153">**Iadsservice**</span><span class="sxs-lookup"><span data-stu-id="8b512-153">**IADsService**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsservice)
</dt> <dt>

[<span data-ttu-id="8b512-154">**Iadsfileshare**</span><span class="sxs-lookup"><span data-stu-id="8b512-154">**IADsFileShare**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsfileshare)
</dt> <dt>

[<span data-ttu-id="8b512-155">Schnittstelleneigenschaften Methoden</span><span class="sxs-lookup"><span data-stu-id="8b512-155">Interface Property Methods</span></span>](interface-property-methods.md)
</dt> </dl>

 

 





