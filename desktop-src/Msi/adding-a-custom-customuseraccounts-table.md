---
description: Eine Spezifikation des Beispiels besteht darin, dass Benutzerkontoinformationen aus einer benutzerdefinierten Tabelle in der Installations Datenbank gelesen und nicht in die benutzerdefinierte Aktion hart codiert werden.
ms.assetid: 1545b4f1-3ccf-4745-90d8-15f1f79d8455
title: Hinzufügen einer benutzerdefinierten customuseraccounts-Tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d58366c725ecc135b9583c926a16383a5ad5a01
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106351639"
---
# <a name="adding-a-custom-customuseraccounts-table"></a><span data-ttu-id="d007d-103">Hinzufügen einer benutzerdefinierten customuseraccounts-Tabelle</span><span class="sxs-lookup"><span data-stu-id="d007d-103">Adding a Custom CustomUserAccounts Table</span></span>

<span data-ttu-id="d007d-104">Eine Spezifikation des Beispiels besteht darin, dass Benutzerkontoinformationen aus einer benutzerdefinierten Tabelle in der Installations Datenbank gelesen und nicht in die benutzerdefinierte Aktion hart codiert werden.</span><span class="sxs-lookup"><span data-stu-id="d007d-104">A specification of the sample is that user account information be read from a custom table in the installation database and not hard-coded into the custom action.</span></span>

<span data-ttu-id="d007d-105">Fügen Sie der Beispiel Installations Datenbank eine benutzerdefinierte Tabelle mit dem Namen customuseraccounts hinzu, um die Benutzerkontoinformationen zu speichern.</span><span class="sxs-lookup"><span data-stu-id="d007d-105">Add a custom table to the sample installation database named CustomUserAccounts to hold user account information.</span></span> <span data-ttu-id="d007d-106">Ein Beispiel für das Hinzufügen einer benutzerdefinierten Tabelle finden Sie unter [Beispiele für Datenbankabfragen mithilfe von SQL und Skript](examples-of-database-queries-using-sql-and-script.md) .</span><span class="sxs-lookup"><span data-stu-id="d007d-106">See [Examples of Database Queries Using SQL and Script](examples-of-database-queries-using-sql-and-script.md) for an example of how to add a custom table.</span></span> <span data-ttu-id="d007d-107">Verwenden Sie das folgende Schema für die customuseraccounts-Tabelle.</span><span class="sxs-lookup"><span data-stu-id="d007d-107">Use the following schema for the CustomUserAccounts table.</span></span> <span data-ttu-id="d007d-108">Eine Erläuterung der Spaltentypen finden Sie unter [Spalten Definitions Format](column-definition-format.md) .</span><span class="sxs-lookup"><span data-stu-id="d007d-108">See [Column Definition Format](column-definition-format.md) for an explanation of the column types.</span></span>



| <span data-ttu-id="d007d-109">Spalte</span><span class="sxs-lookup"><span data-stu-id="d007d-109">Column</span></span>     | <span data-ttu-id="d007d-110">Typ</span><span class="sxs-lookup"><span data-stu-id="d007d-110">Type</span></span> | <span data-ttu-id="d007d-111">Schlüssel</span><span class="sxs-lookup"><span data-stu-id="d007d-111">Key</span></span> | <span data-ttu-id="d007d-112">Nullwerte zulässig</span><span class="sxs-lookup"><span data-stu-id="d007d-112">Nullable</span></span> | <span data-ttu-id="d007d-113">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d007d-113">Description</span></span>                                                                                                                                                                                                                                                                                                |
|------------|------|-----|----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d007d-114">UserName</span><span class="sxs-lookup"><span data-stu-id="d007d-114">UserName</span></span>   | <span data-ttu-id="d007d-115">S72</span><span class="sxs-lookup"><span data-stu-id="d007d-115">s72</span></span>  | <span data-ttu-id="d007d-116">J</span><span class="sxs-lookup"><span data-stu-id="d007d-116">Y</span></span>   | <span data-ttu-id="d007d-117">N</span><span class="sxs-lookup"><span data-stu-id="d007d-117">N</span></span>        | <span data-ttu-id="d007d-118">Der Name des Benutzerkontos, das erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="d007d-118">Name of user account being created.</span></span>                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="d007d-119">Kennwort</span><span class="sxs-lookup"><span data-stu-id="d007d-119">Password</span></span>   | <span data-ttu-id="d007d-120">S72</span><span class="sxs-lookup"><span data-stu-id="d007d-120">s72</span></span>  |     | <span data-ttu-id="d007d-121">N</span><span class="sxs-lookup"><span data-stu-id="d007d-121">N</span></span>        | <span data-ttu-id="d007d-122">Name der Eigenschaft, die das Kennwort für das Konto enthält.</span><span class="sxs-lookup"><span data-stu-id="d007d-122">Name of property containing the password for the account.</span></span> <span data-ttu-id="d007d-123">Dabei handelt es sich um eine [öffentliche Eigenschaft](public-properties.md) , die in der Befehlszeile oder über ein [Bearbeitungs Steuer](edit-control.md) Element in der Benutzeroberfläche festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="d007d-123">This is a [public property](public-properties.md) set on the command line or through an [edit control](edit-control.md) in the user interface.</span></span> <span data-ttu-id="d007d-124">Dieses Bearbeitungs Steuerelement muss über das [Attribut "Password Control](password-control-attribute.md)" verfügen.</span><span class="sxs-lookup"><span data-stu-id="d007d-124">This edit control should have the [Password Control Attribute](password-control-attribute.md).</span></span> |
| <span data-ttu-id="d007d-125">Attribute</span><span class="sxs-lookup"><span data-stu-id="d007d-125">Attributes</span></span> | <span data-ttu-id="d007d-126">i4</span><span class="sxs-lookup"><span data-stu-id="d007d-126">i4</span></span>   |     | <span data-ttu-id="d007d-127">J</span><span class="sxs-lookup"><span data-stu-id="d007d-127">Y</span></span>        | <span data-ttu-id="d007d-128">Attribute für das Konto.</span><span class="sxs-lookup"><span data-stu-id="d007d-128">Attributes for account.</span></span> <span data-ttu-id="d007d-129">Diese werden als **DWORD** -Werte für den usri1 \_ Flags-Member der Struktur "User \_ Info 1" definiert \_ .</span><span class="sxs-lookup"><span data-stu-id="d007d-129">These are defined as the **DWORD** values for the usri1\_flags member of the USER\_INFO\_1 structure.</span></span>                                                                                                                                                                              |



 

<span data-ttu-id="d007d-130">Nachdem die Tabelle customuseraccounts der Datenbank hinzugefügt wurde, können Sie diese Tabelle mithilfe von Orca, einem Tabellen-Editor, der mit dem Windows Installer SDK bereitgestellt wird, oder einem anderen Editor bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="d007d-130">After the CustomUserAccounts table has been added to the database you may edit this table using Orca, a table editor provided with the Windows Installer SDK, or another editor.</span></span> <span data-ttu-id="d007d-131">Geben Sie den folgenden Datensatz in der Tabelle "customuseraccounts" ein, um ein Kenn Wort geschütztes Benutzerkonto für einen Benutzernamens "testuser" zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="d007d-131">Enter the following record in the CustomUserAccounts table to create a password secured user account for a user called TestUser.</span></span> <span data-ttu-id="d007d-132">Beachten Sie, dass 512 der numerische Wert für das Standardkonto "UF" ist \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="d007d-132">Note that 512 is the numeric value for UF\_NORMAL\_ACCOUNT.</span></span>

<span data-ttu-id="d007d-133">Tabelle "customuseraccounts"</span><span class="sxs-lookup"><span data-stu-id="d007d-133">CustomUserAccounts Table</span></span>



| <span data-ttu-id="d007d-134">UserName</span><span class="sxs-lookup"><span data-stu-id="d007d-134">UserName</span></span> | <span data-ttu-id="d007d-135">Kennwort</span><span class="sxs-lookup"><span data-stu-id="d007d-135">Password</span></span>         | <span data-ttu-id="d007d-136">Attribute</span><span class="sxs-lookup"><span data-stu-id="d007d-136">Attributes</span></span> |
|----------|------------------|------------|
| <span data-ttu-id="d007d-137">TestUser</span><span class="sxs-lookup"><span data-stu-id="d007d-137">TestUser</span></span> | <span data-ttu-id="d007d-138">Testuserpassword</span><span class="sxs-lookup"><span data-stu-id="d007d-138">TESTUSERPASSWORD</span></span> | <span data-ttu-id="d007d-139">512</span><span class="sxs-lookup"><span data-stu-id="d007d-139">512</span></span>        |



 

<span data-ttu-id="d007d-140">Fügen Sie der Überprüfungs \_ Tabelle für die benutzerdefinierte Tabelle die folgenden Datensätze hinzu.</span><span class="sxs-lookup"><span data-stu-id="d007d-140">Add the following records to the \_Validation table for the custom table.</span></span>

[<span data-ttu-id="d007d-141">\_Validierungs Tabelle</span><span class="sxs-lookup"><span data-stu-id="d007d-141">\_Validation Table</span></span>](-validation-table.md)



| <span data-ttu-id="d007d-142">Tabelle</span><span class="sxs-lookup"><span data-stu-id="d007d-142">Table</span></span>              | <span data-ttu-id="d007d-143">Spalte</span><span class="sxs-lookup"><span data-stu-id="d007d-143">Column</span></span>     | <span data-ttu-id="d007d-144">Nullwerte zulässig</span><span class="sxs-lookup"><span data-stu-id="d007d-144">Nullable</span></span> | <span data-ttu-id="d007d-145">MinValue</span><span class="sxs-lookup"><span data-stu-id="d007d-145">MinValue</span></span> | <span data-ttu-id="d007d-146">MaxValue</span><span class="sxs-lookup"><span data-stu-id="d007d-146">MaxValue</span></span>   | <span data-ttu-id="d007d-147">KeyTable</span><span class="sxs-lookup"><span data-stu-id="d007d-147">KeyTable</span></span> | <span data-ttu-id="d007d-148">KeyColumn</span><span class="sxs-lookup"><span data-stu-id="d007d-148">KeyColumn</span></span> | <span data-ttu-id="d007d-149">Category</span><span class="sxs-lookup"><span data-stu-id="d007d-149">Category</span></span>                     | <span data-ttu-id="d007d-150">Set</span><span class="sxs-lookup"><span data-stu-id="d007d-150">Set</span></span> | <span data-ttu-id="d007d-151">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d007d-151">Description</span></span> |
|--------------------|------------|----------|----------|------------|----------|-----------|------------------------------|-----|-------------|
| <span data-ttu-id="d007d-152">Customuseraccounts</span><span class="sxs-lookup"><span data-stu-id="d007d-152">CustomUserAccounts</span></span> | <span data-ttu-id="d007d-153">UserName</span><span class="sxs-lookup"><span data-stu-id="d007d-153">UserName</span></span>   | <span data-ttu-id="d007d-154">N</span><span class="sxs-lookup"><span data-stu-id="d007d-154">N</span></span>        |          |            |          |           | [<span data-ttu-id="d007d-155">Text</span><span class="sxs-lookup"><span data-stu-id="d007d-155">Text</span></span>](text.md)             |     |             |
| <span data-ttu-id="d007d-156">Customuseraccounts</span><span class="sxs-lookup"><span data-stu-id="d007d-156">CustomUserAccounts</span></span> | <span data-ttu-id="d007d-157">Kennwort</span><span class="sxs-lookup"><span data-stu-id="d007d-157">Password</span></span>   | <span data-ttu-id="d007d-158">N</span><span class="sxs-lookup"><span data-stu-id="d007d-158">N</span></span>        |          |            |          |           | [<span data-ttu-id="d007d-159">Bezeichner</span><span class="sxs-lookup"><span data-stu-id="d007d-159">Identifier</span></span>](identifier.md) |     |             |
| <span data-ttu-id="d007d-160">Customuseraccounts</span><span class="sxs-lookup"><span data-stu-id="d007d-160">CustomUserAccounts</span></span> | <span data-ttu-id="d007d-161">Attribute</span><span class="sxs-lookup"><span data-stu-id="d007d-161">Attributes</span></span> | <span data-ttu-id="d007d-162">J</span><span class="sxs-lookup"><span data-stu-id="d007d-162">Y</span></span>        | <span data-ttu-id="d007d-163">0</span><span class="sxs-lookup"><span data-stu-id="d007d-163">0</span></span>        | <span data-ttu-id="d007d-164">2147483647</span><span class="sxs-lookup"><span data-stu-id="d007d-164">2147483647</span></span> |          |           | <span data-ttu-id="d007d-165">NULL</span><span class="sxs-lookup"><span data-stu-id="d007d-165">null</span></span>                         |     |             |



 

<span data-ttu-id="d007d-166">Fahren Sie mit [dem Erstellen der Aktions Text-und Fehler Tabellen](authoring-the-actiontext-and-error-tables.md)fort.</span><span class="sxs-lookup"><span data-stu-id="d007d-166">Continue to [Authoring the ActionText and Error Tables](authoring-the-actiontext-and-error-tables.md).</span></span>

 

 



