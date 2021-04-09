---
title: Überwachen von Anwendungen
description: In diesem Thema wird erläutert, wie Elemente der dynamischer Datenaustausch-Verwaltungs Bibliothek zum Erstellen einer Anwendung verwendet werden können, die dynamische Datenaustauschaktivitäten im System überwacht.
ms.assetid: 6705dc8e-d1e9-4057-9fa2-42cd5cf818af
keywords:
- Windows-Benutzeroberfläche, dynamischer Datenaustausch (DDE)
- Dynamischer Datenaustausch (DDE), Überwachen von Anwendungen
- DDE (dynamischer Datenaustausch), Überwachen von Anwendungen
- Datenaustausch, dynamischer Datenaustausch (DDE)
- Windows-Benutzeroberfläche, dynamischer Datenaustausch Verwaltungs Bibliothek (Ddeml)
- Dynamischer Datenaustausch Management Library (Ddeml), Überwachen von Anwendungen
- Ddeml (dynamischer Datenaustausch-Verwaltungs Bibliothek), Überwachen von Anwendungen
- Datenaustausch, dynamischer Datenaustausch Verwaltungs Bibliothek (Ddeml)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1f75685d4caa15e519485b2d8b37983faa35366
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036705"
---
# <a name="monitoring-applications"></a>Überwachen von Anwendungen

Die API-Elemente der Ddeml (dynamischer Datenaustausch Management Library) können verwendet werden, um eine Anwendung zu erstellen, die dynamischer Datenaustausch (DDE)-Aktivität im System überwacht. Wie jede beliebige Ddeml-Anwendung enthält eine DDE-Überwachungsanwendung eine DDE-Rückruffunktion. Die Ddeml benachrichtigt die DDE-Rückruffunktion einer Überwachungsanwendung immer dann, wenn ein DDE-Ereignis auftritt, wobei Informationen über das Ereignis an die Rückruffunktion übergeben werden. Die Anwendung zeigt die Informationen in der Regel in einem Fenster an oder schreibt Sie in eine Datei.

Zum Empfangen von Benachrichtigungen von der Ddeml muss eine Anwendung als DDE-Monitor registriert sein, indem das appclass \_ Monitor-Flag in einem Aufrufe der [**DDEInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) -Funktion angegeben wird. Im gleichen Aufrufs kann die Anwendung mindestens ein monitorflags angeben, um die Ereignis Typen anzugeben, für die die Ddeml die Rückruffunktion der Anwendung benachrichtigen soll. Die folgenden monitorflags können von einer Anwendung angegeben werden:



| Flag          | Beschreibung                                                                                                                                                                                                                                         |
|---------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| MF- \_ Rückrufe | Benachrichtigt die Rückruffunktion, wenn eine Transaktion an eine DDE-Rückruffunktion im System gesendet wird.                                                                                                                                           |
| MF- \_ netzwerkv      | Benachrichtigt die Rückruffunktion, wenn eine Konversation eingerichtet oder beendet wird.                                                                                                                                                                |
| MF- \_ Fehler    | Benachrichtigt die Rückruffunktion, wenn ein Ddeml-Fehler auftritt.                                                                                                                                                                                       |
| Informationen zu MF \_ hsz \_ | Benachrichtigt die Rückruffunktion immer dann, wenn eine Ddeml-Anwendung den Verwendungs Zähler eines Zeichen folgen Handles erstellt, freigibt oder erhöht oder wenn ein Zeichen folgen Handle aufgrund eines Aufrufs der [**ddeuninitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeuninitialize) -Funktion freigegeben wird. |
| MF- \_ Links     | Benachrichtigt die Rückruffunktion, wenn eine Empfehlung-Schleife gestartet oder beendet wird.                                                                                                                                                                         |
| MF- \_ postmsgs  | Benachrichtigt die Rückruffunktion immer dann, wenn das System oder eine Anwendung eine DDE-Nachricht postet.                                                                                                                                                           |
| MF \_ sendmsgs  | Benachrichtigt die Rückruffunktion immer dann, wenn das System oder eine Anwendung eine DDE-Nachricht sendet.                                                                                                                                                           |



 

Im folgenden Beispiel wird gezeigt, wie Sie eine DDE-Überwachungsanwendung registrieren, damit Ihre DDE-Rückruffunktion Benachrichtigungen über alle DDE-Ereignisse empfängt.


```
DWORD idInst; 
PFNCALLBACK lpDdeProc; 
hInst = hInstance; 
 
if (DdeInitialize( 
        (LPDWORD) &idInst,  // instance identifier 
        DDECallback,        // pointer to callback function 
        APPCLASS_MONITOR |  // this is a monitoring application 
        MF_CALLBACKS     |  // monitor callback functions 
        MF_CONV          |  // monitor conversation data 
        MF_ERRORS        |  // monitor DDEML errors 
        MF_HSZ_INFO      |  // monitor data handle activity 
        MF_LINKS         |  // monitor advise loops 
        MF_POSTMSGS      |  // monitor posted DDE messages 
        MF_SENDMSGS,        // monitor sent DDE messages 
        0))                 // reserved 
{
    return FALSE; 
}
```



Die Ddeml informiert eine Überwachungsanwendung über ein DDE-Ereignis, indem eine [**XYP- \_ Monitor**](xtyp-monitor.md) Transaktion an die DDE-Rückruffunktion der Anwendung gesendet wird. Während dieser Transaktion übergibt die Ddeml ein monitorflag, das den Typ des aufgetretenen DDE-Ereignisses angibt, und ein Handle für ein DDE-Objekt, das ausführliche Informationen über das Ereignis enthält. Die Ddeml stellt eine Reihe von Strukturen bereit, die die Anwendung verwenden kann, um die Informationen aus dem DDE-Objekt zu extrahieren. Es gibt eine entsprechende Struktur für jeden Typ von DDE-Ereignis.



| Struktur                                  | BESCHREIBUNG                                                       |
|--------------------------------------------|-------------------------------------------------------------------|
| [**Moncbstruct**](/windows/win32/api/ddeml/ns-ddeml-moncbstruct)     | Enthält Informationen zu einer Transaktion.                         |
| [**Mon-vstruct**](/windows/win32/api/ddeml/ns-ddeml-monconvstruct) | Enthält Informationen zu einer Konversation.                        |
| [**Monerrstruct**](/windows/win32/api/ddeml/ns-ddeml-monerrstruct)   | Enthält Informationen zum letzten DDE-Fehler.                  |
| [**Monlinkstruct**](/windows/win32/api/ddeml/ns-ddeml-monlinkstruct) | Enthält Informationen zu einer-Empfehlung-Schleife.                        |
| [**Monhszstruct**](/windows/win32/api/ddeml/ns-ddeml-monhszstructa)   | Enthält Informationen über ein Zeichen folgen handle.                       |
| [**Monmsgstruct**](/windows/win32/api/ddeml/ns-ddeml-monmsgstruct)   | Enthält Informationen zu einer DDE-Nachricht, die gesendet oder gepostet wurde. |



 

Das folgende Beispiel zeigt die DDE-Rückruffunktion einer DDE-Überwachungsanwendung, die Informationen zu jedem Ereignis des Zeichen folgen Handles formatiert und dann die Informationen in einem-Fenster anzeigt. Die-Funktion verwendet die [**monhszstruct**](/windows/win32/api/ddeml/ns-ddeml-monhszstructa) -Struktur, um die Informationen aus dem DDE-Objekt zu extrahieren.


```
HDDEDATA CALLBACK DDECallback(uType, uFmt, hconv, hsz1, hsz2, 
    hdata, dwData1, dwData2) 
UINT uType; 
UINT uFmt; 
HCONV hconv; 
HSZ hsz1; 
HSZ hsz2; 
HDDEDATA hdata; 
DWORD dwData1; 
DWORD dwData2; 
{ 
    LPVOID lpData; 
    CHAR *szAction; 
    CHAR szBuf[256]; 
    DWORD cb;
    HRESULT hResult; 
 
    switch (uType) 
    { 
        case XTYP_MONITOR: 
            // Obtain a pointer to the global memory object. 
 
            if (lpData = DdeAccessData(hdata, &cb)) 
            { 
                // Examine the monitor flag. 
 
                switch (dwData2) 
                { 
                    case MF_HSZ_INFO: 
 
#define PHSZS ((MONHSZSTRUCT *)lpData) 
 
                        // The global memory object contains 
                        // string handle data. Use the MONHSZSTRUCT 
                        // structure to access the data. 
 
                        switch (PHSZS->fsAction) 
                        { 
                            // Examine the action flags to determine
                            // the action performed on the handle.
 
                            case MH_CREATE: 
                                szAction = "Created"; 
                                break; 
 
                            case MH_KEEP: 
                                szAction = "Incremented"; 
                                break; 
 
                            case MH_DELETE: 
                                szAction = "Deleted"; 
                                break; 
 
                            case MH_CLEANUP: 
                                szAction = "Cleaned up"; 
                                break; 
 
                            default: 
                                DdeUnaccessData(hdata); 
                                return (HDDEDATA) 0; 
                        } 
 
                        // Write formatted output to a buffer. 
                        hResult = StringCchPrintf(szBuf, 256/sizeof(TCHAR),
                            "Handle %s, Task: %x, Hsz: %lx(%s)", 
                            (LPSTR) szAction, PHSZS->hTask, 
                            PHSZS->hsz, (LPSTR) PHSZS->str);
                        if (FAILED(hResult))
                        {
                        // TO DO: Write error handler.
                            return;
                        } 
                        // Display text or write to a file. 
 
                        break; 
 
#undef PHSZS 
 
                    // Process other MF_* flags. 
 
                    default: 
                        break; 
                } 
            } 
 
            // Free the global memory object. 
 
            DdeUnaccessData(hdata); 
            break; 
 
        default: 
            break; 
    } 
    return (HDDEDATA) 0; 
} 
```



 

 




