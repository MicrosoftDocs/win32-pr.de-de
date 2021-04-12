---
description: Msival2.exe ist ein Befehlszeilen-Hilfsprogramm, mit dem eine Suite interner Konsistenz Auswertung-ICES ausgeführt werden kann.
ms.assetid: c48f4584-732a-468d-a651-2c09ce3c9ddd
title: Msival2.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b70ca2ccdeaf72c5191f292a8fa3f9b4de5dd9a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218531"
---
# <a name="msival2exe"></a><span data-ttu-id="2eb61-103">Msival2.exe</span><span class="sxs-lookup"><span data-stu-id="2eb61-103">Msival2.exe</span></span>

<span data-ttu-id="2eb61-104">Msival2.exe ist ein Befehlszeilen-Hilfsprogramm, mit dem eine Suite [interner Konsistenz Auswertung-ICES](internal-consistency-evaluators-ices.md)ausgeführt werden kann.</span><span class="sxs-lookup"><span data-stu-id="2eb61-104">Msival2.exe is a command line utility that can run a suite of [Internal Consistency Evaluators - ICEs](internal-consistency-evaluators-ices.md).</span></span>

<span data-ttu-id="2eb61-105">Dieses Tool ist nur in den [Windows SDK Komponenten für Windows Installer Entwickler](platform-sdk-components-for-windows-installer-developers.md)verfügbar.</span><span class="sxs-lookup"><span data-stu-id="2eb61-105">This tool is only available in the [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).</span></span>

<span data-ttu-id="2eb61-106">Weitere Informationen zu ICES und der CUB-Datei finden [Sie unter Using Internal Konsistenz Evaluators](using-internal-consistency-evaluators.md).</span><span class="sxs-lookup"><span data-stu-id="2eb61-106">For more information about ICEs and the CUB file, see [Using Internal Consistency Evaluators](using-internal-consistency-evaluators.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="2eb61-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="2eb61-107">Syntax</span></span>

<span data-ttu-id="2eb61-108">**Msival2** *{Database} {CUB-Datei} \[ -f \] \[ -l {LogFile} \] \[ -i {Ice ID} \[ : {Ice ID}.. \] \] .*</span><span class="sxs-lookup"><span data-stu-id="2eb61-108">**Msival2** *{database}{CUB file}\[-f\]\[-l {logfile}\]\[-i {ICE Id}\[:{ICE Id}...\]\]*</span></span>

## <a name="command-line-options"></a><span data-ttu-id="2eb61-109">Befehlszeilenoptionen</span><span class="sxs-lookup"><span data-stu-id="2eb61-109">Command Line Options</span></span>

<span data-ttu-id="2eb61-110">Msival2.exe verwendet die folgenden Befehlszeilenoptionen für die Groß-und Kleinschreibung.</span><span class="sxs-lookup"><span data-stu-id="2eb61-110">Msival2.exe uses the following case-insensitive command line options.</span></span> <span data-ttu-id="2eb61-111">Ein Schrägstrich kann auch anstelle eines Bindestrichs verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="2eb61-111">A slash delimiter may also be used in place of a dash.</span></span>



| <span data-ttu-id="2eb61-112">Option</span><span class="sxs-lookup"><span data-stu-id="2eb61-112">Option</span></span> | <span data-ttu-id="2eb61-113">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2eb61-113">Description</span></span>                                                                                                                                                                                                                                                                                               |
|--------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2eb61-114">-f</span><span class="sxs-lookup"><span data-stu-id="2eb61-114">-f</span></span>     | <span data-ttu-id="2eb61-115">Filtert alle Informationsmeldungen aus den angezeigten Ergebnissen heraus.</span><span class="sxs-lookup"><span data-stu-id="2eb61-115">Filter out all informational messages from the displayed results.</span></span> <span data-ttu-id="2eb61-116">Alle anderen Nachrichten Typen werden angezeigt.</span><span class="sxs-lookup"><span data-stu-id="2eb61-116">All other types of messages are displayed.</span></span>                                                                                                                                                                                              |
| <span data-ttu-id="2eb61-117">-i</span><span class="sxs-lookup"><span data-stu-id="2eb61-117">-i</span></span>     | <span data-ttu-id="2eb61-118">Führen Sie nur die in der Befehlszeile aufgelisteten ICES in der angegebenen Reihenfolge aus.</span><span class="sxs-lookup"><span data-stu-id="2eb61-118">Run only the ICEs listed on the command line in the order specified.</span></span> <span data-ttu-id="2eb61-119">Jede benutzerdefinierte Ice-Aktion sollte aufgeführt werden, wie Sie in der [Tabelle CustomAction](customaction-table.md) der CUB-Datei angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="2eb61-119">Each ICE custom action should be listed as it appears in the [CustomAction table](customaction-table.md) of the CUB file.</span></span> <span data-ttu-id="2eb61-120">Wenn diese Option weggelassen wird, führt das Tool den Standardsatz von ICES aus, der vom Autor der CUB-Datei angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="2eb61-120">If this option is omitted, the tool runs the default set of ICEs specified by the author of the CUB file.</span></span> |
| <span data-ttu-id="2eb61-121">-l</span><span class="sxs-lookup"><span data-stu-id="2eb61-121">-l</span></span>     | <span data-ttu-id="2eb61-122">Schreiben Sie Ergebnisse in die angegebene Datei.</span><span class="sxs-lookup"><span data-stu-id="2eb61-122">Write results to the specified file.</span></span> <span data-ttu-id="2eb61-123">Die Datei darf nicht bereits vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="2eb61-123">The file must not already exist.</span></span> <span data-ttu-id="2eb61-124">Wenn die Datei vorhanden ist, wird Sie nicht überschrieben.</span><span class="sxs-lookup"><span data-stu-id="2eb61-124">If the file exists, it is not overwritten.</span></span>                                                                                                                                                                                          |



 

## <a name="related-topics"></a><span data-ttu-id="2eb61-125">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="2eb61-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2eb61-126">Entwicklungs Tools für Windows Installer</span><span class="sxs-lookup"><span data-stu-id="2eb61-126">Windows Installer Development Tools</span></span>](windows-installer-development-tools.md)
</dt> <dt>

[<span data-ttu-id="2eb61-127">Interne Konsistenz Auswertung-ICES</span><span class="sxs-lookup"><span data-stu-id="2eb61-127">Internal Consistency Evaluators - ICEs</span></span>](internal-consistency-evaluators-ices.md)
</dt> <dt>

[<span data-ttu-id="2eb61-128">Veröffentlichte Versionen, Tools und verteilbare Dateien</span><span class="sxs-lookup"><span data-stu-id="2eb61-128">Released Versions, Tools, and Redistributables</span></span>](released-versions-tools-and-redistributables.md)
</dt> </dl>

 

 



