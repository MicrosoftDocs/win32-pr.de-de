---
title: UrlPrefix Strings (UrlPrefix-Zeichenfolgen)
description: In der HTTP-Server-API ist ein UrlPrefix eine Unicode-Zeichenfolge mit Breitzeichen (UTF-16) mit einer kanonischen Form, die einen Abschnitt des URL-Namespace angibt.
ms.assetid: 4f317bf6-ee6a-47a8-a531-78534217109d
keywords:
- URLPrefix-Zeichenfolgen HTTP-Server-API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3fad89bf7abd52ee3681beaa8069a7f5e4ee25b482cd065f880263852690fce
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120047040"
---
# <a name="urlprefix-strings"></a>UrlPrefix Strings (UrlPrefix-Zeichenfolgen)

In der HTTP-Server-API ist ein *UrlPrefix* eine Unicode-Zeichenfolge mit Breitzeichen (UTF-16) mit einer kanonischen Form, die einen Abschnitt des URL-Namespace angibt. Es wird verwendet, um einen Abschnitt des URL-Namespace für ein Benutzerkonto zu reservieren oder einen Abschnitt des URL-Namespace für einen Prozess zu registrieren.

## <a name="urlprefix-format"></a>UrlPrefix-Format

Ein UrlPrefix weist die folgende Syntax auf:

"scheme://host:port/relativeURI"

Die Schema-, Host- und Portelemente eines UrlPrefix müssen vorhanden und nicht leer sein und den folgenden Regeln entsprechen:

<dl> <dt>

<span id="scheme"></span><span id="SCHEME"></span>Schema
</dt> <dd>

Muss entweder http oder https sein, alles in Kleinbuchstaben.

</dd> <dt>

<span id="host"></span><span id="HOST"></span>Host
</dt> <dd>

Muss ein vollqualifizierter Domänenname, eine IPv4- oder IPv6-Literalzeichenfolge oder ein Platzhalter sein. Im Gegensatz zum Schema, das klein geschrieben werden muss, wird bei dem Hostteil die Groß-/Kleinschreibung nicht beachtet. Je nachdem, wie der Hostteil angegeben wird, fällt ein UrlPrefix in eine der folgenden vier Routingkategorien, die unten ausführlicher beschrieben werden:

<dl> <dd>Starker Platzhalter</dd> <dd>Explizit</dd> <dd>IP-gebundener schwacher Platzhalter</dd> <dd>Schwacher Platzhalter</dd> </dl> </dd> <dt>

<span id="port"></span><span id="PORT"></span>Hafen
</dt> <dd>

Eine numerische Dezimalzeichenfolge, die nicht mit 0 beginnt und eine gültige TCP-Portnummer (1 bis 65.535) darstellt. Dieser Wert darf kein Platzhalter sein.

</dd> <dt>

<span id="relativeURI"></span><span id="relativeuri"></span><span id="RELATIVEURI"></span>Relativeuri
</dt> <dd>

Das relativeURI-Element ist optional, aber wenn vorhanden, muss immer ein Schrägstrich ("/") folgen. Dies ist eine Präfixzeichenfolge, die eine Teilstruktur innerhalb des Namespace des Computers angibt, der relativ zum Schema- und Host- und Portwert angegeben ist. Im Gegensatz zum Schema, das klein geschrieben werden muss, wird beim relativeURI-Teil die Groß-/Kleinschreibung nicht beachtet.

</dd> </dl>

Beispiele für ordnungsgemäß formatierte UrlPrefixes sind:

-   `https://www.adatum.com:80/vroot/`
-   `https://adatum.com:443/secure/database/`
-   `https://+:80/vroot/`

## <a name="host-specifier-categories"></a>Host-Specifier Kategorien

Für Flexibilität und Benutzerfreundlichkeit unterstützt die HTTP-Server-API vier verschiedene Methoden zum Angeben von Hosts. Die vier Hostspezifiziererkategorien sind unten nach Rangfolge aufgeführt:

<dl> <dt>

<span id="Strong_wildcard__Plus_Sign_"></span><span id="strong_wildcard__plus_sign_"></span><span id="STRONG_WILDCARD__PLUS_SIGN_"></span>Starker Platzhalter (Pluszeichen)
</dt> <dd>

Wenn das Hostelement eines UrlPrefix aus einem einzelnen Pluszeichen (+) besteht, gleicht das UrlPrefix alle möglichen Hostnamen im Kontext seiner Schema-, Port- und relativeURI-Elemente ab und fällt in die Kategorie mit starkem Platzhalter.

Ein starker Platzhalter ist nützlich, wenn eine Anwendung Anforderungen erfüllen muss, die an eine oder mehrere relativeURIs adressiert sind, unabhängig davon, wie diese Anforderungen auf dem Computer eingehen oder welche Website sie in ihren Hostheadern angeben. Die Verwendung eines starken Platzhalters vermeidet in dieser Situation die Angabe einer vollständigen Liste von Host- und/oder IP-Adressen.

</dd> <dt>

<span id="Explicit"></span><span id="explicit"></span><span id="EXPLICIT"></span>explizit
</dt> <dd>

Ein expliziter Hostname, z. B. ein vollqualifizierte Domänenname im Hostelement, platziert ein UrlPrefix in der expliziten Kategorie. Diese Art von Hostelement wird direkt mit den Hostheadern eingehender Anforderungen abgegleichen.

Explizite Hostspezifikationen sind für Anwendungen mit mehreren Websites nützlich, z. B. Webserver, die je nach Standort, an den die Anforderung weitergeleitet wurde, unterschiedliche Inhalte bereitstellen.

</dd> <dt>

<span id="IP-bound_weak_wildcard"></span><span id="ip-bound_weak_wildcard"></span><span id="IP-BOUND_WEAK_WILDCARD"></span>IP-gebundener schwacher Platzhalter
</dt> <dd>

Wenn eine IP-Adresse als Hostelement angezeigt wird, fällt das UrlPrefix in die IP-gebundene Kategorie Schwacher Platzhalter. Diese Art von UrlPrefix stimmt mit jedem Hostnamen für die angegebene IP-Schnittstelle mit dem angegebenen Schema, Port und relativeURI überein und wurde nicht bereits mit einem starken Platzhalter oder explizitem UrlPrefix abgeglichen. Die IP-Adresse hat eine von zwei Formen im Hostelement:

<dl> <dt>

<span id="IPv4_Literal_String"></span><span id="ipv4_literal_string"></span><span id="IPV4_LITERAL_STRING"></span>IPv4-Literalzeichenfolge
</dt> <dd>

Ein IPv4-Literal besteht aus vier gepunkteten Dezimalzahlen im Bereich von 0 bis 255, z.B. 192.168.0.0.

</dd> <dt>

<span id="IPv6_Literal_String"></span><span id="ipv6_literal_string"></span><span id="IPV6_LITERAL_STRING"></span>IPv6-Literalzeichenfolge
</dt> <dd>

Eine IPv6-Literalzeichenfolge wird in eckige Klammern eingeschlossen und enthält durch Doppelpunkte getrennte hexadezimale Zahlen. Beispiel: \[ ::1 \] oder \[ 3ffe:ffff::6ECB:0101 \] .

</dd> </dl>

IP-gebundene Hostspezifizierer für schwache Platzhalter sind für Anwendungen vorgesehen, die den Inhalt, den sie bedienen, basierend auf der Route variieren, die von eingehenden Anforderungen verwendet wird. Verlassen Sie sich nicht auf IP-gebundene Hostspezifizierer mit schwachem Platzhalter, um die Sicherheit zu erzwingen.

</dd> <dt>

<span id="Weak_wildcard__asterisk_"></span><span id="weak_wildcard__asterisk_"></span><span id="WEAK_WILDCARD__ASTERISK_"></span>Schwacher Platzhalter (Sternchen)
</dt> <dd>

Wenn ein Sternchen \* () als Hostelement angezeigt wird, fällt urlPrefix in die schwache Platzhalterkategorie. Diese Art von UrlPrefix entspricht allen Hostnamen, die dem angegebenen Schema, Port und relativeURI zugeordnet sind, die noch nicht mit einem urlPrefix mit starkem Platzhalter, explizitem oder IP-gebundenem schwachen Platzhalter abgeglichen wurden.

Diese Hostspezifikation kann unter bestimmten Umständen als Standard-Catch-All verwendet werden oder verwendet werden, um einen großen Abschnitt des URL-Namespace anzugeben, ohne viele UrlPrefixe verwenden zu müssen.

</dd> </dl>

## <a name="urlprefix-conflict-detection-during-reservation-and-registration"></a>UrlPrefix-Konflikterkennung während der Reservierung und Registrierung

Zu Reservierungs- und Registrierungszwecken werden die vier verschiedenen UrlPrefix-Kategorien separat behandelt, ohne dass aufeinander verwiesen wird. Es ist möglich, in Konflikt stehende URLPrefixe zu registrieren, solange sie sich in verschiedenen Kategorien befinden. Nur innerhalb derselben Kategorie führt ein Konflikt dazu, dass ein Reservierungsversuch fehlschlägt.

Beispielsweise wäre es möglich, sowohl das explizite UrlPrefix als auch `https://www.adatum.com:80/vroot/` das in Konflikt stehende starke Platzhalter-UrlPrefix zu `https://+:80/vroot/` reservieren, da sie verschiedenen Kategorien angehören. Ein nachfolgender Versuch, einen anderen Benutzer zu reservieren, würde jedoch https://+:80/vroot/ fehlschlagen, da er mit einer vorhandenen Reservierung in seiner eigenen Kategorie in Konflikt geraten würde.

## <a name="routing-behavior"></a>Routingverhalten

Beim Routing einer eingehenden HTTP-Anforderung beginnt die HTTP-Server-API mit der Kategorie mit starkem Platzhalter und vergleicht die eingehende URL mit registrierten und reservierten UrlPrefixes in dieser Kategorie.

Wenn die eingehende URL mit einer Reservierung, aber nicht mit einer Registrierung übereinstimmt, schlägt die HTTP-Server-API die Anforderung fehl. Dadurch wird verhindert, dass Registrierungen mit niedrigerer Priorität Anforderungen aufnehmen können, die nicht für sie vorgesehen sind. Der Status bei einem Fehler lautet 400 ("Ungültige Anforderung") und nicht 503 ("Dienst nicht verfügbar"), da eine 503-Rückgabe manchmal fälschlicherweise von Lastenausgleichsgateways als Hinweis interpretiert wird, dass der Server überlastet war.

Wenn innerhalb der Kategorie eine übereinstimmende Registrierung gefunden wird, wird die Anforderung an die Anforderungswarteschlange weitergeleitet, die dieser Registrierung zugeordnet ist. Die Anforderung wird immer an die Warteschlange weitergeleitet, die dem längsten übereinstimmenden UrlPrefix innerhalb einer Kategorie zugeordnet ist.

Wenn in der Kategorie keine Übereinstimmung gefunden wird, fährt die HTTP-Server-API mit der expliziten Kategorie fort und wiederholt die gleiche Prozedur. Zusammenfassend ist die Reihenfolge, in der die Kategorien untersucht werden, wie folgt:

1.  Starker Platzhalter
2.  Explizit
3.  IP-Bound schwacher Platzhalter
4.  Schwacher Platzhalter

Wenn keine Übereinstimmung in einer der Kategorien gefunden wird, sendet die HTTP-Server-API eine Antwort mit dem Statuscode 400, um anzugeben, dass die Anforderung nicht weitergeleitet werden kann.

## <a name="longest-match-rule"></a>Längste Übereinstimmungsregel

Innerhalb jeder UrlPrefix-Kategorie leitet die HTTP-Server-API eine Anforderung an die Warteschlange weiter, die dem längsten übereinstimmenden UrlPrefix zugeordnet ist. Angenommen, die folgenden beiden UrlPrefixe sind in verschiedenen Warteschlangen registriert:

- `Queue1 https://www.adatum.com:80/`
- `Queue2 https://www.adatum.com:80/dir/sna/`

Die HTTP-Server-API leitet eine Anforderung für `https://www.adatum.com:80/default.htm` an Queue1 und eine Anforderung für `https://www.adatum.com:80/dir/sna/snadefault.htm` an Queue2 weiter. Es leitet eine Anforderung für `https://www.adatum.com:80/dir/app.htm` an Queue1 weiter, da die längste vollständige Übereinstimmung mit dem `https://www.adatum.com:80/` UrlPrefix und nicht mit dem `https://www.adatum.com:80/dir/sna` UrlPrefix erfolgt.

 

 




