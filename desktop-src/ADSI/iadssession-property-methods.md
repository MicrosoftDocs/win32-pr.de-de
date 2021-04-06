---
title: Iadssession-Eigenschaften Methoden (IADs. h)
description: Mit den Eigenschafts Methoden der iadssession-Schnittstelle werden die in der folgenden Tabelle beschriebenen Eigenschaften angezeigt oder festgelegt. Weitere Informationen und eine allgemeine Erörterung von Eigenschaften Methoden finden Sie unter Interface Property Methods.
ms.assetid: b2366da7-c51c-4279-8931-2000d3110d72
ms.tgt_platform: multiple
keywords:
- Iadssession-Eigenschaften Methoden ADSI
topic_type:
- apiref
api_name:
- IADsSession Property Methods
- IADsSession.Computer
- IADsSession.get_Computer
- IADsSession.ComputerPath
- IADsSession.get_ComputerPath
- IADsSession.ConnectTime
- IADsSession.get_ConnectTime
- IADsSession.IdleTime
- IADsSession.get_IdleTime
- IADsSession.User
- IADsSession.get_User
- IADsSession.UserPath
- IADsSession.get_UserPath
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2cf7dd9abe25d731ba63385cd8d632c4212ea349
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103858828"
---
# <a name="iadssession-property-methods"></a><span data-ttu-id="55b15-105">Iadssession-Eigenschaften Methoden</span><span class="sxs-lookup"><span data-stu-id="55b15-105">IADsSession Property Methods</span></span>

<span data-ttu-id="55b15-106">Mit den Eigenschafts Methoden der [**iadssession**](/windows/desktop/api/Iads/nn-iads-iadssession) -Schnittstelle werden die in der folgenden Tabelle beschriebenen Eigenschaften angezeigt oder festgelegt.</span><span class="sxs-lookup"><span data-stu-id="55b15-106">The property methods of the [**IADsSession**](/windows/desktop/api/Iads/nn-iads-iadssession) interface get or set the properties described in the following table.</span></span> <span data-ttu-id="55b15-107">Weitere Informationen und eine allgemeine Erörterung von Eigenschaften Methoden finden Sie unter [Interface Property Methods](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="55b15-107">For more information and a general discussion about property methods, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="55b15-108">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="55b15-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="55b15-109">**Computer**</span><span class="sxs-lookup"><span data-stu-id="55b15-109">**Computer**</span></span>
<span data-ttu-id="55b15-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="55b15-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="55b15-111">Der Name der Client Arbeitsstation.</span><span class="sxs-lookup"><span data-stu-id="55b15-111">Name of the client workstation.</span></span>

<dt>

<span data-ttu-id="55b15-112">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="55b15-112">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="55b15-113">Skript Datentyp: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="55b15-113">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Computer(
  [out] BSTR* pbstrComputer
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="55b15-114">**Computer Pfad**</span><span class="sxs-lookup"><span data-stu-id="55b15-114">**ComputerPath**</span></span>
<span data-ttu-id="55b15-115"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="55b15-115"></dt> <dd> <dl></span></span>

<span data-ttu-id="55b15-116">Der ADsPath des Computer Objekts für die Client Arbeitsstation.</span><span class="sxs-lookup"><span data-stu-id="55b15-116">ADsPath of the computer object for the client workstation.</span></span>

<dt>

<span data-ttu-id="55b15-117">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="55b15-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="55b15-118">Skript Datentyp: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="55b15-118">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_ComputerPath(
  [out] BSTR* pbstrComputerPath
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="55b15-119">**Connecttime**</span><span class="sxs-lookup"><span data-stu-id="55b15-119">**ConnectTime**</span></span>
<span data-ttu-id="55b15-120"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="55b15-120"></dt> <dd> <dl></span></span>

<span data-ttu-id="55b15-121">Verstrichene Zeit (in Sekunden) seit dem Start der Sitzung.</span><span class="sxs-lookup"><span data-stu-id="55b15-121">Elapsed time, in seconds, since the session started.</span></span>

<dt>

<span data-ttu-id="55b15-122">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="55b15-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="55b15-123">Skript Datentyp: **Long**</span><span class="sxs-lookup"><span data-stu-id="55b15-123">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_ConnectTime(
  [out] LONG* plConnectTime
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="55b15-124">**IdleTime**</span><span class="sxs-lookup"><span data-stu-id="55b15-124">**IdleTime**</span></span>
<span data-ttu-id="55b15-125"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="55b15-125"></dt> <dd> <dl></span></span>

<span data-ttu-id="55b15-126">Leerlaufzeit (in Sekunden) der Sitzung.</span><span class="sxs-lookup"><span data-stu-id="55b15-126">Idle time, in seconds, of the session.</span></span>

<dt>

<span data-ttu-id="55b15-127">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="55b15-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="55b15-128">Skript Datentyp: **Long**</span><span class="sxs-lookup"><span data-stu-id="55b15-128">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_IdleTime(
  [out] LONG* plIdleTime
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="55b15-129">**Benutzer**</span><span class="sxs-lookup"><span data-stu-id="55b15-129">**User**</span></span>
<span data-ttu-id="55b15-130"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="55b15-130"></dt> <dd> <dl></span></span>

<span data-ttu-id="55b15-131">Der Name des Benutzers der Sitzung.</span><span class="sxs-lookup"><span data-stu-id="55b15-131">The name of the user of the session.</span></span>

<dt>

<span data-ttu-id="55b15-132">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="55b15-132">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="55b15-133">Skript Datentyp: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="55b15-133">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_User(
  [out] BSTR* pbstrUser
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="55b15-134">**UserPath**</span><span class="sxs-lookup"><span data-stu-id="55b15-134">**UserPath**</span></span>
<span data-ttu-id="55b15-135"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="55b15-135"></dt> <dd> <dl></span></span>

<span data-ttu-id="55b15-136">Der ADsPath des Benutzer Objekts für den Benutzer dieser Sitzung.</span><span class="sxs-lookup"><span data-stu-id="55b15-136">The ADsPath of the user object for the user of this session.</span></span>

<dt>

<span data-ttu-id="55b15-137">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="55b15-137">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="55b15-138">Skript Datentyp: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="55b15-138">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_UserPath(
  [out] BSTR* pbstrUserPath
);
```


</dt> </dl> </dd> </dl>

 

## <a name="examples"></a><span data-ttu-id="55b15-139">Beispiele</span><span class="sxs-lookup"><span data-stu-id="55b15-139">Examples</span></span>

<span data-ttu-id="55b15-140">Im folgenden Codebeispiel wird gezeigt, wie Sie Sitzungen für einen Datei Dienst überprüfen.</span><span class="sxs-lookup"><span data-stu-id="55b15-140">The following code example shows how to examine sessions for a file service.</span></span>


```VB
Dim fso As IADsFileServiceOperations
On Error GoTo Cleanup

' Bind to a file service operations object on "myComputer" in the local domain.
Set fso = GetObject("WinNT://myComputer/LanmanServer")

' Enumerate sessions.
If (IsEmpty(fso) = False) Then
    For Each session In fso.sessions
        MsgBox "Session Computer: " & session.Computer
        MsgBox "Session User: " & session.User
    Next Session
End If

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set fso = Nothing
```



<span data-ttu-id="55b15-141">Im folgenden Codebeispiel wird eine Auflistung von Sitzungen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="55b15-141">The following code example enumerates a collection of sessions.</span></span>


```C++
IADsFileServiceOperations *pFso = NULL;
IADsSession *pSes = NULL;
IADsCollection *pColl = NULL;
HRESULT hr = S_OK;
IUnknown *pUnk = NULL;
BSTR bstr = NULL;
VARIANT var;
ULONG lFetch = 0;
IDispatch *pDisp = NULL;
IEnumVARIANT *pEnum = NULL;

VariantInit(&var);

LPWSTR adsPath = L"WinNT://aMachine/LanmanServer";

hr = ADsGetObject(adsPath,IID_IADsFileServiceOperations,
                  (void**)&pFso);

if(FAILED(hr)) {goto Cleanup;}

hr = pFso->Sessions(&pColl);

// Enumerate sessions. 
hr = pColl->get__NewEnum(&pUnk);
if(FAILED(hr)) {goto Cleanup;}

hr = pUnk->QueryInterface(IID_IEnumVARIANT,(void**)&pEnum);
if(FAILED(hr)) {goto Cleanup;}

// Enumerate.
hr = pEnum->Next(1, &var, &lFetch);
while(hr == S_OK)
{
    if (lFetch == 1)    
    {
        pDisp = V_DISPATCH(&var);
        pDisp->QueryInterface(IID_IADsSession, (void**)&pSes);
        pSes->get_Computer(&bstr);
        printf("Session host: %S\n",bstr);
        SysFreeString(bstr);

        pSes->get_User(&bstr);
        printf("Session user: %S\n",bstr);
        SysFreeString(bstr);

        pRes->Release();
    }

    VariantClear(&var);
    pDisp=NULL;
    hr = pEnum->Next(1, &var, &lFetch);
};

Cleanup:
    if(pFso) pFso->Release();
    if(pColl) pColl->Release();
    if(pUnk) pUnk->Release();
    if(pEnum) pEnum->Release();
```



## <a name="requirements"></a><span data-ttu-id="55b15-142">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="55b15-142">Requirements</span></span>



| <span data-ttu-id="55b15-143">Anforderung</span><span class="sxs-lookup"><span data-stu-id="55b15-143">Requirement</span></span> | <span data-ttu-id="55b15-144">Wert</span><span class="sxs-lookup"><span data-stu-id="55b15-144">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="55b15-145">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="55b15-145">Minimum supported client</span></span><br/> | <span data-ttu-id="55b15-146">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="55b15-146">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="55b15-147">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="55b15-147">Minimum supported server</span></span><br/> | <span data-ttu-id="55b15-148">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="55b15-148">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="55b15-149">Header</span><span class="sxs-lookup"><span data-stu-id="55b15-149">Header</span></span><br/>                   | <dl> <span data-ttu-id="55b15-150"><dt>IADs. h</dt></span><span class="sxs-lookup"><span data-stu-id="55b15-150"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="55b15-151">DLL</span><span class="sxs-lookup"><span data-stu-id="55b15-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="55b15-152"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="55b15-152"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="55b15-153">IID</span><span class="sxs-lookup"><span data-stu-id="55b15-153">IID</span></span><br/>                      | <span data-ttu-id="55b15-154">IID \_ iadssession ist als 398b7da0-4aab-11CF-ae2c-00aa006ebfb9 definiert.</span><span class="sxs-lookup"><span data-stu-id="55b15-154">IID\_IADsSession is defined as 398B7DA0-4AAB-11CF-AE2C-00AA006EBFB9</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="55b15-155">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="55b15-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="55b15-156">**Iadsfileserviceoperations:: Sessions**</span><span class="sxs-lookup"><span data-stu-id="55b15-156">**IADsFileServiceOperations::Sessions**</span></span>](/windows/desktop/api/Iads/nf-iads-iadsfileserviceoperations-sessions)
</dt> <dt>

[<span data-ttu-id="55b15-157">**Iadssession**</span><span class="sxs-lookup"><span data-stu-id="55b15-157">**IADsSession**</span></span>](/windows/desktop/api/Iads/nn-iads-iadssession)
</dt> </dl>

 

 





