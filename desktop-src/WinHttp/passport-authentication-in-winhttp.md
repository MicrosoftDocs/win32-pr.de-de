---
description: Die Microsoft Windows HTTP-Dienste (WinHTTP) unterstützen die Client seitige Verwendung des Microsoft Passport Authentifizierungs Protokolls vollständig. Dieses Thema enthält eine Übersicht über die Transaktionen, die an der Passport-Authentifizierung beteiligt sind und wie Sie behandelt werden.
ms.assetid: 395d7aef-4da0-4664-8328-7d31ce58fedd
title: Passport-Authentifizierung in WinHTTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b8fc00217c7c14fbd4635fab68398d2056c1ea5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484182"
---
# <a name="passport-authentication-in-winhttp"></a>Passport-Authentifizierung in WinHTTP

Die Microsoft Windows HTTP-Dienste (WinHTTP) unterstützen die Client seitige Verwendung des Microsoft Passport Authentifizierungs Protokolls vollständig. Dieses Thema enthält eine Übersicht über die Transaktionen, die an der Passport-Authentifizierung beteiligt sind und wie Sie behandelt werden.

> [!Note]  
> In WinHTTP 5,1 ist die Passport-Authentifizierung standardmäßig deaktiviert.

 

## <a name="passport-14"></a>Passport 1,4

Passport ist eine Kernkomponente der Microsoft .net Baustein Dienste. Dadurch können Unternehmen verteilte Webdienste für eine Vielzahl von Anwendungen entwickeln und anbieten, und die Mitglieder können einen Anmelde Namen und ein Kennwort auf allen Beteiligten Websites verwenden.

WinHTTP bietet Platt Form Unterstützung für Microsoft Passport 1,4 durch Implementieren des Client seitigen Protokolls für die Passport 1,4-Authentifizierung. Anwendungen werden aus den Details der Interaktion mit der Passport-Infrastruktur und den gespeicherten Benutzernamen und Kenn Wörtern in Windows XP freigegeben. Diese Abstraktion unterscheidet sich von der Verwendung von Passport von der Perspektive eines Entwicklers, als herkömmliche Authentifizierungs Schemas wie Basic oder Digest zu verwenden.

**Windows XP:** Der Registrierungsschlüssel " **HKCU \\ Software \\ Microsoft \\ Windows \\ CurrentVersion \\ Internet Settings \\ Passport \\ numregistrationruns** " gibt an, wie oft der Passport Authentication Wizard angezeigt wird, wenn eine Passport-Authentifizierung erforderlich ist. Wenn der Wert für diesen Schlüssel auf eine Zahl größer als 5 festgelegt ist, wird der Assistent nicht angezeigt.

In den folgenden Abschnitten werden die für die Passport-Authentifizierung beteiligten Transaktionen aus der Sicht einer Client Anwendung beschrieben. Informationen zur serverseitigen Passport-Entwicklung finden Sie in der Dokumentation zur Passport SDK-Dokumentation.

-   [Erste Anforderung](#initial-request)
-   [Passport-Anmelde Server](#passport-login-server)
-   [Authentifizierte Anforderung](#authenticated-request)

### <a name="initial-request"></a>Erste Anforderung

Wenn ein Client eine Ressource auf einem Server anfordert, der die Passport-Authentifizierung erfordert, überprüft der Server die Anforderung auf das vorhanden sein von [*Tickets*](glossary.md). Wenn ein gültiges *Ticket* mit der Anforderung gesendet wird, antwortet der Server mit der angeforderten Ressource. Wenn das *Ticket* nicht auf dem Client vorhanden ist, antwortet der Server mit dem Statuscode 302. Die Antwort enthält den Challenge-Header "www-Authenticate: Passport 1.4". Clients, die Passport nicht verwenden, können der Umleitung zum Passport-Anmelde Server folgen. Erweiterte Clients kontaktieren in der Regel den Passport-Nexus, um den Speicherort des Passport-Anmelde Servers zu bestimmen.

> [!Note]  
> In der Mitte des Microsoft Passport Netzwerks ist der Passport *Nexus*, der die Synchronisierung von Passport-Teilnehmer Standorten ermöglicht, um sicherzustellen, dass jeder Standort über die neuesten Details zur Netzwerkkonfiguration und zu anderen Problemen verfügt. Jede Passport-Komponente (Passport Manager, Login Servers, Update Servers usw.) kommuniziert regelmäßig mit dem Nexus, um die Informationen abzurufen, die für die Suche und die ordnungsgemäße Kommunikation mit den anderen Komponenten im Passport-Netzwerk benötigt werden. Diese Informationen werden als XML-Dokument, das als Komponenten Konfigurations Dokument bezeichnet wird, oder als "CCD" abgerufen.

 

Die folgende Abbildung zeigt die anfängliche Anforderung an einen Passport-Partner.

![Image zeigt die anfängliche Anforderung an einen Passport-Partner an.](images/art-passport1.png)

### <a name="passport-login-server"></a>Passport-Anmelde Server

Ein Passport-Anmelde Server verarbeitet alle Anforderungen für [*Tickets*](glossary.md) für beliebige Ressourcen in einer Passport- *Domänen Autorität*. Bevor eine Anforderung mithilfe von Passport authentifiziert werden kann, muss die Client Anwendung den Anmelde Server kontaktieren, um die entsprechenden *Tickets* zu erhalten.

Wenn ein Client [*Tickets*](glossary.md) von einem Passport-Anmelde Server anfordert, antwortet der Anmelde Server in der Regel mit dem Statuscode 401, um anzugeben, dass Benutzer Anmelde Informationen angegeben werden müssen. Wenn diese Anmelde Informationen bereitgestellt werden, antwortet der Anmelde Server mit den *Tickets* , die für den Zugriff auf die angegebene Ressource auf dem Server erforderlich sind, der die ursprünglich angeforderte Ressource enthält. Der Anmelde Server kann den Client auch an einen anderen Server umleiten, der die angeforderte Ressource bereitstellen kann.

![das Image zeigt eine Client Ticket Anforderung an einen Passport-Anmelde Server an.](images/art-passport2.png)

### <a name="authenticated-request"></a>Authentifizierte Anforderung

Wenn der Client über die [*Tickets*](glossary.md) verfügt, die einem bestimmten Server entsprechen, sind diese *Tickets* in allen Anforderungen an diesen Server enthalten. Wenn die *Tickets* nicht geändert wurden, weil Sie vom Passport-Anmelde Server abgerufen wurden und die *Tickets* für den Ressourcen Server gültig sind, sendet der Ressourcen Server eine Antwort mit der angeforderten Ressource und den Cookies, die darauf hinweisen, dass der Benutzer für zukünftige Anforderungen authentifiziert ist.

Die zusätzlichen Cookies in der Antwort dienen dazu, den Authentifizierungsprozess zu beschleunigen. Weitere Anforderungen in derselben Sitzung für Ressourcen auf Servern in derselben Passport-Domänen Autorität enthalten alle diese zusätzlichen Cookies. Anmelde Informationen müssen erst wieder an den Anmelde Server gesendet werden, wenn die Cookies ablaufen.

![das Image zeigt eine authentifizierte Anforderung an den Passport-Anmelde Server an.](images/art-passport3.png)

## <a name="using-passport-in-winhttp"></a>Verwenden von Passport in WinHTTP

Die Passport-Authentifizierung in WinHTTP ähnelt anderen Authentifizierungs Schemas. Eine Übersicht über die Authentifizierung in WinHTTP finden Sie unter [Authentifizierung in WinHTTP](authentication-in-winhttp.md) .

In WinHTTP 5,1 ist die Passport-Authentifizierung standardmäßig deaktiviert und muss vor der Verwendung von [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) explizit aktiviert werden.

WinHTTP behandelt viele Transaktionsdetails intern für die Passport-Authentifizierung. Während der ersten Anforderung antwortet der Server mit einem 302-Statuscode, wenn eine Authentifizierung erforderlich ist. Der 302-Statuscode weist tatsächlich auf eine Umleitung hin und ist Teil des Passport-Protokolls aus Gründen der Abwärtskompatibilität. WinHTTP blendet den 302-Statuscode aus und kontaktiert den Passport-Nexus und den Anmelde Server. Die WinHTTP-Anwendung wird über den 401-Statuscode benachrichtigt, der vom Anmelde Server gesendet wird, um Benutzer Anmelde Informationen anzufordern. Die Anwendung wird jedoch so angezeigt, als ob der 401-Status von dem Server stammt, von dem die Ressource angefordert wurde. Auf diese Weise kennt die WinHTTP-Anwendung keine Interaktionen mit anderen Servern und kann die Passport-Authentifizierung mit dem gleichen Code verarbeiten, der andere Authentifizierungs Schemas behandelt.

Normalerweise antwortet eine WinHTTP-Anwendung auf einen 401-Statuscode, indem Anmelde Informationen zur Authentifizierung bereitgestellt werden. Wenn Anmelde Informationen mit [**winhttpsetanmelde**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetcredentials) Informationen oder [**setanmelde**](iwinhttprequest-setcredentials.md) Informationen für die Passport-Authentifizierung bereitgestellt werden, werden die Anmelde Informationen tatsächlich an den Anmelde Server gesendet, nicht an den in der Anforderung angegebenen Server.

Bei der Reaktion auf einen 407-Statuscode muss eine WinHTTP-Anwendung jedoch " [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) " verwenden, um Proxy Anmelde Informationen anstelle von " [**winhttpsetanmelde**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetcredentials)Informationen" bereitzustellen. Da **WinHttpSetOption** eine weniger sichere Möglichkeit zum Angeben von Anmelde Informationen ist, sollte es normalerweise vermieden werden.

Nach dem Abrufen werden [*Tickets*](glossary.md) intern verwaltet und automatisch an die entsprechenden Server in zukünftigen Anforderungen gesendet.

> [!Note]  
> WinHTTP ermöglicht das Deaktivieren der automatischen Umleitung durch Aufrufen der [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) -Funktion für die [**WinHTTP- \_ Option \_ \_ Feature**](option-flags.md) -Flag deaktivieren und Angeben eines Werts von WinHTTP-Deaktivierungs Umleitungen [**\_ \_**](option-flags.md). Die Deaktivierung der Umleitung beeinträchtigt nicht die Umleitung, die WinHTTP intern für Passport-Transaktionen verarbeitet.

 

WinHTTP kann die Passport-Authentifizierung auch dann erfolgreich vervollständigen, wenn eine Anwendung die automatische Umleitung deaktiviert. Nach Abschluss der Passport-Authentifizierung muss jedoch eine implizite Umleitung von der Passport-Anmelde Server-URL zurück zur ursprünglichen URL erfolgen. Diese Umleitung wird nicht durch eine 302-HTTP-Antwort ausgelöst, ist jedoch im Passport-Protokoll implizit.

WinHTTP behandelt diese implizite Umleitung speziell. Wenn eine Anwendung die automatische Umleitung deaktiviert hat, erfordert WinHTTP, dass die Anwendung die WinHTTP-Berechtigung "Berechtigung" für die automatische Umleitung in diesem Sonderfall erteilt.

Damit WinHTTP nach der Authentifizierung wieder an die ursprüngliche URL umgeleitet wird, muss die Anwendung eine Rückruffunktion mit [**winhttpsetstatus-Rückruf**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetstatuscallback)registrieren. WinHTTP kann die Anwendung dann mit einem WinHTTP- \_ Rückruf \_ Status- \_ Umleitungs Rückruf Benachrichtigen, der es der Anwendung ermöglicht, die Umleitung abzubrechen. Eine Anwendung muss keine Funktionalität in der Rückruffunktion bereitstellen. die Registrierung des Rückrufs ist ausreichend, damit WinHTTP diese spezielle Umleitung befolgt.

\_ \_ \_ Wenn eine Rückruffunktion nicht von der Anwendung festgelegt wird, wird die Fehlermeldung WinHTTP Login Failure (Fehlermeldung) generiert.

### <a name="passport-cobranding"></a>Passport-Cobranding

Im Gegensatz zu herkömmlichen Authentifizierungs Schemas, die von WinHTTP unterstützt werden, kann Passport ausführlich [*coziert*](glossary.md)werden. Nach dem Empfang eines 401-Statuscodes, der eine Herausforderung anzeigt, kann eine Anwendung die *cobrandinggrafik* und den Text abrufen. Rufen Sie eine URL für die *Cobranding* -Grafik ab, indem Sie [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) mit der WinHTTP- \_ Option \_ Passport \_ Cobranding \_ URL-Flag aufrufen. Rufen Sie den *cobrandingtext* ab, indem Sie [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) mit der WinHTTP- \_ Option \_ Passport \_ Cobranding- \_ textflag aufrufen. Diese Elemente können verwendet werden, um ein Dialogfeld zum Erfassen von Anmelde Informationen anzupassen.

### <a name="stored-user-names-and-passwords"></a>Gespeicherte Benutzernamen und Kennwörter

In Windows XP wurde das Konzept von gespeicherten Benutzernamen und Kenn Wörtern eingeführt. Wenn die Passport-Anmelde Informationen eines Benutzers über den **Passport-Registrierungs-Assistenten** oder das Standard **Dialogfeld** Anmelde Informationen gespeichert werden, werden diese in den gespeicherten Benutzernamen und Kenn Wörtern gespeichert. Bei Verwendung von WinHTTP unter Windows XP oder höher verwendet WinHTTP automatisch die Anmelde Informationen in den gespeicherten Benutzernamen und Kenn Wörtern, wenn die Anmelde Informationen nicht explizit festgelegt sind. Dies ähnelt der Unterstützung von Standard Anmelde Informationen für NTLM/Kerberos. Die Verwendung von standardmäßigen Passport-Anmelde Informationen unterliegt jedoch nicht den Einstellungen für die automatische Anmelde Richtlinie.

### <a name="disabling-passport-authentication"></a>Deaktivieren der Passport-Authentifizierung

Einige Anwendungen erfordern möglicherweise die Möglichkeit, die Passport-Authentifizierung zu deaktivieren. Wenn ein Passport-Partner z. b. mit dem ersten 302-Statuscode antwortet, empfiehlt es sich, die folgende Umleitung zu befolgen und die HTML-Passport-Authentifizierungsseite zu erzeugen, anstatt WinHTTP das interne behandeln der Authentifizierung zu gestatten. Die Passport-Authentifizierung ist in WinHTTP deaktiviert, indem die [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) -Funktion mit der WinHTTP \_ -Option " \_ \_ Passport auth" Konfigurieren aufgerufen \_ und der Wert "WinHTTP \_ deaktiviert \_ Passport auth" übergeben wird \_ . Sie kann später mit WinHTTP \_ enable \_ Passport auth wieder aktiviert werden \_ .

Die Passport-Authentifizierung kann nicht deaktiviert werden, wenn das [**WinHttpRequest**](winhttprequest.md) -Objekt verwendet wird.

Wie bereits weiter oben in diesem Abschnitt erwähnt, ist die Passport-Authentifizierung in WinHTTP 5,1 standardmäßig deaktiviert und muss vor der Verwendung von [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) explizit aktiviert werden.

## <a name="passport-configuration-overrides-used-for-testing"></a>Zum Testen verwendete außer Kraft setzungen für die Passport-Konfiguration

WinHTTP basiert auf den Konfigurationsinformationen, die er vom Passport Nexus-Server herunterlädt, um die Passport 1,4-Authentifizierung zu unterstützen. Standardmäßig ist dieser Secure (SSL)-Server Nexus.Passport.com, und die Konfigurations Ressource ist rdr/pprdr. ASP, die als "Live"-Passport-Konfiguration bezeichnet wird. Das Format der Informationen ist ein benutzerdefinierter HTTP-Header "passporturls", gefolgt von durch Trennzeichen getrennten Attribut-Wert-Paaren.

" https://nexus.passport.com/rdr/pprdr.asp " Gibt beispielsweise die folgenden Konfigurationsinformationen zurück:

``` syntax
PassportURLs: DARealm=Passport.net,
DALogin=login.passport.com/login2.asp,
DAReg=https://register.passport.com/defaultwiz.asp,
Properties=https://memberservices.passport.com/ppsecure/MSRV_EditProfile.asp,
Privacy=https://www.passport.com/consumer/privacypolicy.asp,
GeneralRedir=https://nexusrdr.passport.com/redir.asp,
Help=https://memberservices.passport.com/UI/MSRV_UI_Help.asp,
ConfigVersion=2
\r\n
```

Die für WinHTTP relevanten Teile sind darealm, dalogin und ConfigVersion. Aus Leistungsgründen werden Sie während der Lebensdauer einer WinHTTP-Sitzung zwischengespeichert. Diese drei Werte können von Anwendungen außer Kraft gesetzt werden, die für die Arbeit mit einer anderen Passport-Infrastruktur als der "Live"-Produktions Einrichtung erforderlich sind, indem Sie die entsprechenden Registrierungs Einstellungen unter ändern.

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         Windows
            CurrentVersion
               Internet Settings
                  WinHttp
                     Passport Test
```

``` syntax
LoginServerRealm (REG_SZ)    For example: abc.net
LoginServerUrl (REG_SZ)      For example: https://private-login.passport.com/login2.asp
ConfigVersion (REG_DWORD)    For example: 10
```

Wenn LoginServerUrl in der Registrierung vorhanden ist, kontaktiert WinHTTP keine Verbindung mit dem Nexus-Server für andere Konfigurationswerte. In diesem Fall sollten loginserverrealm und ConfigVersion auch über die Registrierung festgelegt werden, um die Werte zu korrigieren.

Eine Anwendung kann zu Testzwecken zum Herunterladen der Passport-Konfiguration von einem privaten Nexus-Server benötigt werden. Dies können Sie erreichen, indem Sie zwei Registrierungs Werte überschreiben.

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         Windows
            CurrentVersion
               Internet Settings
                  WinHttp
                     Passport Test
```

``` syntax
NexusHost (REG_SZ)    e.g. private-nexus.passport.com
NexusObj(REG_SZ)      e.g. config/passport.asp
```

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Authentifizierung in WinHTTP](authentication-in-winhttp.md)
</dt> </dl>

 

 



