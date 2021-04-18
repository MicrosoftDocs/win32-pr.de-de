---
description: Die Execute-Methode des View-Objekts verwendet das Fragezeichen Token zum Darstellen von Parametern in einer SQL-Anweisung. Weitere Informationen finden Sie unter SQL-Syntax. Die Werte dieser Parameter werden als die entsprechenden Felder eines Parameterdaten Satzes übergeben.
ms.assetid: 4f2b2cb8-8f59-4e4a-ba09-6cb092ef81d6
title: View.Exeniedliche Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- View.Execute
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 939d1aa5216085d701fb728ad5e5e9aa9e07e702
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359223"
---
# <a name="viewexecute-method"></a><span data-ttu-id="d6d17-105">View.Exeniedliche Methode</span><span class="sxs-lookup"><span data-stu-id="d6d17-105">View.Execute method</span></span>

<span data-ttu-id="d6d17-106">Die **Execute** -Methode des [**View**](view-object.md) -Objekts verwendet das Fragezeichen Token zum Darstellen von Parametern in einer SQL-Anweisung.</span><span class="sxs-lookup"><span data-stu-id="d6d17-106">The **Execute** method of the [**View**](view-object.md) object uses the question mark token to represent parameters in an SQL statement.</span></span> <span data-ttu-id="d6d17-107">Weitere Informationen finden Sie unter [SQL-Syntax](sql-syntax.md).</span><span class="sxs-lookup"><span data-stu-id="d6d17-107">For more information, see [SQL Syntax](sql-syntax.md).</span></span> <span data-ttu-id="d6d17-108">Die Werte dieser Parameter werden als die entsprechenden Felder eines Parameterdaten Satzes übergeben.</span><span class="sxs-lookup"><span data-stu-id="d6d17-108">The values of these parameters are passed in as the corresponding fields of a parameter record.</span></span>

## <a name="syntax"></a><span data-ttu-id="d6d17-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="d6d17-109">Syntax</span></span>


```JScript
View.Execute(
  record
)
```



## <a name="parameters"></a><span data-ttu-id="d6d17-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="d6d17-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d6d17-111">*record*</span><span class="sxs-lookup"><span data-stu-id="d6d17-111">*record*</span></span> 
</dt> <dd>

<span data-ttu-id="d6d17-112">Optionale [**Datensatz**](record-object.md) -Objekte, die die Werte enthalten, die die Parameter Token (?) in der SQL-Abfrage ersetzen.</span><span class="sxs-lookup"><span data-stu-id="d6d17-112">Optional [**Record**](record-object.md) objects that contains the values that replace the parameter tokens (?) in the SQL query.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d6d17-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d6d17-113">Return value</span></span>

<span data-ttu-id="d6d17-114">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="d6d17-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d6d17-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d6d17-115">Remarks</span></span>

<span data-ttu-id="d6d17-116">Diese Methode muss vor allen Aufrufen der [**Fetch**](view-fetch.md) -Methode aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="d6d17-116">This method must be called before any calls to the [**Fetch**](view-fetch.md) method.</span></span>

<span data-ttu-id="d6d17-117">Wenn die SQL-Abfrage Werte mit Parameter Markierungen (?) angibt, muss ein Datensatz angegeben werden, der alle Ersetzungs Werte enthält, die sich in der gleichen Reihenfolge und dem gleichen Datentyp wie die Parameter Markierungen befinden müssen.</span><span class="sxs-lookup"><span data-stu-id="d6d17-117">If the SQL query specifies values with parameter markers (?), a record must be supplied that contains all of the replacement values, which must be in the same order and of the same data type as the parameter markers.</span></span> <span data-ttu-id="d6d17-118">Wenn diese Methode mit INSERT-und Update-Abfragen verwendet wird, müssen die Fragezeichen Token allen nicht parametrisierten Werten vorangestellt sein.</span><span class="sxs-lookup"><span data-stu-id="d6d17-118">When this method is used with INSERT and UPDATE queries, the question mark tokens must precede all the non-parameterized values.</span></span>

<span data-ttu-id="d6d17-119">Diese Abfragen sind z. b. gültig:</span><span class="sxs-lookup"><span data-stu-id="d6d17-119">For example, these queries are valid:</span></span>

<span data-ttu-id="d6d17-120">Aktualisieren von {Table-List} Set {Column} =?</span><span class="sxs-lookup"><span data-stu-id="d6d17-120">UPDATE {table-list} SET {column}= ?</span></span> <span data-ttu-id="d6d17-121">, {Column} = {Constant}</span><span class="sxs-lookup"><span data-stu-id="d6d17-121">, {column}= {constant}</span></span>

<span data-ttu-id="d6d17-122">INSERT INTO {TABLE} ({Column-List})-Werte (?, {Constant-List})</span><span class="sxs-lookup"><span data-stu-id="d6d17-122">INSERT INTO {table} ({column-list}) VALUES (?, {constant-list})</span></span>

<span data-ttu-id="d6d17-123">Diese Abfragen sind jedoch ungültig:</span><span class="sxs-lookup"><span data-stu-id="d6d17-123">However these queries are invalid:</span></span>

<span data-ttu-id="d6d17-124">Aktualisieren von {Table-List} Set {Column} = {Constant}, {Column} =?</span><span class="sxs-lookup"><span data-stu-id="d6d17-124">UPDATE {table-list} SET {column}= {constant}, {column}=?</span></span>

<span data-ttu-id="d6d17-125">INSERT INTO {TABLE} ({Column-List})-Werte ({Constant-List},?</span><span class="sxs-lookup"><span data-stu-id="d6d17-125">INSERT INTO {table} ({column-list}) VALUES ({constant-list}, ?</span></span> <span data-ttu-id="d6d17-126">)</span><span class="sxs-lookup"><span data-stu-id="d6d17-126">)</span></span>

<span data-ttu-id="d6d17-127">Wenn die Methode fehlschlägt, können Sie erweiterte Fehlerinformationen mithilfe der [**lasterrorrecord**](installer-lasterrorrecord.md) -Methode abrufen.</span><span class="sxs-lookup"><span data-stu-id="d6d17-127">If the method fails, you can obtain extended error information by using the [**LastErrorRecord**](installer-lasterrorrecord.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="d6d17-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d6d17-128">Requirements</span></span>



| <span data-ttu-id="d6d17-129">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d6d17-129">Requirement</span></span> | <span data-ttu-id="d6d17-130">Wert</span><span class="sxs-lookup"><span data-stu-id="d6d17-130">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d6d17-131">Version</span><span class="sxs-lookup"><span data-stu-id="d6d17-131">Version</span></span><br/> | <span data-ttu-id="d6d17-132">Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7.</span><span class="sxs-lookup"><span data-stu-id="d6d17-132">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="d6d17-133">Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="d6d17-133">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="d6d17-134">Windows Installer unter Windows Server 2003 oder Windows XP</span><span class="sxs-lookup"><span data-stu-id="d6d17-134">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="d6d17-135">DLL</span><span class="sxs-lookup"><span data-stu-id="d6d17-135">DLL</span></span><br/>     | <dl> <span data-ttu-id="d6d17-136"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d6d17-136"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="d6d17-137">IID</span><span class="sxs-lookup"><span data-stu-id="d6d17-137">IID</span></span><br/>     | <span data-ttu-id="d6d17-138">IID \_ iView ist definiert als 000c109c-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="d6d17-138">IID\_IView is defined as 000C109C-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                |



 

 




