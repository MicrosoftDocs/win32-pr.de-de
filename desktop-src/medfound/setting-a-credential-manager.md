---
description: Festlegen eines Credential-Managers
ms.assetid: a20c2e6c-e9d9-438f-a57a-e3080587c11c
title: Festlegen eines Credential-Managers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c98d9d9572438a63f93f916a0084f8a33a7bca5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345196"
---
# <a name="setting-a-credential-manager"></a><span data-ttu-id="3af0d-103">Festlegen eines Credential-Managers</span><span class="sxs-lookup"><span data-stu-id="3af0d-103">Setting a Credential Manager</span></span>

<span data-ttu-id="3af0d-104">Eine Anwendung, die Anmelde Informationen für die Netzwerkquelle bereitstellt, muss folgende Aktionen ausführen:</span><span class="sxs-lookup"><span data-stu-id="3af0d-104">An application that provides credentials to the network source must do the following:</span></span>

1.  <span data-ttu-id="3af0d-105">Implementieren Sie ein Anmelde Informationen Manager-Objekt, das die [**IMF netkredentialmanager**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredentialmanager) -Schnittstelle verfügbar macht.</span><span class="sxs-lookup"><span data-stu-id="3af0d-105">Implement a credential manager object that exposes the [**IMFNetCredentialManager**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredentialmanager) interface.</span></span>
2.  <span data-ttu-id="3af0d-106">Erstellen Sie vor dem Erstellen der Netzwerkquelle einen neuen Eigenschaften Speicher.</span><span class="sxs-lookup"><span data-stu-id="3af0d-106">Before you create the network source, create a new property store.</span></span>
3.  <span data-ttu-id="3af0d-107">Legen Sie die Eigenschaft "MF-Anmelde Informations [**\_ \_ Verwaltung**](mfnetsource-credential-manager-property.md) " für den Eigenschaften Speicher fest.</span><span class="sxs-lookup"><span data-stu-id="3af0d-107">Set the [**MFNETSOURCE\_CREDENTIAL\_MANAGER**](mfnetsource-credential-manager-property.md) property on the property store.</span></span> <span data-ttu-id="3af0d-108">Der Wert der-Eigenschaft ist ein Zeiger auf die [**imfnetkredentialmanager**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredentialmanager) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="3af0d-108">The value of the property is a pointer to the [**IMFNetCredentialManager**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredentialmanager) interface.</span></span>
4.  <span data-ttu-id="3af0d-109">Übergeben Sie einen Zeiger zum Eigenschaften Speicher an den Quell Konflikt Löser, wie unter [Konfigurieren einer Medienquelle](configuring-a-media-source.md)beschrieben.</span><span class="sxs-lookup"><span data-stu-id="3af0d-109">Pass a pointer to the property store to the source resolver, as described in [Configuring a Media Source](configuring-a-media-source.md).</span></span>

<span data-ttu-id="3af0d-110">Die Netzwerk Quellen verwenden den Anmelde Informations-Manager, um Benutzer Anmelde Informationen zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="3af0d-110">The network sources uses the credential manager to get user credentials.</span></span> <span data-ttu-id="3af0d-111">Wenn die Netzwerkquelle Anmelde Informationen für den Zugriff auf eine Netzwerkressource erfordert, ruft Sie die [**imfnetkredentialmanager:: begingetanmeldeinformationen**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialmanager-begingetcredentials) -Methode der Anwendung auf.</span><span class="sxs-lookup"><span data-stu-id="3af0d-111">If the network source requires credentials to access a network resource, it calls the application's [**IMFNetCredentialManager::BeginGetCredentials**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialmanager-begingetcredentials) method.</span></span> <span data-ttu-id="3af0d-112">Dieser-Befehl startet eine asynchrone Anforderung, um die Anmelde Informationen des Benutzers abzurufen.</span><span class="sxs-lookup"><span data-stu-id="3af0d-112">This call starts an asynchronous request to gets the user's credentials.</span></span> <span data-ttu-id="3af0d-113">Die **begingetcredensmethode** kann die Anmelde Informationen entweder aus dem Anmelde Informations Cache oder vom Benutzer erhalten.</span><span class="sxs-lookup"><span data-stu-id="3af0d-113">The **BeginGetCredentials** method can get the credentials either from the credential cache or from the user.</span></span> <span data-ttu-id="3af0d-114">Anmelde Informationen werden in einem *Anmelde Informationen-Objekt* gespeichert.</span><span class="sxs-lookup"><span data-stu-id="3af0d-114">Credentials are stored in a *credential object*.</span></span> <span data-ttu-id="3af0d-115">Wenn der Vorgang beendet ist, ruft die Anwendung die Rückruf Schnittstelle auf, um die Netzwerkquelle zu benachrichtigen.</span><span class="sxs-lookup"><span data-stu-id="3af0d-115">When the operation is complete, the application invokes the callback interface to notify the network source.</span></span> <span data-ttu-id="3af0d-116">Die Netzwerkquelle ruft [**imfnetkredentialmanager:: endgetanmelde**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialmanager-endgetcredentials) Informationen auf, um den asynchronen Vorgang abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="3af0d-116">The network source calls [**IMFNetCredentialManager::EndGetCredentials**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialmanager-endgetcredentials) to complete the asynchronous operation.</span></span>

<span data-ttu-id="3af0d-117">Da dies ein asynchroner Vorgang ist, muss die Anwendung den Rückruf am Ende des Vorgangs senden.</span><span class="sxs-lookup"><span data-stu-id="3af0d-117">Because this is an asynchronous operation, the application must dispatch the callback at the end of the operation.</span></span> <span data-ttu-id="3af0d-118">Schritt-für-Schritt-Anleitungen zum Schreiben einer asynchronen Methode finden Sie unter [Schreiben einer asynchronen Methode](writing-an-asynchronous-method.md).</span><span class="sxs-lookup"><span data-stu-id="3af0d-118">For step-by-step instructions about writing an asynchronous method, see [Writing an Asynchronous Method](writing-an-asynchronous-method.md).</span></span>

<span data-ttu-id="3af0d-119">Im folgenden Beispiel wird gezeigt, wie die Eigenschaft " [**mfnetsource \_ Credential \_ Manager**](mfnetsource-credential-manager-property.md) " in der Netzwerkquelle festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="3af0d-119">The following example shows how to set the [**MFNETSOURCE\_CREDENTIAL\_MANAGER**](mfnetsource-credential-manager-property.md) property on the network source.</span></span>


```C++
// Creates a media source from a URL.
//
// Demonstrates how to set a credential manager on the network source.

HRESULT CreateMediaSourceWithCredentialManager(
    PCWSTR pszURL, 
    IMFMediaSource **ppSource
    )
{
    IPropertyStore *pConfig = NULL;

    CCredentialManager *pCredentials = new (std::nothrow) CCredentialManager();

    if (pCredentials == NULL)
    {
        return E_OUTOFMEMORY;
    }

    // Configure the property store.
    HRESULT hr = PSCreateMemoryPropertyStore(IID_PPV_ARGS(&pConfig));

    if (SUCCEEDED(hr))
    {
        PROPERTYKEY key;
        key.fmtid =  MFNETSOURCE_CREDENTIAL_MANAGER;
        key.pid = 0;

        PROPVARIANT var;
        var.vt = VT_UNKNOWN;
        pCredentials->QueryInterface(IID_PPV_ARGS(&var.punkVal));

        hr = pConfig->SetValue(key, var);

        PropVariantClear(&var);
    }

    // Create the source media source.
    if (SUCCEEDED(hr))
    {
        hr = CreateMediaSource(pszURL, pConfig, ppSource);
    }

    SafeRelease(&pConfig);
    SafeRelease(&pCredentials);

    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="3af0d-120">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="3af0d-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3af0d-121">Netzwerk Quellen Authentifizierung</span><span class="sxs-lookup"><span data-stu-id="3af0d-121">Network Source Authentication</span></span>](network-source-authentication.md)
</dt> </dl>

 

 



