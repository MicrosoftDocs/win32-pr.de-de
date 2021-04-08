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
# <a name="urlprefix-strings"></a><span data-ttu-id="d4fda-104">UrlPrefix Strings (UrlPrefix-Zeichenfolgen)</span><span class="sxs-lookup"><span data-stu-id="d4fda-104">UrlPrefix Strings</span></span>

<span data-ttu-id="d4fda-105">In der HTTP-Server-API ist ein *URLPrefix* eine breit Zeichen-Unicode-Zeichenfolge (UTF-16) mit einer kanonischen Form, die einen Abschnitt des URL-Namespace angibt.</span><span class="sxs-lookup"><span data-stu-id="d4fda-105">In the HTTP Server API, a *UrlPrefix* is a wide-character (UTF-16) Unicode string with a canonical form that specifies a section of URL namespace.</span></span> <span data-ttu-id="d4fda-106">Es wird verwendet, um einen Abschnitt des URL-Namespace für ein Benutzerkonto zu reservieren oder um einen Abschnitt des URL-Namespace für einen Prozess zu registrieren.</span><span class="sxs-lookup"><span data-stu-id="d4fda-106">It is used to reserve a section of URL namespace for a user account or register a section of URL namespace for a process.</span></span>

## <a name="urlprefix-format"></a><span data-ttu-id="d4fda-107">URLPrefix-Format</span><span class="sxs-lookup"><span data-stu-id="d4fda-107">UrlPrefix Format</span></span>

<span data-ttu-id="d4fda-108">Ein URLPrefix weist die folgende Syntax auf:</span><span class="sxs-lookup"><span data-stu-id="d4fda-108">A UrlPrefix has the following syntax:</span></span>

<span data-ttu-id="d4fda-109">"Schema://Host: Port/relativeUri"</span><span class="sxs-lookup"><span data-stu-id="d4fda-109">"scheme://host:port/relativeURI"</span></span>

<span data-ttu-id="d4fda-110">Die Elemente "Schema", "Host" und "Port" eines URLPrefix müssen vorhanden und nicht leer sein und müssen die folgenden Regeln einhalten:</span><span class="sxs-lookup"><span data-stu-id="d4fda-110">The scheme, host and port elements of a UrlPrefix must be present and non-empty, and must obey the following rules:</span></span>

<dl> <dt>

<span data-ttu-id="d4fda-111"><span id="scheme"></span><span id="SCHEME"></span>Schrift</span><span class="sxs-lookup"><span data-stu-id="d4fda-111"><span id="scheme"></span><span id="SCHEME"></span>scheme</span></span>
</dt> <dd>

<span data-ttu-id="d4fda-112">Muss entweder "http" oder "https" lauten, in Kleinbuchstaben.</span><span class="sxs-lookup"><span data-stu-id="d4fda-112">Must be either http or https, all in lowercase.</span></span>

</dd> <dt>

<span data-ttu-id="d4fda-113"><span id="host"></span><span id="HOST"></span>Host</span><span class="sxs-lookup"><span data-stu-id="d4fda-113"><span id="host"></span><span id="HOST"></span>host</span></span>
</dt> <dd>

<span data-ttu-id="d4fda-114">Muss ein voll qualifizierter Domänen Name, eine IPv4-oder IPv6-Literalzeichenfolge oder ein Platzhalter sein.</span><span class="sxs-lookup"><span data-stu-id="d4fda-114">Must be a fully qualified domain name, an IPv4 or IPv6 literal string, or a wildcard.</span></span> <span data-ttu-id="d4fda-115">Anders als bei dem Schema, das klein geschrieben werden muss, wird die Groß-/Kleinschreibung nicht beachtet.</span><span class="sxs-lookup"><span data-stu-id="d4fda-115">Unlike the scheme, which must be lowercase, the host portion is case-insensitive.</span></span> <span data-ttu-id="d4fda-116">Abhängig von der Angabe des Host Teils fällt ein URLPrefix in eine der vier folgenden Routing Kategorien, die unten ausführlicher beschrieben werden:</span><span class="sxs-lookup"><span data-stu-id="d4fda-116">Depending on how its host portion is specified, a UrlPrefix falls into one of the following four routing categories, which are described in more detail below:</span></span>

<dl> <dd><span data-ttu-id="d4fda-117">Starker Platzhalter</span><span class="sxs-lookup"><span data-stu-id="d4fda-117">Strong wildcard</span></span></dd> <dd><span data-ttu-id="d4fda-118">Explizit</span><span class="sxs-lookup"><span data-stu-id="d4fda-118">Explicit</span></span></dd> <dd><span data-ttu-id="d4fda-119">IP-gebundene schwache Platzhalter</span><span class="sxs-lookup"><span data-stu-id="d4fda-119">IP-bound weak wildcard</span></span></dd> <dd><span data-ttu-id="d4fda-120">Schwacher Platzhalter</span><span class="sxs-lookup"><span data-stu-id="d4fda-120">Weak wildcard</span></span></dd> </dl> </dd> <dt>

<span data-ttu-id="d4fda-121"><span id="port"></span><span id="PORT"></span>Port</span><span class="sxs-lookup"><span data-stu-id="d4fda-121"><span id="port"></span><span id="PORT"></span>port</span></span>
</dt> <dd>

<span data-ttu-id="d4fda-122">Eine numerische Dezimal Zeichenfolge, die nicht mit 0 beginnt und eine gültige TCP-Portnummer darstellt (1 bis 65.535).</span><span class="sxs-lookup"><span data-stu-id="d4fda-122">A decimal numeric string that does not start with zero and that represents a valid TCP port number (1 to 65,535).</span></span> <span data-ttu-id="d4fda-123">Dieser Wert darf kein Platzhalter sein.</span><span class="sxs-lookup"><span data-stu-id="d4fda-123">This value cannot be a wildcard.</span></span>

</dd> <dt>

<span data-ttu-id="d4fda-124"><span id="relativeURI"></span><span id="relativeuri"></span><span id="RELATIVEURI"></span>relativeURI</span><span class="sxs-lookup"><span data-stu-id="d4fda-124"><span id="relativeURI"></span><span id="relativeuri"></span><span id="RELATIVEURI"></span>relativeURI</span></span>
</dt> <dd>

<span data-ttu-id="d4fda-125">Das relativeUri-Element ist optional, aber wenn Present vorhanden ist, muss immer ein Schrägstrich ("/") gefolgt werden.</span><span class="sxs-lookup"><span data-stu-id="d4fda-125">The relativeURI element is optional, but if present must always be followed by a slash character ("/").</span></span> <span data-ttu-id="d4fda-126">Dies ist eine Präfix Zeichenfolge, die eine Unterstruktur im Namespace des Computers angibt, die relativ zu den Werten für Schema, Host und Port angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="d4fda-126">This is a prefix string that indicates a subtree within the machine's namespace specified relative to the scheme, host and port values.</span></span> <span data-ttu-id="d4fda-127">Anders als bei dem Schema, das klein geschrieben werden muss, wird die Groß-/Kleinschreibung vom relativeUri-Teil nicht beachtet.</span><span class="sxs-lookup"><span data-stu-id="d4fda-127">Unlike the scheme, which must be lowercase, the relativeURI portion is case-insensitive.</span></span>

</dd> </dl>

<span data-ttu-id="d4fda-128">Beispiele für ordnungsgemäß formatierte URLPrefixes:</span><span class="sxs-lookup"><span data-stu-id="d4fda-128">Examples of properly formed UrlPrefixes are:</span></span>

-   `https://www.adatum.com:80/vroot/`
-   `https://adatum.com:443/secure/database/`
-   `https://+:80/vroot/`

## <a name="host-specifier-categories"></a><span data-ttu-id="d4fda-129">Host-Specifier Kategorien</span><span class="sxs-lookup"><span data-stu-id="d4fda-129">Host-Specifier Categories</span></span>

<span data-ttu-id="d4fda-130">Aus Gründen der Flexibilität und Benutzerfreundlichkeit unterstützt die HTTP-Server-API vier verschiedene Möglichkeiten zum Angeben von Hosts.</span><span class="sxs-lookup"><span data-stu-id="d4fda-130">For flexibility and ease of use, the HTTP Server API supports four different ways to specify hosts.</span></span> <span data-ttu-id="d4fda-131">Die vier hostspezifiziererkategorien sind unten in der Rangfolge aufgeführt:</span><span class="sxs-lookup"><span data-stu-id="d4fda-131">The four host-specifier categories are listed below in order of precedence:</span></span>

<dl> <dt>

<span data-ttu-id="d4fda-132"><span id="Strong_wildcard__Plus_Sign_"></span><span id="strong_wildcard__plus_sign_"></span><span id="STRONG_WILDCARD__PLUS_SIGN_"></span>Starker Platzhalter (Plus Zeichen)</span><span class="sxs-lookup"><span data-stu-id="d4fda-132"><span id="Strong_wildcard__Plus_Sign_"></span><span id="strong_wildcard__plus_sign_"></span><span id="STRONG_WILDCARD__PLUS_SIGN_"></span>Strong wildcard (Plus Sign)</span></span>
</dt> <dd>

<span data-ttu-id="d4fda-133">Wenn das Host Element eines URLPrefix aus einem einzelnen Pluszeichen (+) besteht, gleicht das URLPrefix alle möglichen Hostnamen im Kontext seiner Schema-, Port-und relativeUri-Elemente ab und fällt in die Kategorie für den starken Platzhalter.</span><span class="sxs-lookup"><span data-stu-id="d4fda-133">When the host element of a UrlPrefix consists of a single plus sign (+), the UrlPrefix matches all possible host names in the context of its scheme, port and relativeURI elements, and falls into the strong wildcard category.</span></span>

<span data-ttu-id="d4fda-134">Ein starker Platzhalter ist nützlich, wenn eine Anwendung Anforderungen verarbeiten muss, die an mindestens einen relativeuris adressiert sind, unabhängig davon, wie diese Anforderungen auf dem Computer eintreffen oder welche Website Sie in Ihren Host Headern angeben.</span><span class="sxs-lookup"><span data-stu-id="d4fda-134">A strong wildcard is useful when an application needs to serve requests addressed to one or more relativeURIs, regardless of how those requests arrive on the machine or what site they specify in their Host headers.</span></span> <span data-ttu-id="d4fda-135">Durch die Verwendung eines starken Platzhalters in dieser Situation entfällt die Notwendigkeit, eine vollständige Liste von Host-und/oder IP-Adressen anzugeben.</span><span class="sxs-lookup"><span data-stu-id="d4fda-135">Use of a strong wildcard in this situation avoids the need to specify an exhaustive list of host and/or IP-addresses.</span></span>

</dd> <dt>

<span data-ttu-id="d4fda-136"><span id="Explicit"></span><span id="explicit"></span><span id="EXPLICIT"></span>Explizite</span><span class="sxs-lookup"><span data-stu-id="d4fda-136"><span id="Explicit"></span><span id="explicit"></span><span id="EXPLICIT"></span>Explicit</span></span>
</dt> <dd>

<span data-ttu-id="d4fda-137">Ein expliziter Hostname, z. b. ein voll qualifizierter Domänen Name im Host-Element, platziert ein URLPrefix in der expliziten Kategorie.</span><span class="sxs-lookup"><span data-stu-id="d4fda-137">An explicit host name such as a fully qualified domain name in the host element places a UrlPrefix in the explicit category.</span></span> <span data-ttu-id="d4fda-138">Diese Art von Host Element wird direkt mit den Host Headern eingehender Anforderungen abgeglichen.</span><span class="sxs-lookup"><span data-stu-id="d4fda-138">This kind of host element is matched directly against the Host headers of incoming requests.</span></span>

<span data-ttu-id="d4fda-139">Explizite Host Spezifikationen sind für Anwendungen mit mehreren Standorten nützlich, z. b. Webserver, die abhängig von der Website, an die die Anforderung gerichtet wurde, unterschiedliche Inhalte bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="d4fda-139">Explicit host specifications are useful for multi-site applications such as Web servers that deliver different content depending on the site to which the request was directed.</span></span>

</dd> <dt>

<span data-ttu-id="d4fda-140"><span id="IP-bound_weak_wildcard"></span><span id="ip-bound_weak_wildcard"></span><span id="IP-BOUND_WEAK_WILDCARD"></span>IP-gebundene schwache Platzhalter</span><span class="sxs-lookup"><span data-stu-id="d4fda-140"><span id="IP-bound_weak_wildcard"></span><span id="ip-bound_weak_wildcard"></span><span id="IP-BOUND_WEAK_WILDCARD"></span>IP-bound weak wildcard</span></span>
</dt> <dd>

<span data-ttu-id="d4fda-141">Wenn eine IP-Adresse als Host Element angezeigt wird, fällt das URLPrefix in die IP-gebundene schwache Platzhalter Kategorie.</span><span class="sxs-lookup"><span data-stu-id="d4fda-141">When an IP address appears as the host element, then the UrlPrefix falls into the IP-bound Weak Wildcard category.</span></span> <span data-ttu-id="d4fda-142">Diese Art von URLPrefix stimmt mit jedem Hostnamen für die angegebene IP-Schnittstelle mit dem angegebenen Schema, Port und relativeUri überein und ist nicht bereits mit einem starken oder expliziten URLPrefix übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="d4fda-142">This kind of UrlPrefix matches any host name for the specified IP interface with the specified scheme, port and relativeURI, and that has not already been matched by a strong-wildcard or explicit UrlPrefix.</span></span> <span data-ttu-id="d4fda-143">Die IP-Adresse nimmt eine von zwei Formen im Host Element an:</span><span class="sxs-lookup"><span data-stu-id="d4fda-143">The IP address takes one of two forms in the host element:</span></span>

<dl> <dt>

<span data-ttu-id="d4fda-144"><span id="IPv4_Literal_String"></span><span id="ipv4_literal_string"></span><span id="IPV4_LITERAL_STRING"></span>IPv4-Literalzeichen</span><span class="sxs-lookup"><span data-stu-id="d4fda-144"><span id="IPv4_Literal_String"></span><span id="ipv4_literal_string"></span><span id="IPV4_LITERAL_STRING"></span>IPv4 Literal String</span></span>
</dt> <dd>

<span data-ttu-id="d4fda-145">Ein IPv4-Literale besteht aus vier Dezimalzahlen im Bereich 0-255, z. b. 192.168.0.0.</span><span class="sxs-lookup"><span data-stu-id="d4fda-145">An IPv4 literal consists of four dotted decimal numbers, each in the range 0-255, such as 192.168.0.0.</span></span>

</dd> <dt>

<span data-ttu-id="d4fda-146"><span id="IPv6_Literal_String"></span><span id="ipv6_literal_string"></span><span id="IPV6_LITERAL_STRING"></span>IPv6-Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="d4fda-146"><span id="IPv6_Literal_String"></span><span id="ipv6_literal_string"></span><span id="IPV6_LITERAL_STRING"></span>IPv6 Literal String</span></span>
</dt> <dd>

<span data-ttu-id="d4fda-147">Eine IPv6-Literalzeichenfolge wird in eckige Klammern eingeschlossen und enthält durch Doppelpunkte getrennte hexadezimal Zahlen. Beispiel: \[ :: 1 \] oder \[ 3FFE: FFFF:: 6ecb: 0101 \] .</span><span class="sxs-lookup"><span data-stu-id="d4fda-147">An IPv6 literal string is enclosed in square brackets and contains hex numbers separated by colons; for example: \[::1\] or \[3ffe:ffff::6ECB:0101\].</span></span>

</dd> </dl>

<span data-ttu-id="d4fda-148">IP-gebundene Host Bearbeiter mit schwacher Platzhalter sind für Anwendungen bestimmt, die den von Ihnen bereit gedienten Inhalt basierend auf der Route von eingehenden Anforderungen variieren.</span><span class="sxs-lookup"><span data-stu-id="d4fda-148">IP-bound weak-wildcard host specifiers are intended for applications that vary the content they serve based on the route taken by incoming requests.</span></span> <span data-ttu-id="d4fda-149">Verlassen Sie sich nicht auf IP-gebundene hostspezifizierer mit schwacher Platzhalter, um die Sicherheit zu erzwingen.</span><span class="sxs-lookup"><span data-stu-id="d4fda-149">Do not rely on IP-bound weak-wildcard host specifiers to enforce security.</span></span>

</dd> <dt>

<span data-ttu-id="d4fda-150"><span id="Weak_wildcard__asterisk_"></span><span id="weak_wildcard__asterisk_"></span><span id="WEAK_WILDCARD__ASTERISK_"></span>Schwacher Platzhalter (Sternchen)</span><span class="sxs-lookup"><span data-stu-id="d4fda-150"><span id="Weak_wildcard__asterisk_"></span><span id="weak_wildcard__asterisk_"></span><span id="WEAK_WILDCARD__ASTERISK_"></span>Weak wildcard (asterisk)</span></span>
</dt> <dd>

<span data-ttu-id="d4fda-151">Wenn ein Sternchen ( \* ) als Host Element angezeigt wird, fällt das URLPrefix in die schwache Platzhalter Kategorie.</span><span class="sxs-lookup"><span data-stu-id="d4fda-151">When an asterisk (\*) appears as the host element, then the UrlPrefix falls into the weak wildcard category.</span></span> <span data-ttu-id="d4fda-152">Diese Art von URLPrefix entspricht jedem Hostnamen, der dem angegebenen Schema, Port und relativeUri zugeordnet ist, die noch nicht mit einem starken Platzhalter-, expliziten oder IP-gebundenen URLPrefix für schwache Platzhalter übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="d4fda-152">This kind of UrlPrefix matches any host name associated with the specified scheme, port and relativeURI that has not already been matched by a strong-wildcard, explicit, or IP-bound weak-wildcard UrlPrefix.</span></span>

<span data-ttu-id="d4fda-153">Diese Host Spezifikation kann in einigen Fällen als Standard-Catch-All verwendet werden, oder Sie kann verwendet werden, um einen großen Abschnitt des URL-Namespace anzugeben, ohne viele URLPrefixes verwenden zu müssen.</span><span class="sxs-lookup"><span data-stu-id="d4fda-153">This host specification can be used as a default catch-all in some circumstances, or can be used to specify a large section of URL namespace without having to use many UrlPrefixes.</span></span>

</dd> </dl>

## <a name="urlprefix-conflict-detection-during-reservation-and-registration"></a><span data-ttu-id="d4fda-154">URLPrefix-Konflikterkennung während der Reservierung und Registrierung</span><span class="sxs-lookup"><span data-stu-id="d4fda-154">UrlPrefix Conflict Detection During Reservation and Registration</span></span>

<span data-ttu-id="d4fda-155">Zu Reservierungs-und Registrierungszwecken werden die vier unterschiedlichen Kategorien von URLPrefix separat behandelt, ohne dass Sie aufeinander verweisen.</span><span class="sxs-lookup"><span data-stu-id="d4fda-155">For reservation and registration purposes, the four different categories of UrlPrefix are treated separately, without reference to one another.</span></span> <span data-ttu-id="d4fda-156">In Konflikt stehende URLPrefixes können registriert werden, solange Sie sich in verschiedenen Kategorien befinden.</span><span class="sxs-lookup"><span data-stu-id="d4fda-156">It is possible to register conflicting UrlPrefixes as long as they are in different categories.</span></span> <span data-ttu-id="d4fda-157">Nur innerhalb derselben Kategorie führt ein Konflikt dazu, dass ein Reservierungs Versuch fehlschlägt.</span><span class="sxs-lookup"><span data-stu-id="d4fda-157">Only within the same category does a conflict cause a reservation attempt to fail.</span></span>

<span data-ttu-id="d4fda-158">Beispielsweise wäre es möglich, sowohl das explizite URLPrefix `https://www.adatum.com:80/vroot/` als auch das in Konflikt stehende starke Platzhalter-URLPrefix zu reservieren `https://+:80/vroot/` , da Sie zu unterschiedlichen Kategorien gehören.</span><span class="sxs-lookup"><span data-stu-id="d4fda-158">For example, it would be possible to reserve both the explicit UrlPrefix `https://www.adatum.com:80/vroot/` and the conflicting strong wildcard UrlPrefix `https://+:80/vroot/`, since they belong to different categories.</span></span> <span data-ttu-id="d4fda-159">Bei einem nachfolgenden Versuch, einen anderen Benutzer zu reservieren, tritt jedoch ein Fehler auf, https://+:80/vroot/ weil er mit einer vorhandenen Reservierung in seiner eigenen Kategorie in Konflikt steht.</span><span class="sxs-lookup"><span data-stu-id="d4fda-159">However, a subsequent attempt to reserve https://+:80/vroot/ to a different user would fail because it would conflict with an existing reservation in its own category.</span></span>

## <a name="routing-behavior"></a><span data-ttu-id="d4fda-160">Routing Verhalten</span><span class="sxs-lookup"><span data-stu-id="d4fda-160">Routing Behavior</span></span>

<span data-ttu-id="d4fda-161">Wenn Sie eine eingehende HTTP-Anforderung weiterleiten, beginnt die HTTP-Server-API mit der Kategorie "starker Platzhalter" und vergleicht die eingehende URL mit den registrierten und reservierten URLPrefixes in dieser Kategorie.</span><span class="sxs-lookup"><span data-stu-id="d4fda-161">When routing an incoming HTTP request, the HTTP Server API starts with the strong wildcard category and compares the incoming URL with both registered and reserved UrlPrefixes in that category.</span></span>

<span data-ttu-id="d4fda-162">Wenn die eingehende URL mit einer Reservierung, aber nicht mit einer Registrierung übereinstimmt, schlägt die HTTP-Server-API die Anforderung fehl.</span><span class="sxs-lookup"><span data-stu-id="d4fda-162">If the incoming URL matches a reservation but not a registration, the HTTP Server API fails the request.</span></span> <span data-ttu-id="d4fda-163">Dadurch wird verhindert, dass Registrierungen mit niedrigerer Priorität die nicht dafür vorgesehenen Anforderungen abrufen können.</span><span class="sxs-lookup"><span data-stu-id="d4fda-163">This prevents a lower-priority registrations from being able to pick up requests not intended for it.</span></span> <span data-ttu-id="d4fda-164">Der Status bei einem Fehler ist 400 ("Ungültige Anforderung") anstelle von "503" ("Dienst nicht verfügbar"), da eine 503-Rückgabe manchmal versehentlich von Lasten Ausgleichs Gateways interpretiert wird, was darauf hinweist, dass der Server überladen wurde.</span><span class="sxs-lookup"><span data-stu-id="d4fda-164">The status on failure is 400 ("Bad Request") rather than 503 ("Service not available"), because a 503 return is sometimes mistakenly interpreted by load-balancing gateways as indicating that the server was overloaded.</span></span>

<span data-ttu-id="d4fda-165">Wenn eine übereinstimmende Registrierung in der Kategorie gefunden wird, wird die Anforderung an die Anforderungs Warteschlange weitergeleitet, die mit dieser Registrierung verknüpft ist.</span><span class="sxs-lookup"><span data-stu-id="d4fda-165">If a matching registration is found within the category, the request is routed to the request queue associated with that registration.</span></span> <span data-ttu-id="d4fda-166">Die Anforderung wird immer an die Warteschlange weitergeleitet, die dem längsten übereinstimmenden URLPrefix innerhalb einer Kategorie zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="d4fda-166">The request is always routed to the queue associated with the longest matching UrlPrefix within a category.</span></span>

<span data-ttu-id="d4fda-167">Wenn in der Kategorie keine Übereinstimmung gefunden wird, fährt die HTTP-Server-API mit der expliziten Kategorie fort und wiederholt dieselbe Prozedur.</span><span class="sxs-lookup"><span data-stu-id="d4fda-167">If no match is found in the category, then the HTTP Server API proceeds to the explicit category and repeats the same procedure.</span></span> <span data-ttu-id="d4fda-168">Zusammenfassend gilt: die Reihenfolge, in der die Kategorien überprüft werden, lautet wie folgt:</span><span class="sxs-lookup"><span data-stu-id="d4fda-168">To summarize, the order in which the categories are examined is as follows:</span></span>

1.  <span data-ttu-id="d4fda-169">Starker Platzhalter</span><span class="sxs-lookup"><span data-stu-id="d4fda-169">Strong wildcard</span></span>
2.  <span data-ttu-id="d4fda-170">Explizit</span><span class="sxs-lookup"><span data-stu-id="d4fda-170">Explicit</span></span>
3.  <span data-ttu-id="d4fda-171">IP-Bound schwache Platzhalter</span><span class="sxs-lookup"><span data-stu-id="d4fda-171">IP-Bound weak wildcard</span></span>
4.  <span data-ttu-id="d4fda-172">Schwacher Platzhalter</span><span class="sxs-lookup"><span data-stu-id="d4fda-172">Weak wildcard</span></span>

<span data-ttu-id="d4fda-173">Wenn keine Entsprechung in einer der Kategorien gefunden wird, sendet die HTTP-Server-API eine Antwort mit dem Statuscode 400, um anzugeben, dass die Anforderung nicht weitergeleitet werden kann.</span><span class="sxs-lookup"><span data-stu-id="d4fda-173">If no match is found in any of the categories, the HTTP Server API sends a response with a status code of 400 to indicate that the request cannot be routed.</span></span>

## <a name="longest-match-rule"></a><span data-ttu-id="d4fda-174">Längste Übereinstimmungs Regel</span><span class="sxs-lookup"><span data-stu-id="d4fda-174">Longest Match Rule</span></span>

<span data-ttu-id="d4fda-175">Innerhalb jeder URLPrefix-Kategorie leitet die HTTP-Server-API eine Anforderung an die Warteschlange weiter, die dem längsten übereinstimmenden URLPrefix zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="d4fda-175">Within each UrlPrefix category, HTTP Server API routes a request to the queue associated with the longest matching UrlPrefix.</span></span> <span data-ttu-id="d4fda-176">Nehmen wir beispielsweise an, dass die beiden folgenden URLPrefixes für verschiedene Warteschlangen registriert sind:</span><span class="sxs-lookup"><span data-stu-id="d4fda-176">For example, suppose the following two UrlPrefixes are registered to different queues:</span></span>

- `Queue1 https://www.adatum.com:80/`
- `Queue2 https://www.adatum.com:80/dir/sna/`

<span data-ttu-id="d4fda-177">Die HTTP-Server-API leitet eine Anforderung für `https://www.adatum.com:80/default.htm` an "queue1" und eine Anforderung `https://www.adatum.com:80/dir/sna/snadefault.htm` an Queue2.</span><span class="sxs-lookup"><span data-stu-id="d4fda-177">The HTTP Server API routes a request for `https://www.adatum.com:80/default.htm` to Queue1, and a request for `https://www.adatum.com:80/dir/sna/snadefault.htm` to Queue2.</span></span> <span data-ttu-id="d4fda-178">Die Anforderung `https://www.adatum.com:80/dir/app.htm` wird an "queue1" weitergeleitet, da die längste Vervollständigung mit dem `https://www.adatum.com:80/` URLPrefix, nicht mit dem `https://www.adatum.com:80/dir/sna` URLPrefix-Wert ist.</span><span class="sxs-lookup"><span data-stu-id="d4fda-178">It routes a request for `https://www.adatum.com:80/dir/app.htm` to Queue1 because the longest complete match is with the `https://www.adatum.com:80/` UrlPrefix, not with the `https://www.adatum.com:80/dir/sna` UrlPrefix.</span></span>

 

 




