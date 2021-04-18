---
description: Die Merge-Methode des Datenbankobjekts führt die Verweis Datenbank mit der Basisdatenbank zusammen.
ms.assetid: 777060cf-c672-49d5-a1a8-8674fdc4bde4
title: Database. Merge-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Database.Merge
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 0a1d93ba6a9a4dc0304daba11c5868b77ece43b9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354659"
---
# <a name="databasemerge-method"></a><span data-ttu-id="7c759-103">Database. Merge-Methode</span><span class="sxs-lookup"><span data-stu-id="7c759-103">Database.Merge method</span></span>

<span data-ttu-id="7c759-104">Die **Merge** -Methode des [**Daten Bank**](database-object.md) Objekts führt die Verweis Datenbank mit der Basisdatenbank zusammen.</span><span class="sxs-lookup"><span data-stu-id="7c759-104">The **Merge** method of the [**Database**](database-object.md) object merges the reference database with the base database.</span></span>

## <a name="syntax"></a><span data-ttu-id="7c759-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="7c759-105">Syntax</span></span>


```JScript
Database.Merge(
  reference,
  errorTable
)
```



## <a name="parameters"></a><span data-ttu-id="7c759-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="7c759-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7c759-107">*Referenz*</span><span class="sxs-lookup"><span data-stu-id="7c759-107">*reference*</span></span> 
</dt> <dd>

<span data-ttu-id="7c759-108">Das erforderliche [**Daten Bank**](database-object.md) Objekt, das in der Datenbank zusammengeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="7c759-108">The required [**Database**](database-object.md) object to be merged into the database.</span></span>

</dd> <dt>

<span data-ttu-id="7c759-109">*errortable*</span><span class="sxs-lookup"><span data-stu-id="7c759-109">*errorTable*</span></span> 
</dt> <dd>

<span data-ttu-id="7c759-110">Ein optionaler Name einer Tabelle, die die Namen der Tabellen mit Mergekonflikten, die Anzahl der in Konflikt stehenden Zeilen in der Tabelle und einen Verweis auf die Tabelle mit dem Mergekonflikt enthalten soll.</span><span class="sxs-lookup"><span data-stu-id="7c759-110">An optional name of a table to contain the names of the tables containing merge conflicts, the number of conflicting rows within the table, and a reference to the table with the merge conflict.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7c759-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7c759-111">Return value</span></span>

<span data-ttu-id="7c759-112">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="7c759-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="7c759-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7c759-113">Remarks</span></span>

<span data-ttu-id="7c759-114">Die [**msidatabasemerge**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasemergea) -Funktion und die **Merge** -Methode des [**Daten Bank**](database-object.md) Objekts können nicht zum Zusammenführen eines Moduls verwendet werden, das in einem Installationspaket enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="7c759-114">The [**MsiDatabaseMerge**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasemergea) function and the **Merge** method of the [**Database**](database-object.md) object cannot be used to merge a module included within an installation package.</span></span> <span data-ttu-id="7c759-115">Sie sollten nicht zum Zusammenführen von [Mergemodulen](merge-modules.md) in einem Windows Installer Paket verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7c759-115">They should not be used to merge [Merge Modules](merge-modules.md) into a Windows Installer package.</span></span> <span data-ttu-id="7c759-116">Wenn Sie ein Mergemodul in ein Installationspaket einschließen möchten, sollten Autoren von Installationspaketen den Richtlinien folgen, die im Thema [Anwenden von Mergemodulen](applying-merge-modules.md) beschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="7c759-116">To include a merge module in an installation package, authors of installation packages should follow the guidelines that are described in the [Applying Merge Modules](applying-merge-modules.md) topic.</span></span>

<span data-ttu-id="7c759-117">Die **Merge** -Methode kopiert keine eingebetteten CAB- [Dateien](cabinet-files.md) oder [eingebetteten Transformationen](embedded-transforms.md) aus der Verweis Datenbank in die Zieldatenbank.</span><span class="sxs-lookup"><span data-stu-id="7c759-117">The **Merge** method does not copy over embedded [cabinet files](cabinet-files.md) or [embedded transforms](embedded-transforms.md) from the reference database into the target database.</span></span> <span data-ttu-id="7c759-118">Eingebettete Datenströme, die in der [binären Tabelle](binary-table.md) oder in der [Symboltabelle](icon-table.md) aufgeführt sind, werden aus der Verweis Datenbank in die Zieldatenbank kopiert.</span><span class="sxs-lookup"><span data-stu-id="7c759-118">Embedded data streams that are listed in the [Binary Table](binary-table.md) or [Icon Table](icon-table.md) are copied from the reference database to the target database.</span></span> <span data-ttu-id="7c759-119">In die Verweis Datenbank eingebettete Storages werden nicht in die Zieldatenbank kopiert.</span><span class="sxs-lookup"><span data-stu-id="7c759-119">Storages embedded in the reference database are not copied to the target database.</span></span>

<span data-ttu-id="7c759-120">Wenn keine Tabelle angegeben wird, gibt die allgemeine Fehlermeldung die Anzahl der Tabellen mit Mergekonflikten an.</span><span class="sxs-lookup"><span data-stu-id="7c759-120">If no table is provided, the general error message provides the number of tables containing merge conflicts.</span></span> <span data-ttu-id="7c759-121">Eine beliebige Tabelle kann zwar übermittelt werden, aber alle anderen Spalten müssen NULL-Werte zulassen, da der Vorgang zum Aktualisieren der [Fehler Tabelle](error-table.md) fehlschlägt, wenn eine Spalte keine NULL-Werte zulässt.</span><span class="sxs-lookup"><span data-stu-id="7c759-121">Any table can be passed in, but all other columns must be nullable because the operation to update the [Error Table](error-table.md) fails if a column is not nullable.</span></span> <span data-ttu-id="7c759-122">Eine neu erstellte Tabelle kann ebenfalls übermittelt werden, da die **Merge** -Methode automatisch die Spalten erstellt, die Sie verwendet, wenn Mergekonflikte gefunden werden.</span><span class="sxs-lookup"><span data-stu-id="7c759-122">A newly created table can be passed in as well because the **Merge** method automatically creates the columns it uses if merge conflicts are found.</span></span> <span data-ttu-id="7c759-123">Zum Darstellen von Mergekonflikten werden zwei Spalten verwendet.</span><span class="sxs-lookup"><span data-stu-id="7c759-123">Two columns are used to present merge conflicts.</span></span> <span data-ttu-id="7c759-124">Die erste Spalte ist der Tabellenname und die Primärschlüssel Spalte.</span><span class="sxs-lookup"><span data-stu-id="7c759-124">The first column is the table name and the primary key column.</span></span> <span data-ttu-id="7c759-125">Die zweite Spalte gibt die Anzahl der Zeilen in der Tabelle an, die Mergefehler aufweisen.</span><span class="sxs-lookup"><span data-stu-id="7c759-125">The second column is the number of rows of that table that have merge failures.</span></span>

<span data-ttu-id="7c759-126">Wenn Tabellen mit demselben Namen in beiden Datenbanken nicht mit der Anzahl der Primärschlüssel, den Spaltentypen, der Spalten Anzahl oder den Spaltennamen übereinstimmen, schlägt die **Merge** -Methode fehl und gibt eine Fehlermeldung an, die angibt, was aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="7c759-126">If tables of the same name in both databases do not match in the number of primary keys, the column types, the number of columns, or the column names, the **Merge** method fails and posts an error message stating what occurred.</span></span>

<span data-ttu-id="7c759-127">Damit die Fehler Tabelle beibehalten wird, muss der Fehlerhandler die Datenbank, zu der die Fehler Tabelle gehört, ein Commit für die Datenbank durchsetzen.</span><span class="sxs-lookup"><span data-stu-id="7c759-127">For the Error table to remain, the error handler must commit the database to which the Error table belongs.</span></span> <span data-ttu-id="7c759-128">Allerdings sollte dieser Commit ausgeführt werden, nachdem die dritte Spalte verwendet wurde, um die Verweise auf Tabellen zu erhalten, in denen Mergekonflikte aufgetreten sind.</span><span class="sxs-lookup"><span data-stu-id="7c759-128">However, this commit should be done after using the third column to obtain the references to those tables where merge conflicts occurred.</span></span>

<span data-ttu-id="7c759-129">Wenn die Methode fehlschlägt, können Sie erweiterte Fehlerinformationen mithilfe der [**lasterrorrecord**](installer-lasterrorrecord.md) -Methode abrufen.</span><span class="sxs-lookup"><span data-stu-id="7c759-129">If the method fails, you can obtain extended error information by using the [**LastErrorRecord**](installer-lasterrorrecord.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="7c759-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7c759-130">Requirements</span></span>



| <span data-ttu-id="7c759-131">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7c759-131">Requirement</span></span> | <span data-ttu-id="7c759-132">Wert</span><span class="sxs-lookup"><span data-stu-id="7c759-132">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7c759-133">Version</span><span class="sxs-lookup"><span data-stu-id="7c759-133">Version</span></span><br/> | <span data-ttu-id="7c759-134">Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7.</span><span class="sxs-lookup"><span data-stu-id="7c759-134">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="7c759-135">Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="7c759-135">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="7c759-136">Windows Installer unter Windows Server 2003 oder Windows XP</span><span class="sxs-lookup"><span data-stu-id="7c759-136">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="7c759-137">DLL</span><span class="sxs-lookup"><span data-stu-id="7c759-137">DLL</span></span><br/>     | <dl> <span data-ttu-id="7c759-138"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7c759-138"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="7c759-139">IID</span><span class="sxs-lookup"><span data-stu-id="7c759-139">IID</span></span><br/>     | <span data-ttu-id="7c759-140">IID \_ idatabase ist definiert als 000c109d-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="7c759-140">IID\_IDatabase is defined as 000C109D-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                            |



 

 




