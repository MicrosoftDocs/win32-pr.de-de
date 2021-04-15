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
# <a name="ndf-helper-class-extension"></a>NDF-Hilfsklassen Erweiterung

In diesem Beispiel wird veranschaulicht, wie NDF-Diagnose-und Reparaturfunktionen implementiert werden. In diesem Beispiel muss eine wichtige Konfigurationsdatei vorhanden sein, damit das Systemfehler frei bleibt. Dementsprechend besteht das Problem darin, zu bestimmen, ob die Datei vorhanden ist. Wenn dies nicht der Fall ist, ist das Systemfehler Haft, und das Problem wird von der NDF diagnostiziert. Die Reparatur besteht darin, die fehlende Datei neu zu erstellen.

Um das Problem zu diagnostizieren und zu beheben, müssen Sie vier [**inetdiaghelper**](/windows/desktop/api/ndhelper/nn-ndhelper-inetdiaghelper) -Methoden verwenden: [**Initialize**](/windows/desktop/api/ndhelper/nf-ndhelper-inetdiaghelper-initialize), [**lowhealth**](/windows/desktop/api/ndhelper/nf-ndhelper-inetdiaghelper-lowhealth), [**getrepirren Info**](/windows/desktop/api/ndhelper/nf-ndhelper-inetdiaghelper-getrepairinfo)und [**Repair**](/windows/desktop/api/ndhelper/nf-ndhelper-inetdiaghelper-repair).

## <a name="initializing-the-helper-class"></a>Initialisieren der Hilfsklasse

Initialisieren Sie den Namen der zu suchenden Datei, und rufen Sie ihn ab. Der Dateiname wird während der Diagnose als hilfsattribut mit dem Namen "Dateiname" übermittelt.


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



## <a name="checking-on-the-files-existence"></a>Es wird geprüft, ob die Datei vorhanden ist.

Die [**lowhealth**](/windows/desktop/api/ndhelper/nf-ndhelper-inetdiaghelper-lowhealth) -Methode wird verwendet, um das vorhanden sein der Datei zu überprüfen. Wenn die Datei vorhanden ist, wird der Diagnose Status **auf \_ Abgelehnte DS** festgelegt, was darauf hinweist, dass nichts falsch ist. Wenn die Datei nicht gefunden werden kann, wird der Diagnose Status auf **DS \_ bestätigt** festgelegt.


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



## <a name="determining-the-repair-action"></a>Bestimmen der Reparaturaktion

Wenn [**lowhealth**](/windows/desktop/api/ndhelper/nf-ndhelper-inetdiaghelper-lowhealth) **DS \_ bestätigt** zurückgibt, wird [**getrepirren Info**](/windows/desktop/api/ndhelper/nf-ndhelper-inetdiaghelper-getrepairinfo) implementiert, um die entsprechende Reparaturaktion zu bestimmen. In diesem Beispiel bedeutet dies, dass die Datei neu erstellt wird.


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



## <a name="repairing-the-problem"></a>Beheben des Problems

Dem Benutzer werden die von [**getrepaarinfo**](/windows/desktop/api/ndhelper/nf-ndhelper-inetdiaghelper-getrepairinfo)zurückgegebenen Korrektur Optionen angezeigt, es sei denn, es gibt nur eine Reparaturoption. in diesem Fall wird er automatisch ausgeführt. Die [**Repair**](/windows/desktop/api/ndhelper/nf-ndhelper-inetdiaghelper-repair) -Methode wird mit der entsprechenden [**repairiinfo**](/windows/win32/api/ndattrib/ns-ndattrib-repairinfo) -Struktur aufgerufen, damit die Konfigurationsdatei wieder hergestellt werden kann.


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



 

 




