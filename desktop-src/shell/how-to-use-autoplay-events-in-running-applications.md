---
description: Die IHWEventHandler-Schnittstelle kann in der laufenden Objekttabelle (Running Object Table, ROT) registriert werden, damit ausgeführte Anwendungen Zugriff auf AutoPlay-Ereignisse haben.
ms.assetid: 6FEFFB5D-DD8B-4FEA-B273-D32FC30CAFEA
title: Verwenden von AutoPlay-Ereignissen in ausgeführten Anwendungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab30fa020b5501f8832a5b350ad409934ecbb4258d75adf147e908c699516474
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119714816"
---
# <a name="how-to-use-autoplay-events-in-running-applications"></a>Verwenden von AutoPlay-Ereignissen in ausgeführten Anwendungen

Die [**IHWEventHandler-Schnittstelle**](/windows/desktop/api/Shobjidl/nn-shobjidl-ihweventhandler) kann in der laufenden Objekttabelle (Running Object Table, ROT) registriert werden, damit ausgeführte Anwendungen Zugriff auf AutoPlay-Ereignisse haben.

In den folgenden Anweisungen wird beschrieben, wie AutoPlay-Ereignisse in ausgeführten Anwendungen verwendet werden.

## <a name="instructions"></a>Anweisungen

### <a name="step-1"></a>Schritt 1:

Erstellen Sie eine neue Komponente, die die [**IHWEventHandler-Schnittstelle**](/windows/desktop/api/Shobjidl/nn-shobjidl-ihweventhandler) implementiert.

### <a name="step-2"></a>Schritt 2:

Initialisieren Sie die neue Komponente mit dem InitCmdLine-Wert aus dem Eintrag des **jeweiligen** Handlers unter dem Handlerschlüssel.

Dieser Schritt ist erforderlich, da die automatische Wiedergabe die Initialize-Methode nicht aufruft.

### <a name="step-3"></a>Schritt 3:

Rufen Sie die [**CreateHardwareEventMoniker-Funktion**](createhardwareeventmoniker.md) auf, um einen Moniker abzurufen, der Ihre Komponente und den Ereignishandler darstellt, den Sie aufrufen möchten.

### <a name="step-4"></a>Schritt 4:

Verwenden Sie den *ppmoniker-Parameter,* um Ihre Komponente im ROT zu registrieren.

## <a name="remarks"></a>Hinweise

> [!Note]  
> [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) kann Sicherheitsrisiken darstellen. Informationen zum ordnungsgemäßen Laden von DLLs mit verschiedenen Versionen von Windows finden Sie in der **LoadLibrary-Dokumentation.**

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

Der Aufruf von [**IRunningObjectTable::Register**](/windows/win32/api/objidl/nf-objidl-irunningobjecttable-register) erfordert, dass die Komponente über die folgenden **AppID-Informationen** in der Registrierung verfügt.

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

## <a name="related-topics"></a>Zugehörige Themen

[**IHWEventHandler**](/windows/desktop/api/Shobjidl/nn-shobjidl-ihweventhandler)

[**CreateHardwareEventMoniker**](createhardwareeventmoniker.md)
