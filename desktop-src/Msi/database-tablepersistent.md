---
description: Die tablepersistent-Eigenschaft des Database-Objekts gibt den persistenzstatus der Tabelle als einen der folgenden Parameter zurück.
ms.assetid: c395e99c-5cdc-4d7b-ac55-a79d4e1477dc
title: Database. tablepersistent (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Database.TablePersistent
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 1a1e91e1c01ca3fe2efc45855583031e84dc2b47
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372737"
---
# <a name="databasetablepersistent-property"></a><span data-ttu-id="afc59-103">Database. tablepersistent (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="afc59-103">Database.TablePersistent property</span></span>

<span data-ttu-id="afc59-104">Die **tablepersistent** -Eigenschaft des [**Database**](database-object.md) -Objekts gibt den persistenzstatus der Tabelle als einen der folgenden Parameter zurück.</span><span class="sxs-lookup"><span data-stu-id="afc59-104">The **TablePersistent** property of the [**Database**](database-object.md) object returns the persistence state of the table as one of the following parameters.</span></span>



| <span data-ttu-id="afc59-105">Tabellen Status</span><span class="sxs-lookup"><span data-stu-id="afc59-105">Table state</span></span>               | <span data-ttu-id="afc59-106">Wert</span><span class="sxs-lookup"><span data-stu-id="afc59-106">Value</span></span> | <span data-ttu-id="afc59-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="afc59-107">Description</span></span>                    |
|---------------------------|-------|--------------------------------|
| <span data-ttu-id="afc59-108">msievaluateconditionfalse</span><span class="sxs-lookup"><span data-stu-id="afc59-108">msiEvaluateConditionFalse</span></span> | <span data-ttu-id="afc59-109">0</span><span class="sxs-lookup"><span data-stu-id="afc59-109">0</span></span>     | <span data-ttu-id="afc59-110">Die Tabelle ist temporär.</span><span class="sxs-lookup"><span data-stu-id="afc59-110">Table is temporary.</span></span>            |
| <span data-ttu-id="afc59-111">msievaluateconditiontrue</span><span class="sxs-lookup"><span data-stu-id="afc59-111">msiEvaluateConditionTrue</span></span>  | <span data-ttu-id="afc59-112">1</span><span class="sxs-lookup"><span data-stu-id="afc59-112">1</span></span>     | <span data-ttu-id="afc59-113">Die Tabelle ist persistent.</span><span class="sxs-lookup"><span data-stu-id="afc59-113">Table is persistent.</span></span>           |
| <span data-ttu-id="afc59-114">msievaluateconditionnone</span><span class="sxs-lookup"><span data-stu-id="afc59-114">msiEvaluateConditionNone</span></span>  | <span data-ttu-id="afc59-115">2</span><span class="sxs-lookup"><span data-stu-id="afc59-115">2</span></span>     | <span data-ttu-id="afc59-116">Die Tabelle befindet sich nicht in der Datenbank.</span><span class="sxs-lookup"><span data-stu-id="afc59-116">Table is not in the database.</span></span>  |
| <span data-ttu-id="afc59-117">msievaluateconditionerror</span><span class="sxs-lookup"><span data-stu-id="afc59-117">msiEvaluateConditionError</span></span> | <span data-ttu-id="afc59-118">3</span><span class="sxs-lookup"><span data-stu-id="afc59-118">3</span></span>     | <span data-ttu-id="afc59-119">Ungültiger oder fehlender Tabellenname.</span><span class="sxs-lookup"><span data-stu-id="afc59-119">Invalid or missing table name.</span></span> |



 

<span data-ttu-id="afc59-120">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="afc59-120">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="afc59-121">Syntax</span><span class="sxs-lookup"><span data-stu-id="afc59-121">Syntax</span></span>


```JScript
propVal = Database.TablePersistent
```



## <a name="property-value"></a><span data-ttu-id="afc59-122">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="afc59-122">Property value</span></span>

## <a name="requirements"></a><span data-ttu-id="afc59-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="afc59-123">Requirements</span></span>



| <span data-ttu-id="afc59-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="afc59-124">Requirement</span></span> | <span data-ttu-id="afc59-125">Wert</span><span class="sxs-lookup"><span data-stu-id="afc59-125">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="afc59-126">Version</span><span class="sxs-lookup"><span data-stu-id="afc59-126">Version</span></span><br/> | <span data-ttu-id="afc59-127">Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7.</span><span class="sxs-lookup"><span data-stu-id="afc59-127">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="afc59-128">Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="afc59-128">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="afc59-129">Windows Installer unter Windows Server 2003 oder Windows XP</span><span class="sxs-lookup"><span data-stu-id="afc59-129">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="afc59-130">DLL</span><span class="sxs-lookup"><span data-stu-id="afc59-130">DLL</span></span><br/>     | <dl> <span data-ttu-id="afc59-131"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="afc59-131"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="afc59-132">IID</span><span class="sxs-lookup"><span data-stu-id="afc59-132">IID</span></span><br/>     | <span data-ttu-id="afc59-133">IID \_ idatabase ist definiert als 000c109d-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="afc59-133">IID\_IDatabase is defined as 000C109D-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                            |



 

 




