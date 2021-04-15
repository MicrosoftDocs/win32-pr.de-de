---
description: In der odbcdriver-Tabelle werden die ODBC-Treiber aufgelistet, die zur Installation gehören.
ms.assetid: 3518b370-0652-4b54-8057-9871365d5e8c
title: Odbcdriver-Tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3257f3eec5b60191df727d156572293489aa1956
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525781"
---
# <a name="odbcdriver-table"></a><span data-ttu-id="e5fec-103">Odbcdriver-Tabelle</span><span class="sxs-lookup"><span data-stu-id="e5fec-103">ODBCDriver Table</span></span>

<span data-ttu-id="e5fec-104">In der odbcdriver-Tabelle werden die ODBC-Treiber aufgelistet, die zur Installation gehören.</span><span class="sxs-lookup"><span data-stu-id="e5fec-104">The ODBCDriver table lists the ODBC drivers belonging to the installation.</span></span>

<span data-ttu-id="e5fec-105">Die odbcdriver-Tabelle weist die folgenden Spalten auf.</span><span class="sxs-lookup"><span data-stu-id="e5fec-105">The ODBCDriver table has the following columns.</span></span>



| <span data-ttu-id="e5fec-106">Spalte</span><span class="sxs-lookup"><span data-stu-id="e5fec-106">Column</span></span>      | <span data-ttu-id="e5fec-107">Typ</span><span class="sxs-lookup"><span data-stu-id="e5fec-107">Type</span></span>                         | <span data-ttu-id="e5fec-108">Schlüssel</span><span class="sxs-lookup"><span data-stu-id="e5fec-108">Key</span></span> | <span data-ttu-id="e5fec-109">Nullwerte zulässig</span><span class="sxs-lookup"><span data-stu-id="e5fec-109">Nullable</span></span> |
|-------------|------------------------------|-----|----------|
| <span data-ttu-id="e5fec-110">Treiber</span><span class="sxs-lookup"><span data-stu-id="e5fec-110">Driver</span></span>      | [<span data-ttu-id="e5fec-111">Bezeichner</span><span class="sxs-lookup"><span data-stu-id="e5fec-111">Identifier</span></span>](identifier.md) | <span data-ttu-id="e5fec-112">J</span><span class="sxs-lookup"><span data-stu-id="e5fec-112">Y</span></span>   | <span data-ttu-id="e5fec-113">N</span><span class="sxs-lookup"><span data-stu-id="e5fec-113">N</span></span>        |
| <span data-ttu-id="e5fec-114">Komponente\_</span><span class="sxs-lookup"><span data-stu-id="e5fec-114">Component\_</span></span> | [<span data-ttu-id="e5fec-115">Bezeichner</span><span class="sxs-lookup"><span data-stu-id="e5fec-115">Identifier</span></span>](identifier.md) | <span data-ttu-id="e5fec-116">N</span><span class="sxs-lookup"><span data-stu-id="e5fec-116">N</span></span>   | <span data-ttu-id="e5fec-117">N</span><span class="sxs-lookup"><span data-stu-id="e5fec-117">N</span></span>        |
| <span data-ttu-id="e5fec-118">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e5fec-118">Description</span></span> | [<span data-ttu-id="e5fec-119">Text</span><span class="sxs-lookup"><span data-stu-id="e5fec-119">Text</span></span>](text.md)             | <span data-ttu-id="e5fec-120">N</span><span class="sxs-lookup"><span data-stu-id="e5fec-120">N</span></span>   | <span data-ttu-id="e5fec-121">N</span><span class="sxs-lookup"><span data-stu-id="e5fec-121">N</span></span>        |
| <span data-ttu-id="e5fec-122">Datei\_</span><span class="sxs-lookup"><span data-stu-id="e5fec-122">File\_</span></span>      | [<span data-ttu-id="e5fec-123">Bezeichner</span><span class="sxs-lookup"><span data-stu-id="e5fec-123">Identifier</span></span>](identifier.md) | <span data-ttu-id="e5fec-124">N</span><span class="sxs-lookup"><span data-stu-id="e5fec-124">N</span></span>   | <span data-ttu-id="e5fec-125">N</span><span class="sxs-lookup"><span data-stu-id="e5fec-125">N</span></span>        |
| <span data-ttu-id="e5fec-126">Datei \_ Einrichtung</span><span class="sxs-lookup"><span data-stu-id="e5fec-126">File\_Setup</span></span> | [<span data-ttu-id="e5fec-127">Bezeichner</span><span class="sxs-lookup"><span data-stu-id="e5fec-127">Identifier</span></span>](identifier.md) | <span data-ttu-id="e5fec-128">N</span><span class="sxs-lookup"><span data-stu-id="e5fec-128">N</span></span>   | <span data-ttu-id="e5fec-129">J</span><span class="sxs-lookup"><span data-stu-id="e5fec-129">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="e5fec-130">Spalten</span><span class="sxs-lookup"><span data-stu-id="e5fec-130">Columns</span></span>

<dl> <dt>

<span data-ttu-id="e5fec-131"><span id="Driver"></span><span id="driver"></span><span id="DRIVER"></span>Trei</span><span class="sxs-lookup"><span data-stu-id="e5fec-131"><span id="Driver"></span><span id="driver"></span><span id="DRIVER"></span>Driver</span></span>
</dt> <dd>

<span data-ttu-id="e5fec-132">Interner Tokenname für den Treiber.</span><span class="sxs-lookup"><span data-stu-id="e5fec-132">Internal token name for driver.</span></span> <span data-ttu-id="e5fec-133">Ein Primärschlüssel für die Tabelle</span><span class="sxs-lookup"><span data-stu-id="e5fec-133">A primary key for the table</span></span>

</dd> <dt>

<span data-ttu-id="e5fec-134"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Zulieferern\_</span><span class="sxs-lookup"><span data-stu-id="e5fec-134"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Component\_</span></span>
</dt> <dd>

<span data-ttu-id="e5fec-135">Externer Schlüssel in der Komponenten Tabelle.</span><span class="sxs-lookup"><span data-stu-id="e5fec-135">External key into the Component table.</span></span>

</dd> <dt>

<span data-ttu-id="e5fec-136"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e5fec-136"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Description</span></span>
</dt> <dd>

<span data-ttu-id="e5fec-137">Die Beschreibung, die für diesen ODBC-Treiber registriert ist.</span><span class="sxs-lookup"><span data-stu-id="e5fec-137">The description registered for this ODBC driver.</span></span> <span data-ttu-id="e5fec-138">Dieser Wert kann nicht lokalisiert werden.</span><span class="sxs-lookup"><span data-stu-id="e5fec-138">This value cannot be localized.</span></span>

</dd> <dt>

<span data-ttu-id="e5fec-139"><span id="File_"></span><span id="file_"></span><span id="FILE_"></span>Datei\_</span><span class="sxs-lookup"><span data-stu-id="e5fec-139"><span id="File_"></span><span id="file_"></span><span id="FILE_"></span>File\_</span></span>
</dt> <dd>

<span data-ttu-id="e5fec-140">Die DLL-Datei für Treiber, die in der Spalte Treiber aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="e5fec-140">The DLL file for drivers listed in the Driver column.</span></span> <span data-ttu-id="e5fec-141">Die Datei \_ Spalte ist ein externer Schlüssel in der [Dateitabelle](file-table.md).</span><span class="sxs-lookup"><span data-stu-id="e5fec-141">The File\_ column is an external key into the [File table](file-table.md).</span></span> <span data-ttu-id="e5fec-142">Der Dateiname, der in der Dateiname-Spalte dieses Datei Tabellendaten Satzes eingegeben wird, muss das Kurznamen Format aufweisen.</span><span class="sxs-lookup"><span data-stu-id="e5fec-142">The filename entered in the Filename column of that File table record must be in the short filename format.</span></span> <span data-ttu-id="e5fec-143">Die SFN- \| LFN-Syntax kann nicht verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e5fec-143">The SFN\|LFN syntax cannot be used.</span></span>

</dd> <dt>

<span data-ttu-id="e5fec-144"><span id="File_Setup"></span><span id="file_setup"></span><span id="FILE_SETUP"></span>Datei \_ Einrichtung</span><span class="sxs-lookup"><span data-stu-id="e5fec-144"><span id="File_Setup"></span><span id="file_setup"></span><span id="FILE_SETUP"></span>File\_Setup</span></span>
</dt> <dd>

<span data-ttu-id="e5fec-145">Die Setup-DLL-Datei für den Treiber, wenn dieser sich von dem Treiber unterscheidet.</span><span class="sxs-lookup"><span data-stu-id="e5fec-145">The setup DLL file for the driver if it is different than from Driver.</span></span> <span data-ttu-id="e5fec-146">Die Datei \_ Spalte ist ein externer Schlüssel in der [Dateitabelle](file-table.md).</span><span class="sxs-lookup"><span data-stu-id="e5fec-146">The File\_ column is an external key into the [File table](file-table.md).</span></span> <span data-ttu-id="e5fec-147">Der Dateiname, der in der Dateiname-Spalte dieses Datei Tabellendaten Satzes eingegeben wird, muss das Kurznamen Format aufweisen.</span><span class="sxs-lookup"><span data-stu-id="e5fec-147">The filename entered in the Filename column of that File table record must be in the short filename format.</span></span> <span data-ttu-id="e5fec-148">Die SFN- \| LFN-Syntax kann nicht verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e5fec-148">The SFN\|LFN syntax cannot be used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e5fec-149">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e5fec-149">Remarks</span></span>

<span data-ttu-id="e5fec-150">Die Informationen in dieser Tabelle werden durch die [installlodbc](installodbc-action.md) -und [removeodbc](removeodbc-action.md) -Aktionen in [*Sequenz Tabellen*](s-gly.md) verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="e5fec-150">The [InstallODBC](installodbc-action.md) and [RemoveODBC](removeodbc-action.md) actions in [*sequence tables*](s-gly.md) process the information in this table.</span></span> <span data-ttu-id="e5fec-151">Weitere Informationen zum Verwenden von *Sequenz Tabellen* finden Sie unter [Verwenden einer Sequenz Tabelle](using-a-sequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="e5fec-151">For information about using *sequence tables*, see [Using a Sequence Table](using-a-sequence-table.md).</span></span>

## <a name="validation"></a><span data-ttu-id="e5fec-152">Überprüfen</span><span class="sxs-lookup"><span data-stu-id="e5fec-152">Validation</span></span>

<dl>

[<span data-ttu-id="e5fec-153">ICE03</span><span class="sxs-lookup"><span data-stu-id="e5fec-153">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="e5fec-154">ICE06</span><span class="sxs-lookup"><span data-stu-id="e5fec-154">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="e5fec-155">ICE32</span><span class="sxs-lookup"><span data-stu-id="e5fec-155">ICE32</span></span>](ice32.md)  
</dl>

 

 



