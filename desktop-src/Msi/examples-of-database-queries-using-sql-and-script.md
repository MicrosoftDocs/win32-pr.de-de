---
description: Ein Beispiel für die Verwendung von Skript gesteuerten Datenbankabfragen finden Sie im Windows Installer Software Development Kit (SDK) als Dienst WiRunSQL.vbs.
ms.assetid: aa38dbe5-411d-432e-b3fe-09994fc59c75
title: Beispiele für Datenbankabfragen mit SQL und Skript
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bbd839151b40ddd5e9a265c6c370c27a4a9fd125
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103755625"
---
# <a name="examples-of-database-queries-using-sql-and-script"></a><span data-ttu-id="8fc50-103">Beispiele für Datenbankabfragen mit SQL und Skript</span><span class="sxs-lookup"><span data-stu-id="8fc50-103">Examples of Database Queries Using SQL and Script</span></span>

<span data-ttu-id="8fc50-104">Ein Beispiel für die Verwendung von Skript gesteuerten Datenbankabfragen finden Sie im Windows [Installer Software Development Kit](platform-sdk-components-for-windows-installer-developers.md) (SDK) als Dienstprogramm WiRunSQL.vbs.</span><span class="sxs-lookup"><span data-stu-id="8fc50-104">An example of using script-driven database queries is provided in the Windows [Installer Software Development Kit](platform-sdk-components-for-windows-installer-developers.md) (SDK) as the utility WiRunSQL.vbs.</span></span> <span data-ttu-id="8fc50-105">Dieses Hilfsprogramm verarbeitet Datenbankabfragen mithilfe der Windows Installer SQL-Version, die im Abschnitt [SQL-Syntax](sql-syntax.md)beschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="8fc50-105">This utility handles database queries using the Windows Installer version of SQL described in the section [SQL Syntax](sql-syntax.md).</span></span>

<span data-ttu-id="8fc50-106">**Löschen eines Datensatzes aus einer Tabelle**</span><span class="sxs-lookup"><span data-stu-id="8fc50-106">**Delete a record from a table**</span></span>

<span data-ttu-id="8fc50-107">Mit der folgenden Befehlszeile wird der Datensatz mit dem Primärschlüssel aus der [Funktions](feature-table.md) Tabelle der Test.msi Datenbank gelöscht.</span><span class="sxs-lookup"><span data-stu-id="8fc50-107">The following command line deletes the record having the primary key RED from the [Feature](feature-table.md) table of the Test.msi database.</span></span>

<span data-ttu-id="8fc50-108">**Cscript WiRunSQL.vbs Test.msi "DELETE FROM \` Feature \` \` \` . \` Feature \` = ' red ' "**</span><span class="sxs-lookup"><span data-stu-id="8fc50-108">**Cscript WiRunSQL.vbs Test.msi "DELETE FROM \`Feature\` WHERE \`Feature\`.\`Feature\`='RED'"**</span></span>

<span data-ttu-id="8fc50-109">**Hinzufügen einer Tabelle zu einer Datenbank**</span><span class="sxs-lookup"><span data-stu-id="8fc50-109">**Add a table to a database**</span></span>

<span data-ttu-id="8fc50-110">Mit der folgenden Befehlszeile wird die [Verzeichnis](directory-table.md) Tabelle der Test.msi Datenbank hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="8fc50-110">The following command line adds the [Directory](directory-table.md) table to the Test.msi database.</span></span>

<span data-ttu-id="8fc50-111">**Cscript-WiRunSQL.vbs Test.msi "Create Table \` Directory \` ( \` Verzeichnis \` char (72) nicht NULL, \` Verzeichnis \_ Parent \` char (72), \` DefaultDir \` char (255) NOT NULL localisierbares Primärschlüssel \` Verzeichnis \` )"**</span><span class="sxs-lookup"><span data-stu-id="8fc50-111">**CScript WiRunSQL.vbs Test.msi "CREATE TABLE \`Directory\` (\`Directory\` CHAR(72) NOT NULL, \`Directory\_Parent\` CHAR(72), \`DefaultDir\` CHAR(255) NOT NULL LOCALIZABLE PRIMARY KEY \`Directory\`)"**</span></span>

<span data-ttu-id="8fc50-112">**Entfernen einer Tabelle aus einer Datenbank**</span><span class="sxs-lookup"><span data-stu-id="8fc50-112">**Remove a table from a database**</span></span>

<span data-ttu-id="8fc50-113">Mit der folgenden Befehlszeile wird die [Funktions](feature-table.md) Tabelle aus der Test.msi-Datenbank entfernt.</span><span class="sxs-lookup"><span data-stu-id="8fc50-113">The following command line removes the [Feature](feature-table.md) table from the Test.msi database.</span></span>

<span data-ttu-id="8fc50-114">**Cscript-WiRunSQL.vbs Test.msi "Drop Table- \` Funktion \` "**</span><span class="sxs-lookup"><span data-stu-id="8fc50-114">**Cscript WiRunSQL.vbs Test.msi "DROP TABLE \`Feature\`"**</span></span>

<span data-ttu-id="8fc50-115">**Hinzufügen einer neuen Spalte zu einer Tabelle**</span><span class="sxs-lookup"><span data-stu-id="8fc50-115">**Add a new column to a table**</span></span>

<span data-ttu-id="8fc50-116">Mit der folgenden Befehlszeile wird die Test Spalte der Tabelle " [CustomAction](customaction-table.md) " der Test.msi Datenbank hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="8fc50-116">The following command line adds the Test column to the [CustomAction](customaction-table.md) table of the Test.msi database.</span></span>

<span data-ttu-id="8fc50-117">**Cscript-WiRunSQL.vbs Test.msi "alter Table \` CustomAction \` Add \` Test \` Integer"**</span><span class="sxs-lookup"><span data-stu-id="8fc50-117">**CScript WiRunSQL.vbs Test.msi "ALTER TABLE \`CustomAction\` ADD \`Test\` INTEGER"**</span></span>

<span data-ttu-id="8fc50-118">**Einfügen eines neuen Datensatzes in eine Tabelle**</span><span class="sxs-lookup"><span data-stu-id="8fc50-118">**Insert a new record into a table**</span></span>

<span data-ttu-id="8fc50-119">Mit der folgenden Befehlszeile wird ein neuer Datensatz in die [Funktions](feature-table.md) Tabelle der Test.msi-Datenbank eingefügt.</span><span class="sxs-lookup"><span data-stu-id="8fc50-119">The following command line inserts a new record into the [Feature](feature-table.md) table of the Test.msi database.</span></span>

<span data-ttu-id="8fc50-120">**Cscript WiRunSQL.vbs Test.msi "INSERT INTO- \` Funktion \` ( \` Feature \` . \` Feature \` , \` Feature \` . \` Über \_ geordnetes Element \` , \` Feature \` . \` Titel \` , \` Feature \` . \` Beschreibung \` , \` Feature \` . \` Anzeigen \` , \` Feature \` . \` Ebene \` , \` Funktion \` . \` Verzeichnis \_ \` , \` Feature \` . \` Attribute \` ) Werte ("Tennis", "Sport", "Tennis", "Turnier", 25, 3, "sportdir", 2) "**</span><span class="sxs-lookup"><span data-stu-id="8fc50-120">**Cscript WiRunSQL.vbs Test.msi "INSERT INTO \`Feature\` (\`Feature\`.\`Feature\`,\`Feature\`.\`Feature\_Parent\`,\`Feature\`.\`Title\`,\`Feature\`.\`Description\`, \`Feature\`.\`Display\`,\`Feature\`.\`Level\`,\`Feature\`.\`Directory\_\`,\`Feature\`.\`Attributes\`) VALUES ('Tennis','Sport','Tennis','Tournament',25,3,'SPORTDIR',2)"**</span></span>

<span data-ttu-id="8fc50-121">Dadurch wird der folgende Datensatz in die [Featuretabelle Test.msi](feature-table.md) eingefügt.</span><span class="sxs-lookup"><span data-stu-id="8fc50-121">This inserts the following record into the [Feature](feature-table.md) table of Test.msi.</span></span>

<span data-ttu-id="8fc50-122">[Feature](feature-table.md) Glaub</span><span class="sxs-lookup"><span data-stu-id="8fc50-122">[Feature](feature-table.md) Table</span></span>



| <span data-ttu-id="8fc50-123">Funktion</span><span class="sxs-lookup"><span data-stu-id="8fc50-123">Feature</span></span> | <span data-ttu-id="8fc50-124">Über \_ geordnetes Element</span><span class="sxs-lookup"><span data-stu-id="8fc50-124">Feature\_Parent</span></span> | <span data-ttu-id="8fc50-125">Titel</span><span class="sxs-lookup"><span data-stu-id="8fc50-125">Title</span></span>  | <span data-ttu-id="8fc50-126">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8fc50-126">Description</span></span> | <span data-ttu-id="8fc50-127">Anzeige</span><span class="sxs-lookup"><span data-stu-id="8fc50-127">Display</span></span> | <span data-ttu-id="8fc50-128">Ebene</span><span class="sxs-lookup"><span data-stu-id="8fc50-128">Level</span></span> | <span data-ttu-id="8fc50-129">Verzeichnis\_</span><span class="sxs-lookup"><span data-stu-id="8fc50-129">Directory\_</span></span> | <span data-ttu-id="8fc50-130">Attribute</span><span class="sxs-lookup"><span data-stu-id="8fc50-130">Attributes</span></span> |
|---------|-----------------|--------|-------------|---------|-------|-------------|------------|
| <span data-ttu-id="8fc50-131">Tennis</span><span class="sxs-lookup"><span data-stu-id="8fc50-131">Tennis</span></span>  | <span data-ttu-id="8fc50-132">Sport</span><span class="sxs-lookup"><span data-stu-id="8fc50-132">Sport</span></span>           | <span data-ttu-id="8fc50-133">Tennis</span><span class="sxs-lookup"><span data-stu-id="8fc50-133">Tennis</span></span> | <span data-ttu-id="8fc50-134">Turnier</span><span class="sxs-lookup"><span data-stu-id="8fc50-134">Tournament</span></span>  | <span data-ttu-id="8fc50-135">25</span><span class="sxs-lookup"><span data-stu-id="8fc50-135">25</span></span>      | <span data-ttu-id="8fc50-136">3</span><span class="sxs-lookup"><span data-stu-id="8fc50-136">3</span></span>     | <span data-ttu-id="8fc50-137">Sportdir</span><span class="sxs-lookup"><span data-stu-id="8fc50-137">SPORTDIR</span></span>    | <span data-ttu-id="8fc50-138">2</span><span class="sxs-lookup"><span data-stu-id="8fc50-138">2</span></span>          |



 

<span data-ttu-id="8fc50-139">Beachten Sie, dass Binärdaten nicht direkt mithilfe der INSERT INTO-oder Update SQL-Abfragen in eine Tabelle eingefügt werden können.</span><span class="sxs-lookup"><span data-stu-id="8fc50-139">Note that binary data cannot be inserted into a table directly using the INSERT INTO or UPDATE SQL queries.</span></span> <span data-ttu-id="8fc50-140">Weitere Informationen finden [Sie unter Hinzufügen von Binärdaten zu einer Tabelle mithilfe von SQL](adding-binary-data-to-a-table-using-sql.md).</span><span class="sxs-lookup"><span data-stu-id="8fc50-140">For information see [Adding Binary Data to a Table Using SQL](adding-binary-data-to-a-table-using-sql.md).</span></span>

<span data-ttu-id="8fc50-141">**Ändern eines vorhandenen Datensatzes in einer Tabelle**</span><span class="sxs-lookup"><span data-stu-id="8fc50-141">**Modify an existing record in a table**</span></span>

<span data-ttu-id="8fc50-142">Mit der folgenden Befehlszeile wird der vorhandene Wert im Feld "Title" in "Performance" geändert.</span><span class="sxs-lookup"><span data-stu-id="8fc50-142">The following command line changes the existing value in the Title field to "Performances."</span></span> <span data-ttu-id="8fc50-143">Der aktualisierte Datensatz weist "Arts" als Primärschlüssel auf und befindet sich in der Featuretabelle der Test.msi Datenbank.</span><span class="sxs-lookup"><span data-stu-id="8fc50-143">The updated record has "Arts" as its primary key and is in the Feature table of the Test.msi database.</span></span>

<span data-ttu-id="8fc50-144">**Cscript-WiRunSQL.vbs Test.msi Feature "Featuresatz aktualisieren" \` \` \` \` . \` Title \` = ' Performance ' in der \` Funktion \` . \` Feature \` = ' Arts '**</span><span class="sxs-lookup"><span data-stu-id="8fc50-144">**Cscript WiRunSQL.vbs Test.msi "UPDATE \`Feature\` SET \`Feature\`.\`Title\`='Performances' WHERE \`Feature\`.\`Feature\`='Arts'"**</span></span>

<span data-ttu-id="8fc50-145">**Gruppe von Datensätzen auswählen**</span><span class="sxs-lookup"><span data-stu-id="8fc50-145">**Select a group of records**</span></span>

<span data-ttu-id="8fc50-146">Die folgende Befehlszeile wählt den Namen und den Typ aller Steuerelemente aus, die zum ErrorDialog in der Test.msi-Datenbank gehören.</span><span class="sxs-lookup"><span data-stu-id="8fc50-146">The following command line selects the name and type of all controls that belong to the ErrorDialog in the Test.msi database.</span></span>

<span data-ttu-id="8fc50-147">**Cscript-WiRunSQL.vbs Test.msi "Select- \` Steuerelement \` , \` Typ \` von \` Control \` Where \` Dialog \_ \` = ' ErrorDialog '"**</span><span class="sxs-lookup"><span data-stu-id="8fc50-147">**CScript WiRunSQL.vbs Test.msi "SELECT \`Control\`, \`Type\` FROM \`Control\` WHERE \`Dialog\_\`='ErrorDialog' "**</span></span>

<span data-ttu-id="8fc50-148">**Speichern einer Tabelle im Arbeitsspeicher**</span><span class="sxs-lookup"><span data-stu-id="8fc50-148">**Hold a table in memory**</span></span>

<span data-ttu-id="8fc50-149">Die folgende Befehlszeile sperrt die [Komponenten](component-table.md) Tabelle der Test.msi-Datenbank im Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="8fc50-149">The following command line locks the [Component](component-table.md) table of the Test.msi database in memory.</span></span>

<span data-ttu-id="8fc50-150">**Cscript-WiRunSQL.vbs Test.msi "alter Table \` Component \` Hold"**</span><span class="sxs-lookup"><span data-stu-id="8fc50-150">**CScript WiRunSQL.vbs Test.msi "ALTER TABLE \`Component\` HOLD"**</span></span>

<span data-ttu-id="8fc50-151">**Freigeben einer Tabelle im Arbeitsspeicher**</span><span class="sxs-lookup"><span data-stu-id="8fc50-151">**Free a table in memory**</span></span>

<span data-ttu-id="8fc50-152">Mit der folgenden Befehlszeile wird die [Komponenten](component-table.md) Tabelle der Test.msi Datenbank aus dem Arbeitsspeicher freigegeben.</span><span class="sxs-lookup"><span data-stu-id="8fc50-152">The following command line frees the [Component](component-table.md) table of the Test.msi database from memory.</span></span>

<span data-ttu-id="8fc50-153">**Cscript-WiRunSQL.vbs Test.msi "alter Table \` Component \` Free"**</span><span class="sxs-lookup"><span data-stu-id="8fc50-153">**CScript WiRunSQL.vbs Test.msi "ALTER TABLE \`Component\` FREE"**</span></span>

 

 



