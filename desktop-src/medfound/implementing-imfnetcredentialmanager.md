---
description: Implementieren von MANAGERSNetCredentialManager
ms.assetid: 3eb2afec-195c-4d8d-8e08-7e6ec7c572f8
title: Implementieren von MANAGERSNetCredentialManager
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9877a1782a9703a8f43ed385f21f572576858955253cea5e38fa2d3143383e24
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119827840"
---
# <a name="implementing-imfnetcredentialmanager"></a>Implementieren von MANAGERSNetCredentialManager

Gehen Sie in der [**METHODE SFCNetCredentialManager::BeginGetCredentials**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialmanager-begingetcredentials) wie folgt vor.

1.  Wenn Sie noch keinen [**POINTERNetCredentialCache-Zeiger**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredentialcache) haben, rufen Sie [**MFCreateCredentialCache**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatecredentialcache) auf, um das Credential Cache-Objekt zu erstellen. Store diesen Zeiger.
2.  Rufen Sie [**ÜBERNETCredentialCache::GetCredential**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialcache-getcredential)auf. Legen Sie die Flags im *dwAuthenticationFlags-Parameter* wie folgt fest:
    -   Wenn das **hrOp-Element** der [**MFNetCredentialManagerGetParam-Struktur**](/windows/desktop/api/mfidl/ns-mfidl-mfnetcredentialmanagergetparam) **gleich NS \_ E PROXY \_ \_ ACCESSDENIED** ist, legen Sie das **PROXYflag MFNET AUTHENTICATION \_ \_ fest.**
    -   Wenn **fClearTextPackage** **TRUE** ist, legen Sie das **MFNET AUTHENTICATION \_ CLEAR \_ \_ TEXT-Flag** fest.
    -   Wenn **fAllowLoggedOnUser** auf **TRUE** festgelegt ist, legen Sie das **FLAG MFNET AUTHENTICATION \_ \_ LOGGED ON \_ \_ USER** fest.
3.  Die [**GetCredential-Methode**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialcache-getcredential) gibt einen [**POINTERNetCredential-Zeiger**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredential) und möglicherweise das REQUIRE \_ PROMPT-Flag zurück. Store dem **POINTERNetCredential-Zeiger.**
4.  Wenn [**GetCredential**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialcache-getcredential) das **REQUIRE \_ PROMPT-Flag** nicht zurückgibt, sind Sie fertig. Fahren Sie mit Schritt 9 fort.
5.  Andernfalls müssen Sie den Benutzer zur Eingabe seines Benutzernamens und Kennworts auffordern, wenn [**GetCredential**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialcache-getcredential) das **REQUIRE \_ PROMPT-Flag** zurückgibt.
6.  Wenn **fClearTextPackage** **FALSE** ist, verschlüsseln Sie die Anmeldeinformationen.
7.  Rufen Sie DEN NAMEN UND das Kennwort des Benutzers für das Credentials-Objekt auf, [**um**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredential-setpassword) [**DIE**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredential-setuser) NAMEN UND KENNWÖRTER DES Benutzers festzulegen.
8.  Rufen Sie optional [**ÜBERNETCredentialCache::SetUserOptions**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialcache-setuseroptions) auf, um das Cacheobjekt für Anmeldeinformationen mit den Einstellungen des Benutzers zum Speichern und Senden von Anmeldeinformationen zu aktualisieren.
9.  Rufen Sie den [**RÜCKRUF FÜR ASYNCHRONCALLBACK**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) auf, indem Sie [**MFInvokeCallback**](/windows/desktop/api/mfapi/nf-mfapi-mfinvokecallback)aufrufen.

Geben Sie in der [**SFCNetCredentialManager::EndGetCredentials-Methode**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialmanager-endgetcredentials) den in der [**BeginGetCredentials-Methode abgerufenen**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialmanager-begingetcredentials) [**POINTERNetCredential-Zeiger**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredential) zurück.

Übergeben Sie die Eingabeparameter in der [**METHODE VONNETCredentialManager::SetGood**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialmanager-setgood) direkt an die [**METHODE "LIXNetCredentialCache::SetGood".**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialcache-setgood) Dadurch wird der Anmeldeinformationscache benachrichtigt, ob die Anmeldeinformationen vom Server akzeptiert wurden.

Wenn Sie den Benutzer auffordern (Schritt 5) oder die Anmeldeinformationen verschlüsseln müssen (Schritt 6), sollten Sie dies in einem Arbeitswarteschlangenthread tun, damit Sie die Microsoft Media Foundation Pipeline nicht blockieren. Rufen Sie [**MFPutWorkItem auf,**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitem) und führen Sie dann die verbleibenden Schritte innerhalb des Work-Queue-Rückrufs aus.

> [!Note]  
> Beachten Sie, dass [**BeginGetCredentials**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialmanager-begingetcredentials) während der Erstellung der Netzwerkquelle aufgerufen werden kann. Wenn Sie daher die Netzwerkquelle durch Aufrufen der synchronen [**SYNCHRONENSOURCEResolver::CreateObjectFromURL-Methode**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-createobjectfromurl) erstellen, wird ihr aufrufender Thread möglicherweise blockiert, während die Anmeldeinformationen erfasst werden. Aus diesem Grund wird empfohlen, stattdessen die asynchrone [**ASYNCHRONOUSSOURCEResolver::BeginCreateObjectFromURL-Methode**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-begincreateobjectfromurl) zu verwenden.

 

## <a name="example"></a>Beispiel

Dieses Beispiel zeigt eine Art von Verhalten, die ein Anmeldeinformations-Manager bereitstellen kann.

Im Folgenden finden Sie eine Deklaration der -Klasse, die [**DASNETCredentialManager**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredentialmanager)implementiert.


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



Um den Status des [**BeginGetCredentials-Vorgangs**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialmanager-begingetcredentials) nachzuverfolgen, verwendet die -Klasse das folgende Hilfsobjekt:


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



Die [**BeginGetCredentials-Methode**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialmanager-begingetcredentials) erstellt den Anmeldeinformationscache und ruft einen [**POINTERNetCredential-Zeiger**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredential) ab. Wenn der Benutzer aufgefordert werden muss (angegeben durch das **REQUIRE \_ PROMPT-Flag),** ruft die Methode [**MFPutWorkItem**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitem) auf, um ein neues Arbeitselement in die Warteschlange zu stellen:


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



Der Arbeitswarteschlangenthread ruft [**Invoke auf,**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke)wodurch der Benutzer aufgefordert wird und dann [**MFInvokeCallback**](/windows/desktop/api/mfapi/nf-mfapi-mfinvokecallback) aufgerufen wird, um den Rückrufzeiger aufzurufen, der in [**BeginGetCredentials**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialmanager-begingetcredentials)bereitgestellt wurde.


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



Die [**EndGetCredentials-Methode**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialmanager-endgetcredentials) schließt den Vorgang ab, indem der [**POINTERNetCredential-Zeiger**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredential) an den Aufrufer zurückgegeben wird.


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



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Netzwerkquellauthentifizierung](network-source-authentication.md)
</dt> </dl>

 

 



