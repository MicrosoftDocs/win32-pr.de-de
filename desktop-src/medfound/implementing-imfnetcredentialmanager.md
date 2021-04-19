---
description: Implementieren von IMF netkredentialmanager
ms.assetid: 3eb2afec-195c-4d8d-8e08-7e6ec7c572f8
title: Implementieren von IMF netkredentialmanager
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55c026f2c12b2ff248032a56d9c48a0e0e1576c1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106360056"
---
# <a name="implementing-imfnetcredentialmanager"></a><span data-ttu-id="77971-103">Implementieren von IMF netkredentialmanager</span><span class="sxs-lookup"><span data-stu-id="77971-103">Implementing IMFNetCredentialManager</span></span>

<span data-ttu-id="77971-104">Führen Sie in der [**IMF netkredentialmanager:: beginget-Anmelde**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialmanager-begingetcredentials) Informationen-Methode die folgenden Schritte aus.</span><span class="sxs-lookup"><span data-stu-id="77971-104">In the [**IMFNetCredentialManager::BeginGetCredentials**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialmanager-begingetcredentials) method, do the following.</span></span>

1.  <span data-ttu-id="77971-105">Wenn Sie nicht bereits über einen [**imfnetkredentialcache**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredentialcache) -Zeiger verfügen, rufen Sie [**mfkreatecredentialcache**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatecredentialcache) auf, um das Anmelde Informations Cache-Objekt zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="77971-105">If you do not have an [**IMFNetCredentialCache**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredentialcache) pointer already, call [**MFCreateCredentialCache**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatecredentialcache) to create the credential cache object.</span></span> <span data-ttu-id="77971-106">Speichern Sie diesen Zeiger.</span><span class="sxs-lookup"><span data-stu-id="77971-106">Store this pointer.</span></span>
2.  <span data-ttu-id="77971-107">[**Imfnetkredentialcache:: GetCredential**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialcache-getcredential)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="77971-107">Call [**IMFNetCredentialCache::GetCredential**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialcache-getcredential).</span></span> <span data-ttu-id="77971-108">Legen Sie die Flags im *dwauthenticationflags* -Parameter wie folgt fest:</span><span class="sxs-lookup"><span data-stu-id="77971-108">Set the flags in the *dwAuthenticationFlags* parameter as follows:</span></span>
    -   <span data-ttu-id="77971-109">Wenn das **hrop** -Element der [**mfnetfordentialmanagergetparam**](/windows/desktop/api/mfidl/ns-mfidl-mfnetcredentialmanagergetparam) -Struktur gleich **NS \_ E \_ Proxy \_ AccessDenied** ist, legen Sie das **mfnet- \_ Authentifizierungsproxy \_** -Flag fest.</span><span class="sxs-lookup"><span data-stu-id="77971-109">If the **hrOp** member of the [**MFNetCredentialManagerGetParam**](/windows/desktop/api/mfidl/ns-mfidl-mfnetcredentialmanagergetparam) structure equals **NS\_E\_PROXY\_ACCESSDENIED**, set the **MFNET\_AUTHENTICATION\_PROXY** flag.</span></span>
    -   <span data-ttu-id="77971-110">Wenn der Wert für " **f** " auf " **true**" festgelegt ist, legen Sie das Flag für die **MF- \_ Authentifizierung \_ \_**</span><span class="sxs-lookup"><span data-stu-id="77971-110">If **fClearTextPackage** is **TRUE**, set the **MFNET\_AUTHENTICATION\_CLEAR\_TEXT** flag.</span></span>
    -   <span data-ttu-id="77971-111">Wenn für " **fiallowloggedonuser** " der Wert " **true**" festgelegt ist, legen Sie das Flag **\_ \_ \_ für \_ die MF-Authentifizierung**</span><span class="sxs-lookup"><span data-stu-id="77971-111">If **fAllowLoggedOnUser** is **TRUE**, set the **MFNET\_AUTHENTICATION\_LOGGED\_ON\_USER** flag.</span></span>
3.  <span data-ttu-id="77971-112">Die [**GetCredential**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialcache-getcredential) -Methode gibt einen [**IMF Network Credential**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredential) -Zeiger und möglicherweise das Flag "Prompt anfordern" zurück \_ .</span><span class="sxs-lookup"><span data-stu-id="77971-112">The [**GetCredential**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialcache-getcredential) method returns an [**IMFNetCredential**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredential) pointer and possibly the REQUIRE\_PROMPT flag.</span></span> <span data-ttu-id="77971-113">Speichern Sie den **IMF Network Credential** -Zeiger.</span><span class="sxs-lookup"><span data-stu-id="77971-113">Store the **IMFNetCredential** pointer.</span></span>
4.  <span data-ttu-id="77971-114">Wenn [**GetCredential**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialcache-getcredential) das Flag zum Anfordern **der \_ Eingabeaufforderung** nicht zurückgibt, sind Sie damit abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="77971-114">If [**GetCredential**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialcache-getcredential) does not return the **REQUIRE\_PROMPT** flag, you are done.</span></span> <span data-ttu-id="77971-115">Fahren Sie mit Schritt 9 fort.</span><span class="sxs-lookup"><span data-stu-id="77971-115">Skip to step 9.</span></span>
5.  <span data-ttu-id="77971-116">Andernfalls müssen Sie den Benutzer zur Eingabe des Benutzernamens und des Kennworts auffordern, wenn [**GetCredential**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialcache-getcredential) das Flag zum Anfordern der **\_ Eingabeaufforderung** zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="77971-116">Otherwise, if [**GetCredential**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialcache-getcredential) returns the **REQUIRE\_PROMPT** flag, you must prompt the user for his or her user name and password.</span></span>
6.  <span data-ttu-id="77971-117">Wenn **das** Feld " **false**" lautet, verschlüsseln Sie die Anmelde Informationen.</span><span class="sxs-lookup"><span data-stu-id="77971-117">If **fClearTextPackage** is **FALSE**, encrypt the credentials.</span></span>
7.  <span data-ttu-id="77971-118">Rufen Sie [**imfnetcredential:: SETUSER**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredential-setuser) und [**imfnetcredential:: SetPassword**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredential-setpassword) auf, um den Namen und das Kennwort des Benutzers für das Anmelde Informationsobjekt festzulegen.</span><span class="sxs-lookup"><span data-stu-id="77971-118">Call [**IMFNetCredential::SetUser**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredential-setuser) and [**IMFNetCredential::SetPassword**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredential-setpassword) to set the user's name and password on the credentials object.</span></span>
8.  <span data-ttu-id="77971-119">Rufen Sie optional [**imfnetkredentialcache:: setuseroptions**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialcache-setuseroptions) auf, um das Anmelde Informations Cache-Objekt mit den Einstellungen des Benutzers zum Speichern und Senden von Anmelde Informationen zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="77971-119">Optionally, call [**IMFNetCredentialCache::SetUserOptions**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialcache-setuseroptions) to update the credential cache object with the user's preferences for storing and sending credentials.</span></span>
9.  <span data-ttu-id="77971-120">Rufen Sie den [**imfasynccallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) -Rückruf auf, indem Sie [**mfinvokecallback**](/windows/desktop/api/mfapi/nf-mfapi-mfinvokecallback)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="77971-120">Invoke the [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) callback by calling [**MFInvokeCallback**](/windows/desktop/api/mfapi/nf-mfapi-mfinvokecallback).</span></span>

<span data-ttu-id="77971-121">Geben Sie in der [**IMF netkredentialmanager:: endgetcredential**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialmanager-endgetcredentials) -Methode den [**IMF netcredential**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredential) -Zeiger zurück, der in der [**begingetcreden-**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialmanager-begingetcredentials) Methode abgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="77971-121">In the [**IMFNetCredentialManager::EndGetCredentials**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialmanager-endgetcredentials) method, return the [**IMFNetCredential**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredential) pointer obtained in the [**BeginGetCredentials**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialmanager-begingetcredentials) method.</span></span>

<span data-ttu-id="77971-122">Übergeben Sie in der [**imfnetkredentialmanager:: setgood**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialmanager-setgood) -Methode die Eingabeparameter direkt an die [**imfnetkredentialcache:: setgood**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialcache-setgood) -Methode.</span><span class="sxs-lookup"><span data-stu-id="77971-122">In the [**IMFNetCredentialManager::SetGood**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialmanager-setgood) method, pass the input parameters directly to the [**IMFNetCredentialCache::SetGood**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialcache-setgood) method.</span></span> <span data-ttu-id="77971-123">Dadurch wird der Anmelde Informations Cache benachrichtigt, ob die Anmelde Informationen vom Server akzeptiert wurden.</span><span class="sxs-lookup"><span data-stu-id="77971-123">This notifies the credential cache whether the credentials were accepted by the server.</span></span>

<span data-ttu-id="77971-124">Wenn Sie den Benutzer auffordern müssen (Schritt 5) oder die Anmelde Informationen verschlüsseln (Schritt 6), sollten Sie dies in einem Arbeits Warteschlangen Thread tun, sodass Sie die Microsoft Media Foundation Pipeline nicht blockieren.</span><span class="sxs-lookup"><span data-stu-id="77971-124">If you need to prompt the user (step 5) or encrypt the credentials (step 6), you should do so on a work-queue thread, so that you do not block the Microsoft Media Foundation pipeline.</span></span> <span data-ttu-id="77971-125">Rufen Sie [**mfputworkitem**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitem) auf, und führen Sie dann die restlichen Schritte innerhalb des Arbeits Warteschlangen Rückrufs aus.</span><span class="sxs-lookup"><span data-stu-id="77971-125">Call [**MFPutWorkItem**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitem) and then perform the remaining steps inside the work-queue callback.</span></span>

> [!Note]  
> <span data-ttu-id="77971-126">Beachten Sie, dass [**begingetanmeldeinformationen**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialmanager-begingetcredentials) möglicherweise aufgerufen werden, während die Netzwerkquelle erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="77971-126">Be aware that [**BeginGetCredentials**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialmanager-begingetcredentials) might be invoked while the network source is being created.</span></span> <span data-ttu-id="77971-127">Wenn Sie daher die Netzwerkquelle durch Aufrufen der synchronen [**imfsourceresolver:: createobjectfromurl**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-createobjectfromurl) -Methode erstellen, kann der aufrufenden Thread blockieren, während die Anmelde Informationen abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="77971-127">Therefore, if you create the network source by calling the synchronous [**IMFSourceResolver::CreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-createobjectfromurl) method, your calling thread might block while the credentials are acquired.</span></span> <span data-ttu-id="77971-128">Daher wird empfohlen, stattdessen die asynchrone [**imfsourceresolver:: beginkreateobjectfromurl**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-begincreateobjectfromurl) -Methode zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="77971-128">Therefore, it is recommended to use the asynchronous [**IMFSourceResolver::BeginCreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-begincreateobjectfromurl) method instead.</span></span>

 

## <a name="example"></a><span data-ttu-id="77971-129">Beispiel</span><span class="sxs-lookup"><span data-stu-id="77971-129">Example</span></span>

<span data-ttu-id="77971-130">Dieses Beispiel zeigt eine Art von Verhalten, das von einem Anmelde Informationen-Manager bereitgestellt werden kann.</span><span class="sxs-lookup"><span data-stu-id="77971-130">This example shows one type of behavior that a credential manager could provide.</span></span>

<span data-ttu-id="77971-131">Hier ist eine Deklaration der-Klasse, die [**IMF netkredentialmanager**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredentialmanager)implementiert.</span><span class="sxs-lookup"><span data-stu-id="77971-131">Here is a declaration of the class that implements [**IMFNetCredentialManager**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredentialmanager).</span></span>


```C++
class CCredentialManager : public IMFNetCredentialManager, IMFAsyncCallback 
{
    long                    m_cRef;
    IMFNetCredentialCache   *m_pCredentialCache;

public:
    CCredentialManager () : m_cRef(1), m_pCredentialCache(NULL)
    { 
    }
    ~CCredentialManager()
    {
        SafeRelease(&m_pCredentialCache);
    }

    STDMETHODIMP QueryInterface(REFIID riid, void** ppv)
    {
        static const QITAB qit[] = 
        {
            QITABENT(CCredentialManager, IMFNetCredentialManager),
            QITABENT(CCredentialManager, IMFAsyncCallback),
            { 0 }
        };
        return QISearch(this, qit, riid, ppv);
    }      

    STDMETHODIMP_(ULONG) AddRef()
    {
        return InterlockedIncrement(&m_cRef);
    }

    STDMETHODIMP_(ULONG) Release()
    {
        LONG cRef = InterlockedDecrement(&m_cRef);
        if (cRef == 0)
        {
            delete this;
        }
        return cRef;
    }

    STDMETHODIMP BeginGetCredentials(
        MFNetCredentialManagerGetParam* pParam,
        IMFAsyncCallback* pCallback,
        IUnknown* pState
        );

    STDMETHODIMP EndGetCredentials(
        IMFAsyncResult* pResult, 
        IMFNetCredential** ppCred);

    STDMETHODIMP SetGood(IMFNetCredential* pCred, BOOL fGood)
    {
        if (!pCred)
        {
            return E_POINTER;
        }

        return m_pCredentialCache->SetGood(pCred, fGood);
    }


    STDMETHODIMP GetParameters(DWORD* pdwFlags, DWORD* pdwQueue)
    {
        return E_NOTIMPL;
    }

    STDMETHODIMP Invoke(IMFAsyncResult* pResult);
};
```



<span data-ttu-id="77971-132">Zum Nachverfolgen des Status des [**begingetanmelde**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialmanager-begingetcredentials) -Vorgangs verwendet die-Klasse das folgende Hilfsobjekt:</span><span class="sxs-lookup"><span data-stu-id="77971-132">To track the state of the [**BeginGetCredentials**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialmanager-begingetcredentials) operation, the class uses the following helper object:</span></span>


```C++
// Holds state information for the GetCredentials operation, so that work can 
// be moved to a work-queue thread.

struct CredentialOp : public IUnknown
{
    long                m_cRef;
    IMFNetCredential    *m_pCredential;
    DWORD               m_dwFlags;

    CredentialOp(IMFNetCredential *pCredential) 
        : m_cRef(1), m_dwFlags(0), m_pCredential(pCredential)
    {
        m_pCredential->AddRef();
    }

    ~CredentialOp()
    {
        SafeRelease(&m_pCredential);
    }

    STDMETHODIMP QueryInterface(REFIID riid, void** ppv)
    {
        static const QITAB qit[] = 
        {
            QITABENT(CredentialOp, IUnknown),
            { 0 }
        };
        return QISearch(this, qit, riid, ppv);
    }      

    STDMETHODIMP_(ULONG) AddRef()
    {
        return InterlockedIncrement(&m_cRef);
    }

    STDMETHODIMP_(ULONG) Release()
    {
        LONG cRef = InterlockedDecrement(&m_cRef);
        if (cRef == 0)
        {
            delete this;
        }
        return cRef;
    }
};
```



<span data-ttu-id="77971-133">Die [**begingetcredential**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialmanager-begingetcredentials) -Methode erstellt den Anmelde Informations Cache und Ruft einen [**IMF netcredential**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredential) -Zeiger ab.</span><span class="sxs-lookup"><span data-stu-id="77971-133">The [**BeginGetCredentials**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialmanager-begingetcredentials) method creates the credential cache and gets an [**IMFNetCredential**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredential) pointer.</span></span> <span data-ttu-id="77971-134">Wenn der Benutzer aufgefordert werden muss (angegeben durch das Flag zum Anfordern von **\_ Eingabeaufforderung** ), ruft die Methode [**mfputworkitem**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitem) auf, um eine neue Arbeitsaufgabe in die Warteschlange zu stellen:</span><span class="sxs-lookup"><span data-stu-id="77971-134">If the user must be prompted (indicated by the **REQUIRE\_PROMPT** flag), the method calls [**MFPutWorkItem**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitem) to queue a new work item:</span></span>


```C++
STDMETHODIMP CCredentialManager::BeginGetCredentials(
    MFNetCredentialManagerGetParam* pParam,
    IMFAsyncCallback* pCallback,
    IUnknown* pState
    )
{
    if (!pParam || !pCallback)
    {
        return E_POINTER;
    }

    DWORD dwAuthenticationFlags = 0;
    DWORD dwRequirementFlags = 0;

    if (pParam->hrOp == NS_E_PROXY_ACCESSDENIED)
    {
        dwAuthenticationFlags |= MFNET_AUTHENTICATION_PROXY;
    }

    if (pParam->fAllowLoggedOnUser)
    {
        dwAuthenticationFlags |= MFNET_AUTHENTICATION_LOGGED_ON_USER;
    }

    if (pParam->fClearTextPackage)
    {
        dwAuthenticationFlags |= MFNET_AUTHENTICATION_CLEAR_TEXT;
    }

    IMFNetCredential *pCredential =  NULL;
    IMFAsyncResult* pResult = NULL;

    HRESULT hr = S_OK;

    if (m_pCredentialCache == NULL)
    {
        hr = MFCreateCredentialCache(&m_pCredentialCache);
        if (FAILED(hr))
        {
            goto done;
        }
    }

    hr = m_pCredentialCache->GetCredential(
        pParam->pszUrl, 
        pParam->pszRealm, 
        dwAuthenticationFlags, 
        &pCredential, 
        &dwRequirementFlags
        );

    if (FAILED(hr))
    {
        goto done;
    }

    if( ( dwRequirementFlags & REQUIRE_PROMPT ) == 0 )
    {
        // The credential is good to use. Prompting the user is not required.
        hr = S_OK;
        goto done;
    }

    // The credential requires prompting the user. 
    CredentialOp *pOp = new (std::nothrow) CredentialOp(pCredential);

    if (pOp == NULL)
    {
        hr = E_OUTOFMEMORY;
        goto done;
    }

    // Set flags. Use these to inform the user if the credentials will
    // be sent in plaintext or saved in the credential cache.

    if (pParam->fClearTextPackage)
    {
        // Notify the user that credentials will be sent in plaintext.
        pOp->m_dwFlags |= MFNET_CREDENTIAL_ALLOW_CLEAR_TEXT;
    }

    if(dwRequirementFlags & REQUIRE_SAVE_SELECTED )
    {
        // Credentials will be saved in the cache by default.
        pOp->m_dwFlags |= MFNET_CREDENTIAL_SAVE;
    }

    // NOTE: The application should enable to user to deselect these two flags;
    // for example, through check boxes in the prompt dialog.


    // Now queue the work item.

    hr = MFCreateAsyncResult(pOp, pCallback, pState, &pResult);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = MFPutWorkItem(MFASYNC_CALLBACK_QUEUE_LONG_FUNCTION, this, pResult);

done:
    SafeRelease(&pResult);
    SafeRelease(&pCredential);
    SafeRelease(&pOp);
    return hr;
}
```



<span data-ttu-id="77971-135">Der Arbeits Warteschlangen Thread ruft " [**aufrufen**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke)" auf, der den Benutzer auffordert und dann " [**mfinvokecallback**](/windows/desktop/api/mfapi/nf-mfapi-mfinvokecallback) " aufruft, um den Rückruf Zeiger aufzurufen, der in [**begingetanmeldeinformationen**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialmanager-begingetcredentials)bereitgestellt wurde.</span><span class="sxs-lookup"><span data-stu-id="77971-135">The work-queue thread calls [**Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke), which prompts the user and then calls [**MFInvokeCallback**](/windows/desktop/api/mfapi/nf-mfapi-mfinvokecallback) to invoke the callback pointer that was provided in [**BeginGetCredentials**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialmanager-begingetcredentials).</span></span>


```C++
STDMETHODIMP CCredentialManager::Invoke(IMFAsyncResult* pResult)
{
    IUnknown *pState = NULL;
    IMFAsyncResult *pGetCredentialsResult = NULL;
    IUnknown *pOpState = NULL;

    CredentialOp *pOp = NULL;   // not AddRef'd

    HRESULT hr = pResult->GetState(&pState);

    if (SUCCEEDED(hr))
    {
        hr = pState->QueryInterface(IID_PPV_ARGS(&pGetCredentialsResult));
    }

    if (SUCCEEDED(hr))
    {
        hr = pGetCredentialsResult->GetObject(&pOpState);
    }

    if (SUCCEEDED(hr))
    {
        pOp = static_cast<CredentialOp*>(pOpState);

        // Display a dialog for the user to enter user name and password.
        hr = PromptUserCredentials(pOp);
    }

    if (SUCCEEDED(hr) && m_pCredentialCache)
    {
        // Update with options set by the user.
        hr = m_pCredentialCache->SetUserOptions(
            pOp->m_pCredential, 
            pOp->m_dwFlags
            );
    }

    if (pGetCredentialsResult)
    {
        pGetCredentialsResult->SetStatus(hr);
        MFInvokeCallback(pGetCredentialsResult);
    }

    SafeRelease(&pState);
    SafeRelease(&pGetCredentialsResult);
    SafeRelease(&pOpState);
    return S_OK;
}
```



<span data-ttu-id="77971-136">Die [**endgetcredensmethode**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialmanager-endgetcredentials) schließt den Vorgang ab, indem der [**imfnetcredential**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredential) -Zeiger an den Aufrufer zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="77971-136">The [**EndGetCredentials**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialmanager-endgetcredentials) method completes the operation by returning the [**IMFNetCredential**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredential) pointer to the caller.</span></span>


```C++
STDMETHODIMP CCredentialManager::EndGetCredentials(
    IMFAsyncResult* pResult, 
    IMFNetCredential** ppCred
    )
{
    if (!pResult || !ppCred)
    {
        return E_POINTER;
    }

    *ppCred = NULL;

    IUnknown *pUnk = NULL;

    // Check the result of the asynchronous operation.
    HRESULT hr = pResult->GetStatus();

    if (FAILED(hr))
    {
        // The operation failed.
        goto done;
    }

    hr = pResult->GetObject(&pUnk);
    if (FAILED(hr))
    {
        goto done;
    }

    CredentialOp *pOp = static_cast<CredentialOp*>(pUnk);

    *ppCred = pOp->m_pCredential;
    pOp->m_pCredential = NULL;

done:
    SafeRelease(&pUnk);
    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="77971-137">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="77971-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="77971-138">Netzwerk Quellen Authentifizierung</span><span class="sxs-lookup"><span data-stu-id="77971-138">Network Source Authentication</span></span>](network-source-authentication.md)
</dt> </dl>

 

 



