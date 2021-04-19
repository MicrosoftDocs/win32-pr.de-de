---
description: Das stringlist-Objekt ist eine Auflistung von Zeichen folgen. Der Client muss überprüfen, ob das stringlist-Objekt vorhanden und nicht leer ist, bevor auf seine Eigenschaften verwiesen wird.
ms.assetid: 7021320a-d01a-43e8-90a5-6105a11a4613
title: Stringlist-Objekt
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- StringList
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 6493b9e1723d46ce290c7472bbcee7eb9ec34725
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361916"
---
# <a name="stringlist-object"></a><span data-ttu-id="51115-104">Stringlist-Objekt</span><span class="sxs-lookup"><span data-stu-id="51115-104">StringList object</span></span>

<span data-ttu-id="51115-105">Das **stringlist** -Objekt ist eine Auflistung von Zeichen folgen.</span><span class="sxs-lookup"><span data-stu-id="51115-105">The **StringList** object is a collection of strings.</span></span> <span data-ttu-id="51115-106">Der Client muss überprüfen, ob das **stringlist** -Objekt vorhanden und nicht leer ist, bevor auf seine Eigenschaften verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="51115-106">The client must verify that the **StringList** object exists and is not empty before referencing its properties.</span></span>

## <a name="members"></a><span data-ttu-id="51115-107">Member</span><span class="sxs-lookup"><span data-stu-id="51115-107">Members</span></span>

<span data-ttu-id="51115-108">Das **stringlist** -Objekt verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="51115-108">The **StringList** object has these types of members:</span></span>

-   [<span data-ttu-id="51115-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="51115-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="51115-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="51115-110">Properties</span></span>

<span data-ttu-id="51115-111">Das **stringlist** -Objekt verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="51115-111">The **StringList** object has these properties.</span></span>



| <span data-ttu-id="51115-112">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="51115-112">Property</span></span>                                     | <span data-ttu-id="51115-113">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="51115-113">Description</span></span>                                                          |
|:---------------------------------------------|:---------------------------------------------------------------------|
| [<span data-ttu-id="51115-114">**Countdown**</span><span class="sxs-lookup"><span data-stu-id="51115-114">**Count**</span></span>](stringlist-count.md)<br/> | <span data-ttu-id="51115-115">Gibt die Anzahl der Elemente im **stringlist** -Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="51115-115">Returns the number of items in the **StringList** object.</span></span><br/> |
| [<span data-ttu-id="51115-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="51115-116">**Item**</span></span>](stringlist-item.md)<br/>   | <span data-ttu-id="51115-117">Gibt eine Zeichenfolge in der **stringlist** -Objekt Auflistung zurück.</span><span class="sxs-lookup"><span data-stu-id="51115-117">Returns a string in the **StringList** object collection.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="51115-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="51115-118">Requirements</span></span>



| <span data-ttu-id="51115-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="51115-119">Requirement</span></span> | <span data-ttu-id="51115-120">Wert</span><span class="sxs-lookup"><span data-stu-id="51115-120">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="51115-121">Version</span><span class="sxs-lookup"><span data-stu-id="51115-121">Version</span></span><br/> | <span data-ttu-id="51115-122">Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7.</span><span class="sxs-lookup"><span data-stu-id="51115-122">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="51115-123">Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="51115-123">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="51115-124">Windows Installer unter Windows Server 2003 oder Windows XP</span><span class="sxs-lookup"><span data-stu-id="51115-124">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="51115-125">DLL</span><span class="sxs-lookup"><span data-stu-id="51115-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="51115-126"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="51115-126"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="51115-127">IID</span><span class="sxs-lookup"><span data-stu-id="51115-127">IID</span></span><br/>     | <span data-ttu-id="51115-128">IID \_ istringlist ist definiert als 000c1095-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="51115-128">IID\_IStringList is defined as 000C1095-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                          |



## <a name="see-also"></a><span data-ttu-id="51115-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="51115-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="51115-130">Skript Beispiele für Windows Installer</span><span class="sxs-lookup"><span data-stu-id="51115-130">Windows Installer Scripting Examples</span></span>](windows-installer-scripting-examples.md)
</dt> </dl>

 

 




