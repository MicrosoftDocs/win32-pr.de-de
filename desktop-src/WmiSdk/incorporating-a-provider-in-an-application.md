---
description: Beschreibt, wie der WMI-com-Anbieter als Komponente in einer Anwendung statt in den Prozess in WMI eingeschlossen wird. Dies wird als entkoppelter Anbieter bezeichnet und ist der empfohlene Typ des WMI-com-Anbieters, der für Windows 2000 und spätere Betriebssysteme erstellt werden soll.
ms.assetid: a502f0dd-9add-4ebd-bc25-743a55eb78ac
ms.tgt_platform: multiple
title: Einbinden eines Anbieters in eine Anwendung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb544cd3b04cc75cef026bb2e4d2e579b8dbf135
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104555651"
---
# <a name="incorporating-a-provider-in-an-application"></a>Einbinden eines Anbieters in eine Anwendung

Beim Erstellen einer Anwendung, die instrumentiert werden soll, besteht die bewährte Vorgehensweise darin, den Anbieter als Komponente in die Anwendung selbst einzubeziehen. Mit dieser Vorgehensweise können Windows-Verwaltungsinstrumentation (WMI) direkt anstelle von indirekt über die Programm-API mit dem Dienstanbieter interagieren. Wenn der Anbieter von WMI entkoppelt wird, wird die Anwendung auch von der Lebensdauer des Anbieters anstatt von WMI gesteuert. Weitere Informationen zum Schreiben eines Anbieters, der im WMI-Prozess ausgeführt wird, finden [Sie unter Bereitstellen von Daten für WMI durch Schreiben eines Anbieters](supplying-data-to-wmi-by-writing-a-provider.md). Weitere Informationen zum Hostingmodell und den Sicherheitseinstellungen für den Anbieter finden Sie unter [Anbieter Hosting und-Sicherheit](provider-hosting-and-security.md).

Das folgende Diagramm veranschaulicht die Beziehung zwischen WMI, einem entkoppelten Anbieter und einer Anwendung.

![Beziehung zwischen WMI, entkoppelten Anbieter und Anwendung](images/decoupledprov.png)

Weitere Informationen über entkoppelte Anbieter Methoden finden Sie unter [**iwbementkopppledregistrar**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemdecoupledregistrar) und [**iwbementkopppledbasiceventprovider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemdecoupledbasiceventprovider).

> [!Note]  
> Der entkoppelte Anbieter unterstützt Instanz, Methode, Ereignis Anbieter und Ereignisconsumer. Klassen-und Eigenschaften Anbieter werden nicht unterstützt. Weitere Informationen finden Sie unter [Schreiben eines Klassen Anbieters](writing-a-class-provider.md) und [Schreiben eines Eigenschafts Anbieters](writing-a-property-provider.md).

 

Die Codebeispiele in diesem Thema erfordern die folgenden Verweise und \# include-Anweisungen, um ordnungsgemäß zu kompilieren.


```C++
#define _WIN32_DCOM
#include <iostream>
using namespace std;
#include <comdef.h>
#include <wbemidl.h>
#pragma comment(lib, "wbemuuid.lib")
```



Im folgenden Verfahren werden C++-Codebeispiele verwendet, um zu beschreiben, wie ein entkoppelter Anbieter in Ihre Anwendung integriert wird. Die Initialisierungs Methode der Anwendung führt die folgenden Schritte aus, damit WMI nur mit einem registrierten entkoppelten Anbieter interagiert.

**So implementieren Sie einen entkoppelten Anbieter in einer C++-Anwendung**

1.  Initialisieren Sie die com-Bibliothek für die Verwendung durch den aufrufenden Thread.

    Im folgenden Codebeispiel wird gezeigt, wie die com-Bibliothek initialisiert wird.

    ```C++
    HRESULT hr = S_OK ;
    hr = CoInitializeEx (0, COINIT_MULTITHREADED );
    ```

    

2.  Legen Sie die standardmäßige Prozess Sicherheitsstufe fest.

    Auf dieser Ebene wird die Sicherheitsstufe festgelegt, die von anderen Prozessen zum Zugreifen auf die Informationen des Client Prozesses erforderlich ist. Die Authentifizierungs Ebene sollte standardmäßig auf RPC- \_ C- \_ authn- \_ Ebene eingestellt sein \_ . Weitere Informationen finden Sie unter Verwalten der [WMI-Sicherheit](maintaining-wmi-security.md).

    Im folgenden Codebeispiel wird gezeigt, wie die Standard Sicherheitsstufe festgelegt wird.

    ```C++
    hr = CoInitializeSecurity (NULL, 
        -1, 
        NULL, 
        NULL,
        RPC_C_AUTHN_LEVEL_DEFAULT,
        RPC_C_IMP_LEVEL_IMPERSONATE,
        NULL, 
        EOAC_DYNAMIC_CLOAKING, 
        NULL);

    if (FAILED(hr))
    {
      CoUninitialize();
      cout << "Failed to initialize security. Error code = 0x"
           << hex << hr << endl;
      return;
    }
    ```

    

3.  Registrieren Sie die entkoppelte Anbieter-Registrierungsstelle.

    Im folgenden Codebeispiel wird gezeigt, wie die entkoppelte Anbieter Registrierungsstelle registriert wird.

    ```C++
    CLSID CLSID_WbemDecoupledRegistrar;
    IID IID_IWbemDecoupledRegistrar;
    IWbemDecoupledRegistrar *myRegistrar = NULL;

    hr = CoCreateInstance(CLSID_WbemDecoupledRegistrar,
                          NULL,
                          CLSCTX_INPROC_SERVER,
                          IID_IWbemDecoupledRegistrar,
                          (void**)&myRegistrar);
    if (SUCCEEDED(hr))
    {
        IUnknown *pIUnknown = NULL;
        // CMyProv is the class added for WMI instance / event provider
        HRESULT hr = CMyProv::CreateInstance(NULL,&pIUnknown);
        if ( SUCCEEDED(hr))
        {
            hr = myRegistrar->Register(0,
                NULL,
                NULL,
                NULL,
                L"root\\cimv2",
                L"DecoupledInstanceProvider",
                pIUnknown);

                pIUnknown->Release();
        }
    }

    if (FAILED (hr))
    {
        if ( myRegistrar )
        {
            myRegistrar->Release () ;
        }
    }
    ```

    

4.  Registrieren Sie den entkoppelten Ereignis Anbieter.

    Im folgenden Codebeispiel wird gezeigt, wie der entkoppelte Ereignis Anbieter registriert wird.

    ```C++
    IWbemDecoupledBasicEventProvider *myEvtRegistrar;

    // -- Create an instance of IWbemDecoupledEventProvider
    hr = CoCreateInstance(CLSID_WbemDecoupledBasicEventProvider,
                          NULL,
                          CLSCTX_INPROC_SERVER,
                          IID_IWbemDecoupledBasicEventProvider,
                          (void**)&myEvtRegistrar);

    if (SUCCEEDED(hr))
    {
       // -- Register the DecoupledEventProvider
       hr = myEvtRegistrar->Register(0,
                                     NULL,
                                     NULL,
                                     L"root\\cimv2",
                                     L"DecoupledEventProvider",
                                     NULL, NULL);
       if (SUCCEEDED(hr))
       {
          IWbemServices *pService = NULL;
          hr = myEvtRegistrar->GetService (0, NULL, &pService);
          if (SUCCEEDED(hr))
          {
             IWbemObjectSink *pSink = NULL;
             hr = myEvtRegistrar->GetSink ( 0, NULL, &pSink );
             if (SUCCEEDED(hr))
             {
                // Provide events
             }
          }
       } 
    }
    ```

    

5.  Führen [Sie die Aufrufe von WMI](making-calls-to-wmi.md) durch die Funktionalität des Anbieters aus. Weitere Informationen finden Sie unter Bearbeiten von [Klassen-und Instanzinformationen](manipulating-class-and-instance-information.md). Weitere Informationen, wenn der Anbieter eine Anforderung für Daten von einem Skript oder einer Anwendung verarbeitet, finden Sie unter Annehmen der Identität [eines Clients](impersonating-a-client.md).

Unmittelbar vor dem beenden muss die Anwendung nach selbst bereinigt werden. Im folgenden Verfahren wird beschrieben, wie die Registrierung des entkoppelten Anbieters aufgehoben wird, damit von WMI keine Informationen abgefragt werden können.

Im folgenden Verfahren wird beschrieben, wie die Registrierung des entkoppelten Anbieters aufgehoben wird.

**So heben Sie die Registrierung des entkoppelten Anbieters auf**

1.  Aufheben der Registrierung und Freigeben der Registrierungsstelle

    Im folgenden Codebeispiel wird gezeigt, wie die Registrierung aufgehoben und die Registrierungsstelle freigegeben wird.

    ```C++
    myRegistrar->UnRegister();
    myRegistrar->Release();
    ```

    

2.  Aufheben der Registrierung und Freigeben des Ereignis Anbieters.

    Im folgenden Codebeispiel wird gezeigt, wie die Registrierung aufgehoben und der Ereignis Anbieter freigegeben wird.

    ```C++
    myEvtRegistrar->UnRegister();
    myEvtRegistrar->Release();
    ```

    

3.  Bereinigen Sie den com-Server.

    Im folgenden Codebeispiel wird gezeigt, wie die Initialisierung der com-Bibliothek initialisiert wird.

    ```C++
    CoUninitialize();
    ```

    

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Festlegen von namepace-Sicherheits Deskriptoren](setting-namespace-security-descriptors.md)
</dt> <dt>

[Sichern Ihres Anbieters](securing-your-provider.md)
</dt> <dt>

[Entwickeln eines WMI-Anbieters](developing-a-wmi-provider.md)
</dt> </dl>

 

 



