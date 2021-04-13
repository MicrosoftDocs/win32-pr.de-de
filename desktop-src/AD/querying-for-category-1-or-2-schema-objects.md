---
title: Abfragen von Schema Objekten der Kategorie 1 oder 2
description: Das systemFlags-Attribut von attributeSchema-und classSchema-Objekten ist eine ganzzahlige Bitmaske, die Flags enthält, die zusätzliche System Qualitäten des Attributs oder der Klasse angeben.
ms.assetid: 5cc8f296-df3e-4643-9694-543f069a2cc7
ms.tgt_platform: multiple
keywords:
- Abfragen von Schema Objekten der Kategorie 1 oder 2
- Objekt-AD, Abfragen von Schema Objekten der Kategorie 1 oder 2
- Schema AD, Abfragen von Schema Objekten der Kategorie 1 oder 2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c67b57821cbebc80b3b6e93d158bbb8af8f7103
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/17/2020
ms.locfileid: "104314619"
---
# <a name="querying-for-category-1-or-2-schema-objects"></a><span data-ttu-id="24629-106">Abfragen von Schema Objekten der Kategorie 1 oder 2</span><span class="sxs-lookup"><span data-stu-id="24629-106">Querying for Category 1 or 2 Schema Objects</span></span>

<span data-ttu-id="24629-107">Das **systemFlags** -Attribut von **attributeSchema** -und **classSchema** -Objekten ist eine ganzzahlige Bitmaske, die Flags enthält, die zusätzliche System Qualitäten des Attributs oder der Klasse angeben.</span><span class="sxs-lookup"><span data-stu-id="24629-107">The **systemFlags** attribute of **attributeSchema** and **classSchema** objects is an integer bitmask that contains flags that indicate additional system qualities of the attribute or class.</span></span> <span data-ttu-id="24629-108">Die [**ADS \_ Systemflag \_ enum**](/windows/win32/api/iads/ne-iads-ads_systemflag_enum) -Enumeration enthält Werte, die den Bits entsprechen, die Sie im **systemFlags** -Attribut festlegen können.</span><span class="sxs-lookup"><span data-stu-id="24629-108">The [**ADS\_SYSTEMFLAG\_ENUM**](/windows/win32/api/iads/ne-iads-ads_systemflag_enum) enumeration contains values that correspond to the bits you can set in the **systemFlags** attribute.</span></span> <span data-ttu-id="24629-109">Es gibt weitere **systemFlags** -Bits, die Sie nicht festlegen können, z. b. das 0x10-Bit, das angibt, ob das Attribut oder die Klasse Kategorie 1 oder Kategorie 2 ist.</span><span class="sxs-lookup"><span data-stu-id="24629-109">There are additional **systemFlags** bits that you cannot set, such as the 0x10 bit which indicates whether the attribute or class is category 1 or category 2.</span></span> <span data-ttu-id="24629-110">Das 0x10-Bit ist für Objekte der Kategorie 1 festgelegt, bei denen es sich um die Klassen und Attribute handelt, die in dem im System enthaltenen Basis Schema enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="24629-110">The 0x10 bit is set for category 1 objects, which are the classes and attributes included in the base schema included with the system.</span></span> <span data-ttu-id="24629-111">Das-Bit ist nicht für Attribute und Klassen der Kategorie 2 festgelegt, bei denen es sich um Erweiterungen für das Schema handelt.</span><span class="sxs-lookup"><span data-stu-id="24629-111">The bit is not set for category 2 attributes and classes, which are extensions to the schema.</span></span> <span data-ttu-id="24629-112">Wenn für ein **attributeSchema** -oder **classSchema** -Objekt keine **systemFlags** -Eigenschaft vorhanden ist, ist es Kategorie 2.</span><span class="sxs-lookup"><span data-stu-id="24629-112">If no **systemFlags** property exists on an **attributeSchema** or **classSchema** object, it is category 2.</span></span>

<span data-ttu-id="24629-113">Das **Bit mit der LDAP-abgleichsregel \_ \_ \_ \_ und** die abgleichsregel können verwendet werden, um nach Objekten zu suchen, für die das 0x10-Flag im **systemFlags** -Attribut</span><span class="sxs-lookup"><span data-stu-id="24629-113">The **LDAP\_MATCHING\_RULE\_BIT\_AND** matching rule can be used to search for objects that have the 0x10 flag set in the **systemFlags** attribute.</span></span> <span data-ttu-id="24629-114">Weitere Informationen finden Sie unter [Such Filter Syntax](/windows/desktop/ADSI/search-filter-syntax).</span><span class="sxs-lookup"><span data-stu-id="24629-114">For more information, see [Search Filter Syntax](/windows/desktop/ADSI/search-filter-syntax).</span></span>

## <a name="querying-for-category-1"></a><span data-ttu-id="24629-115">Abfragen für Kategorie 1</span><span class="sxs-lookup"><span data-stu-id="24629-115">Querying for Category 1</span></span>

<span data-ttu-id="24629-116">Die folgende Abfrage Zeichenfolge sucht nach Kategorie 1-Attributen (**attributeSchema** -Objekte mit dem 0x10-Bit, das in der **systemFlags** -Eigenschaft festgelegt ist).</span><span class="sxs-lookup"><span data-stu-id="24629-116">The following query string searches for category 1 attributes (**attributeSchema** objects with the 0x10 bit set in the **systemFlags** property).</span></span>


```C++
(&(objectCategory=attributeSchema)(systemFlags:1.2.840.113556.1.4.803:=16) )
```



<span data-ttu-id="24629-117">Beachten Sie, dass die LDAP-Abfrage Syntax im obigen Beispiel Dezimalwerte erfordert. Daher muss der hexadezimale Wert des Flags in "Decimal" konvertiert werden.</span><span class="sxs-lookup"><span data-stu-id="24629-117">Be aware that, in the example above, the LDAP query syntax requires decimal values; therefore, the hex value of the flag must be converted to decimal.</span></span> <span data-ttu-id="24629-118">In diesem Fall ist Category 1 Bit 0x10, sodass der Filter Wert als 16 angegeben werden muss.</span><span class="sxs-lookup"><span data-stu-id="24629-118">In this case, category 1 bit is 0x10 so the filter value must be specified as 16.</span></span>

## <a name="querying-for-category-2"></a><span data-ttu-id="24629-119">Abfragen für Kategorie 2</span><span class="sxs-lookup"><span data-stu-id="24629-119">Querying for Category 2</span></span>

<span data-ttu-id="24629-120">Mit der folgenden Abfrage Zeichenfolge wird nach Kategorie 2 Attributen gesucht (**attributeSchema** -Objekte, für die das 0x10-Bit nicht in der **systemFlags** -Eigenschaft festgelegt ist).</span><span class="sxs-lookup"><span data-stu-id="24629-120">The following query string searches for category 2 attributes (**attributeSchema** objects that do not have the 0x10 bit set in the **systemFlags** property).</span></span>


```C++
(&(objectCategory=attributeSchema)(!(systemFlags:1.2.840.113556.1.4.803:=16)))
```



<span data-ttu-id="24629-121">Beachten Sie, dass diese Abfrage auch **attributeSchema** -Objekte zurückgibt, die nicht über eine **systemFlags** -Eigenschaft verfügen, und daher implizit nicht das angegebene Flag festgelegt haben.</span><span class="sxs-lookup"><span data-stu-id="24629-121">Be aware that this query also returns **attributeSchema** objects that do not have a **systemFlags** property, and, therefore, implicitly do not have the specified flag set.</span></span>

 

 