---
title: Suchfiltersyntax
description: Mit Suchfiltern können Sie Suchkriterien definieren und effizientere und effektivere Suchvorgänge bereitstellen.
ms.assetid: 3ce4709c-5ef7-4713-8fb7-b46ab284339f
ms.tgt_platform: multiple
keywords:
- Search Filter Syntax ADSI
- Abfragen, Suchfiltersyntax
ms.topic: article
ms.date: 09/25/2020
ms.openlocfilehash: 9ea6b347da1c840ef6bd1dd32bb32f96e7be86dfb93e6c1e71cdbb06bd52ba97
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120005490"
---
# <a name="search-filter-syntax"></a>Suchfiltersyntax

Mit Suchfiltern können Sie Suchkriterien definieren und effizientere und effektivere Suchvorgänge bereitstellen.

ADSI unterstützt die IN RFC2254 definierten LDAP-Suchfilter. Diese Suchfilter werden durch Unicode-Zeichenfolgen dargestellt. In der folgenden Tabelle sind einige Beispiele für LDAP-Suchfilter aufgeführt.



| Suchfilter                                                               | BESCHREIBUNG                                                |
|-----------------------------------------------------------------------------|------------------------------------------------------------|
| "(objectClass= \* )"                                                          | Alle -Objekte.                                               |
| "(&(objectCategory=person)(objectClass=user)(!( cn=andy)))                  | Alle Benutzerobjekte außer "andy".                               |
| "(sn=sm \* )"                                                                 | Alle Objekte mit einem Nachnamen, der mit "sm" beginnt.          |
| "(&(objectCategory=person)(objectClass=contact)( \| (sn=Smith)(sn=Smith)))" | Alle Kontakte mit einem Nachnamen gleich "Smith" oder "Smith". |



 

Diese Suchfilter verwenden eines der folgenden Formate.


```C++
<filter>=(<attribute><operator><value>)
```



oder


```C++
(<operator><filter1><filter2>)
```



Die ADSI-Suchfilter werden auf zwei Arten verwendet. Sie bilden einen Teil des LDAP-Dialekts zum Übermitteln von Abfragen über den OLE DB-Anbieter. Sie werden auch mit der [**IDirectorySearch-Schnittstelle**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) verwendet.

## <a name="operators"></a>Operatoren

In der folgenden Tabelle sind häufig verwendete Suchfilteroperatoren aufgeführt.



| Logischer Operator | BESCHREIBUNG                                |
|------------------|--------------------------------------------|
| =                | Gleich                                   |
| ~=               | Ungefähr gleich                     |
| <=            | Lexikografischer Kleiner als oder gleich    |
| >=            | Lexikografischer Größer als oder gleich |
| &                | AND                                        |
| \|               | oder                                         |
| !                | NICHT                                        |



 

Zusätzlich zu den oben genannten Operatoren definiert LDAP zwei übereinstimmende Regelobjektbezeichner (OIDs), die zum Durchführen bitweiser Vergleiche numerischer Werte verwendet werden können. Abgleichsregeln weisen die folgende Syntax auf.


```C++
<attribute name>:<matching rule OID>:=<value>
```



" &lt; Attributname &gt; " ist der **lDAPDisplayName** des Attributs, " &lt; Rule OID " ist die &gt; OID für die übereinstimmende Regel, und " &lt; value " ist der &gt; Wert, der für den Vergleich verwendet werden soll. Beachten Sie, dass in dieser Zeichenfolge keine Leerzeichen verwendet werden können. " &lt; value " muss eine &gt; Dezimalzahl sein. Es darf keine Hexadezimalzahl oder ein konstanter Name wie **ADS GROUP TYPE SECURITY \_ \_ \_ \_ ENABLED** sein. Weitere Informationen zu den verfügbaren Active Directory-Attributen finden Sie unter [Alle Attribute.](/windows/desktop/ADSchema/attributes-all)

In der folgenden Tabelle sind die von LDAP implementierten Übereinstimmenden Regel-OIDs aufgeführt.



| Abgleichsregel-OID       | Zeichenfolgenbezeichner (aus Ntldap.h)   | BESCHREIBUNG                                                                                                                                                                                   |
|-------------------------|-------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 1.2.840.113556.1.4.803  | **\_ \_ LDAP-ABGLEICHSREGELBIT \_ \_ UND**  | Eine Übereinstimmung wird nur gefunden, wenn alle Bits aus dem Attribut mit dem Wert übereinstimmen. Diese Regel entspricht einem  bitweisen AND-Operator.                                                                  |
| 1.2.840.113556.1.4.804  | **\_ \_ LDAP-ABGLEICHSREGELBIT \_ \_ ODER**   | Eine Übereinstimmung wird gefunden, wenn Bits aus dem Attribut mit dem Wert übereinstimmen. Diese Regel entspricht einem  bitweisen OR-Operator.                                                                        |
| 1.2.840.113556.1.4.1941 | **\_LDAP-ABGLEICHSREGEL \_ \_ IN \_ KETTE** | Diese Regel ist auf Filter beschränkt, die für den DN gelten. Dies ist ein spezieller "erweiterter" Übereinstimmungsoperator, der die Kette der Ketten in Objekten bis zum Stamm durchläuft, bis eine Übereinstimmung gefunden wird. |



 

Die folgende Beispielabfragezeichenfolge sucht nach Gruppenobjekten, für die das **ADS GROUP TYPE SECURITY \_ \_ \_ \_ ENABLED-Flag** festgelegt ist. Beachten Sie, dass der Dezimalwert **ADS GROUP TYPE SECURITY \_ \_ \_ \_ ENABLED** (0x80000000 = 2147483648) für den Vergleichswert verwendet wird.


```C++
(&(objectCategory=group)(groupType:1.2.840.113556.1.4.803:=2147483648))
```



Die **\_ LDAP-ABGLEICHSREGEL \_ \_ IN \_ CHAIN** ist eine Abgleichsregel-OID, die eine Methode zum Suchen der Empfindlichkeit eines Objekts bereitstellt. Viele Anwendungen, die AD und AD LDS verwenden, arbeiten in der Regel mit hierarchischen Daten, die nach Über-/Unterordnungsbeziehungen sortiert sind. Zuvor führten Anwendungen eine transitive Gruppenerweiterung durch, um die Gruppenmitgliedschaft zu herausfinden, die zu viel Netzwerkbandbreite beanspruchte. -Anwendungen mussten mehrere Roundtrips durchführen, um herauszufinden, ob ein Objekt "in der Kette" sinkt, wenn ein Link bis zum Ende durchlaufen wird.

Ein Beispiel für eine solche Abfrage ist eine Abfrage, die überprüft, ob ein Benutzer "user1" Mitglied der Gruppe "group1" ist. Sie würden die Basis auf den Benutzer-DN und den Bereich auf festlegen `(cn=user1, cn=users, dc=x)` und die folgende Abfrage `base` verwenden.


```C++
(memberof:1.2.840.113556.1.4.1941:=cn=Group1,OU=groupsOU,DC=x)
```



Um alle Gruppen zu finden, denen "user1" angehört, legen Sie die Basis auf den Gruppencontainer DN fest. verwenden Sie z. B. `(OU=groupsOU, dc=x)` und den Bereich auf , und verwenden Sie den folgenden `subtree` Filter.


```C++
(member:1.2.840.113556.1.4.1941:=cn=user1,cn=users,DC=x)
```



Beachten Sie, dass bei Verwendung der **\_ LDAP-ABGLEICHSREGEL \_ \_ IN \_ CHAIN** der Bereich nicht beschränkt ist– er kann `base` , oder `one-level` `subtree` sein. Einige solche Abfragen für Teilstrukturen sind möglicherweise prozessorintensiver, z. B. das Suchen nach Links mit einem hohen Auffächern; Das heißt, alle Gruppen aufzulisten, denen ein Benutzer angehört. Ineffiziente Suchvorgänge protokollieren entsprechende Ereignisprotokollmeldungen, wie bei jedem anderen Abfragetyp.

## <a name="wildcards"></a>Platzhalter

Sie können einem LDAP-Suchfilter auch Platzhalter und Bedingungen hinzufügen. Die folgenden Beispiele zeigen Teilzeichenfolgen, die zum Durchsuchen des Verzeichnisses verwendet werden können.

Abrufen aller Einträge:


```C++
(objectClass=*)
```



Abrufen von Einträgen, die "bob" im allgemeinen Namen enthalten:


```C++
(cn=*bob*)
```



Abrufen von Einträgen mit einem allgemeinen Namen, der größer oder gleich "bob" ist:


```C++
(cn>='bob')
```



Abrufen aller Benutzer mit einem E-Mail-Attribut:


```C++
(&(objectClass=user)(email=*))
```



Abrufen aller Benutzereinträge mit einem E-Mail-Attribut und einem Nachnamen gleich "smith":


```C++
(&(sn=smith)(objectClass=user)(email=*))
```



Abrufen aller Benutzereinträge mit einem allgemeinen Namen, der mit "andy", "steve" oder "soll" beginnt:


```C++
(&(objectClass=user)(| (cn=andy*)(cn=steve*)(cn=margaret*)))
```



Abrufen aller Einträge ohne E-Mail-Attribut:


```C++
(!(email=*))
```



Die formale Definition des Suchfilters lautet wie folgt (aus [RFC 2254):](https://tools.ietf.org/html/rfc2254)


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



Das Token &lt; attr &gt; ist eine Zeichenfolge, die einen AttributeType darstellt. Der &lt; Tokenwert &gt; ist eine Zeichenfolge, die einen AttributeValue darstellt, dessen Format vom zugrunde liegenden Verzeichnisdienst definiert wird.

Wenn ein &lt; Wert &gt; das Sternchen \* (), die linke Klammer (() oder die rechte Klammer ()) enthalten muss, sollte dem Zeichen der umgekehrte Schrägstrich () vorangestellt \\ werden.

## <a name="special-characters"></a>Sonderzeichen

Wenn eines der folgenden Sonderzeichen im Suchfilter als Literale angezeigt werden muss, müssen sie durch die aufgelistete Escapesequenz ersetzt werden.



| ASCII-Zeichen | Escapesequenz-Ersatz |
|-----------------|----------------------------|
| \*              | \\2a                       |
| (               | \\28                       |
| )               | \\29                       |
| \\              | \\5c                       |
| NUL             | \\00                       |
| /               | \\2f                       |



 

> [!Note]  
> In Fällen, in denen ein Multibyte-Zeichensatz verwendet wird, müssen die oben aufgeführten Escapesequenzen verwendet werden, wenn die Suche von ADO mit dem SQL Dialekt ausgeführt wird.

 

Darüber hinaus können beliebige binäre Daten mithilfe der Escapesequenzsyntax dargestellt werden, indem jedes Byte binärer Daten mit dem umgekehrten Schrägstrich ( \\ ) codiert wird, gefolgt von zwei Hexadezimalziffern. Beispielsweise wird der 4-Byte-Wert 0x00000004 \\ in einer Filterzeichenfolge als 00 \\ \\ 00 \\ 00 04 codiert.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[LDAP-Dialekt](ldap-dialect.md)
</dt> <dt>

[SQL Dialekt](sql-dialect.md)
</dt> <dt>

[Suchen mit der IDirectorySearch-Schnittstelle](searching-with-idirectorysearch.md)
</dt> <dt>

[Suchen mit ActiveX-Datenobjekten](searching-with-activex-data-objects-ado.md)
</dt> <dt>

[Suchen mit OLE DB](searching-with-ole-db.md)
</dt> </dl>

 

 
