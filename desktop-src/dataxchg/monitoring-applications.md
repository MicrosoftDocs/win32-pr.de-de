---
title: Überwachen von Anwendungen
description: In diesem Thema wird erläutert, wie Elemente der dynamische Daten Exchange Management Library verwendet werden können, um eine Anwendung zu erstellen, die dynamische Datenaustauschaktivitäten im System überwacht.
ms.assetid: 6705dc8e-d1e9-4057-9fa2-42cd5cf818af
keywords:
- Windows Benutzeroberfläche,dynamische Daten Exchange (DDE)
- dynamische Daten Exchange (DDE), Überwachen von Anwendungen
- DDE (dynamische Daten Exchange),Überwachen von Anwendungen
- Datenaustausch,dynamische Daten Exchange (DDE)
- Windows Benutzeroberfläche,dynamische Daten Exchange Management Library (DDEML)
- dynamische Daten Exchange Management Library (DDEML), Überwachen von Anwendungen
- DDEML (dynamische Daten Exchange Management Library), Überwachen von Anwendungen
- Datenaustausch,dynamische Daten Exchange Management Library (DDEML)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8fbf6db1faa765378ea2b22b1146de770e9c94b14cf7e9e511ab862be48369c2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119128552"
---
# <a name="monitoring-applications"></a>Überwachen von Anwendungen

Die API-Elemente der dynamische Daten Exchange Management Library (DDEML) können verwendet werden, um eine Anwendung zu erstellen, die dynamische Daten Exchange(DDE)-Aktivität im System überwacht. Wie jede DDEML-Anwendung enthält eine DDE-Überwachungsanwendung eine DDE-Rückruffunktion. Die DDEML benachrichtigt die DDE-Rückruffunktion einer Überwachungsanwendung, wenn ein DDE-Ereignis auftritt, und über gibt Informationen über das Ereignis an die Rückruffunktion weiter. Die Anwendung zeigt die Informationen in der Regel in einem Fenster an oder schreibt sie in eine Datei.

Um Benachrichtigungen von DDEML zu empfangen, muss eine Anwendung als DDE-Monitor registriert sein, indem das APPCLASS MONITOR-Flag in einem Aufruf der \_ [**DdeInitialize-Funktion angegeben**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) wird. In diesem Aufruf kann die Anwendung ein oder mehrere Monitorflags angeben, um die Ereignistypen anzugeben, für die die DDEML die Rückruffunktion der Anwendung benachrichtigen soll. Die folgenden Monitorflags können von einer Anwendung angegeben werden:



| Flag          | Beschreibung                                                                                                                                                                                                                                         |
|---------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_MF-RÜCKRUFE | Benachrichtigt die Rückruffunktion, wenn eine Transaktion an eine DDE-Rückruffunktion im System gesendet wird.                                                                                                                                           |
| MF \_ CONV      | Benachrichtigt die Rückruffunktion, wenn eine Konversation hergestellt oder beendet wird.                                                                                                                                                                |
| \_MF-FEHLER    | Benachrichtigt die Rückruffunktion, wenn ein DDEML-Fehler auftritt.                                                                                                                                                                                       |
| MF \_ HSZ \_ INFO | Benachrichtigt die Rückruffunktion, wenn eine DDEML-Anwendung die Nutzungsanzahl eines Zeichenfolgenhandls erstellt, freigibt oder erhöht oder wenn ein Zeichenfolgenhandle als Ergebnis eines Aufrufs der [**DdeUninitialize-Funktion**](/windows/desktop/api/Ddeml/nf-ddeml-ddeuninitialize) freigibt. |
| \_MF-LINKS     | Benachrichtigt die Rückruffunktion, wenn eine Advise-Schleife gestartet oder beendet wird.                                                                                                                                                                         |
| MF \_ POSTMSGS  | Benachrichtigt die Rückruffunktion, wenn das System oder eine Anwendung eine DDE-Nachricht veröffentlicht.                                                                                                                                                           |
| MF \_ SENDMSGS  | Benachrichtigt die Rückruffunktion, wenn das System oder eine Anwendung eine DDE-Nachricht sendet.                                                                                                                                                           |



 

Das folgende Beispiel zeigt, wie Sie eine DDE-Überwachungsanwendung registrieren, damit die DDE-Rückruffunktion Benachrichtigungen über alle DDE-Ereignisse empfängt.


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



Die DDEML informiert eine Überwachungsanwendung über ein DDE-Ereignis, indem eine [**XTYP \_ MONITOR-Transaktion**](xtyp-monitor.md) an die DDE-Rückruffunktion der Anwendung sendet. Während dieser Transaktion übergibt die DDEML ein Monitorflag, das den Typ des aufgetretenen DDE-Ereignisses angibt, sowie ein Handle an ein DDE-Objekt, das ausführliche Informationen zum Ereignis enthält. Die DDEML stellt eine Reihe von Strukturen zur Verfügung, mit denen die Anwendung die Informationen aus dem DDE-Objekt extrahieren kann. Es gibt eine entsprechende -Struktur für jeden DDE-Ereignistyp.



| Struktur                                  | Beschreibung                                                       |
|--------------------------------------------|-------------------------------------------------------------------|
| [**MONCBSTRUCT**](/windows/win32/api/ddeml/ns-ddeml-moncbstruct)     | Enthält Informationen zu einer Transaktion.                         |
| [**MONCONVSTRUCT**](/windows/win32/api/ddeml/ns-ddeml-monconvstruct) | Enthält Informationen zu einer Konversation.                        |
| [**MONERRSTRUCT**](/windows/win32/api/ddeml/ns-ddeml-monerrstruct)   | Enthält Informationen zum letzten DDE-Fehler.                  |
| [**MONLINKSTRUCT**](/windows/win32/api/ddeml/ns-ddeml-monlinkstruct) | Enthält Informationen zu einer Advise-Schleife.                        |
| [**MONHSZSTRUCT**](/windows/win32/api/ddeml/ns-ddeml-monhszstructa)   | Enthält Informationen zu einem Zeichenfolgenhand handle.                       |
| [**MONMSGSTRUCT**](/windows/win32/api/ddeml/ns-ddeml-monmsgstruct)   | Enthält Informationen zu einer gesendeten oder gesendeten DDE-Nachricht. |



 

Das folgende Beispiel zeigt die DDE-Rückruffunktion einer DDE-Überwachungsanwendung, die Informationen zu jedem Zeichenfolgenhandpunkt-Ereignis formatiert und die Informationen dann in einem Fenster anzeigt. Die Funktion verwendet die [**MONHSZSTRUCT-Struktur,**](/windows/win32/api/ddeml/ns-ddeml-monhszstructa) um die Informationen aus dem DDE-Objekt zu extrahieren.


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



 

 




