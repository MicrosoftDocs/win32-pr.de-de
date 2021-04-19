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
# <a name="search-filter-syntax"></a>Such Filter Syntax

Durch Suchfilter können Sie Suchkriterien definieren und effizientere und effektive suchen bereitstellen.

ADSI unterstützt die LDAP-Suchfilter gemäß der Definition in RFC2254. Diese Suchfilter werden durch Unicode-Zeichen folgen dargestellt. In der folgenden Tabelle sind einige Beispiele für LDAP-Suchfilter aufgeführt.



| Suchfilter                                                               | BESCHREIBUNG                                                |
|-----------------------------------------------------------------------------|------------------------------------------------------------|
| "(objectClass = \* )"                                                          | Alle-Objekte.                                               |
| "(& (objectCategory = Person) (objectClass = User) (! ( CN = Andy))) "                  | Alle Benutzer Objekte, aber "Andy".                               |
| "(SN = SM \* )"                                                                 | Alle Objekte mit einem Nachnamen, der mit "SM" beginnt.          |
| "(& (objectCategory = Person) (objectClass = Contact) ( \| (SN = Smith) (SN = Johnson)))" | Alle Kontakte mit einem Nachnamen gleich "Smith" oder "Johnson". |



 

Diese Suchfilter verwenden eines der folgenden Formate.


```C++
<filter>=(<attribute><operator><value>)
```



oder


```C++
(<operator><filter1><filter2>)
```



Die ADSI-Suchfilter werden auf zweierlei Weise verwendet. Sie bilden einen Teil des LDAP-Dialekts zum Übermitteln von Abfragen über den OLE DB-Anbieter. Sie werden auch mit der [**idirector ysearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) -Schnittstelle verwendet.

## <a name="operators"></a>Operatoren

In der folgenden Tabelle werden häufig verwendete Suchfilter Operatoren aufgelistet.



| Logischer Operator | BESCHREIBUNG                                |
|------------------|--------------------------------------------|
| =                | Gleich                                   |
| ~=               | Ungefähr gleich                     |
| <=            | Lexikografisch kleiner als oder gleich    |
| >=            | Lexikografisch größer als oder gleich |
| &                | AND                                        |
| \|               | oder                                         |
| !                | NICHT                                        |



 

Zusätzlich zu den oben aufgeführten Operatoren definiert LDAP zwei übereinstimmende Regel Objekt-IDs (OIDs), die verwendet werden können, um bitweise Vergleiche numerischer Werte auszuführen. Abgleichsregeln haben die folgende Syntax.


```C++
<attribute name>:<matching rule OID>:=<value>
```



" &lt; Attribut Name &gt; " ist der **ldapDisplayName** des Attributs, " &lt; rule OID &gt; " ist die OID für die abgleichsregel und " &lt; Value &gt; " ist der Wert, der für den Vergleich verwendet werden soll. Beachten Sie, dass in dieser Zeichenfolge keine Leerzeichen verwendet werden können. " &lt; Value &gt; " muss eine Dezimalzahl sein. es kann sich nicht um eine hexadezimale Zahl oder um einen konstanten Namen handeln, wie z. b. die **\_ \_ \_ \_ aktivierte Gruppentyp Sicherheit**. Weitere Informationen zu den verfügbaren Active Directory Attributen finden Sie unter [alle Attribute](/windows/desktop/ADSchema/attributes-all).

In der folgenden Tabelle sind die von LDAP implementierten übereinstimmenden Regel-OIDs aufgeführt.



| Abgleichsregel OID       | Zeichen folgen Bezeichner (von ntldap. h)   | BESCHREIBUNG                                                                                                                                                                                   |
|-------------------------|-------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 1.2.840.113556.1.4.803  | **Bit der LDAP \_ -abgleichsregel \_ \_ \_**  | Eine Entsprechung wird nur gefunden, wenn alle Bits aus dem Attribut dem Wert entsprechen. Diese Regel entspricht einem bitweisen **and-** Operator.                                                                  |
| 1.2.840.113556.1.4.804  | **Bit der LDAP- \_ abgleichsregel \_ \_ \_**   | Eine Entsprechung wird gefunden, wenn Bits aus dem Attribut mit dem Wert verglichen werden. Diese Regel entspricht einem bitweisen **or** -Operator.                                                                        |
| 1.2.840.113556.1.4.1941 | **LDAP \_ - \_ abgleichsregel \_ in \_ Kette** | Diese Regel ist auf Filter beschränkt, die für den DN gelten. Dies ist ein spezieller "Erweiterter" Übereinstimmungs Operator, der die Kette der Herkunft in Objekten bis zum Stamm durchläuft, bis eine Entsprechung gefunden wird. |



 

Im folgenden Beispiel wird die Abfrage Zeichenfolge nach Gruppen Objekten durchsucht, für die das Flag für die **\_ \_ \_ Sicherheits \_ aktivierte ADS-Gruppentyp** Beachten Sie, dass der dezimale Wert der **ADS- \_ \_ Gruppentyp \_ Sicherheit \_ aktiviert** (0x80000000 = 2147483648) als Vergleichswert verwendet wird.


```C++
(&(objectCategory=group)(groupType:1.2.840.113556.1.4.803:=2147483648))
```



Die **LDAP-abgleichsregel \_ \_ \_ in \_ Kette** ist eine passende Regel-OID, die eine Methode zur Suche nach der Herkunft eines Objekts bereitstellen soll. Viele Anwendungen, die AD und AD LDS verwenden, arbeiten in der Regel mit hierarchischen Daten, die nach über-und untergeordneten Beziehungen geordnet sind. Bisher haben Anwendungen transitiv Gruppen Erweiterungen durchgeführt, um die Gruppenmitgliedschaft zu ermitteln, die zu viel Netzwerkbandbreite verbraucht hat. Anwendungen, die benötigt werden, um mehrere Roundtrips auszuführen, um herauszufinden, ob ein Objekt "in der Kette" verfällt, wenn eine Verknüpfung bis zum Ende durchlaufen wird.

Ein Beispiel für eine solche Abfrage soll überprüft werden, ob ein Benutzer "user1" Mitglied der Gruppe "group1" ist. Legen Sie die Basis auf den Benutzer-DN `(cn=user1, cn=users, dc=x)` und den Bereich auf fest `base` , und verwenden Sie die folgende Abfrage.


```C++
(memberof:1.2.840.113556.1.4.1941:=cn=Group1,OU=groupsOU,DC=x)
```



Um alle Gruppen zu suchen, in denen "user1" Mitglied ist, legen Sie die Basis auf den Gruppen Container-DN fest. `(OU=groupsOU, dc=x)` verwenden Sie z. b. und den Bereich auf `subtree` , und verwenden Sie den folgenden Filter.


```C++
(member:1.2.840.113556.1.4.1941:=cn=user1,cn=users,DC=x)
```



Beachten Sie, dass der Bereich bei Verwendung der **LDAP-abgleichsregel \_ \_ \_ in der \_ Kette** nicht begrenzt ist – es kann `base` sich um, oder handeln `one-level` `subtree` . Einige solcher Abfragen für Teil Strukturen können mehr Prozessor intensiv sein, z. b. das Nachverfolgen von Links mit einem hohen Lüfter. Das heißt, alle Gruppen, in denen ein Benutzer Mitglied ist. Durch ineffiziente suchen werden entsprechende Ereignisprotokoll Meldungen protokolliert, wie bei jedem anderen Abfragetyp.

## <a name="wildcards"></a>Platzhalter

Sie können einem LDAP-Suchfilter auch Platzhalter und Bedingungen hinzufügen. In den folgenden Beispielen werden Teil Zeichenfolgen gezeigt, die zum Durchsuchen des Verzeichnisses verwendet werden können.

Alle Einträge erhalten:


```C++
(objectClass=*)
```



Einträge mit "Bob" an einer beliebigen Stelle im allgemeinen Namen erhalten:


```C++
(cn=*bob*)
```



Einträge mit einem gemeinsamen Namen erhalten, der größer oder gleich "Bob" ist:


```C++
(cn>='bob')
```



Alle Benutzer mit einem e-Mail-Attribut erhalten:


```C++
(&(objectClass=user)(email=*))
```



Alle Benutzereinträge mit einem e-Mail-Attribut und einem Nachnamen mit dem Namen "Smith" erhalten:


```C++
(&(sn=smith)(objectClass=user)(email=*))
```



Hiermit werden alle Benutzereinträge mit einem allgemeinen Namen, der mit "Andy", "Steve" oder "Margaret" beginnt, angezeigt:


```C++
(&(objectClass=user)(| (cn=andy*)(cn=steve*)(cn=margaret*)))
```



Alle Einträge ohne e-Mail-Attribut erhalten:


```C++
(!(email=*))
```



Die formale Definition des Suchfilters lautet wie folgt (aus [RFC 2254](https://tools.ietf.org/html/rfc2254)):


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



Das Token &lt; attr &gt; ist eine Zeichenfolge, die einen attributeType darstellt. Der &lt; Tokenwert &gt; ist eine Zeichenfolge, die einen AttributeValue darstellt, dessen Format vom zugrunde liegenden Verzeichnisdienst definiert wird.

Wenn ein &lt; Wert &gt; das Sternchen ( \* ), das linke Klammern Zeichen (() oder das schließende Klammer Zeichen () enthalten muss, sollte dem Zeichen ein umgekehrter Schrägstrich () vorangestellt werden \\ .

## <a name="special-characters"></a>Sonderzeichen

Wenn eines der folgenden Sonderzeichen als Literale im Suchfilter angezeigt werden muss, müssen Sie durch die aufgeführte Escapesequenz ersetzt werden.



| ASCII-Zeichen | Escapesequenzersatz |
|-----------------|----------------------------|
| \*              | \\2a                       |
| (               | \\28                       |
| )               | \\27                       |
| \\              | \\5C                       |
| NUL             | \\4,00                       |
| /               | \\2F                       |



 

> [!Note]  
> In Fällen, in denen ein Multibyte-Zeichensatz verwendet wird, müssen die oben aufgeführten Escapesequenzen verwendet werden, wenn die Suche von ADO mit dem SQL-Dialekt ausgeführt wird.

 

Darüber hinaus können beliebige Binärdaten mithilfe der Escapesequenzsyntax dargestellt werden, indem jedes Byte der Binärdaten mit dem umgekehrten Schrägstrich ( \\ ) gefolgt von zwei hexadezimalen Ziffern codiert wird. Beispielsweise wird der vier-Byte-Wert 0x00000004 \\ \\ \\ \\ in einer Filter Zeichenfolge als 00 00 00 00.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[LDAP-Dialekt](ldap-dialect.md)
</dt> <dt>

[SQL-Dialekt](sql-dialect.md)
</dt> <dt>

[Suchen mit der idirector ysearch-Schnittstelle](searching-with-idirectorysearch.md)
</dt> <dt>

[Suchen mit ActiveX Data Objects](searching-with-activex-data-objects-ado.md)
</dt> <dt>

[Suchen mit OLE DB](searching-with-ole-db.md)
</dt> </dl>

 

 
