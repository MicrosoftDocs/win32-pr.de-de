---
title: Suchen nach Gruppen nach Gültigkeitsbereich oder Typ in einer Domäne
description: In Windows 2000-Domänen gibt es eine einzelne Klasse namens "Group" für alle Gruppen Bereiche (lokale Domäne, Global, universell) und Typen (Sicherheit, Verteilung).
ms.assetid: e32629d9-aa62-4953-aa49-43af726b7deb
ms.tgt_platform: multiple
keywords:
- Suchen nach Gruppen nach Gültigkeitsbereich oder Typ in einer Domäne AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ee9aae5e2c7be7b9cba590f9bc80f0517bca918
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/17/2020
ms.locfileid: "103724425"
---
# <a name="searching-for-groups-by-scope-or-type-in-a-domain"></a>Suchen nach Gruppen nach Gültigkeitsbereich oder Typ in einer Domäne

In Windows 2000-Domänen gibt es eine einzelne Klasse namens " [**Group**](/windows/desktop/ADSchema/c-group) " für alle Gruppen Bereiche (lokale Domäne, Global, universell) und Typen (Sicherheit, Verteilung). Das [**GroupType**](/windows/desktop/ADSchema/a-grouptype) -Attribut des Group-Objekts gibt den Gruppentyp und den Gültigkeitsbereich an.

Wenn Sie den Typ oder den Bereich für die Suche nach Gruppen in Windows 2000-Domänen verwenden möchten, verwenden Sie einen Filter mit einer abgleichsregel für das [**GroupType**](/windows/desktop/ADSchema/a-grouptype) -Attribut. Weitere Informationen zu abgleichsregeln finden Sie unter [Such Filter Syntax](/windows/desktop/ADSI/search-filter-syntax).

Weitere Informationen und ein Codebeispiel, das zeigt, wie Sie Gruppen in einer Domäne suchen, finden Sie unter [Beispielcode für die Suche nach Gruppen in einer Domäne](example-code-for-performing-a-query-in-a-domain.md).

## <a name="example-ldap-query-strings"></a>LDAP-Beispiel Abfrage Zeichenfolgen

Die folgenden Beispiele für Abfrage Zeichenfolgen veranschaulichen, wie eine LDAP-Abfrage Zeichenfolge zum Suchen oder Filtern spezifischer Gruppen Typen erstellt wird.

Mit der folgenden Abfrage Zeichenfolge wird nach Sicherheitsgruppen gesucht. In diesem Beispiel wird "-2147483648" als Dezimaltrennzeichen für das **AD \_ Group \_ Type \_ Security \_ aktivierte** Flag verwendet.


```C++
(&(objectCategory=group)(groupType:1.2.840.113556.1.4.803:=-2147483648))
```



Mit der folgenden Abfrage Zeichenfolge wird nach universellen Verteiler Gruppen gesucht. Das heißt, dass Gruppen, die den **ADS- \_ \_ Gruppentyp \_ Universal \_ Group** -Flag enthalten und nicht das Flag **AD \_ Group \_ Type \_ Security \_ aktiviertes** Flag enthalten. In diesem Beispiel wird "8" als Dezimaltrennzeichen der " **ADS \_ Group \_ Type \_ Universal \_ Group** " und "-2147483648" als Dezimaltrennzeichen für das Flag " **AD \_ Group \_ Type \_ Security \_ aktivierte** " verwendet.


```C++
(&(objectCategory=group)((&(groupType:1.2.840.113556.1.4.803:=8)(!(groupType:1.2.840.113556.1.4.803:=-2147483648)))))
```



 

 