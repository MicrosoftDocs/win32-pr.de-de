---
description: Windows-Verwaltungsinstrumentation (WMI) kann die Senke erstellen, um asynchrone Rückrufe für eine Client Anwendung in einem separaten Prozess zu empfangen.
ms.assetid: 3d3111ac-7d83-48d6-94e4-36cb46a506fa
ms.tgt_platform: multiple
title: Verringern der Sicherheit für eine Senke in einem separaten Prozess
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63aec8bcb451d254961acae8278cb45cb4454f37
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106358585"
---
# <a name="lowering-the-security-for-a-sink-in-a-separate-process"></a>Verringern der Sicherheit für eine Senke in einem separaten Prozess

Windows-Verwaltungsinstrumentation (WMI) kann die Senke erstellen, um asynchrone Rückrufe für eine Client Anwendung in einem separaten Prozess zu empfangen. Der separate Prozess ist Unsecapp.exe. Verwenden Sie die [**iwbemunsecuder**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemunsecuredapartment) -Schnittstelle. Mit **iwbemunsecuredapartment** können Sie steuern, ob Unsecapp.exe Rückrufe für die Senke authentifiziert. Weitere Informationen finden Sie unter [Festlegen der Sicherheit für einen asynchronen](setting-security-on-an-asynchronous-call.md)-Befehl.

Anschließend können Sie die Sicherheit für diesen Prozess verringern, und WMI kann ohne Einschränkung auf die Senke zugreifen. Zur Unterstützung dieser Technik stellt WMI den Unsecapp.exe Prozess bereit, der als separater Prozess fungiert. Sie können Unsecapp.exe hosten, indem Sie die [**iunsecuredapartment**](/windows/desktop/api/Wbemcli/nn-wbemcli-iunsecuredapartment) -Schnittstelle abrufen.

Die [**iunsecumenpartment**](/windows/desktop/api/Wbemcli/nn-wbemcli-iunsecuredapartment) -Schnittstelle ermöglicht es einer Client Anwendung, einen separaten dedizierten Prozess zu erstellen, der Unsecapp.exe zum Hosting einer [**iwbebobjectsink**](iwbemobjectsink.md) -Implementierung ausgeführt wird. Der dedizierte Prozess kann [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) aufrufen, um den WMI-Zugriff auf den dedizierten Prozess zu gewähren, ohne die Sicherheit des Haupt Prozesses zu beeinträchtigen. Nach der Initialisierung fungiert der dedizierte Prozess als Vermittler zwischen dem Hauptprozess und WMI.

Im folgenden Verfahren wird beschrieben, wie ein asynchroner-Befehl mit [**iunsecuredapartment**](/windows/desktop/api/Wbemcli/nn-wbemcli-iunsecuredapartment)durchgeführt wird.

**So führen Sie einen asynchronen aufrufsbefehl mit iunsecuredapartment aus**

1.  Erstellen Sie einen dedizierten Prozess mit einem Aufrufen von [**cokreateinstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance).

    Im folgenden Codebeispiel wird [**cokreatanstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) aufgerufen, um einen dedizierten Prozess zu erstellen.

    ```C++
    IUnsecuredApartment* pUnsecApp = NULL;

    CoCreateInstance(CLSID_UnsecuredApartment, NULL, 
      CLSCTX_LOCAL_SERVER, IID_IUnsecuredApartment, 
      (void**)&pUnsecApp);
    ```

    

2.  Instanziieren Sie das sink-Objekt.

    Im folgenden Codebeispiel wird ein neues Sink-Objekt erstellt.

    ```C++
    CMySink* pSink = new CMySink;
    pSink->AddRef();
    ```

    

3.  Erstellen Sie einen Stub für die Senke.

    Ein Stub ist eine Wrapper Funktion, die von der Senke erzeugt wird.

    Im folgenden Codebeispiel wird " [**itateobjectstub**](/windows/desktop/api/Wbemcli/nf-wbemcli-iunsecuredapartment-createobjectstub) " aufgerufen, um einen Stub für die Senke zu erstellen.

    ```C++
    IUnknown* pStubUnk = NULL; 
    pUnsecApp->CreateObjectStub(pSink, &pStubUnk);
    ```

    

4.  Aufrufen von [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) für den Wrapper und Anfordern eines Zeigers auf die [**iwbemubjectsink**](iwbemobjectsink.md) -Schnittstelle.

    Im folgenden Codebeispiel wird [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) aufgerufen und ein Zeiger auf die [**iwbemubjectsink**](iwbemobjectsink.md) -Schnittstelle angefordert.

    ```C++
    IWbemObjectSink* pStubSink = NULL;
    pStubUnk->QueryInterface(IID_IWbemObjectSink, (void **)&pStubSink); pStubUnk->Release();
    ```

    

5.  Geben Sie den Sink-Objekt Zeiger frei.

    Sie können den Objekt Zeiger freigeben, da der Stub jetzt den-Zeiger besitzt.

    Im folgenden Codebeispiel wird der Senke-Objekt Zeiger freigegeben.

    ```C++
    pSink->Release();
    ```

    

6.  Verwenden Sie den Stub in einem beliebigen asynchronen-Befehl.

    Wenn Sie mit dem-Befehl fertig sind, geben Sie den lokalen Verweis Zähler frei.

    Im folgenden Codebeispiel wird der Stub in einem asynchronen-Befehl verwendet.

    ```C++
    // pServices is an IWbemServices* object
    pServices->CreateInstanceEnumAsync(strClassName, 0, NULL, pStubSink);
    ```

    

    Manchmal müssen Sie möglicherweise einen asynchronen Aufrufvorgang abbrechen, nachdem Sie den-Befehl durchführen. Wenn Sie den-Befehl abbrechen müssen, brechen Sie den-Befehl mit dem gleichen Zeiger ab, der ursprünglich den-Befehl durchgeführt hat.

    Im folgenden Codebeispiel wird gezeigt, wie ein asynchroner-Befehl abgebrochen wird.

    ```C++
    pServices->CancelAsyncCall(pStubSink);
    ```

    

7.  Geben Sie den lokalen Verweis Zähler frei, wenn Sie die Verwendung des asynchronen Aufrufes abgeschlossen haben.

    Stellen Sie sicher, dass Sie den *pstubsink* -Zeiger erst freigeben, nachdem Sie sich vergewissert haben, dass der asynchrone-Befehl nicht abgebrochen werden muss. Außerdem sollten Sie *pstubsink* nicht freigeben, nachdem WMI den *psink* -Senke-Zeiger freigegeben hat. Durch das Freigeben von *pstubsink* nach *psink* wird eine zirkuläre Verweis Anzahl erstellt, in der die Senke und der Stub immer im Speicher bleiben. Stattdessen ist ein möglicher Speicherort für die Freigabe des Zeigers der [**iwbewbjectsink:: SetStatus**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-setstatus) -Befehl, der von WMI erstellt wurde, um zu melden, dass der ursprüngliche asynchrone-Aufrufvorgang abgeschlossen ist.

8.  Wenn Sie den Vorgang abgeschlossen haben, können Sie com mit einem [**Release von Release ()**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release)aufzurufen.

    Im folgenden Codebeispiel wird gezeigt, wie [**Release ()**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) auf dem *punsecapp* -Zeiger aufgerufen wird.

    ```C++
    pUnsecApp->Release();
    ```

    

    Die Codebeispiele in diesem Thema erfordern den folgenden Verweis und die \# include-Anweisung zur ordnungsgemäßen Kompilierung.

    ```C++
    #include <wbemidl.h>
    #pragma comment(lib, "wbemuuid.lib")
    ```

    

Weitere Informationen zur [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) -Funktion und zu Parametern finden Sie in der [com](../cossdk/component-services-portal.md) -Dokumentation im Platform Software Development Kit (SDK).

 

 
