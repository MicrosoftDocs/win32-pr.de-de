---
description: In diesem Thema werden die wichtigsten Unterschiede zwischen der WinHTTP-Version 5,1 und der Version 5,0 beschrieben.
ms.assetid: df3fcf27-3012-4818-b29c-b8a4dc409828
title: Neuerungen in WinHTTP 5,1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 909d5ae8fb1d169af01782d21d2ead56b25c940c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345727"
---
# <a name="whats-new-in-winhttp-51"></a>Neues in WinHTTP 5,1

In diesem Thema werden die wichtigsten Unterschiede zwischen der WinHTTP-Version 5,1 und der Version 5,0 beschrieben. Viele dieser Unterschiede erfordern Codeänderungen in Anwendungen, die von Version 5,0 zu Version 5,1 migrieren. Einige der Features in Version 5,1 sind nur ab Windows Server 2003 und Windows XP mit Service Pack 2 (SP2) verfügbar. Dies gilt insbesondere für Features, die sich auf die Verbesserung der Sicherheit des Clients vor bösartigen Webservern beziehen.

> [!IMPORTANT]
> Mit der Veröffentlichung von WinHTTP-Version 5,1 ist der WinHTTP 5,0-Download nicht mehr verfügbar. Ab dem 1. Oktober 2004 hat Microsoft das WinHTTP 5,0 SDK-Download von MSDN entfernt und hat den Produktsupport für Version 5,0 beendet.

 

## <a name="dll-name-change"></a>DLL-Namensänderung

Der Name der neuen WinHTTP 5,1-dll ist Winhttp.dll, während der Name der WinHTTP 5,0-dll Winhttp5.dll ist.

WinHTTP 5,0 und 5,1 können auf demselben System nebeneinander vorhanden sein. WinHTTP 5,1 ersetzt oder installiert nicht WinHTTP 5,0.

## <a name="redistribution"></a>Weiterverteilung

WinHTTP 5,1 ist nur für Windows Server 2003, Windows 2000 Professional mit Service Pack 3 (SP3), Windows XP mit Service Pack 1 (SP1) und spätere Betriebssysteme verfügbar. Eine verteilbare Mergemoduldatei (. MSM) ist für WinHTTP 5,1 nicht verfügbar.

## <a name="winhttprequest-progid"></a>WinHttpRequest-ProgID

Die ProgID der WinHttpRequest-Komponente wurde von "WinHTTP. WinHttpRequest. 5" in "WinHTTP. WinHttpRequest. 5.1" geändert. Die CLSID der [**WinHttpRequest**](winhttprequest.md) -Klasse hat sich ebenfalls geändert.

## <a name="async-callback-behavior-change"></a>Änderung des Async-Rückruf Verhaltens

Wenn Sie die Funktionen " [**winhttpschreitedata**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpwritedata)", " [**winhttpquerydataavailable**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpquerydataavailable) " und " [**WinHttpReadData**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreaddata) " im asynchronen Modus aufrufen, verlassen Sie sich nicht darauf, dass die entsprechenden *lpdwnumofbyteswritten*-, *lpdwnumofbytesavailable*-und *lpdwnumofbytesread* out-Parameter festgelegt Wenn der Funktions Aufrufvorgang asynchron abgeschlossen wird, schreibt WinHTTP nicht in diese Zeiger, die vom Anwendungscode bereitgestellt werden. Stattdessen sollte die Anwendung diese Werte mit den Parametern *lpvstatusinformation* und *dwstatusinformationlength* für die Rückruffunktion abrufen.

## <a name="changes-to-default-settings"></a>Änderungen an den Standardeinstellungen

Änderungen an den Standardeinstellungen umfassen:

-   Die Überprüfung des SSL-Serverzertifikats ist in WinHTTP 5,1 standardmäßig aktiviert. WinHTTP 5,0 behandelt keine Fehler, die beim Validieren des Serverzertifikats als schwerwiegender Fehler aufgetreten sind. Sie werden der Anwendung mithilfe einer **sicheren \_ Fehler** Rückruf Benachrichtigung gemeldet, führen jedoch nicht dazu, dass die Anforderung abgebrochen wird. WinHTTP 5,1 behandelt auch Fehler bei der Überprüfung des Serverzertifikats als schwerwiegende Fehler, die die Anforderung abbrechen. Die Anwendung kann WinHTTP anweisen, eine kleine Teilmenge von Zertifikat Fehlern wie z. b. unbekannte ZS, ungültiges/abgelaufenes Zertifikat Datum oder einen ungültigen Zertifikat Antragsteller Namen mithilfe der Option " **WinHTTP- \_ Option \_ \_ sicherheitsflags** " zu ignorieren.
-   Die Unterstützung für die Passport-Authentifizierung ist in WinHTTP 5,1 standardmäßig deaktiviert. Die Passport-Unterstützung kann mit der **WinHTTP- \_ Option " \_ \_ Passport \_ auth konfigurieren** " aktiviert werden. Das automatische Suchen von Passport-Anmelde Informationen im Schlüsselbund ist ebenfalls standardmäßig deaktiviert.
-   Umleitungs Behavior Change: HTTP-Umleitungen von einer sicheren **https:** URL zu einer regulären **http:** -URL werden aus Sicherheitsgründen nicht mehr automatisch befolgt. Es gibt eine neue Option, **WinHTTP- \_ Option \_ Umleitungs \_ Richtlinie**, um das Standardumleitungs Verhalten in WinHTTP 5,1 zu überschreiben. Verwenden Sie bei der **WinHttpRequest** COM-Komponente die neue Option **winhttprequestoption \_ enablehttpstohttpreumgeleitet** , um Umleitungen von https: an http: URLs zu aktivieren.
-   Wenn eine WinHTTP-Ablauf Verfolgungs Datei erstellt wird, wird der Zugriff durch eine ACL eingeschränkt, sodass nur Administratoren die Datei lesen oder schreiben können. Das Benutzerkonto, unter dem die Tracefile erstellt wurde, kann auch die ACL ändern, um anderen Benutzern Zugriff zu gewähren. Dieser Schutz ist nur für Dateisysteme verfügbar, die die Sicherheit unterstützen. d. h. NTFS, nicht FAT32).
-   Ab Windows Server 2003 und Windows XP SP2 ist das Senden von Anforderungen an die folgenden bekannten, nicht-HTTP-Ports aus Sicherheitsgründen eingeschränkt: 21 (FTP), 25 (SMTP), 70 (Gopher), 110 (POP3), 119 (NNTP), 143 (IMAP).
-   Ab Windows Server 2003 und Windows XP mit SP2 beträgt die maximale Menge an Header Daten, die WinHTTP in einer HTTP-Antwort akzeptiert, standardmäßig 64 KB. Wenn die HTTP-Antwort des Servers mehr als 64 KB gesamter Header Daten enthält, schlägt WinHTTP die Anforderung mit einem Fehler fehl, wenn der **Fehler " \_ WinHTTP \_ ungültige \_ Server \_ Antwort** " lautet. Das Limit von 64K kann mithilfe der neuen **WinHTTP- \_ Option \_ Max \_ Response \_ Header \_ size** -Option überschrieben werden.

## <a name="ipv6-support"></a>IPv6-Unterstützung

WinHTTP 5,1 bietet Unterstützung für IPv6 (Internet Protocol Version 6). WinHTTP kann HTTP-Anforderungen an einen Server senden, dessen DNS-Name in eine IPv6-Adresse aufgelöst wird. ab Windows Server 2003 und Windows XP mit SP2 unterstützt WinHTTP auch IPv6-Literaladressen.

## <a name="new-options-in-the-cc-api-for-winhttp"></a>Neue Optionen in der C/C++-API für WinHTTP

WinHTTP 5,1 implementiert die folgenden neuen Optionen:

<dl> " \# Definieren der WinHTTP- \_ Option \_ Passport \_ Sign \_ out 86"  
" \# define WinHTTP \_ Option \_ Passport \_ Return \_ URL 87"  
" \# Definieren der WinHTTP- \_ Option \_ Umleitungs \_ Richtlinie 88"  
</dl>

Ab Windows Server 2003 und Windows XP mit SP2 implementiert WinHTTP 5,1 die folgenden neuen Optionen. Bei Windows 2000 Professional mit SP3 oder Windows XP mit SP1 schlagen Aufrufe von [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) oder [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) mit diesen Options-IDs jedoch fehl:

<dl> " \# Timeout für die \_ \_ \_ Antwort auf die WinHTTP-Option definieren \_ "  
" \# Definieren der WinHTTP- \_ Option \_ Max \_ http \_ Automatic \_ Umleitungen 89"  
" \# define WinHTTP- \_ Option \_ Max \_ http \_ Status \_ Continue 90"  
" \# Definieren der \_ Max- \_ \_ Antwort Header Größe von WinHTTP-Optionen \_ \_ 91"  
" \# define WinHTTP \_ Option \_ Max \_ Response-Ausgleichs \_ \_ Größe 92"  
</dl>

## <a name="new-options-in-the-winhttprequest-51-component"></a>Neue Optionen in der WinHttpRequest 5,1-Komponente

Die Komponente WinHttpRequest 5,1 implementiert die folgenden neuen Optionen:

<dl> "Winhttprequestoption \_ revertimpersonationoverssl"  
"Winhttprequestoption \_ enablehttpstohttpredirektionen"  
"Winhttprequestoption \_ enablepassportauthentication"  
</dl>

Die folgenden neuen Optionen für WinHttpRequest 5,1 sind ab Windows Server 2003 und Windows XP mit SP2 verfügbar:

<dl> "Winhttprequestoption \_ maxautomatikreumgeleitet"  
"Winhttprequestoption \_ maxresponsheadersize"  
"Winhttprequestoption \_ maxresponabdrainsize"  
"Winhttprequestoptions \_ EnableHttp1 \_ 1"  
</dl>

## <a name="proxies-are-not-trusted-when-auto-logon-security-is-set-to-high"></a>Proxys sind nicht vertrauenswürdig, wenn die automatische Anmelde Sicherheit auf High festgelegt ist.

In WinHTTP 5,0 sind Proxy Server für die automatische Anmeldung immer vertrauenswürdig. Dies ist für WinHTTP 5,1, das unter Windows Server 2003 und Windows XP mit SP2 ausgeführt wird, nicht mehr gültig, wenn die Option **WinHTTP \_ Autologon \_ Security \_ Level \_ High** Policy festgelegt ist.

## <a name="web-proxy-auto-discovery-autoproxy-api"></a>API für die automatische Ermittlung von Webproxys (AutoProxy)

Zum Vereinfachen der Konfiguration von Proxy Einstellungen für WinHTTP-basierte Anwendungen implementiert WinHTTP jetzt das WPAD-Protokoll (Web Proxy Auto-Discovery), das auch als " *aktivierter automatischer Proxy*" bezeichnet wird. Dabei handelt es sich um dasselbe Protokoll, das Webbrowser, wie z. b. Internet Explorer, implementieren, um die Proxykonfiguration automatisch zu ermitteln, ohne dass ein Endbenutzer einen Proxy Server manuell angeben muss. Zur Unterstützung von AutoProxy implementiert WinHTTP 5,1 eine neue C/C++-Funktion, [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl), plus zwei unterstützende Funktionen, [**winhttpdetectautoproxyconfigurl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpdetectautoproxyconfigurl) und [**WinHttpGetIEProxyConfigForCurrentUser**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetieproxyconfigforcurrentuser).

## <a name="known-issues"></a>Bekannte Probleme

Die folgenden Probleme sind bekanntermaßen in WinHTTP 5,1 unter Windows 2000 Professional mit SP3 und Windows XP mit SP1 vorhanden. Diese Probleme werden für WinHTTP gelöst, beginnend mit Windows Server 2003 und Windows XP mit SP2:

-   Wenn die Anwendung die [**winhttpsettimeouts**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsettimeouts) -Funktion oder die [**settimeouts**](iwinhttprequest-settimeouts.md) -Methode in der [**WinHttpRequest**](iwinhttprequest-interface.md) -Komponente verwendet, um ein nicht unendliches DNS-Auflösungs Timeout festzulegen, z. b. den *dwresolvetimeout* -Parameter, tritt ein Thread handle-Fehler auf, wenn WinHTTP einen DNS-Namen auflöst. Bei einer großen Anzahl von HTTP-Anforderungen verursacht dies einen erheblichen Speicherplatz. Die Problem Umgehung besteht darin, die Standardeinstellung für das unbegrenzte Auflösungs Timeout unverändert zu lassen (der Wert 0 gibt ein unendliches Timeout an). Dies wird in jedem Fall dringend empfohlen, da die Unterstützung von Timeouts für DNS-Namens Auflösungen in WinHTTP in Bezug auf die Leistung teuer ist. Bei Windows 2000 und höher ist das Festlegen eines DNS-Auflösungs Timeouts in WinHTTP unnötig, da der zugrunde liegende DNS-Client Dienst ein eigenes Auflösungs Timeout implementiert.
-   Bei der Verarbeitung von asynchronen Anforderungen verarbeitet WinHTTP den Thread Identitätswechsel nicht ordnungsgemäß. Dies bewirkt, dass Anforderungen, die NTLM/Aushandlungs Authentifizierung erfordern, fehlschlagen, es sei denn, Anmelde Informationen werden explizit mithilfe der Funktionen [**winhttpsetanmelde**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetcredentials) Informationen oder [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) angegeben.

 

 



