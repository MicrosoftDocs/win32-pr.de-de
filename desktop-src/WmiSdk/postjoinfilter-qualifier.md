---
description: Sie können die Instanzen einer Verknüpfungs Ansichts Klasse filtern, indem Sie dem postjoinfilter-Qualifizierer eine WQL-Abfrage zuweisen.
ms.assetid: 926a7262-ea6b-4a5a-8aa7-6ec0ae389031
ms.tgt_platform: multiple
title: Postjoinfilter-Qualifizierer
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PostJoinFilter
api_type:
- NA
api_location: ''
ms.openlocfilehash: ac86aeafefc8057a1612c5007e55e7633c655c59
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352196"
---
# <a name="postjoinfilter-qualifier"></a><span data-ttu-id="62f92-103">Postjoinfilter-Qualifizierer</span><span class="sxs-lookup"><span data-stu-id="62f92-103">PostJoinFilter Qualifier</span></span>

<span data-ttu-id="62f92-104">Sie können die Instanzen einer Verknüpfungs Ansichts Klasse filtern, indem Sie dem **postjoinfilter** -Qualifizierer eine WQL-Abfrage zuweisen.</span><span class="sxs-lookup"><span data-stu-id="62f92-104">You can filter the instances of a join view class by assigning a WQL query to the **PostJoinFilter** qualifier.</span></span> <span data-ttu-id="62f92-105">Der Wert der WQL-Abfrage wird auf die Instanzen der joinansichts Klasse angewendet.</span><span class="sxs-lookup"><span data-stu-id="62f92-105">The value of the WQL query is applied to the instances of the join view class.</span></span> <span data-ttu-id="62f92-106">Sie können diesen Qualifizierer verwenden, um die Instanzen der Ansichts Klasse auf jene zu beschränken, die bestimmte Bedingungen erfüllen.</span><span class="sxs-lookup"><span data-stu-id="62f92-106">You can use this qualifier to restrict the instances of your view class to those that meet specific conditions.</span></span> <span data-ttu-id="62f92-107">Die folgende WQL-Abfrage filtert Instanzen einer Verknüpfungs Klasse, die auf der Grundlage von Instanzen von [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk)aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="62f92-107">The following WQL query filters instances of a join class called based on instances of [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk).</span></span>


```C++
PostJoinFilter("SELECT * FROM JoinDrive" +
    " WHERE FreeSpace > 1000000" +
    " and Description = \"3 1/2 Inch Floppy Drive\"")
```



<span data-ttu-id="62f92-108">Es gibt mehrere Einschränkungen bei der Verwendung dieses Qualifizierers:</span><span class="sxs-lookup"><span data-stu-id="62f92-108">There are several restrictions to the use of this qualifier:</span></span>

-   <span data-ttu-id="62f92-109">**Postjoinfilter** ist nur für Verknüpfungs Ansichts Klassen verfügbar.</span><span class="sxs-lookup"><span data-stu-id="62f92-109">**PostJoinFilter** is only available to join view classes.</span></span>
-   <span data-ttu-id="62f92-110">Die in der Abfrage angegebenen Klassennamen und Eigenschaftsnamen verweisen auf die Eigenschaften der Ansichts Klasse, nicht auf die Quell Klasse.</span><span class="sxs-lookup"><span data-stu-id="62f92-110">The class name and property names specified in the query refer to the properties of the view class, not the source class.</span></span>
-   <span data-ttu-id="62f92-111">Es ist kein Ausschluss der Eigenschaften zulässig. nur `SELECT *` typabfragen sind zulässig.</span><span class="sxs-lookup"><span data-stu-id="62f92-111">No exclusion of properties is permitted; only `SELECT *` type queries are allowed.</span></span>

## <a name="requirements"></a><span data-ttu-id="62f92-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="62f92-112">Requirements</span></span>



| <span data-ttu-id="62f92-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="62f92-113">Requirement</span></span> | <span data-ttu-id="62f92-114">Wert</span><span class="sxs-lookup"><span data-stu-id="62f92-114">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="62f92-115">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="62f92-115">Minimum supported client</span></span><br/> | <span data-ttu-id="62f92-116">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="62f92-116">Windows Vista</span></span><br/>       |
| <span data-ttu-id="62f92-117">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="62f92-117">Minimum supported server</span></span><br/> | <span data-ttu-id="62f92-118">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="62f92-118">Windows Server 2008</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="62f92-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="62f92-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="62f92-120">**Spezifische Qualifizierer für den Ansichts Anbieter**</span><span class="sxs-lookup"><span data-stu-id="62f92-120">**Qualifiers Specific to the View Provider**</span></span>](qualifiers-specific-to-the-view-provider.md)
</dt> </dl>

 

