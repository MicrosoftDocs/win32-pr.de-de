---
description: Das RecordList-Objekt ist eine Sammlung von Datensatz-Objekten. Sie müssen überprüfen, ob das RecordList-Objekt vorhanden und nicht leer ist, bevor Sie auf seine Eigenschaften verweisen.
ms.assetid: 7f5ac153-8da1-4dc8-9bb7-defd4e821142
title: RecordList-Objekt
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RecordList
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: b3f09887333d8ddbf83de4bea2b2e654411883e0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371674"
---
# <a name="recordlist-object"></a><span data-ttu-id="97c5c-104">RecordList-Objekt</span><span class="sxs-lookup"><span data-stu-id="97c5c-104">RecordList object</span></span>

<span data-ttu-id="97c5c-105">Das **RecordList** -Objekt ist eine Sammlung von [**Datensatz**](record-object.md) -Objekten.</span><span class="sxs-lookup"><span data-stu-id="97c5c-105">The **RecordList** object is a collection of [**Record**](record-object.md) objects.</span></span> <span data-ttu-id="97c5c-106">Sie müssen überprüfen, ob das **RecordList** -Objekt vorhanden und nicht leer ist, bevor Sie auf seine Eigenschaften verweisen.</span><span class="sxs-lookup"><span data-stu-id="97c5c-106">You must verify that the **RecordList** object exists and is not empty before referencing its properties.</span></span>

## <a name="members"></a><span data-ttu-id="97c5c-107">Member</span><span class="sxs-lookup"><span data-stu-id="97c5c-107">Members</span></span>

<span data-ttu-id="97c5c-108">Das **RecordList** -Objekt verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="97c5c-108">The **RecordList** object has these types of members:</span></span>

-   [<span data-ttu-id="97c5c-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="97c5c-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="97c5c-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="97c5c-110">Properties</span></span>

<span data-ttu-id="97c5c-111">Das **RecordList** -Objekt verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="97c5c-111">The **RecordList** object has these properties.</span></span>



| <span data-ttu-id="97c5c-112">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="97c5c-112">Property</span></span>                                     | <span data-ttu-id="97c5c-113">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="97c5c-113">Description</span></span>                                                          |
|:---------------------------------------------|:---------------------------------------------------------------------|
| [<span data-ttu-id="97c5c-114">**Countdown**</span><span class="sxs-lookup"><span data-stu-id="97c5c-114">**Count**</span></span>](recordlist-count.md)<br/> | <span data-ttu-id="97c5c-115">Gibt die Anzahl der Elemente im **RecordList** -Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="97c5c-115">Returns the number of items in the **RecordList** object.</span></span><br/> |
| [<span data-ttu-id="97c5c-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="97c5c-116">**Item**</span></span>](recordlist-item.md)<br/>   | <span data-ttu-id="97c5c-117">Gibt einen Datensatz in einer **RecordList** -Objekt Auflistung zurück.</span><span class="sxs-lookup"><span data-stu-id="97c5c-117">Returns a record in a **RecordList** object collection.</span></span><br/>   |



 

## <a name="requirements"></a><span data-ttu-id="97c5c-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="97c5c-118">Requirements</span></span>



| <span data-ttu-id="97c5c-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="97c5c-119">Requirement</span></span> | <span data-ttu-id="97c5c-120">Wert</span><span class="sxs-lookup"><span data-stu-id="97c5c-120">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="97c5c-121">Version</span><span class="sxs-lookup"><span data-stu-id="97c5c-121">Version</span></span><br/> | <span data-ttu-id="97c5c-122">Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7.</span><span class="sxs-lookup"><span data-stu-id="97c5c-122">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="97c5c-123">Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="97c5c-123">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="97c5c-124">Windows Installer unter Windows Server 2003 oder Windows XP</span><span class="sxs-lookup"><span data-stu-id="97c5c-124">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="97c5c-125">DLL</span><span class="sxs-lookup"><span data-stu-id="97c5c-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="97c5c-126"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="97c5c-126"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="97c5c-127">IID</span><span class="sxs-lookup"><span data-stu-id="97c5c-127">IID</span></span><br/>     | <span data-ttu-id="97c5c-128">IID \_ irecordlist ist definiert als 000c1096-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="97c5c-128">IID\_IRecordList is defined as 000C1096-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                          |



## <a name="see-also"></a><span data-ttu-id="97c5c-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="97c5c-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="97c5c-130">**Datensatz**</span><span class="sxs-lookup"><span data-stu-id="97c5c-130">**Record**</span></span>](record-object.md)
</dt> <dt>

[<span data-ttu-id="97c5c-131">Skript Beispiele für Windows Installer</span><span class="sxs-lookup"><span data-stu-id="97c5c-131">Windows Installer Scripting Examples</span></span>](windows-installer-scripting-examples.md)
</dt> </dl>

 

 




