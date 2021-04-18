---
description: Zum Abrufen von Benachrichtigungen über ungültige logische Netzwerke verwenden Sie die wsanspioctl-Funktion, um für Netzwerkadressen Änderungs Ereignisse zu registrieren.
ms.assetid: 531b6269-5f35-44c1-ad0f-c5f103029893
title: Abfragen von NLA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ac7a4f57e14bb967b04d3a9fd6fe66717da3878
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347919"
---
# <a name="querying-nla"></a>Abfragen von NLA

Zum Abrufen von Benachrichtigungen über ungültige logische Netzwerke verwenden Sie die [**wsanspioctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsanspioctl) -Funktion, um für Netzwerkadressen Änderungs Ereignisse zu registrieren. Mit zwei Methoden können Sie feststellen, ob ein zuvor gültiger Netzwerk Speicherort ungültig geworden ist: Abruf Methoden oder Benachrichtigungen mit überlappenden e/a-Vorgängen oder Windows-Messaging.

Abfragen werden mithilfe der Funktionen [**wsalookupservicebegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina), [**WSALookupServiceNext**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta) und [**WSALookupServiceEnd**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupserviceend) erstellt, um alle verfügbaren logischen Netzwerke aufzuzählen. Die Verwendung der einzelnen Funktionen wird im Verlauf dieses Abschnitts, beginnend mit der **wsalookupservicebegin** -Funktion, einzeln erläutert.

> [!Note]  
> NLA erfordert die Header Datei "mswap. h", die standardmäßig nicht in der Datei "Winsock2. h" enthalten ist.

 

## <a name="step-1-initiate-the-query"></a>Schritt 1: Initiieren der Abfrage

Zur schnellen Referenz weist die [**wsalookupservicebegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina) -Funktion die folgende Syntax auf:

``` syntax
INT WSALookupServiceBegin(
  LPWSAQUERYSET lpqsRestrictions,
  DWORD dwControlFlags,
  LPHANDLE lphLookup
);
```

NLA unterstützt die folgenden *dwcontrolflags* -lookupflags:

<dl> Name der Lup- \_ Rückgabe \_  
Lup- \_ Rückgabe \_ Kommentar  
Lup- \_ Rückgabe- \_ BLOB  
Lup \_ alle zurückgeben \_  
\_tiefer Lupe  
</dl>

Diese Flags schränken die Resultsets ein, die bei nachfolgenden Aufrufen der [**WSALookupServiceNext**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta)-Funktion zurückgegeben werden, an Netzwerke, die Felder des angegebenen Typs enthalten. Wenn Sie z. b. das Lup- \_ Rückgabe- \_ BLOB im *dwcontrolflags* -Parameter des [**wsalookupservicebegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina) -Funktionsaufrufs angeben, werden die Resultsets von nachfolgenden Aufrufen von **WSALookupServiceNext** auf Netzwerke beschränkt, die BLOB-Informationen enthalten. Die Verwendung des "Lup \_ Return \_ all"-Flags entspricht dem Angeben des \_ luprückgabenamens, des luprückgabetyps \_ \_ und des \_ Lup- \_ Rückgabe- \_ BLOBs, aber \_

Eine Erläuterung dieser Suchflags finden Sie auf der [**wsalookupservicebegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina) -Funktionsreferenz Seite.

Das Such handle, das von der NLA im *lphlookup* -Parameter zurückgegeben wird, ist für NLA Privat und sollte nicht geändert werden. Da das zurückgegebene Handle für NLA privat ist, sind Funktionen wie [**wsagetoverlappedresult**](/windows/desktop/api/Winsock2/nf-winsock2-wsagetoverlappedresult) nicht verfügbar.

NLA gibt nach erfolgreichem Abschluss 0 (null) zurück, wie in der [**wsalookupservicebegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina) -Funktionsreferenz Seite definiert. Andernfalls unterstützt NLA die folgenden Fehlercodes.

| Fehler                    | Bedeutung                                                                                                                                                     |
|--------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| WSANOTINITIALISED        | Ein erfolgreicher Rückruf der [**WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup) -Funktion zum Initialisieren der NLA wurde nicht ausgeführt.                                                   |
| Wsaabval                | Mindestens ein Parameter war ungültig, oder die im Funktions aufruten angegebenen Parameter gelten für andere Protokolle als IP.                                         |
| wsaservice \_ nicht \_ gefunden.   | Der *lpserviceclassid-* Parameter der [**wsaqueryset**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) -Struktur, die im *lpqsrestrictions* -Parameter übergeben wird, enthält eine ungültige GUID. |
| wsano- \_ Daten              | Das Flag für die Lup- \_ Container wurde im *dwcontrolflags* -Parameter angegeben.                                                                                       |
| WSAEFAULT                | Beim Versuch, auf vom Benutzer bereitgestellte Parameter zuzugreifen, ist eine Zugriffsverletzung aufgetreten.                                                                            |
| Wsasysnotready           | Der NLA-Dienst ist nicht verfügbar, um die Anforderung zu verarbeiten.                                                                                                      |
| WSA \_ nicht \_ genügend Arbeits \_ Speicher | NLA oder der NLA-Dienst konnte nicht genügend Arbeitsspeicher zuordnen, um diese Anforderung zu verarbeiten.                                                                        |



 

## <a name="step-2-perform-the-query"></a>Schritt 2: Ausführen der Abfrage

Der nächste Schritt bei der Abfrage von NLA erfordert die Verwendung der [**WSALookupServiceNext**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta) -Funktion. Für die Kurzübersicht weist die **WSALookupServiceNext**-Funktion die folgende Syntax auf:

``` syntax
INT WSALookupServiceNext(
  HANDLE hLookup,
  DWORD dwControlFlags,
  LPDWORD lpdwBufferLength,
  LPWSAQUERYSET lpqsResults
);
```

Der *llookup* -Parameter ist das Nachschlage handle, das vom vorherigen Aufrufen der [**wsalookupservicebegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina) -Funktion zurückgegeben wurde.

Der *dwcontrolflags* -Parameter unterstützt die folgenden Flags:

<dl> Name der Lup- \_ Rückgabe \_  
Lup- \_ Rückgabe \_ Kommentar  
Lup- \_ Rückgabe- \_ BLOB  
Lup \_ alle zurückgeben \_  
Lup- \_ flushprevious  
</dl>

Diese Flags sind unabhängig von den Flags, die im [**wsalookupservicebegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina) -Funktionsaufrufen unterstützt werden. Beachten Sie, dass alle Einschränkungen, die im vorherigen Aufrufen der **wsalookupservicebegin** -Funktion angegeben wurden, die Suche einschränken. das Hinzufügen von Flags mit der [**WSALookupServiceNext**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta) -Funktion in einem Versuch, die Abfrage über die Einschränkungen hinaus zu erweitern, die im Aufruf von **wsalookupservicebegin** angegeben sind, wird automatisch ignoriert. Die Angabe eines restriktiveren Satzes von Flags, die im **wsalookupservicebegin** -Befehl angegeben sind, ist jedoch zulässig.

Wenn es sich bei dem in *lpqsresults* beschriebenen Netzwerk um ein aktives Netzwerk handelt, wird eine Reihe von **NLA- \_ BLOB** -Strukturen angefügt, die im **lpblob** -Member der in *lpqsresults* zurückgegebenen [**wsaqueryset**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) -Struktur angegeben ist. Diese **NLA- \_ BLOB** -Strukturen können verkettet werden und durch Durchlaufen der Liste aufgelistet werden, während NLA \_ BLOB. Header. nexderffset ungleich NULL ist. Um Ergebnisse für alle Netzwerkadressen Informationen zu erhalten, fahren Sie mit dem Aufruf der [**WSALookupServiceNext**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta)-Funktion fort, bis der Fehler "WSA \_ E" \_ \_ zurückgegeben wird, wie auf der Referenzseite zu **WSALookupServiceNext** erläutert.

Die [**WSALookupServiceNext**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta) -Funktion wird auch in Verbindung mit der [**wsanspioctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsanspioctl) -Funktion verwendet, um Benachrichtigungen über Netzwerk Änderungen zu empfangen. Weitere Informationen finden Sie [unter Benachrichtigung von NLA](notification-from-nla-2.md) .

NLA gibt nach erfolgreichem Abschluss NULL zurück. Clients von NLA sollten weiterhin die [**WSALookupServiceNext**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta)-Funktion aufrufen, bis WSA \_ E \_ nicht \_ mehr zurückgegeben wird, was bedeutet, dass alle Informationen zu verfügbaren Netzwerken zurückgegeben wurden.

Andernfalls unterstützt der Aufruf der [**WSALookupServiceNext**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta)-Funktion für NLA die folgenden Fehlercodes.

| Fehler                    | Bedeutung                                                                                                                                                                                                                                                                                                                                                                                                     |
|--------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| WSANOTINITIALISED        | Ein erfolgreicher Rückruf der [**WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup) -Funktion, die NLA initialisierte, wurde nicht ausgeführt.                                                                                                                                                                                                                                                                                                |
| Ungültiges WSA- \_ \_ handle     | Das im *HLOOKUP* -Parameter angegebene Nachschlage Handle war kein gültiges NLA-SP-handle. Clients müssen zunächst die [**wsalookupservicebegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina) -Funktion aufrufen und ein gültiges NLA-SP-handle erhalten, um Abfrageergebnisse zu erhalten.                                                                                                                                                               |
| Wsaesysnotready          | Der NLA-Dienst ist nicht verfügbar, um diese Anforderung zu verarbeiten.                                                                                                                                                                                                                                                                                                                                                     |
| WSAEFAULT                | Die im *lpdwbufferlength* -Parameter angegebene Puffergröße war nicht ausreichend, um die Ergebnisse zu speichern, auf die von *lpqsresults* verwiesen wird. Der erforderliche Puffer wird in " *lpdwbufferlength*;" angegeben. Wenn der Client keinen ausreichend großen Puffer bereitstellen kann, kann der Client die [**WSALookupServiceNext**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta) -Funktion aufrufen, wobei *dwcontrolflags* auf Lup flushprevious festgelegt ist, \_ um den Eintrag zu überspringen. |
| WSA \_ nicht \_ genügend Arbeits \_ Speicher | NLA kann aufgrund von unzureichendem Arbeitsspeicher im aufrufenden Prozess keine Netzwerkinformationen vom NLA-Systemdienst abrufen.                                                                                                                                                                                                                                                                                  |
| WSA \_ E \_ nicht \_ mehr         | Es sind keine zusätzlichen Netzwerke zum Auflisten der Abfrage vorhanden.                                                                                                                                                                                                                                                                                                                                                |



 

## <a name="step-3-terminate-the-query"></a>Schritt 3: Beenden der Abfrage

Wenn alle Abfragen für NLA abgeschlossen sind und eine Anwendung die Verwendung von NLA nicht mehr benötigt, sollte ein Aufrufen der [**WSALookupServiceEnd**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupserviceend) -Funktion erfolgen. Nennen Sie **WSALookupServiceEnd** nicht, wenn die Anwendung die Änderungs Benachrichtigung auf der Grundlage der gesendeten Abfrage empfängt. Weitere Informationen zum Empfangen von Benachrichtigungen finden Sie [unter Benachrichtigung von NLA](notification-from-nla-2.md) . Wie die meisten Windows Sockets-Dienstanbieter verwaltet NLA einen Verweis Zähler für die Clients. Wenn Sie die **WSALookupServiceEnd** -Funktion aufrufen, wenn Abfragen an NLA abgeschlossen werden, werden Systemressourcen, die von der NLA nicht mehr benötigt werden, nicht mehr zur Freigabe

NLA unterstützt die folgenden Fehlercodes für [**WSALookupServiceEnd**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupserviceend) -Funktionsaufrufe.

| Fehler                | Bedeutung                                                                                                   |
|----------------------|-----------------------------------------------------------------------------------------------------------|
| WSANOTINITIALISED    | Ein erfolgreicher Rückruf der [**WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup) -Funktion zum Initialisieren der NLA wurde nicht ausgeführt. |
| Ungültiges WSA- \_ \_ handle | Das im *HLOOKUP* -Parameter angegebene Handle war kein gültiges NLA-SP-handle.                             |



 

 

 



