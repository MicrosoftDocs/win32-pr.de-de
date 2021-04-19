---
description: Wie bei allen Anwendungen empfängt WMI Fehlercodes vom Windows-Betriebssystem.
ms.assetid: f54b8e7c-c531-47d5-bab8-780652b94555
ms.tgt_platform: multiple
title: Abrufen eines Fehlercodes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75c42dbd160ef6412c332e2da2c01f6590e10966
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345244"
---
# <a name="retrieving-an-error-code"></a>Abrufen eines Fehlercodes

Wie bei allen Anwendungen empfängt WMI Fehlercodes vom Windows-Betriebssystem.

Wenn Sie einen Fehlercode erhalten, haben Sie die folgenden Optionen:

-   Sehen Sie sich das Ereignisprotokoll an.

    WMI sendet Fehlermeldungen an den Ereignisprotokoll Dienst, der die Ereignisprotokolle prüft, um die Ursache eines Fehlers zu ermitteln. Sie können die Klassen, die vom [Ereignisprotokoll](/previous-versions/windows/desktop/eventlogprov/event-log-provider) Anbieter unterstützt werden, für den programmgesteuerten Zugriff auf Ereignisprotokolle verwenden.

-   Rufen Sie den Fehlercode in der Regel ab.

    WMI unterstützt die Standardverfahren zum Abrufen von Fehlercodes, die com-Fehlercodes für C++ sind, und systemeigene Fehler Objekte wie [Err Object (VBScript)](/previous-versions//sbf5ze0e(v=vs.85))oder [**Swap-LastError**](swbemlasterror.md) , wenn der Anbieter Fehlerinformationen liefert.

Weitere Informationen finden Sie unter Bearbeiten von [Klassen-und Instanzinformationen](manipulating-class-and-instance-information.md).

In diesem Thema werden die folgenden Abschnitte erläutert:

-   [Behandeln eines Fehlers mit VBScript](#handling-an-error-with-vbscript)
-   [Behandeln eines Fehlers mithilfe von C++](#handling-an-error-using-c)

## <a name="handling-an-error-with-vbscript"></a>Behandeln eines Fehlers mit VBScript

Wenn ein WMI-Aufrufe über die Skript-API für WMI einen Fehler verursacht, haben Sie die folgenden Optionen für den Zugriff auf die Fehlerinformationen:

-   Verwenden Sie Native Fehler Mechanismen der Skriptsprache, z. b. Wenn Sie in VBScript das [Err-Objekt (VBScript)](/previous-versions//sbf5ze0e(v=vs.85)) verwenden, um die Fehlerbehandlung zu unterstützen.
-   Erstellen Sie ein " [**taubemlasterror**](swbemlasterror.md) "-Objekt, um einen Fehlerbericht zu erhalten.

Das folgende Skript zeigt die Verwendung des nativen [Err-Objekts (VBScript)](/previous-versions//sbf5ze0e(v=vs.85)). Wenn ein falscher Wert für das Prozess handle angegeben ist, wird ein Fehler generiert.


```VB
On Error Resume Next
Set objProcess = GetObject( _
    "winmgmts:root\cimv2:Win32_Process.Handle='one'")
Wscript.Echo Err.Number
```



> [!Note]
>
> Die **Description** -Eigenschaft des [Err-Objekts (VBScript)](/previous-versions//sbf5ze0e(v=vs.85)) ist beim Herstellen einer Verbindung mit WMI über den Moniker "winmgmts:" leer. Wenn Sie jedoch mithilfe von " [**Swap-Locator**](swbemlocator.md)" eine Verbindung herstellen, ist die Beschreibung verfügbar.
>
> In der folgenden Tabelle werden die Eigenschaften des [Err-Objekts (VBScript)](/previous-versions//sbf5ze0e(v=vs.85))aufgelistet.
>
> 
>
> | Eigenschaft                   | Enthält                                                       |
> |----------------------------|----------------------------------------------------------------|
> | **Beschreibung**<br/> | Lokalisierte, lesbare Beschreibung des Fehlers.<br/> |
> | **Number**<br/>      | **HRESULT** , das von der Skript-API für WMI zurückgegeben wurde.<br/>  |
> | **Quelle**<br/>      | Identifiziert das Objekt, das den Fehler ausgelöst hat.<br/>        |
>
> 
>
>  

 

Das folgende Skript veranschaulicht die Verwendung eines " [**Swap**](swbemlasterror.md) "-Objekts, um ausführliche Fehlerinformationen abzurufen. Beachten Sie, dass nicht alle Anbieter Informationen für " **taubemlasterror**" bereitstellen. Weitere Informationen zu Fehlercodes in Skripts finden Sie unter [WbemErrorEnum](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemerrorenum).


```VB
On Error Resume Next
Set obj = GetObject("winmgmts:root\cimv2:Win32_Process.Handle='one'")
Set LastError = createobject("wbemscripting.swbemlasterror")
Wscript.Echo "Operation = " & LastError.operation & VBCRLF & "ParameterInfo = " _
            & LastError.ParameterInfo & VBCRLF & "ProviderName = " & LastError.ProviderName
```



## <a name="handling-an-error-using-c"></a>Behandeln eines Fehlers mithilfe von C++

Eine WMI-Client Anwendung kann entweder com-oder WMI-spezifische Fehler empfangen. Die com-Fehler entsprechen der Struktur von com-Fehlercodes. Alle WMI-Schnittstellen können einen com-spezifischen Fehler außer den Schnittstellen [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext), [**IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject)und [**iwbemqualifierset**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemqualifierset) zurückgeben. Weitere Informationen zu COM-Fehlercodes finden Sie unter [Fehlerbehandlung](../com/error-handling-in-com.md). Auf den Referenzseiten der WMI-Schnittstellen werden die entsprechenden WMI-Fehlercodes im Abschnitt Fehlercodes aufgeführt.

Eine Client Anwendung muss die com-Standards zum Überprüfen von Status-und Fehlerrückgabe Codes einhalten. Der Hauptunterschied, den Sie auswählen müssen, ist, ob Sie den Fehlercode von einem synchronen, semisynchronen oder asynchronen aufrufen möchten.

**So greifen Sie mit C++ auf synchrone und semisynchrone Fehlermeldungen zu**

1.  Rufen Sie die Fehlerinformationen mit einem Aufrufen der com-Funktion [GetErrorInfo]( /windows/win32/api/oleauto/nf-oleauto-geterrorinfo) ab.

    Stellen Sie sicher, dass [GetErrorInfo]( /windows/win32/api/oleauto/nf-oleauto-geterrorinfo) unmittelbar nach einer Schnittstellen Methode aufgerufen wird, die auf einen Fehler hinweist. Dies schließt alle [**iwbemcallresult**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemcallresult) -Methoden ein, die Sie bei der Verarbeitung eines semisynchronen Prozesses aufrufen.

2.  Überprüfen Sie das zurückgegebene com-Fehler Objekt mit einem Rückruf der [**IErrorInterface:: QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) -Methode.

    Stellen Sie sicher, dass IID \_ wbemclassobject für den *riid* -Parameter im [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) -Befehl angegeben wird. Die **QueryInterface** -Methode gibt eine Instanz einer WMI-Klasse zurück, in der Regel [**\_ \_ ExtendedStatus**](--extendedstatus.md).

WMI stellt das Fehler Objekt nicht über [GetErrorInfo]( /windows/win32/api/oleauto/nf-oleauto-geterrorinfo) für einen asynchronen-Befehl bereit, da es keine Möglichkeit gibt, zu wissen, wann oder in welchem Thread der asynchrone-Befehl aufgetreten ist. Daher kann Ihr Code nur bestimmte Fehler verarbeiten oder den Fehler des Aufrufes über com übergeben.

> [!Note]  
> Da der Rückruf für die Senke möglicherweise nicht auf derselben Authentifizierungs Ebene wie der Client zurückgegeben wird, wird empfohlen, semisynchrone anstelle der asynchronen Kommunikation zu verwenden. Weitere Informationen finden Sie unter [Aufrufen einer Methode](calling-a-method.md).

 

**So greifen Sie mithilfe von C++ auf asynchrone Fehlermeldungen zu**

-   Rufen Sie das com-Fehler Objekt aus der Implementierung von [**iwbemubjectsink:: SetStatus**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-setstatus)ab.

    Der folgende Pseudo Code zeigt eine typische Implementierung der Fehlerbehandlung für eine Client Anwendung.

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

    

 

