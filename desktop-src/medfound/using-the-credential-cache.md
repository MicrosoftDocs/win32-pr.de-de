---
description: Verwenden des Anmelde Informations Caches
ms.assetid: b58d0a6e-ecae-48a1-a3af-d4246caa272b
title: Verwenden des Anmelde Informations Caches
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d512d0bab8f45f50a587e3c8eda2a73c4832685f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106356842"
---
# <a name="using-the-credential-cache"></a><span data-ttu-id="fa5ee-103">Verwenden des Anmelde Informations Caches</span><span class="sxs-lookup"><span data-stu-id="fa5ee-103">Using the Credential Cache</span></span>

<span data-ttu-id="fa5ee-104">Media Foundation stellt eine Standard Implementierung der [**IMF netkredentialcache**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredentialcache) -Schnittstelle bereit.</span><span class="sxs-lookup"><span data-stu-id="fa5ee-104">Media Foundation provides a default implementation of the [**IMFNetCredentialCache**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredentialcache) interface.</span></span> <span data-ttu-id="fa5ee-105">Eine Anwendung, die die [**imfnetkredentialmanager**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredentialmanager) -Schnittstelle implementiert, kann das standardmäßige Anmelde Informations Cache-Objekt verwenden, um die Anmelde Informationen des Benutzers zu speichern.</span><span class="sxs-lookup"><span data-stu-id="fa5ee-105">An application that implements the [**IMFNetCredentialManager**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredentialmanager) interface can use the default credential cache object to store the user's credentials.</span></span>

<span data-ttu-id="fa5ee-106">Um das standardmäßige Cache Objekt für Anmelde Informationen zu erstellen, rufen Sie die [**mfkreatecredentialcache**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatecredentialcache) -Funktion auf.</span><span class="sxs-lookup"><span data-stu-id="fa5ee-106">To create the default credential cache object, call the [**MFCreateCredentialCache**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatecredentialcache) function.</span></span>


```C++
HRESULT hr = S_OK;
IMFNetCredentialCache *pCredentialCache = NULL;
hr = MFCreateCredentialCache(&pCredentialCache);
```



<span data-ttu-id="fa5ee-107">Nachdem der Anmelde Informations Cache erstellt wurde, kann die Anwendung die folgenden Methoden verwenden, um ein Anmelde Informationsobjekt zu erhalten, Benutzer Anmelde Informationen festzulegen und die Cache Optionen anzugeben.</span><span class="sxs-lookup"><span data-stu-id="fa5ee-107">After the credential cache is created, the application can use the following methods to get a credential object, set user credentials, and specify the caching options.</span></span>

-   <span data-ttu-id="fa5ee-108">Um das Anmelde Informationen-Objekt für eine URL abzurufen, wenden Sie [**imfnetkredentialcache:: GetCredential**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialcache-getcredential)an.</span><span class="sxs-lookup"><span data-stu-id="fa5ee-108">To get the credential object for a URL, call [**IMFNetCredentialCache::GetCredential**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialcache-getcredential).</span></span>

    ```C++
    hr = pCredentialCache-> GetCredential(
            pszUrl,
            pszRealm,
            dwAuthenticationFlags,
            &pCredential,
            &dwRequirementsFlags);
    ```

    

    <span data-ttu-id="fa5ee-109">Wenn die Anmelde Informationen für die angegebene URL im Anmelde Informations Cache nicht vorhanden sind, erstellt [**GetCredential**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialcache-getcredential) ein neues Anmelde Informationsobjekt mit leeren Benutzernamen-und Kenn Wort Werten.</span><span class="sxs-lookup"><span data-stu-id="fa5ee-109">If the credentials for the specified URL do not exist in the credential cache, [**GetCredential**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialcache-getcredential) creates a new credential object with empty user name and password values.</span></span>

-   <span data-ttu-id="fa5ee-110">Um den Benutzernamen und das Kennwort für das Anmelde Informationen-Objekt festzulegen, rufen Sie [**imfnetcredential:: SETUSER**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredential-setuser) und [**imfnetcredential:: SetPassword**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredential-setpassword)auf.</span><span class="sxs-lookup"><span data-stu-id="fa5ee-110">To set the user name and password on the credential object, call [**IMFNetCredential::SetUser**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredential-setuser) and [**IMFNetCredential::SetPassword**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredential-setpassword).</span></span>
-   <span data-ttu-id="fa5ee-111">Um die Cache Optionen für das Anmelde Informationen-Objekt festzulegen, rufen Sie [**imfnetkredentialcache:: setuseroptions**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialcache-setuseroptions)auf.</span><span class="sxs-lookup"><span data-stu-id="fa5ee-111">To set the caching options on the credential object, call [**IMFNetCredentialCache::SetUserOptions**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialcache-setuseroptions).</span></span>

    ```C++
    hr = pCredentialCache-> SetUserOptions( 
            pCredentialCache,
            MFNET_CREDENTIAL_SAVE);
    ```

    

    <span data-ttu-id="fa5ee-112">Die *dwoptionsflags* -Parameterwerte werden in der [**MF netkredentialoptions**](/windows/desktop/api/mfidl/ne-mfidl-mfnetcredentialoptions) -Enumeration definiert.</span><span class="sxs-lookup"><span data-stu-id="fa5ee-112">The *dwOptionsFlags* parameter values are defined in the [**MFNetCredentialOptions**](/windows/desktop/api/mfidl/ne-mfidl-mfnetcredentialoptions) enumeration.</span></span> <span data-ttu-id="fa5ee-113">Um Benutzer Anmelde Informationen für eine URL in einem permanenten Speicher zu speichern, legen Sie das kennflag für die mfnet-Anmelde Informationen fest \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="fa5ee-113">To save user credentials for a URL in a persistent storage, set the MFNET\_CREDENTIAL\_SAVE flag.</span></span> <span data-ttu-id="fa5ee-114">Wenn der [**setuseroptions**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialcache-setuseroptions) -Befehl erfolgreich abgeschlossen wird, sucht der nachfolgende [**GetCredential**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialcache-getcredential) -Rückruf nach den Anmelde Informationen im persistenten Speicher.</span><span class="sxs-lookup"><span data-stu-id="fa5ee-114">If the [**SetUserOptions**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialcache-setuseroptions) call completes successfully, then the subsequent call to [**GetCredential**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialcache-getcredential) searches for the credentials in the persistent storage.</span></span> <span data-ttu-id="fa5ee-115">Wenn eine Entsprechung gefunden wird, gibt diese Methode einen Zeiger auf das Anmelde Informationen-Objekt zurück, das die Informationen enthält.</span><span class="sxs-lookup"><span data-stu-id="fa5ee-115">If a match is found, this method returns a pointer to the credential object that contains the information.</span></span>

    <span data-ttu-id="fa5ee-116">Standardmäßig werden Benutzer Anmelde Informationen verschlüsselt, die über das Netzwerk gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="fa5ee-116">By default, user credentials sent over the network are encrypted.</span></span> <span data-ttu-id="fa5ee-117">Um dies in Klartext zu ändern, legen Sie das Flag für die mfnet-Anmelde Informationen \_ \_ Allow \_ Clear \_ Text fest.</span><span class="sxs-lookup"><span data-stu-id="fa5ee-117">To change this to clear text, set the MFNET\_CREDENTIAL\_ALLOW\_CLEAR\_TEXT flag.</span></span>

    <span data-ttu-id="fa5ee-118">Rufen Sie zum Entfernen von Informationen aus der Registrierung [**GetCredential**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialcache-getcredential) auf, um das Anmelde Informationen-Objekt abzurufen, und rufen Sie dann [**setuseroption**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialcache-setuseroptions) auf, und legen Sie *dwoptionsflags* auf mfnet \_ Anmelde Informationen \_ Not \_ Cache fest.</span><span class="sxs-lookup"><span data-stu-id="fa5ee-118">To remove information from the registry, call [**GetCredential**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialcache-getcredential) to get the credential object, and then call [**SetUserOption**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialcache-setuseroptions) and set *dwOptionsFlags* to MFNET\_CREDENTIAL\_DONT\_CACHE.</span></span>

## <a name="related-topics"></a><span data-ttu-id="fa5ee-119">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="fa5ee-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fa5ee-120">Netzwerk Quellen Authentifizierung</span><span class="sxs-lookup"><span data-stu-id="fa5ee-120">Network Source Authentication</span></span>](network-source-authentication.md)
</dt> </dl>

 

 



