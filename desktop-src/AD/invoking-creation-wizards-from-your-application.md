---
title: Aufrufen von Erstellungs-Assistenten aus Ihrer Anwendung
description: Eine Anwendung oder Komponente kann die gleichen Assistenten zum Erstellen von Verzeichnisdienstobjekten verwenden, die von den MMC-Snap-Ins der Active Directory-Verwaltung verwendet werden. Dies wird mit der IDsAdminCreateObj-Schnittstelle erreicht.
ms.assetid: be4b6101-f795-403b-b93e-960759ac4f14
ms.tgt_platform: multiple
keywords:
- Aufrufen von Erstellungs-Assistenten aus Ihrem Anwendungs-AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba1d5f8c722e3f673d998d3baaf33b4110293c70875a68fd03e8117f667351bd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118187074"
---
# <a name="invoking-creation-wizards-from-your-application"></a>Aufrufen von Erstellungs-Assistenten aus Ihrer Anwendung

Eine Anwendung oder Komponente kann die gleichen Assistenten zum Erstellen von Verzeichnisdienstobjekten verwenden, die von den MMC-Snap-Ins der Active Directory-Verwaltung verwendet werden. Dies wird mit der [**IDsAdminCreateObj-Schnittstelle**](/windows/desktop/api/DSAdmin/nn-dsadmin-idsadmincreateobj) erreicht.

## <a name="using-the-idsadmincreateobj-interface"></a>Verwenden der IDsAdminCreateObj-Schnittstelle

Eine Anwendung oder Komponente (Client) erstellt eine Instanz der [**IDsAdminCreateObj-Schnittstelle,**](/windows/desktop/api/DSAdmin/nn-dsadmin-idsadmincreateobj) indem [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) mit dem **CLSID-Klassenbezeichner \_ DsAdminCreateObj** aufgerufen wird. COM muss durch Aufrufen von [**CoInitialize initialisiert**](/windows/win32/api/objbase/nf-objbase-coinitialize) werden, bevor **CoCreateInstance** aufgerufen wird.

Der Client ruft dann [**IDsAdminCreateObj::Initialize**](/windows/desktop/api/DSAdmin/nf-dsadmin-idsadmincreateobj-initialize) auf, um das [**IDsAdminCreateObj-Objekt**](/windows/desktop/api/DSAdmin/nn-dsadmin-idsadmincreateobj) zu initialisieren. **IDsAdminCreateObj::Initialize** akzeptiert einen [**IADsContainer-Schnittstellenzeiger,**](/windows/desktop/api/iads/nn-iads-iadscontainer) der den Container darstellt, in dem das Objekt erstellt werden soll, und den Klassennamen des zu erstellenden Objekts. Beim Erstellen von Benutzerobjekten ist es auch möglich, ein vorhandenes Objekt anzugeben, das in das neue Objekt kopiert wird.

Wenn das [**IDsAdminCreateObj-Objekt**](/windows/desktop/api/DSAdmin/nn-dsadmin-idsadmincreateobj) initialisiert wurde, ruft der Client [**IDsAdminCreateObj::CreateModal**](/windows/desktop/api/DSAdmin/nf-dsadmin-idsadmincreateobj-createmodal) auf, um den Objekterstellungs-Assistenten anzuzeigen.

Im Gegensatz zu den meisten Klassen- und Schnittstellenbezeichnern sind **CLSID \_ DsAdminCreateObj** und **IID \_ ADsAdminCreateObj** nicht in einer Bibliotheksdatei definiert. Dies bedeutet, dass Sie den Speicher für diese Bezeichner in Ihrer Anwendung definieren müssen. Hierzu müssen Sie die Datei initguid.h unmittelbar vor dem Einfügen von dsadmin.h einschließen. Die Datei initguid.h darf nur einmal in einer Anwendung enthalten sein. Das folgende Codebeispiel zeigt, wie diese Dateien eingeschlossen werden.


```C++
#include <initguid.h>
#include <dsadmin.h>
```



Das folgende Codebeispiel zeigt, wie die [**IDsAdminCreateObj-Schnittstelle**](/windows/desktop/api/DSAdmin/nn-dsadmin-idsadmincreateobj) erstellt und zum Starten des Objekterstellungs-Assistenten für ein Benutzerobjekt verwendet werden kann.


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



 

 