---
description: Die msisfcbypass-Tabelle enthält eine Liste von Dateien, mit denen der Windows-Datei Schutz umgangen werden muss, wenn die Dateien unter Microsoft Windows Me installiert werden.
ms.assetid: 86de0dc1-ed8f-410c-a411-6c44c8e5c9fd
title: Msisfcbypass-Tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 707294e9461aaf321add8a3959682a0db555cc2c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104347338"
---
# <a name="msisfcbypass-table"></a><span data-ttu-id="3691a-103">Msisfcbypass-Tabelle</span><span class="sxs-lookup"><span data-stu-id="3691a-103">MsiSFCBypass Table</span></span>

<span data-ttu-id="3691a-104">Die msisfcbypass-Tabelle enthält eine Liste von Dateien, mit denen der Windows-Datei Schutz umgangen werden muss, wenn die Dateien unter Microsoft Windows Me installiert werden.</span><span class="sxs-lookup"><span data-stu-id="3691a-104">The MsiSFCBypass Table contains a list of files that should bypass Windows File Protection when the files are installed on Microsoft Windows Me.</span></span>

<span data-ttu-id="3691a-105">Die msisfcbypass-Tabelle weist die folgende Spalte auf.</span><span class="sxs-lookup"><span data-stu-id="3691a-105">The MsiSFCBypass Table has the following column.</span></span>



| <span data-ttu-id="3691a-106">Spalte</span><span class="sxs-lookup"><span data-stu-id="3691a-106">Column</span></span> | <span data-ttu-id="3691a-107">Typ</span><span class="sxs-lookup"><span data-stu-id="3691a-107">Type</span></span>                         | <span data-ttu-id="3691a-108">Schlüssel</span><span class="sxs-lookup"><span data-stu-id="3691a-108">Key</span></span> | <span data-ttu-id="3691a-109">Nullwerte zulässig</span><span class="sxs-lookup"><span data-stu-id="3691a-109">Nullable</span></span> |
|--------|------------------------------|-----|----------|
| <span data-ttu-id="3691a-110">Datei\_</span><span class="sxs-lookup"><span data-stu-id="3691a-110">File\_</span></span> | [<span data-ttu-id="3691a-111">Bezeichner</span><span class="sxs-lookup"><span data-stu-id="3691a-111">Identifier</span></span>](identifier.md) | <span data-ttu-id="3691a-112">J</span><span class="sxs-lookup"><span data-stu-id="3691a-112">Y</span></span>   | <span data-ttu-id="3691a-113">N</span><span class="sxs-lookup"><span data-stu-id="3691a-113">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="3691a-114">Spalten</span><span class="sxs-lookup"><span data-stu-id="3691a-114">Columns</span></span>

<dl> <dt>

<span data-ttu-id="3691a-115"><span id="File_"></span><span id="file_"></span><span id="FILE_"></span>Datei\_</span><span class="sxs-lookup"><span data-stu-id="3691a-115"><span id="File_"></span><span id="file_"></span><span id="FILE_"></span>File\_</span></span>
</dt> <dd>

<span data-ttu-id="3691a-116">Der Fremdschlüssel für die [Dateitabelle](file-table.md) , der die Datei angibt, die den Windows-Datei Schutz umgehen soll, wenn die Datei unter Windows Me installiert ist.</span><span class="sxs-lookup"><span data-stu-id="3691a-116">The foreign key to the [File Table](file-table.md) that specifies the file that should bypass Windows File Protection when the file is installed on Windows Me.</span></span>

</dd> </dl>

 

 



