---
description: Microsoft Windows HTTP Services (WinHTTP) unterstützen die clientseitige Verwendung des Microsoft Passport-Authentifizierungsprotokolls vollständig. Dieses Thema bietet eine Übersicht über die Transaktionen, die an der Passport-Authentifizierung beteiligt sind, und wie sie behandelt werden.
ms.assetid: 395d7aef-4da0-4664-8328-7d31ce58fedd
title: Passport-Authentifizierung in WinHTTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f69d6aff7f8924c307d4e21efb77bc57ebae2469e50361b57d12dce5b348555e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118114305"
---
# <a name="passport-authentication-in-winhttp"></a>Passport-Authentifizierung in WinHTTP

Microsoft Windows HTTP Services (WinHTTP) unterstützen die clientseitige Verwendung des Microsoft Passport-Authentifizierungsprotokolls vollständig. Dieses Thema bietet eine Übersicht über die Transaktionen, die an der Passport-Authentifizierung beteiligt sind, und wie sie behandelt werden.

> [!Note]  
> In WinHTTP 5.1 ist die Passport-Authentifizierung standardmäßig deaktiviert.

 

## <a name="passport-14"></a>Passport 1.4

Passport ist eine Kernkomponente der Microsoft .NET Bausteindienste. Sie ermöglicht Es Unternehmen, verteilte Webdienste für eine Vielzahl von Anwendungen zu entwickeln und anzubieten, und ihre Mitglieder können einen Anmeldenamen und ein Kennwort auf allen beteiligten Websites verwenden.

WinHTTP bietet Plattformunterstützung für Microsoft Passport 1.4, indem das clientseitige Protokoll für die Passport 1.4-Authentifizierung implementiert wird. Anwendungen werden aus den Details der Interaktion mit der Passport-Infrastruktur und den gespeicherten Benutzernamen und Kennwörtern in Windows XP freigegeben. Diese Abstraktion unterscheidet die Verwendung von Passport nicht von der Perspektive eines Entwicklers als die Verwendung herkömmlicher Authentifizierungsschemas wie Basic oder Digest.

**Windows XP:** Der **Registrierungsschlüssel HKCU \\ Software Microsoft Windows \\ \\ \\ CurrentVersion Internet Einstellungen Passport \\ \\ \\ NumRegistrationRuns** gibt an, wie oft der Passport-Authentifizierungs-Assistent angezeigt wird, wenn die PassPort-Authentifizierung erforderlich ist. Wenn der Wert für diesen Schlüssel auf eine Zahl größer als 5 festgelegt ist, wird der Assistent nicht angezeigt.

In den folgenden Abschnitten werden die Transaktionen beschrieben, die aus Sicht einer Clientanwendung an der Passport-Authentifizierung beteiligt sind. Informationen zur serverseitigen Passport-Entwicklung finden Sie in der Übersicht über die Passport SDK-Dokumentation.

-   [Erste Anforderung](#initial-request)
-   [Passport-Anmeldeserver](#passport-login-server)
-   [Authentifizierte Anforderung](#authenticated-request)

### <a name="initial-request"></a>Erste Anforderung

Wenn ein Client eine Ressource auf einem Server anfordert, für den die Passport-Authentifizierung erforderlich ist, überprüft der Server die Anforderung auf das Vorhandensein von [*Tickets.*](glossary.md) Wenn mit der Anforderung ein gültiges *Ticket* gesendet wird, antwortet der Server mit der angeforderten Ressource. Wenn das *Ticket* auf dem Client nicht vorhanden ist, antwortet der Server mit dem Statuscode 302. Die Antwort enthält den Abfrageheader "WWW-Authenticate: Passport1.4". Clients, die Passport nicht verwenden, können der Umleitung zum Passport-Anmeldeserver folgen. Erweiterte Clients wenden sich in der Regel an den Passport-Nexus, um den Standort des Passport-Anmeldeservers zu ermitteln.

> [!Note]  
> Ein zentraler Bestandteil des Microsoft Passport Netzwerks ist Passport *Nexus,* das die Synchronisierung von Passport-Teilnehmerstandorten ermöglicht, um sicherzustellen, dass jeder Standort über die neuesten Details zur Netzwerkkonfiguration und andere Probleme verfügt. Jede Passport-Komponente (Passport-Manager, Anmeldeserver, Updateserver usw.) kommuniziert in regelmäßigen Abständen mit nexus, um die Informationen abzurufen, die sie benötigt, um die anderen Komponenten im Passport-Netzwerk zu finden und ordnungsgemäß mit ihnen zu kommunizieren. Diese Informationen werden als XML-Dokument abgerufen, das als Komponentenkonfigurationsdokument oder CCD bezeichnet wird.

 

Die folgende Abbildung zeigt die erste Anforderung an einen Passport-Partner.

![Abbildung der ersten Anforderung an einen Passport-Partner.](images/art-passport1.png)

### <a name="passport-login-server"></a>Passport-Anmeldeserver

Ein Passport-Anmeldeserver verarbeitet alle Anforderungen für [*Tickets*](glossary.md) für jede Ressource in einer *Passport-Domänenautorität.* Bevor eine Anforderung mit Passport authentifiziert werden kann, muss sich die Clientanwendung an den Anmeldeserver wenden, um die entsprechenden *Tickets* zu erhalten.

Wenn ein Client [*Tickets*](glossary.md) von einem Passport-Anmeldeserver anfordert, antwortet der Anmeldeserver in der Regel mit dem Statuscode 401, um anzugeben, dass Benutzeranmeldeinformationen angegeben werden müssen. Wenn diese Anmeldeinformationen bereitgestellt werden, antwortet der Anmeldeserver mit den *Tickets,* die für den Zugriff auf die angegebene Ressource auf dem Server erforderlich sind, der die ursprünglich angeforderte Ressource enthält. Der Anmeldeserver kann den Client auch an einen anderen Server umleiten, der die angeforderte Ressource bereitstellen kann.

![Die Abbildung zeigt eine Clientticketanforderung an einen Passport-Anmeldeserver.](images/art-passport2.png)

### <a name="authenticated-request"></a>Authentifizierte Anforderung

Wenn der Client über die [*Tickets*](glossary.md) verfügt, die einem bestimmten Server entsprechen, sind diese *Tickets* in allen Anforderungen an diesen Server enthalten. Wenn die *Tickets* seit dem Abrufen vom Passport-Anmeldeserver nicht geändert wurden und die *Tickets* für den Ressourcenserver gültig sind, sendet der Ressourcenserver eine Antwort, die sowohl die angeforderte Ressource als auch Cookies enthält, die angeben, dass der Benutzer für zukünftige Anforderungen authentifiziert ist.

Die zusätzlichen Cookies in der Antwort sollen den Authentifizierungsprozess beschleunigen. Zusätzliche Anforderungen in derselben Sitzung für Ressourcen auf Servern in derselben Passport-Domänenautorität enthalten alle diese zusätzlichen Cookies. Anmeldeinformationen müssen erst wieder an den Anmeldeserver gesendet werden, wenn die Cookies ablaufen.

![Die Abbildung zeigt eine authentifizierte Anforderung an den Passport-Anmeldeserver.](images/art-passport3.png)

## <a name="using-passport-in-winhttp"></a>Verwenden von Passport in WinHTTP

Die Passport-Authentifizierung in WinHTTP ähnelt sehr anderen Authentifizierungsschemas. Eine Übersicht über die Authentifizierung [in WinHTTP](authentication-in-winhttp.md) finden Sie unter Authentifizierung in WinHTTP.

In WinHTTP 5.1 ist die Passport-Authentifizierung standardmäßig deaktiviert und muss vor der Verwendung explizit mit [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) aktiviert werden.

WinHTTP verarbeitet viele Transaktionsdetails intern für die Passport-Authentifizierung. Während der ersten Anforderung antwortet der Server mit dem Statuscode 302, wenn eine Authentifizierung erforderlich ist. Der Statuscode 302 gibt tatsächlich eine Umleitung an und ist Aus Gründen der Abwärtskompatibilität Teil des Passport-Protokolls. WinHTTP blendet den Statuscode 302 aus und kontaktiert das Passport-Nexus und dann den Anmeldeserver. Die WinHTTP-Anwendung wird über den Statuscode 401 benachrichtigt, der vom Anmeldeserver gesendet wird, um Benutzeranmeldeinformationen anzufordern. Für die Anwendung sieht es jedoch so aus, als ob der Status 401 von dem Server stammt, von dem die Ressource angefordert wurde. Auf diese Weise kennt die WinHTTP-Anwendung keine Interaktionen mit anderen Servern und kann die Passport-Authentifizierung mit demselben Code verarbeiten, der auch andere Authentifizierungsschemas verarbeitet.

In der Regel antwortet eine WinHTTP-Anwendung auf einen 401-Statuscode, indem Authentifizierungsanmeldeinformationen angegeben werden. Wenn Anmeldeinformationen mit [**WinHttpSetCredentials**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetcredentials) oder [**SetCredentials**](iwinhttprequest-setcredentials.md) für die Passport-Authentifizierung bereitgestellt werden, werden die Anmeldeinformationen tatsächlich an den Anmeldeserver und nicht an den in der Anforderung angegebenen Server gesendet.

Wenn sie jedoch auf einen 407-Statuscode antwortet, muss eine WinHTTP-Anwendung [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) verwenden, um Proxyanmeldeinformationen anstelle von [**WinHttpSetCredentials**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetcredentials)bereitzustellen. Da **WinHttpSetOption** eine weniger sichere Möglichkeit zum Bereitstellen von Anmeldeinformationen ist, sollte dies normalerweise vermieden werden.

Nach dem Abrufen werden [*Tickets*](glossary.md) intern verwaltet und bei zukünftigen Anforderungen automatisch an die entsprechenden Server gesendet.

> [!Note]  
> Mit WinHTTP können Sie die automatische Umleitung deaktivieren, indem Sie die [**WinHttpSetOption-Funktion**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) für das [**WINHTTP \_ OPTION DISABLE \_ \_ FEATURE-Flag**](option-flags.md) aufrufen und den Wert [**WINHTTP DISABLE \_ \_ REDIRECTS**](option-flags.md)angeben. Das Deaktivieren der Umleitung beeinträchtigt nicht die Umleitung, die WinHTTP intern für Passport-Transaktionen verarbeitet.

 

WinHTTP kann die Passport-Authentifizierung auch dann erfolgreich abschließen, wenn eine Anwendung die automatische Umleitung deaktiviert. Nach Abschluss der Passport-Authentifizierung muss jedoch eine implizite Umleitung von der Passport-Anmeldeserver-URL zurück zur ursprünglichen URL erfolgen. Diese Umleitung wird nicht durch eine 302-HTTP-Antwort ausgelöst, sondern ist im Passport-Protokoll implizit.

WinHTTP verarbeitet diese implizite Umleitung speziell. Wenn eine Anwendung die automatische Umleitung deaktiviert hat, erfordert WinHTTP, dass die Anwendung WinHTTP in diesem Sonderfall die Berechtigung zum automatischen Umleiten erteilt.

Damit WinHTTP nach der Authentifizierung zur ursprünglichen URL zurückgeleitet wird, muss die Anwendung eine Rückruffunktion mit [**WinHttpSetStatusCallback**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetstatuscallback)registrieren. WinHTTP kann die Anwendung dann mit einem WINHTTP \_ CALLBACK \_ STATUS \_ REDIRECT-Rückruf benachrichtigen, der es der Anwendung ermöglicht, die Umleitung abzubrechen. Eine Anwendung muss keine Funktionen in der Rückruffunktion bereitstellen. Die Registrierung des Rückrufs ist ausreichend, damit WinHTTP dieser Umleitung in Sonderfällen folgen kann.

Die FEHLERMELDUNG ERROR \_ WINHTTP \_ LOGIN FAILURE wird \_ generiert, wenn eine Rückruffunktion nicht von der Anwendung festgelegt wird.

### <a name="passport-cobranding"></a>Passport-Cobranding

Im Gegensatz zu herkömmlichen Authentifizierungsschemas, die von WinHTTP unterstützt werden, kann Passport umfassend [*mit Cobranding markiert*](glossary.md)werden. Wenn ein 401-Statuscode empfangen wird, der auf eine Herausforderung hinweist, kann eine Anwendung die *Cobrandinggrafik* und den Text abrufen. Rufen Sie eine URL für die *Cobrandinggrafik* ab, indem [**Sie WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) mit dem WINHTTP \_ OPTION PASSPORT \_ \_ COBRANDING \_ URL-Flag aufrufen. Rufen Sie den *Cobrandingtext ab,* indem [**Sie WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) mit dem WINHTTP \_ OPTION PASSPORT \_ \_ COBRANDING \_ TEXT-Flag aufrufen. Diese Elemente können verwendet werden, um ein Dialogfeld zum Sammeln von Anmeldeinformationen anzupassen.

### <a name="stored-user-names-and-passwords"></a>Gespeicherte Benutzernamen und Kennwörter

Windows XP hat das Konzept von gespeicherten Benutzernamen und Kennwörtern eingeführt. Wenn die Passport-Anmeldeinformationen eines Benutzers über den **Passport-Registrierungs-Assistenten** oder das **Standarddialogfeld für Anmeldeinformationen** gespeichert werden, werden sie in den gespeicherten Benutzernamen und Kennwörtern gespeichert. Wenn WinHTTP auf Windows XP oder höher verwendet wird, verwendet WinHTTP automatisch die Anmeldeinformationen in den gespeicherten Benutzernamen und Kennwörtern, wenn die Anmeldeinformationen nicht explizit festgelegt sind. Dies ähnelt der Unterstützung von Standardanmeldeinformationen für NTLM/Kerberos. Die Verwendung von Passport-Standardanmeldeinformationen unterliegt jedoch nicht den Einstellungen für die automatische Anmeldungsrichtlinie.

### <a name="disabling-passport-authentication"></a>Deaktivieren der Passport-Authentifizierung

Einige Anwendungen erfordern möglicherweise die Möglichkeit, die Passport-Authentifizierung zu deaktivieren. Wenn beispielsweise ein Passport-Partner mit dem anfänglichen 302-Statuscode antwortet, ist es möglicherweise besser, der angegebenen Umleitung zu folgen und die HTML Passport-Authentifizierungsseite zu rendern, anstatt WinHTTP die interne Verarbeitung der Authentifizierung zu erlauben. Die Passport-Authentifizierung ist in WinHTTP deaktiviert, indem die [**WinHttpSetOption-Funktion**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) mit der OPTION WINHTTP OPTION CONFIGURE PASSPORT AUTH aufgerufen \_ und der Wert \_ \_ \_ WINHTTP DISABLE PASSPORT AUTH übergeben \_ \_ \_ wird. Sie kann später mit WINHTTP ENABLE PASSPORT AUTH erneut aktiviert \_ \_ \_ werden.

Die Passport-Authentifizierung kann bei Verwendung des [**WinHttpRequest-Objekts**](winhttprequest.md) nicht deaktiviert werden.

Wie bereits erwähnt, ist die Passport-Authentifizierung in WinHTTP 5.1 standardmäßig deaktiviert und muss vor der Verwendung explizit mit [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) aktiviert werden.

## <a name="passport-configuration-overrides-used-for-testing"></a>Für Tests verwendete Passport-Konfigurationsüberschreibungen

WinHTTP basiert auf den Konfigurationsinformationen, die vom Passport Nexus-Server heruntergeladen werden, um die Passport 1.4-Authentifizierung zu unterstützen. Standardmäßig ist dieser sichere Server (SSL) nexus.passport.com, und die Konfigurationsressource ist rdr/pprdr.asp, die als "Live"-Passport-Konfiguration bezeichnet wird. Das Format der Informationen ist ein benutzerdefinierter HTTP-Header "PassportURLs", gefolgt von durch Kommas getrennten Attribut-Wert-Paaren.

Beispielsweise gibt " https://nexus.passport.com/rdr/pprdr.asp " die folgenden Konfigurationsinformationen zurück:

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

Die für WinHTTP relevanten Teile sind DARealm, DALogin und ConfigVersion. Aus Leistungsgründen werden sie für die Lebensdauer einer WinHTTP-Sitzung zwischengespeichert. Diese drei Werte können von Anwendungen überschrieben werden, die für die Arbeit mit einer anderen Passport-Infrastruktur als dem "Live"-Produktionssetup erforderlich sind, indem die entsprechenden Registrierungseinstellungen unter geändert werden.

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

Wenn LoginServerUrl in der Registrierung vorhanden ist, kontaktiert WinHTTP den Nexus-Server nicht für andere Konfigurationswerte. In diesem Fall sollten LoginServerRealm und ConfigVersion auch über die Registrierung festgelegt werden, um Werte zu korrigieren.

Eine Anwendung kann zu Testzwecken erforderlich sein, um die Passport-Konfiguration von einem privaten Nexus-Server herunterzuladen. Dies kann durch Überschreiben von zwei Registrierungswerten unter erfolgen.

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

 

 



