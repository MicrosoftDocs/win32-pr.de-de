---
description: Die primarykeys-Eigenschaft des Database-Objekts gibt ein Datensatz-Objekt zurück, das den Tabellennamen in Feld 0 und die Spaltennamen (bestehend aus den primär Schlüsseln) in nachfolgenden Feldern enthält, die ihren Spalten Nummern entsprechen.
ms.assetid: 9aeafda4-65b8-4469-a391-eb25ca72459d
title: Database. primarykeys (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Database.PrimaryKeys
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: dc266bc2e563e6f32b7ff9b8c7c8cb0df69b723d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364531"
---
# <a name="databaseprimarykeys-property"></a><span data-ttu-id="1aab4-103">Database. primarykeys (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="1aab4-103">Database.PrimaryKeys property</span></span>

<span data-ttu-id="1aab4-104">Die **primarykeys** -Eigenschaft des [**Database**](database-object.md) -Objekts gibt ein [**Datensatz**](record-object.md) -Objekt zurück, das den Tabellennamen in Feld 0 und die Spaltennamen (bestehend aus den primär Schlüsseln) in nachfolgenden Feldern enthält, die ihren Spalten Nummern entsprechen.</span><span class="sxs-lookup"><span data-stu-id="1aab4-104">The **PrimaryKeys** property of the [**Database**](database-object.md) object returns a [**Record**](record-object.md) object containing the table name in field 0 and the column names (comprising the primary keys) in succeeding fields corresponding to their column numbers.</span></span> <span data-ttu-id="1aab4-105">Die Feld Anzahl des Datensatzes entspricht der Anzahl von Primärschlüssel Spalten.</span><span class="sxs-lookup"><span data-stu-id="1aab4-105">The field count of the record is the count of primary key columns.</span></span>

<span data-ttu-id="1aab4-106">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="1aab4-106">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="1aab4-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="1aab4-107">Syntax</span></span>


```JScript
propVal = Database.PrimaryKeys
```



## <a name="property-value"></a><span data-ttu-id="1aab4-108">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="1aab4-108">Property value</span></span>

<span data-ttu-id="1aab4-109">Erforderlicher Name einer vorhandenen Tabelle.</span><span class="sxs-lookup"><span data-stu-id="1aab4-109">Required name of an existing table.</span></span> <span data-ttu-id="1aab4-110">Wenn die Tabelle nicht vorhanden ist, wird ein Fehler generiert.</span><span class="sxs-lookup"><span data-stu-id="1aab4-110">An error is generated if the table does not exist.</span></span>

## <a name="remarks"></a><span data-ttu-id="1aab4-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1aab4-111">Remarks</span></span>

<span data-ttu-id="1aab4-112">Die **primarykeys** -Eigenschaft kann nicht mit der Tabellen [ \_ Tabelle](-tables-table.md) oder der [ \_ Spalten Tabelle](-columns-table.md)verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1aab4-112">The **PrimaryKeys** property cannot be used with the [\_Tables table](-tables-table.md) or the [\_Columns table](-columns-table.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="1aab4-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1aab4-113">Requirements</span></span>



| <span data-ttu-id="1aab4-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1aab4-114">Requirement</span></span> | <span data-ttu-id="1aab4-115">Wert</span><span class="sxs-lookup"><span data-stu-id="1aab4-115">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1aab4-116">Version</span><span class="sxs-lookup"><span data-stu-id="1aab4-116">Version</span></span><br/> | <span data-ttu-id="1aab4-117">Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7.</span><span class="sxs-lookup"><span data-stu-id="1aab4-117">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="1aab4-118">Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="1aab4-118">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="1aab4-119">Windows Installer unter Windows Server 2003 oder Windows XP</span><span class="sxs-lookup"><span data-stu-id="1aab4-119">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="1aab4-120">DLL</span><span class="sxs-lookup"><span data-stu-id="1aab4-120">DLL</span></span><br/>     | <dl> <span data-ttu-id="1aab4-121"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1aab4-121"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="1aab4-122">IID</span><span class="sxs-lookup"><span data-stu-id="1aab4-122">IID</span></span><br/>     | <span data-ttu-id="1aab4-123">IID \_ idatabase ist definiert als 000c109d-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="1aab4-123">IID\_IDatabase is defined as 000C109D-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                            |



 

 




