---
title: NDF-Hilfsklassen Erweiterung
description: In diesem Beispiel wird veranschaulicht, wie NDF-Diagnose-und Reparaturfunktionen implementiert werden.
ms.assetid: 18e66d09-e565-4b86-8bc3-600f2159a4bd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5b2a0dbcba29449b8f21850fa0669f8154dcbd7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104515428"
---
# <a name="ndf-helper-class-extension"></a><span data-ttu-id="7014d-103">NDF-Hilfsklassen Erweiterung</span><span class="sxs-lookup"><span data-stu-id="7014d-103">NDF Helper Class Extension</span></span>

<span data-ttu-id="7014d-104">In diesem Beispiel wird veranschaulicht, wie NDF-Diagnose-und Reparaturfunktionen implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="7014d-104">This example illustrates how to implement NDF diagnosis and repair functions.</span></span> <span data-ttu-id="7014d-105">In diesem Beispiel muss eine wichtige Konfigurationsdatei vorhanden sein, damit das Systemfehler frei bleibt.</span><span class="sxs-lookup"><span data-stu-id="7014d-105">In this example, a critical configuration file must exist for the system to remain healthy.</span></span> <span data-ttu-id="7014d-106">Dementsprechend besteht das Problem darin, zu bestimmen, ob die Datei vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="7014d-106">Accordingly, the problem is to determine whether the file exists.</span></span> <span data-ttu-id="7014d-107">Wenn dies nicht der Fall ist, ist das Systemfehler Haft, und das Problem wird von der NDF diagnostiziert.</span><span class="sxs-lookup"><span data-stu-id="7014d-107">If it does not, the system is unhealthy and the problem is diagnosed by NDF.</span></span> <span data-ttu-id="7014d-108">Die Reparatur besteht darin, die fehlende Datei neu zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="7014d-108">The repair is to re-create the missing file.</span></span>

<span data-ttu-id="7014d-109">Um das Problem zu diagnostizieren und zu beheben, müssen Sie vier [**inetdiaghelper**](/windows/desktop/api/ndhelper/nn-ndhelper-inetdiaghelper) -Methoden verwenden: [**Initialize**](/windows/desktop/api/ndhelper/nf-ndhelper-inetdiaghelper-initialize), [**lowhealth**](/windows/desktop/api/ndhelper/nf-ndhelper-inetdiaghelper-lowhealth), [**getrepirren Info**](/windows/desktop/api/ndhelper/nf-ndhelper-inetdiaghelper-getrepairinfo)und [**Repair**](/windows/desktop/api/ndhelper/nf-ndhelper-inetdiaghelper-repair).</span><span class="sxs-lookup"><span data-stu-id="7014d-109">To diagnose and repair the problem requires using four [**INetDiagHelper**](/windows/desktop/api/ndhelper/nn-ndhelper-inetdiaghelper) methods: [**Initialize**](/windows/desktop/api/ndhelper/nf-ndhelper-inetdiaghelper-initialize), [**LowHealth**](/windows/desktop/api/ndhelper/nf-ndhelper-inetdiaghelper-lowhealth), [**GetRepairInfo**](/windows/desktop/api/ndhelper/nf-ndhelper-inetdiaghelper-getrepairinfo), and [**Repair**](/windows/desktop/api/ndhelper/nf-ndhelper-inetdiaghelper-repair).</span></span>

## <a name="initializing-the-helper-class"></a><span data-ttu-id="7014d-110">Initialisieren der Hilfsklasse</span><span class="sxs-lookup"><span data-stu-id="7014d-110">Initializing the Helper Class</span></span>

<span data-ttu-id="7014d-111">Initialisieren Sie den Namen der zu suchenden Datei, und rufen Sie ihn ab.</span><span class="sxs-lookup"><span data-stu-id="7014d-111">Initialize and retrieve the name of the file to locate.</span></span> <span data-ttu-id="7014d-112">Der Dateiname wird während der Diagnose als hilfsattribut mit dem Namen "Dateiname" übermittelt.</span><span class="sxs-lookup"><span data-stu-id="7014d-112">This filename is passed during diagnosis as a helper attribute called "filename".</span></span>


```C++
#include <windows.h>
//utility function to simplify string allocation and copies, user throughout example
HRESULT 
StringCchCopyWithAlloc (
    PWSTR* Dest, 
    size_t cchMaxLen,
    in PCWSTR Src)
{
    if (NULL == Dest || NULL == Src || cchMaxLen > USHRT_MAX)
    {
        return E_INVALIDARG;
    }
    size_t cchSize = 0;

    HRESULT hr = StringCchLength(Src, cchMaxLen - 1, &cchSize); 
    if (FAILED(hr))
    {
        return hr;
    }

    size_t cbSize = (cchSize + 1)*sizeof(WCHAR);
    *Dest = (PWSTR) CoTaskMemAlloc(cbSize);
    if (NULL == *Dest)
    {
        return E_OUTOFMEMORY;
    }
    SecureZeroMemory(*Dest, cbSize);

    return StringCchCopy((STRSAFE_LPWSTR)*Dest, cchSize + 1, Src);    
}

HRESULT SimpleFileHelperClass::Initialize(
        /* [in] */ ULONG celt,
        /* [size_is][in] */ HELPER_ATTRIBUTE rgAttributes[  ])
{
    if(celt < 1)
    {
        return E_INVALIDARG;
    }
    if(rgAttributes == NULL)
    {
        return E_INVALIDARG; 
    }
    else
    {
        //verify the attribute is named as expected
        if (wcscmp(rgAttributes[0].pwszName, L"filename")==0)
        {
            //copy the attribute to member variable
            return StringCchCopyWithAlloc(&m_pwszTestFile, MAX_PATH, 
                    rgAttributes[0].PWStr);
        } else {
            //the attribute isn't named as expected
            return E_INVALIDARG;
        }
    }
}

```



## <a name="checking-on-the-files-existence"></a><span data-ttu-id="7014d-113">Es wird geprüft, ob die Datei vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="7014d-113">Checking on the File's Existence</span></span>

<span data-ttu-id="7014d-114">Die [**lowhealth**](/windows/desktop/api/ndhelper/nf-ndhelper-inetdiaghelper-lowhealth) -Methode wird verwendet, um das vorhanden sein der Datei zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="7014d-114">The [**LowHealth**](/windows/desktop/api/ndhelper/nf-ndhelper-inetdiaghelper-lowhealth) method is used to check on the existence of the file.</span></span> <span data-ttu-id="7014d-115">Wenn die Datei vorhanden ist, wird der Diagnose Status **auf \_ Abgelehnte DS** festgelegt, was darauf hinweist, dass nichts falsch ist.</span><span class="sxs-lookup"><span data-stu-id="7014d-115">If the file exists, diagnosis status is set to **DS\_REJECTED**, indicating nothing is wrong.</span></span> <span data-ttu-id="7014d-116">Wenn die Datei nicht gefunden werden kann, wird der Diagnose Status auf **DS \_ bestätigt** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="7014d-116">If the file cannot be found, the diagnosis status is set to **DS\_CONFIRMED**.</span></span>


```C++
#include <windows.h>

HRESULT SimpleFileHelperClass::LowHealth( 
            /* [unique][string][in] */ LPCWSTR pwszInstanceDescription,
            /* [string][out] */ LPWSTR *ppwszDescription,
            /* [out] */ long *pDeferredTime,
            /* [out] */ DIAGNOSIS_STATUS *pStatus) 

{
    HANDLE hFile = NULL;
    LPWSTR pwszDiagString=NULL;
    // does the file already exist?
    hFile = CreateFile(
        m_pwszTestFile, 
        GENERIC_READ, 
        0, 
        NULL, 
        OPEN_EXISTING, 
        FILE_ATTRIBUTE_NORMAL, 
        NULL);

    if(INVALID_HANDLE_VALUE == hFile)
    { 
        // alloc and set the diagnosis description and status
        HRESULT hr = StringCchCopyWithAlloc(&pwszDiagString, MAX_PATH, 
                    L"The file was deleted.");
        if (FAILED(hr))
        {
            return hr;
        }
  
        *ppwszDescription = pwszDiagString;
        *pStatus = DS_CONFIRMED;
        return S_OK;
    }
    CloseHandle(hFile); 
    
    //the file exists
    *pStatus = DS_REJECTED;
    return S_OK;
}
```



## <a name="determining-the-repair-action"></a><span data-ttu-id="7014d-117">Bestimmen der Reparaturaktion</span><span class="sxs-lookup"><span data-stu-id="7014d-117">Determining the Repair Action</span></span>

<span data-ttu-id="7014d-118">Wenn [**lowhealth**](/windows/desktop/api/ndhelper/nf-ndhelper-inetdiaghelper-lowhealth) **DS \_ bestätigt** zurückgibt, wird [**getrepirren Info**](/windows/desktop/api/ndhelper/nf-ndhelper-inetdiaghelper-getrepairinfo) implementiert, um die entsprechende Reparaturaktion zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="7014d-118">If [**LowHealth**](/windows/desktop/api/ndhelper/nf-ndhelper-inetdiaghelper-lowhealth) returns **DS\_CONFIRMED**, [**GetRepairInfo**](/windows/desktop/api/ndhelper/nf-ndhelper-inetdiaghelper-getrepairinfo) is implemented to determine the appropriate repair action.</span></span> <span data-ttu-id="7014d-119">In diesem Beispiel bedeutet dies, dass die Datei neu erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="7014d-119">In this example, that means re-creating the file.</span></span>


```C++
#include <windows.h>

HRESULT  
SimpleFileHelperClass::GetRepairInfo( 
            /* [in] */ PROBLEM_TYPE problem,
            /* [out] */ ULONG *pcelt,
            /* [size_is][size_is][out] */ RepairInfo **ppInfo)
{
    HRESULT hr=S_OK;
    RepairInfo* pRepair = (RepairInfo *)CoTaskMemAlloc(sizeof(RepairInfo));
    if (pRepair == NULL) {
        return E_OUTOFMEMORY;
    }
    SecureZeroMemory(pRepair,sizeof(RepairInfo));

    // set the repair description and class name
    hr = StringCchCopyWithAlloc(&pRepair->pwszClassName, MAX_PATH,
                L"SimpleFileHelperClass");
    if (FAILED(hr))
    {
        goto Error;
    }

    hr = StringCchCopyWithAlloc(&pRepair->pwszDescription, MAX_PATH, 
                L"Low Health Repair");
    if (FAILED(hr))
    {
        goto Error;
    }
  
    // set the resolution GUID and cost
    pRepair->guid = ID_LowHealthRepair;
    pRepair->cost = 0;
    // set repair status flags
    pRepair->sidType = WinWorldSid;
    pRepair->scope = RS_SYSTEM;
    pRepair->risk = RR_NORISK;
    pRepair->flags |= DF_IMPERSONATION; //impersonate the user when repairing
    pRepair->UiInfo.type = UIT_NONE;
    
    //pass back the repair
    *ppInfo = pRepair; 
    *pcelt = 1; //number of repairs

    return S_OK;

Error:
    if(pRepair){
        if(pRepair->pwszClassName){
            CoTaskMemFree(pRepair->pwszClassName);
        }
        if(pRepair->pwszDescription){
            CoTaskMemFree(pRepair->pwszDescription);
        }
    }
    return hr;
}

```



## <a name="repairing-the-problem"></a><span data-ttu-id="7014d-120">Beheben des Problems</span><span class="sxs-lookup"><span data-stu-id="7014d-120">Repairing the Problem</span></span>

<span data-ttu-id="7014d-121">Dem Benutzer werden die von [**getrepaarinfo**](/windows/desktop/api/ndhelper/nf-ndhelper-inetdiaghelper-getrepairinfo)zurückgegebenen Korrektur Optionen angezeigt, es sei denn, es gibt nur eine Reparaturoption. in diesem Fall wird er automatisch ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="7014d-121">The user is presented with the fix options returned by the [**GetRepairInfo**](/windows/desktop/api/ndhelper/nf-ndhelper-inetdiaghelper-getrepairinfo), unless there is only one repair option, in which case it is automatically executed.</span></span> <span data-ttu-id="7014d-122">Die [**Repair**](/windows/desktop/api/ndhelper/nf-ndhelper-inetdiaghelper-repair) -Methode wird mit der entsprechenden [**repairiinfo**](/windows/win32/api/ndattrib/ns-ndattrib-repairinfo) -Struktur aufgerufen, damit die Konfigurationsdatei wieder hergestellt werden kann.</span><span class="sxs-lookup"><span data-stu-id="7014d-122">The [**Repair**](/windows/desktop/api/ndhelper/nf-ndhelper-inetdiaghelper-repair) method is called with the applicable [**RepairInfo**](/windows/win32/api/ndattrib/ns-ndattrib-repairinfo) structure so the configuration file can be restored.</span></span>


```C++
#include <windows.h>

HRESULT  
SimpleFileHelperClass::Repair( 
            /* [in] */ RepairInfo *pInfo,
            /* [out] */ long *pDeferredTime,
            /* [out] */ REPAIR_STATUS *pStatus)
{
    //verify expected repair was requested
    if(IsEqualGUID(ID_LowHealthRepair, pInfo->guid)){
        HANDLE hFile = NULL;
        hFile = CreateFile(m_pwszTestFile, 
                                GENERIC_WRITE, 
                                0, 
                                NULL, 
                                CREATE_ALWAYS,
                                FILE_ATTRIBUTE_NORMAL, 
                                NULL);
        if(INVALID_HANDLE_VALUE == hFile)
        {
            // repair failed
            *pStatus = RS_UNREPAIRED;
            return HRESULT_FROM_WIN32(GetLastError());
        }
        CloseHandle(hFile);
        
        // repair succeeded
        *pStatus = RS_REPAIRED;
    } else {
        return E_INVALIDARG; //unkown repair passed in
    }
    return S_OK;
}
```



 

 




