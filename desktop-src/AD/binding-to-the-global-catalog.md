---
title: Binden an den globalen Katalog
description: Der globale Katalog ist ein Namespace, der Verzeichnis Daten für alle Domänen in einer Gesamtstruktur enthält.
ms.assetid: c3c131c7-d9dd-4dbd-a909-abd0ffd9f375
ms.tgt_platform: multiple
keywords:
- Binden an den globalen Katalog AD
- globaler Katalog AD, Bindung an
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08fe40b944130f66617b0c111b361ca51cbef126
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/17/2020
ms.locfileid: "104038801"
---
# <a name="binding-to-the-global-catalog"></a>Binden an den globalen Katalog

Der globale Katalog ist ein Namespace, der Verzeichnis Daten für alle Domänen in einer Gesamtstruktur enthält. Der globale Katalog enthält ein partielles Replikat jedes Domänen Verzeichnisses. Sie enthält einen Eintrag für jedes Objekt in der Enterprise-Gesamtstruktur, enthält jedoch nicht alle Eigenschaften der einzelnen Objekte. Stattdessen enthält Sie nur die Eigenschaften, die für die Einbindung in den globalen Katalog angegeben werden.

Der globale Katalog wird auf bestimmten Servern im gesamten Unternehmen gespeichert. Nur Domänen Controller können als globale Katalogserver fungieren. Administratoren geben mithilfe der Active Directory Standorte und Dienste-Manager an, ob ein bestimmter Domänen Controller einen globalen Katalog enthält.

Verwenden Sie zum Binden an den globalen Katalog mit ADSI den "GC:"-Moniker.

Es gibt zwei Möglichkeiten, eine Bindung zum globalen Katalog herzustellen, um eine Suche in einer Gesamtstruktur durchzuführen:

-   Binden Sie an das Stamm Objekt des Unternehmens, um alle Domänen in der Gesamtstruktur zu durchsuchen.
-   Binden an ein bestimmtes Objekt, um das Objekt und seine untergeordneten Elemente zu durchsuchen. Wenn Sie z. b. eine Bindung an eine Domäne herstellen, die in einer Domänen Struktur in der Gesamtstruktur über zwei Domänen verfügt, können Sie diese drei Domänen durchsuchen. Beachten Sie, dass der Distinguished Name für das Objekt, an das die Bindung erfolgen soll, identisch mit dem Distinguished Name ist, der zum Binden an den "LDAP:"-Namespace verwendet wird. Beachten Sie, dass "LDAP:" ein vollständiges Replikat einer einzelnen Domäne ist und dass "GC:" ein partielles Replikat aller Domänen in der Gesamtstruktur ist.

Ebenso wie der "LDAP:"-Moniker können Sie eine Server lose Bindung oder eine Bindung an einen bestimmten globalen Katalogserver verwenden. Wenn Sie in der aktuellen Gesamtstruktur suchen, verwenden Sie die Server lose Bindung. Wenn Sie jedoch in einer anderen Gesamtstruktur suchen, geben Sie entweder einen Domänen Namen oder einen globalen Katalogserver an, an den die Bindung erfolgen soll, wie in den folgenden Beispielen gezeigt.

Binden mithilfe des Domänen Namens:

``` syntax
GC://fabrikam.com
```

Binden mit dem Servernamen:

``` syntax
GC://servername
```

Sie können auch eine Bindung an ein bestimmtes Objekt innerhalb des globalen Katalogs herstellen. Verwenden Sie das folgende Format, um eine Bindung zum Sales-Objekt in der Fabrikam-Domäne herzustellen.

``` syntax
GC://fabrikam.com/DC=sales,DC=fabrikam,DC=com
```

Oder verwenden Sie das folgende Format, um eine Bindung an das Sales-Objekt auf dem Server herzustellen.

``` syntax
GC://servername.fabrikam.com/DC=sales,DC=fabrikam,DC=com
```

**So durchsuchen Sie die gesamte Gesamtstruktur**

1.  Binden Sie an den Stamm des globalen Katalog-Namespace.
2.  Listet den globalen Katalog Container auf. Der Container für den globalen Katalog enthält ein einzelnes-Objekt, das Sie zum Durchsuchen der gesamten Gesamtstruktur verwenden können.
3.  Verwenden Sie das-Objekt im Container, um die Suche auszuführen. In C/C++ wird [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) aufgerufen, um einen [**IDirectorySearch**](/windows/desktop/api/iads/nn-iads-idirectorysearch) -Zeiger auf das Objekt zu erhalten, sodass Sie die **IDirectorySearch** -Schnittstelle zum Durchführen der Suche verwenden können. Verwenden Sie in Visual Basic das Objekt, das von der-Enumeration in der ADO-Abfrage zurückgegeben wird.

Um die globalen Katalogserver an einem Standort aufzulisten, führen Sie eine LDAP-Unterstruktur Suche von "CN = <yoursite> , CN = Sites <DN of the configurationNamingContext> " mithilfe der folgenden Filter Zeichenfolge aus.

``` syntax
(&(objectCategory=nTDSDSA)(options:1.2.840.113556.1.4.803:=1))
```

Dieser Filter verwendet das **LDAP \_ \_ -Vergleichs \_ Regel \_ -Bit und** den abgleichsregeloperator (1.2.840.113556.1.4.803), um **NTDSDSA** -Objekte zu suchen, für die das niedrige Bit in der Bitmaske des **options** -Attributs festgelegt ist. Das niedrig wertige Bit, das der in NTDSAPI. h definierten **\_ \_ \_ GC** -Konstante entspricht, identifiziert das **NTDSDSA** -Objekt eines globalen Katalog Servers. Weitere Informationen zu abgleichsregeln finden Sie unter [Such Filter Syntax](/windows/desktop/ADSI/search-filter-syntax).

Das übergeordnete Element des **NTDSDSA** -Objekts ist das Server Objekt, und die **dNSHostName** -Eigenschaft des Server Objekts ist der DNS-Name des globalen Katalog Servers.

Sie können keine \# Definieren von Konstanten wie **NTDSDSA \_ opt \_ is \_ GC** und **LDAP \_ Matching \_ rule \_ Bit \_ und** direkt in einer Suchfilter Zeichenfolge verwenden. Allerdings können Sie diese Konstanten als Argumente für eine Funktion wie z. [**b. "tauprintf \_ s**](/windows/win32/api/winuser/nf-winuser-wsprintfa) " verwenden, um die Konstanten Werte in eine Filter Zeichenfolge einzufügen.

Der globale Katalog stellt nicht die gesamte Gesamtstruktur Struktur dar. Beispielsweise können Sie davon ausgehen, dass im folgenden Codebeispiel alle Domänen in der Gesamtstruktur und alle untergeordneten Objekte der einzelnen Domänen aufgelistet werden. Tatsächlich werden in Wirklichkeit alle Domänen in der Gesamtstruktur aufgelistet, aber keines der aufgelisteten Domänen Objekte enthält untergeordnete Elemente. Dies ist eine Einschränkung des globalen Katalogs.


```VB
Dim oGC As IADs
Dim oDomain As IADs
Dim oChild As IADs

Set oGC = GetObject("GC:")
For Each oDomain In oGC
    ' Print the name of the domain.
    Debug.Print oDomain.Name
    
    ' Enumerate the child objects of the domain.
    For Each oChild In oDomain
        Debug.Print oChild.Name
    Next
Next
```



Um dies zu korrigieren, ist es erforderlich, eine Bindung an jedes Domänen Objekt herzustellen und dann die untergeordneten Objekte der einzelnen Domänen aufzuzählen. Das richtige Verfahren wird im folgenden Codebeispiel gezeigt.


```VB
Dim oGC As IADs
Dim oDomainEnum As IADs
Dim oDomainBind As IADs
Dim oChild As IADs

Set oGC = GetObject("GC:")
For Each oDomainEnum In oGC
    ' Print the name of the domain.
    Debug.Print oDomainEnum.Name
    
    ' Bind to the domain.
    Set oDomainBind = GetObject("LDAP://" + oDomainEnum.Name)
    
    ' Enumerate the child objects of the domain.
    For Each oChild In oDomainBind
        Debug.Print oChild.Name
    Next
Next
```



Weitere Informationen und Codebeispiele, die zeigen, wie eine ganze Gesamtstruktur durchsucht wird, finden Sie unter [Beispielcode zum Durchsuchen einer](example-code-for-searching-a-forest.md)Gesamtstruktur.

 

 