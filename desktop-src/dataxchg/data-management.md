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
# <a name="data-management"></a>Datenverwaltung

Da dynamischer Datenaustausch (DDE) Arbeitsspeicher Objekte verwendet, um Daten von einer Anwendung an eine andere zu übergeben, bietet die dynamischer Datenaustausch Management Library (Ddeml) eine Reihe von Funktionen, die DDE-Anwendungen zum Erstellen und Verwalten von DDE-Objekten verwenden können.

Alle Transaktionen, die den Datenaustausch betreffen, erfordern, dass die Anwendung die Daten bereitstellt, um einen lokalen Puffer mit den Daten zu erstellen und dann die Funktion [**ddecreatedatahandle**](/windows/desktop/api/Ddeml/nf-ddeml-ddecreatedatahandle) aufzurufen. Diese Funktion weist ein DDE-Objekt zu, kopiert die Daten aus dem Puffer in das-Objekt und gibt ein Daten Handle zurück. Ein Daten Handle ist ein **DWORD** -Wert, der von der Ddeml verwendet wird, um den Zugriff auf Daten im DDE-Objekt bereitzustellen. Um die Daten in einem DDE-Objekt freizugeben, übergibt eine Anwendung das Daten Handle an die Ddeml, und die Ddeml übergibt das Handle an die DDE-Rückruffunktion der Anwendung, die die Daten Transaktion empfängt.

Im folgenden Beispiel wird gezeigt, wie ein DDE-Objekt erstellt und ein Handle für das-Objekt abgerufen wird. Während der [**xD \_ advreq**](xtyp-advreq.md) -Transaktion konvertiert die Rückruffunktion die aktuelle Uhrzeit in eine ASCII-Zeichenfolge, kopiert die Zeichenfolge in einen lokalen Puffer und erstellt dann ein DDE-Objekt, das die Zeichenfolge enthält. Die Rückruffunktion gibt das Handle für das DDE-Objekt (hddedata) an die Ddeml zurück, die das Handle an die Client Anwendung übergibt.


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



Die empfangende Anwendung erhält einen Zeiger auf das DDE-Objekt, indem das Daten Handle an die [**DDE AccessData**](/windows/desktop/api/Ddeml/nf-ddeml-ddeaccessdata) -Funktion übergeben wird. Der von **DDE AccessData** zurückgegebene Zeiger bietet schreibgeschützten Zugriff. Die Anwendung sollte den Zeiger verwenden, um die Daten zu überprüfen, und dann die [**ddeunaccessdata**](/windows/desktop/api/Ddeml/nf-ddeml-ddeunaccessdata) -Funktion aufzurufen, um den Zeiger für ungültig zu erklären. Die Anwendung kann die Daten mithilfe der [**DDE GetData**](/windows/desktop/api/Ddeml/nf-ddeml-ddegetdata) -Funktion in einen lokalen Puffer kopieren.

Im folgenden Beispiel wird ein Zeiger auf das DDE-Objekt abgerufen, das durch den *hdata* -Parameter identifiziert wird, und der Inhalt wird in einen lokalen Puffer kopiert. Anschließend wird der Zeiger für ungültig erklärt.


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



Normalerweise wird das Handle in der Erstellungs Anwendung ungültig, wenn eine Anwendung, die ein Daten Handle erstellt hat, dieses Handle an die Ddeml übergibt. Diese Situation ist kein Problem, wenn die Anwendung Daten nur mit einer einzigen Anwendung gemeinsam verwenden muss. Wenn eine Anwendung die gleichen Daten mit mehreren Anwendungen gemeinsam verwenden muss, sollte die Erstellungs Anwendung jedoch das hdata- \_ Flag appowned in [**ddecreatedatahandle**](/windows/desktop/api/Ddeml/nf-ddeml-ddecreatedatahandle)angeben. Dadurch erhält der Besitz des DDE-Objekts für die Erstellungs Anwendung, und die Ddeml verhindert, dass das Daten Handle ungültig wird. Die Anwendung kann dann das Daten handle beliebig oft nach dem Aufruf von **ddecreatedatahandle** übergeben.

Wenn eine Anwendung das Flag hdata \_ appowned im *afcmd* -Parameter von [**ddecreatedatahandle**](/windows/desktop/api/Ddeml/nf-ddeml-ddecreatedatahandle)angibt, muss Sie die [**ddefreedatahandle**](/windows/desktop/api/Ddeml/nf-ddeml-ddefreedatahandle) -Funktion aufrufen, um das Speicher Handle freizugeben, unabhängig davon, ob es das Handle an die Ddeml übergeben hat. Bevor die Anwendung beendet wird, muss Sie **ddefreedatahandle** zum Freigeben von Daten Handles, die Sie erstellt, aber nicht an die Ddeml übergeben hat, abrufen.

Eine Anwendung, die noch nicht das Handle an ein DDE-Objekt an die Ddeml übermittelt hat, kann dem Objektdaten hinzufügen oder Daten im Objekt überschreiben, indem die [**ddeadddata**](/windows/desktop/api/Ddeml/nf-ddeml-ddeadddata) -Funktion verwendet wird. In der Regel verwendet eine Anwendung **ddeadddata** , um ein nicht initialisiertes DDE-Objekt zu füllen. Wenn eine Anwendung ein Daten Handle an die Ddeml übergibt, kann das von dem Handle identifizierte DDE-Objekt nicht geändert werden. Sie kann nur freigegeben werden.

 

 




