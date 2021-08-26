---
title: Datenverwaltung
description: In diesem Thema wird erläutert, wie Speicherobjekte Daten von einer Anwendung an eine andere übergeben.
ms.assetid: 32919f27-4699-4831-8837-c5160b1daf4e
keywords:
- Windows Benutzeroberfläche,dynamische Daten Exchange (DDE)
- dynamische Daten Exchange (DDE), Datenverwaltung
- DDE (dynamische Daten Exchange),Datenverwaltung
- Datenaustausch,dynamische Daten Exchange (DDE)
- Windows Benutzeroberfläche,dynamische Daten Exchange Management Library (DDEML)
- dynamische Daten Exchange Management Library (DDEML), Datenverwaltung
- DDEML (dynamische Daten Exchange Management Library),Datenverwaltung
- Datenaustausch,dynamische Daten Exchange-Verwaltungsbibliothek (DDEML)
- dynamische Daten Exchange (DDE), Objekte
- DDE (dynamische Daten Exchange),Objekte
- dynamische Daten Exchange Management Library (DDEML), Objects
- DDEML (dynamische Daten Exchange Management Library),Objects
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85dc9b8ccd82d184866ac9ed28f15bdeac424ec0bf9bd7767a520dea69bc4d11
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119953740"
---
# <a name="data-management"></a>Datenverwaltung

Da dynamische Daten Exchange (DDE) Speicherobjekte verwendet, um Daten von einer Anwendung an eine andere zu übergeben, stellt die dynamische Daten Exchange Management Library (DDEML) eine Reihe von Funktionen bereit, mit denen DDE-Anwendungen DDE-Objekte erstellen und verwalten können.

Für alle Transaktionen, die den Datenaustausch beinhalten, muss die Anwendung die Daten bereitstellen, um einen lokalen Puffer mit den Daten zu erstellen und dann die [**DdeCreateDataHandle-Funktion**](/windows/desktop/api/Ddeml/nf-ddeml-ddecreatedatahandle) aufzurufen. Diese Funktion ordnet ein DDE-Objekt zu, kopiert die Daten aus dem Puffer in das -Objekt und gibt ein Datenhandle zurück. Ein Datenhandle ist ein **DWORD-Wert,** den die DDEML verwendet, um Zugriff auf Daten im DDE-Objekt bereitzustellen. Um die Daten in einem DDE-Objekt freizugeben, übergibt eine Anwendung das Datenhandle an die DDEML, und die DDEML übergibt das Handle an die DDE-Rückruffunktion der Anwendung, die die Datentransaktion empfängt.

Das folgende Beispiel zeigt, wie Sie ein DDE-Objekt erstellen und ein Handle für das -Objekt abrufen. Während der [**XTYP \_ ADOAQ-Transaktion**](xtyp-advreq.md) konvertiert die Rückruffunktion die aktuelle Zeit in eine ASCII-Zeichenfolge, kopiert die Zeichenfolge in einen lokalen Puffer und erstellt dann ein DDE-Objekt, das die Zeichenfolge enthält. Die Rückruffunktion gibt das Handle für das DDE-Objekt (HDDEDATA) an die DDEML zurück, das das Handle an die Clientanwendung übergibt.


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



Die empfangende Anwendung ruft einen Zeiger auf das DDE-Objekt ab, indem das Datenhandle an die [**DdeAccessData-Funktion**](/windows/desktop/api/Ddeml/nf-ddeml-ddeaccessdata) übergeben wird. Der von **DdeAccessData** zurückgegebene Zeiger bietet schreibgeschützten Zugriff. Die Anwendung sollte den Zeiger verwenden, um die Daten zu überprüfen, und dann die [**DdeUnaccessData-Funktion**](/windows/desktop/api/Ddeml/nf-ddeml-ddeunaccessdata) aufrufen, um den Zeiger ungültig zu machen. Die Anwendung kann die Daten mithilfe der [**DdeGetData-Funktion**](/windows/desktop/api/Ddeml/nf-ddeml-ddegetdata) in einen lokalen Puffer kopieren.

Das folgende Beispiel ruft einen Zeiger auf das DDE-Objekt ab, das durch den *hData-Parameter* identifiziert wird, kopiert den Inhalt in einen lokalen Puffer und macht dann den Zeiger ungültig.


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



Wenn eine Anwendung, die ein Datenhandle erstellt hat, dieses Handle an die DDEML übergibt, wird das Handle in der erstellenden Anwendung in der Regel ungültig. Diese Situation ist kein Problem, wenn die Anwendung Daten nur für eine einzelne Anwendung freigeben muss. Wenn eine Anwendung jedoch dieselben Daten für mehrere Anwendungen freigeben muss, sollte die erstellende Anwendung das HDATA \_ APPOWNED-Flag in [**DdeCreateDataHandle**](/windows/desktop/api/Ddeml/nf-ddeml-ddecreatedatahandle)angeben. Dadurch erhält die erstellende Anwendung den Besitz des DDE-Objekts und verhindert, dass die DDEML das Datenhandle ungültig macht. Die Anwendung kann das Datenhandle dann beliebig oft übergeben, nachdem **DdeCreateDataHandle** nur einmal aufgerufen wurde.

Wenn eine Anwendung das HDATA \_ APPOWNED-Flag im *afCmd-Parameter* von [**DdeCreateDataHandle**](/windows/desktop/api/Ddeml/nf-ddeml-ddecreatedatahandle)angibt, muss sie die [**DdeFreeDataHandle-Funktion**](/windows/desktop/api/Ddeml/nf-ddeml-ddefreedatahandle) aufrufen, um das Speicherhandle freizugeben, unabhängig davon, ob das Handle an die DDEML übergeben wurde. Bevor sie beendet wird, muss eine Anwendung **DdeFreeDataHandle** aufrufen, um alle datenhandles freigibt, die sie erstellt, aber nicht an die DDEML übergeben hat.

Eine Anwendung, die das Handle noch nicht an ein DDE-Objekt an die DDEML übergeben hat, kann dem Objekt Daten hinzufügen oder Daten im Objekt mithilfe der [**DdeAddData-Funktion**](/windows/desktop/api/Ddeml/nf-ddeml-ddeadddata) überschreiben. In der Regel verwendet eine Anwendung **DdeAddData,** um ein nicht initialisiertes DDE-Objekt auszufüllen. Nachdem eine Anwendung ein Datenhandle an die DDEML übergeben hat, kann das durch das Handle identifizierte DDE-Objekt nicht mehr geändert werden. sie kann nur freigegeben werden.

 

 




