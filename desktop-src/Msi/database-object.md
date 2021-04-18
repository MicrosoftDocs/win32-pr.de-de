---
description: Das Datenbankobjekt greift auf eine Installerdatenbank zu.
ms.assetid: 97765884-3e1c-486a-932c-6430b113fac8
title: Datenbankobjekt
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Database
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 5b47e4678d9475abe90c4b55d6adb514314dcc0e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364468"
---
# <a name="database-object"></a><span data-ttu-id="0a8f4-103">Datenbankobjekt</span><span class="sxs-lookup"><span data-stu-id="0a8f4-103">Database object</span></span>

<span data-ttu-id="0a8f4-104">Das **Daten Bank** Objekt greift auf eine Installerdatenbank zu.</span><span class="sxs-lookup"><span data-stu-id="0a8f4-104">The **Database** object accesses an installer database.</span></span>

<span data-ttu-id="0a8f4-105">Das **Daten Bank** Objekt wird freigegeben, wenn es entweder außerhalb des gültigen Bereichs liegt oder wenn die zugeordnete Objekt Variable auf NULL festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="0a8f4-105">The **Database** object is released when it is either taken out of scope or when the object variable associated with it is set to null.</span></span> <span data-ttu-id="0a8f4-106">Die [**Commit**](database-commit.md) -Methode muss aufgerufen werden, bevor das **Database** -Objekt freigegeben wird, um alle persistenten Änderungen zu schreiben.</span><span class="sxs-lookup"><span data-stu-id="0a8f4-106">The [**Commit**](database-commit.md) method must be called before the **Database** object is released to write out all persistent changes.</span></span> <span data-ttu-id="0a8f4-107">Wenn die **Commit** -Methode nicht aufgerufen wird, führt das Installationsprogramm bei der Objekt Zerstörung ein implizites ROLLBACK durch.</span><span class="sxs-lookup"><span data-stu-id="0a8f4-107">If the **Commit** method is not called, the installer performs an implicit rollback upon object destruction.</span></span>

<span data-ttu-id="0a8f4-108">Der-Client kann das folgende Verfahren für den Datenzugriff verwenden.</span><span class="sxs-lookup"><span data-stu-id="0a8f4-108">The client can use the following procedure for data access.</span></span>

<span data-ttu-id="0a8f4-109">**Abfragen der API-Sequenzierung**</span><span class="sxs-lookup"><span data-stu-id="0a8f4-109">**To Query API Sequencing**</span></span>

1.  <span data-ttu-id="0a8f4-110">Rufen Sie ein **Daten Bank** Objekt ab, indem Sie [**OpenDatabase**](installer-opendatabase.md) oder das [**Installer**](installer-object.md) -Objekt aufrufen.</span><span class="sxs-lookup"><span data-stu-id="0a8f4-110">Obtain a **Database** object by calling the [**OpenDatabase**](installer-opendatabase.md) or the [**Installer**](installer-object.md) object.</span></span>
2.  <span data-ttu-id="0a8f4-111">Initiieren Sie eine Abfrage mithilfe einer SQL-Zeichenfolge, indem Sie die [**OpenView**](database-openview.md) -Methode des **Daten Bank** Objekts aufrufen.</span><span class="sxs-lookup"><span data-stu-id="0a8f4-111">Initiate a query using a SQL string by calling the [**OpenView**](database-openview.md) method of the **Database** object.</span></span>
3.  <span data-ttu-id="0a8f4-112">Legen Sie Abfrage Parameter in einem [**Datensatz**](record-object.md) -Objekt fest, und führen Sie die Datenbankabfrage durch Aufrufen der [**Execute**](view-execute.md) -Methode des [**View**](view-object.md) -Objekts aus.</span><span class="sxs-lookup"><span data-stu-id="0a8f4-112">Set query parameters in a [**Record**](record-object.md) object and execute the database query by calling the [**Execute**](view-execute.md) method of the [**View**](view-object.md) object.</span></span> <span data-ttu-id="0a8f4-113">Dies erzeugt ein Ergebnis, das abgerufen oder aktualisiert werden kann.</span><span class="sxs-lookup"><span data-stu-id="0a8f4-113">This produces a result that can be fetched or updated.</span></span>
4.  <span data-ttu-id="0a8f4-114">Rufen Sie die [**Fetch**](view-fetch.md) -Methode des [**View**](view-object.md) -Objekts wiederholt auf, um [**Daten Satz**](record-object.md) Objekte zurückzugeben</span><span class="sxs-lookup"><span data-stu-id="0a8f4-114">Call the [**Fetch**](view-fetch.md) method of the [**View**](view-object.md) object repeatedly to return [**Record**](record-object.md) objects.</span></span>
5.  <span data-ttu-id="0a8f4-115">Aktualisieren von Daten Bank Zeilen eines [**Datensatz**](record-object.md) -Objekts, das von der [**Fetch**](view-fetch.md) -Methode abgerufen wurde, mithilfe der [**Modify**](view-modify.md) -Methode des [**View**](view-object.md) -Objekts.</span><span class="sxs-lookup"><span data-stu-id="0a8f4-115">Update database rows of a [**Record**](record-object.md) object obtained by the [**Fetch**](view-fetch.md) method using the [**Modify**](view-modify.md) method of the [**View**](view-object.md) object.</span></span>
6.  <span data-ttu-id="0a8f4-116">Geben Sie die Abfrage und alle nicht abgerufenen Datensätze durch Aufrufen der [**Close**](view-close.md) -Methode des [**View**](view-object.md) -Objekts frei.</span><span class="sxs-lookup"><span data-stu-id="0a8f4-116">Release the query and any unfetched records by calling the [**Close**](view-close.md) method of the [**View**](view-object.md) object.</span></span>
7.  <span data-ttu-id="0a8f4-117">Speichern Sie alle Datenbankupdates, indem Sie die [**Commit**](database-commit.md) -Methode des **Daten Bank** Objekts aufrufen.</span><span class="sxs-lookup"><span data-stu-id="0a8f4-117">Persist any database updates by calling the [**Commit**](database-commit.md) method of the **Database** object.</span></span>

## <a name="members"></a><span data-ttu-id="0a8f4-118">Member</span><span class="sxs-lookup"><span data-stu-id="0a8f4-118">Members</span></span>

<span data-ttu-id="0a8f4-119">Das **Daten Bank** Objekt verfügt über folgende Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="0a8f4-119">The **Database** object has these types of members:</span></span>

-   [<span data-ttu-id="0a8f4-120">Methoden</span><span class="sxs-lookup"><span data-stu-id="0a8f4-120">Methods</span></span>](#methods)
-   [<span data-ttu-id="0a8f4-121">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="0a8f4-121">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="0a8f4-122">Methoden</span><span class="sxs-lookup"><span data-stu-id="0a8f4-122">Methods</span></span>

<span data-ttu-id="0a8f4-123">Das **Daten Bank** Objekt verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="0a8f4-123">The **Database** object has these methods.</span></span>



| <span data-ttu-id="0a8f4-124">Methode</span><span class="sxs-lookup"><span data-stu-id="0a8f4-124">Method</span></span>                                                                    | <span data-ttu-id="0a8f4-125">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0a8f4-125">Description</span></span>                                                                                                                                                               |
|:--------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0a8f4-126">**Applytransform**</span><span class="sxs-lookup"><span data-stu-id="0a8f4-126">**ApplyTransform**</span></span>](database-applytransform.md)                         | <span data-ttu-id="0a8f4-127">Wendet die Transformation auf diese Datenbank an.</span><span class="sxs-lookup"><span data-stu-id="0a8f4-127">Applies the transform to this database.</span></span><br/>                                                                                                                        |
| [<span data-ttu-id="0a8f4-128">**Einzusetzen**</span><span class="sxs-lookup"><span data-stu-id="0a8f4-128">**Commit**</span></span>](database-commit.md)                                         | <span data-ttu-id="0a8f4-129">Schließt die persistente Form der Datenbank ab.</span><span class="sxs-lookup"><span data-stu-id="0a8f4-129">Finalizes the persistent form of the database.</span></span><br/>                                                                                                                 |
| [<span data-ttu-id="0a8f4-130">**"Kreatetransformsummaryinfo"**</span><span class="sxs-lookup"><span data-stu-id="0a8f4-130">**CreateTransformSummaryInfo**</span></span>](database-createtransformsummaryinfo.md) | <span data-ttu-id="0a8f4-131">Erstellt den Zusammenfassungs Informationsdaten Strom einer vorhandenen Transformations Datei und füllt ihn auf.</span><span class="sxs-lookup"><span data-stu-id="0a8f4-131">Creates and populates the summary information stream of an existing transform file.</span></span><br/>                                                                            |
| [<span data-ttu-id="0a8f4-132">**Enableuipreview**</span><span class="sxs-lookup"><span data-stu-id="0a8f4-132">**EnableUIPreview**</span></span>](database-enableuipreview.md)                       | <span data-ttu-id="0a8f4-133">Erleichtert das Erstellen von Dialogfeldern und-Plakaten durch Bereitstellen der Unterstützung, die zum Anzeigen der in der Installer-Datenbank gespeicherten Dialogfelder für Benutzeroberflächen erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="0a8f4-133">Facilitates the authoring of dialog boxes and billboards by providing the support needed to view user interface dialog boxes stored in the installer database.</span></span><br/> |
| [<span data-ttu-id="0a8f4-134">**Exportieren**</span><span class="sxs-lookup"><span data-stu-id="0a8f4-134">**Export**</span></span>](database-export.md)                                         | <span data-ttu-id="0a8f4-135">Kopiert die Struktur und die Daten aus einer angegebenen Tabelle in eine Textarchiv Datei.</span><span class="sxs-lookup"><span data-stu-id="0a8f4-135">Copies the structure and data from a specified table to a text archive file.</span></span><br/>                                                                                   |
| [<span data-ttu-id="0a8f4-136">**Gene Rate Transform**</span><span class="sxs-lookup"><span data-stu-id="0a8f4-136">**GenerateTransform**</span></span>](database-generatetransform.md)                   | <span data-ttu-id="0a8f4-137">Erstellt eine Transformation.</span><span class="sxs-lookup"><span data-stu-id="0a8f4-137">Creates a transform.</span></span><br/>                                                                                                                                           |
| [<span data-ttu-id="0a8f4-138">**Importieren**</span><span class="sxs-lookup"><span data-stu-id="0a8f4-138">**Import**</span></span>](database-import.md)                                         | <span data-ttu-id="0a8f4-139">Importiert eine Datenbanktabelle aus einer Textarchiv Datei.</span><span class="sxs-lookup"><span data-stu-id="0a8f4-139">Imports a database table from a text archive file.</span></span><br/>                                                                                                             |
| [<span data-ttu-id="0a8f4-140">**Merge**</span><span class="sxs-lookup"><span data-stu-id="0a8f4-140">**Merge**</span></span>](database-merge.md)                                           | <span data-ttu-id="0a8f4-141">Führt die Verweis Datenbank mit der Basisdatenbank zusammen.</span><span class="sxs-lookup"><span data-stu-id="0a8f4-141">Merges the reference database with the base database.</span></span><br/>                                                                                                          |
| [<span data-ttu-id="0a8f4-142">**OpenView –**</span><span class="sxs-lookup"><span data-stu-id="0a8f4-142">**OpenView**</span></span>](database-openview.md)                                     | <span data-ttu-id="0a8f4-143">Gibt ein [**Ansichts**](view-object.md) Objekt zurück, das die von einer SQL-Zeichenfolge angegebene Abfrage darstellt.</span><span class="sxs-lookup"><span data-stu-id="0a8f4-143">Returns a [**View**](view-object.md) object representing the query specified by a SQL string.</span></span><br/>                                                                 |



 

### <a name="properties"></a><span data-ttu-id="0a8f4-144">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="0a8f4-144">Properties</span></span>

<span data-ttu-id="0a8f4-145">Das **Daten Bank** Objekt verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="0a8f4-145">The **Database** object has these properties.</span></span>



| <span data-ttu-id="0a8f4-146">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="0a8f4-146">Property</span></span>                                                                               | <span data-ttu-id="0a8f4-147">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0a8f4-147">Description</span></span>                                                                                                                                                      |
|:---------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0a8f4-148">**Databasestate**</span><span class="sxs-lookup"><span data-stu-id="0a8f4-148">**DatabaseState**</span></span>](database-databasestate.md)<br/>                             | <span data-ttu-id="0a8f4-149">Gibt den persistenzstatus der Datenbank zurück.</span><span class="sxs-lookup"><span data-stu-id="0a8f4-149">Returns the persistence state of the database.</span></span><br/>                                                                                                        |
| [<span data-ttu-id="0a8f4-150">**PrimaryKeys**</span><span class="sxs-lookup"><span data-stu-id="0a8f4-150">**PrimaryKeys**</span></span>](database-primarykeys.md)<br/>                                 | <span data-ttu-id="0a8f4-151">Gibt ein [**Daten Satz**](record-object.md) Objekt zurück, das den Tabellennamen und die Spaltennamen (die die Primärschlüssel umfasst) enthält.</span><span class="sxs-lookup"><span data-stu-id="0a8f4-151">Returns a [**Record**](record-object.md) object containing the table name and the column names (comprising the primary keys).</span></span><br/>                        |
| [<span data-ttu-id="0a8f4-152">**SummaryInformation (Datenbankobjekt)**</span><span class="sxs-lookup"><span data-stu-id="0a8f4-152">**SummaryInformation (Database Object)**</span></span>](database-summaryinformation.md)<br/> | <span data-ttu-id="0a8f4-153">Gibt ein [**SummaryInfo**](summaryinfo-object.md) -Objekt zurück, das zum Überprüfen, aktualisieren und Hinzufügen von Eigenschaften zum Zusammenfassungs Informationsdaten Strom verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="0a8f4-153">Returns a [**SummaryInfo**](summaryinfo-object.md) object that can be used to examine, update, and add properties to the summary information stream.</span></span><br/> |
| [<span data-ttu-id="0a8f4-154">**Tablepersistent**</span><span class="sxs-lookup"><span data-stu-id="0a8f4-154">**TablePersistent**</span></span>](database-tablepersistent.md)<br/>                         | <span data-ttu-id="0a8f4-155">Gibt den persistenzstatus der Tabelle zurück.</span><span class="sxs-lookup"><span data-stu-id="0a8f4-155">Returns the persistence state of the table.</span></span><br/>                                                                                                           |



 

## <a name="requirements"></a><span data-ttu-id="0a8f4-156">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0a8f4-156">Requirements</span></span>



| <span data-ttu-id="0a8f4-157">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0a8f4-157">Requirement</span></span> | <span data-ttu-id="0a8f4-158">Wert</span><span class="sxs-lookup"><span data-stu-id="0a8f4-158">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0a8f4-159">Version</span><span class="sxs-lookup"><span data-stu-id="0a8f4-159">Version</span></span><br/> | <span data-ttu-id="0a8f4-160">Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7.</span><span class="sxs-lookup"><span data-stu-id="0a8f4-160">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="0a8f4-161">Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="0a8f4-161">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="0a8f4-162">Windows Installer unter Windows Server 2003 oder Windows XP</span><span class="sxs-lookup"><span data-stu-id="0a8f4-162">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="0a8f4-163">DLL</span><span class="sxs-lookup"><span data-stu-id="0a8f4-163">DLL</span></span><br/>     | <dl> <span data-ttu-id="0a8f4-164"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0a8f4-164"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="0a8f4-165">IID</span><span class="sxs-lookup"><span data-stu-id="0a8f4-165">IID</span></span><br/>     | <span data-ttu-id="0a8f4-166">IID \_ idatabase ist definiert als 000c109d-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="0a8f4-166">IID\_IDatabase is defined as 000C109D-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                            |



## <a name="see-also"></a><span data-ttu-id="0a8f4-167">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0a8f4-167">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0a8f4-168">Skript Beispiele für Windows Installer</span><span class="sxs-lookup"><span data-stu-id="0a8f4-168">Windows Installer Scripting Examples</span></span>](windows-installer-scripting-examples.md)
</dt> </dl>

 

 




