---
title: Caching (Windows Internet)
description: Die WinInet-Funktionen verfügen über eine einfache, aber flexible integrierte Cache Unterstützung.
ms.assetid: 44c268c9-a745-432a-8540-60d7e7d2cb2d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e753d826ec3abe580b94158296562208dcbed44
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "104102679"
---
# <a name="caching-windows-internet"></a>Caching (Windows Internet)

Die WinInet-Funktionen verfügen über eine einfache, aber flexible integrierte Cache Unterstützung. Alle aus dem Netzwerk abgerufenen Daten werden auf der Festplatte zwischengespeichert und für nachfolgende Anforderungen abgerufen. Die Anwendung kann das Caching für jede Anforderung steuern. Bei HTTP-Anforderungen vom Server werden die meisten empfangenen Header ebenfalls zwischengespeichert. Wenn eine HTTP-Anforderung aus dem Cache erfüllt wird, werden die zwischengespeicherten Header auch an den Aufrufer zurückgegeben. Dadurch werden Daten nahtlos heruntergeladen, unabhängig davon, ob die Daten aus dem Cache oder aus dem Netzwerk stammen.

Anwendungen müssen einen Puffer ordnungsgemäß zuordnen, um die gewünschten Ergebnisse zu erhalten, wenn Sie die persistenten URL-zwischen Speicherungs Funktionen verwenden. Weitere Informationen finden Sie unter [Verwenden von Puffern](appendix-b-using-buffers.md).

## <a name="cache-behavior-during-response-processing"></a>Cache Verhalten während der Antwort Verarbeitung

Der WinInet-Cache ist kompatibel mit den HTTP-Cache-Control-Direktiven, die in RFC 2616 beschrieben werden. Die Cache-Control-Direktiven und anwendungssetflags bestimmen, was zwischengespeichert werden kann. Allerdings bestimmt WinInet, was nach dem folgenden Kriterium tatsächlich zwischengespeichert wird:

-   WinInet speichert nur http-und FTP-Antworten zwischen.
-   Nur gut verhaltene Antworten können von einem Cache gespeichert und in einer Antwort auf eine nachfolgende Anforderung verwendet werden. Wohl verhaltene Antworten werden als Antworten definiert, die erfolgreich zurückgegeben werden.
-   Standardmäßig speichert WinInet erfolgreiche Antworten zwischen, es sei denn, entweder eine Cache Steuerungs Direktive vom Server oder ein Anwendungs definiertes Flag gibt ausdrücklich an, dass die Antwort nicht zwischengespeichert werden darf.
-   Im Allgemeinen werden Antworten auf das Get-Verb zwischengespeichert, wenn die oben aufgeführten Anforderungen erfüllt sind. Antworten auf Put-und Post-Verben werden unter keinen Umständen zwischengespeichert.
-   Elemente werden zwischengespeichert, auch wenn der Cache voll ist. Wenn ein hinzugefügtes Element den Cache über der Größenbeschränkung überschreitet, wird die Cache-Scavenger geplant. Standardmäßig ist es nicht sichergestellt, dass Elemente im Cache mehr als 10 Minuten verbleiben. Weitere Informationen finden Sie im Abschnitt [Cache Scavenger](#cache-scavenger) weiter unten.
-   HTTPS wird standardmäßig zwischengespeichert. Dies wird durch eine globale Einstellung verwaltet, die nicht durch Anwendungs definierte Cache Direktiven überschrieben werden kann. Wenn Sie die globale Einstellung außer Kraft setzen möchten, wählen Sie in der Systemsteuerung das Applet Internet Optionen aus, und navigieren Sie zur Registerkarte Erweitert. Aktivieren Sie das Kontrollkästchen "verschlüsselte Seiten auf dem Datenträger nicht speichern" im Abschnitt "Sicherheit".

## <a name="cache-scavenger"></a>Scavenger Zwischenspeichern

Der Cache Scavenger bereinigt regelmäßig Elemente aus dem Cache. Wenn ein Element dem Cache hinzugefügt wird und der Cache voll ist, wird das Element dem Cache hinzugefügt, und der Cache Scavenger ist geplant. Wenn die Cache-Scavenger eine Rundungs Runde abgeschlossen hat und der Cache das Cache Limit nicht erreicht hat, wird für die Scavenger eine weitere Runde eingeplant, wenn dem Cache ein anderes Element hinzugefügt wird. Im Allgemeinen wird die Scavenger geplant, wenn ein hinzugefügtes Element den Cache über das Größenlimit hinaus verschiebt. Standardmäßig ist die minimale Gültigkeitsdauer im Cache auf 10 Minuten festgelegt, sofern in einer Cache Steuerungs Anweisung nichts anderes angegeben ist. Wenn die Cache-Scavenger initiiert wird, gibt es keine Garantie dafür, dass die ältesten Elemente als erstes aus dem Cache gelöscht werden.

Der Cache wird für denselben Benutzer für alle WinINet-Anwendungen auf dem Computer freigegeben. Ab Windows Vista und Windows Server 2008 ist die Cache Größe auf 1/32 ND die Größe des Datenträgers mit einer Mindestgröße von 8 MB und einer maximalen Größe von 50 MB festgelegt.

## <a name="using-flags-to-control-caching"></a>Verwenden von Flags zum Steuern der Zwischenspeicherung

Mithilfe der cacheflags kann eine Anwendung steuern, wann und wie Sie den Cache verwendet. Diese Flags können allein oder in Kombination mit dem *dwFlags* -Parameter in Funktionen verwendet werden, die auf Informationen oder Ressourcen im Internet zugreifen. Standardmäßig werden von den Funktionen alle aus dem Internet heruntergeladenen Daten gespeichert.

Die folgenden Flags können verwendet werden, um das Zwischenspeichern zu steuern.



| Wert                                                                                                                                                  | Bedeutung                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|--------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Internet- \_ Flag- \_ Cache \_ Async**](api-flags.md)                                                                            | Dieses Flag hat keine Wirkung.                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| [**Internet- \_ Flag- \_ Cache, \_ Wenn \_ net \_ fehlschlägt**](api-flags.md)                                                              | Gibt die Ressource aus dem Cache zurück, wenn die Netzwerk Anforderung für die Ressource aufgrund eines [Fehlers \_ beim \_ \_ Zurücksetzen der Internetverbindung](wininet-errors.md) oder des Fehlers " [ \_ Internet \_ kann nicht \_ verbunden](wininet-errors.md) werden" fehlschlägt. Dieses Flag wird von [**httpoperrequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta)verwendet.                                                                                                              |
| [**internetflag nicht zwischen \_ \_ \_ Speichern**](api-flags.md)                                                                              | Speichert die Daten weder lokal noch in Gateways. Identisch mit dem bevorzugten Wert, [**Internet \_ Flag \_ kein \_ Cache \_ Schreibvorgang**](api-flags.md).                                                                                                                                                                                                                                                                                 |
|                                                                                                                                                        | Gibt an, dass dies eine Formular Übermittlung ist.                                                                                                                                                                                                                                                                                                                                                                                                                        |
| [**Internet \_ Flag \_ aus \_ Cache**](api-flags.md)[**Internet \_ Flag zum über \_ \_ Mitteln von Formularen**](api-flags.md) | Keine Netzwerk Anforderungen. Alle Entitäten werden aus dem Cache zurückgegeben. Wenn sich das angeforderte Element nicht im Cache befindet, wird ein geeigneter Fehler (z \_ . b. Fehler Datei \_ nicht \_ gefunden) zurückgegeben. Nur die [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena) -Funktion verwendet dieses Flag.                                                                                                                                                                                                       |
| [**Internet Kennzeichen- \_ Flag \_ \_ zurück**](api-flags.md)                                                                                  | Gibt an, dass die Funktion die Kopie der Ressource verwenden soll, die sich derzeit im Internet Cache befindet. Das Ablaufdatum und andere Informationen über die Ressource werden nicht geprüft. Wenn das angeforderte Element nicht im Internet Cache gefunden wird, versucht das System, die Ressource im Netzwerk zu finden. Dieser Wert wurde in Microsoft Internet Explorer 5 eingeführt und ist den vorwärts-und **rückwärts** -Schaltflächen **Vorgängen** von Internet Explorer zugeordnet. |
| [**Hyperlink zum Internet Kennzeichen \_ \_**](api-flags.md)                                                                                 | Zwingt die Anwendung, eine Ressource erneut zu laden, wenn keine Ablaufzeit und keine Zeit für die letzte Änderung zurückgegeben wurden, als die Ressource im Cache gespeichert wurde.                                                                                                                                                                                                                                                                                                                  |
| [**\_internetflag \_ \_ dauerhaft machen**](api-flags.md)                                                                    | Wird nicht mehr unterstützt.                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| [**Internet \_ Kennzeichen \_ muss \_ Anforderung Zwischenspeichern \_**](api-flags.md)                                                             | Bewirkt, dass eine temporäre Datei erstellt wird, wenn die Datei nicht zwischengespeichert werden kann. Dies ist identisch mit dem bevorzugten Wert, [**Internet \_ Flag \_ benötigt \_ Datei**](api-flags.md).                                                                                                                                                                                                                                                                            |
| [**Internet- \_ Flag \_ benötigt \_ Datei**](api-flags.md)                                                                                | Bewirkt, dass eine temporäre Datei erstellt wird, wenn die Datei nicht zwischengespeichert werden kann.                                                                                                                                                                                                                                                                                                                                                                                               |
| [**Internet \_ Kennzeichen \_ ohne \_ Cache \_ Schreibvorgang**](api-flags.md)                                                                     | Lehnt den Versuch der Funktion ab, aus dem Internet heruntergeladene Daten im Cache zu speichern. Dieses Flag ist erforderlich, wenn die Anwendung nicht möchten, dass heruntergeladene Ressourcen lokal gespeichert werden.                                                                                                                                                                                                                                                               |
| [**Internet \_ Flag \_ keine \_ Benutzeroberfläche**](api-flags.md)                                                                                        | Deaktiviert das Cookie-Dialogfeld. Dieses Flag kann von [**httpopanrequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) und [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) verwendet werden (nur HTTP-Anforderungen).                                                                                                                                                                                                                                                                                          |
| [**Internet- \_ Flag \_ Offline**](api-flags.md)                                                                                     | Verhindert, dass die Anwendung Anforderungen an das Netzwerk sendet. Alle Anforderungen werden mithilfe der im Cache gespeicherten Ressourcen aufgelöst. Wenn sich die Ressource nicht im Cache befindet, wird ein geeigneter Fehler (z \_ . b. Fehler Datei \_ nicht gefunden) \_ zurückgegeben.                                                                                                                                                                                                                            |
| [**Internet \_ Flag \_ pragma \_ NoCache**](api-flags.md)                                                                      | Erzwingt, dass die Anforderung vom Ursprungsserver aufgelöst wird, auch wenn eine zwischengespeicherte Kopie auf dem Proxy vorhanden ist. Die Funktion " [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) " (nur bei http-und HTTPS-Anforderungen) und die Funktion " [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) " verwenden dieses Flag.                                                                                                                                                                                               |
| [**Internet Kennzeichen erneut \_ \_ Laden**](api-flags.md)                                                                                       | Erzwingt, dass die Funktion die angeforderte Ressource direkt aus dem Internet abruft. Die heruntergeladenen Informationen werden im Cache gespeichert.                                                                                                                                                                                                                                                                                                                     |
| [**Internet- \_ Flag \_ erneut synchronisieren**](api-flags.md)                                                                         | Bewirkt, dass eine Anwendung einen bedingten Download der Ressource aus dem Internet ausführt. Wenn die im Cache gespeicherte Version aktuell ist, werden die Informationen aus dem Cache heruntergeladen. Andernfalls werden die Informationen vom Server erneut geladen.                                                                                                                                                                                                                   |



 

## <a name="persistent-caching-functions"></a>Persistente Caching-Funktionen

Clients, die persistente Cache Dienste benötigen, verwenden die persistenten Caching-Funktionen, um Ihren Anwendungen das Speichern von Daten im lokalen Dateisystem für die nachfolgende Verwendung zu ermöglichen, z. b. in Situationen, in denen eine Verbindung mit geringer Bandbreite den Zugriff auf die Daten einschränkt oder der Zugriff überhaupt nicht verfügbar ist.

Die Cache Funktionen bieten persistentes Zwischenspeichern und Offline-Browsen. Wenn das [**Internet \_ Flag \_ kein \_ Cache \_ Schreib**](api-flags.md) Flag explizit das Zwischenspeichern angibt, werden von den Funktionen alle aus dem Netzwerk heruntergeladenen Daten zwischengespeichert. Die Antworten auf Post-Daten werden nicht zwischengespeichert.

## <a name="using-the-persistent-url-cache-functions"></a>Verwenden der persistenten URL-Cache Funktionen

Mit den folgenden permanenten URL-Cache Funktionen kann eine Anwendung auf im Cache gespeicherte Informationen zugreifen und diese bearbeiten.



| Funktion                                                           | BESCHREIBUNG                                                                                                                                                   |
|--------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Commiturlcacheentrya**](/windows/desktop/api/Wininet/nf-wininet-commiturlcacheentrya)               | Speichert Daten in der angegebenen Datei im Cache Speicher zwischen und ordnet Sie der angegebenen URL zu.                                                                  |
| [**Commiturlcacheentryw**](/windows/desktop/api/Wininet/nf-wininet-commiturlcacheentryw)               | Speichert Daten in der angegebenen Datei im Cache Speicher zwischen und ordnet Sie der angegebenen URL zu.                                                                  |
| [**"Kreateurlcacheentry"**](/windows/desktop/api/Wininet/nf-wininet-createurlcacheentrya)                 | Ordnet den angeforderten Cache Speicher zu und erstellt einen lokalen Dateinamen zum Speichern des Cache Eintrags, der dem Quellnamen entspricht.                           |
| [**"Kreateurlcachegroup"**](/windows/desktop/api/Wininet/nf-wininet-createurlcachegroup)                 | Generiert eine Cache Gruppenidentifikation.                                                                                                                       |
| [**Deleteurlcacheentry**](/windows/desktop/api/Wininet/nf-wininet-deleteurlcacheentry)                 | Entfernt die Datei, die dem Quellnamen zugeordnet ist, aus dem Cache, wenn die Datei vorhanden ist.                                                                          |
| [**Deleteurlcachegroup**](/windows/desktop/api/Wininet/nf-wininet-deleteurlcachegroup)                 | Gibt eine **GroupID** und einen beliebigen zugeordneten Zustand in der Cache Indexdatei frei.                                                                                      |
| [**Findcloseurlcache**](/windows/desktop/api/Wininet/nf-wininet-findcloseurlcache)                     | Schließt das angegebene enumerationshandle.                                                                                                                      |
| [**Findfirsturlcacheentry**](/windows/desktop/api/Wininet/nf-wininet-findfirsturlcacheentrya)           | Beginnt die Enumeration des Caches.                                                                                                                          |
| [**Findfirsturlcacheentryex**](/windows/desktop/api/Wininet/nf-wininet-findfirsturlcacheentryexa)       | Beginnt eine gefilterte Enumeration des Caches.                                                                                                                   |
| [**Findnexturlcacheentry**](/windows/desktop/api/Wininet/nf-wininet-findnexturlcacheentrya)             | Ruft den nächsten Eintrag im Cache ab.                                                                                                                        |
| [**Findnexturlcacheentryex**](/windows/desktop/api/Wininet/nf-wininet-findnexturlcacheentryexa)         | Ruft den nächsten Eintrag in einer gefilterten Cache Enumeration ab.                                                                                                     |
| [**Geturlcacheentryinfo**](/windows/desktop/api/Wininet/nf-wininet-geturlcacheentryinfoa)               | Ruft Informationen zu einem Cache Eintrag ab.                                                                                                                    |
| [**Geturlcacheentryinfoex**](/windows/desktop/api/Wininet/nf-wininet-geturlcacheentryinfoexa)           | Sucht nach der URL, nachdem alle zwischengespeicherten Umleitungen übertragen wurden, die von [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta)im Offline Modus angewendet werden.           |
| [**"Read urlcacheentrystream"**](/windows/desktop/api/Wininet/nf-wininet-readurlcacheentrystream)         | Liest die zwischengespeicherten Daten aus einem Stream, der mithilfe von " [**retrieveurlcacheentrystream**](/windows/desktop/api/Wininet/nf-wininet-retrieveurlcacheentrystreama)" geöffnet wurde.                            |
| [**"Retrieveurlcacheentryfile"**](/windows/desktop/api/Wininet/nf-wininet-retrieveurlcacheentryfilea)     | Ruft einen Cache Eintrag aus dem Cache in Form einer Datei ab.                                                                                                 |
| [**"Retrieveurlcacheentrystream"**](/windows/desktop/api/Wininet/nf-wininet-retrieveurlcacheentrystreama) | Bietet die effizienteste und Implementierungs unabhängige Möglichkeit des Zugriffs auf die Cache Daten.                                                                   |
| [**"Tarturlcacheentrygroup"**](/windows/desktop/api/Wininet/nf-wininet-seturlcacheentrygroup)             | Fügt Einträge aus einer Cache Gruppe hinzu oder entfernt Sie.                                                                                                                   |
| [**"Tarturlcacheentryinfo"**](/windows/desktop/api/Wininet/nf-wininet-seturlcacheentryinfoa)               | Legt die angegebenen Elemente der [**Internet \_ Cache- \_ Eintrags \_ Informations**](/windows/desktop/api/Wininet/ns-wininet-internet_cache_entry_infoa) Struktur fest.                                                |
| [**Unlockurlcacheentryfile**](/windows/desktop/api/Wininet/nf-wininet-unlockurlcacheentryfile)         | Entsperrt den Cache Eintrag, der gesperrt war, als die Datei für die Verwendung im Cache durch " [**retrieveurlcacheentryfile**](/windows/desktop/api/Wininet/nf-wininet-retrieveurlcacheentryfilea)" abgerufen wurde. |
| [**Unlockurlcacheentrystream**](/windows/desktop/api/Wininet/nf-wininet-unlockurlcacheentrystream)     | Schließt den Datenstrom, der mithilfe von " [**retrieveurlcacheentrystream**](/windows/desktop/api/Wininet/nf-wininet-retrieveurlcacheentrystreama)" abgerufen wurde.                                           |



 

### <a name="enumerating-the-cache"></a>Auflisten des Caches

Die Funktionen [**findfirsturlcacheentry**](/windows/desktop/api/Wininet/nf-wininet-findfirsturlcacheentrya) und [**findnexturlcacheentry**](/windows/desktop/api/Wininet/nf-wininet-findnexturlcacheentrya) zählen die im Cache gespeicherten Informationen auf. [**Findfirsturlcacheentry**](/windows/desktop/api/Wininet/nf-wininet-findfirsturlcacheentrya) startet die Enumeration, indem ein Suchmuster, ein Puffer und eine Puffergröße zum Erstellen eines Handles und zum Zurückgeben des ersten Cache Eintrags übernommen werden. [**Findnexturlcacheentry**](/windows/desktop/api/Wininet/nf-wininet-findnexturlcacheentrya) übernimmt das von [**findfirsturlcacheentry**](/windows/desktop/api/Wininet/nf-wininet-findfirsturlcacheentrya)erstellte handle, einen Puffer und eine Puffergröße, um den nächsten Cache Eintrag zurückzugeben.

Beide Funktionen speichern eine [**Internet \_ Cache- \_ Eintrags \_ Informations**](/windows/desktop/api/Wininet/ns-wininet-internet_cache_entry_infoa) Struktur im Puffer. Die Größe dieser Struktur variiert je nach Eintrag. Wenn die an eine der beiden Funktionen über gegebene Puffergröße unzureichend ist, schlägt die Funktion fehl, und [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) gibt einen fehlerhaften \_ \_ Puffer zurück. Die Puffergrößen Variable enthält die Puffergröße, die zum Abrufen dieses Cache Eintrags benötigt wurde. Ein Puffer der Größe, die durch die Puffergrößen Variable angegeben wird, muss zugeordnet werden, und die Funktion sollte erneut mit dem neuen Puffer aufgerufen werden.

Die Informationsstruktur " [**Internet \_ Cache \_ Entry \_**](/windows/desktop/api/Wininet/ns-wininet-internet_cache_entry_infoa) " enthält die Struktur Größe, die URL der zwischengespeicherten Informationen, den lokalen Dateinamen, den Cache Eintrags Typ, die Anzahl der Treffer, die Treffer Rate, die Uhrzeit der letzten Änderung, den Ablauf, den letzten Zugriff, den Zeitpunkt der letzten Synchronisierung, Header Informationen, die Größe der Header Informationen und die Datei

Die [**findfirsturlcacheentry**](/windows/desktop/api/Wininet/nf-wininet-findfirsturlcacheentrya) -Funktion nimmt ein Suchmuster, einen Puffer, in dem die Informationsstruktur für den [**Internet \_ Cache \_ Eintrag \_**](/windows/desktop/api/Wininet/ns-wininet-internet_cache_entry_infoa) gespeichert ist, und die Puffergröße. Derzeit wird nur das Standard Suchmuster implementiert, das alle Cache Einträge zurückgibt.

Nachdem der Cache aufgezählt wurde, sollte die Anwendung [**findcloseurlcache**](/windows/desktop/api/Wininet/nf-wininet-findcloseurlcache) aufrufen, um das Cache-enumerationshandle zu schließen.

Im folgenden Beispiel wird die URL jedes Cache Eintrags in einem Listenfeld, **IDC \_ cachelist**, angezeigt. Sie verwendet \_ die maximale Größe der Cache \_ Eintrags \_ Informationen, \_ um anfänglich einen Puffer zuzuweisen, da die frühen Versionen der WinInet-API den Cache nicht ordnungsgemäß auflisten. Spätere Versionen zählen den Cache ordnungsgemäß auf, und es gibt keine Cache Größenbeschränkung. Alle Anwendungen, die auf Computern mit der Version der WinInet-API aus Internet Explorer 4,0 ausgeführt werden, müssen einen Puffer mit der erforderlichen Größe zuordnen. Weitere Informationen finden Sie unter [Verwenden von Puffern](appendix-b-using-buffers.md).


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



### <a name="retrieving-cache-entry-information"></a>Abrufen von Informationen zum Cache Eintrag

Mit der [**geturlcacheentryinfo**](/windows/desktop/api/Wininet/nf-wininet-geturlcacheentryinfoa) -Funktion können Sie die [**Internet \_ Cache \_ Entry \_ Info**](/windows/desktop/api/Wininet/ns-wininet-internet_cache_entry_infoa) -Struktur für die angegebene URL abrufen. Diese Struktur enthält die Struktur Größe, die URL der zwischengespeicherten Informationen, den lokalen Dateinamen, den Cache Eintrags Typ, die Anzahl, die Treffer Rate, die Größe, die Uhrzeit der letzten Änderung, den Ablauf, den letzten Zugriff, den Zeitpunkt der letzten Synchronisierung, Header Informationen, die Header Informations Größe und die Dateinamenerweiterung.

[**Geturlcacheentryinfo**](/windows/desktop/api/Wininet/nf-wininet-geturlcacheentryinfoa) akzeptiert eine URL, einen Puffer für eine [**Internet \_ Cache- \_ Eintrags \_ Informations**](/windows/desktop/api/Wininet/ns-wininet-internet_cache_entry_infoa) Struktur und die Puffergröße. Wenn die URL gefunden wird, werden die Informationen in den Puffer kopiert. Andernfalls schlägt die Funktion fehl, und [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) gibt die Fehler \_ Datei \_ nicht \_ gefunden zurück. Wenn die Puffergröße zum Speichern der Cache Eintrags Informationen unzureichend ist, tritt bei der Funktion ein Fehler auf, und [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) gibt einen \_ nicht ausreichenden \_ Puffer zurück. Die zum Abrufen der Informationen erforderliche Größe wird in der Puffergrößen Variablen gespeichert.

" [**Geturlcacheentryinfo**](/windows/desktop/api/Wininet/nf-wininet-geturlcacheentryinfoa) " führt keine URL-Verarbeitung aus, sodass eine URL, die einen Anker ( \# ) enthält, nicht im Cache gefunden wird, auch wenn die Ressource zwischengespeichert wird. Wenn z. b. die URL " https://example.com/example.htm\#sample " übermittelt wird, gibt die Funktion die Fehler \_ Datei nicht gefunden zurück, \_ \_ auch wenn https://example.com/example.htm sich "" im Cache befindet.

Im folgenden Beispiel werden die Cache Eintrags Informationen für die angegebene URL abgerufen. Die-Funktion zeigt dann die Header Informationen im Fenster " **IDC \_ cachedump** Edit" an.


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



### <a name="creating-a-cache-entry"></a>Erstellen eines Cache Eintrags

Eine Anwendung erstellt einen Cache Eintrag mithilfe der Funktionen " [**comateurlcacheentry**](/windows/desktop/api/Wininet/nf-wininet-createurlcacheentrya) " und " [**commiturlcacheentry**](/windows/desktop/api/Wininet/nf-wininet-commiturlcacheentrya) ".

" [**Kreateurlcacheentry**](/windows/desktop/api/Wininet/nf-wininet-createurlcacheentrya) " akzeptiert die URL, die erwartete Dateigröße und die Dateinamenerweiterung. Die-Funktion erstellt dann einen lokalen Dateinamen zum Speichern des Cache Eintrags, der der URL-und Dateinamenerweiterung entspricht.

Schreiben Sie die Daten mit dem Namen der lokalen Datei in die lokale Datei. Nachdem die Daten in die lokale Datei geschrieben wurden, sollte die Anwendung [**commiturlcacheentry**](/windows/desktop/api/Wininet/nf-wininet-commiturlcacheentrya)aufruft.

[**Commiturlcacheentry**](/windows/desktop/api/Wininet/nf-wininet-commiturlcacheentrya) akzeptiert die URL, den lokalen Dateinamen, den Ablauf, den Zeitpunkt der letzten Änderung, den Cache Eintrags Typ, die Header Informationen, die Header Informations Größe und die Dateinamenerweiterung. Die Funktion speichert dann Daten in der im Cache Speicher angegebenen Datei zwischen und ordnet Sie der angegebenen URL zu.

Im folgenden Beispiel wird der lokale [**Dateiname**](/windows/desktop/api/Wininet/nf-wininet-createurlcacheentrya)verwendet, der von einem vorherigen aufgerufen wurde, der im Textfeld **IDC \_ LocalFile** gespeichert wurde, um den Text aus dem Textfeld **IDC \_ cachedump** im Cache Eintrag zu speichern. Nachdem die Daten mithilfe von **fopen**, **fprintf** und **fclose** in die Datei geschrieben wurden, wird für den Eintrag mithilfe von [**commiturlcacheentry ein Commit**](/windows/desktop/api/Wininet/nf-wininet-commiturlcacheentrya)ausgeführt.


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



### <a name="deleting-a-cache-entry"></a>Löschen eines Cache Eintrags

Die [**deleteurlcacheentry**](/windows/desktop/api/Wininet/nf-wininet-deleteurlcacheentry) -Funktion nimmt eine URL an und entfernt die zugeordnete Cachedatei. Wenn die Cachedatei nicht vorhanden ist, schlägt die Funktion fehl, und [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) gibt die Fehler \_ Datei \_ nicht \_ gefunden zurück. Wenn die Cachedatei zurzeit gesperrt ist oder verwendet wird, schlägt die Funktion fehl, und [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) gibt den Fehler \_ Zugriff \_ verweigert zurück. Die Datei wird gelöscht, wenn Sie entsperrt wird.

### <a name="retrieving-cache-entry-files"></a>Abrufen von Cache Eintrags Dateien

Verwenden Sie für Anwendungen, für die der Dateiname einer Ressource erforderlich ist, die Funktionen " [**retrieveurlcacheentryfile**](/windows/desktop/api/Wininet/nf-wininet-retrieveurlcacheentryfilea) " und " [**unlockurlcacheentryfile**](/windows/desktop/api/Wininet/nf-wininet-unlockurlcacheentryfile) ". Anwendungen, für die der Dateiname nicht erforderlich ist, müssen die Funktionen " [**retrieveurlcacheentrystream**](/windows/desktop/api/Wininet/nf-wininet-retrieveurlcacheentrystreama)", " [**infourlcacheentrystream**](/windows/desktop/api/Wininet/nf-wininet-readurlcacheentrystream)" und " [**unlockurlcacheentrystream**](/windows/desktop/api/Wininet/nf-wininet-unlockurlcacheentrystream) " verwenden, um die Informationen im Cache abzurufen.

" [**Retrieveurlcacheentrystream**](/windows/desktop/api/Wininet/nf-wininet-retrieveurlcacheentrystreama) " führt keine URL-Verarbeitung aus, sodass eine URL, die einen Anker ( \# ) enthält, nicht im Cache gefunden wird, auch wenn die Ressource zwischengespeichert wird. Wenn z. b. die URL " https://example.com/example.htm\#sample " übermittelt wird, gibt die Funktion die Fehler \_ Datei nicht gefunden zurück, \_ \_ auch wenn https://example.com/example.htm sich "" im Cache befindet.

" [**Retrieveurlcacheentryfile**](/windows/desktop/api/Wininet/nf-wininet-retrieveurlcacheentryfilea) " akzeptiert eine URL, einen Puffer, in dem die Informationsstruktur für den [**Internet \_ Cache \_ Eintrag \_**](/windows/desktop/api/Wininet/ns-wininet-internet_cache_entry_infoa) gespeichert ist, und die Puffergröße. Die Funktion wird für den Aufrufer abgerufen und gesperrt.

Nachdem die Informationen in der Datei verwendet wurden, sollte die Anwendung [**unlockurlcacheentryfile**](/windows/desktop/api/Wininet/nf-wininet-unlockurlcacheentryfile) zum Entsperren der Datei abrufen.

### <a name="cache-groups"></a>Cache Gruppen

Um eine Cache Gruppe zu erstellen, muss [**die Funktion "**](/windows/desktop/api/Wininet/nf-wininet-createurlcachegroup) Funktion" von "" die Funktion "" für die Cache Gruppe aufgerufen werden, um eine **GroupID** zu generieren. Einträge können der Cache Gruppe hinzugefügt werden, indem die URL des Cache Eintrags und das \_ Add-Flag der Internet Cache \_ Gruppe der \_ [**seturlcacheentrygroup**](/windows/desktop/api/Wininet/nf-wininet-seturlcacheentrygroup) -Funktion bereitgestellt werden. Wenn Sie einen Cache Eintrag aus einer Gruppe entfernen möchten, übergeben Sie die URL des Cache Eintrags und das Remove-Flag der Internet \_ Cache \_ Gruppe \_ an [**seturlcacheentrygroup**](/windows/desktop/api/Wininet/nf-wininet-seturlcacheentrygroup).

Die Funktionen " [**findfirsturlcacheentryex**](/windows/desktop/api/Wininet/nf-wininet-findfirsturlcacheentryexa) " und " [**findnexturlcacheentryex**](/windows/desktop/api/Wininet/nf-wininet-findnexturlcacheentryexa) " können zum Auflisten der Einträge in einer angegebenen Cache Gruppe verwendet werden. Nachdem die Enumeration abgeschlossen ist, sollte die Funktion [**findcloseurlcache**](/windows/desktop/api/Wininet/nf-wininet-findcloseurlcache)aufrufen.

## <a name="handling-structures-with-variable-size-information"></a>Behandeln von Strukturen mit Variablen Größen Informationen

Der Cache kann Informationen variabler Größe für jede gespeicherte URL enthalten. Dies wird in der Info Struktur des [**Internet \_ Cache \_ Eintrags \_**](/windows/desktop/api/Wininet/ns-wininet-internet_cache_entry_infoa) widergespiegelt. Wenn die Cache Funktionen diese Struktur zurückgeben, erstellen Sie einen Puffer, der immer die Größe der [**Internet \_ Cache- \_ Eintrags \_**](/windows/desktop/api/Wininet/ns-wininet-internet_cache_entry_infoa) Informationen zuzüglich aller Variablen Größen Informationen ist. Wenn ein Zeiger Element nicht **null** ist, zeigt es auf den Speicherbereich direkt hinter der Struktur. Beim Kopieren des von einer Funktion zurückgegebenen Puffers in einen anderen Puffer sollten die Zeiger Elemente so korrigiert werden, dass Sie auf die entsprechende Stelle im neuen Puffer zeigen, wie im folgenden Beispiel gezeigt.

``` syntax
lpDstCEInfo->lpszSourceUrlName = 
    (LPINTERNET_CACHE_ENTRY_INFO) ((LPBYTE) lpSrcCEInfo + 
       ((DWORD)(lpOldCEInfo->lpszSourceUrlName) - (DWORD)lpOldCEInfo));
```

Bei einigen Cache Funktionen \_ \_ tritt ein Fehler auf, wenn Sie einen Puffer angeben, der zu klein ist, um die von der Funktion abgerufenen Cache Eintrags Informationen zu enthalten. In diesem Fall gibt die Funktion auch die erforderliche Größe des Puffers zurück. Anschließend können Sie einen Puffer der entsprechenden Größe zuordnen und die Funktion erneut aufzurufen.

> [!Note]  
> WinInet unterstützt keine Server Implementierungen. Außerdem sollte Sie nicht von einem Dienst verwendet werden. Verwenden Sie für Server Implementierungen oder-Dienste [Microsoft Windows HTTP-Dienste (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).

 

 

 
