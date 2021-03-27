---
description: Die ihweventhandler-Schnittstelle kann in der Running Object Table (rot) registriert werden, damit die Ausführung von Anwendungen auf AutoPlay-Ereignisse zugreifen kann.
ms.assetid: 6FEFFB5D-DD8B-4FEA-B273-D32FC30CAFEA
title: Verwenden von AutoPlay-Ereignissen in laufenden Anwendungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 51795a3992bdb40dde833bb3e352905efaa2be63
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959686"
---
# <a name="how-to-use-autoplay-events-in-running-applications"></a><span data-ttu-id="5005f-103">Verwenden von AutoPlay-Ereignissen in laufenden Anwendungen</span><span class="sxs-lookup"><span data-stu-id="5005f-103">How to Use AutoPlay Events in Running Applications</span></span>

<span data-ttu-id="5005f-104">Die [**ihweventhandler**](/windows/desktop/api/Shobjidl/nn-shobjidl-ihweventhandler) -Schnittstelle kann in der Running Object Table (rot) registriert werden, damit die Ausführung von Anwendungen auf AutoPlay-Ereignisse zugreifen kann.</span><span class="sxs-lookup"><span data-stu-id="5005f-104">The [**IHWEventHandler**](/windows/desktop/api/Shobjidl/nn-shobjidl-ihweventhandler) interface can be registered in the running object table (ROT) so that running applications have access to AutoPlay events.</span></span>

<span data-ttu-id="5005f-105">In den folgenden Anweisungen wird beschrieben, wie Sie Autoplay-Ereignisse in Ausführung von-Anwendungen verwenden.</span><span class="sxs-lookup"><span data-stu-id="5005f-105">The following instructions describe how to use AutoPlay events in running applications.</span></span>

## <a name="instructions"></a><span data-ttu-id="5005f-106">Instructions</span><span class="sxs-lookup"><span data-stu-id="5005f-106">Instructions</span></span>

### <a name="step-1"></a><span data-ttu-id="5005f-107">Schritt 1:</span><span class="sxs-lookup"><span data-stu-id="5005f-107">Step 1:</span></span>

<span data-ttu-id="5005f-108">Erstellen Sie eine neue-Komponente, die die [**ihweventhandler**](/windows/desktop/api/Shobjidl/nn-shobjidl-ihweventhandler) -Schnittstelle implementiert.</span><span class="sxs-lookup"><span data-stu-id="5005f-108">Create a new component that implements the [**IHWEventHandler**](/windows/desktop/api/Shobjidl/nn-shobjidl-ihweventhandler) interface.</span></span>

### <a name="step-2"></a><span data-ttu-id="5005f-109">Schritt 2:</span><span class="sxs-lookup"><span data-stu-id="5005f-109">Step 2:</span></span>

<span data-ttu-id="5005f-110">Initialisieren Sie die neue Komponente mit dem initcmdline-Wert aus dem Eintrag eines bestimmten **Handlers** unter dem Handler-Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="5005f-110">Initialize the new component with the InitCmdLine value from the particular handler's entry under the **Handlers** key.</span></span>

<span data-ttu-id="5005f-111">Dieser Schritt ist erforderlich, da die Methode "Initialize" nicht von der automatischen Wiedergabe aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="5005f-111">This step is required because Autoplay does not call the Initialize method.</span></span>

### <a name="step-3"></a><span data-ttu-id="5005f-112">Schritt 3:</span><span class="sxs-lookup"><span data-stu-id="5005f-112">Step 3:</span></span>

<span data-ttu-id="5005f-113">Aufrufen der Funktion " [**reatehardwareeventmoniker**](createhardwareeventmoniker.md) ", um einen Moniker zu erhalten, der die Komponente und den Ereignishandler darstellt, den Sie aufrufen möchten.</span><span class="sxs-lookup"><span data-stu-id="5005f-113">Call the [**CreateHardwareEventMoniker**](createhardwareeventmoniker.md) function to get a moniker that represents your component and the event handler that you want to call.</span></span>

### <a name="step-4"></a><span data-ttu-id="5005f-114">Schritt 4:</span><span class="sxs-lookup"><span data-stu-id="5005f-114">Step 4:</span></span>

<span data-ttu-id="5005f-115">Verwenden Sie den *ppmoniker* -Parameter, um die Komponente in der rot zu registrieren.</span><span class="sxs-lookup"><span data-stu-id="5005f-115">Use the *ppmoniker* parameter to register your component in the ROT.</span></span>

## <a name="remarks"></a><span data-ttu-id="5005f-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5005f-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="5005f-117">[**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) kann Sicherheitsrisiken darstellen.</span><span class="sxs-lookup"><span data-stu-id="5005f-117">[**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) can pose security risks.</span></span> <span data-ttu-id="5005f-118">Informationen zum ordnungsgemäßen Laden von DLLs mit unterschiedlichen Versionen von Windows finden Sie in der Dokumentation zu **LoadLibrary** .</span><span class="sxs-lookup"><span data-stu-id="5005f-118">Refer to the **LoadLibrary** documentation for information on how to correctly load DLLs with different versions of Windows.</span></span>

```cpp
typedef HRESULT (*CREATEHARDWAREEVENTMONIKER)(REFCLSID clsid, LPCWSTR pszEventHandler, IMoniker **ppmoniker);

HRESULT RegisterComponent(IUnknown* punk, DWORD* dpwToken)
{
    HRESULT hr = E_FAIL;
    HINSTANCE hinstShSvcs = LoadLibrary(TEXT("shsvcs.dll"));
    
    if (hinstShSvcs)
    {   
        CREATEHARDWAREEVENTMONIKER fct = (CREATEHARDWAREEVENTMONIKER)GetProcAddress(hinstShSvcs, "CreateHardwareEventMoniker");
        if (fct)
        {
            IMoniker* pmoniker;
            
            hr = fct(CLSID_App, TEXT("VideoCameraArrival"), &pmoniker);

            if (SUCCEEDED(hr))
            {
                IRunningObjectTable *prot;
                    
                if (SUCCEEDED(GetRunningObjectTable(0, &prot)))
                {
                    hr = prot->Register(ROTFLAGS_ALLOWANYCLIENT | ROTFLAGS_REGISTRATIONKEEPSALIVE, punk, pmoniker, &_dwRegisterROT);
                    prot->Release();
                }
                pmoniker->Release();
            }
            CoRegisterClassObject(CLSID_App, static_cast<IClassFactory *>(this), CLSCTX_LOCAL_SERVER, REGCLS_MULTIPLEUSE, &_dwRegisterClass;
        }
        FreeLibrary(hinstShSvcs);
    }
    return hr;
}
```

<span data-ttu-id="5005f-119">Für den Aufrufen von " [**ununningobjec\:: Register**](/windows/win32/api/objidl/nf-objidl-irunningobjecttable-register) " ist es erforderlich, dass die Komponente über die folgenden **AppID** -Informationen in der Registrierung verfügt.</span><span class="sxs-lookup"><span data-stu-id="5005f-119">The call to [**IRunningObjectTable::Register**](/windows/win32/api/objidl/nf-objidl-irunningobjecttable-register) requires that the component have the following **AppID** information in the registry.</span></span>

```
HKEY_CLASSES_ROOT
   AppID
      MyApp.exe
         (Default) = MyApplication
         AppID [REG_SZ] = {Your GUID here}
```

```
HKEY_CLASSES_ROOT
   AppID
      {The same GUID here}
         (Default) = MyApplication
         RunAs = Interactive User
```

## <a name="related-topics"></a><span data-ttu-id="5005f-120">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="5005f-120">Related topics</span></span>

[<span data-ttu-id="5005f-121">**Ihweventhandler**</span><span class="sxs-lookup"><span data-stu-id="5005f-121">**IHWEventHandler**</span></span>](/windows/desktop/api/Shobjidl/nn-shobjidl-ihweventhandler)

[<span data-ttu-id="5005f-122">**"Kreatehardwareeventmoniker"**</span><span class="sxs-lookup"><span data-stu-id="5005f-122">**CreateHardwareEventMoniker**</span></span>](createhardwareeventmoniker.md)
