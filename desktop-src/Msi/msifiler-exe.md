---
description: MsiFiler.exe füllt die Dateitabelle mit Dateiversionen, Sprachen und Größen auf Grundlage eines Quell Verzeichnisses auf. Außerdem kann die msiflehash-Tabelle mit Dateihashes aktualisiert werden.
ms.assetid: cc3db60b-0b1d-4582-8b40-0b55f83e00be
title: Msifiler.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2d7aeceae7abd8a9786079788e68c7d7bda35ae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106356735"
---
# <a name="msifilerexe"></a><span data-ttu-id="8f156-104">Msifiler.exe</span><span class="sxs-lookup"><span data-stu-id="8f156-104">Msifiler.exe</span></span>

<span data-ttu-id="8f156-105">MsiFiler.exe füllt die [Dateitabelle](file-table.md) mit Dateiversionen, Sprachen und Größen auf Grundlage eines Quell Verzeichnisses auf.</span><span class="sxs-lookup"><span data-stu-id="8f156-105">MsiFiler.exe populates the [File table](file-table.md) with file versions, languages, and sizes based upon a source directory.</span></span> <span data-ttu-id="8f156-106">Außerdem kann die [msiflehash-Tabelle](msifilehash-table.md) mit Dateihashes aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="8f156-106">It can also update the [MsiFileHash table](msifilehash-table.md) with file hashes.</span></span>

## <a name="syntax"></a><span data-ttu-id="8f156-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="8f156-107">Syntax</span></span>

<span data-ttu-id="8f156-108">**msifiler.exe-d** *{Database}* **\[ -v \] \[ -h \] \[ -s altsource \]**</span><span class="sxs-lookup"><span data-stu-id="8f156-108">**msifiler.exe -d** *{database}* **\[-v\] \[-h\] \[-s ALTSOURCE\]**</span></span>

## <a name="command-line-options"></a><span data-ttu-id="8f156-109">Befehlszeilenoptionen</span><span class="sxs-lookup"><span data-stu-id="8f156-109">Command Line Options</span></span>

<span data-ttu-id="8f156-110">Msifiler.exe verwendet die folgenden Befehlszeilenoptionen für die Groß-und Kleinschreibung.</span><span class="sxs-lookup"><span data-stu-id="8f156-110">Msifiler.exe uses the following case-insensitive command line options.</span></span> <span data-ttu-id="8f156-111">Ein Schrägstrich kann auch anstelle eines Bindestrichs verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="8f156-111">A slash delimiter may also be used in place of a dash.</span></span>



| <span data-ttu-id="8f156-112">Option</span><span class="sxs-lookup"><span data-stu-id="8f156-112">Option</span></span> | <span data-ttu-id="8f156-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="8f156-113">Parameter</span></span>   | <span data-ttu-id="8f156-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8f156-114">Description</span></span>                                                                                                                                                                  |
|--------|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8f156-115">-d</span><span class="sxs-lookup"><span data-stu-id="8f156-115">-d</span></span>     | <span data-ttu-id="8f156-116">*database*</span><span class="sxs-lookup"><span data-stu-id="8f156-116">*database*</span></span>  | <span data-ttu-id="8f156-117">Die zu Aktualisier Ende Datenbank (MSI-Datei).</span><span class="sxs-lookup"><span data-stu-id="8f156-117">The database (.msi file) that is to be updated.</span></span>                                                                                                                              |
| <span data-ttu-id="8f156-118">-v</span><span class="sxs-lookup"><span data-stu-id="8f156-118">-v</span></span>     |             | <span data-ttu-id="8f156-119">Verwenden Sie den ausführlichen Modus.</span><span class="sxs-lookup"><span data-stu-id="8f156-119">Use verbose mode.</span></span>                                                                                                                                                            |
| <span data-ttu-id="8f156-120">-h</span><span class="sxs-lookup"><span data-stu-id="8f156-120">-h</span></span>     |             | <span data-ttu-id="8f156-121">Füllen Sie die [Tabelle "msiflehash](msifilehash-table.md)" auf.</span><span class="sxs-lookup"><span data-stu-id="8f156-121">Populate the [MsiFileHash table](msifilehash-table.md).</span></span> <span data-ttu-id="8f156-122">Dadurch wird die Tabelle erstellt, wenn Sie nicht bereits vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="8f156-122">This creates the table if it does not already exist.</span></span> <span data-ttu-id="8f156-123">Die msiflehash-Tabelle kann nur mit Dateien ohne Versions Angabe verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="8f156-123">The MsiFileHash table can only be used with unversioned files.</span></span> |
| <span data-ttu-id="8f156-124">-S</span><span class="sxs-lookup"><span data-stu-id="8f156-124">-s</span></span>     | <span data-ttu-id="8f156-125">*Altsource*</span><span class="sxs-lookup"><span data-stu-id="8f156-125">*ALTSOURCE*</span></span> | <span data-ttu-id="8f156-126">Altsource gibt ein alternatives Verzeichnis an, in dem die Dateien gefunden werden.</span><span class="sxs-lookup"><span data-stu-id="8f156-126">ALTSOURCE specifies an alternative directory to find the files.</span></span>                                                                                                              |



 

<span data-ttu-id="8f156-127">Dieses Tool ist nur in den [Windows SDK Komponenten für Windows Installer Entwickler](platform-sdk-components-for-windows-installer-developers.md)verfügbar.</span><span class="sxs-lookup"><span data-stu-id="8f156-127">This tool is only available in the [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="8f156-128">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="8f156-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8f156-129">Entwicklungs Tools für Windows Installer</span><span class="sxs-lookup"><span data-stu-id="8f156-129">Windows Installer Development Tools</span></span>](windows-installer-development-tools.md)
</dt> <dt>

[<span data-ttu-id="8f156-130">Verwenden der Verzeichnis Tabelle</span><span class="sxs-lookup"><span data-stu-id="8f156-130">Using the Directory Table</span></span>](using-the-directory-table.md)
</dt> <dt>

[<span data-ttu-id="8f156-131">Veröffentlichte Versionen, Tools und verteilbare Dateien</span><span class="sxs-lookup"><span data-stu-id="8f156-131">Released Versions, Tools, and Redistributables</span></span>](released-versions-tools-and-redistributables.md)
</dt> </dl>

 

 



