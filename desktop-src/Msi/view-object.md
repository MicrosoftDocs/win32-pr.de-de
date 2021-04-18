---
description: Das View-Objekt stellt ein Resultset dar, das bei der Verarbeitung einer Abfrage mit der OpenView-Methode des Datenbankobjekts abgerufen wurde.
ms.assetid: d9d6583a-1cf3-4c33-a851-83e862e2338e
title: Objekt anzeigen
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- View
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: c26cfa3c4873913d70fca63537f1d25532648a42
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371164"
---
# <a name="view-object"></a><span data-ttu-id="996f7-103">Objekt anzeigen</span><span class="sxs-lookup"><span data-stu-id="996f7-103">View object</span></span>

<span data-ttu-id="996f7-104">Das **View** -Objekt stellt ein Resultset dar, das bei der Verarbeitung einer Abfrage mit der [**OpenView**](database-openview.md) -Methode des [**Daten Bank**](database-object.md) Objekts abgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="996f7-104">The **View** object represents a result set obtained when processing a query using the [**OpenView**](database-openview.md) method of the [**Database**](database-object.md) object.</span></span> <span data-ttu-id="996f7-105">Bevor Daten übertragen werden können, muss die Abfrage mit der [**Execute**](view-execute.md) -Methode ausgeführt werden, wobei alle ersetzbaren Parameter, die in der SQL-Abfrage Zeichenfolge festgelegt sind, übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="996f7-105">Before any data can be transferred, the query must be executed using the [**Execute**](view-execute.md) method, passing to it all replaceable parameters designated within the SQL query string.</span></span> <span data-ttu-id="996f7-106">Die Abfrage wird möglicherweise erneut ausgeführt, mit unterschiedlichen Parametern, wenn erforderlich, aber erst nach der Freigabe des Resultsets, indem alle Datensätze abgerufen oder die [**Close**](view-close.md) -Methode aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="996f7-106">The query may be executed again, with different parameters if needed, but only after freeing the result set either by fetching all the records or by calling the [**Close**](view-close.md) method.</span></span>

## <a name="members"></a><span data-ttu-id="996f7-107">Member</span><span class="sxs-lookup"><span data-stu-id="996f7-107">Members</span></span>

<span data-ttu-id="996f7-108">Das **Ansichts** Objekt enthält die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="996f7-108">The **View** object has these types of members:</span></span>

-   [<span data-ttu-id="996f7-109">Methoden</span><span class="sxs-lookup"><span data-stu-id="996f7-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="996f7-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="996f7-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="996f7-111">Methoden</span><span class="sxs-lookup"><span data-stu-id="996f7-111">Methods</span></span>

<span data-ttu-id="996f7-112">Das **View** -Objekt verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="996f7-112">The **View** object has these methods.</span></span>



| <span data-ttu-id="996f7-113">Methode</span><span class="sxs-lookup"><span data-stu-id="996f7-113">Method</span></span>                            | <span data-ttu-id="996f7-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="996f7-114">Description</span></span>                                                                                                                                                                     |
|:----------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="996f7-115">**Schließen**</span><span class="sxs-lookup"><span data-stu-id="996f7-115">**Close**</span></span>](view-close.md)       | <span data-ttu-id="996f7-116">Beendet die Abfrage Ausführung und gibt Datenbankressourcen frei.</span><span class="sxs-lookup"><span data-stu-id="996f7-116">Terminates query execution and releases database resources.</span></span><br/>                                                                                                          |
| [<span data-ttu-id="996f7-117">**Auszuführen**</span><span class="sxs-lookup"><span data-stu-id="996f7-117">**Execute**</span></span>](view-execute.md)   | <span data-ttu-id="996f7-118">Verwendet das Fragezeichen Token, um Parameter in einer SQL-Abfrage darzustellen.</span><span class="sxs-lookup"><span data-stu-id="996f7-118">Uses the question mark token to represent parameters in a SQL query.</span></span> <span data-ttu-id="996f7-119">Die Werte dieser Parameter werden als die entsprechenden Felder eines Parameterdaten Satzes übergeben.</span><span class="sxs-lookup"><span data-stu-id="996f7-119">The values of these parameters are passed in as the corresponding fields of a parameter record.</span></span><br/> |
| [<span data-ttu-id="996f7-120">**Fetti**</span><span class="sxs-lookup"><span data-stu-id="996f7-120">**Fetch**</span></span>](view-fetch.md)       | <span data-ttu-id="996f7-121">Gibt ein Daten Satz Objekt zurück, das die angeforderten Spaltendaten enthält, wenn weitere Zeilen im Resultset verfügbar sind. andernfalls wird NULL zurück [**gegeben**](record-object.md) .</span><span class="sxs-lookup"><span data-stu-id="996f7-121">Returns a [**Record**](record-object.md) object containing the requested column data if more rows are available in the result set, otherwise, it returns null.</span></span><br/>      |
| [<span data-ttu-id="996f7-122">**GetError**</span><span class="sxs-lookup"><span data-stu-id="996f7-122">**GetError**</span></span>](view-geterror.md) | <span data-ttu-id="996f7-123">Gibt den Validierungs Fehler und den Spaltennamen zurück, für den der Fehler aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="996f7-123">Returns the Validation error and column name for which the error occurred.</span></span><br/>                                                                                           |
| [<span data-ttu-id="996f7-124">**Ändern**</span><span class="sxs-lookup"><span data-stu-id="996f7-124">**Modify**</span></span>](view-modify.md)     | <span data-ttu-id="996f7-125">Ändert eine Datenbankzeile mit einem geänderten [**Daten Satz**](record-object.md) Objekt, das von der [**Fetch**](view-fetch.md) -Methode abgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="996f7-125">Modifies a database row with a modified [**Record**](record-object.md) object obtained by the [**Fetch**](view-fetch.md) method.</span></span><br/>                                   |



 

### <a name="properties"></a><span data-ttu-id="996f7-126">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="996f7-126">Properties</span></span>

<span data-ttu-id="996f7-127">Das **Ansichts** Objekt verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="996f7-127">The **View** object has these properties.</span></span>



| <span data-ttu-id="996f7-128">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="996f7-128">Property</span></span>                                         | <span data-ttu-id="996f7-129">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="996f7-129">Description</span></span>                                                                                                                           |
|:-------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="996f7-130">**ColumnInfo**</span><span class="sxs-lookup"><span data-stu-id="996f7-130">**ColumnInfo**</span></span>](view-columninfo.md)<br/> | <span data-ttu-id="996f7-131">Gibt ein [**Daten Satz**](record-object.md) Objekt zurück, das die angeforderten Informationen zu jeder Spalte im Resultset enthält.</span><span class="sxs-lookup"><span data-stu-id="996f7-131">Returns a [**Record**](record-object.md) object containing the requested information about each column in the result set.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="996f7-132">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="996f7-132">Requirements</span></span>



| <span data-ttu-id="996f7-133">Anforderung</span><span class="sxs-lookup"><span data-stu-id="996f7-133">Requirement</span></span> | <span data-ttu-id="996f7-134">Wert</span><span class="sxs-lookup"><span data-stu-id="996f7-134">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="996f7-135">Version</span><span class="sxs-lookup"><span data-stu-id="996f7-135">Version</span></span><br/> | <span data-ttu-id="996f7-136">Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7.</span><span class="sxs-lookup"><span data-stu-id="996f7-136">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="996f7-137">Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="996f7-137">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="996f7-138">Windows Installer unter Windows Server 2003 oder Windows XP</span><span class="sxs-lookup"><span data-stu-id="996f7-138">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="996f7-139">DLL</span><span class="sxs-lookup"><span data-stu-id="996f7-139">DLL</span></span><br/>     | <dl> <span data-ttu-id="996f7-140"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="996f7-140"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="996f7-141">IID</span><span class="sxs-lookup"><span data-stu-id="996f7-141">IID</span></span><br/>     | <span data-ttu-id="996f7-142">IID \_ iView ist definiert als 000c109c-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="996f7-142">IID\_IView is defined as 000C109C-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                |



## <a name="see-also"></a><span data-ttu-id="996f7-143">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="996f7-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="996f7-144">Skript Beispiele für Windows Installer</span><span class="sxs-lookup"><span data-stu-id="996f7-144">Windows Installer Scripting Examples</span></span>](windows-installer-scripting-examples.md)
</dt> </dl>

 

 




