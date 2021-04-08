---
title: UrlPrefix Strings (UrlPrefix-Zeichenfolgen)
description: In der HTTP-Server-API ist ein URLPrefix eine breit Zeichen-Unicode-Zeichenfolge (UTF-16) mit einer kanonischen Form, die einen Abschnitt des URL-Namespace angibt.
ms.assetid: 4f317bf6-ee6a-47a8-a531-78534217109d
keywords:
- URLPrefix-Zeichen folgen http-Server-API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bddc484f26bc1b3de5d20196dadec9201d3ea272
ms.sourcegitcommit: 73417d55867c804274a55abe5ca71bcba7006119
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/20/2020
ms.locfileid: "103734737"
---
# <a name="urlprefix-strings"></a>UrlPrefix Strings (UrlPrefix-Zeichenfolgen)

In der HTTP-Server-API ist ein *URLPrefix* eine breit Zeichen-Unicode-Zeichenfolge (UTF-16) mit einer kanonischen Form, die einen Abschnitt des URL-Namespace angibt. Es wird verwendet, um einen Abschnitt des URL-Namespace für ein Benutzerkonto zu reservieren oder um einen Abschnitt des URL-Namespace für einen Prozess zu registrieren.

## <a name="urlprefix-format"></a>URLPrefix-Format

Ein URLPrefix weist die folgende Syntax auf:

"Schema://Host: Port/relativeUri"

Die Elemente "Schema", "Host" und "Port" eines URLPrefix müssen vorhanden und nicht leer sein und müssen die folgenden Regeln einhalten:

<dl> <dt>

<span id="scheme"></span><span id="SCHEME"></span>Schrift
</dt> <dd>

Muss entweder "http" oder "https" lauten, in Kleinbuchstaben.

</dd> <dt>

<span id="host"></span><span id="HOST"></span>Host
</dt> <dd>

Muss ein voll qualifizierter Domänen Name, eine IPv4-oder IPv6-Literalzeichenfolge oder ein Platzhalter sein. Anders als bei dem Schema, das klein geschrieben werden muss, wird die Groß-/Kleinschreibung nicht beachtet. Abhängig von der Angabe des Host Teils fällt ein URLPrefix in eine der vier folgenden Routing Kategorien, die unten ausführlicher beschrieben werden:

<dl> <dd>Starker Platzhalter</dd> <dd>Explizit</dd> <dd>IP-gebundene schwache Platzhalter</dd> <dd>Schwacher Platzhalter</dd> </dl> </dd> <dt>

<span id="port"></span><span id="PORT"></span>Port
</dt> <dd>

Eine numerische Dezimal Zeichenfolge, die nicht mit 0 beginnt und eine gültige TCP-Portnummer darstellt (1 bis 65.535). Dieser Wert darf kein Platzhalter sein.

</dd> <dt>

<span id="relativeURI"></span><span id="relativeuri"></span><span id="RELATIVEURI"></span>relativeURI
</dt> <dd>

Das relativeUri-Element ist optional, aber wenn Present vorhanden ist, muss immer ein Schrägstrich ("/") gefolgt werden. Dies ist eine Präfix Zeichenfolge, die eine Unterstruktur im Namespace des Computers angibt, die relativ zu den Werten für Schema, Host und Port angegeben wird. Anders als bei dem Schema, das klein geschrieben werden muss, wird die Groß-/Kleinschreibung vom relativeUri-Teil nicht beachtet.

</dd> </dl>

Beispiele für ordnungsgemäß formatierte URLPrefixes:

-   `https://www.adatum.com:80/vroot/`
-   `https://adatum.com:443/secure/database/`
-   `https://+:80/vroot/`

## <a name="host-specifier-categories"></a>Host-Specifier Kategorien

Aus Gründen der Flexibilität und Benutzerfreundlichkeit unterstützt die HTTP-Server-API vier verschiedene Möglichkeiten zum Angeben von Hosts. Die vier hostspezifiziererkategorien sind unten in der Rangfolge aufgeführt:

<dl> <dt>

<span id="Strong_wildcard__Plus_Sign_"></span><span id="strong_wildcard__plus_sign_"></span><span id="STRONG_WILDCARD__PLUS_SIGN_"></span>Starker Platzhalter (Plus Zeichen)
</dt> <dd>

Wenn das Host Element eines URLPrefix aus einem einzelnen Pluszeichen (+) besteht, gleicht das URLPrefix alle möglichen Hostnamen im Kontext seiner Schema-, Port-und relativeUri-Elemente ab und fällt in die Kategorie für den starken Platzhalter.

Ein starker Platzhalter ist nützlich, wenn eine Anwendung Anforderungen verarbeiten muss, die an mindestens einen relativeuris adressiert sind, unabhängig davon, wie diese Anforderungen auf dem Computer eintreffen oder welche Website Sie in Ihren Host Headern angeben. Durch die Verwendung eines starken Platzhalters in dieser Situation entfällt die Notwendigkeit, eine vollständige Liste von Host-und/oder IP-Adressen anzugeben.

</dd> <dt>

<span id="Explicit"></span><span id="explicit"></span><span id="EXPLICIT"></span>Explizite
</dt> <dd>

Ein expliziter Hostname, z. b. ein voll qualifizierter Domänen Name im Host-Element, platziert ein URLPrefix in der expliziten Kategorie. Diese Art von Host Element wird direkt mit den Host Headern eingehender Anforderungen abgeglichen.

Explizite Host Spezifikationen sind für Anwendungen mit mehreren Standorten nützlich, z. b. Webserver, die abhängig von der Website, an die die Anforderung gerichtet wurde, unterschiedliche Inhalte bereitstellen.

</dd> <dt>

<span id="IP-bound_weak_wildcard"></span><span id="ip-bound_weak_wildcard"></span><span id="IP-BOUND_WEAK_WILDCARD"></span>IP-gebundene schwache Platzhalter
</dt> <dd>

Wenn eine IP-Adresse als Host Element angezeigt wird, fällt das URLPrefix in die IP-gebundene schwache Platzhalter Kategorie. Diese Art von URLPrefix stimmt mit jedem Hostnamen für die angegebene IP-Schnittstelle mit dem angegebenen Schema, Port und relativeUri überein und ist nicht bereits mit einem starken oder expliziten URLPrefix übereinstimmt. Die IP-Adresse nimmt eine von zwei Formen im Host Element an:

<dl> <dt>

<span id="IPv4_Literal_String"></span><span id="ipv4_literal_string"></span><span id="IPV4_LITERAL_STRING"></span>IPv4-Literalzeichen
</dt> <dd>

Ein IPv4-Literale besteht aus vier Dezimalzahlen im Bereich 0-255, z. b. 192.168.0.0.

</dd> <dt>

<span id="IPv6_Literal_String"></span><span id="ipv6_literal_string"></span><span id="IPV6_LITERAL_STRING"></span>IPv6-Zeichenfolge
</dt> <dd>

Eine IPv6-Literalzeichenfolge wird in eckige Klammern eingeschlossen und enthält durch Doppelpunkte getrennte hexadezimal Zahlen. Beispiel: \[ :: 1 \] oder \[ 3FFE: FFFF:: 6ecb: 0101 \] .

</dd> </dl>

IP-gebundene Host Bearbeiter mit schwacher Platzhalter sind für Anwendungen bestimmt, die den von Ihnen bereit gedienten Inhalt basierend auf der Route von eingehenden Anforderungen variieren. Verlassen Sie sich nicht auf IP-gebundene hostspezifizierer mit schwacher Platzhalter, um die Sicherheit zu erzwingen.

</dd> <dt>

<span id="Weak_wildcard__asterisk_"></span><span id="weak_wildcard__asterisk_"></span><span id="WEAK_WILDCARD__ASTERISK_"></span>Schwacher Platzhalter (Sternchen)
</dt> <dd>

Wenn ein Sternchen ( \* ) als Host Element angezeigt wird, fällt das URLPrefix in die schwache Platzhalter Kategorie. Diese Art von URLPrefix entspricht jedem Hostnamen, der dem angegebenen Schema, Port und relativeUri zugeordnet ist, die noch nicht mit einem starken Platzhalter-, expliziten oder IP-gebundenen URLPrefix für schwache Platzhalter übereinstimmen.

Diese Host Spezifikation kann in einigen Fällen als Standard-Catch-All verwendet werden, oder Sie kann verwendet werden, um einen großen Abschnitt des URL-Namespace anzugeben, ohne viele URLPrefixes verwenden zu müssen.

</dd> </dl>

## <a name="urlprefix-conflict-detection-during-reservation-and-registration"></a>URLPrefix-Konflikterkennung während der Reservierung und Registrierung

Zu Reservierungs-und Registrierungszwecken werden die vier unterschiedlichen Kategorien von URLPrefix separat behandelt, ohne dass Sie aufeinander verweisen. In Konflikt stehende URLPrefixes können registriert werden, solange Sie sich in verschiedenen Kategorien befinden. Nur innerhalb derselben Kategorie führt ein Konflikt dazu, dass ein Reservierungs Versuch fehlschlägt.

Beispielsweise wäre es möglich, sowohl das explizite URLPrefix `https://www.adatum.com:80/vroot/` als auch das in Konflikt stehende starke Platzhalter-URLPrefix zu reservieren `https://+:80/vroot/` , da Sie zu unterschiedlichen Kategorien gehören. Bei einem nachfolgenden Versuch, einen anderen Benutzer zu reservieren, tritt jedoch ein Fehler auf, https://+:80/vroot/ weil er mit einer vorhandenen Reservierung in seiner eigenen Kategorie in Konflikt steht.

## <a name="routing-behavior"></a>Routing Verhalten

Wenn Sie eine eingehende HTTP-Anforderung weiterleiten, beginnt die HTTP-Server-API mit der Kategorie "starker Platzhalter" und vergleicht die eingehende URL mit den registrierten und reservierten URLPrefixes in dieser Kategorie.

Wenn die eingehende URL mit einer Reservierung, aber nicht mit einer Registrierung übereinstimmt, schlägt die HTTP-Server-API die Anforderung fehl. Dadurch wird verhindert, dass Registrierungen mit niedrigerer Priorität die nicht dafür vorgesehenen Anforderungen abrufen können. Der Status bei einem Fehler ist 400 ("Ungültige Anforderung") anstelle von "503" ("Dienst nicht verfügbar"), da eine 503-Rückgabe manchmal versehentlich von Lasten Ausgleichs Gateways interpretiert wird, was darauf hinweist, dass der Server überladen wurde.

Wenn eine übereinstimmende Registrierung in der Kategorie gefunden wird, wird die Anforderung an die Anforderungs Warteschlange weitergeleitet, die mit dieser Registrierung verknüpft ist. Die Anforderung wird immer an die Warteschlange weitergeleitet, die dem längsten übereinstimmenden URLPrefix innerhalb einer Kategorie zugeordnet ist.

Wenn in der Kategorie keine Übereinstimmung gefunden wird, fährt die HTTP-Server-API mit der expliziten Kategorie fort und wiederholt dieselbe Prozedur. Zusammenfassend gilt: die Reihenfolge, in der die Kategorien überprüft werden, lautet wie folgt:

1.  Starker Platzhalter
2.  Explizit
3.  IP-Bound schwache Platzhalter
4.  Schwacher Platzhalter

Wenn keine Entsprechung in einer der Kategorien gefunden wird, sendet die HTTP-Server-API eine Antwort mit dem Statuscode 400, um anzugeben, dass die Anforderung nicht weitergeleitet werden kann.

## <a name="longest-match-rule"></a>Längste Übereinstimmungs Regel

Innerhalb jeder URLPrefix-Kategorie leitet die HTTP-Server-API eine Anforderung an die Warteschlange weiter, die dem längsten übereinstimmenden URLPrefix zugeordnet ist. Nehmen wir beispielsweise an, dass die beiden folgenden URLPrefixes für verschiedene Warteschlangen registriert sind:

- `Queue1 https://www.adatum.com:80/`
- `Queue2 https://www.adatum.com:80/dir/sna/`

Die HTTP-Server-API leitet eine Anforderung für `https://www.adatum.com:80/default.htm` an "queue1" und eine Anforderung `https://www.adatum.com:80/dir/sna/snadefault.htm` an Queue2. Die Anforderung `https://www.adatum.com:80/dir/app.htm` wird an "queue1" weitergeleitet, da die längste Vervollständigung mit dem `https://www.adatum.com:80/` URLPrefix, nicht mit dem `https://www.adatum.com:80/dir/sna` URLPrefix-Wert ist.

 

 




