---
title: Caching (Windows Internet)
description: Die WinINet-Funktionen verfügen über einfache, aber flexible, integrierte Cacheunterstützung.
ms.assetid: 44c268c9-a745-432a-8540-60d7e7d2cb2d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cea485e1c6fc8b2b474d217d940c715b65b45de8f7d211ad37bff9bdd9a4243b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119955610"
---
# <a name="caching-windows-internet"></a>Caching (Windows Internet)

Die WinINet-Funktionen verfügen über einfache, aber flexible, integrierte Cacheunterstützung. Alle aus dem Netzwerk abgerufenen Daten werden auf der Festplatte zwischengespeichert und für nachfolgende Anforderungen abgerufen. Die Anwendung kann die Zwischenspeicherung bei jeder Anforderung steuern. Bei HTTP-Anforderungen vom Server werden die meisten empfangenen Header ebenfalls zwischengespeichert. Wenn eine HTTP-Anforderung aus dem Cache erfüllt wird, werden die zwischengespeicherten Header auch an den Aufrufer zurückgegeben. Dadurch wird der Datendownload nahtlos, unabhängig davon, ob die Daten aus dem Cache oder aus dem Netzwerk stammen.

Anwendungen müssen einen Puffer ordnungsgemäß zuordnen, um die gewünschten Ergebnisse zu erhalten, wenn die persistenten URL-Zwischenspeicherfunktionen verwendet werden. Weitere Informationen finden Sie unter [Verwenden von Puffern.](appendix-b-using-buffers.md)

## <a name="cache-behavior-during-response-processing"></a>Cacheverhalten während der Antwortverarbeitung

Der WinINet-Cache ist mit den in RFC 2616 beschriebenen HTTP-Cachesteuerungsdirektiven kompatibel. Die Cachesteuerungsdirektiven und Anwendungssatzflags bestimmen, was zwischengespeichert werden kann. WinINet bestimmt jedoch anhand des folgenden Kriteriums, was tatsächlich zwischengespeichert wird:

-   WinINet speichert nur HTTP- und FTP-Antworten zwischen.
-   Nur gut verhaltene Antworten können von einem Cache gespeichert und in einer Antwort auf eine nachfolgende Anforderung verwendet werden. Gut reagierende Antworten werden als Antworten definiert, die erfolgreich zurückgegeben werden.
-   WinINet speichert erfolgreiche Antworten standardmäßig zwischen, es sei denn, entweder eine Cachesteuerungsdirektive vom Server oder ein anwendungsdefiniertes Flag geben ausdrücklich an, dass die Antwort möglicherweise nicht zwischengespeichert wird.
-   Im Allgemeinen werden Antworten auf das GET-Verb zwischengespeichert, wenn die oben aufgeführten Anforderungen erfüllt sind. Antworten auf PUT- und POST-Verben werden unter keinen Umständen zwischengespeichert.
-   Elemente werden auch dann zwischengespeichert, wenn der Cache voll ist. Wenn ein hinzugefügtes Element den Cache über das Größenlimit setzt, wird der Cachespeicher geplant. Standardmäßig ist nicht garantiert, dass Elemente mehr als 10 Minuten im Cache verbleiben. Weitere Informationen finden Sie weiter unten im Abschnitt [Cache scavenger.](#cache-scavenger)
-   HTTPS wird standardmäßig zwischengespeichert. Dies wird durch eine globale Einstellung verwaltet, die nicht durch anwendungsdefinierte Cachedirektiven überschrieben werden kann. Um die globale Einstellung außer Kraft zu setzen, wählen Sie in der Systemsteuerung das Applet Internetoptionen aus, und wechseln Sie zur Registerkarte Erweitert. Aktivieren Sie im Abschnitt "Sicherheit" das Kontrollkästchen "Verschlüsselte Seiten nicht auf Datenträger speichern".

## <a name="cache-scavenger"></a>Cache Scavenger

Der Cachespeicher bereinigt in regelmäßigen Abständen Elemente aus dem Cache. Wenn dem Cache ein Element hinzugefügt wird und der Cache voll ist, wird das Element dem Cache hinzugefügt, und der Cachespeicher wird geplant. Wenn der Cachespeicher eine Kapselungsrunde abschließt und der Cache das Cachelimit nicht erreicht hat, wird für den Cache eine weitere Runde geplant, wenn dem Cache ein anderes Element hinzugefügt wird. Im Allgemeinen wird der Scavenger geplant, wenn ein hinzugefügtes Element den Cache über die Größenbeschränkung setzt. Standardmäßig ist die Mindestlebensdauer im Cache auf 10 Minuten festgelegt, sofern in einer Cachesteuerungsdirektive nichts anderes angegeben ist. Wenn der Cachespeicher initiiert wird, gibt es keine Garantie dafür, dass die ältesten Elemente die ersten elemente sind, die aus dem Cache gelöscht werden.

Der Cache wird für alle WinINet-Anwendungen auf dem Computer für denselben Benutzer freigegeben. Ab Windows Vista und Windows Server 2008 wird die Cachegröße auf 1/32 und die Größe des Datenträgers mit einer Mindestgröße von 8 MB und einer maximalen Größe von 50 MB festgelegt.

## <a name="using-flags-to-control-caching"></a>Verwenden von Flags zum Steuern der Zwischenspeicherung

Mithilfe der Zwischenspeicherungsflags kann eine Anwendung steuern, wann und wie der Cache verwendet wird. Diese Flags können allein oder in Kombination mit dem *dwFlags-Parameter* in Funktionen verwendet werden, die auf Informationen oder Ressourcen im Internet zugreifen. Standardmäßig speichern die Funktionen alle aus dem Internet heruntergeladenen Daten.

Die folgenden Flags können verwendet werden, um das Zwischenspeichern zu steuern.



| Wert                                                                                                                                                  | Bedeutung                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|--------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**INTERNET \_ FLAG \_ CACHE \_ ASYNC**](api-flags.md)                                                                            | Dieses Flag hat keine Wirkung.                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| [**\_INTERNETFLAGCACHE \_ BEI \_ \_ \_ NET-FEHLER**](api-flags.md)                                                              | Gibt die Ressource aus dem Cache zurück, wenn die Netzwerkanforderung für die Ressource aufgrund eines FEHLERS BEI [ \_ DER \_ \_ ZURÜCKSETZUNG](wininet-errors.md) DER INTERNETVERBINDUNG oder eines [FEHLERS INTERNET CANNOT \_ \_ \_ CONNECT](wininet-errors.md) fehlschlägt. Dieses Flag wird von [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta)verwendet.                                                                                                              |
| [**\_INTERNETFLAG \_ DONT \_ CACHE**](api-flags.md)                                                                              | Speichert die Daten weder lokal noch in gateways zwischen. Identisch mit dem bevorzugten Wert, [**INTERNET FLAG NO CACHE \_ \_ \_ \_ WRITE**](api-flags.md).                                                                                                                                                                                                                                                                                 |
|                                                                                                                                                        | Gibt an, dass es sich um eine Formularübermittlung handelt.                                                                                                                                                                                                                                                                                                                                                                                                                        |
| [**INTERNET \_ FLAG \_ FROM \_ CACHE**](api-flags.md)[**INTERNET FLAG FORMS \_ \_ \_ SUBMIT**](api-flags.md) | Stellt keine Netzwerkanforderungen. Alle Entitäten werden aus dem Cache zurückgegeben. Wenn sich das angeforderte Element nicht im Cache befindet, wird ein geeigneter Fehler zurückgegeben, z. B. ERROR \_ FILE \_ NOT \_ FOUND. Nur die [**InternetOpen-Funktion**](/windows/desktop/api/Wininet/nf-wininet-internetopena) verwendet dieses Flag.                                                                                                                                                                                                       |
| [**\_ \_ INTERNETFLAG FWD \_ BACK**](api-flags.md)                                                                                  | Gibt an, dass die Funktion die Kopie der Ressource verwenden soll, die sich derzeit im Internetcache befindet. Das Ablaufdatum und andere Informationen zur Ressource werden nicht überprüft. Wenn das angeforderte Element nicht im Internetcache gefunden wird, versucht das System, die Ressource im Netzwerk zu finden. Dieser Wert wurde in Microsoft Internet Explorer 5 eingeführt und ist **den** Vorwärts- und Zurück-Schaltflächenvorgängen von Internet Explorer zugeordnet.  |
| [**\_ \_ INTERNETFLAGLINK**](api-flags.md)                                                                                 | Erzwingt, dass die Anwendung eine Ressource erneut lädt, wenn keine Ablaufzeit und kein Zeitpunkt der letzten Änderung zurückgegeben wurde, als die Ressource im Cache gespeichert wurde.                                                                                                                                                                                                                                                                                                                  |
| [**\_INTERNETFLAG \_ MAKE \_ PERSISTENT**](api-flags.md)                                                                    | Wird nicht mehr unterstützt.                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| [**\_INTERNETFLAG \_ MUSS ANFORDERUNG \_ \_ ZWISCHENSPEICHERN**](api-flags.md)                                                             | Bewirkt, dass eine temporäre Datei erstellt wird, wenn die Datei nicht zwischengespeichert werden kann. Dies ist identisch mit dem bevorzugten Wert INTERNET [**\_ FLAG NEED \_ \_ FILE**](api-flags.md).                                                                                                                                                                                                                                                                            |
| [**\_INTERNETFLAG: \_ DATEI ERFORDERLICH \_**](api-flags.md)                                                                                | Bewirkt, dass eine temporäre Datei erstellt wird, wenn die Datei nicht zwischengespeichert werden kann.                                                                                                                                                                                                                                                                                                                                                                                               |
| [**\_INTERNETFLAG \_ KEIN \_ \_ CACHESCHREIBVORGANG**](api-flags.md)                                                                     | Lehnt jeden Versuch der Funktion ab, aus dem Internet heruntergeladene Daten im Cache zu speichern. Dieses Flag ist erforderlich, wenn die Anwendung nicht möchte, dass heruntergeladene Ressourcen lokal gespeichert werden.                                                                                                                                                                                                                                                               |
| [**\_INTERNETFLAG \_ KEINE \_ BENUTZEROBERFLÄCHE**](api-flags.md)                                                                                        | Deaktiviert das Dialogfeld "Cookie". Dieses Flag kann von [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) und [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) (nur HTTP-Anforderungen) verwendet werden.                                                                                                                                                                                                                                                                                          |
| [**\_INTERNETFLAG \_ OFFLINE**](api-flags.md)                                                                                     | Verhindert, dass die Anwendung Anforderungen an das Netzwerk sendet. Alle Anforderungen werden mithilfe der im Cache gespeicherten Ressourcen aufgelöst. Wenn sich die Ressource nicht im Cache befindet, wird ein geeigneter Fehler zurückgegeben, z. B. ERROR \_ FILE \_ NOT \_ FOUND.                                                                                                                                                                                                                            |
| [**\_INTERNETFLAG \_ PRAGMA \_ NOCACHE**](api-flags.md)                                                                      | Erzwingt, dass die Anforderung vom Ursprungsserver aufgelöst wird, auch wenn eine zwischengespeicherte Kopie auf dem Proxy vorhanden ist. Die [**Funktion InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) (nur bei HTTP- und HTTPS-Anforderungen) und [**die HttpOpenRequest-Funktion**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) verwenden dieses Flag.                                                                                                                                                                                               |
| [**ERNEUTES \_ LADEN DES INTERNETFLAGS \_**](api-flags.md)                                                                                       | Erzwingt, dass die Funktion die angeforderte Ressource direkt aus dem Internet abruft. Die heruntergeladenen Informationen werden im Cache gespeichert.                                                                                                                                                                                                                                                                                                                     |
| [**\_INTERNETFLAG \_ NEU SYNCHRONISIEREN**](api-flags.md)                                                                         | Bewirkt, dass eine Anwendung einen bedingten Download der Ressource aus dem Internet ausführt. Wenn die im Cache gespeicherte Version aktuell ist, werden die Informationen aus dem Cache heruntergeladen. Andernfalls werden die Informationen erneut vom Server geladen.                                                                                                                                                                                                                   |



 

## <a name="persistent-caching-functions"></a>Funktionen für persistentes Zwischenspeichern

Clients, die persistente Cachedienste benötigen, verwenden die Funktionen für das persistente Zwischenspeichern, um ihren Anwendungen das Speichern von Daten im lokalen Dateisystem zur späteren Verwendung zu ermöglichen, z. B. in Situationen, in denen ein Link mit geringer Bandbreite den Zugriff auf die Daten einschränkt oder der Zugriff überhaupt nicht verfügbar ist.

Die Cachefunktionen bieten persistentes Zwischenspeichern und Offlinebrowsen. Sofern das [**FLAG INTERNET FLAG NO CACHE \_ \_ \_ \_ WRITE**](api-flags.md) nicht explizit keine Zwischenspeicherung angibt, werden alle aus dem Netzwerk heruntergeladenen Daten von den Funktionen zwischengespeichert. Die Antworten auf POST-Daten werden nicht zwischengespeichert.

## <a name="using-the-persistent-url-cache-functions"></a>Verwenden der persistenten URL-Cachefunktionen

Mit den folgenden persistenten URL-Cachefunktionen kann eine Anwendung auf im Cache gespeicherte Informationen zugreifen und diese bearbeiten.



| Funktion                                                           | BESCHREIBUNG                                                                                                                                                   |
|--------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CommitUrlCacheEntryA**](/windows/desktop/api/Wininet/nf-wininet-commiturlcacheentrya)               | Speichert Daten in der angegebenen Datei im Cachespeicher zwischen und ordnet sie der angegebenen URL zu.                                                                  |
| [**CommitUrlCacheEntryW**](/windows/desktop/api/Wininet/nf-wininet-commiturlcacheentryw)               | Speichert Daten in der angegebenen Datei im Cachespeicher zwischen und ordnet sie der angegebenen URL zu.                                                                  |
| [**CreateUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-createurlcacheentrya)                 | Ordnet den angeforderten Cachespeicher zu und erstellt einen lokalen Dateinamen zum Speichern des Cacheeintrags, der dem Quellnamen entspricht.                           |
| [**CreateUrlCacheGroup**](/windows/desktop/api/Wininet/nf-wininet-createurlcachegroup)                 | Generiert eine Cachegruppenidentifikation.                                                                                                                       |
| [**DeleteUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-deleteurlcacheentry)                 | Entfernt die dem Quellnamen zugeordnete Datei aus dem Cache, wenn die Datei vorhanden ist.                                                                          |
| [**DeleteUrlCacheGroup**](/windows/desktop/api/Wininet/nf-wininet-deleteurlcachegroup)                 | Gibt eine **GROUPID** und alle zugeordneten Zustände in der Cacheindexdatei frei.                                                                                      |
| [**FindCloseUrlCache**](/windows/desktop/api/Wininet/nf-wininet-findcloseurlcache)                     | Schließt das angegebene Enumerationshandle.                                                                                                                      |
| [**FindFirstUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-findfirsturlcacheentrya)           | Startet die Enumeration des Caches.                                                                                                                          |
| [**FindFirstUrlCacheEntryEx**](/windows/desktop/api/Wininet/nf-wininet-findfirsturlcacheentryexa)       | Startet eine gefilterte Enumeration des Caches.                                                                                                                   |
| [**FindNextUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-findnexturlcacheentrya)             | Ruft den nächsten Eintrag im Cache ab.                                                                                                                        |
| [**FindNextUrlCacheEntryEx**](/windows/desktop/api/Wininet/nf-wininet-findnexturlcacheentryexa)         | Ruft den nächsten Eintrag in einer gefilterten Cacheenumeration ab.                                                                                                     |
| [**GetUrlCacheEntryInfo**](/windows/desktop/api/Wininet/nf-wininet-geturlcacheentryinfoa)               | Ruft Informationen zu einem Cacheeintrag ab.                                                                                                                    |
| [**GetUrlCacheEntryInfoEx**](/windows/desktop/api/Wininet/nf-wininet-geturlcacheentryinfoexa)           | Sucht nach der URL, nachdem zwischengespeicherte Umleitungen übersetzt wurden, die im Offlinemodus von [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta)angewendet werden.           |
| [**ReadUrlCacheEntryStream**](/windows/desktop/api/Wininet/nf-wininet-readurlcacheentrystream)         | Liest die zwischengespeicherten Daten aus einem Stream, der mit [**RetrieveUrlCacheEntryStream**](/windows/desktop/api/Wininet/nf-wininet-retrieveurlcacheentrystreama)geöffnet wurde.                            |
| [**RetrieveUrlCacheEntryFile**](/windows/desktop/api/Wininet/nf-wininet-retrieveurlcacheentryfilea)     | Ruft einen Cacheeintrag aus dem Cache in Form einer Datei ab.                                                                                                 |
| [**RetrieveUrlCacheEntryStream**](/windows/desktop/api/Wininet/nf-wininet-retrieveurlcacheentrystreama) | Stellt die effizienteste und implementierungsunabhängigste Methode für den Zugriff auf die Cachedaten bereit.                                                                   |
| [**SetUrlCacheEntryGroup**](/windows/desktop/api/Wininet/nf-wininet-seturlcacheentrygroup)             | Fügt Einer Cachegruppe Einträge hinzu oder entfernt diese.                                                                                                                   |
| [**SetUrlCacheEntryInfo**](/windows/desktop/api/Wininet/nf-wininet-seturlcacheentryinfoa)               | Legt die angegebenen Member der [**INTERNET \_ CACHE ENTRY \_ \_ INFO-Struktur**](/windows/desktop/api/Wininet/ns-wininet-internet_cache_entry_infoa) fest.                                                |
| [**UnlockUrlCacheEntryFile**](/windows/desktop/api/Wininet/nf-wininet-unlockurlcacheentryfile)         | Entsperrt den Cacheeintrag, der gesperrt wurde, als die Datei zur Verwendung aus dem Cache von [**RetrieveUrlCacheEntryFile**](/windows/desktop/api/Wininet/nf-wininet-retrieveurlcacheentryfilea)abgerufen wurde. |
| [**UnlockUrlCacheEntryStream**](/windows/desktop/api/Wininet/nf-wininet-unlockurlcacheentrystream)     | Schließt den Stream, der mit [**RetrieveUrlCacheEntryStream**](/windows/desktop/api/Wininet/nf-wininet-retrieveurlcacheentrystreama)abgerufen wurde.                                           |



 

### <a name="enumerating-the-cache"></a>Aufzählen des Caches

Die Funktionen [**FindFirstUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-findfirsturlcacheentrya) und [**FindNextUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-findnexturlcacheentrya) enthalten die im Cache gespeicherten Informationen. [**FindFirstUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-findfirsturlcacheentrya) startet die Enumeration, indem ein Suchmuster, ein Puffer und eine Puffergröße verwendet werden, um ein Handle zu erstellen und den ersten Cacheeintrag zurückzugeben. [**FindNextUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-findnexturlcacheentrya) übernimmt das von [**FindFirstUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-findfirsturlcacheentrya)erstellte Handle, einen Puffer und eine Puffergröße, um den nächsten Cacheeintrag zurückzugeben.

Beide Funktionen speichern eine [**INTERNET \_ CACHE ENTRY \_ \_ INFO-Struktur**](/windows/desktop/api/Wininet/ns-wininet-internet_cache_entry_infoa) im Puffer. Die Größe dieser Struktur variiert für jeden Eintrag. Wenn die an eine der Beiden Funktionen übergebene Puffergröße unzureichend ist, schlägt die Funktion fehl, und [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) gibt ERROR \_ INSUFFICIENT BUFFER \_ zurück. Die Puffergrößenvariable enthält die Puffergröße, die zum Abrufen dieses Cacheeintrags benötigt wurde. Ein Puffer der durch die Puffergrößenvariablen angegebenen Größe sollte zugeordnet werden, und die Funktion sollte mit dem neuen Puffer erneut aufgerufen werden.

Die [**INTERNET CACHE ENTRY \_ \_ \_ INFO-Struktur**](/windows/desktop/api/Wininet/ns-wininet-internet_cache_entry_infoa) enthält die Strukturgröße, die URL der zwischengespeicherten Informationen, den lokalen Dateinamen, den Cacheeintragstyp, die Anzahl der Verwendungsdaten, die Trefferrate, die Größe, den Zeitpunkt der letzten Änderung, den Ablauf, den letzten Zugriff, die letzte Synchronisierungszeit, Headerinformationen, die Größe der Headerinformationen und die Dateinamenerweiterung.

Die [**FindFirstUrlCacheEntry-Funktion**](/windows/desktop/api/Wininet/nf-wininet-findfirsturlcacheentrya) nimmt ein Suchmuster, einen Puffer, der die [**INTERNET CACHE ENTRY \_ \_ \_ INFO-Struktur**](/windows/desktop/api/Wininet/ns-wininet-internet_cache_entry_infoa) speichert, und die Puffergröße an. Derzeit wird nur das Standardsuchmuster implementiert, das alle Cacheeinträge zurückgibt.

Nachdem der Cache aufgelistet wurde, sollte die Anwendung [**FindCloseUrlCache**](/windows/desktop/api/Wininet/nf-wininet-findcloseurlcache) aufrufen, um das Cacheenumerationshandle zu schließen.

Im folgenden Beispiel wird die URL jedes Cacheeintrags in einem Listenfeld **IDC \_ CacheList** angezeigt. Sie verwendet MAX \_ CACHE ENTRY INFO SIZE zum \_ \_ \_ anfänglichen Zuordnen eines Puffers, da frühe Versionen der WinINet-API den Cache andernfalls nicht ordnungsgemäß aufzählen. In späteren Versionen wird der Cache ordnungsgemäß aufzählt, und es gibt kein Limit für die Cachegröße. Alle Anwendungen, die auf Computern mit der Version der WinINet-API von Internet Explorer 4.0 ausgeführt werden, müssen einen Puffer der erforderlichen Größe zuordnen. Weitere Informationen finden Sie unter [Verwenden von Puffern.](appendix-b-using-buffers.md)


```C++
int WINAPI EnumerateCacheOld(HWND hX)
{
    DWORD dwEntrySize;
    LPINTERNET_CACHE_ENTRY_INFO lpCacheEntry;
    DWORD MAX_CACHE_ENTRY_INFO_SIZE = 4096;
    HANDLE hCacheDir;
    int nCount=0;

    SendDlgItemMessage(hX,IDC_CacheList,LB_RESETCONTENT,0,0);
    
    SetCursor(LoadCursor(NULL,IDC_WAIT));

    dwEntrySize = MAX_CACHE_ENTRY_INFO_SIZE;
    lpCacheEntry = (LPINTERNET_CACHE_ENTRY_INFO) new char[dwEntrySize];
    lpCacheEntry->dwStructSize = dwEntrySize;

again:

    hCacheDir = FindFirstUrlCacheEntry(NULL,
                                       lpCacheEntry,
                                       &dwEntrySize);
    if (!hCacheDir)                                             
    {
        delete[]lpCacheEntry;
        switch(GetLastError())
        {
            case ERROR_NO_MORE_ITEMS: 
                TCHAR tempout[80];
                _stprintf_s(tempout, 
                            80,   
                            TEXT("The number of cache entries = %d \n"),
                            nCount);
                MessageBox(hX,tempout,TEXT("Cache Enumeration"),MB_OK);
                FindCloseUrlCache(hCacheDir);
                SetCursor(LoadCursor(NULL,IDC_ARROW));
                return TRUE;
                break;
            case ERROR_INSUFFICIENT_BUFFER:
                lpCacheEntry = (LPINTERNET_CACHE_ENTRY_INFO) 
                                new char[dwEntrySize];
                lpCacheEntry->dwStructSize = dwEntrySize;
                goto again;
                break;
            default:
                ErrorOut( hX,GetLastError(),
                          TEXT("FindNextUrlCacheEntry Init"));
                FindCloseUrlCache(hCacheDir);
                SetCursor(LoadCursor(NULL,IDC_ARROW));
                return FALSE;
        }
    }

    SendDlgItemMessage(hX,IDC_CacheList,LB_ADDSTRING,
                       0,(LPARAM)(lpCacheEntry->lpszSourceUrlName));
    nCount++;
    delete (lpCacheEntry);

    do 
    {
        dwEntrySize = MAX_CACHE_ENTRY_INFO_SIZE;
        lpCacheEntry = (LPINTERNET_CACHE_ENTRY_INFO) new char[dwEntrySize];
        lpCacheEntry->dwStructSize = dwEntrySize;

retry:
        if (!FindNextUrlCacheEntry(hCacheDir,
                                   lpCacheEntry, 
                                   &dwEntrySize))
        {
            delete[]lpCacheEntry;
            switch(GetLastError())
            {
                case ERROR_NO_MORE_ITEMS: 
                    TCHAR tempout[80];
                    _stprintf_s(tempout,
                                80,
                                TEXT("The number of cache entries = %d \n"),nCount);
                    MessageBox(hX,
                               tempout,
                               TEXT("Cache Enumeration"),MB_OK);
                    FindCloseUrlCache(hCacheDir);
                    return TRUE;
                    break;
                case ERROR_INSUFFICIENT_BUFFER:
                    lpCacheEntry = 
                             (LPINTERNET_CACHE_ENTRY_INFO) 
                              new char[dwEntrySize];
                    lpCacheEntry->dwStructSize = dwEntrySize;
                    goto retry;
                    break;
                default:
                    ErrorOut(hX,
                             GetLastError(),
                             TEXT("FindNextUrlCacheEntry Init"));
                    FindCloseUrlCache(hCacheDir);
                    return FALSE;
            }
        }

        SendDlgItemMessage(hX,
                           IDC_CacheList,LB_ADDSTRING,
                           0,
                          (LPARAM)(lpCacheEntry->lpszSourceUrlName));
        nCount++;
        delete[] lpCacheEntry;        
    }  while (TRUE);

    SetCursor(LoadCursor(NULL,IDC_ARROW));
    return TRUE;        
}
```



### <a name="retrieving-cache-entry-information"></a>Abrufen von Cacheeintragsinformationen

Mit der [**GetUrlCacheEntryInfo-Funktion**](/windows/desktop/api/Wininet/nf-wininet-geturlcacheentryinfoa) können Sie die [**INTERNET CACHE ENTRY \_ \_ \_ INFO-Struktur**](/windows/desktop/api/Wininet/ns-wininet-internet_cache_entry_infoa) für die angegebene URL abrufen. Diese Struktur enthält die Strukturgröße, die URL der zwischengespeicherten Informationen, den lokalen Dateinamen, den Cacheeintragstyp, die Anzahl der Verwendungen, die Trefferrate, die Größe, den Zeitpunkt der letzten Änderung, den Ablauf, den letzten Zugriff, den Zeitpunkt der letzten Synchronisierung, Headerinformationen, die Größe der Headerinformationen und die Dateinamenerweiterung.

[**GetUrlCacheEntryInfo**](/windows/desktop/api/Wininet/nf-wininet-geturlcacheentryinfoa) akzeptiert eine URL, einen Puffer für eine [**INTERNET CACHE ENTRY \_ \_ \_ INFO-Struktur**](/windows/desktop/api/Wininet/ns-wininet-internet_cache_entry_infoa) und die Puffergröße. Wenn die URL gefunden wird, werden die Informationen in den Puffer kopiert. Andernfalls schlägt die Funktion fehl, und [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) gibt ERROR \_ FILE NOT FOUND \_ \_ zurück. Wenn die Puffergröße nicht ausreicht, um die Cacheeintragsinformationen zu speichern, schlägt die Funktion fehl, und [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) gibt ERROR \_ INSUFFICIENT BUFFER \_ zurück. Die zum Abrufen der Informationen erforderliche Größe wird in der Puffergrößenvariablen gespeichert.

[**GetUrlCacheEntryInfo**](/windows/desktop/api/Wininet/nf-wininet-geturlcacheentryinfoa) führt keine URL-Analyse durch, sodass eine URL, die einen Anker ( \# ) enthält, nicht im Cache gefunden wird, auch wenn die Ressource zwischengespeichert wird. Wenn beispielsweise die URL " https://example.com/example.htm\#sample " " übergeben wird, gibt die Funktion ERROR \_ FILE NOT FOUND \_ \_ zurück, auch wenn " " https://example.com/example.htm sich im Cache befindet.

Im folgenden Beispiel werden die Cacheeintragsinformationen für die angegebene URL abgerufen. Die Funktion zeigt dann die Headerinformationen im **Bearbeitungsfeld IDC \_ CacheDump** an.


```C++
int WINAPI GetCacheEntryInfo(HWND hX,LPTSTR lpszUrl)
{
    DWORD dwEntrySize=0;
    LPINTERNET_CACHE_ENTRY_INFO lpCacheEntry;

    SetCursor(LoadCursor(NULL,IDC_WAIT));
    if (!GetUrlCacheEntryInfo(lpszUrl,NULL,&dwEntrySize))
    {
        if (GetLastError()!=ERROR_INSUFFICIENT_BUFFER)
        {
            ErrorOut(hX,GetLastError(),TEXT("GetUrlCacheEntryInfo"));
            SetCursor(LoadCursor(NULL,IDC_ARROW));
            return FALSE;
        }
        else
            lpCacheEntry = (LPINTERNET_CACHE_ENTRY_INFO) 
                            new char[dwEntrySize];
    }
    else
        return FALSE; // should not be successful w/ NULL buffer
                      // and 0 size

    if (!GetUrlCacheEntryInfo(lpszUrl,lpCacheEntry,&dwEntrySize))
    {
        ErrorOut(hX,GetLastError(),TEXT("GetUrlCacheEntryInfo"));
        SetCursor(LoadCursor(NULL,IDC_ARROW));
        return FALSE;
    }
    else
    {
        if ((lpCacheEntry->dwHeaderInfoSize)!=0)
        {
            LPSTR(lpCacheEntry->lpHeaderInfo)
                                [lpCacheEntry->dwHeaderInfoSize]=TEXT('\0');
            SetDlgItemText(hX,IDC_Headers,
                           lpCacheEntry->lpHeaderInfo);
        }
        else
        {
            SetDlgItemText(hX,IDC_Headers,TEXT("None"));
        }

        SetCursor(LoadCursor(NULL,IDC_ARROW));
        return TRUE;
    }
        
}
```



### <a name="creating-a-cache-entry"></a>Erstellen eines Cacheeintrags

Eine Anwendung verwendet die Funktionen [**CreateUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-createurlcacheentrya) und [**CommitUrlCacheEntry,**](/windows/desktop/api/Wininet/nf-wininet-commiturlcacheentrya) um einen Cacheeintrag zu erstellen.

[**CreateUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-createurlcacheentrya) akzeptiert die URL, die erwartete Dateigröße und die Dateinamenerweiterung. Die Funktion erstellt dann einen lokalen Dateinamen zum Speichern des Cacheeintrags, der der URL- und Dateierweiterung entspricht.

Schreiben Sie die Daten unter Verwendung des lokalen Dateinamens in die lokale Datei. Nachdem die Daten in die lokale Datei geschrieben wurden, sollte die Anwendung [**CommitUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-commiturlcacheentrya)aufrufen.

[**CommitUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-commiturlcacheentrya) akzeptiert url, local file name, expiration, last modified time, cache entry type, header information, header information size und file name extension. Die Funktion speichert dann Daten in der im Cachespeicher angegebenen Datei zwischen und ordnet sie der angegebenen URL zu.

Im folgenden Beispiel wird der lokale Dateiname verwendet, der durch einen vorherigen Aufruf von [**CreateUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-createurlcacheentrya)erstellt wurde und im Textfeld **IDC \_ LocalFile** gespeichert ist, um den Text aus dem Textfeld **IDC \_ CacheDump** im Cacheeintrag zu speichern. Nachdem die Daten mit **fopen,** **fprintf** und **fclose** in die Datei geschrieben wurden, wird für den Eintrag [**commitUrlCacheEntry verwendet.**](/windows/desktop/api/Wininet/nf-wininet-commiturlcacheentrya)


```C++
int WINAPI CommitEntry(HWND hX)
{
    LPTSTR lpszUrl, lpszExt, lpszFileName;
    LPTSTR lpszData,lpszSize;
    DWORD dwSize;
    DWORD dwEntryType=0;
    FILE *lpfCacheEntry;
    LPFILETIME lpdtmExpire, lpdtmLastModified;
    LPSYSTEMTIME lpdtmSysTime;
    errno_t err;

    if( SendDlgItemMessage(hX,IDC_RBNormal,BM_GETCHECK,0,0) )
    {
        dwEntryType = dwEntryType + NORMAL_CACHE_ENTRY;
    }
    else if( SendDlgItemMessage(hX,IDC_RBSticky, BM_GETCHECK,0,0) )
    {
        dwEntryType = dwEntryType + STICKY_CACHE_ENTRY;
    }
    else if(SendDlgItemMessage( hX,IDC_RBSparse, BM_GETCHECK,0,0) )
    {
        dwEntryType = dwEntryType + SPARSE_CACHE_ENTRY;
    }
 

    if( SendDlgItemMessage(hX,IDC_RBCookie, BM_GETCHECK,0,0))
    {
            dwEntryType = dwEntryType + COOKIE_CACHE_ENTRY;
    }
    else if( SendDlgItemMessage(hX,IDC_RBUrl, BM_GETCHECK,0,0) )
    {
        dwEntryType = dwEntryType + URLHISTORY_CACHE_ENTRY;
    }


    if( SendDlgItemMessage(hX,IDC_RBNone, BM_GETCHECK,0,0) )
    {
        dwEntryType=0;
    }
        
    lpdtmSysTime = new SYSTEMTIME;
    lpdtmExpire = new FILETIME;
    lpdtmLastModified = new FILETIME;

    GetLocalTime(lpdtmSysTime);
    SystemTimeToFileTime(lpdtmSysTime,lpdtmExpire);
    SystemTimeToFileTime(lpdtmSysTime,lpdtmLastModified);
    delete(lpdtmSysTime);

    lpszUrl = new TCHAR[MAX_PATH];
    lpszFileName = new TCHAR[MAX_PATH];
    lpszExt = new TCHAR[5];
    lpszSize = new TCHAR[10];

    GetDlgItemText(hX,IDC_SourceURL,lpszUrl,MAX_PATH);
    GetDlgItemText(hX,IDC_LocalFile,lpszFileName,MAX_PATH);
    GetDlgItemText(hX,IDC_FileExt,lpszExt,5);

    GetDlgItemText(hX,IDC_SizeLow,lpszSize,10);
    dwSize = (DWORD)_ttol(lpszSize);
    delete(lpszSize);

    if (dwSize==0)
    {
        if((MessageBox(hX,
                       TEXT("Incorrect File Size.\nUsing 8000 characters, Okay?\n"),
                       TEXT("Commit Entry"),MB_YESNO))
                        ==IDYES)
        {
            dwSize = 8000;
        }
        else
        {
            return FALSE;
        }
    }

    lpszData = new TCHAR[dwSize];
    GetDlgItemText(hX,IDC_CacheDump,lpszData,dwSize);
        
     err = _tfopen_s(&lpfCacheEntry,lpszFileName,_T("w"));
     if (err)
        return FALSE;
    fprintf(lpfCacheEntry,"%s",lpszData);
    fclose(lpfCacheEntry);
    delete(lpszData);

    if ( !CommitUrlCacheEntry( lpszUrl, 
                               lpszFileName, 
                               *lpdtmExpire,
                               *lpdtmLastModified, 
                               dwEntryType,
                               NULL,
                               0,
                               lpszExt,
                               0) )
    {
        ErrorOut(hX,GetLastError(),TEXT("Commit Cache Entry"));
        delete(lpszUrl);
        delete(lpszFileName);
        delete(lpszExt);
        delete(lpdtmExpire);
        delete(lpdtmLastModified);
        return FALSE;
    }
    else
    {
        delete(lpszUrl);
        delete(lpszFileName);
        delete(lpszExt);
        delete(lpdtmExpire);
        delete(lpdtmLastModified);
        return TRUE;
    }
}
```



### <a name="deleting-a-cache-entry"></a>Löschen eines Cacheeintrags

Die [**DeleteUrlCacheEntry-Funktion**](/windows/desktop/api/Wininet/nf-wininet-deleteurlcacheentry) nimmt eine URL entgegen und entfernt die ihr zugeordnete Cachedatei. Wenn die Cachedatei nicht vorhanden ist, schlägt die Funktion fehl, und [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) gibt ERROR \_ FILE NOT FOUND \_ \_ zurück. Wenn die Cachedatei derzeit gesperrt ist oder verwendet wird, schlägt die Funktion fehl, und [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) gibt ERROR \_ ACCESS \_ DENIED zurück. Die Datei wird gelöscht, wenn sie entsperrt wird.

### <a name="retrieving-cache-entry-files"></a>Abrufen von Cacheeintragsdateien

Verwenden Sie für Anwendungen, die den Dateinamen einer Ressource benötigen, die Funktionen [**RetrieveUrlCacheEntryFile**](/windows/desktop/api/Wininet/nf-wininet-retrieveurlcacheentryfilea) und [**UnlockUrlCacheEntryFile.**](/windows/desktop/api/Wininet/nf-wininet-unlockurlcacheentryfile) Anwendungen, die den Dateinamen nicht benötigen, sollten die Funktionen [**RetrieveUrlCacheEntryStream,**](/windows/desktop/api/Wininet/nf-wininet-retrieveurlcacheentrystreama) [**ReadUrlCacheEntryStream**](/windows/desktop/api/Wininet/nf-wininet-readurlcacheentrystream)und [**UnlockUrlCacheEntryStream**](/windows/desktop/api/Wininet/nf-wininet-unlockurlcacheentrystream) verwenden, um die Informationen im Cache abzurufen.

[**RetrieveUrlCacheEntryStream**](/windows/desktop/api/Wininet/nf-wininet-retrieveurlcacheentrystreama) führt keine URL-Analyse durch, sodass eine URL, die einen Anker ( \# ) enthält, nicht im Cache gefunden wird, auch wenn die Ressource zwischengespeichert wird. Wenn beispielsweise die URL " https://example.com/example.htm\#sample " " übergeben wird, gibt die Funktion ERROR \_ FILE NOT FOUND \_ \_ zurück, auch wenn " " https://example.com/example.htm sich im Cache befindet.

[**RetrieveUrlCacheEntryFile**](/windows/desktop/api/Wininet/nf-wininet-retrieveurlcacheentryfilea) akzeptiert eine URL, einen Puffer, der die [**INTERNET CACHE ENTRY \_ \_ \_ INFO-Struktur**](/windows/desktop/api/Wininet/ns-wininet-internet_cache_entry_infoa) speichert, und die Puffergröße. Die Funktion wird abgerufen und für den Aufrufer gesperrt.

Nachdem die Informationen in der Datei verwendet wurden, sollte die Anwendung [**UnlockUrlCacheEntryFile**](/windows/desktop/api/Wininet/nf-wininet-unlockurlcacheentryfile) aufrufen, um die Datei zu entsperren.

### <a name="cache-groups"></a>Cachegruppen

Um eine Cachegruppe zu erstellen, muss die [**CreateUrlCacheGroup-Funktion**](/windows/desktop/api/Wininet/nf-wininet-createurlcachegroup) aufgerufen werden, um eine **GROUPID** für die Cachegruppe zu generieren. Einträge können der Cachegruppe hinzugefügt werden, indem sie die URL des Cacheeintrags und das \_ INTERNET CACHE \_ GROUP \_ ADD-Flag für die [**SetUrlCacheEntryGroup-Funktion**](/windows/desktop/api/Wininet/nf-wininet-seturlcacheentrygroup) angeben. Um einen Cacheeintrag aus einer Gruppe zu entfernen, übergeben Sie die URL des Cacheeintrags und das FLAG INTERNET \_ CACHE GROUP REMOVE an \_ \_ [**SetUrlCacheEntryGroup**](/windows/desktop/api/Wininet/nf-wininet-seturlcacheentrygroup).

Die Funktionen [**FindFirstUrlCacheEntryEx**](/windows/desktop/api/Wininet/nf-wininet-findfirsturlcacheentryexa) und [**FindNextUrlCacheEntryEx**](/windows/desktop/api/Wininet/nf-wininet-findnexturlcacheentryexa) können verwendet werden, um die Einträge in einer angegebenen Cachegruppe aufzuzählen. Nach Abschluss der Enumeration sollte die Funktion [**FindCloseUrlCache**](/windows/desktop/api/Wininet/nf-wininet-findcloseurlcache)aufrufen.

## <a name="handling-structures-with-variable-size-information"></a>Verarbeiten von Strukturen mit Variablengrößeninformationen

Der Cache kann Variablengrößeninformationen für jede gespeicherte URL enthalten. Dies wird in der [**INTERNET \_ CACHE ENTRY \_ \_ INFO-Struktur**](/windows/desktop/api/Wininet/ns-wininet-internet_cache_entry_infoa) widergespiegelt. Wenn die Cachefunktionen diese Struktur zurückgeben, erstellen sie einen Puffer, der immer die Größe von [**INTERNET \_ CACHE ENTRY \_ \_ INFO**](/windows/desktop/api/Wininet/ns-wininet-internet_cache_entry_infoa) sowie alle Variablengrößeninformationen aufweist. Wenn ein Zeigermember nicht **NULL** ist, zeigt es direkt nach der -Struktur auf den Speicherbereich. Beim Kopieren des Puffers, der von einer Funktion in einen anderen Puffer zurückgegeben wird, sollten die Zeigermember so korrigiert werden, dass sie auf die entsprechende Stelle im neuen Puffer zeigen, wie im folgenden Beispiel gezeigt.

``` syntax
lpDstCEInfo->lpszSourceUrlName = 
    (LPINTERNET_CACHE_ENTRY_INFO) ((LPBYTE) lpSrcCEInfo + 
       ((DWORD)(lpOldCEInfo->lpszSourceUrlName) - (DWORD)lpOldCEInfo));
```

Einige Cachefunktionen schlagen mit der Fehlermeldung ERROR \_ INSUFFICIENT \_ BUFFER fehl, wenn Sie einen Puffer angeben, der zu klein ist, um die von der Funktion abgerufenen Cacheeintragsinformationen zu enthalten. In diesem Fall gibt die Funktion auch die erforderliche Größe des Puffers zurück. Anschließend können Sie einen Puffer der entsprechenden Größe zuordnen und die Funktion erneut aufrufen.

> [!Note]  
> WinINet unterstützt keine Serverimplementierungen. Darüber hinaus sollte sie nicht von einem Dienst verwendet werden. Verwenden Sie für Serverimplementierungen oder -dienste [Microsoft Windows HTTP-Dienste (WinHTTP).](/windows/desktop/WinHttp/winhttp-start-page)

 

 

 
