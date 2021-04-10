---
title: Wenn Verweise generiert werden
description: Ein Verweis ist die Methode, mit der ein Verzeichnisserver kommuniziert, dass er nicht die Daten enthält, die zum Durchführen einer Abfrage erforderlich sind, sondern einen Verweis auf einen Server enthält, der möglicherweise die erforderlichen Daten enthält.
ms.assetid: 2c11a52a-26e2-4a50-a0a3-5463a0852b27
ms.tgt_platform: multiple
keywords:
- Verweis Generierung Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06e47c1e172f3eaed34dad452aa46847980cd66f
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/17/2020
ms.locfileid: "103858115"
---
# <a name="when-referrals-are-generated"></a>Wenn Verweise generiert werden

Ein Verweis ist die Methode, mit der ein Verzeichnisserver kommuniziert, dass er nicht die Daten enthält, die zum Durchführen einer Abfrage erforderlich sind, sondern einen Verweis auf einen Server enthält, der möglicherweise die erforderlichen Daten enthält. Beachten Sie, dass Verweise nicht nur von Abfrage Anforderungen generiert werden.

Die folgenden Vorgänge können zu mindestens einem Verweis führen:

-   Bindung an einen Server, der das durch den angeforderten Distinguished Name angegebene Objekt nicht enthält, aber über Daten zu einem Server oder einer Domäne verfügt, der dieses Objekt enthalten kann. Bei ADSI kann dies vorkommen, wenn die Anwendung [**ADsGetObject**](/windows/desktop/api/adshlp/nf-adshlp-adsgetobject) oder [**ADsOpenObject**](/windows/desktop/api/adshlp/nf-adshlp-adsopenobject) aufruft, um an ein Objekt zu binden, das in einer anderen Domäne in der Gesamtstruktur (interner Verweis) vorhanden ist, oder in einem namens Kontext, der vollständig von der Gesamtstruktur getrennt ist (externer Verweis). Bei der LDAP-API kann dies beim Ausführen von Add-, Modify-, DELETE-oder Search-Vorgängen auftreten, die ein Objekt angeben, das sich in einer anderen Domäne in der Gesamtstruktur (interner Verweis) oder einem namens Kontext befindet, der vollständig von der Gesamtstruktur getrennt ist (externer Verweis).

    Wenn bei der Namensauflösung ein Objekt nicht lokal gefunden werden kann und keine **CrossRef** -Objekte für diesen Teil des Namespaces vorhanden sind, versucht der Domänen Controller, einen externen Verweis auf der Grundlage der Domänen Komponenten des Distinguished Name zu erstellen. Wenn eine Suche z. b. auf "CN = a, CN = b, DC = c, DC = d, DC = e" basiert, erstellt der Domänen Controller einen Verweis auf den LDAP-Server bei der DNS-Adresse "c. d. e".

    Alle Windows 2000-Domänen Controller (die nur DC = Naming für die oberen Komponenten unterstützen) erkennen einander, und es sind keine externen Querverweise erforderlich, damit ein Client von einer Gesamtstruktur an einen anderen gebunden werden kann. Wenn andere nicht-Windows 2000-Verzeichnisserver, wie z. b. ein Netscape-Server, DC = Naming verwendet und eine entsprechende SRV RR in DNS registriert ist, erhält Sie auch die Vorteile der automatischen Verweise. Andernfalls muss ein externes **CrossRef** -Objekt manuell hinzugefügt werden.

-   Durchführen einer Unterstruktur Suche in einer Domäne, die untergeordnete Domänen in der Gesamtstruktur oder untergeordneten externen Domänen, Schemas oder Konfigurations Containern enthält. Ein Verweis auf die untergeordnete Domäne, die externe Domäne, das Schema oder den Konfigurations Container wird erstellt. Wenn die Verweis Verfolgung aktiviert ist, ist der Verweis für den Aufrufer transparent.

 

 