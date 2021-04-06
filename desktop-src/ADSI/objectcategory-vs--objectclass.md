---
title: objectCategory im Vergleich zu objectClass
description: Das objectCategory-Attribut und das objectClass-Attribut können auf eine bestimmte Schema Klasse eines Verzeichnis Objekts verweisen.
ms.assetid: 66dadedb-61e4-4184-9b87-0fff036a94d9
ms.tgt_platform: multiple
keywords:
- objectCategory im Vergleich zu objectClass ADSI
- Attribute ASI, suchen nach objectCategory-und objectClass-Attributen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dbbb8c5fe737b7c81193a75cdae6b772db64e69c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036309"
---
# <a name="objectcategory-vs-objectclass"></a><span data-ttu-id="2c5a5-105">objectCategory im Vergleich zu objectClass</span><span class="sxs-lookup"><span data-stu-id="2c5a5-105">objectCategory vs. objectClass</span></span>

<span data-ttu-id="2c5a5-106">Das **objectCategory** -Attribut und das **objectClass** -Attribut können auf eine bestimmte Schema Klasse eines Verzeichnis Objekts verweisen.</span><span class="sxs-lookup"><span data-stu-id="2c5a5-106">Both the **objectCategory** and **objectClass** attributes can refer to a given schema class of a directory object.</span></span> <span data-ttu-id="2c5a5-107">Es gibt jedoch einen wichtigen Unterschied in der Semantik zwischen den beiden.</span><span class="sxs-lookup"><span data-stu-id="2c5a5-107">However, there is an important distinction in semantics between the two.</span></span> <span data-ttu-id="2c5a5-108">"objectClass = Joy" bezieht sich auf solche Verzeichnisobjekte, bei denen "Joy" eine beliebige Klasse in der Objektklassen Hierarchie darstellt.</span><span class="sxs-lookup"><span data-stu-id="2c5a5-108">"objectClass=joy" refers to such directory objects in which "joy" represents any class in the object class hierarchy.</span></span> <span data-ttu-id="2c5a5-109">"objectCategory = Joy" bezieht sich hingegen auf die Verzeichnisobjekte, in denen "Joy" eine bestimmte Klasse in der Objektklassen Hierarchie identifiziert.</span><span class="sxs-lookup"><span data-stu-id="2c5a5-109">"objectCategory=joy", on the other hand, refers to those directory objects in which "joy" identifies a specific class in the object class hierarchy.</span></span>

<span data-ttu-id="2c5a5-110">**objectClass** kann mehrere Werte annehmen, während **objectCategory** einen einzelnen Wert annimmt.</span><span class="sxs-lookup"><span data-stu-id="2c5a5-110">**objectClass** can take multiple values whereas **objectCategory** takes a single value.</span></span> <span data-ttu-id="2c5a5-111">Aus diesem Grund eignet sich **objectCategory** besser für die Typübereinstimmung von Objekten in einer Verzeichnis Suche.</span><span class="sxs-lookup"><span data-stu-id="2c5a5-111">Because of this, **objectCategory** is better suited for type matching of objects in a directory search.</span></span> <span data-ttu-id="2c5a5-112">ADSI verwendet dies als Standard Übereinstimmungs Kriterium.</span><span class="sxs-lookup"><span data-stu-id="2c5a5-112">ADSI uses this as the default matching criterion.</span></span> <span data-ttu-id="2c5a5-113">Suchvorgänge mit einer **objectClass** können nicht in großen Datenbanken skaliert werden.</span><span class="sxs-lookup"><span data-stu-id="2c5a5-113">Searches using one **objectClass** are not scalable to large databases.</span></span> <span data-ttu-id="2c5a5-114">ADSI unterstützt die Syntaxen "(objectCategory = somedn)" und "(objectCategory = LDAP \_ Display \_ Name \_ of \_ Class)".</span><span class="sxs-lookup"><span data-stu-id="2c5a5-114">ADSI supports "(objectCategory=SomeDN)" and "(objectCategory=Ldap\_Display\_Name\_of\_Class)" syntaxes.</span></span>

<span data-ttu-id="2c5a5-115">Eine Ausnahme besteht darin, dass der LDAP-Suchfilter "(objectClass = \* )" keine Suche in der Objektklasse angibt, sondern lediglich prüft, ob die Objekte vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="2c5a5-115">The exception to all of this is that the LDAP search filter "(objectClass=\*)" does not specify a search on object class, but merely tests for the presence of the objects.</span></span>

 

 




