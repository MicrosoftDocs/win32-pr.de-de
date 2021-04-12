---
title: Aufrufen von Erstellungs-Assistenten aus der Anwendung
description: Eine Anwendung oder Komponente kann dieselben Assistenten für die Erstellung von Verzeichnisdienst Objekten verwenden, die von den MMC-Snap-Ins für die Active Directory Verwaltung verwendet werden. Dies wird mit der idsadminkreateobj-Schnittstelle erreicht.
ms.assetid: be4b6101-f795-403b-b93e-960759ac4f14
ms.tgt_platform: multiple
keywords:
- Aufrufen von Erstellungs-Assistenten aus ihrer Anwendungs Anzeige
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa523d3b861d1d4a7588455b04c1a9633734253a
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/17/2020
ms.locfileid: "104472524"
---
# <a name="invoking-creation-wizards-from-your-application"></a><span data-ttu-id="7c7a9-104">Aufrufen von Erstellungs-Assistenten aus der Anwendung</span><span class="sxs-lookup"><span data-stu-id="7c7a9-104">Invoking Creation Wizards from Your Application</span></span>

<span data-ttu-id="7c7a9-105">Eine Anwendung oder Komponente kann dieselben Assistenten für die Erstellung von Verzeichnisdienst Objekten verwenden, die von den MMC-Snap-Ins für die Active Directory Verwaltung verwendet werden. Dies wird mit der [**idsadminkreateobj**](/windows/desktop/api/DSAdmin/nn-dsadmin-idsadmincreateobj) -Schnittstelle erreicht.</span><span class="sxs-lookup"><span data-stu-id="7c7a9-105">An application or component can use the same directory service object creation wizards used by the Active Directory administrative MMC snap-ins. This is accomplished with the [**IDsAdminCreateObj**](/windows/desktop/api/DSAdmin/nn-dsadmin-idsadmincreateobj) interface.</span></span>

## <a name="using-the-idsadmincreateobj-interface"></a><span data-ttu-id="7c7a9-106">Verwenden der idsadminkreateobj-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="7c7a9-106">Using the IDsAdminCreateObj Interface</span></span>

<span data-ttu-id="7c7a9-107">Eine Anwendung oder Komponente (Client) erstellt eine Instanz der [**idsadmincreateobj**](/windows/desktop/api/DSAdmin/nn-dsadmin-idsadmincreateobj) -Schnittstelle durch Aufrufen von [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) mit dem **CLSID- \_ dsadmincreateobj** -Klassen Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="7c7a9-107">An application or component (client) creates an instance of the [**IDsAdminCreateObj**](/windows/desktop/api/DSAdmin/nn-dsadmin-idsadmincreateobj) interface by calling [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) with the **CLSID\_DsAdminCreateObj** class identifier.</span></span> <span data-ttu-id="7c7a9-108">COM muss initialisiert werden, indem [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) aufgerufen wird, bevor **CoCreateInstance** aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="7c7a9-108">COM must be initialized by calling [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) before **CoCreateInstance** is called.</span></span>

<span data-ttu-id="7c7a9-109">Der Client ruft dann [**idsadminkreateobj:: Initialisieren**](/windows/desktop/api/DSAdmin/nf-dsadmin-idsadmincreateobj-initialize) auf, um das [**idsadminkreateobj**](/windows/desktop/api/DSAdmin/nn-dsadmin-idsadmincreateobj) -Objekt zu initialisieren.</span><span class="sxs-lookup"><span data-stu-id="7c7a9-109">The client then calls [**IDsAdminCreateObj::Initialize**](/windows/desktop/api/DSAdmin/nf-dsadmin-idsadmincreateobj-initialize) to initialize the [**IDsAdminCreateObj**](/windows/desktop/api/DSAdmin/nn-dsadmin-idsadmincreateobj) object.</span></span> <span data-ttu-id="7c7a9-110">**Idsadminkreateobj:: Initialize** akzeptiert einen [**IADsContainer**](/windows/desktop/api/iads/nn-iads-iadscontainer) -Schnittstellen Zeiger, der den Container darstellt, in dem das Objekt erstellt werden soll, und den Klassennamen des zu erstellenden Objekts.</span><span class="sxs-lookup"><span data-stu-id="7c7a9-110">**IDsAdminCreateObj::Initialize** accepts an [**IADsContainer**](/windows/desktop/api/iads/nn-iads-iadscontainer) interface pointer that represents the container that the object should be created in, and the class name of the object to be created.</span></span> <span data-ttu-id="7c7a9-111">Beim Erstellen von Benutzer Objekten ist es auch möglich, ein vorhandenes Objekt anzugeben, das in das neue-Objekt kopiert wird.</span><span class="sxs-lookup"><span data-stu-id="7c7a9-111">When creating user objects, it is also possible to specify an existing object that will be copied to the new object.</span></span>

<span data-ttu-id="7c7a9-112">Wenn das [**idsadminkreateobj**](/windows/desktop/api/DSAdmin/nn-dsadmin-idsadmincreateobj) -Objekt initialisiert wurde, ruft der Client " [**idsadminkreateobj::**](/windows/desktop/api/DSAdmin/nf-dsadmin-idsadmincreateobj-createmodal) up" auf, um den Objekterstellungs-Assistenten anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="7c7a9-112">When the [**IDsAdminCreateObj**](/windows/desktop/api/DSAdmin/nn-dsadmin-idsadmincreateobj) object has been initialized, the client calls [**IDsAdminCreateObj::CreateModal**](/windows/desktop/api/DSAdmin/nf-dsadmin-idsadmincreateobj-createmodal) to display the object creation wizard.</span></span>

<span data-ttu-id="7c7a9-113">Im Gegensatz zu den meisten Klassen-und Schnittstellen Bezeichner sind **CLSID \_ dsadminkreateobj** und **IID \_ adsadminkreateobj** nicht in einer Bibliotheksdatei definiert.</span><span class="sxs-lookup"><span data-stu-id="7c7a9-113">Unlike most class and interface identifiers, **CLSID\_DsAdminCreateObj** and **IID\_ADsAdminCreateObj** are not defined in a library file.</span></span> <span data-ttu-id="7c7a9-114">Dies bedeutet, dass Sie den Speicher für diese Bezeichner in der Anwendung definieren müssen.</span><span class="sxs-lookup"><span data-stu-id="7c7a9-114">This means you must define the storage for these identifiers within your application.</span></span> <span data-ttu-id="7c7a9-115">Zu diesem Zweck müssen Sie die Datei "Initguid. h" direkt einschließen, bevor Sie "DSAdmin. h" einschließen.</span><span class="sxs-lookup"><span data-stu-id="7c7a9-115">To do this, you must include the file initguid.h immediately before including dsadmin.h.</span></span> <span data-ttu-id="7c7a9-116">Die Datei "Initguid. h" darf nur einmal in einer Anwendung eingeschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="7c7a9-116">The initguid.h file must only be included once in an application.</span></span> <span data-ttu-id="7c7a9-117">Im folgenden Codebeispiel wird gezeigt, wie Sie diese Dateien einschließen.</span><span class="sxs-lookup"><span data-stu-id="7c7a9-117">The following code example shows how to include these files.</span></span>


```C++
#include <initguid.h>
#include <dsadmin.h>
```



<span data-ttu-id="7c7a9-118">Das folgende Codebeispiel zeigt, wie die [**idsadminkreateobj**](/windows/desktop/api/DSAdmin/nn-dsadmin-idsadmincreateobj) -Schnittstelle erstellt und zum Starten des Objekterstellungs-Assistenten für ein Benutzerobjekt verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="7c7a9-118">The following code example shows how the [**IDsAdminCreateObj**](/windows/desktop/api/DSAdmin/nn-dsadmin-idsadmincreateobj) interface can be created and used to start the object creation wizard for a user object.</span></span>


```C++
//  Add activeds.lib to your project
//  Add adsiid.lib to your project

#include "stdafx.h"
#include <atlbase.h>
#include <atlstr.h>
#include "activeds.h"
#include <initguid.h> // Only include this in one source file
#include <dsadmin.h>

//  GetUserContainer() function binds to the user container
IADsContainer* GetUserContainer(void)
{
    IADsContainer *pUsers = NULL;
    HRESULT hr;
    IADs *pRoot;

    //  Bind to the rootDSE.
    hr = ADsGetObject(L"LDAP://rootDSE", IID_IADs, (LPVOID*)&pRoot);

    if(SUCCEEDED(hr))
    {
        VARIANT var;
        VariantInit(&var);
        CComBSTR sbstr(L"defaultNamingContext");

        //  Get the default naming context (domain) DN.
        hr = pRoot->Get(sbstr, &var);
        if(SUCCEEDED(hr) && (VT_BSTR == var.vt))
        {
            CStringW sstr(L"LDAP://CN=Users,");
            sstr += var.bstrVal;

            //  Bind to the User container.
            hr = ADsGetObject(sstr, IID_IADsContainer, (LPVOID*)&pUsers);

            VariantClear(&var);
        }
    }

    return pUsers;
}


//  The LaunchNewUserWizard() function launches the user wizard.
HRESULT LaunchNewUserWizard(IADs** ppAdsOut)
{
    if(NULL == ppAdsOut)
    {
        return E_INVALIDARG;
    }

    HRESULT hr;
    IDsAdminCreateObj* pCreateObj = NULL;

    hr = ::CoCreateInstance(CLSID_DsAdminCreateObj,
                            NULL, 
                            CLSCTX_INPROC_SERVER,
                            IID_IDsAdminCreateObj,
                            (void**)&pCreateObj);

    if(SUCCEEDED(hr))
    {
        IADsContainer *pContainer;

        pContainer = GetUserContainer();

        if(pContainer)
        {
            hr = pCreateObj->Initialize(pContainer, NULL, L"user");
            if(SUCCEEDED(hr))
            {
                HWND    hwndParent;

                hwndParent = GetDesktopWindow();

                hr = pCreateObj->CreateModal(hwndParent, ppAdsOut);
            }

            pContainer->Release();
        }

        pCreateObj->Release();
    }

    return hr;    
}

//  Entry point to the application
int main(void)
{
    HRESULT hr;
    IADs *pAds = NULL;

    CoInitialize(NULL);

    hr = LaunchNewUserWizard(&pAds);
    if((S_OK == hr) && (NULL != pAds))
    {
        pAds->Release();
    }

    CoUninitialize();

    return 0;
}
```



 

 