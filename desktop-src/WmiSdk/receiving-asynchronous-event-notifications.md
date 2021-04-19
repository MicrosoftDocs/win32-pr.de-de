---
description: Asynchrone Ereignis Benachrichtigung ist eine Technik, mit der eine Anwendung Ereignisse ständig überwachen kann, ohne die Systemressourcen zu überwachen.
ms.assetid: 69ec8ead-9073-4689-bc66-5134728ab147
ms.tgt_platform: multiple
title: Empfangen von asynchronen Ereignis Benachrichtigungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d883908475c796a6bcf31895f2928345541c940
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106364055"
---
# <a name="receiving-asynchronous-event-notifications"></a>Empfangen von asynchronen Ereignis Benachrichtigungen

Asynchrone Ereignis Benachrichtigung ist eine Technik, mit der eine Anwendung Ereignisse ständig überwachen kann, ohne die Systemressourcen zu überwachen. Für asynchrone Ereignis Benachrichtigungen gelten die gleichen Sicherheitseinschränkungen wie für andere asynchrone Aufrufe. Sie können stattdessen semisynchrone Aufrufe durchführen. Weitere Informationen finden Sie unter [Aufrufen einer Methode](calling-a-method.md).

Die Warteschlange für asynchrone Ereignisse, die an einen Client weitergeleitet werden, ist möglicherweise sehr groß. Daher implementiert WMI eine systemweite Richtlinie, um zu vermeiden, dass nicht genügend Arbeitsspeicher verfügbar ist. WMI verlangsamt Ereignisse oder löscht Ereignisse aus der Warteschlange, wenn die Warteschlange eine bestimmte Größe überschreitet.

WMI verwendet die Eigenschaften [**lowgrenzoldonevents**](/windows/desktop/CIMWin32Prov/win32-wmisetting) und [**highgrenzoldonevents**](/windows/desktop/CIMWin32Prov/win32-wmisetting) der [**Win32 \_ wmisetting**](/windows/desktop/CIMWin32Prov/win32-wmisetting) -Klasse, um Grenzwerte für die Vermeidung von nicht genügend Arbeitsspeicher festzulegen. Der Minimalwert gibt an, wann WMI mit der Verlangsamung der Ereignis Benachrichtigung beginnen soll, und der Höchstwert gibt an, wann Ereignisse gelöscht werden sollen. Die Standardwerte für die niedrigen und hohen Schwellenwerte sind 1 Million (10 MB) und 2 Millionen (20 MB). Außerdem können Sie die [**maxwaitonevents**](/windows/desktop/CIMWin32Prov/win32-wmisetting) -Eigenschaft so festlegen, dass Sie die Zeitspanne beschreibt, die WMI warten soll, bevor Ereignisse gelöscht werden. Der Standardwert für **maxwaitonevents** ist 2000 oder 2 Sekunden.

## <a name="receiving-asynchronous-event-notifications-in-vbscript"></a>Empfangen von asynchronen Ereignis Benachrichtigungen in VBScript

Die Skript Aufrufe für den Empfang von Ereignis Benachrichtigungen sind im Wesentlichen identisch mit allen asynchronen Aufrufen mit denselben Sicherheitsproblemen. Weitere Informationen finden Sie unter [Erstellen eines asynchronen Aufrufes mit VBScript](making-an-asynchronous-call-with-vbscript.md).

**So empfangen Sie asynchrone Ereignis Benachrichtigungen in VBScript**

1.  Erstellen Sie ein Sink-Objekt, indem Sie [WScript. CreateObject](/previous-versions//xzysf6hc(v=vs.85)) aufrufen und die ProgID von "WbemScripting" und den Objekttyp von " [**Swap-Sink**](swbemsink.md)" angeben. Das sink-Objekt empfängt die Benachrichtigungen.
2.  Schreiben Sie eine Unterroutine für jedes Ereignis, das Sie verarbeiten möchten. In der folgenden Tabelle sind die [**slibemsink**](swbemsink.md) -Ereignisse aufgeführt.

    

    | Ereignis                                            | Bedeutung                                                                                                                         |
    |--------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
    | [**Onobjectready**](swbemsink-onobjectready.md) | Meldet die Rückgabe eines Objekts an die Senke. Bei Verwendung dieses Aufrufes wird jedes Mal ein Objekt zurückgegeben, bis der Vorgang beendet ist.     |
    | [**OnCompleted**](swbemsink-oncompleted.md)     | Meldet den Abschluss eines asynchronen Aufrufes. Dieses Ereignis tritt nie auf, wenn der Vorgang unbegrenzt ist.                          |
    | [**Onobjectput**](swbemsink-onobjectput.md)     | Meldet den Abschluss eines asynchronen Put-Vorgangs. Dieses Ereignis gibt den Objekt Pfad der-Instanz oder der gespeicherten-Klasse zurück. |
    | [**OnProgress**](swbemsink-onprogress.md)       | Meldet den Status eines asynchronen aufrulaufs, der gerade ausgeführt wird. Nicht alle Anbieter unterstützen zwischenfortschritts Berichte.             |
    | [**Abbrechen**](swbemsink-cancel.md)               | Bricht alle ausstehenden asynchronen Vorgänge ab, die dieser Objekt Senke zugeordnet sind.                                        |

    

     

Im folgenden VBScript-Codebeispiel wird das Löschen von Prozessen mit einem 10 Sekunden-Abruf Intervall benachrichtigt. In diesem Skript behandelt die Unterroutine-Senke \_ onobjectready das Ereignis vorkommen. Im Beispiel hat das sink-Objekt den Namen "Sink", aber Sie können dieses Objekt bei der Auswahl benennen.


```VB
strComputer = "." 
Set objWMIService = GetObject("winmgmts:\\" & strComputer & "\root\CIMV2") 
Set MySink = WScript.CreateObject( _
    "WbemScripting.SWbemSink","SINK_")

objWMIservice.ExecNotificationQueryAsync MySink, _
    "SELECT * FROM __InstanceDeletionEvent" _
    & " WITHIN 10 WHERE TargetInstance ISA 'Win32_Process'"


WScript.Echo "Waiting for events..."

While (True)
    Wscript.Sleep(1000)
Wend

Sub SINK_OnObjectReady(objObject, objAsyncContext)
    Wscript.Echo "__InstanceDeletionEvent event has occurred."
End Sub

Sub SINK_OnCompleted(objObject, objAsyncContext)
    WScript.Echo "Event call complete."
End Sub
```



## <a name="receiving-asynchronous-event-notifications-in-c"></a>Empfangen von asynchronen Ereignis Benachrichtigungen in C++

Um eine asynchrone Benachrichtigung auszuführen, erstellen Sie nur einen separaten Thread, um Ereignisse von Windows-Verwaltungsinstrumentation (WMI) zu überwachen und zu empfangen. Wenn dieser Thread eine Nachricht empfängt, benachrichtigt der Thread Ihre Hauptanwendung.

Indem Sie einen separaten Thread zuweisen, gestatten Sie Ihrem Hauptprozess das Ausführen anderer Aktivitäten, während Sie auf das Eintreffen eines Ereignisses warten. Die asynchrone Übermittlung von Benachrichtigungen verbessert die Leistung, bietet jedoch möglicherweise weniger Sicherheit als Sie möchten. In C++ haben Sie die Möglichkeit, die [**iwbemunsecuagentpartment**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemunsecuredapartment) -Schnittstelle zu verwenden oder Zugriffs Überprüfungen für Sicherheits Deskriptoren auszuführen. Weitere Informationen finden Sie unter [Festlegen der Sicherheit für einen asynchronen](setting-security-on-an-asynchronous-call.md)-Befehl.

**So richten Sie asynchrone Ereignis Benachrichtigungen ein**

1.  Bevor Sie asynchrone Benachrichtigungen initialisieren, stellen Sie sicher, dass die Parameter zur Vermeidung von nicht genügend Arbeitsspeicher in [**Win32- \_ wmisetting**](/windows/desktop/CIMWin32Prov/win32-wmisetting)korrekt festgelegt sind.

2.  Bestimmen Sie, welche Art von Ereignissen Sie empfangen möchten.

    WMI unterstützt systeminterne und extrinsische Ereignisse. Ein System internes Ereignis ist ein von WMI vordefiniertes Ereignis, wohingegen ein extrinsisches Ereignis ein Ereignis ist, das von einem Drittanbieter definiert wird. Weitere Informationen finden Sie unter [bestimmen des empfangenden Ereignis Typs](determining-the-type-of-event-to-receive.md).

Im folgenden Verfahren wird beschrieben, wie asynchrone Ereignis Benachrichtigungen in C++ empfangen werden.

**So empfangen Sie asynchrone Ereignis Benachrichtigungen in C++**

1.  Richten Sie Ihre Anwendung mit Aufrufen der Funktionen [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) und [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) ein.

    Durch den Aufruf von [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) wird com initialisiert, während [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) WMI die Berechtigung zum Aufrufen in den consumerprozess erteilt. Die **CoInitializeEx** -Funktion erteilt Ihnen außerdem die Möglichkeit, eine Multithread-Anwendung zu programmieren, die für die asynchrone Benachrichtigung erforderlich ist. Weitere Informationen finden Sie unter Verwalten der [WMI-Sicherheit](maintaining-wmi-security.md).

    Der Code in diesem Thema erfordert die folgenden Verweise und \# include-Anweisungen, um ordnungsgemäß zu kompilieren.

    ```C++
    #define _WIN32_DCOM
    #include <iostream>
    using namespace std;
    #include <wbemidl.h>
    ```

    

    Im folgenden Codebeispiel wird beschrieben, wie der temporäre Ereignisconsumer mit Aufrufen von [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) und [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity)eingerichtet wird.

    ```C++
    void main(int argc, char **argv)
    {
        HRESULT hr = 0;
        hr = CoInitializeEx (0, COINIT_MULTITHREADED);
        hr = CoInitializeSecurity (NULL, 
           -1, 
           NULL, 
           NULL,   
           RPC_C_AUTHN_LEVEL_NONE, 
           RPC_C_IMP_LEVEL_IMPERSONATE, 
           NULL,
           EOAC_NONE,
           NULL); 

        if (FAILED(hr))
        {
           CoUninitialize();
           cout << "Failed to initialize security. Error code = 0x"
               << hex << hr << endl;
           return;
        }

    // ...
    }
    ```

    

2.  Erstellen Sie ein Sink-Objekt über die [**iwbemubjectsink**](iwbemobjectsink.md) -Schnittstelle.

    WMI verwendet zum Senden von Ereignis Benachrichtigungen und zum Melden des Status für einen asynchronen Vorgang oder eine Ereignis Benachrichtigung " [**iwbemubjectsink**](iwbemobjectsink.md) ".

3.  Registrieren Sie Ihren Ereignisconsumer durch einen Aufruf der [**IWbemServices:: ExecNotificationQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationqueryasync) -Methode.

    Stellen Sie sicher, dass der *presponsehandler* -Parameter auf das sink-Objekt verweist, das im vorherigen Schritt erstellt wurde.

    Der Zweck der Registrierung besteht darin, nur die erforderlichen Benachrichtigungen zu empfangen. Das empfangen überflüssiger Benachrichtigungen verschwendet Verarbeitungs-und Übermittlungs Zeit. und verwendet nicht die Filterungs Fähigkeit von WMI, um das volle Potenzial zu haben.

    Ein temporärer Consumer kann jedoch mehr als einen Ereignistyp empfangen. In diesem Fall muss ein temporärer Consumer für jeden Ereignistyp separate Aufrufe von [**IWbemServices:: ExecNotificationQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationqueryasync) ausführen. Ein Consumer benötigt z. b. möglicherweise eine Benachrichtigung, wenn neue Prozesse erstellt werden (ein instanzerstellungs Ereignis oder [**\_ \_ instancecreationevent**](--instancecreationevent.md)) und für Änderungen an bestimmten Registrierungs Schlüsseln (ein Registrierungs Ereignis wie " [**RegistryKeyChangeEvent**](/previous-versions/windows/desktop/regprov/registrykeychangeevent)"). Daher führt der Consumer einen Aufruf an [**ExecNotificationQueryAsync**](swbemservices-execnotificationqueryasync.md) aus, um sich für instanzerstellungsereignisse und einen weiteren Aufruf von **ExecNotificationQueryAsync** zu registrieren, um Registrierungs Ereignisse zu registrieren.

    Wenn Sie einen Ereignisconsumer erstellen, der sich für mehrere Ereignisse registriert, sollten Sie das Registrieren mehrerer Klassen mit der gleichen Senke vermeiden. Verwenden Sie stattdessen eine separate Senke für jede Klasse des registrierten Ereignisses. Eine dedizierte Senke vereinfacht die Verarbeitung und unterstützt die Wartung, sodass Sie eine Registrierung abbrechen können, ohne dass sich dies auf die anderen auswirkt.

4.  Führen Sie alle notwendigen Aktivitäten in Ihrem Ereignisconsumer aus.

    Dieser Schritt sollte den größten Teil Ihres Codes enthalten und solche Aktivitäten wie das Anzeigen von Ereignissen für eine Benutzeroberfläche einschließen.

5.  Wenn Sie den Vorgang abgeschlossen haben, heben Sie die Registrierung für den temporären Ereignisconsumer mit einem Befehl des [**IWbemServices:: cancelasynccall**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-cancelasynccall) -Ereignisses auf.

    Löschen Sie das sink-Objekt nicht, bis der Verweis Zähler des Objekts Null erreicht wird, unabhängig davon, ob der Rückruf von [**cancelasynccall**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-cancelasynccall) erfolgreich ist oder fehlschlägt. Weitere Informationen finden Sie unter [Aufrufen einer Methode](calling-a-method.md).

 

 
