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
# <a name="searching-for-groups-by-scope-or-type-in-a-domain"></a><span data-ttu-id="3b81f-104">Suchen nach Gruppen nach Gültigkeitsbereich oder Typ in einer Domäne</span><span class="sxs-lookup"><span data-stu-id="3b81f-104">Searching for Groups by Scope or Type in a Domain</span></span>

<span data-ttu-id="3b81f-105">In Windows 2000-Domänen gibt es eine einzelne Klasse namens " [**Group**](/windows/desktop/ADSchema/c-group) " für alle Gruppen Bereiche (lokale Domäne, Global, universell) und Typen (Sicherheit, Verteilung).</span><span class="sxs-lookup"><span data-stu-id="3b81f-105">In Windows 2000 domains, there is single class called [**group**](/windows/desktop/ADSchema/c-group) for all group scopes (Domain Local, Global, Universal) and types (security, distribution).</span></span> <span data-ttu-id="3b81f-106">Das [**GroupType**](/windows/desktop/ADSchema/a-grouptype) -Attribut des Group-Objekts gibt den Gruppentyp und den Gültigkeitsbereich an.</span><span class="sxs-lookup"><span data-stu-id="3b81f-106">The [**groupType**](/windows/desktop/ADSchema/a-grouptype) attribute of the group object specifies the group type and scope.</span></span>

<span data-ttu-id="3b81f-107">Wenn Sie den Typ oder den Bereich für die Suche nach Gruppen in Windows 2000-Domänen verwenden möchten, verwenden Sie einen Filter mit einer abgleichsregel für das [**GroupType**](/windows/desktop/ADSchema/a-grouptype) -Attribut.</span><span class="sxs-lookup"><span data-stu-id="3b81f-107">To use type or scope to search for groups on Windows 2000 domains, use a filter that contains a matching rule for the [**groupType**](/windows/desktop/ADSchema/a-grouptype) attribute.</span></span> <span data-ttu-id="3b81f-108">Weitere Informationen zu abgleichsregeln finden Sie unter [Such Filter Syntax](/windows/desktop/ADSI/search-filter-syntax).</span><span class="sxs-lookup"><span data-stu-id="3b81f-108">For more information about matching rules, see [Search Filter Syntax](/windows/desktop/ADSI/search-filter-syntax).</span></span>

<span data-ttu-id="3b81f-109">Weitere Informationen und ein Codebeispiel, das zeigt, wie Sie Gruppen in einer Domäne suchen, finden Sie unter [Beispielcode für die Suche nach Gruppen in einer Domäne](example-code-for-performing-a-query-in-a-domain.md).</span><span class="sxs-lookup"><span data-stu-id="3b81f-109">For more information and a code example that shows how to search for groups in a domain, see [Example Code for Searching for Groups in a Domain](example-code-for-performing-a-query-in-a-domain.md).</span></span>

## <a name="example-ldap-query-strings"></a><span data-ttu-id="3b81f-110">LDAP-Beispiel Abfrage Zeichenfolgen</span><span class="sxs-lookup"><span data-stu-id="3b81f-110">Example LDAP Query Strings</span></span>

<span data-ttu-id="3b81f-111">Die folgenden Beispiele für Abfrage Zeichenfolgen veranschaulichen, wie eine LDAP-Abfrage Zeichenfolge zum Suchen oder Filtern spezifischer Gruppen Typen erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="3b81f-111">The following query string examples show how to construct an LDAP query string used to search for or filter specific group types.</span></span>

<span data-ttu-id="3b81f-112">Mit der folgenden Abfrage Zeichenfolge wird nach Sicherheitsgruppen gesucht.</span><span class="sxs-lookup"><span data-stu-id="3b81f-112">The following query string will search for security groups.</span></span> <span data-ttu-id="3b81f-113">In diesem Beispiel wird "-2147483648" als Dezimaltrennzeichen für das **AD \_ Group \_ Type \_ Security \_ aktivierte** Flag verwendet.</span><span class="sxs-lookup"><span data-stu-id="3b81f-113">This example uses "-2147483648" as the decimal equivalent of the **ADS\_GROUP\_TYPE\_SECURITY\_ENABLED** flag.</span></span>


```C++
(&(objectCategory=group)(groupType:1.2.840.113556.1.4.803:=-2147483648))
```



<span data-ttu-id="3b81f-114">Mit der folgenden Abfrage Zeichenfolge wird nach universellen Verteiler Gruppen gesucht. Das heißt, dass Gruppen, die den **ADS- \_ \_ Gruppentyp \_ Universal \_ Group** -Flag enthalten und nicht das Flag **AD \_ Group \_ Type \_ Security \_ aktiviertes** Flag enthalten.</span><span class="sxs-lookup"><span data-stu-id="3b81f-114">The following query string will search for universal distribution groups; that is, groups that contain the **ADS\_GROUP\_TYPE\_UNIVERSAL\_GROUP** flag and do not contain the **ADS\_GROUP\_TYPE\_SECURITY\_ENABLED** flag.</span></span> <span data-ttu-id="3b81f-115">In diesem Beispiel wird "8" als Dezimaltrennzeichen der " **ADS \_ Group \_ Type \_ Universal \_ Group** " und "-2147483648" als Dezimaltrennzeichen für das Flag " **AD \_ Group \_ Type \_ Security \_ aktivierte** " verwendet.</span><span class="sxs-lookup"><span data-stu-id="3b81f-115">This example uses "8" as the decimal equivalent of **ADS\_GROUP\_TYPE\_UNIVERSAL\_GROUP** and "-2147483648" as the decimal equivalent of the **ADS\_GROUP\_TYPE\_SECURITY\_ENABLED** flag.</span></span>


```C++
(&(objectCategory=group)((&(groupType:1.2.840.113556.1.4.803:=8)(!(groupType:1.2.840.113556.1.4.803:=-2147483648)))))
```



 

 