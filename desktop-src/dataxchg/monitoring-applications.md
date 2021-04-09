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
# <a name="monitoring-applications"></a><span data-ttu-id="e9bbe-111">Überwachen von Anwendungen</span><span class="sxs-lookup"><span data-stu-id="e9bbe-111">Monitoring Applications</span></span>

<span data-ttu-id="e9bbe-112">Die API-Elemente der Ddeml (dynamischer Datenaustausch Management Library) können verwendet werden, um eine Anwendung zu erstellen, die dynamischer Datenaustausch (DDE)-Aktivität im System überwacht.</span><span class="sxs-lookup"><span data-stu-id="e9bbe-112">The API elements of the Dynamic Data Exchange Management Library (DDEML) can be used to create an application that monitors Dynamic Data Exchange (DDE) activity in the system.</span></span> <span data-ttu-id="e9bbe-113">Wie jede beliebige Ddeml-Anwendung enthält eine DDE-Überwachungsanwendung eine DDE-Rückruffunktion.</span><span class="sxs-lookup"><span data-stu-id="e9bbe-113">Like any DDEML application, a DDE monitoring application contains a DDE callback function.</span></span> <span data-ttu-id="e9bbe-114">Die Ddeml benachrichtigt die DDE-Rückruffunktion einer Überwachungsanwendung immer dann, wenn ein DDE-Ereignis auftritt, wobei Informationen über das Ereignis an die Rückruffunktion übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="e9bbe-114">The DDEML notifies a monitoring application's DDE callback function whenever a DDE event occurs, passing information about the event to the callback function.</span></span> <span data-ttu-id="e9bbe-115">Die Anwendung zeigt die Informationen in der Regel in einem Fenster an oder schreibt Sie in eine Datei.</span><span class="sxs-lookup"><span data-stu-id="e9bbe-115">The application typically displays the information in a window or writes it to a file.</span></span>

<span data-ttu-id="e9bbe-116">Zum Empfangen von Benachrichtigungen von der Ddeml muss eine Anwendung als DDE-Monitor registriert sein, indem das appclass \_ Monitor-Flag in einem Aufrufe der [**DDEInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) -Funktion angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="e9bbe-116">To receive notifications from the DDEML, an application must have registered as a DDE monitor by specifying the APPCLASS\_MONITOR flag in a call to the [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) function.</span></span> <span data-ttu-id="e9bbe-117">Im gleichen Aufrufs kann die Anwendung mindestens ein monitorflags angeben, um die Ereignis Typen anzugeben, für die die Ddeml die Rückruffunktion der Anwendung benachrichtigen soll.</span><span class="sxs-lookup"><span data-stu-id="e9bbe-117">In this same call, the application can specify one or more monitor flags to indicate the types of events for which the DDEML is to notify the application's callback function.</span></span> <span data-ttu-id="e9bbe-118">Die folgenden monitorflags können von einer Anwendung angegeben werden:</span><span class="sxs-lookup"><span data-stu-id="e9bbe-118">The following monitor flags can be specified by an application:</span></span>



| <span data-ttu-id="e9bbe-119">Flag</span><span class="sxs-lookup"><span data-stu-id="e9bbe-119">Flag</span></span>          | <span data-ttu-id="e9bbe-120">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e9bbe-120">Description</span></span>                                                                                                                                                                                                                                         |
|---------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e9bbe-121">MF- \_ Rückrufe</span><span class="sxs-lookup"><span data-stu-id="e9bbe-121">MF\_CALLBACKS</span></span> | <span data-ttu-id="e9bbe-122">Benachrichtigt die Rückruffunktion, wenn eine Transaktion an eine DDE-Rückruffunktion im System gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="e9bbe-122">Notifies the callback function whenever a transaction is sent to any DDE callback function in the system.</span></span>                                                                                                                                           |
| <span data-ttu-id="e9bbe-123">MF- \_ netzwerkv</span><span class="sxs-lookup"><span data-stu-id="e9bbe-123">MF\_CONV</span></span>      | <span data-ttu-id="e9bbe-124">Benachrichtigt die Rückruffunktion, wenn eine Konversation eingerichtet oder beendet wird.</span><span class="sxs-lookup"><span data-stu-id="e9bbe-124">Notifies the callback function whenever a conversation is established or terminated.</span></span>                                                                                                                                                                |
| <span data-ttu-id="e9bbe-125">MF- \_ Fehler</span><span class="sxs-lookup"><span data-stu-id="e9bbe-125">MF\_ERRORS</span></span>    | <span data-ttu-id="e9bbe-126">Benachrichtigt die Rückruffunktion, wenn ein Ddeml-Fehler auftritt.</span><span class="sxs-lookup"><span data-stu-id="e9bbe-126">Notifies the callback function whenever a DDEML error occurs.</span></span>                                                                                                                                                                                       |
| <span data-ttu-id="e9bbe-127">Informationen zu MF \_ hsz \_</span><span class="sxs-lookup"><span data-stu-id="e9bbe-127">MF\_HSZ\_INFO</span></span> | <span data-ttu-id="e9bbe-128">Benachrichtigt die Rückruffunktion immer dann, wenn eine Ddeml-Anwendung den Verwendungs Zähler eines Zeichen folgen Handles erstellt, freigibt oder erhöht oder wenn ein Zeichen folgen Handle aufgrund eines Aufrufs der [**ddeuninitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeuninitialize) -Funktion freigegeben wird.</span><span class="sxs-lookup"><span data-stu-id="e9bbe-128">Notifies the callback function whenever a DDEML application creates, frees, or increments the usage count of a string handle or whenever a string handle is freed as a result of a call to the [**DdeUninitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeuninitialize) function.</span></span> |
| <span data-ttu-id="e9bbe-129">MF- \_ Links</span><span class="sxs-lookup"><span data-stu-id="e9bbe-129">MF\_LINKS</span></span>     | <span data-ttu-id="e9bbe-130">Benachrichtigt die Rückruffunktion, wenn eine Empfehlung-Schleife gestartet oder beendet wird.</span><span class="sxs-lookup"><span data-stu-id="e9bbe-130">Notifies the callback function whenever an advise loop is started or ended.</span></span>                                                                                                                                                                         |
| <span data-ttu-id="e9bbe-131">MF- \_ postmsgs</span><span class="sxs-lookup"><span data-stu-id="e9bbe-131">MF\_POSTMSGS</span></span>  | <span data-ttu-id="e9bbe-132">Benachrichtigt die Rückruffunktion immer dann, wenn das System oder eine Anwendung eine DDE-Nachricht postet.</span><span class="sxs-lookup"><span data-stu-id="e9bbe-132">Notifies the callback function whenever the system or an application posts a DDE message.</span></span>                                                                                                                                                           |
| <span data-ttu-id="e9bbe-133">MF \_ sendmsgs</span><span class="sxs-lookup"><span data-stu-id="e9bbe-133">MF\_SENDMSGS</span></span>  | <span data-ttu-id="e9bbe-134">Benachrichtigt die Rückruffunktion immer dann, wenn das System oder eine Anwendung eine DDE-Nachricht sendet.</span><span class="sxs-lookup"><span data-stu-id="e9bbe-134">Notifies the callback function whenever the system or an application sends a DDE message.</span></span>                                                                                                                                                           |



 

<span data-ttu-id="e9bbe-135">Im folgenden Beispiel wird gezeigt, wie Sie eine DDE-Überwachungsanwendung registrieren, damit Ihre DDE-Rückruffunktion Benachrichtigungen über alle DDE-Ereignisse empfängt.</span><span class="sxs-lookup"><span data-stu-id="e9bbe-135">The following example shows how to register a DDE monitoring application so that its DDE callback function receives notifications of all DDE events.</span></span>


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



<span data-ttu-id="e9bbe-136">Die Ddeml informiert eine Überwachungsanwendung über ein DDE-Ereignis, indem eine [**XYP- \_ Monitor**](xtyp-monitor.md) Transaktion an die DDE-Rückruffunktion der Anwendung gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="e9bbe-136">The DDEML informs a monitoring application of a DDE event by sending an [**XTYP\_MONITOR**](xtyp-monitor.md) transaction to the application's DDE callback function.</span></span> <span data-ttu-id="e9bbe-137">Während dieser Transaktion übergibt die Ddeml ein monitorflag, das den Typ des aufgetretenen DDE-Ereignisses angibt, und ein Handle für ein DDE-Objekt, das ausführliche Informationen über das Ereignis enthält.</span><span class="sxs-lookup"><span data-stu-id="e9bbe-137">During this transaction, the DDEML passes a monitor flag that specifies the type of DDE event that has occurred and a handle to a DDE object that contains detailed information about the event.</span></span> <span data-ttu-id="e9bbe-138">Die Ddeml stellt eine Reihe von Strukturen bereit, die die Anwendung verwenden kann, um die Informationen aus dem DDE-Objekt zu extrahieren.</span><span class="sxs-lookup"><span data-stu-id="e9bbe-138">The DDEML provides a set of structures that the application can use to extract the information from the DDE object.</span></span> <span data-ttu-id="e9bbe-139">Es gibt eine entsprechende Struktur für jeden Typ von DDE-Ereignis.</span><span class="sxs-lookup"><span data-stu-id="e9bbe-139">There is a corresponding structure for each type of DDE event.</span></span>



| <span data-ttu-id="e9bbe-140">Struktur</span><span class="sxs-lookup"><span data-stu-id="e9bbe-140">Structure</span></span>                                  | <span data-ttu-id="e9bbe-141">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e9bbe-141">Description</span></span>                                                       |
|--------------------------------------------|-------------------------------------------------------------------|
| [<span data-ttu-id="e9bbe-142">**Moncbstruct**</span><span class="sxs-lookup"><span data-stu-id="e9bbe-142">**MONCBSTRUCT**</span></span>](/windows/win32/api/ddeml/ns-ddeml-moncbstruct)     | <span data-ttu-id="e9bbe-143">Enthält Informationen zu einer Transaktion.</span><span class="sxs-lookup"><span data-stu-id="e9bbe-143">Contains information about a transaction.</span></span>                         |
| [<span data-ttu-id="e9bbe-144">**Mon-vstruct**</span><span class="sxs-lookup"><span data-stu-id="e9bbe-144">**MONCONVSTRUCT**</span></span>](/windows/win32/api/ddeml/ns-ddeml-monconvstruct) | <span data-ttu-id="e9bbe-145">Enthält Informationen zu einer Konversation.</span><span class="sxs-lookup"><span data-stu-id="e9bbe-145">Contains information about a conversation.</span></span>                        |
| [<span data-ttu-id="e9bbe-146">**Monerrstruct**</span><span class="sxs-lookup"><span data-stu-id="e9bbe-146">**MONERRSTRUCT**</span></span>](/windows/win32/api/ddeml/ns-ddeml-monerrstruct)   | <span data-ttu-id="e9bbe-147">Enthält Informationen zum letzten DDE-Fehler.</span><span class="sxs-lookup"><span data-stu-id="e9bbe-147">Contains information about the latest DDE error.</span></span>                  |
| [<span data-ttu-id="e9bbe-148">**Monlinkstruct**</span><span class="sxs-lookup"><span data-stu-id="e9bbe-148">**MONLINKSTRUCT**</span></span>](/windows/win32/api/ddeml/ns-ddeml-monlinkstruct) | <span data-ttu-id="e9bbe-149">Enthält Informationen zu einer-Empfehlung-Schleife.</span><span class="sxs-lookup"><span data-stu-id="e9bbe-149">Contains information about an advise loop.</span></span>                        |
| [<span data-ttu-id="e9bbe-150">**Monhszstruct**</span><span class="sxs-lookup"><span data-stu-id="e9bbe-150">**MONHSZSTRUCT**</span></span>](/windows/win32/api/ddeml/ns-ddeml-monhszstructa)   | <span data-ttu-id="e9bbe-151">Enthält Informationen über ein Zeichen folgen handle.</span><span class="sxs-lookup"><span data-stu-id="e9bbe-151">Contains information about a string handle.</span></span>                       |
| [<span data-ttu-id="e9bbe-152">**Monmsgstruct**</span><span class="sxs-lookup"><span data-stu-id="e9bbe-152">**MONMSGSTRUCT**</span></span>](/windows/win32/api/ddeml/ns-ddeml-monmsgstruct)   | <span data-ttu-id="e9bbe-153">Enthält Informationen zu einer DDE-Nachricht, die gesendet oder gepostet wurde.</span><span class="sxs-lookup"><span data-stu-id="e9bbe-153">Contains information about a DDE message that was sent or posted.</span></span> |



 

<span data-ttu-id="e9bbe-154">Das folgende Beispiel zeigt die DDE-Rückruffunktion einer DDE-Überwachungsanwendung, die Informationen zu jedem Ereignis des Zeichen folgen Handles formatiert und dann die Informationen in einem-Fenster anzeigt.</span><span class="sxs-lookup"><span data-stu-id="e9bbe-154">The following example shows the DDE callback function of a DDE monitoring application that formats information about each string handle event and then displays the information in a window.</span></span> <span data-ttu-id="e9bbe-155">Die-Funktion verwendet die [**monhszstruct**](/windows/win32/api/ddeml/ns-ddeml-monhszstructa) -Struktur, um die Informationen aus dem DDE-Objekt zu extrahieren.</span><span class="sxs-lookup"><span data-stu-id="e9bbe-155">The function uses the [**MONHSZSTRUCT**](/windows/win32/api/ddeml/ns-ddeml-monhszstructa) structure to extract the information from the DDE object.</span></span>


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



 

 




