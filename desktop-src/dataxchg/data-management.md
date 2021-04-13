---
title: Datenverwaltung
description: In diesem Thema wird erläutert, wie Speicher Objekte Daten von einer Anwendung an eine andere übergeben.
ms.assetid: 32919f27-4699-4831-8837-c5160b1daf4e
keywords:
- Windows-Benutzeroberfläche, dynamischer Datenaustausch (DDE)
- Dynamischer Datenaustausch (DDE), Datenverwaltung
- DDE (dynamischer Datenaustausch), Datenverwaltung
- Datenaustausch, dynamischer Datenaustausch (DDE)
- Windows-Benutzeroberfläche, dynamischer Datenaustausch Verwaltungs Bibliothek (Ddeml)
- Dynamischer Datenaustausch Management Library (Ddeml), Datenverwaltung
- Ddeml (dynamischer Datenaustausch-Verwaltungs Bibliothek), Datenverwaltung
- Datenaustausch, dynamischer Datenaustausch Verwaltungs Bibliothek (Ddeml)
- Dynamischer Datenaustausch (DDE), Objekte
- DDE (dynamischer Datenaustausch), Objekte
- Dynamischer Datenaustausch Management Library (Ddeml), Objekte
- Ddeml (dynamischer Datenaustausch-Verwaltungs Bibliothek), Objekte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dfc5178f636cf4b75111d4fc48e17fd144400a91
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388769"
---
# <a name="data-management"></a><span data-ttu-id="bc3cf-115">Datenverwaltung</span><span class="sxs-lookup"><span data-stu-id="bc3cf-115">Data Management</span></span>

<span data-ttu-id="bc3cf-116">Da dynamischer Datenaustausch (DDE) Arbeitsspeicher Objekte verwendet, um Daten von einer Anwendung an eine andere zu übergeben, bietet die dynamischer Datenaustausch Management Library (Ddeml) eine Reihe von Funktionen, die DDE-Anwendungen zum Erstellen und Verwalten von DDE-Objekten verwenden können.</span><span class="sxs-lookup"><span data-stu-id="bc3cf-116">Because Dynamic Data Exchange (DDE) uses memory objects to pass data from one application to another, the Dynamic Data Exchange Management Library (DDEML) provides a set of functions that DDE applications can use to create and manage DDE objects.</span></span>

<span data-ttu-id="bc3cf-117">Alle Transaktionen, die den Datenaustausch betreffen, erfordern, dass die Anwendung die Daten bereitstellt, um einen lokalen Puffer mit den Daten zu erstellen und dann die Funktion [**ddecreatedatahandle**](/windows/desktop/api/Ddeml/nf-ddeml-ddecreatedatahandle) aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="bc3cf-117">All transactions that involve the exchange of data require the application supplying the data to create a local buffer containing the data and then to call the [**DdeCreateDataHandle**](/windows/desktop/api/Ddeml/nf-ddeml-ddecreatedatahandle) function.</span></span> <span data-ttu-id="bc3cf-118">Diese Funktion weist ein DDE-Objekt zu, kopiert die Daten aus dem Puffer in das-Objekt und gibt ein Daten Handle zurück.</span><span class="sxs-lookup"><span data-stu-id="bc3cf-118">This function allocates a DDE object, copies the data from the buffer to the object, and returns a data handle.</span></span> <span data-ttu-id="bc3cf-119">Ein Daten Handle ist ein **DWORD** -Wert, der von der Ddeml verwendet wird, um den Zugriff auf Daten im DDE-Objekt bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="bc3cf-119">A data handle is a **DWORD** value that the DDEML uses to provide access to data in the DDE object.</span></span> <span data-ttu-id="bc3cf-120">Um die Daten in einem DDE-Objekt freizugeben, übergibt eine Anwendung das Daten Handle an die Ddeml, und die Ddeml übergibt das Handle an die DDE-Rückruffunktion der Anwendung, die die Daten Transaktion empfängt.</span><span class="sxs-lookup"><span data-stu-id="bc3cf-120">To share the data in a DDE object, an application passes the data handle to the DDEML, and the DDEML passes the handle to the DDE callback function of the application that is receiving the data transaction.</span></span>

<span data-ttu-id="bc3cf-121">Im folgenden Beispiel wird gezeigt, wie ein DDE-Objekt erstellt und ein Handle für das-Objekt abgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="bc3cf-121">The following example shows how to create a DDE object and obtain a handle to the object.</span></span> <span data-ttu-id="bc3cf-122">Während der [**xD \_ advreq**](xtyp-advreq.md) -Transaktion konvertiert die Rückruffunktion die aktuelle Uhrzeit in eine ASCII-Zeichenfolge, kopiert die Zeichenfolge in einen lokalen Puffer und erstellt dann ein DDE-Objekt, das die Zeichenfolge enthält.</span><span class="sxs-lookup"><span data-stu-id="bc3cf-122">During the [**XTYP\_ADVREQ**](xtyp-advreq.md) transaction, the callback function converts the current time to an ASCII string, copies the string to a local buffer, and then creates a DDE object that contains the string.</span></span> <span data-ttu-id="bc3cf-123">Die Rückruffunktion gibt das Handle für das DDE-Objekt (hddedata) an die Ddeml zurück, die das Handle an die Client Anwendung übergibt.</span><span class="sxs-lookup"><span data-stu-id="bc3cf-123">The callback function returns the handle to the DDE object (HDDEDATA) to the DDEML, which passes the handle to the client application.</span></span>


```
typedef struct tagTIME 
{ 
    INT     hour;   // 0 - 11 hours for analog clock 
    INT     hour12; // 12-hour format 
    INT     hour24; // 24-hour format 
    INT     minute; 
    INT     second; 
    INT     ampm;   // 0 - AM , 1 - PM 
} TIME; 
 
HDDEDATA EXPENTRY DdeCallback(uType, uFmt, hconv, hsz1, hsz2, 
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
 
    CHAR szBuf[32];
    HRESULT hResult;
    size_t * pcch;
    HRESULT hResult; 
 
    switch (uType) 
    { 
    case XTYP_ADVREQ: 
        if ((hsz1 == hszTime && hsz2 == hszNow) && 
                (uFmt == CF_TEXT)) 
        { 
            // Copy the formatted string to a buffer. 
 
            itoa(tmTime.hour, szBuf, 10);
            hResult = StringCchCat(szBuf, 32/sizeof(TCHAR), ":"); 
            if (FAILED(hResult))
            {
            // TO DO: Write error handler.
                return;
            }
            if (tmTime.minute < 10)
                hResult = StringCchCat(szBuf, 32/sizeof(TCHAR), "0"); 
                if (FAILED(hResult)
            {
            // TO DO: Write error handler.
                return;
            } 
            hResult = StringCchLength(szBuf, 32/sizeof(TCHAR), pcch);
            if (FAILED(hResult))
            {
            // TO DO: Write error handler.
                return;
            }
            itoa(tmTime.minute, &szBuf[*pcch], 10);
            hResult = StringCchCat(szBuf, 32/sizeof(TCHAR), ":"); 
            if (FAILED(hResult)
            {
            // TO DO: Write error handler.
                return;
            }
            if (tmTime.second < 10) 
                hResult = StringCchCat(szBuf, 32/sizeof(TCHAR), "0"); 
            if (FAILED(hResult)
            {
            // TO DO: Write error handler.
                return;
            }
            hResult = StringCchLength(szBuf, 32/sizeof(TCHAR), pcch);
            if (FAILED(hResult))
            {
            // TO DO: Write error handler.
                return;
            }
            itoa(tmTime.second, &szBuf[*pcch], 10);
            hResult = StringCchLength(szBuf, 32/sizeof(TCHAR), pcch);
            if (FAILED(hResult))
            {
            // TO DO: Write error handler.
                return;
            } 
            szBuf[*pcch] = '\0'; 
 
            // Create a global object and return its data handle. 
            hResult = StringCchLength(szBuf, 32/sizeof(TCHAR), pcch);
            if (FAILED(hResult))
            {
            // TO DO: Write error handler.
                return;
            }
            return (DdeCreateDataHandle( 
                idInst, 
                (LPBYTE) szBuf,     // instance identifier 
                *pcch + 1,          // source buffer length 
                0,                  // offset from beginning 
                hszNow,             // item name string 
                CF_TEXT,            // clipboard format 
                0));                // no creation flags 
        } else return (HDDEDATA) NULL; 
 
    // Process other transactions. 
    } 
} 
```



<span data-ttu-id="bc3cf-124">Die empfangende Anwendung erhält einen Zeiger auf das DDE-Objekt, indem das Daten Handle an die [**DDE AccessData**](/windows/desktop/api/Ddeml/nf-ddeml-ddeaccessdata) -Funktion übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="bc3cf-124">The receiving application obtains a pointer to the DDE object by passing the data handle to the [**DdeAccessData**](/windows/desktop/api/Ddeml/nf-ddeml-ddeaccessdata) function.</span></span> <span data-ttu-id="bc3cf-125">Der von **DDE AccessData** zurückgegebene Zeiger bietet schreibgeschützten Zugriff.</span><span class="sxs-lookup"><span data-stu-id="bc3cf-125">The pointer returned by **DdeAccessData** provides read-only access.</span></span> <span data-ttu-id="bc3cf-126">Die Anwendung sollte den Zeiger verwenden, um die Daten zu überprüfen, und dann die [**ddeunaccessdata**](/windows/desktop/api/Ddeml/nf-ddeml-ddeunaccessdata) -Funktion aufzurufen, um den Zeiger für ungültig zu erklären.</span><span class="sxs-lookup"><span data-stu-id="bc3cf-126">The application should use the pointer to review the data and then call the [**DdeUnaccessData**](/windows/desktop/api/Ddeml/nf-ddeml-ddeunaccessdata) function to invalidate the pointer.</span></span> <span data-ttu-id="bc3cf-127">Die Anwendung kann die Daten mithilfe der [**DDE GetData**](/windows/desktop/api/Ddeml/nf-ddeml-ddegetdata) -Funktion in einen lokalen Puffer kopieren.</span><span class="sxs-lookup"><span data-stu-id="bc3cf-127">The application can copy the data to a local buffer by using the [**DdeGetData**](/windows/desktop/api/Ddeml/nf-ddeml-ddegetdata) function.</span></span>

<span data-ttu-id="bc3cf-128">Im folgenden Beispiel wird ein Zeiger auf das DDE-Objekt abgerufen, das durch den *hdata* -Parameter identifiziert wird, und der Inhalt wird in einen lokalen Puffer kopiert. Anschließend wird der Zeiger für ungültig erklärt.</span><span class="sxs-lookup"><span data-stu-id="bc3cf-128">The following example obtains a pointer to the DDE object identified by the *hData* parameter, copies the contents to a local buffer, and then invalidates the pointer.</span></span>


```
HDDEDATA hdata; 
LPBYTE lpszAdviseData; 
DWORD cbDataLen; 
DWORD i; 
char szData[32]; 
 
// 
case XTYP_ADVDATA: 
    lpszAdviseData = DdeAccessData(hdata, &cbDataLen); 
    for (i = 0; i < cbDataLen; i++) 
        szData[i] = *lpszAdviseData++; 
    DdeUnaccessData(hdata); 
    return (HDDEDATA) TRUE; 
//
```



<span data-ttu-id="bc3cf-129">Normalerweise wird das Handle in der Erstellungs Anwendung ungültig, wenn eine Anwendung, die ein Daten Handle erstellt hat, dieses Handle an die Ddeml übergibt.</span><span class="sxs-lookup"><span data-stu-id="bc3cf-129">Usually, when an application that created a data handle passes that handle to the DDEML, the handle becomes invalid in the creating application.</span></span> <span data-ttu-id="bc3cf-130">Diese Situation ist kein Problem, wenn die Anwendung Daten nur mit einer einzigen Anwendung gemeinsam verwenden muss.</span><span class="sxs-lookup"><span data-stu-id="bc3cf-130">This situation is not a problem if the application must share data with only a single application.</span></span> <span data-ttu-id="bc3cf-131">Wenn eine Anwendung die gleichen Daten mit mehreren Anwendungen gemeinsam verwenden muss, sollte die Erstellungs Anwendung jedoch das hdata- \_ Flag appowned in [**ddecreatedatahandle**](/windows/desktop/api/Ddeml/nf-ddeml-ddecreatedatahandle)angeben.</span><span class="sxs-lookup"><span data-stu-id="bc3cf-131">If an application must share the same data with multiple applications, however, the creating application should specify the HDATA\_APPOWNED flag in [**DdeCreateDataHandle**](/windows/desktop/api/Ddeml/nf-ddeml-ddecreatedatahandle).</span></span> <span data-ttu-id="bc3cf-132">Dadurch erhält der Besitz des DDE-Objekts für die Erstellungs Anwendung, und die Ddeml verhindert, dass das Daten Handle ungültig wird.</span><span class="sxs-lookup"><span data-stu-id="bc3cf-132">Doing so gives ownership of the DDE object to the creating application and prevents the DDEML from invalidating the data handle.</span></span> <span data-ttu-id="bc3cf-133">Die Anwendung kann dann das Daten handle beliebig oft nach dem Aufruf von **ddecreatedatahandle** übergeben.</span><span class="sxs-lookup"><span data-stu-id="bc3cf-133">The application can then pass the data handle any number of times after calling **DdeCreateDataHandle** only once.</span></span>

<span data-ttu-id="bc3cf-134">Wenn eine Anwendung das Flag hdata \_ appowned im *afcmd* -Parameter von [**ddecreatedatahandle**](/windows/desktop/api/Ddeml/nf-ddeml-ddecreatedatahandle)angibt, muss Sie die [**ddefreedatahandle**](/windows/desktop/api/Ddeml/nf-ddeml-ddefreedatahandle) -Funktion aufrufen, um das Speicher Handle freizugeben, unabhängig davon, ob es das Handle an die Ddeml übergeben hat.</span><span class="sxs-lookup"><span data-stu-id="bc3cf-134">If an application specifies the HDATA\_APPOWNED flag in the *afCmd* parameter of [**DdeCreateDataHandle**](/windows/desktop/api/Ddeml/nf-ddeml-ddecreatedatahandle), it must call the [**DdeFreeDataHandle**](/windows/desktop/api/Ddeml/nf-ddeml-ddefreedatahandle) function to free the memory handle, regardless of whether it passed the handle to the DDEML.</span></span> <span data-ttu-id="bc3cf-135">Bevor die Anwendung beendet wird, muss Sie **ddefreedatahandle** zum Freigeben von Daten Handles, die Sie erstellt, aber nicht an die Ddeml übergeben hat, abrufen.</span><span class="sxs-lookup"><span data-stu-id="bc3cf-135">Before it terminates, an application must call **DdeFreeDataHandle** to free any data handle that it created but did not pass to the DDEML.</span></span>

<span data-ttu-id="bc3cf-136">Eine Anwendung, die noch nicht das Handle an ein DDE-Objekt an die Ddeml übermittelt hat, kann dem Objektdaten hinzufügen oder Daten im Objekt überschreiben, indem die [**ddeadddata**](/windows/desktop/api/Ddeml/nf-ddeml-ddeadddata) -Funktion verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="bc3cf-136">An application that has not yet passed the handle to a DDE object to the DDEML can add data to the object or overwrite data in the object by using the [**DdeAddData**](/windows/desktop/api/Ddeml/nf-ddeml-ddeadddata) function.</span></span> <span data-ttu-id="bc3cf-137">In der Regel verwendet eine Anwendung **ddeadddata** , um ein nicht initialisiertes DDE-Objekt zu füllen.</span><span class="sxs-lookup"><span data-stu-id="bc3cf-137">Typically, an application uses **DdeAddData** to fill an uninitialized DDE object.</span></span> <span data-ttu-id="bc3cf-138">Wenn eine Anwendung ein Daten Handle an die Ddeml übergibt, kann das von dem Handle identifizierte DDE-Objekt nicht geändert werden. Sie kann nur freigegeben werden.</span><span class="sxs-lookup"><span data-stu-id="bc3cf-138">After an application passes a data handle to the DDEML, the DDE object identified by the handle cannot be changed; it can only be freed.</span></span>

 

 




