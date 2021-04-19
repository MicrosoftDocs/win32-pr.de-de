---
title: Such Filter Syntax
description: Durch Suchfilter können Sie Suchkriterien definieren und effizientere und effektive suchen bereitstellen.
ms.assetid: 3ce4709c-5ef7-4713-8fb7-b46ab284339f
ms.tgt_platform: multiple
keywords:
- Such Filter Syntax ADSI
- Abfragen, Suchfilter Syntax
ms.topic: article
ms.date: 09/25/2020
ms.openlocfilehash: 28875bd49a3d1df7418c37706e58852066bbe08a
ms.sourcegitcommit: 4570ac533e129ff88b23f2c2b69e0140ead3a4a4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/26/2021
ms.locfileid: "106372523"
---
# <a name="search-filter-syntax"></a><span data-ttu-id="1c87c-105">Such Filter Syntax</span><span class="sxs-lookup"><span data-stu-id="1c87c-105">Search Filter Syntax</span></span>

<span data-ttu-id="1c87c-106">Durch Suchfilter können Sie Suchkriterien definieren und effizientere und effektive suchen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="1c87c-106">Search filters enable you to define search criteria and provide more efficient and effective searches.</span></span>

<span data-ttu-id="1c87c-107">ADSI unterstützt die LDAP-Suchfilter gemäß der Definition in RFC2254.</span><span class="sxs-lookup"><span data-stu-id="1c87c-107">ADSI supports the LDAP search filters as defined in RFC2254.</span></span> <span data-ttu-id="1c87c-108">Diese Suchfilter werden durch Unicode-Zeichen folgen dargestellt.</span><span class="sxs-lookup"><span data-stu-id="1c87c-108">These search filters are represented by Unicode strings.</span></span> <span data-ttu-id="1c87c-109">In der folgenden Tabelle sind einige Beispiele für LDAP-Suchfilter aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="1c87c-109">The following table lists some examples of LDAP search filters.</span></span>



| <span data-ttu-id="1c87c-110">Suchfilter</span><span class="sxs-lookup"><span data-stu-id="1c87c-110">Search filter</span></span>                                                               | <span data-ttu-id="1c87c-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1c87c-111">Description</span></span>                                                |
|-----------------------------------------------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="1c87c-112">"(objectClass = \* )"</span><span class="sxs-lookup"><span data-stu-id="1c87c-112">"(objectClass=\*)"</span></span>                                                          | <span data-ttu-id="1c87c-113">Alle-Objekte.</span><span class="sxs-lookup"><span data-stu-id="1c87c-113">All objects.</span></span>                                               |
| <span data-ttu-id="1c87c-114">"(& (objectCategory = Person) (objectClass = User) (! ( CN = Andy))) "</span><span class="sxs-lookup"><span data-stu-id="1c87c-114">"(&(objectCategory=person)(objectClass=user)(!(cn=andy)))"</span></span>                  | <span data-ttu-id="1c87c-115">Alle Benutzer Objekte, aber "Andy".</span><span class="sxs-lookup"><span data-stu-id="1c87c-115">All user objects but "andy".</span></span>                               |
| <span data-ttu-id="1c87c-116">"(SN = SM \* )"</span><span class="sxs-lookup"><span data-stu-id="1c87c-116">"(sn=sm\*)"</span></span>                                                                 | <span data-ttu-id="1c87c-117">Alle Objekte mit einem Nachnamen, der mit "SM" beginnt.</span><span class="sxs-lookup"><span data-stu-id="1c87c-117">All objects with a surname that starts with "sm".</span></span>          |
| <span data-ttu-id="1c87c-118">"(& (objectCategory = Person) (objectClass = Contact) ( \| (SN = Smith) (SN = Johnson)))"</span><span class="sxs-lookup"><span data-stu-id="1c87c-118">"(&(objectCategory=person)(objectClass=contact)(\|(sn=Smith)(sn=Johnson)))"</span></span> | <span data-ttu-id="1c87c-119">Alle Kontakte mit einem Nachnamen gleich "Smith" oder "Johnson".</span><span class="sxs-lookup"><span data-stu-id="1c87c-119">All contacts with a surname equal to "Smith" or "Johnson".</span></span> |



 

<span data-ttu-id="1c87c-120">Diese Suchfilter verwenden eines der folgenden Formate.</span><span class="sxs-lookup"><span data-stu-id="1c87c-120">These search filters use one of the following formats.</span></span>


```C++
<filter>=(<attribute><operator><value>)
```



<span data-ttu-id="1c87c-121">oder</span><span class="sxs-lookup"><span data-stu-id="1c87c-121">or</span></span>


```C++
(<operator><filter1><filter2>)
```



<span data-ttu-id="1c87c-122">Die ADSI-Suchfilter werden auf zweierlei Weise verwendet.</span><span class="sxs-lookup"><span data-stu-id="1c87c-122">The ADSI search filters are used in two ways.</span></span> <span data-ttu-id="1c87c-123">Sie bilden einen Teil des LDAP-Dialekts zum Übermitteln von Abfragen über den OLE DB-Anbieter.</span><span class="sxs-lookup"><span data-stu-id="1c87c-123">They form a part of the LDAP dialect for submitting queries through the OLE DB provider.</span></span> <span data-ttu-id="1c87c-124">Sie werden auch mit der [**idirector ysearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) -Schnittstelle verwendet.</span><span class="sxs-lookup"><span data-stu-id="1c87c-124">They are also used with the [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) interface.</span></span>

## <a name="operators"></a><span data-ttu-id="1c87c-125">Operatoren</span><span class="sxs-lookup"><span data-stu-id="1c87c-125">Operators</span></span>

<span data-ttu-id="1c87c-126">In der folgenden Tabelle werden häufig verwendete Suchfilter Operatoren aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="1c87c-126">The following table lists frequently used search filter operators.</span></span>



| <span data-ttu-id="1c87c-127">Logischer Operator</span><span class="sxs-lookup"><span data-stu-id="1c87c-127">Logical operator</span></span> | <span data-ttu-id="1c87c-128">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1c87c-128">Description</span></span>                                |
|------------------|--------------------------------------------|
| =                | <span data-ttu-id="1c87c-129">Gleich</span><span class="sxs-lookup"><span data-stu-id="1c87c-129">Equal to</span></span>                                   |
| ~=               | <span data-ttu-id="1c87c-130">Ungefähr gleich</span><span class="sxs-lookup"><span data-stu-id="1c87c-130">Approximately equal to</span></span>                     |
| <=            | <span data-ttu-id="1c87c-131">Lexikografisch kleiner als oder gleich</span><span class="sxs-lookup"><span data-stu-id="1c87c-131">Lexicographically less than or equal to</span></span>    |
| >=            | <span data-ttu-id="1c87c-132">Lexikografisch größer als oder gleich</span><span class="sxs-lookup"><span data-stu-id="1c87c-132">Lexicographically greater than or equal to</span></span> |
| &                | <span data-ttu-id="1c87c-133">AND</span><span class="sxs-lookup"><span data-stu-id="1c87c-133">AND</span></span>                                        |
| \|               | <span data-ttu-id="1c87c-134">oder</span><span class="sxs-lookup"><span data-stu-id="1c87c-134">OR</span></span>                                         |
| <span data-ttu-id="1c87c-135">!</span><span class="sxs-lookup"><span data-stu-id="1c87c-135">!</span></span>                | <span data-ttu-id="1c87c-136">NICHT</span><span class="sxs-lookup"><span data-stu-id="1c87c-136">NOT</span></span>                                        |



 

<span data-ttu-id="1c87c-137">Zusätzlich zu den oben aufgeführten Operatoren definiert LDAP zwei übereinstimmende Regel Objekt-IDs (OIDs), die verwendet werden können, um bitweise Vergleiche numerischer Werte auszuführen.</span><span class="sxs-lookup"><span data-stu-id="1c87c-137">In addition to the operators above, LDAP defines two matching rule object identifiers (OIDs) that can be used to perform bitwise comparisons of numeric values.</span></span> <span data-ttu-id="1c87c-138">Abgleichsregeln haben die folgende Syntax.</span><span class="sxs-lookup"><span data-stu-id="1c87c-138">Matching rules have the following syntax.</span></span>


```C++
<attribute name>:<matching rule OID>:=<value>
```



<span data-ttu-id="1c87c-139">" &lt; Attribut Name &gt; " ist der **ldapDisplayName** des Attributs, " &lt; rule OID &gt; " ist die OID für die abgleichsregel und " &lt; Value &gt; " ist der Wert, der für den Vergleich verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="1c87c-139">"&lt;attribute name&gt;" is the **lDAPDisplayName** of the attribute, "&lt;rule OID&gt;" is the OID for the matching rule, and "&lt;value&gt;" is the value to use for comparison.</span></span> <span data-ttu-id="1c87c-140">Beachten Sie, dass in dieser Zeichenfolge keine Leerzeichen verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="1c87c-140">Be aware that spaces cannot be used in this string.</span></span> <span data-ttu-id="1c87c-141">" &lt; Value &gt; " muss eine Dezimalzahl sein. es kann sich nicht um eine hexadezimale Zahl oder um einen konstanten Namen handeln, wie z. b. die **\_ \_ \_ \_ aktivierte Gruppentyp Sicherheit**.</span><span class="sxs-lookup"><span data-stu-id="1c87c-141">"&lt;value&gt;" must be a decimal number; it cannot be a hexadecimal number or a constant name such as **ADS\_GROUP\_TYPE\_SECURITY\_ENABLED**.</span></span> <span data-ttu-id="1c87c-142">Weitere Informationen zu den verfügbaren Active Directory Attributen finden Sie unter [alle Attribute](/windows/desktop/ADSchema/attributes-all).</span><span class="sxs-lookup"><span data-stu-id="1c87c-142">For more information about the available Active Directory attributes, see [All Attributes](/windows/desktop/ADSchema/attributes-all).</span></span>

<span data-ttu-id="1c87c-143">In der folgenden Tabelle sind die von LDAP implementierten übereinstimmenden Regel-OIDs aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="1c87c-143">The following table lists the matching rule OIDs implemented by LDAP.</span></span>



| <span data-ttu-id="1c87c-144">Abgleichsregel OID</span><span class="sxs-lookup"><span data-stu-id="1c87c-144">Matching rule OID</span></span>       | <span data-ttu-id="1c87c-145">Zeichen folgen Bezeichner (von ntldap. h)</span><span class="sxs-lookup"><span data-stu-id="1c87c-145">String identifier (from Ntldap.h)</span></span>   | <span data-ttu-id="1c87c-146">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1c87c-146">Description</span></span>                                                                                                                                                                                   |
|-------------------------|-------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1c87c-147">1.2.840.113556.1.4.803</span><span class="sxs-lookup"><span data-stu-id="1c87c-147">1.2.840.113556.1.4.803</span></span>  | <span data-ttu-id="1c87c-148">**Bit der LDAP \_ -abgleichsregel \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="1c87c-148">**LDAP\_MATCHING\_RULE\_BIT\_AND**</span></span>  | <span data-ttu-id="1c87c-149">Eine Entsprechung wird nur gefunden, wenn alle Bits aus dem Attribut dem Wert entsprechen.</span><span class="sxs-lookup"><span data-stu-id="1c87c-149">A match is found only if all bits from the attribute match the value.</span></span> <span data-ttu-id="1c87c-150">Diese Regel entspricht einem bitweisen **and-** Operator.</span><span class="sxs-lookup"><span data-stu-id="1c87c-150">This rule is equivalent to a bitwise **AND** operator.</span></span>                                                                  |
| <span data-ttu-id="1c87c-151">1.2.840.113556.1.4.804</span><span class="sxs-lookup"><span data-stu-id="1c87c-151">1.2.840.113556.1.4.804</span></span>  | <span data-ttu-id="1c87c-152">**Bit der LDAP- \_ abgleichsregel \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="1c87c-152">**LDAP\_MATCHING\_RULE\_BIT\_OR**</span></span>   | <span data-ttu-id="1c87c-153">Eine Entsprechung wird gefunden, wenn Bits aus dem Attribut mit dem Wert verglichen werden.</span><span class="sxs-lookup"><span data-stu-id="1c87c-153">A match is found if any bits from the attribute match the value.</span></span> <span data-ttu-id="1c87c-154">Diese Regel entspricht einem bitweisen **or** -Operator.</span><span class="sxs-lookup"><span data-stu-id="1c87c-154">This rule is equivalent to a bitwise **OR** operator.</span></span>                                                                        |
| <span data-ttu-id="1c87c-155">1.2.840.113556.1.4.1941</span><span class="sxs-lookup"><span data-stu-id="1c87c-155">1.2.840.113556.1.4.1941</span></span> | <span data-ttu-id="1c87c-156">**LDAP \_ - \_ abgleichsregel \_ in \_ Kette**</span><span class="sxs-lookup"><span data-stu-id="1c87c-156">**LDAP\_MATCHING\_RULE\_IN\_CHAIN**</span></span> | <span data-ttu-id="1c87c-157">Diese Regel ist auf Filter beschränkt, die für den DN gelten.</span><span class="sxs-lookup"><span data-stu-id="1c87c-157">This rule is limited to filters that apply to the DN.</span></span> <span data-ttu-id="1c87c-158">Dies ist ein spezieller "Erweiterter" Übereinstimmungs Operator, der die Kette der Herkunft in Objekten bis zum Stamm durchläuft, bis eine Entsprechung gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="1c87c-158">This is a special "extended" match operator that walks the chain of ancestry in objects all the way to the root until it finds a match.</span></span> |



 

<span data-ttu-id="1c87c-159">Im folgenden Beispiel wird die Abfrage Zeichenfolge nach Gruppen Objekten durchsucht, für die das Flag für die **\_ \_ \_ Sicherheits \_ aktivierte ADS-Gruppentyp**</span><span class="sxs-lookup"><span data-stu-id="1c87c-159">The following example query string searches for group objects that have the **ADS\_GROUP\_TYPE\_SECURITY\_ENABLED** flag set.</span></span> <span data-ttu-id="1c87c-160">Beachten Sie, dass der dezimale Wert der **ADS- \_ \_ Gruppentyp \_ Sicherheit \_ aktiviert** (0x80000000 = 2147483648) als Vergleichswert verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="1c87c-160">Be aware that the decimal value of **ADS\_GROUP\_TYPE\_SECURITY\_ENABLED** (0x80000000 = 2147483648) is used for the comparison value.</span></span>


```C++
(&(objectCategory=group)(groupType:1.2.840.113556.1.4.803:=2147483648))
```



<span data-ttu-id="1c87c-161">Die **LDAP-abgleichsregel \_ \_ \_ in \_ Kette** ist eine passende Regel-OID, die eine Methode zur Suche nach der Herkunft eines Objekts bereitstellen soll.</span><span class="sxs-lookup"><span data-stu-id="1c87c-161">The **LDAP\_MATCHING\_RULE\_IN\_CHAIN** is a matching rule OID that is designed to provide a method to look up the ancestry of an object.</span></span> <span data-ttu-id="1c87c-162">Viele Anwendungen, die AD und AD LDS verwenden, arbeiten in der Regel mit hierarchischen Daten, die nach über-und untergeordneten Beziehungen geordnet sind.</span><span class="sxs-lookup"><span data-stu-id="1c87c-162">Many applications using AD and AD LDS usually work with hierarchical data, which is ordered by parent-child relationships.</span></span> <span data-ttu-id="1c87c-163">Bisher haben Anwendungen transitiv Gruppen Erweiterungen durchgeführt, um die Gruppenmitgliedschaft zu ermitteln, die zu viel Netzwerkbandbreite verbraucht hat. Anwendungen, die benötigt werden, um mehrere Roundtrips auszuführen, um herauszufinden, ob ein Objekt "in der Kette" verfällt, wenn eine Verknüpfung bis zum Ende durchlaufen wird.</span><span class="sxs-lookup"><span data-stu-id="1c87c-163">Previously, applications performed transitive group expansion to figure out group membership, which used too much network bandwidth; applications needed to make multiple roundtrips to figure out if an object fell "in the chain" if a link is traversed through to the end.</span></span>

<span data-ttu-id="1c87c-164">Ein Beispiel für eine solche Abfrage soll überprüft werden, ob ein Benutzer "user1" Mitglied der Gruppe "group1" ist.</span><span class="sxs-lookup"><span data-stu-id="1c87c-164">An example of such a query is one designed to check if a user "user1" is a member of group "group1".</span></span> <span data-ttu-id="1c87c-165">Legen Sie die Basis auf den Benutzer-DN `(cn=user1, cn=users, dc=x)` und den Bereich auf fest `base` , und verwenden Sie die folgende Abfrage.</span><span class="sxs-lookup"><span data-stu-id="1c87c-165">You would set the base to the user DN `(cn=user1, cn=users, dc=x)` and the scope to `base`, and use the following query.</span></span>


```C++
(memberof:1.2.840.113556.1.4.1941:=cn=Group1,OU=groupsOU,DC=x)
```



<span data-ttu-id="1c87c-166">Um alle Gruppen zu suchen, in denen "user1" Mitglied ist, legen Sie die Basis auf den Gruppen Container-DN fest. `(OU=groupsOU, dc=x)` verwenden Sie z. b. und den Bereich auf `subtree` , und verwenden Sie den folgenden Filter.</span><span class="sxs-lookup"><span data-stu-id="1c87c-166">Similarly, to find all the groups that "user1" is a member of, set the base to the groups container DN; for example `(OU=groupsOU, dc=x)` and the scope to `subtree`, and use the following filter.</span></span>


```C++
(member:1.2.840.113556.1.4.1941:=cn=user1,cn=users,DC=x)
```



<span data-ttu-id="1c87c-167">Beachten Sie, dass der Bereich bei Verwendung der **LDAP-abgleichsregel \_ \_ \_ in der \_ Kette** nicht begrenzt ist – es kann `base` sich um, oder handeln `one-level` `subtree` .</span><span class="sxs-lookup"><span data-stu-id="1c87c-167">Note that when using **LDAP\_MATCHING\_RULE\_IN\_CHAIN**, scope is not limited—it can be `base`, `one-level`, or `subtree`.</span></span> <span data-ttu-id="1c87c-168">Einige solcher Abfragen für Teil Strukturen können mehr Prozessor intensiv sein, z. b. das Nachverfolgen von Links mit einem hohen Lüfter. Das heißt, alle Gruppen, in denen ein Benutzer Mitglied ist.</span><span class="sxs-lookup"><span data-stu-id="1c87c-168">Some such queries on subtrees may be more processor intensive, such as chasing links with a high fan-out; that is, listing all the groups that a user is a member of.</span></span> <span data-ttu-id="1c87c-169">Durch ineffiziente suchen werden entsprechende Ereignisprotokoll Meldungen protokolliert, wie bei jedem anderen Abfragetyp.</span><span class="sxs-lookup"><span data-stu-id="1c87c-169">Inefficient searches will log appropriate event log messages, as with any other type of query.</span></span>

## <a name="wildcards"></a><span data-ttu-id="1c87c-170">Platzhalter</span><span class="sxs-lookup"><span data-stu-id="1c87c-170">Wildcards</span></span>

<span data-ttu-id="1c87c-171">Sie können einem LDAP-Suchfilter auch Platzhalter und Bedingungen hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="1c87c-171">You can also add wildcards and conditions to an LDAP search filter.</span></span> <span data-ttu-id="1c87c-172">In den folgenden Beispielen werden Teil Zeichenfolgen gezeigt, die zum Durchsuchen des Verzeichnisses verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="1c87c-172">The following examples show substrings that can be used to search the directory.</span></span>

<span data-ttu-id="1c87c-173">Alle Einträge erhalten:</span><span class="sxs-lookup"><span data-stu-id="1c87c-173">Get all entries:</span></span>


```C++
(objectClass=*)
```



<span data-ttu-id="1c87c-174">Einträge mit "Bob" an einer beliebigen Stelle im allgemeinen Namen erhalten:</span><span class="sxs-lookup"><span data-stu-id="1c87c-174">Get entries containing "bob" somewhere in the common name:</span></span>


```C++
(cn=*bob*)
```



<span data-ttu-id="1c87c-175">Einträge mit einem gemeinsamen Namen erhalten, der größer oder gleich "Bob" ist:</span><span class="sxs-lookup"><span data-stu-id="1c87c-175">Get entries with a common name greater than or equal to "bob":</span></span>


```C++
(cn>='bob')
```



<span data-ttu-id="1c87c-176">Alle Benutzer mit einem e-Mail-Attribut erhalten:</span><span class="sxs-lookup"><span data-stu-id="1c87c-176">Get all users with an email attribute:</span></span>


```C++
(&(objectClass=user)(email=*))
```



<span data-ttu-id="1c87c-177">Alle Benutzereinträge mit einem e-Mail-Attribut und einem Nachnamen mit dem Namen "Smith" erhalten:</span><span class="sxs-lookup"><span data-stu-id="1c87c-177">Get all user entries with an email attribute and a surname equal to "smith":</span></span>


```C++
(&(sn=smith)(objectClass=user)(email=*))
```



<span data-ttu-id="1c87c-178">Hiermit werden alle Benutzereinträge mit einem allgemeinen Namen, der mit "Andy", "Steve" oder "Margaret" beginnt, angezeigt:</span><span class="sxs-lookup"><span data-stu-id="1c87c-178">Get all user entries with a common name that starts with "andy", "steve", or "margaret":</span></span>


```C++
(&(objectClass=user)(| (cn=andy*)(cn=steve*)(cn=margaret*)))
```



<span data-ttu-id="1c87c-179">Alle Einträge ohne e-Mail-Attribut erhalten:</span><span class="sxs-lookup"><span data-stu-id="1c87c-179">Get all entries without an email attribute:</span></span>


```C++
(!(email=*))
```



<span data-ttu-id="1c87c-180">Die formale Definition des Suchfilters lautet wie folgt (aus [RFC 2254](https://tools.ietf.org/html/rfc2254)):</span><span class="sxs-lookup"><span data-stu-id="1c87c-180">The formal definition of the search filter is as follows (from [RFC 2254](https://tools.ietf.org/html/rfc2254)):</span></span>


```C++
<filter> ::= '(' <filtercomp> ')'
<filtercomp> ::= <and> | <or> | <not> | <item>
<and> ::= '&' <filterlist>
<or> ::= '|' <filterlist>
<not> ::= '!' <filter>
<filterlist> ::= <filter> | <filter> <filterlist>
<item>::= <simple> | <present> | <substring>
<simple> ::= <attr> <filtertype> <value><filtertype> ::= <equal> | <approx> | <ge> | <le>
<equal> ::= '='
<approx> ::= '~='
<ge> ::= '>='
<le> ::= '<='
<present> ::= <attr> '=*'
<substring> ::= <attr> '=' <initial> <any> <final>
<initial> ::= NULL | <value><any> ::= '*' <starval>
<starval> ::= NULL | <value>'*' <starval>
<final> ::= NULL | <value>
```



<span data-ttu-id="1c87c-181">Das Token &lt; attr &gt; ist eine Zeichenfolge, die einen attributeType darstellt.</span><span class="sxs-lookup"><span data-stu-id="1c87c-181">The token &lt;attr&gt; is a string that represents an AttributeType.</span></span> <span data-ttu-id="1c87c-182">Der &lt; Tokenwert &gt; ist eine Zeichenfolge, die einen AttributeValue darstellt, dessen Format vom zugrunde liegenden Verzeichnisdienst definiert wird.</span><span class="sxs-lookup"><span data-stu-id="1c87c-182">The token &lt;value&gt; is a string that represents an AttributeValue whose format is defined by the underlying directory service.</span></span>

<span data-ttu-id="1c87c-183">Wenn ein &lt; Wert &gt; das Sternchen ( \* ), das linke Klammern Zeichen (() oder das schließende Klammer Zeichen () enthalten muss, sollte dem Zeichen ein umgekehrter Schrägstrich () vorangestellt werden \\ .</span><span class="sxs-lookup"><span data-stu-id="1c87c-183">If a &lt;value&gt; must contain the asterisk (\*), left parenthesis ((), or right parenthesis ()) character, the character should be preceded by the backslash escape character (\\).</span></span>

## <a name="special-characters"></a><span data-ttu-id="1c87c-184">Sonderzeichen</span><span class="sxs-lookup"><span data-stu-id="1c87c-184">Special Characters</span></span>

<span data-ttu-id="1c87c-185">Wenn eines der folgenden Sonderzeichen als Literale im Suchfilter angezeigt werden muss, müssen Sie durch die aufgeführte Escapesequenz ersetzt werden.</span><span class="sxs-lookup"><span data-stu-id="1c87c-185">If any of the following special characters must appear in the search filter as literals, they must be replaced by the listed escape sequence.</span></span>



| <span data-ttu-id="1c87c-186">ASCII-Zeichen</span><span class="sxs-lookup"><span data-stu-id="1c87c-186">ASCII character</span></span> | <span data-ttu-id="1c87c-187">Escapesequenzersatz</span><span class="sxs-lookup"><span data-stu-id="1c87c-187">Escape sequence substitute</span></span> |
|-----------------|----------------------------|
| \*              | <span data-ttu-id="1c87c-188">\\2a</span><span class="sxs-lookup"><span data-stu-id="1c87c-188">\\2a</span></span>                       |
| <span data-ttu-id="1c87c-189">(</span><span class="sxs-lookup"><span data-stu-id="1c87c-189">(</span></span>               | <span data-ttu-id="1c87c-190">\\28</span><span class="sxs-lookup"><span data-stu-id="1c87c-190">\\28</span></span>                       |
| <span data-ttu-id="1c87c-191">)</span><span class="sxs-lookup"><span data-stu-id="1c87c-191">)</span></span>               | <span data-ttu-id="1c87c-192">\\27</span><span class="sxs-lookup"><span data-stu-id="1c87c-192">\\29</span></span>                       |
| \\              | <span data-ttu-id="1c87c-193">\\5C</span><span class="sxs-lookup"><span data-stu-id="1c87c-193">\\5c</span></span>                       |
| <span data-ttu-id="1c87c-194">NUL</span><span class="sxs-lookup"><span data-stu-id="1c87c-194">NUL</span></span>             | <span data-ttu-id="1c87c-195">\\4,00</span><span class="sxs-lookup"><span data-stu-id="1c87c-195">\\00</span></span>                       |
| /               | <span data-ttu-id="1c87c-196">\\2F</span><span class="sxs-lookup"><span data-stu-id="1c87c-196">\\2f</span></span>                       |



 

> [!Note]  
> <span data-ttu-id="1c87c-197">In Fällen, in denen ein Multibyte-Zeichensatz verwendet wird, müssen die oben aufgeführten Escapesequenzen verwendet werden, wenn die Suche von ADO mit dem SQL-Dialekt ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1c87c-197">In cases where a MultiByte Character Set is being used, the escape sequences listed above must be used if the search is performed by ADO with the SQL dialect.</span></span>

 

<span data-ttu-id="1c87c-198">Darüber hinaus können beliebige Binärdaten mithilfe der Escapesequenzsyntax dargestellt werden, indem jedes Byte der Binärdaten mit dem umgekehrten Schrägstrich ( \\ ) gefolgt von zwei hexadezimalen Ziffern codiert wird.</span><span class="sxs-lookup"><span data-stu-id="1c87c-198">In addition, arbitrary binary data may be represented by using the escape sequence syntax by encoding each byte of binary data with the backslash (\\) followed by two hexadecimal digits.</span></span> <span data-ttu-id="1c87c-199">Beispielsweise wird der vier-Byte-Wert 0x00000004 \\ \\ \\ \\ in einer Filter Zeichenfolge als 00 00 00 00.</span><span class="sxs-lookup"><span data-stu-id="1c87c-199">For example, the four-byte value 0x00000004 is encoded as \\00\\00\\00\\04 in a filter string.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1c87c-200">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="1c87c-200">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1c87c-201">LDAP-Dialekt</span><span class="sxs-lookup"><span data-stu-id="1c87c-201">LDAP dialect</span></span>](ldap-dialect.md)
</dt> <dt>

[<span data-ttu-id="1c87c-202">SQL-Dialekt</span><span class="sxs-lookup"><span data-stu-id="1c87c-202">SQL dialect</span></span>](sql-dialect.md)
</dt> <dt>

[<span data-ttu-id="1c87c-203">Suchen mit der idirector ysearch-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="1c87c-203">Searching with the IDirectorySearch Interface</span></span>](searching-with-idirectorysearch.md)
</dt> <dt>

[<span data-ttu-id="1c87c-204">Suchen mit ActiveX Data Objects</span><span class="sxs-lookup"><span data-stu-id="1c87c-204">Searching with ActiveX Data Objects</span></span>](searching-with-activex-data-objects-ado.md)
</dt> <dt>

[<span data-ttu-id="1c87c-205">Suchen mit OLE DB</span><span class="sxs-lookup"><span data-stu-id="1c87c-205">Searching with OLE DB</span></span>](searching-with-ole-db.md)
</dt> </dl>

 

 
