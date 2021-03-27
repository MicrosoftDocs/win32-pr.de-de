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
# <a name="how-to-use-autoplay-events-in-running-applications"></a>Verwenden von AutoPlay-Ereignissen in laufenden Anwendungen

Die [**ihweventhandler**](/windows/desktop/api/Shobjidl/nn-shobjidl-ihweventhandler) -Schnittstelle kann in der Running Object Table (rot) registriert werden, damit die Ausführung von Anwendungen auf AutoPlay-Ereignisse zugreifen kann.

In den folgenden Anweisungen wird beschrieben, wie Sie Autoplay-Ereignisse in Ausführung von-Anwendungen verwenden.

## <a name="instructions"></a>Instructions

### <a name="step-1"></a>Schritt 1:

Erstellen Sie eine neue-Komponente, die die [**ihweventhandler**](/windows/desktop/api/Shobjidl/nn-shobjidl-ihweventhandler) -Schnittstelle implementiert.

### <a name="step-2"></a>Schritt 2:

Initialisieren Sie die neue Komponente mit dem initcmdline-Wert aus dem Eintrag eines bestimmten **Handlers** unter dem Handler-Schlüssel.

Dieser Schritt ist erforderlich, da die Methode "Initialize" nicht von der automatischen Wiedergabe aufgerufen wird.

### <a name="step-3"></a>Schritt 3:

Aufrufen der Funktion " [**reatehardwareeventmoniker**](createhardwareeventmoniker.md) ", um einen Moniker zu erhalten, der die Komponente und den Ereignishandler darstellt, den Sie aufrufen möchten.

### <a name="step-4"></a>Schritt 4:

Verwenden Sie den *ppmoniker* -Parameter, um die Komponente in der rot zu registrieren.

## <a name="remarks"></a>Bemerkungen

> [!Note]  
> [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) kann Sicherheitsrisiken darstellen. Informationen zum ordnungsgemäßen Laden von DLLs mit unterschiedlichen Versionen von Windows finden Sie in der Dokumentation zu **LoadLibrary** .

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

Für den Aufrufen von " [**ununningobjec\:: Register**](/windows/win32/api/objidl/nf-objidl-irunningobjecttable-register) " ist es erforderlich, dass die Komponente über die folgenden **AppID** -Informationen in der Registrierung verfügt.

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

[**Ihweventhandler**](/windows/desktop/api/Shobjidl/nn-shobjidl-ihweventhandler)

[**"Kreatehardwareeventmoniker"**](createhardwareeventmoniker.md)
