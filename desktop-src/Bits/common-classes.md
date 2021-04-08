---
title: Allgemeine Beispiel Klassen
description: Sie können die Codebeispiele in diesem Thema als Ausgangspunkt für viele Background Intelligent Transfer Service (Bits)-Anwendungen verwenden, die COM-Initialisierung ausführen, Fehlerbehandlung und Rückruf Benachrichtigungen erhalten.
ms.assetid: 8fe722a3-fbab-4843-b298-1ea11f54d7a5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 864fe4aa8d7af5bb6a248364b0e2c636e1c250a6
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/04/2020
ms.locfileid: "103734848"
---
# <a name="example-common-classes"></a><span data-ttu-id="d92dc-103">Beispiel: allgemeine Klassen</span><span class="sxs-lookup"><span data-stu-id="d92dc-103">Example: Common Classes</span></span>

<span data-ttu-id="d92dc-104">Sie können die Codebeispiele in diesem Thema als Ausgangspunkt für viele Background Intelligent Transfer Service (Bits)-Anwendungen verwenden, die COM-Initialisierung ausführen, Fehlerbehandlung und Rückruf Benachrichtigungen erhalten.</span><span class="sxs-lookup"><span data-stu-id="d92dc-104">You can use the code examples in this topic as a starting point for many Background Intelligent Transfer Service (BITS) applications that perform COM initialization, need error handling, and receive callback notifications.</span></span>


<span data-ttu-id="d92dc-105">Im folgenden Codebeispiel wird eine Ausnahme Klasse zum Behandeln von Fehlern definiert.</span><span class="sxs-lookup"><span data-stu-id="d92dc-105">The following code example defines an exception class to handle errors.</span></span>


```C++
class MyException
{
public:
    MyException(HRESULT hr, LPWSTR message):Error(hr), Message(message)
    {

    }
    HRESULT Error;
    std::wstring Message;
};
```



<span data-ttu-id="d92dc-106">Die myException-Klasse ist eine generische Ausnahme Klasse, die einen HRESULT-Code und eine Fehler Zeichenfolge akzeptiert.</span><span class="sxs-lookup"><span data-stu-id="d92dc-106">The MyException class is a generic exception class that accepts an HRESULT code and error string.</span></span>


<span data-ttu-id="d92dc-107">Im folgenden Codebeispiel wird eine ressourcenerwerbs-Hilfsklasse für die [CoInitializeEx](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) -Funktion definiert.</span><span class="sxs-lookup"><span data-stu-id="d92dc-107">The following code example defines a resource acquisition helper class for the [CoInitializeEx](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) function.</span></span>


```C++
class CCoInitializer 
{
public:
    CCoInitializer( DWORD dwCoInit ) 
    { 
        HRESULT hr = CoInitializeEx( NULL, dwCoInit );
        if (FAILED(hr))
        {
            throw MyException(hr,L"CoInitialize");
        }
    } 

    ~CCoInitializer() throw() 
    { 
        CoUninitialize(); 
    } 
};
```



<span data-ttu-id="d92dc-108">Die ccoinitializer-Klasse behandelt die Zuordnung und Aufhebung der Zuordnung von Ressourcen für die COM-Initialisierung.</span><span class="sxs-lookup"><span data-stu-id="d92dc-108">The CCoInitializer class deals with resource allocation and deallocation for COM initialization.</span></span> <span data-ttu-id="d92dc-109">Mit dieser Klasse kann der Dekonstruktor aufgerufen werden, wenn die Klasse den Gültigkeitsbereich verlässt.</span><span class="sxs-lookup"><span data-stu-id="d92dc-109">This class enables the destructor to be called when the class goes out of scope.</span></span> <span data-ttu-id="d92dc-110">Diese Klasse entfällt, dass die Methode " [count Initialize](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize) " nach jedem Ausnahme Block aufgerufen werden muss.</span><span class="sxs-lookup"><span data-stu-id="d92dc-110">This class eliminates the need for the [CoUninitialize](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize) method to be called after every exception block.</span></span>


<span data-ttu-id="d92dc-111">Das folgende Codebeispiel ist die Deklaration der cnotifyinterface-Rückruf Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="d92dc-111">The following code example is the declaration of the CNotifyInterface callback interface.</span></span>


```C++
// Implementation of the Callback interface
//
class CNotifyInterface : public IBackgroundCopyCallback
{
    LONG m_lRefCount;

public:
    //Constructor
    CNotifyInterface() {m_lRefCount = 1;};

//Destructor
    ~CNotifyInterface() {};

    //IUnknown methods
    HRESULT __stdcall QueryInterface(REFIID riid, LPVOID *ppvObj);
    ULONG __stdcall AddRef();
    ULONG __stdcall Release();

    //IBackgroundCopyCallback methods
    HRESULT __stdcall JobTransferred(IBackgroundCopyJob* pJob);
    HRESULT __stdcall JobError(IBackgroundCopyJob* pJob, IBackgroundCopyError* pError);
    HRESULT __stdcall JobModification(IBackgroundCopyJob* pJob, DWORD dwReserved);

private:
    CNotifyInterface(const CNotifyInterface&);
    CNotifyInterface& operator=(const CNotifyInterface&);
};
```



<span data-ttu-id="d92dc-112">Die cnotifyinterface-Klasse, die von der [**ibackgroundcopycallback**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopycallback) -Schnittstelle abgeleitet ist.</span><span class="sxs-lookup"><span data-stu-id="d92dc-112">The CNotifyInterface class derived from the [**IBackgroundCopyCallback**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopycallback) interface.</span></span> <span data-ttu-id="d92dc-113">Die cnotifyinterface-Klasse implementiert die IUnknown-Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="d92dc-113">The CNotifyInterface class implements the IUnknown interface.</span></span> <span data-ttu-id="d92dc-114">Weitere Informationen finden Sie unter [IUnknown]( /windows/win32/api/unknwn/nn-unknwn-iunknown).</span><span class="sxs-lookup"><span data-stu-id="d92dc-114">For more information, see [IUnknown]( /windows/win32/api/unknwn/nn-unknwn-iunknown).</span></span>

<span data-ttu-id="d92dc-115">Cnotifyinterface verwendet die folgenden Methoden, um die Benachrichtigung zu empfangen, dass ein Auftrag abgeschlossen ist, geändert wurde oder sich in einem Fehlerzustand befindet: [**jobübertragenen**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopycallback-jobtransferred), [**jobmodified**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopycallback-jobmodification)und [**joberror**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopycallback-joberror).</span><span class="sxs-lookup"><span data-stu-id="d92dc-115">CNotifyInterface uses the following methods to receive notification that a job is complete, has been modified, or is in an error state: [**JobTransferred**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopycallback-jobtransferred), [**JobModification**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopycallback-jobmodification), and [**JobError**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopycallback-joberror).</span></span> <span data-ttu-id="d92dc-116">Alle diese Methoden nehmen ein [**ibackgroundcopyjob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) -Auftrags Objekt an.</span><span class="sxs-lookup"><span data-stu-id="d92dc-116">All of these methods take an [**IBackgroundCopyJob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) job object.</span></span>

<span data-ttu-id="d92dc-117">In diesem Beispiel wird die [CoTaskMemFree](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) verwendet, um Speicherressourcen freizugeben.</span><span class="sxs-lookup"><span data-stu-id="d92dc-117">This example uses the [CoTaskMemFree](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) to free memory resources.</span></span>


<span data-ttu-id="d92dc-118">Das folgende Codebeispiel ist die Implementierung der [**ibackgroundcopycallback**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopycallback) -Rückruf Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="d92dc-118">The following code example is the implementation of the [**IBackgroundCopyCallback**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopycallback) callback interface.</span></span>


```C++
HRESULT CNotifyInterface::QueryInterface(REFIID riid, LPVOID* ppvObj) 
{
    if (riid == __uuidof(IUnknown) || riid == __uuidof(IBackgroundCopyCallback)) 
    {
        *ppvObj = this;
    }
    else
    {
        *ppvObj = NULL; 
        return E_NOINTERFACE;
    }

    AddRef();
    return NOERROR;
}

ULONG CNotifyInterface::AddRef() 
{
    return InterlockedIncrement(&m_lRefCount);
}

ULONG CNotifyInterface::Release() 
{
    // not thread safe
    ULONG  ulCount = InterlockedDecrement(&m_lRefCount);

    if(0 == ulCount) 
    {
        delete this;
    }

    return ulCount;
}

HRESULT CNotifyInterface::JobTransferred(IBackgroundCopyJob* pJob)
{
    HRESULT hr;

    wprintf(L"Job transferred. Completing Job...\n");
    hr = pJob->Complete();
    if (FAILED(hr))
    {
        //BITS probably was unable to rename one or more of the 
        //temporary files. See the Remarks section of the IBackgroundCopyJob::Complete 
        //method for more details.
        wprintf(L"Job Completion Failed with error %x\n", hr);
    }

    PostQuitMessage(0);

    //If you do not return S_OK, BITS continues to call this callback.
    return S_OK;
}

HRESULT CNotifyInterface::JobModification(IBackgroundCopyJob* pJob, DWORD dwReserved)
{
    return S_OK;
}

HRESULT CNotifyInterface::JobError(IBackgroundCopyJob* pJob, IBackgroundCopyError* pError)
{
    WCHAR* pszJobName = NULL;
    WCHAR* pszErrorDescription = NULL;

    //Use pJob and pError to retrieve information of interest. For example,
    //if the job is an upload reply, call the IBackgroundCopyError::GetError method 
    //to determine the context in which the job failed. 

    wprintf(L"Job entered error state...\n");
    HRESULT hr = pJob->GetDisplayName(&pszJobName);
    if (FAILED(hr))
    {
        wprintf(L"Unable to get job name\n");
    }

    hr = pError->GetErrorDescription(GetUserDefaultUILanguage(), &pszErrorDescription);
    if (FAILED(hr))
    {
        wprintf(L"Unable to get error description\n");
    }
    if (pszJobName && pszErrorDescription)
    {
        wprintf(L"Job %s ",pszJobName);
        wprintf(L"encountered the following error:\n");
        wprintf(L"%s\n",pszErrorDescription);
    }
    
    // Clean up
    CoTaskMemFree(pszJobName);
    CoTaskMemFree(pszErrorDescription);

    PostQuitMessage(hr);

    //If you do not return S_OK, BITS continues to call this callback.
    return S_OK;
}
```




<span data-ttu-id="d92dc-119">Die folgende Header Datei wird für die allgemeinen Code Klassen verwendet.</span><span class="sxs-lookup"><span data-stu-id="d92dc-119">The following header file is used for the common code classes.</span></span> <span data-ttu-id="d92dc-120">Diese Klassen werden in den vorherigen Codebeispielen verwendet.</span><span class="sxs-lookup"><span data-stu-id="d92dc-120">These classes are used in the previous code examples.</span></span>


```C++
// commoncode.h
#pragma once

//
// Exception class used for error handling
//
class MyException
{
public:
    MyException(HRESULT hr, LPWSTR message):Error(hr), Message(message)
    {

    }
    HRESULT Error;
    std::wstring Message;
};

// CoInitialize helper class
class CCoInitializer 
{
public:
    CCoInitializer( DWORD dwCoInit ) 
    { 
        HRESULT hr = CoInitializeEx( NULL, dwCoInit );
        if (FAILED(hr))
        {
            throw MyException(hr,L"CoInitialize");
        }
    } 

    ~CCoInitializer() throw() 
    { 
        CoUninitialize(); 
    } 
};

//
// Implementation of the Callback interface
//
class CNotifyInterface : public IBackgroundCopyCallback
{
    LONG m_lRefCount;

public:
    //Constructor, Destructor
    CNotifyInterface() {m_lRefCount = 1;};
    ~CNotifyInterface() {};

    //IUnknown
    HRESULT __stdcall QueryInterface(REFIID riid, LPVOID *ppvObj);
    ULONG __stdcall AddRef();
    ULONG __stdcall Release();

    //IBackgroundCopyCallback2 methods
    HRESULT __stdcall JobTransferred(IBackgroundCopyJob* pJob);
    HRESULT __stdcall JobError(IBackgroundCopyJob* pJob, IBackgroundCopyError* pError);
    HRESULT __stdcall JobModification(IBackgroundCopyJob* pJob, DWORD dwReserved);
private:
    CNotifyInterface(const CNotifyInterface&);
    CNotifyInterface& operator=(const CNotifyInterface&);
};
```




<span data-ttu-id="d92dc-121">Der folgende Beispielcode ist die Implementierung der allgemeinen Code Klassen.</span><span class="sxs-lookup"><span data-stu-id="d92dc-121">The following example code is the implementation of the common code classes.</span></span>


```C++
//commoncode.cpp

#include <bits.h>
#include <bits4_0.h>
#include <stdio.h>
#include <tchar.h>
#include <lm.h>
#include <iostream>
#include <exception>
#include <string>
#include <atlbase.h>
#include <memory>
#include <new>
#include "CommonCode.h"

HRESULT CNotifyInterface::QueryInterface(REFIID riid, LPVOID* ppvObj) 
{
    if (riid == __uuidof(IUnknown) || riid == __uuidof(IBackgroundCopyCallback)) 
    {
        *ppvObj = this;
    }
    else
    {
        *ppvObj = NULL; 
        return E_NOINTERFACE;
    }

    AddRef();
    return NOERROR;
}

ULONG CNotifyInterface::AddRef() 
{
    return InterlockedIncrement(&m_lRefCount);
}

ULONG CNotifyInterface::Release() 
{
    // not thread safe
    ULONG  ulCount = InterlockedDecrement(&m_lRefCount);

    if(0 == ulCount) 
    {
        delete this;
    }

    return ulCount;
}

HRESULT CNotifyInterface::JobTransferred(IBackgroundCopyJob* pJob)
{
    HRESULT hr;

    wprintf(L"Job transferred. Completing Job...\n");
    hr = pJob->Complete();
    if (FAILED(hr))
    {
        //BITS probably was unable to rename one or more of the 
        //temporary files. See the Remarks section of the IBackgroundCopyJob::Complete 
        //method for more details.
        wprintf(L"Job Completion Failed with error %x\n", hr);
    }

    PostQuitMessage(0);

    //If you do not return S_OK, BITS continues to call this callback.
    return S_OK;
}

HRESULT CNotifyInterface::JobModification(IBackgroundCopyJob* pJob, DWORD dwReserved)
{
    return S_OK;
}

HRESULT CNotifyInterface::JobError(IBackgroundCopyJob* pJob, IBackgroundCopyError* pError)
{
    WCHAR* pszJobName = NULL;
    WCHAR* pszErrorDescription = NULL;

    //Use pJob and pError to retrieve information of interest. For example,
    //if the job is an upload reply, call the IBackgroundCopyError::GetError method 
    //to determine the context in which the job failed.

    wprintf(L"Job entered error state...\n");
    HRESULT hr = pJob->GetDisplayName(&pszJobName);
    if (FAILED(hr))
    {
        wprintf(L"Unable to get job name\n");
    }

    hr = pError->GetErrorDescription(GetUserDefaultUILanguage(), &pszErrorDescription);
    if (FAILED(hr))
    {
        wprintf(L"Unable to get error description\n");
    }
    if (pszJobName && pszErrorDescription)
    {
        wprintf(L"Job %s ",pszJobName);
        wprintf(L"encountered the following error:\n");
        wprintf(L"%s\n",pszErrorDescription);
    }

    CoTaskMemFree(pszJobName);
    CoTaskMemFree(pszErrorDescription);

    PostQuitMessage(hr);

    //If you do not return S_OK, BITS continues to call this callback.
    return S_OK;
}
```



## <a name="related-topics"></a><span data-ttu-id="d92dc-122">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="d92dc-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d92dc-123">IUnknown</span><span class="sxs-lookup"><span data-stu-id="d92dc-123">IUnknown</span></span>]( /windows/win32/api/unknwn/nn-unknwn-iunknown)
</dt> <dt>

[<span data-ttu-id="d92dc-124">**Ibackgroundcopycallback**</span><span class="sxs-lookup"><span data-stu-id="d92dc-124">**IBackgroundCopyCallback**</span></span>](/windows/desktop/api/Bits/nn-bits-ibackgroundcopycallback)
</dt> <dt>

[<span data-ttu-id="d92dc-125">**IBackgroundCopyJob**</span><span class="sxs-lookup"><span data-stu-id="d92dc-125">**IBackgroundCopyJob**</span></span>](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob)
</dt> <dt>

[<span data-ttu-id="d92dc-126">CoInitializeEx</span><span class="sxs-lookup"><span data-stu-id="d92dc-126">CoInitializeEx</span></span>](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex)
</dt> <dt>

[<span data-ttu-id="d92dc-127">CoUninitialize</span><span class="sxs-lookup"><span data-stu-id="d92dc-127">CoUninitialize</span></span>](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize)
</dt> </dl>

 

 