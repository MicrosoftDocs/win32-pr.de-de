---
description: Wie bei allen Anwendungen empfängt WMI Fehlercodes vom Windows Betriebssystem.
ms.assetid: f54b8e7c-c531-47d5-bab8-780652b94555
ms.tgt_platform: multiple
title: Abrufen eines Fehlercodes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f16bb7af3c5c2b17d3a99ac00c9122a2ddfa6c075f463819e182fe44193613a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119640630"
---
# <a name="retrieving-an-error-code"></a>Abrufen eines Fehlercodes

Wie bei allen Anwendungen empfängt WMI Fehlercodes vom Windows Betriebssystem.

Wenn Sie einen Fehlercode erhalten, haben Sie die folgenden Optionen:

-   Sehen Sie sich das Ereignisprotokoll an.

    WMI sendet Fehlermeldungen an den Ereignisprotokolldienst, der die Ereignisprotokolle überprüft, um die Ursache eines Fehlers zu ermitteln. Sie können die Klassen verwenden, die der [Ereignisprotokollanbieter](/previous-versions/windows/desktop/eventlogprov/event-log-provider) unterstützt, um programmgesteuert auf Ereignisprotokolle zuzugreifen.

-   Rufen Sie den Fehlercode normal ab.

    WMI unterstützt die Standardtechniken zum Abrufen von Fehlercodes, bei denen es sich um COM-Fehlercodes für C++ handelt, sowie native Fehlerobjekte wie [Err Object (VBScript)](/previous-versions//sbf5ze0e(v=vs.85))oder [**SWbemLastError,**](swbemlasterror.md) wenn der Anbieter Fehlerinformationen liefert.

Weitere Informationen finden Sie unter [Bearbeiten von Klassen- und Instanzinformationen.](manipulating-class-and-instance-information.md)

Die folgenden Abschnitte werden in diesem Thema erläutert:

-   [Behandeln eines Fehlers mit VBScript](#handling-an-error-with-vbscript)
-   [Behandeln eines Fehlers mit C++](#handling-an-error-using-c)

## <a name="handling-an-error-with-vbscript"></a>Behandeln eines Fehlers mit VBScript

Wenn ein Aufruf von WMI über die Skripterstellungs-API für WMI einen Fehler verursacht, haben Sie die folgenden Optionen, um auf die Fehlerinformationen zuzugreifen:

-   Verwenden Sie native Fehlermechanismen der Skriptsprache, z. B. verwenden Sie in VBScript [Err Object (VBScript),](/previous-versions//sbf5ze0e(v=vs.85)) um die Fehlerbehandlung zu unterstützen.
-   Erstellen Sie ein [**SWbemLastError-Objekt,**](swbemlasterror.md) um einen Fehlerbericht abzurufen.

Das folgende Skript zeigt die Verwendung des [nativen Err-Objekts (VBScript).](/previous-versions//sbf5ze0e(v=vs.85)) Wenn ein falscher Wert für das Prozesshandle angegeben wird, wird ein Fehler generiert.


```VB
On Error Resume Next
Set objProcess = GetObject( _
    "winmgmts:root\cimv2:Win32_Process.Handle='one'")
Wscript.Echo Err.Number
```



> [!Note]
>
> Die **Description-Eigenschaft** von [Err Object (VBScript)](/previous-versions//sbf5ze0e(v=vs.85)) ist leer, wenn eine Verbindung mit WMI über den Moniker "winmgmts:" hergestellt wird. Wenn Sie jedoch eine Verbindung mit [**SWbemLocator**](swbemlocator.md)herstellen, ist die Beschreibung verfügbar.
>
> In der folgenden Tabelle sind die Eigenschaften von [Err Object (VBScript)](/previous-versions//sbf5ze0e(v=vs.85))aufgeführt.
>
> 
>
> | Eigenschaft                   | Enthält                                                       |
> |----------------------------|----------------------------------------------------------------|
> | **Beschreibung**<br/> | Lokalisierte, lesbare Beschreibung des Fehlers.<br/> |
> | **Number**<br/>      | **HRESULT, das** von der Skripterstellungs-API für WMI zurückgegeben wird.<br/>  |
> | **Quelle**<br/>      | Identifiziert das Objekt, das den Fehler ausgelöst hat.<br/>        |
>
> 
>
>  

 

Das folgende Skript zeigt die Verwendung eines [**SWbemLastError-Objekts,**](swbemlasterror.md) um ausführliche Fehlerinformationen abzurufen. Beachten Sie, dass nicht alle Anbieter Informationen für **SWbemLastError** bereitstellen. Weitere Informationen zu Fehlercodes im Skript finden Sie unter [WbemErrorEnum](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemerrorenum).


```VB
On Error Resume Next
Set obj = GetObject("winmgmts:root\cimv2:Win32_Process.Handle='one'")
Set LastError = createobject("wbemscripting.swbemlasterror")
Wscript.Echo "Operation = " & LastError.operation & VBCRLF & "ParameterInfo = " _
            & LastError.ParameterInfo & VBCRLF & "ProviderName = " & LastError.ProviderName
```



## <a name="handling-an-error-using-c"></a>Behandeln eines Fehlers mit C++

Eine WMI-Clientanwendung kann com- oder WMI-spezifische Fehler empfangen. Die COM-Fehler entsprechen der Struktur der COM-Fehlercodes. Alle WMI-Schnittstellen können einen COM-spezifischen Fehler zurückgeben, mit Ausnahme der Schnittstellen [**IWbemContext,**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) [**IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject)und [**IWbemQualifierSet.**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemqualifierset) Weitere Informationen zu COM-Fehlercodes finden Sie unter [Fehlerbehandlung.](../com/error-handling-in-com.md) Auf den Referenzseiten der WMI-Schnittstellen werden die entsprechenden WMI-Fehlercodes im Abschnitt Fehlercodes aufgeführt.

Eine Clientanwendung muss die COM-Standards zum Überprüfen von Status- und Fehlerrückgabecodes befolgen. Der Hauptunterschied, den Sie auswählen müssen, ist, ob Sie den Fehlercode aus einem synchronen, semisynchronen oder asynchronen Aufruf abrufen möchten.

**So greifen Sie mit C++ auf synchrone und semisynchrone Fehlermeldungen zu**

1.  Rufen Sie die Fehlerinformationen mit einem Aufruf der [COM-Funktion GetErrorInfo]( /windows/win32/api/oleauto/nf-oleauto-geterrorinfo) ab.

    Stellen Sie sicher, dass [GetErrorInfo]( /windows/win32/api/oleauto/nf-oleauto-geterrorinfo) sofort aufgerufen wird, nachdem eine Schnittstellenmethode einen Fehler angegeben hat. Dies schließt eine der [**IWbemCallResult-Methoden**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemcallresult) ein, die Sie während der Verarbeitung eines semisynchronen Prozesses aufrufen.

2.  Untersuchen Sie das zurückgegebene COM-Fehlerobjekt mit einem Aufruf der [**IErrorInterface::QueryInterface-Methode.**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q))

    Stellen Sie sicher, dass Sie IID \_ WbemClassObject für den *riid-Parameter* im [**QueryInterface-Aufruf**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) angeben. Die **QueryInterface-Methode** gibt eine Instanz einer WMI-Klasse zurück, in der Regel [**\_ \_ ExtendedStatus**](--extendedstatus.md).

WMI übermittelt das Fehlerobjekt nicht über [GetErrorInfo]( /windows/win32/api/oleauto/nf-oleauto-geterrorinfo) für einen asynchronen Aufruf, da es keine Möglichkeit gibt, zu wissen, wann oder in welchem Thread der asynchrone Aufruf aufgetreten ist. Daher kann Ihr Code nur bestimmte Fehler behandeln oder den Aufruffehler über COM übergeben.

> [!Note]  
> Da der Rückruf an die Senke möglicherweise nicht auf der gleichen Authentifizierungsebene zurückgegeben wird, die der Client erfordert, wird empfohlen, anstelle der asynchronen Kommunikation semisynchron zu verwenden. Weitere Informationen finden Sie unter [Aufrufen einer Methode.](calling-a-method.md)

 

**So greifen Sie mit C++ auf asynchrone Fehlermeldungen zu**

-   Rufen Sie das COM-Fehlerobjekt aus Ihrer Implementierung von [**IWbemObjectSink::SetStatus ab.**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-setstatus)

    Der folgende Pseudocode zeigt eine typische Fehlerbehandlungsimplementierungen für eine Clientanwendung.

    ```C++
    HRESULT hRes = SomeMethod;

    // Check for specific error and status codes.
    if (hRes == WBEM_E_NOT_FOUND)
    {
    // Processing to handle specific error code
    }
    else if hRes == WBEM_S_DUPLICATE_OBJECTS
    {
    // All other cases, including errors specific to COM
    }
    else if (FAILED(hRes))
    {

    }
    ```

    

 

