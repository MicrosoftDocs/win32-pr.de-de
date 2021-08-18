---
title: Suchen nach Gruppen nach Bereich oder Typ in einer Domäne
description: In Windows 2000 Domänen gibt es eine einzelne Klasse namens group für alle Gruppenbereiche (Domäne lokal, Global, Universell) und Typen (Sicherheit, Verteilung).
ms.assetid: e32629d9-aa62-4953-aa49-43af726b7deb
ms.tgt_platform: multiple
keywords:
- Suchen nach Gruppen nach Bereich oder Typ in einem Domänen-AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 84d424ce21912aa1e7fa7104099fc8359a5a1c80beeae1fc143aa0bd4aea71d0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119024948"
---
# <a name="searching-for-groups-by-scope-or-type-in-a-domain"></a>Suchen nach Gruppen nach Bereich oder Typ in einer Domäne

In Windows 2000 Domänen gibt es eine einzelne Klasse namens [**group**](/windows/desktop/ADSchema/c-group) für alle Gruppenbereiche (Domäne lokal, Global, Universell) und Typen (Sicherheit, Verteilung). Das [**groupType-Attribut**](/windows/desktop/ADSchema/a-grouptype) des Gruppenobjekts gibt den Gruppentyp und den Bereich an.

Verwenden Sie zum Suchen nach Gruppen in Windows 2000 Domänen einen Filter, der eine Abgleichsregel für das [**groupType-Attribut**](/windows/desktop/ADSchema/a-grouptype) enthält. Weitere Informationen zu Abgleichsregeln finden Sie unter [Suchfiltersyntax.](/windows/desktop/ADSI/search-filter-syntax)

Weitere Informationen und ein Codebeispiel, das zeigt, wie Nach Gruppen in einer Domäne gesucht wird, finden Sie unter [Beispielcode für die Suche nach Gruppen in einer Domäne.](example-code-for-performing-a-query-in-a-domain.md)

## <a name="example-ldap-query-strings"></a>Beispiel für LDAP-Abfragezeichenfolgen

Die folgenden Beispiele für Abfragezeichenfolgen zeigen, wie Sie eine LDAP-Abfragezeichenfolge erstellen, die zum Suchen oder Filtern bestimmter Gruppentypen verwendet wird.

Die folgende Abfragezeichenfolge sucht nach Sicherheitsgruppen. In diesem Beispiel wird "-2147483648" als Dezimaläquivalent des **ADS GROUP TYPE SECURITY \_ \_ \_ \_ ENABLED-Flags verwendet.**


```C++
(&(objectCategory=group)(groupType:1.2.840.113556.1.4.803:=-2147483648))
```



Die folgende Abfragezeichenfolge sucht nach universellen Verteilergruppen. Das heißt, Gruppen, die das **ADS GROUP TYPE UNIVERSAL \_ \_ \_ \_ GROUP-Flag** und nicht das **ADS GROUP TYPE SECURITY \_ \_ \_ \_ ENABLED-Flag** enthalten. In diesem Beispiel wird "8" als dezimales Äquivalent von **ADS GROUP TYPE UNIVERSAL \_ \_ \_ \_ GROUP** und "-2147483648" als Dezimaläquivalent des ADS GROUP TYPE SECURITY ENABLED-Flags **\_ \_ \_ \_ verwendet.**


```C++
(&(objectCategory=group)((&(groupType:1.2.840.113556.1.4.803:=8)(!(groupType:1.2.840.113556.1.4.803:=-2147483648)))))
```



 

 