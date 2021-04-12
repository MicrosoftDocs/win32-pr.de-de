---
title: Schreiben eines benutzerdefinierten Ersatz Zeichens
description: Schreiben eines benutzerdefinierten Ersatz Zeichens
ms.assetid: 510e38e5-1965-46f4-b09c-6fa585cff993
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af0899702f6626d586f8a819e8fee2c2e67b7c80
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "104316514"
---
# <a name="writing-a-custom-surrogate"></a><span data-ttu-id="16a62-103">Schreiben eines benutzerdefinierten Ersatz Zeichens</span><span class="sxs-lookup"><span data-stu-id="16a62-103">Writing a Custom Surrogate</span></span>

<span data-ttu-id="16a62-104">Das vom System bereitgestellte Ersatz Zeichen ist für die meisten Situationen mehr als ausreichend. es gibt jedoch einige Fälle, in denen das Schreiben eines benutzerdefinierten Ersatz Zeichens sinnvoll sein könnte.</span><span class="sxs-lookup"><span data-stu-id="16a62-104">While the system-supplied surrogate will be more than adequate for most situations, there are some cases where writing a custom surrogate could be worthwhile.</span></span> <span data-ttu-id="16a62-105">Nachstehend sind einige Beispiele aufgeführt:</span><span class="sxs-lookup"><span data-stu-id="16a62-105">Following are some examples:</span></span>

-   <span data-ttu-id="16a62-106">Ein benutzerdefiniertes Ersatz Zeichen kann einige Optimierungen oder Semantik bereitstellen, die nicht im System-Ersatz Zeichen vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="16a62-106">A custom surrogate could provide some optimizations or semantics not present in the system surrogate.</span></span>
-   <span data-ttu-id="16a62-107">Wenn eine in-Process-DLL Code enthält, der davon abhängt, dass Sie sich im gleichen Prozess wie der Client befinden, funktioniert der DLL-Server nicht ordnungsgemäß, wenn er im System-Ersatz Zeichen ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="16a62-107">If an in-process DLL contains code that depends on being in the same process as the client, the DLL server will not function correctly if it is running in the system surrogate.</span></span> <span data-ttu-id="16a62-108">Ein benutzerdefiniertes Ersatz Zeichen kann auf eine bestimmte dll zugeschnitten werden, um dies zu tun.</span><span class="sxs-lookup"><span data-stu-id="16a62-108">A custom surrogate could be tailored to a specific DLL to deal with this.</span></span>
-   <span data-ttu-id="16a62-109">Das System-Ersatz Zeichen unterstützt ein gemischtes Threading Modell, sodass es sowohl kostenlose als auch Apartment-Modell-DLLs laden kann.</span><span class="sxs-lookup"><span data-stu-id="16a62-109">The system surrogate supports a mixed-threading model so that it can load both free and apartment model DLLs.</span></span> <span data-ttu-id="16a62-110">Ein benutzerdefiniertes Ersatz Zeichen ist möglicherweise so angepasst, dass nur Apartment-DLLs geladen werden. Dies kann aus Gründen der Effizienz oder das akzeptieren eines Befehlszeilen Arguments für den Typ der DLL erfolgen, die geladen werden darf.</span><span class="sxs-lookup"><span data-stu-id="16a62-110">A custom surrogate might be tailored to load only apartment DLLs for reasons of efficiency or to accept a command-line argument for the type of DLL it is allowed to load.</span></span>
-   <span data-ttu-id="16a62-111">Ein benutzerdefiniertes Ersatz Zeichen kann zusätzliche Befehlszeilenparameter verwenden, die vom System-Ersatz Zeichen nicht unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="16a62-111">A custom surrogate could take extra command-line parameters that the system surrogate does not.</span></span>
-   <span data-ttu-id="16a62-112">Der System Ersatz ruft [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) auf und weist ihn an, alle vorhandenen Sicherheitseinstellungen zu verwenden, die unter dem [AppID](appid-key.md) -Schlüssel in der Registrierung gefunden werden.</span><span class="sxs-lookup"><span data-stu-id="16a62-112">The system surrogate calls [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) and tells it to use any existing security settings found under the [AppID](appid-key.md) key in the registry.</span></span> <span data-ttu-id="16a62-113">Ein benutzerdefiniertes Ersatz Zeichen könnte einen anderen Sicherheitskontext verwenden.</span><span class="sxs-lookup"><span data-stu-id="16a62-113">A custom surrogate could use another security context.</span></span>
-   <span data-ttu-id="16a62-114">Schnittstellen, die nicht Remote fähig sind (z. b. die für die letzten okxs), funktionieren nicht mit dem System Ersatz Zeichen.</span><span class="sxs-lookup"><span data-stu-id="16a62-114">Interfaces that aren't remotable (such as those for recent OCXs) will not work with the system surrogate.</span></span> <span data-ttu-id="16a62-115">Ein benutzerdefiniertes Ersatz Zeichen kann die Schnittstellen der DLL-Datei mit einer eigenen Implementierung umschließen und Proxy-/Stub-DLLs mit einer Remote fähigen IDL-Definition verwenden, die eine Remote Schnittstelle der Schnittstelle ermöglichen würde.</span><span class="sxs-lookup"><span data-stu-id="16a62-115">A custom surrogate could wrap the DLL's interfaces with its own implementation and use proxy/stub DLLs with a remotable IDL definition that would allow the interface to be remoted.</span></span>

<span data-ttu-id="16a62-116">Der Haupt-Ersatz Thread sollte in der Regel die folgenden Setup Schritte ausführen:</span><span class="sxs-lookup"><span data-stu-id="16a62-116">The main surrogate thread should typically perform the following setup steps:</span></span>

1.  <span data-ttu-id="16a62-117">[**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex) aufrufen, um den Thread zu initialisieren und das Threading Modell festzulegen.</span><span class="sxs-lookup"><span data-stu-id="16a62-117">Call [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex) to initialize the thread and set the threading model.</span></span>
2.  <span data-ttu-id="16a62-118">Wenn Sie möchten, dass die DLL-Server, die auf dem Server ausgeführt werden sollen, die Sicherheitseinstellungen im **AppID** -Registrierungsschlüssel verwenden können, müssen Sie [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) mit der eoac- \_ AppID-Funktion abrufen.</span><span class="sxs-lookup"><span data-stu-id="16a62-118">If you want the DLL servers that are to run in the server to be able to use the security settings in the **AppID** registry key, call [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) with the EOAC\_APPID capability.</span></span> <span data-ttu-id="16a62-119">Andernfalls werden ältere Sicherheitseinstellungen verwendet.</span><span class="sxs-lookup"><span data-stu-id="16a62-119">Otherwise, legacy security settings will be used.</span></span>
3.  <span data-ttu-id="16a62-120">Ruft [**coregisterersatz**](/windows/desktop/api/combaseapi/nf-combaseapi-coregistersurrogate) auf, um die Ersatz Schnittstelle für com zu registrieren.</span><span class="sxs-lookup"><span data-stu-id="16a62-120">Call [**CoRegisterSurrogate**](/windows/desktop/api/combaseapi/nf-combaseapi-coregistersurrogate) to register the surrogate interface to COM.</span></span>
4.  <span data-ttu-id="16a62-121">Nennen Sie [**isurrogate:: loaddllserver**](/windows/win32/api/objidlbase/nf-objidlbase-isurrogate-loaddllserver) für die angeforderte CLSID.</span><span class="sxs-lookup"><span data-stu-id="16a62-121">Call [**ISurrogate::LoadDllServer**](/windows/win32/api/objidlbase/nf-objidlbase-isurrogate-loaddllserver) for the requested CLSID.</span></span>
5.  <span data-ttu-id="16a62-122">Platzieren Sie den Haupt Thread in einer Schleife, um [**cofreunusedlibraries**](/windows/desktop/api/combaseapi/nf-combaseapi-cofreeunusedlibraries) in regelmäßigen Abständen aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="16a62-122">Put main thread in a loop to call [**CoFreeUnusedLibraries**](/windows/desktop/api/combaseapi/nf-combaseapi-cofreeunusedlibraries) periodically.</span></span>
6.  <span data-ttu-id="16a62-123">Wenn com [**isurrogate:: freesurrogate**](/windows/win32/api/objidlbase/nf-objidlbase-isurrogate-freesurrogate)aufruft, widerrufen Sie alle Klassenfactorys, und beenden Sie.</span><span class="sxs-lookup"><span data-stu-id="16a62-123">When COM calls [**ISurrogate::FreeSurrogate**](/windows/win32/api/objidlbase/nf-objidlbase-isurrogate-freesurrogate), revoke all class factories and exit.</span></span>

<span data-ttu-id="16a62-124">Ein Ersatzprozess muss die [**isurrogate**](/windows/win32/api/objidlbase/nn-objidlbase-isurrogate) -Schnittstelle implementieren.</span><span class="sxs-lookup"><span data-stu-id="16a62-124">A surrogate process must implement the [**ISurrogate**](/windows/win32/api/objidlbase/nn-objidlbase-isurrogate) interface.</span></span> <span data-ttu-id="16a62-125">Diese Schnittstelle muss registriert werden, wenn ein neuer Ersatz Zeichen gestartet wird und nach dem Aufrufen von [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex).</span><span class="sxs-lookup"><span data-stu-id="16a62-125">This interface should be registered when a new surrogate is started and after calling [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex).</span></span> <span data-ttu-id="16a62-126">Wie in den vorherigen Schritten angegeben, verfügt die **isurrogate** -Schnittstelle über zwei Methoden, die com aufruft: [**loaddllserver**](/windows/win32/api/objidlbase/nf-objidlbase-isurrogate-loaddllserver), um neue dll-Server dynamisch in vorhandene Surrogates zu laden. und [**freesurrogate**](/windows/win32/api/objidlbase/nf-objidlbase-isurrogate-freesurrogate), um das Ersatz Zeichen freizugeben.</span><span class="sxs-lookup"><span data-stu-id="16a62-126">As indicated in the preceding steps, the **ISurrogate** interface has two methods that COM calls: [**LoadDllServer**](/windows/win32/api/objidlbase/nf-objidlbase-isurrogate-loaddllserver), to dynamically load new DLL servers into existing surrogates; and [**FreeSurrogate**](/windows/win32/api/objidlbase/nf-objidlbase-isurrogate-freesurrogate), to free the surrogate.</span></span>

<span data-ttu-id="16a62-127">Die Implementierung von [**loaddllserver**](/windows/win32/api/objidlbase/nf-objidlbase-isurrogate-loaddllserver), die com mit einer Lade Anforderung aufruft, muss zunächst ein klassenfactoryobjekt erstellen, das [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown), [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory)und [**IMarshal**](/windows/win32/api/objidlbase/nn-objidlbase-imarshal)unterstützt, und dann [**CoRegisterClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-coregisterclassobject) aufrufen, um das Objekt als Klassenfactory für die angeforderte CLSID zu registrieren.</span><span class="sxs-lookup"><span data-stu-id="16a62-127">The implementation of [**LoadDllServer**](/windows/win32/api/objidlbase/nf-objidlbase-isurrogate-loaddllserver), which COM calls with a load request, must first create a class factory object that supports [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown), [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory), and [**IMarshal**](/windows/win32/api/objidlbase/nn-objidlbase-imarshal), and then call [**CoRegisterClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-coregisterclassobject) to register the object as the class factory for the requested CLSID.</span></span>

<span data-ttu-id="16a62-128">Die vom Ersatzprozess registrierte Klassenfactory ist nicht die tatsächliche Klassenfactory, die vom dll-Server implementiert wird. Sie ist jedoch eine generische Klassenfactory, die von dem Ersatzprozess implementiert wird, der [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory) und [**IMarshal**](/windows/win32/api/objidlbase/nn-objidlbase-imarshal)unterstützt.</span><span class="sxs-lookup"><span data-stu-id="16a62-128">The class factory registered by the surrogate process is not the actual class factory implemented by the DLL server but is a generic class factory implemented by the surrogate process that supports [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory) and [**IMarshal**](/windows/win32/api/objidlbase/nn-objidlbase-imarshal).</span></span> <span data-ttu-id="16a62-129">Da es sich um die Klassenfactory des Ersatz Zeichens handelt, anstatt um die des dll-Servers, die registriert wird, muss die Klassenfactory des Ersatz dienstangs die echte Klassenfactory verwenden, um eine Instanz des Objekts für die registrierte CLSID zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="16a62-129">Because it is the surrogate's class factory, rather than that of the DLL server that is being registered, the surrogate's class factory will need to use the real class factory to create an instance of the object for the registered CLSID.</span></span> <span data-ttu-id="16a62-130">Die [**IClassFactory::**](/windows/desktop/api/Unknwn/nf-unknwn-iclassfactory-createinstance) -Methode des Ersatz Zeichens sollte in etwa wie im folgenden Beispiel aussehen:</span><span class="sxs-lookup"><span data-stu-id="16a62-130">The surrogate's [**IClassFactory::CreateInstance**](/windows/desktop/api/Unknwn/nf-unknwn-iclassfactory-createinstance) should look something like the following example:</span></span>


```C++
STDMETHODIMP CSurrogateFactory::CreateInstance(
  IUnknown* pUnkOuter, 
  REFIID iid, 
  void** ppv)
{
    void* pcf;
    HRESULT hr;
 
    hr = CoGetClassObject(clsid, CLSCTX_INPROC_SERVER, NULL, IID_IClassFactory, &pcf);
    if ( FAILED(hr) )
        return hr;
    hr = ((IClassFactory*)pcf)->CreateInstance(pUnkOuter, iid, ppv);
    ((IClassFactory*)pcf)->Release();
    return hr;
}
 
```



<span data-ttu-id="16a62-131">Die Klassenfactory des Ersatz Zeichens muss auch " [**IMarshal**](/windows/win32/api/objidlbase/nn-objidlbase-imarshal) " unterstützen, da ein [**CoGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetclassobject) -aufrufen eine beliebige Schnittstelle aus der registrierten Klassenfactory anfordern kann, nicht nur " [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory)".</span><span class="sxs-lookup"><span data-stu-id="16a62-131">The surrogate's class factory must also support [**IMarshal**](/windows/win32/api/objidlbase/nn-objidlbase-imarshal) because a call to [**CoGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetclassobject) can request any interface from the registered class factory, not just [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory).</span></span> <span data-ttu-id="16a62-132">Da die generische Klassenfactory nur [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) und **IClassFactory** unterstützt, müssen Anforderungen für andere Schnittstellen an das echte Objekt weitergeleitet werden.</span><span class="sxs-lookup"><span data-stu-id="16a62-132">Further, since the generic class factory supports only [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) and **IClassFactory**, requests for other interfaces must be directed to the real object.</span></span> <span data-ttu-id="16a62-133">Daher sollte eine [**MarshalInterface**](/windows/win32/api/objidlbase/nf-objidlbase-imarshal-marshalinterface) -Methode vorhanden sein, die der folgenden ähnelt:</span><span class="sxs-lookup"><span data-stu-id="16a62-133">Thus, there should be a [**MarshalInterface**](/windows/win32/api/objidlbase/nf-objidlbase-imarshal-marshalinterface) method which should be similar to the following:</span></span>


```C++
STDMETHODIMP CSurrogateFactory::MarshalInterface(
  IStream *pStm,  
  REFIID riid, void *pv, 
  WORD dwDestContext, 
  void *pvDestContext, 
  DWORD mshlflags )
{   
    void * pCF = NULL;
    HRESULT hr;
 
    hr = CoGetClassObject(clsid, CLSCTX_INPROC_SERVER, NULL, riid, &pCF);
    if ( FAILED(hr) )
        return hr;   
    hr = CoMarshalInterface(pStm, riid, (IUnknown*)pCF, dwDestContext, pvDestContext,  mshlflags);
    ((IUnknown*)pCF)->Release();
    return S_OK;
 
```



<span data-ttu-id="16a62-134">Das Ersatz Zeichen, das einen dll-Server enthält, muss die Klassen Objekte des dll-Servers mit einem [**CoRegisterClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-coregisterclassobject)-Aufrufer veröffentlichen.</span><span class="sxs-lookup"><span data-stu-id="16a62-134">The surrogate that houses a DLL server must publish the DLL server's class object(s) with a call to [**CoRegisterClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-coregisterclassobject).</span></span> <span data-ttu-id="16a62-135">Alle Klassenfactorys für dll-Surrogates müssen als REGCLS-Ersatz Zeichen registriert werden \_ .</span><span class="sxs-lookup"><span data-stu-id="16a62-135">All class factories for DLL surrogates should be registered as REGCLS\_SURROGATE.</span></span> <span data-ttu-id="16a62-136">REGCLS \_ singluse und REGCLS \_ multipleuse sollten nicht für dll-Server verwendet werden, die in Surrogates geladen werden.</span><span class="sxs-lookup"><span data-stu-id="16a62-136">REGCLS\_SINGLUSE and REGCLS\_MULTIPLEUSE should not be used for DLL servers loaded into surrogates.</span></span>

<span data-ttu-id="16a62-137">Befolgen Sie diese Richtlinien, um einen Ersatzprozess zu erstellen, wenn dies erforderlich ist, sollten Sie das richtige Verhalten sicherstellen.</span><span class="sxs-lookup"><span data-stu-id="16a62-137">Following these guidelines for creating a surrogate process when it is necessary to do so should ensure proper behavior.</span></span>

## <a name="related-topics"></a><span data-ttu-id="16a62-138">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="16a62-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="16a62-139">DLL-Surrogates</span><span class="sxs-lookup"><span data-stu-id="16a62-139">DLL Surrogates</span></span>](dll-surrogates.md)
</dt> </dl>

 

 