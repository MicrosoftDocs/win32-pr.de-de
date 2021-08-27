---
title: Binden an den globalen Katalog
description: Der globale Katalog ist ein Namespace, der Verzeichnisdaten für alle Domänen in einer Gesamtstruktur enthält.
ms.assetid: c3c131c7-d9dd-4dbd-a909-abd0ffd9f375
ms.tgt_platform: multiple
keywords:
- Bindung an das globale Katalog-AD
- globales Katalog-AD, Bindung an
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4d094a0c07a40fa063b726d0ba1c5a15977873d
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122881642"
---
# <a name="binding-to-the-global-catalog"></a>Binden an den globalen Katalog

Der globale Katalog ist ein Namespace, der Verzeichnisdaten für alle Domänen in einer Gesamtstruktur enthält. Der globale Katalog enthält ein Teilreplikat jedes Domänenverzeichnisses. Sie enthält einen Eintrag für jedes Objekt in der Gesamtstruktur des Unternehmens, aber nicht alle Eigenschaften der einzelnen Objekte. Stattdessen enthält sie nur die Eigenschaften, die für die Aufnahme in den globalen Katalog angegeben sind.

Der globale Katalog wird auf bestimmten Servern im gesamten Unternehmen gespeichert. Nur Domänencontroller können als globale Katalogserver dienen. Administratoren geben mithilfe des Active Directory-Standort- und -Dienst-Managers an, ob ein angegebener Domänencontroller einen globalen Katalog enthält.

Verwenden Sie zum Binden an den globalen Katalog mit ADSI den Moniker "GC:".

Es gibt zwei Möglichkeiten, eine Bindung an den globalen Katalog zu erstellen, um eine Suche in einer Gesamtstruktur durchzuführen:

-   Binden Sie eine Bindung an das Unternehmensstammobjekt, um alle Domänen in der Gesamtstruktur zu durchsuchen.
-   Binden sie an ein bestimmtes Objekt, um dieses Objekt und seine unteren Objekte zu durchsuchen. Wenn Sie beispielsweise eine Bindung an eine Domäne mit zwei Darunter liegenden Domänen in einer Domänenstruktur in der Gesamtstruktur erstellen, können Sie diese drei Domänen durchsuchen. Beachten Sie, dass der Distinguished Name für das Objekt, an das gebunden werden soll, genau mit dem Distinguished Name identisch ist, der zum Binden an den LDAP:-Namespace verwendet wird. Denken Sie daran, dass "LDAP:" ein vollständiges Replikat einer einzelnen Domäne und "GC:" ein Teilreplikat aller Domänen in der Gesamtstruktur ist.

Wie beim Moniker "LDAP:" können Sie eine serverlose Bindung verwenden oder eine Bindung an einen bestimmten globalen Katalogserver herstellen. Wenn Sie in der aktuellen Gesamtstruktur suchen, verwenden Sie die serverlose Bindung. Wenn Sie jedoch in einer anderen Gesamtstruktur suchen, geben Sie entweder einen Domänennamen oder einen globalen Katalogserver für die Bindung an, wie in den folgenden Beispielen gezeigt.

Binden mithilfe des Domänennamens:

``` syntax
GC://fabrikam.com
```

Binden mithilfe des Servernamens:

``` syntax
GC://servername
```

Sie können auch eine Bindung an ein bestimmtes Objekt innerhalb des globalen Katalogs erstellen. Verwenden Sie das folgende Format, um eine Bindung an das Sales-Objekt in der Domäne fabrikam zu erstellen.

``` syntax
GC://fabrikam.com/DC=sales,DC=fabrikam,DC=com
```

Oder verwenden Sie das folgende Format, um eine Bindung an das Sales-Objekt auf dem Server herzustellen.

``` syntax
GC://servername.fabrikam.com/DC=sales,DC=fabrikam,DC=com
```

**So durchsuchen Sie die gesamte Gesamtstruktur**

1.  Binden sie an den Stamm des Globalen Katalognamespace.
2.  Enumerieren Sie den globalen Katalogcontainer. Der Globale Katalogcontainer enthält ein einzelnes Objekt, mit dem Sie die gesamte Gesamtstruktur durchsuchen können.
3.  Verwenden Sie das -Objekt im Container, um die Suche durchzuführen. Rufen Sie in C/C++ [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) auf, um einen [**IDirectorySearch-Zeiger**](/windows/desktop/api/iads/nn-iads-idirectorysearch) für das Objekt zu erhalten, damit Sie die **IDirectorySearch-Schnittstelle** zum Ausführen der Suche verwenden können. Verwenden Visual Basic in der ADO-Abfrage das von der -Enumeration zurückgegebene -Objekt.

Um die globalen Katalogserver an einem Standort aufzählen zu können, führen Sie mithilfe der folgenden Filterzeichenfolge eine LDAP-Unterstruktursuche nach "cn= &lt; yoursite &gt; ,cn=sites, <DN of the configurationNamingContext> " durch.

``` syntax
(&(objectCategory=nTDSDSA)(options:1.2.840.113556.1.4.803:=1))
```

Dieser Filter verwendet den **LDAP MATCHING RULE BIT \_ \_ \_ \_ AND** Matching Rule Operator (1.2.840.113556.1.4.803), um **nTDSDSA-Objekte** zu suchen, für die das low-order-Bit in der Bitmaske des **Optionsattributs** festgelegt ist. Das niedrige Bit, das der in Ntdsapi.h definierten **NTDSDSA \_ OPT IS \_ \_ GC-Konstante** entspricht, identifiziert das **nTDSDSA-Objekt** eines globalen Katalogservers. Weitere Informationen zu Abgleichsregeln finden Sie unter [Suchfiltersyntax](/windows/desktop/ADSI/search-filter-syntax).

Das übergeordnete Element des **nTDSDSA-Objekts** ist das Serverobjekt, und die **dNSHostName-Eigenschaft** des Serverobjekts ist der DNS-Name des globalen Katalogservers.

Sie können keine \# Konstanten wie **NTDSDSA \_ OPT IS \_ \_ GC** und **LDAP MATCHING RULE BIT \_ \_ \_ \_ AND** direkt in einer Suchfilterzeichenfolge verwenden. Sie können diese Konstanten jedoch als Argumente für eine Funktion wie [**swprintf \_ s**](/windows/win32/api/winuser/nf-winuser-wsprintfa) verwenden, um die konstanten Werte in eine Filterzeichenfolge zu einfügen.

Der globale Katalog stellt nicht die gesamte Struktur der Gesamtstruktur dar. Beispielsweise können Sie davon ausgehen, dass im folgenden Codebeispiel alle Domänen in der Gesamtstruktur und alle untergeordneten Objekte jeder Domäne aufzählt werden. Tatsächlich werden alle Domänen in der Gesamtstruktur aufzählt, aber keines der aufzählten Domänenobjekte enthält keines der aufzählten Domänenobjekte. Dies ist eine Einschränkung des globalen Katalogs.


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



Um dies zu korrigieren, ist es erforderlich, eine Bindung an jedes Domänenobjekt zu erstellen und dann die untergeordneten Objekte jeder Domäne aufzählen. Die richtige Technik wird im folgenden Codebeispiel gezeigt.


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



Weitere Informationen und Codebeispiele, die zeigen, wie eine gesamte Gesamtstruktur durchsucht wird, finden Sie unter Beispielcode für die Suche [nach einer Gesamtstruktur.](example-code-for-searching-a-forest.md)

 

 
