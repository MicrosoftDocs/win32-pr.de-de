---
title: HTTP-Cookies
description: HTTP-Cookies bieten dem Server einen Mechanismus zum Speichern und Abrufen von Zustandsinformationen im System der Client Anwendung.
ms.assetid: c3574592-572f-4fde-adfa-aed3e862f13f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a6855f0b105dc73760541bf9eb7a6da80dfb38e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106342355"
---
# <a name="http-cookies"></a>HTTP-Cookies

HTTP-Cookies bieten dem Server einen Mechanismus zum Speichern und Abrufen von Zustandsinformationen im System der Client Anwendung. Dieser Mechanismus ermöglicht webbasierten Anwendungen die Speicherung von Informationen über ausgewählte Elemente, Benutzereinstellungen, Registrierungsinformationen und andere Informationen, die später abgerufen werden können.

## <a name="cookie-related-headers"></a>Cookie-Related-Header

Es gibt zwei Header (Set-Cookie und Cookie), die mit Cookies in Beziehung stehen. Der Set-Cookie-Header wird vom Server als Antwort auf eine HTTP-Anforderung gesendet, die zum Erstellen eines Cookies im System des Benutzers verwendet wird. Der Cookie-Header ist in der Client Anwendung enthalten, wenn eine HTTP-Anforderung an einen Server gesendet wird, wenn ein Cookie vorhanden ist, das über eine übereinstimmende Domäne und einen entsprechenden Pfad verfügt.

### <a name="set-cookie-header"></a>Set-Cookie-Header

Der Set-Cookie-Antwortheader verwendet das folgende Format:

``` syntax
Set-Cookie: <name>=<value>[; <name>=<value>]...
[; expires=<date>][; domain=<domain_name>]
[; path=<some_path>][; secure][; httponly]
```

Eine oder mehrere Zeichen folgen Sequenzen (getrennt durch Semikolons), die dem Wert des Muster *namens* folgen, =  müssen in den Set-Cookie-Antwortheader eingeschlossen werden. Der Server kann diese Zeichen folgen Sequenzen verwenden, um Daten im System des Clients zu speichern.

Das Ablaufdatum wird mit dem Format läuft =*Date* festgelegt, wobei *Date* das Ablaufdatum in Greenwich Mean Time (GMT) ist. Wenn das Ablaufdatum nicht festgelegt ist, läuft das Cookie ab, nachdem die Internet Sitzung beendet wurde. Andernfalls wird das Cookie bis zum Ablaufdatum im Cache beibehalten. Für das Datum muss folgendes Format verwendet werden:

*Tag*, *DD* - *mmm* - *yyyy* *HH*:*mm*:*SS* GMT

<dl> <dt>

<span id="DAY"></span><span id="day"></span>*Ertag*
</dt> <dd>

Der Wochentag (Sun, Mon, di, Wed, Do, Fri, Sat).

</dd> <dt>

<span id="DD"></span><span id="dd"></span>*Benutzen*
</dt> <dd>

Der Tag im Monat (z. b. 01 für den ersten Tag des Monats).

</dd> <dt>

<span id="MMM"></span><span id="mmm"></span>*Schlampe*
</dt> <dd>

Die drei buchstabige Abkürzung für den Monat (Jan, Feb, Mar, Apr, May, Jun, Jul, Aug, Sep, Oct, Nov, Dec).

</dd> <dt>

<span id="YYYY"></span><span id="yyyy"></span>*JJJJ*
</dt> <dd>

Das Jahr.

</dd> <dt>

<span id="HH"></span><span id="hh"></span>*HH*
</dt> <dd>

Der Stunden Wert in der militärischen Zeit (z. b. 10:00 22 Uhr).

</dd> <dt>

<span id="MM"></span><span id="mm"></span>*MM*
</dt> <dd>

Der Wert für die Minute.

</dd> <dt>

<span id="SS"></span><span id="ss"></span>*Schaden*
</dt> <dd>

Der zweite Wert.

</dd> </dl>

Das Angeben des Domänen Namens mit dem Muster Domain =*Domain \_ Name* ist für persistente Cookies optional und wird verwendet, um das Ende der Domäne anzugeben, für die das Cookie gültig ist. Sitzungs Cookies, die eine Domäne angeben, werden abgelehnt. Wenn der angegebene Domänen Name mit der Anforderung übereinstimmt, versucht das Cookie, den Pfad abzugleichen, um zu bestimmen, ob das Cookie gesendet werden soll. Wenn der Domänen Name z. b. ". Microsoft.com" lautet, werden Anforderungen an Home.Microsoft.com und Support.Microsoft.com geprüft, um festzustellen, ob das angegebene Muster mit der Anforderung übereinstimmt. Der Domänen Name muss mindestens zwei oder drei Zeiträume enthalten, um zu verhindern, dass Cookies für häufig verwendete Domänen namens enden festgelegt werden, z. b.. com,. edu und Co.JP. Zulässige Domänen Namen ähneln. Microsoft.com,. someschool.edu und. someserver.co.JP. Nur Hosts innerhalb der angegebenen Domäne können ein Cookie für eine Domäne festlegen.

Das Festlegen des Pfads unter Verwendung des Muster Pfads = Pfad ist optional und kann verwendet werden, um eine Teilmenge der URLs *anzugeben, für \_* die das Cookie gültig ist. Wenn ein Pfad angegeben wird, gilt das Cookie als gültig für alle Anforderungen, die diesem Pfad entsprechen. Wenn der angegebene Pfad z. b./example lautet, entsprechen Anforderungen mit den Pfaden/examplecode und/Example/code.htm. Wenn kein Pfad angegeben wird, wird davon ausgegangen, dass es sich bei dem Pfad um den Pfad der Ressource handelt, die dem Set-Cookie-Header zugeordnet ist.

Das Cookie kann auch als sicher gekennzeichnet werden, was angibt, dass das Cookie nur an HTTPS-Server gesendet werden kann.

Schließlich kann ein Cookie als HttpOnly gekennzeichnet werden (bei Attributen wird die Groß-/Kleinschreibung nicht beachtet), um anzugeben, dass das Cookie nicht skriptfähig ist und nicht für die Client Anwendung offengelegt werden sollte, aus Sicherheitsgründen. Innerhalb von Windows Internet bedeutet dies, dass das Cookie nicht über die **InternetGetCookie** -Funktion abgerufen werden kann.

### <a name="cookie-header"></a>Cookie-Header

Der Cookie-Header ist in HTTP-Anforderungen mit einem Cookie enthalten, dessen Domäne und Pfad der Anforderung entsprechen. Der Cookie-Header weist das folgende Format auf:

``` syntax
Cookie: <name>=<value> [;<name>=<value>]...
```

Eine oder mehrere Zeichen folgen Sequenzen, bei denen der Format *Name*- = *Wert* verwendet wird, enthalten die Informationen, die im Cookie festgelegt wurden.

## <a name="generating-cookies"></a>Erstellen von Cookies

Es gibt drei Methoden zum Erstellen von Cookies für Microsoft Internet Explorer: die Verwendung von Microsoft JScript, die Verwendung der WinInet-Funktionen und die Verwendung eines CGI-Skripts. Alle Methoden müssen die Informationen festlegen, die im Set-Cookie-Header enthalten sind.

### <a name="generating-a-cookie-using-the-dhtml-object-model"></a>Erstellen eines Cookies mit dem DHTML-Objektmodell

Mit **dem dynamischen** HTML-Objektmodell (DHTML) können Cookies durch Aufrufen der Cookieeigenschaft des Dokument Objekts festgelegt werden, wie im folgenden Beispiel gezeigt.

``` syntax
<SCRIPT language="JavaScript">
<!--
    document.cookie = "SomeValueName = Some_Value";
-->
</SCRIPT>
```

### <a name="generating-a-cookie-using-the-wininet-functions"></a>Erstellen eines Cookies mit den WinInet-Funktionen

Cookies können von Anwendungen mithilfe der [**InternetSetCookie**](/windows/desktop/api/Wininet/nf-wininet-internetsetcookiea) -Funktion erstellt werden. Weitere Informationen finden Sie unter [Festlegen eines Cookies](managing-cookies.md).

### <a name="generating-a-cookie-using-a-cgi-script"></a>Erstellen eines Cookies mithilfe eines CGI-Skripts

Cookies werden generiert, indem ein Set-Cookie-Header als Teil eines CGI-Skripts hinzugefügt wird, das in der HTTP-Antwort für eine Anforderung enthalten ist.

Das folgende Beispiel ist ein CGI-Skript, das einen Set-Cookie-Header mit perl enthält.

``` syntax
print "Set-Cookie:Test=test_value; 
      expires=Sat, 01-Jan-2000 00:00:00 GMT;
      path=/;"
```

> [!Note]  
> WinInet unterstützt keine Server Implementierungen. Außerdem sollte Sie nicht von einem Dienst verwendet werden. Verwenden Sie für Server Implementierungen oder-Dienste [Microsoft Windows HTTP-Dienste (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).

 

 

 