---
title: HTTP-Cookies
description: HTTP-Cookies bieten dem Server einen Mechanismus zum Speichern und Abrufen von Zustandsinformationen auf dem System der Clientanwendung.
ms.assetid: c3574592-572f-4fde-adfa-aed3e862f13f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0ba5b2d3917ea8f140e334f5f78b1bd730908d25506d9023667403410833c80
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118113714"
---
# <a name="http-cookies"></a>HTTP-Cookies

HTTP-Cookies bieten dem Server einen Mechanismus zum Speichern und Abrufen von Zustandsinformationen auf dem System der Clientanwendung. Dieser Mechanismus ermöglicht webbasierten Anwendungen das Speichern von Informationen zu ausgewählten Elementen, Benutzereinstellungen, Registrierungsinformationen und anderen Informationen, die später abgerufen werden können.

## <a name="cookie-related-headers"></a>Cookie-Related Header

Es gibt zwei Header, Set-Cookie und Cookie, die sich auf Cookies bezogen haben. Der Set-Cookie-Header wird vom Server als Antwort auf eine HTTP-Anforderung gesendet, die zum Erstellen eines Cookies auf dem System des Benutzers verwendet wird. Der Cookie-Header wird von der Clientanwendung mit einer HTTP-Anforderung an einen Server gesendet, wenn ein Cookie mit einer übereinstimmenden Domäne und einem übereinstimmenden Pfad vor liegt.

### <a name="set-cookie-header"></a>Set-Cookie Header

Der Set-Cookie Antwortheader verwendet das folgende Format:

``` syntax
Set-Cookie: <name>=<value>[; <name>=<value>]...
[; expires=<date>][; domain=<domain_name>]
[; path=<some_path>][; secure][; httponly]
```

Eine oder mehrere Zeichenfolgensequenzen (durch Semikolons getrennt), die dem Wert des Musternamens folgen, müssen im Antwortheader Set-Cookie =  enthalten sein. Der Server kann diese Zeichenfolgensequenzen verwenden, um Daten auf dem System des Clients zu speichern.

Das Ablaufdatum wird mit dem Format expires=*date* festgelegt, wobei *date* das Ablaufdatum in Greenwich Mean Time (GMT) ist. Wenn das Ablaufdatum nicht festgelegt ist, läuft das Cookie ab, nachdem die Internetsitzung beendet wurde. Andernfalls wird das Cookie bis zum Ablaufdatum im Cache beibehalten. Das Datum muss das folgende Format verwenden:

*DAY*, *DD* - *MMM* - *YYYY* *HH*:*MM*:*SS* GMT

<dl> <dt>

<span id="DAY"></span><span id="day"></span>*Tag*
</dt> <dd>

Der Wochentag (So, Mon, Tue, Wed, Do, Fr, Sa).

</dd> <dt>

<span id="DD"></span><span id="dd"></span>*Dd*
</dt> <dd>

Der Tag im Monat (z. B. 01 für den ersten Tag des Monats).

</dd> <dt>

<span id="MMM"></span><span id="mmm"></span>*Mmm*
</dt> <dd>

Die drei buchstabenbasierte Abkürzung für den Monat (Jan, Feb, Mar, Apr, May, Jun, Jul, Aug, Sep, Oct, Nov, Dec).

</dd> <dt>

<span id="YYYY"></span><span id="yyyy"></span>*Jjjj*
</dt> <dd>

Das Jahr.

</dd> <dt>

<span id="HH"></span><span id="hh"></span>*Hh*
</dt> <dd>

Der Stundenwert in Der Uhrzeit (22 wäre z. B. 22:00 Uhr).

</dd> <dt>

<span id="MM"></span><span id="mm"></span>*Mm*
</dt> <dd>

Der Wert für die Minute.

</dd> <dt>

<span id="SS"></span><span id="ss"></span>*Ss*
</dt> <dd>

Der zweite Wert.

</dd> </dl>

Die Angabe des Domänennamens unter Verwendung des Domänennamens pattern *domain= \_* ist für persistente Cookies optional und wird verwendet, um das Ende der Domäne anzugeben, für die das Cookie gültig ist. Sitzungscookies, die eine Domäne angeben, werden abgelehnt. Wenn das angegebene Domänennamenende der Anforderung entspricht, versucht das Cookie, mit dem Pfad zu übereinstimmen, um zu bestimmen, ob das Cookie gesendet werden soll. Wenn der Domänenname beispielsweise auf .microsoft.com endet, werden Anforderungen an home.microsoft.com und support.microsoft.com überprüft, um zu überprüfen, ob das angegebene Muster der Anforderung entspricht. Der Domänenname muss mindestens zwei oder drei Punkte haben, um zu verhindern, dass Cookies für häufig verwendete Domänennamenenden wie .com, .edu und co.jp. Zulässige Domänennamen ähneln .microsoft.com, .someschool.edu und .someserver.co.jp. Nur Hosts innerhalb der angegebenen Domäne können ein Cookie für eine Domäne festlegen.

Das Festlegen des Pfads *\_* mithilfe des Musterpfads = eines Pfads ist optional und kann verwendet werden, um eine Teilmenge der URLs anzugeben, für die das Cookie gültig ist. Wenn ein Pfad angegeben wird, wird das Cookie für alle Anforderungen, die mit diesem Pfad übereinstimmen, als gültig betrachtet. Wenn der angegebene Pfad beispielsweise /example ist, würden Anforderungen mit den Pfaden /examplecode und /example/code.htm übereinstimmen. Wenn kein Pfad angegeben wird, wird davon ausgegangen, dass es sich bei dem Pfad um den Pfad der Ressource handelt, die dem Set-Cookie zugeordnet ist.

Das Cookie kann auch als sicher markiert werden, was angibt, dass das Cookie nur an HTTPS-Server gesendet werden kann.

Schließlich kann ein Cookie als HttpOnly gekennzeichnet werden (bei Attributen wird die Schreibung nicht beachtet), um anzugeben, dass das Cookie nicht skriptfähig ist und aus Sicherheitsgründen nicht für die Clientanwendung angezeigt werden sollte. Innerhalb Windows Internet bedeutet dies, dass das Cookie nicht über die **InternetGetCookie-Funktion abgerufen werden** kann.

### <a name="cookie-header"></a>Cookieheader

Der Cookie-Header ist in allen HTTP-Anforderungen enthalten, die über ein Cookie verfügen, dessen Domäne und Pfad mit der Anforderung übereinstimmen. Der Cookie-Header hat das folgende Format:

``` syntax
Cookie: <name>=<value> [;<name>=<value>]...
```

Mindestens eine Zeichenfolgensequenz mit dem *Formatnamenswert* enthält die Informationen, = die im Cookie festgelegt wurden.

## <a name="generating-cookies"></a>Generieren von Cookies

Es gibt drei Methoden zum Generieren von Cookies für Microsoft Internet Explorer: die Verwendung von Microsoft JScript, die Verwendung der WinINet-Funktionen und die Verwendung eines CGI-Skripts. Alle Methoden müssen die Informationen festlegen, die im Header Set-Cookie sind.

### <a name="generating-a-cookie-using-the-dhtml-object-model"></a>Generieren eines Cookies mithilfe des DHTML-Objektmodells

Mithilfe des DHTML-Objektmodells (Dynamic HTML) können Cookies durch Aufrufen der **Cookieeigenschaft** des Dokumentobjekts festgelegt werden, wie im folgenden Beispiel gezeigt.

``` syntax
<SCRIPT language="JavaScript">
<!--
    document.cookie = "SomeValueName = Some_Value";
-->
</SCRIPT>
```

### <a name="generating-a-cookie-using-the-wininet-functions"></a>Generieren eines Cookies mithilfe der WinInet-Funktionen

Cookies können von Anwendungen mithilfe der [**InternetSetCookie-Funktion erstellt**](/windows/desktop/api/Wininet/nf-wininet-internetsetcookiea) werden. Weitere Informationen finden Sie unter [Setting a Cookie](managing-cookies.md).

### <a name="generating-a-cookie-using-a-cgi-script"></a>Generieren eines Cookies mithilfe eines CGI-Skripts

Cookies werden generiert, indem ein Set-Cookie-Header als Teil eines CGI-Skripts eingeschlossen wird, das in der HTTP-Antwort auf eine Anforderung enthalten ist.

Das folgende Beispiel ist ein CGI-Skript, das einen Set-Cookie per Perl enthält.

``` syntax
print "Set-Cookie:Test=test_value; 
      expires=Sat, 01-Jan-2000 00:00:00 GMT;
      path=/;"
```

> [!Note]  
> WinINet unterstützt keine Serverimplementierung. Darüber hinaus sollte sie nicht von einem Dienst verwendet werden. Verwenden Sie für Serverimplementierungen oder -dienste [Microsoft Windows HTTP Services (WinHTTP).](/windows/desktop/WinHttp/winhttp-start-page)

 

 

 