---
description: Asynchrone Aufrufe stellen schwerwiegende Sicherheitsrisiken dar, da ein Rückruf für die Senke möglicherweise nicht das Ergebnis des asynchronen Aufrufs durch die ursprüngliche Anwendung oder das Skript ist.
ms.assetid: 2b839ea9-e1e6-4123-a98a-04ebee907b3b
ms.tgt_platform: multiple
title: Festlegen der Sicherheit für einen asynchronen-Befehl
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e39f78315814d3b66c97e60a6b8045d7ea9e7afe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106359553"
---
# <a name="setting-security-on-an-asynchronous-call"></a>Festlegen der Sicherheit für einen asynchronen-Befehl

Asynchrone Aufrufe stellen schwerwiegende Sicherheitsrisiken dar, da ein Rückruf für die [*Senke*](gloss-s.md) möglicherweise nicht das Ergebnis des asynchronen Aufrufs durch die ursprüngliche Anwendung oder das Skript ist. Die Sicherheit in Remote Verbindungen basiert auf der Verschlüsselung der Kommunikation zwischen dem Client und dem Anbieter auf dem Remote Computer. In C++ können Sie im [**CoInitializeSecurity-CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity)-Parameter die Verschlüsselung über den Authentifizierungs Ebenen-Parameter festlegen. Legen Sie in der Skripterstellung *AuthenticationLevel* in der monikerverbindung oder in einem [**Swap Security**](swbemsecurity.md) -Objekt fest. Weitere Informationen finden Sie unter [Festlegen der standardmäßigen Prozess Sicherheitsstufe mithilfe von VBScript](setting-the-default-process-security-level-using-vbscript.md).

Das Sicherheitsrisiko für asynchrone Aufrufe besteht darin, dass WMI die Authentifizierungs Ebene für einen Rückruf verringert, bis der Rückruf erfolgreich ist. Bei einem ausgehenden asynchronen-Befehl kann der Client die Authentifizierungs Ebene für die Verbindung mit WMI festlegen. WMI Ruft die Sicherheitseinstellungen für den Client-Befehl ab und versucht, den Rückruf mit der gleichen Authentifizierungs Ebene durchzusetzen. Der Rückruf wird immer auf der **\_ \_ \_ \_ Pkt- \_ Datenschutzebene der RPC-C-authn-Ebene** initiiert. Wenn der Rückruf fehlschlägt, wird die Authentifizierungs Ebene von WMI auf eine Ebene gesenkt, bei der der Rückruf ggf. für die **RPC- \_ C- \_ authn-Ebene " \_ \_ None**" erfolgreich ist. Im Kontext von aufrufen innerhalb des lokalen Systems, bei dem der Authentifizierungsdienst nicht Kerberos ist, wird der Rückruf immer auf **RPC- \_ C- \_ authn-Ebene " \_ \_ None**" zurückgegeben.

Die minimale Authentifizierungs Ebene ist **RPC \_ C \_ authn \_ Level \_ Pkt** (**wbemauthenticationlevelpkt** für die Skripterstellung). Sie können jedoch eine höhere Ebene angeben, z. **b. RPC-C- \_ \_ authn- \_ Ebene \_ Pkt \_ Privacy** (**wbemauthenticationlevelpktprivacy**). Es wird empfohlen, dass Client Anwendungen oder Skripts die Authentifizierungs Ebene auf den **\_ \_ \_ \_ Standardwert der RPC C authn-Ebene** (**wbemauthenticationleveldefault**) festlegen, sodass die Authentifizierungs Ebene auf die vom Server angegebene Ebene ausgehandelt werden kann.

Der Registrierungs Wert " **HKEY \_ local \_ Machine** \\ **Software** \\ **Microsoft** \\ **WBEM** \\ **CIMOM** \\ **unsecappaccesscontroldefault** " steuert, ob WMI in Rückrufen eine akzeptable Authentifizierungs Ebene prüft. Dies ist der einzige Mechanismus zum Schutz der senkensicherheit für asynchrone Aufrufe in Skript-oder Visual Basic. Standardmäßig ist dieser Registrierungsschlüssel auf 0 (null) festgelegt. Wenn der Registrierungsschlüssel NULL ist, überprüft WMI keine Authentifizierungs Ebenen. Um asynchrone Aufrufe in der Skripterstellung zu sichern, legen Sie den Registrierungsschlüssel auf 1 fest. C++-Clients können den Zugriff auf die Senke über [**iwbemunseculinipartment:: kreatesinkstub**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemunsecuredapartment-createsinkstub) steuern. Der Wert wird standardmäßig an einem beliebigen Speicherort erstellt.

Die folgenden Themen enthalten Beispiele für das Festlegen der Sicherheit für den asynchronen Sicherheitsdienst:

-   [Festlegen der Sicherheit für einen asynchronen VBScript-Anrufe](setting-security-on-an-asynchronous-call-in-vbscript.md)
-   Festlegen der Sicherheit für asynchrone Aufrufe in C++

## <a name="setting-asynchronous-call-security-in-c"></a>Festlegen der Sicherheit für asynchrone Aufrufe in C++

Die Methode [**iwbemunsecuanpartment:: kreatesinkstub**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemunsecuredapartment-createsinkstub) ähnelt der [**iunsecuagentpartment::**](/windows/desktop/api/Wbemcli/nf-wbemcli-iunsecuredapartment-createobjectstub) -Methode, und erstellt eine Senke in einem separaten Prozess, Unsecapp.exe, um Rückrufe zu empfangen. Die Methode " **upatesinkstub** " verfügt jedoch über einen *dwFlag*-Parameter, der angibt, wie der separate Prozess die Zugriffs Steuerung behandelt.

Der *dwFlag* -Parameter gibt eine der folgenden Aktionen für Unsecapp.exe an:

-   Verwenden Sie die Registrierungsschlüssel Einstellung, um zu bestimmen, ob der Zugriff überprüft werden soll oder nicht.
-   Ignorieren Sie den Registrierungsschlüssel, und überprüfen Sie immer den Zugriff.
-   Ignorieren Sie den Registrierungsschlüssel, und überprüfen Sie den Zugriff nie.

Das Codebeispiel in diesem Thema erfordert, dass die folgende \# include-Anweisung ordnungsgemäß kompiliert wird.


```C++
#include <wbemidl.h>
```



Im folgenden Verfahren wird beschrieben, wie ein asynchroner Befehl mit [**iwbemunsecuredapartment**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemunsecuredapartment)durchgeführt wird.

**So führen Sie einen asynchronen aufrufbefehl mit iwbemunsecuredapartment aus**

1.  Erstellen Sie einen dedizierten Prozess mit einem Aufrufen von [**cokreateinstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance).

    Im folgenden Codebeispiel wird [**cokreatanstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) aufgerufen, um einen dedizierten Prozess zu erstellen.

    ```C++
    CLSID                    CLSID_WbemUnsecuredApartment;
    IWbemUnsecuredApartment* pUnsecApp = NULL;

    CoCreateInstance(CLSID_WbemUnsecuredApartment, 
                     NULL, 
                     CLSCTX_LOCAL_SERVER, 
                     IID_IWbemUnsecuredApartment, 
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

    Im folgenden Codebeispiel wird ein Stub für die Senke erstellt.

    ```C++
    LPCWSTR          wszReserved = NULL;           
    IWbemObjectSink* pStubSink   = NULL;
    IUnknown*        pStubUnk    = NULL; 

    pUnsecApp->CreateSinkStub(pSink,
                              WBEM_FLAG_UNSECAPP_CHECK_ACCESS,  //Authenticate callbacks regardless of registry key
                              wszReserved,
                              &pStubSink);
    ```

    

4.  Geben Sie den Sink-Objekt Zeiger frei.

    Sie können den Objekt Zeiger freigeben, da der Stub jetzt den-Zeiger besitzt.

    Im folgenden Codebeispiel wird der Objekt Zeiger freigegeben.

    ```C++
    pSink->Release();
    ```

    

5.  Verwenden Sie den Stub in einem beliebigen asynchronen-Befehl.

    Wenn Sie mit dem-Befehl fertig sind, geben Sie den lokalen Verweis Zähler frei.

    Im folgenden Codebeispiel wird der Stub in einem asynchronen-Befehl verwendet.

    ```C++
    // pServices is an IWbemServices* object
    pServices->CreateInstanceEnumAsync(strClassName, 0, NULL, pStubSink);
    ```

    

    Manchmal müssen Sie möglicherweise einen asynchronen Aufrufvorgang abbrechen, nachdem Sie den-Befehl durchführen. Wenn Sie den-Befehl abbrechen müssen, brechen Sie den-Befehl mit dem gleichen Zeiger ab, der ursprünglich den-Befehl durchgeführt hat.

    Im folgenden Codebeispiel wird beschrieben, wie ein asynchroner-Befehl abgebrochen wird.

    ```C++
    pServices->CancelAsyncCall(pStubSink);
    ```

    

6.  Geben Sie den lokalen Verweis Zähler frei, wenn Sie die Verwendung des asynchronen Aufrufes abgeschlossen haben.

    Stellen Sie sicher, dass Sie den *pstubsink* -Zeiger nur freigeben, nachdem Sie sich vergewissert haben, dass der asynchrone-Befehl nicht abgebrochen werden muss Außerdem sollten Sie *pstubsink* nicht freigeben, nachdem WMI den *psink* -Senke-Zeiger freigegeben hat. Durch das Freigeben von *pstubsink* nach *psink* wird eine zirkuläre Verweis Anzahl erstellt, in der die Senke und der Stub immer im Speicher bleiben. Stattdessen ist ein möglicher Speicherort für die Freigabe des Zeigers der [**iwbewbjectsink:: SetStatus**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-setstatus) -Befehl, der von WMI erstellt wurde, um zu melden, dass der ursprüngliche asynchrone-Aufrufvorgang abgeschlossen ist.

7.  Wenn Sie den Vorgang abgeschlossen haben, können Sie com mit einem [**Release von Release ()**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release)aufzurufen.

    Im folgenden Codebeispiel wird gezeigt, wie [**Release ()**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) auf dem *punsecapp* -Zeiger aufgerufen wird.

    ```C++
    pUnsecApp->Release();
    ```

    

Weitere Informationen zur [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) -Funktion und zu Parametern finden Sie in der [com](../cossdk/component-services-portal.md) -Dokumentation.

 

 
