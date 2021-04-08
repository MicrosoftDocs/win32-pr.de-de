---
description: Nachdem Sie die Sicherheitsstufen für Ihren IWbemServices-Zeiger festgelegt haben, können Sie auf die verschiedenen Funktionen von WMI zugreifen. Nachdem Sie die Verwendung von WMI abgeschlossen haben, müssen Sie die Anwendung Herunterfahren.
ms.assetid: 32bc7dd8-cb05-4354-bf46-f4359ac1f0d8
ms.tgt_platform: multiple
title: Bereinigen und Herunterfahren einer WMI-Anwendung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7758cbdba81e018ff3362cec86aa5096838dc9e0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960223"
---
# <a name="cleaning-up-and-shutting-down-a-wmi-application"></a>Bereinigen und Herunterfahren einer WMI-Anwendung

Nachdem Sie die Sicherheitsstufen für Ihren [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) -Zeiger festgelegt haben, können Sie auf die verschiedenen Funktionen von WMI zugreifen. Nachdem Sie die Verwendung von WMI abgeschlossen haben, müssen Sie die Anwendung Herunterfahren.

Im folgenden Verfahren wird beschrieben, wie Sie eine WMI-Anwendung bereinigen und Herunterfahren.

**So können Sie eine WMI-Anwendung bereinigen und Herunterfahren**

1.  Freigeben beliebiger offener com-Schnittstellen.

    Die beiden primären Schnittstellen, die Sie sich merken müssen, sind [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) und [**IWBEMLocator**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemlocator).

2.  [**CallInitialize**](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize)aufruft.

    Wie bei allen com-Anwendungen müssen Sie " [**zählinitialize**](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize) " am Ende der Anwendung anfügen.

3.  Beenden Sie die Anwendung.

    Im folgenden Codebeispiel wird gezeigt, wie eine WMI-Client Anwendung beendet wird.

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
    > Die `pSvc` Variable ist vom Typ [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) \* , und die ploc-Variable ist vom Typ [**IWBEMLocator**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemlocator) \* .

     

Sie haben nun erfolgreich com initialisiert, auf WMI zugegriffen und die Anwendung beendet. Weitere Informationen finden Sie unter [Beispiel: Erstellen einer WMI-Anwendung](example-creating-a-wmi-application.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Erstellen einer WMI-Anwendung mithilfe von C++](creating-a-wmi-application-using-c-.md)
</dt> </dl>

 

 
