---
description: In der odbctranslator-Tabelle werden die ODBC-Konvertierer aufgelistet, die zur Installation gehören.
ms.assetid: fecb7454-29bb-4ddf-b4d5-2e56c20ff2dc
title: Odbctranslator-Tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9fdf85f73b649e18c0980508e234bf7599e69c5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106363420"
---
# <a name="odbctranslator-table"></a><span data-ttu-id="8b599-103">Odbctranslator-Tabelle</span><span class="sxs-lookup"><span data-stu-id="8b599-103">ODBCTranslator Table</span></span>

<span data-ttu-id="8b599-104">In der odbctranslator-Tabelle werden die ODBC-Konvertierer aufgelistet, die zur Installation gehören.</span><span class="sxs-lookup"><span data-stu-id="8b599-104">The ODBCTranslator table lists the ODBC translators belonging to the installation.</span></span>

<span data-ttu-id="8b599-105">Die odbctranslator-Tabelle weist die folgenden Spalten auf.</span><span class="sxs-lookup"><span data-stu-id="8b599-105">The ODBCTranslator table has the following columns.</span></span>



| <span data-ttu-id="8b599-106">Spalte</span><span class="sxs-lookup"><span data-stu-id="8b599-106">Column</span></span>      | <span data-ttu-id="8b599-107">Typ</span><span class="sxs-lookup"><span data-stu-id="8b599-107">Type</span></span>                         | <span data-ttu-id="8b599-108">Schlüssel</span><span class="sxs-lookup"><span data-stu-id="8b599-108">Key</span></span> | <span data-ttu-id="8b599-109">Nullwerte zulässig</span><span class="sxs-lookup"><span data-stu-id="8b599-109">Nullable</span></span> |
|-------------|------------------------------|-----|----------|
| <span data-ttu-id="8b599-110">Translator</span><span class="sxs-lookup"><span data-stu-id="8b599-110">Translator</span></span>  | [<span data-ttu-id="8b599-111">Bezeichner</span><span class="sxs-lookup"><span data-stu-id="8b599-111">Identifier</span></span>](identifier.md) | <span data-ttu-id="8b599-112">J</span><span class="sxs-lookup"><span data-stu-id="8b599-112">Y</span></span>   | <span data-ttu-id="8b599-113">N</span><span class="sxs-lookup"><span data-stu-id="8b599-113">N</span></span>        |
| <span data-ttu-id="8b599-114">Komponente\_</span><span class="sxs-lookup"><span data-stu-id="8b599-114">Component\_</span></span> | [<span data-ttu-id="8b599-115">Bezeichner</span><span class="sxs-lookup"><span data-stu-id="8b599-115">Identifier</span></span>](identifier.md) | <span data-ttu-id="8b599-116">N</span><span class="sxs-lookup"><span data-stu-id="8b599-116">N</span></span>   | <span data-ttu-id="8b599-117">N</span><span class="sxs-lookup"><span data-stu-id="8b599-117">N</span></span>        |
| <span data-ttu-id="8b599-118">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8b599-118">Description</span></span> | [<span data-ttu-id="8b599-119">Text</span><span class="sxs-lookup"><span data-stu-id="8b599-119">Text</span></span>](text.md)             | <span data-ttu-id="8b599-120">N</span><span class="sxs-lookup"><span data-stu-id="8b599-120">N</span></span>   | <span data-ttu-id="8b599-121">N</span><span class="sxs-lookup"><span data-stu-id="8b599-121">N</span></span>        |
| <span data-ttu-id="8b599-122">Datei\_</span><span class="sxs-lookup"><span data-stu-id="8b599-122">File\_</span></span>      | [<span data-ttu-id="8b599-123">Bezeichner</span><span class="sxs-lookup"><span data-stu-id="8b599-123">Identifier</span></span>](identifier.md) | <span data-ttu-id="8b599-124">N</span><span class="sxs-lookup"><span data-stu-id="8b599-124">N</span></span>   | <span data-ttu-id="8b599-125">N</span><span class="sxs-lookup"><span data-stu-id="8b599-125">N</span></span>        |
| <span data-ttu-id="8b599-126">Datei \_ Einrichtung</span><span class="sxs-lookup"><span data-stu-id="8b599-126">File\_Setup</span></span> | [<span data-ttu-id="8b599-127">Bezeichner</span><span class="sxs-lookup"><span data-stu-id="8b599-127">Identifier</span></span>](identifier.md) | <span data-ttu-id="8b599-128">N</span><span class="sxs-lookup"><span data-stu-id="8b599-128">N</span></span>   | <span data-ttu-id="8b599-129">J</span><span class="sxs-lookup"><span data-stu-id="8b599-129">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="8b599-130">Spalten</span><span class="sxs-lookup"><span data-stu-id="8b599-130">Columns</span></span>

<dl> <dt>

<span data-ttu-id="8b599-131"><span id="Translator"></span><span id="translator"></span><span id="TRANSLATOR"></span>Translator</span><span class="sxs-lookup"><span data-stu-id="8b599-131"><span id="Translator"></span><span id="translator"></span><span id="TRANSLATOR"></span>Translator</span></span>
</dt> <dd>

<span data-ttu-id="8b599-132">Interner Tokenname für Translator.</span><span class="sxs-lookup"><span data-stu-id="8b599-132">Internal token name for translator.</span></span> <span data-ttu-id="8b599-133">Ein Primärschlüssel für die Tabelle.</span><span class="sxs-lookup"><span data-stu-id="8b599-133">A primary key for the table.</span></span>

</dd> <dt>

<span data-ttu-id="8b599-134"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Zulieferern\_</span><span class="sxs-lookup"><span data-stu-id="8b599-134"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Component\_</span></span>
</dt> <dd>

<span data-ttu-id="8b599-135">Externer Schlüssel in der Komponenten Tabelle.</span><span class="sxs-lookup"><span data-stu-id="8b599-135">External key into the Component table.</span></span>

</dd> <dt>

<span data-ttu-id="8b599-136"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8b599-136"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Description</span></span>
</dt> <dd>

<span data-ttu-id="8b599-137">Die Beschreibung, die für diesen ODBC-Treiber Konvertierer registriert ist.</span><span class="sxs-lookup"><span data-stu-id="8b599-137">The description registered for this ODBC driver translator.</span></span> <span data-ttu-id="8b599-138">Dieser Wert kann nicht lokalisiert werden.</span><span class="sxs-lookup"><span data-stu-id="8b599-138">This value cannot be localized.</span></span>

</dd> <dt>

<span data-ttu-id="8b599-139"><span id="File_"></span><span id="file_"></span><span id="FILE_"></span>Datei\_</span><span class="sxs-lookup"><span data-stu-id="8b599-139"><span id="File_"></span><span id="file_"></span><span id="FILE_"></span>File\_</span></span>
</dt> <dd>

<span data-ttu-id="8b599-140">Die DLL-Datei für die in der Spalte Translator aufgelistete Übertragung.</span><span class="sxs-lookup"><span data-stu-id="8b599-140">The DLL file for the transfer listed in the Translator column.</span></span> <span data-ttu-id="8b599-141">Die Datei \_ Spalte ist ein externer Schlüssel in der [Dateitabelle](file-table.md).</span><span class="sxs-lookup"><span data-stu-id="8b599-141">The File\_ column is an external key into the [File table](file-table.md).</span></span> <span data-ttu-id="8b599-142">Der Dateiname, der in der Dateiname-Spalte dieses Datei Tabellendaten Satzes eingegeben wird, muss das Kurznamen Format aufweisen.</span><span class="sxs-lookup"><span data-stu-id="8b599-142">The filename entered in the Filename column of that File table record must be in the short filename format.</span></span> <span data-ttu-id="8b599-143">Die SFN- \| LFN-Syntax kann nicht verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="8b599-143">The SFN\|LFN syntax cannot be used.</span></span>

</dd> <dt>

<span data-ttu-id="8b599-144"><span id="File_Setup"></span><span id="file_setup"></span><span id="FILE_SETUP"></span>Datei \_ Einrichtung</span><span class="sxs-lookup"><span data-stu-id="8b599-144"><span id="File_Setup"></span><span id="file_setup"></span><span id="FILE_SETUP"></span>File\_Setup</span></span>
</dt> <dd>

<span data-ttu-id="8b599-145">Die Setup-DLL-Datei für den Konvertierer, wenn Sie sich von der Übersetzer Spalte unterscheidet.</span><span class="sxs-lookup"><span data-stu-id="8b599-145">The setup DLL file for the translator if it is different from the Translator column.</span></span> <span data-ttu-id="8b599-146">Die Datei \_ Spalte ist ein externer Schlüssel in der [Dateitabelle](file-table.md).</span><span class="sxs-lookup"><span data-stu-id="8b599-146">The File\_ column is an external key into the [File table](file-table.md).</span></span> <span data-ttu-id="8b599-147">Der Dateiname, der in der Dateiname-Spalte dieses Datei Tabellendaten Satzes eingegeben wird, muss das Kurznamen Format aufweisen.</span><span class="sxs-lookup"><span data-stu-id="8b599-147">The filename entered in the Filename column of that File table record must be in the short filename format.</span></span> <span data-ttu-id="8b599-148">Die SFN- \| LFN-Syntax kann nicht verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="8b599-148">The SFN\|LFN syntax cannot be used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8b599-149">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8b599-149">Remarks</span></span>

<span data-ttu-id="8b599-150">Die Informationen in dieser Tabelle werden durch die [installlodbc](installodbc-action.md) -und [removeodbc](removeodbc-action.md) -Aktionen in [*Sequenz Tabellen*](s-gly.md) verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="8b599-150">The [InstallODBC](installodbc-action.md) and [RemoveODBC](removeodbc-action.md) actions in [*sequence tables*](s-gly.md) process the information in this table.</span></span> <span data-ttu-id="8b599-151">Weitere Informationen zum Verwenden von *Sequenz Tabellen* finden Sie unter [Verwenden einer Sequenz Tabelle](using-a-sequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="8b599-151">For information about using *sequence tables*, see [Using a Sequence Table](using-a-sequence-table.md).</span></span>

## <a name="validation"></a><span data-ttu-id="8b599-152">Überprüfen</span><span class="sxs-lookup"><span data-stu-id="8b599-152">Validation</span></span>

<dl>

[<span data-ttu-id="8b599-153">ICE03</span><span class="sxs-lookup"><span data-stu-id="8b599-153">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="8b599-154">ICE06</span><span class="sxs-lookup"><span data-stu-id="8b599-154">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="8b599-155">ICE32</span><span class="sxs-lookup"><span data-stu-id="8b599-155">ICE32</span></span>](ice32.md)  
</dl>

 

 



