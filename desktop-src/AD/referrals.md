---
title: Verweise (AD DS)
description: Active Directory Domain Services die Verweis Daten in CrossRef-Objekten verwalten, die im Partitions Container (crossrebcontainer) im Konfigurations Container gespeichert sind.
ms.assetid: e4d6cc8a-9c2c-4e0f-acca-e9ecdd5e879b
ms.tgt_platform: multiple
keywords:
- Verweise anzeigen
- Active Directory, Verweise
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f63c87fb0248d85ab20191296f9659eb58e460f6
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/17/2020
ms.locfileid: "106341918"
---
# <a name="referrals-ad-ds"></a>Verweise (AD DS)

Active Directory Domain Services die Verweis Daten in [**CrossRef**](/windows/desktop/ADSchema/c-crossref) -Objekten verwalten, die im Partitions Container ([**crossrebcontainer**](/windows/desktop/ADSchema/c-crossrefcontainer)) im Konfigurations Container gespeichert sind. Im Thema [entscheiden, wo die Suche durch](where-to-search.md) geführt werden soll, werden Verweise im Kontext einer Domäne innerhalb einer Domänen Struktur und der Generierung von Verweisen auf untergeordnete Domänen in einer Unterstruktur Suche erörtert.

Active Directory Domain Services erstellen und Verwalten von [**CrossRef**](/windows/desktop/ADSchema/c-crossref) -Objekten für alle Domänen in der Gesamtstruktur. Außerdem sind **CrossRef** -Objekte für die Konfigurations-und Schema Container vorhanden. Diese **CrossRef** -Objekte werden verwendet, um Verweise als Antwort auf Abfragen zu generieren, die Daten zu Objekten anfordern, die in der Gesamtstruktur vorhanden sind, aber nicht auf dem Verzeichnisserver enthalten sind, der die Anforderung verarbeitet. Diese werden als *interne Querverweise* bezeichnet, da Sie auf Domänen, Schema und Konfigurations Container innerhalb der Gesamtstruktur verweisen.

Wenn die verweisverfolgung nicht aktiviert ist und eine Unterstruktur Suche durchgeführt wird, gibt die Suche alle Objekte innerhalb der angegebenen Domäne zurück, die den Suchkriterien entsprechen. Bei der Suche werden auch Verweise auf alle untergeordneten Domänen zurückgegeben, bei denen es sich um direkte Nachfolger der Verzeichnisserver Domäne handelt. Der Client muss die Verweise auflösen, indem er an den Pfad gebunden wird, der durch den Verweis angegeben wird, und eine andere Abfrage übermittelt.

Wenn die Weiterleitungs Verfolgung aktiviert ist und eine Unterstruktur Suche durchgeführt wird, versucht die zugrunde liegende LDAP-API automatisch, eine Bindung an alle Verweise herzustellen und die Suchergebnisse dem Resultset hinzuzufügen. In den meisten Fällen ist die Verweis Verfolgung für den Aufrufer transparent. Wenn der Verweis auf ein Objekt in einer anderen Domäne oder Gesamtstruktur erfolgt, versucht die zugrunde liegende LDAP-API, die aktuellen Anmelde Informationen zum Binden an das Ziel der Referenz zu verwenden. Wenn dies erfolgreich ist, wird die Verweis Verfolgung transparent. Wenn dies nicht erfolgreich ist, werden der Verweis und der Verweis Fehlercode zurückgegeben.

Weitere Informationen zum Festlegen der bevorzugte Such Einstellung für die Verweis Verfolgung finden Sie unter [Angeben anderer Suchoptionen](specifying-other-search-options.md).

Zusätzlich zu den Eigenschaften [**dnsRoot**](/windows/desktop/ADSchema/a-dnsroot) (DNS-Name der Domäne) und [**NCName**](/windows/desktop/ADSchema/a-ncname) (Distinguished Name für die Domäne) enthält das [**CrossRef**](/windows/desktop/ADSchema/c-crossref) -Objekt auch den **NetbiosName** (NetBIOS-Namen der Domäne) und **trustparent** (Distinguished Name für das **CrossRef** -Objekt, das die direkte übergeordnete Domäne der Domäne darstellt).

Active Directory Domain Services können auch *externe Querverweise* aufweisen, die auf Objekte außerhalb der Gesamtstruktur verweisen. Externe Querverweise müssen explizit von einem Administrator hinzugefügt werden. Beachten Sie, dass der Zielserver des externen quer Verweises einen DNS-Stamm aufweisen muss. Das heißt, es muss RFC 2247 befolgt werden.

Ein externer Querverweis verweist auf ein Objekt in einer anderen Gesamtstruktur, sofern der Name in der Ziel Gesamtstruktur eindeutig ist. Beispielsweise können LDAP-Client Anwendungen, die von Ihrem Unternehmen verwendet werden, Vorgänge an Ihre Verzeichnisserver für fabrikam.com übermitteln. Sie erstellen ein [**CrossRef**](/windows/desktop/ADSchema/c-crossref) -Objekt für fabrikam.com. Anstatt den Fehler "Objekt nicht gefunden" zurückzugeben, können Ihre Verzeichnisserver einen Verweis auf ein Objekt in der Domäne "fabrikam.com" zurückgeben, und die Clients können den Verweis verfolgen. Wenn Sie z. b. ein-Objekt mit dem folgenden definierten Namen haben:


```C++
CN=SomeObject,OU=SomeOU,DC=Fabrikam,DC=Com
```



Sie können einen externen Querverweis für ein Objekt mit dem Namen "childoschsomeobject" hinzufügen.


```C++
CN=ChildOfSomeObject,CN=SomeObject,OU=SomeOU,DC=Fabrikam,DC=Com
```



Eine Unterstruktur Suche, die "SomeObject" enthält, gibt auch einen Verweis auf "childofsomeobject" zurück. Beachten Sie, dass ein LDAP-Server an der Adresse vorhanden sein muss, die durch den Verweis angegeben wird (eine der Eigenschaften für das [**CrossRef**](/windows/desktop/ADSchema/c-crossref) -Objekt), und dass dieser LDAP-Server den Namespace bedienen muss, der durch "childoatsomeobject" identifiziert wird.

Da [**CrossRef**](/windows/desktop/ADSchema/c-crossref) -Objekte im Konfigurations Container gespeichert werden, verfügt jeder Domänen Controller (DC) über eine Kopie aller **CrossRef** -Objekte. Daher enthält jeder Domänen Controllerdaten zu jeder Domäne in der Gesamtstruktur sowie ihren übergeordneten/untergeordneten Beziehungen. Dies ermöglicht es jedem Domänen Controller, Verweise auf eine beliebige Domäne in der Gesamtstruktur zu generieren, und Verweise auf die untergeordnete Domäne, das Schema oder die Konfigurations Container in einer Unterstruktur Suche.

Weitere Informationen über Verweise finden Sie unter:

-   [Wenn Verweise generiert werden](when-referrals-are-generated.md)
-   [Erstellen eines externen Verweises](creating-an-external-referral.md)

Weitere Informationen und ein Codebeispiel, das zeigt, wie Sie den Distinguished Name des Partitions Containers abrufen, finden Sie unter [Beispielcode für die Suche nach dem Partitions Container](example-code-for-locating-the-partitions-container.md).

 

 