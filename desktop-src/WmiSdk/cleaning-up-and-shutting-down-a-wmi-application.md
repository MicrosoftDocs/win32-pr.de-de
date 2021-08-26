---
description: Nachdem Sie die Sicherheitsebenen für Ihren IWbemServices-Zeiger festgelegt haben, können Sie auf die verschiedenen Funktionen von WMI zugreifen. Nachdem Sie die Verwendung von WMI abgeschlossen haben, müssen Sie Die Anwendung herunterfahren.
ms.assetid: 32bc7dd8-cb05-4354-bf46-f4359ac1f0d8
ms.tgt_platform: multiple
title: Bereinigen und Herunterfahren einer WMI-Anwendung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 296d2093b16491bcb600438d781fa833a09754fdc5d0cc8cc83feb710a6d2727
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120120910"
---
# <a name="cleaning-up-and-shutting-down-a-wmi-application"></a>Bereinigen und Herunterfahren einer WMI-Anwendung

Nachdem Sie die Sicherheitsebenen für Ihren [**IWbemServices-Zeiger**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) festgelegt haben, können Sie auf die verschiedenen Funktionen von WMI zugreifen. Nachdem Sie die Verwendung von WMI abgeschlossen haben, müssen Sie Die Anwendung herunterfahren.

Im folgenden Verfahren wird beschrieben, wie Sie eine WMI-Anwendung bereinigt und herunterfahren.

**So bereinigt und herunterfahren Sie eine WMI-Anwendung**

1.  Lassen Sie alle geöffneten COM-Schnittstellen frei.

    Die beiden primären Schnittstellen, die Sie veröffentlichen müssen, sind [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) und [**IWbemLocator.**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemlocator)

2.  Rufen Sie [**CoUninitialize auf.**](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize)

    Wie bei allen COM-Anwendungen müssen Sie [**CoUninitialize am**](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize) Ende Ihrer Anwendung aufrufen.

3.  Beenden Sie Ihre Anwendung.

    Das folgende Codebeispiel zeigt, wie eine WMI-Clientanwendung beendet wird.

    ```C++
        // The following #include and #define statements need
        // to be used with this code:
        // #define _WIN32_DCOM
        // #include <wbemidl.h>  
        // #pragma comment(lib, "wbemuuid.lib")
        
        // pSvc was declared as IWbemServices *pSvc;
        // pLoc was declared as IWbemLocator *pLoc;

        pSvc->Release();
        pLoc->Release();     
        CoUninitialize();
        return 0;   // Program successfully completed.
    ```

    

    > [!Note]  
    > Die `pSvc` Variable ist vom Typ [**IWbemServices,**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) \* und die pLoc-Variable ist vom Typ [**IWbemLocator.**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemlocator) \*

     

Sie haben com nun erfolgreich initialisiert, auf WMI zugegriffen und Ihre Anwendung beendet. Weitere Informationen finden Sie unter [Beispiel: Erstellen einer WMI-Anwendung](example-creating-a-wmi-application.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Erstellen einer WMI-Anwendung mit C++](creating-a-wmi-application-using-c-.md)
</dt> </dl>

 

 
