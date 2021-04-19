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
# <a name="implementing-imfnetcredentialmanager"></a>Implementieren von IMF netkredentialmanager

Führen Sie in der [**IMF netkredentialmanager:: beginget-Anmelde**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialmanager-begingetcredentials) Informationen-Methode die folgenden Schritte aus.

1.  Wenn Sie nicht bereits über einen [**imfnetkredentialcache**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredentialcache) -Zeiger verfügen, rufen Sie [**mfkreatecredentialcache**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatecredentialcache) auf, um das Anmelde Informations Cache-Objekt zu erstellen. Speichern Sie diesen Zeiger.
2.  [**Imfnetkredentialcache:: GetCredential**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialcache-getcredential)aufrufen. Legen Sie die Flags im *dwauthenticationflags* -Parameter wie folgt fest:
    -   Wenn das **hrop** -Element der [**mfnetfordentialmanagergetparam**](/windows/desktop/api/mfidl/ns-mfidl-mfnetcredentialmanagergetparam) -Struktur gleich **NS \_ E \_ Proxy \_ AccessDenied** ist, legen Sie das **mfnet- \_ Authentifizierungsproxy \_** -Flag fest.
    -   Wenn der Wert für " **f** " auf " **true**" festgelegt ist, legen Sie das Flag für die **MF- \_ Authentifizierung \_ \_**
    -   Wenn für " **fiallowloggedonuser** " der Wert " **true**" festgelegt ist, legen Sie das Flag **\_ \_ \_ für \_ die MF-Authentifizierung**
3.  Die [**GetCredential**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialcache-getcredential) -Methode gibt einen [**IMF Network Credential**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredential) -Zeiger und möglicherweise das Flag "Prompt anfordern" zurück \_ . Speichern Sie den **IMF Network Credential** -Zeiger.
4.  Wenn [**GetCredential**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialcache-getcredential) das Flag zum Anfordern **der \_ Eingabeaufforderung** nicht zurückgibt, sind Sie damit abgeschlossen. Fahren Sie mit Schritt 9 fort.
5.  Andernfalls müssen Sie den Benutzer zur Eingabe des Benutzernamens und des Kennworts auffordern, wenn [**GetCredential**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialcache-getcredential) das Flag zum Anfordern der **\_ Eingabeaufforderung** zurückgibt.
6.  Wenn **das** Feld " **false**" lautet, verschlüsseln Sie die Anmelde Informationen.
7.  Rufen Sie [**imfnetcredential:: SETUSER**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredential-setuser) und [**imfnetcredential:: SetPassword**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredential-setpassword) auf, um den Namen und das Kennwort des Benutzers für das Anmelde Informationsobjekt festzulegen.
8.  Rufen Sie optional [**imfnetkredentialcache:: setuseroptions**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialcache-setuseroptions) auf, um das Anmelde Informations Cache-Objekt mit den Einstellungen des Benutzers zum Speichern und Senden von Anmelde Informationen zu aktualisieren.
9.  Rufen Sie den [**imfasynccallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) -Rückruf auf, indem Sie [**mfinvokecallback**](/windows/desktop/api/mfapi/nf-mfapi-mfinvokecallback)aufrufen.

Geben Sie in der [**IMF netkredentialmanager:: endgetcredential**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialmanager-endgetcredentials) -Methode den [**IMF netcredential**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredential) -Zeiger zurück, der in der [**begingetcreden-**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialmanager-begingetcredentials) Methode abgerufen wurde.

Übergeben Sie in der [**imfnetkredentialmanager:: setgood**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialmanager-setgood) -Methode die Eingabeparameter direkt an die [**imfnetkredentialcache:: setgood**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialcache-setgood) -Methode. Dadurch wird der Anmelde Informations Cache benachrichtigt, ob die Anmelde Informationen vom Server akzeptiert wurden.

Wenn Sie den Benutzer auffordern müssen (Schritt 5) oder die Anmelde Informationen verschlüsseln (Schritt 6), sollten Sie dies in einem Arbeits Warteschlangen Thread tun, sodass Sie die Microsoft Media Foundation Pipeline nicht blockieren. Rufen Sie [**mfputworkitem**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitem) auf, und führen Sie dann die restlichen Schritte innerhalb des Arbeits Warteschlangen Rückrufs aus.

> [!Note]  
> Beachten Sie, dass [**begingetanmeldeinformationen**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialmanager-begingetcredentials) möglicherweise aufgerufen werden, während die Netzwerkquelle erstellt wird. Wenn Sie daher die Netzwerkquelle durch Aufrufen der synchronen [**imfsourceresolver:: createobjectfromurl**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-createobjectfromurl) -Methode erstellen, kann der aufrufenden Thread blockieren, während die Anmelde Informationen abgerufen werden. Daher wird empfohlen, stattdessen die asynchrone [**imfsourceresolver:: beginkreateobjectfromurl**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-begincreateobjectfromurl) -Methode zu verwenden.

 

## <a name="example"></a>Beispiel

Dieses Beispiel zeigt eine Art von Verhalten, das von einem Anmelde Informationen-Manager bereitgestellt werden kann.

Hier ist eine Deklaration der-Klasse, die [**IMF netkredentialmanager**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredentialmanager)implementiert.


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



Zum Nachverfolgen des Status des [**begingetanmelde**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialmanager-begingetcredentials) -Vorgangs verwendet die-Klasse das folgende Hilfsobjekt:


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



Die [**begingetcredential**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialmanager-begingetcredentials) -Methode erstellt den Anmelde Informations Cache und Ruft einen [**IMF netcredential**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredential) -Zeiger ab. Wenn der Benutzer aufgefordert werden muss (angegeben durch das Flag zum Anfordern von **\_ Eingabeaufforderung** ), ruft die Methode [**mfputworkitem**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitem) auf, um eine neue Arbeitsaufgabe in die Warteschlange zu stellen:


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



Der Arbeits Warteschlangen Thread ruft " [**aufrufen**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke)" auf, der den Benutzer auffordert und dann " [**mfinvokecallback**](/windows/desktop/api/mfapi/nf-mfapi-mfinvokecallback) " aufruft, um den Rückruf Zeiger aufzurufen, der in [**begingetanmeldeinformationen**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialmanager-begingetcredentials)bereitgestellt wurde.


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



Die [**endgetcredensmethode**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialmanager-endgetcredentials) schließt den Vorgang ab, indem der [**imfnetcredential**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredential) -Zeiger an den Aufrufer zurückgegeben wird.


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

[Netzwerk Quellen Authentifizierung](network-source-authentication.md)
</dt> </dl>

 

 



