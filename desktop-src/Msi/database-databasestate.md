---
description: Die databasestate-Eigenschaft des Database-Objekts ist eine schreibgeschützte Eigenschaft.
ms.assetid: 0a466e53-4ff5-4b95-b754-1aac0af16805
title: Database. databasestate (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Database.DatabaseState
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 12a667bf145ea00f7a881c8219987f21c99af4ff
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359296"
---
# <a name="databasedatabasestate-property"></a><span data-ttu-id="680bb-103">Database. databasestate (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="680bb-103">Database.DatabaseState property</span></span>

<span data-ttu-id="680bb-104">Die **databasestate** -Eigenschaft des [**Database**](database-object.md) -Objekts ist eine schreibgeschützte Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="680bb-104">The **DatabaseState** property of the [**Database**](database-object.md) object is a read-only property.</span></span>

<span data-ttu-id="680bb-105">Diese Eigenschaft gibt den persistenzstatus der Datenbank als einen der folgenden Parameter zurück.</span><span class="sxs-lookup"><span data-stu-id="680bb-105">This property returns the persistence state of the database as one of the following parameters.</span></span>



| <span data-ttu-id="680bb-106">Daten Bank Status</span><span class="sxs-lookup"><span data-stu-id="680bb-106">Database state</span></span>        | <span data-ttu-id="680bb-107">Wert</span><span class="sxs-lookup"><span data-stu-id="680bb-107">Value</span></span> | <span data-ttu-id="680bb-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="680bb-108">Description</span></span>                                                                                                |
|-----------------------|-------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="680bb-109">msidatabasestatueread</span><span class="sxs-lookup"><span data-stu-id="680bb-109">msiDatabaseStateRead</span></span>  | <span data-ttu-id="680bb-110">0</span><span class="sxs-lookup"><span data-stu-id="680bb-110">0</span></span>     | <span data-ttu-id="680bb-111">Die Datenbank wird schreibgeschützt geöffnet.</span><span class="sxs-lookup"><span data-stu-id="680bb-111">Database opens as read-only.</span></span> <span data-ttu-id="680bb-112">Änderungen an persistenten Daten sind nicht zulässig, und temporäre Daten werden nicht gespeichert.</span><span class="sxs-lookup"><span data-stu-id="680bb-112">Changes to persistent data are not permitted and temporary data is not saved.</span></span> |
| <span data-ttu-id="680bb-113">msidatabasestatewrite</span><span class="sxs-lookup"><span data-stu-id="680bb-113">msiDatabaseStateWrite</span></span> | <span data-ttu-id="680bb-114">1</span><span class="sxs-lookup"><span data-stu-id="680bb-114">1</span></span>     | <span data-ttu-id="680bb-115">Die Datenbank ist für Lese-und Schreibvorgänge voll funktionsfähig.</span><span class="sxs-lookup"><span data-stu-id="680bb-115">Database is fully operational for read and write.</span></span>                                                          |



 

<span data-ttu-id="680bb-116">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="680bb-116">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="680bb-117">Syntax</span><span class="sxs-lookup"><span data-stu-id="680bb-117">Syntax</span></span>


```JScript
propVal = Database.DatabaseState
```



## <a name="property-value"></a><span data-ttu-id="680bb-118">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="680bb-118">Property value</span></span>

## <a name="requirements"></a><span data-ttu-id="680bb-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="680bb-119">Requirements</span></span>



| <span data-ttu-id="680bb-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="680bb-120">Requirement</span></span> | <span data-ttu-id="680bb-121">Wert</span><span class="sxs-lookup"><span data-stu-id="680bb-121">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="680bb-122">Version</span><span class="sxs-lookup"><span data-stu-id="680bb-122">Version</span></span><br/> | <span data-ttu-id="680bb-123">Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7.</span><span class="sxs-lookup"><span data-stu-id="680bb-123">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="680bb-124">Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="680bb-124">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="680bb-125">Windows Installer unter Windows Server 2003 oder Windows XP</span><span class="sxs-lookup"><span data-stu-id="680bb-125">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="680bb-126">DLL</span><span class="sxs-lookup"><span data-stu-id="680bb-126">DLL</span></span><br/>     | <dl> <span data-ttu-id="680bb-127"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="680bb-127"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="680bb-128">IID</span><span class="sxs-lookup"><span data-stu-id="680bb-128">IID</span></span><br/>     | <span data-ttu-id="680bb-129">IID \_ idatabase ist definiert als 000c109d-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="680bb-129">IID\_IDatabase is defined as 000C109D-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                            |



 

 




