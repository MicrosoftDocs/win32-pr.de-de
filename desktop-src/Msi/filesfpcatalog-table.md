---
description: In der filesfpcatalog-Tabelle werden angegebene Dateien den Katalogdateien zugeordnet, die vom Systemdatei Schutz verwendet werden.
ms.assetid: 70c8b64a-cf15-411c-8388-4a7e3051f45c
title: Filesfpcatalog-Tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2300b73cc1639d8a54e206ea609043cf657c91f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362371"
---
# <a name="filesfpcatalog-table"></a><span data-ttu-id="c59a6-103">Filesfpcatalog-Tabelle</span><span class="sxs-lookup"><span data-stu-id="c59a6-103">FileSFPCatalog Table</span></span>

<span data-ttu-id="c59a6-104">In der filesfpcatalog-Tabelle werden angegebene Dateien den Katalogdateien zugeordnet, die vom Systemdatei Schutz verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c59a6-104">The FileSFPCatalog table associates specified files with the catalog files used by system file protection.</span></span>

<span data-ttu-id="c59a6-105">**Windows Vista, Windows Server 2003 und Windows XP:** Nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="c59a6-105">**Windows Vista, Windows Server 2003 and Windows XP:** Not supported.</span></span>

<span data-ttu-id="c59a6-106">Die filesfpcatalog-Tabelle weist die folgenden Spalten auf.</span><span class="sxs-lookup"><span data-stu-id="c59a6-106">The FileSFPCatalog table has the following columns.</span></span>



| <span data-ttu-id="c59a6-107">Spalte</span><span class="sxs-lookup"><span data-stu-id="c59a6-107">Column</span></span>       | <span data-ttu-id="c59a6-108">Typ</span><span class="sxs-lookup"><span data-stu-id="c59a6-108">Type</span></span>                         | <span data-ttu-id="c59a6-109">Schlüssel</span><span class="sxs-lookup"><span data-stu-id="c59a6-109">Key</span></span> | <span data-ttu-id="c59a6-110">Nullwerte zulässig</span><span class="sxs-lookup"><span data-stu-id="c59a6-110">Nullable</span></span> |
|--------------|------------------------------|-----|----------|
| <span data-ttu-id="c59a6-111">Datei\_</span><span class="sxs-lookup"><span data-stu-id="c59a6-111">File\_</span></span>       | [<span data-ttu-id="c59a6-112">Bezeichner</span><span class="sxs-lookup"><span data-stu-id="c59a6-112">Identifier</span></span>](identifier.md) | <span data-ttu-id="c59a6-113">J</span><span class="sxs-lookup"><span data-stu-id="c59a6-113">Y</span></span>   | <span data-ttu-id="c59a6-114">N</span><span class="sxs-lookup"><span data-stu-id="c59a6-114">N</span></span>        |
| <span data-ttu-id="c59a6-115">Sfpcatalog\_</span><span class="sxs-lookup"><span data-stu-id="c59a6-115">SFPCatalog\_</span></span> | [<span data-ttu-id="c59a6-116">Filename</span><span class="sxs-lookup"><span data-stu-id="c59a6-116">Filename</span></span>](filename.md)     | <span data-ttu-id="c59a6-117">J</span><span class="sxs-lookup"><span data-stu-id="c59a6-117">Y</span></span>   | <span data-ttu-id="c59a6-118">N</span><span class="sxs-lookup"><span data-stu-id="c59a6-118">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="c59a6-119">Spalten</span><span class="sxs-lookup"><span data-stu-id="c59a6-119">Columns</span></span>

<dl> <dt>

<span data-ttu-id="c59a6-120"><span id="File_"></span><span id="file_"></span><span id="FILE_"></span>Datei\_</span><span class="sxs-lookup"><span data-stu-id="c59a6-120"><span id="File_"></span><span id="file_"></span><span id="FILE_"></span>File\_</span></span>
</dt> <dd>

<span data-ttu-id="c59a6-121">Fremdschlüssel für die [Dateitabelle](file-table.md).</span><span class="sxs-lookup"><span data-stu-id="c59a6-121">Foreign key to the [File table](file-table.md).</span></span>

</dd> <dt>

<span data-ttu-id="c59a6-122"><span id="SFPCatalog_"></span><span id="sfpcatalog_"></span><span id="SFPCATALOG_"></span>Sfpcatalog\_</span><span class="sxs-lookup"><span data-stu-id="c59a6-122"><span id="SFPCatalog_"></span><span id="sfpcatalog_"></span><span id="SFPCATALOG_"></span>SFPCatalog\_</span></span>
</dt> <dd>

<span data-ttu-id="c59a6-123">Fremdschlüssel für die [sfpcatalog-Tabelle](sfpcatalog-table.md).</span><span class="sxs-lookup"><span data-stu-id="c59a6-123">Foreign key to the [SFPCatalog table](sfpcatalog-table.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c59a6-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c59a6-124">Remarks</span></span>

<span data-ttu-id="c59a6-125">Mit der [Aktion installsfpcatalogfile](installsfpcatalogfile-action.md) werden die [Komponenten Tabelle](component-table.md), die [Dateitabelle](file-table.md), die filesfpcatalog-Tabelle und die [sfpcatalog-Tabelle](sfpcatalog-table.md)abgefragt.</span><span class="sxs-lookup"><span data-stu-id="c59a6-125">The [InstallSFPCatalogFile action](installsfpcatalogfile-action.md) queries the [Component table](component-table.md), [File table](file-table.md), FileSFPCatalog table and [SFPCatalog table](sfpcatalog-table.md).</span></span>

## <a name="validation"></a><span data-ttu-id="c59a6-126">Überprüfen</span><span class="sxs-lookup"><span data-stu-id="c59a6-126">Validation</span></span>

<dl>

[<span data-ttu-id="c59a6-127">ICE03</span><span class="sxs-lookup"><span data-stu-id="c59a6-127">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="c59a6-128">ICE06</span><span class="sxs-lookup"><span data-stu-id="c59a6-128">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="c59a6-129">ICE32</span><span class="sxs-lookup"><span data-stu-id="c59a6-129">ICE32</span></span>](ice32.md)  
[<span data-ttu-id="c59a6-130">ICE66</span><span class="sxs-lookup"><span data-stu-id="c59a6-130">ICE66</span></span>](ice66.md)  
[<span data-ttu-id="c59a6-131">ICE76</span><span class="sxs-lookup"><span data-stu-id="c59a6-131">ICE76</span></span>](ice76.md)  
</dl>

 

 



