---
description: ICE60 überprüft die Dateitabelle einer Windows Installer Datenbank.
ms.assetid: 95d9b8b4-0b65-451a-8629-f0b276d6e35d
title: ICE60
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e26c6f296fd514f582a699a5f839a7e145169e3e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106349530"
---
# <a name="ice60"></a><span data-ttu-id="cbfdb-103">ICE60</span><span class="sxs-lookup"><span data-stu-id="cbfdb-103">ICE60</span></span>

<span data-ttu-id="cbfdb-104">ICE60 prüft, ob die Dateien in der [Dateitabelle](file-table.md) die folgende Bedingung erfüllen:</span><span class="sxs-lookup"><span data-stu-id="cbfdb-104">ICE60 checks that files in the [File table](file-table.md) meet the following condition:</span></span>

-   <span data-ttu-id="cbfdb-105">Wenn es sich bei der Datei nicht um eine Schriftart handelt, die über eine Version verfügt, muss Sie über eine Sprache verfügen.</span><span class="sxs-lookup"><span data-stu-id="cbfdb-105">If the file is not a font and has a version, then it must have a language.</span></span>
-   <span data-ttu-id="cbfdb-106">ICE60 prüft, ob in der [Tabelle "msiflehash](msifilehash-table.md)" keine Dateien mit Versions Angabe aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="cbfdb-106">ICE60 checks that no versioned files are listed in the [MsiFileHash table](msifilehash-table.md).</span></span>

<span data-ttu-id="cbfdb-107">Wenn eine Warnung, die von ICE60 gemeldet wird, nicht behoben werden kann, führt dies im Allgemeinen dazu, dass eine Datei bei einer Produkt Reparatur unnötig neu installiert wird.</span><span class="sxs-lookup"><span data-stu-id="cbfdb-107">Failure to fix a warning reported by ICE60 generally leads to a file being needlessly reinstalled when a product repair is done.</span></span> <span data-ttu-id="cbfdb-108">Dies liegt daran, dass die Datei, die bei der Reparatur installiert werden soll, und die vorhandene Datei auf dem Datenträger die gleiche Version (dieselbe Datei), aber unterschiedliche Sprachen aufweisen.</span><span class="sxs-lookup"><span data-stu-id="cbfdb-108">This happens because the file to be installed in the repair and the existing file on disk have the same version (they are the same file) but different languages.</span></span> <span data-ttu-id="cbfdb-109">In der Dateitabelle wird die Sprache als NULL aufgelistet, aber die Datei selbst hat einen sprach Wert in der Ressource.</span><span class="sxs-lookup"><span data-stu-id="cbfdb-109">The file table lists the language as null, but the file itself has a language value in the resource.</span></span> <span data-ttu-id="cbfdb-110">Basierend auf den [Regeln für die Datei Versions](file-versioning-rules.md)Verwaltung bevorzugt das Installationsprogramm die zu installierende Datei, sodass Sie unnötig neu kopiert wird.</span><span class="sxs-lookup"><span data-stu-id="cbfdb-110">Based on the [file versioning rules](file-versioning-rules.md), the installer favors the file to be installed, so it is recopied needlessly.</span></span>

## <a name="result"></a><span data-ttu-id="cbfdb-111">Ergebnis</span><span class="sxs-lookup"><span data-stu-id="cbfdb-111">Result</span></span>

<span data-ttu-id="cbfdb-112">ICE60 gibt eine Warnung oder einen Fehler aus, wenn eine Datei in der [Dateitabelle](file-table.md) , die keine Schriftart ist und eine Version aufweist, nicht über eine Sprache verfügt.</span><span class="sxs-lookup"><span data-stu-id="cbfdb-112">ICE60 posts a warning or an error if a file in the [File table](file-table.md) that is not a font and has a version, does not have a language.</span></span>

<span data-ttu-id="cbfdb-113">ICE60 gibt den folgenden Fehler aus, wenn eine in der Tabelle "msiflehash" aufgeführte Datei mit Versions Angabe versehen ist.</span><span class="sxs-lookup"><span data-stu-id="cbfdb-113">ICE60 posts the following error if a file listed in the MsiFileHash table is versioned.</span></span>

``` syntax
ERROR: "The file [1] is Versioned. It cannot be hashed"
```

## <a name="example"></a><span data-ttu-id="cbfdb-114">Beispiel</span><span class="sxs-lookup"><span data-stu-id="cbfdb-114">Example</span></span>

<span data-ttu-id="cbfdb-115">ICE60 meldet den folgenden Fehler und die Warnung für das gezeigte Beispiel.</span><span class="sxs-lookup"><span data-stu-id="cbfdb-115">ICE60 reports the following error and warning for the example shown.</span></span> <span data-ttu-id="cbfdb-116">(Datei B ist eine Schriftart, die anderen Dateien nicht.)</span><span class="sxs-lookup"><span data-stu-id="cbfdb-116">(File B is a font; the other files are not.)</span></span>

``` syntax
WARNING: The file FileE is not a Font, and its version is not a companion file reference. It should have a language specified in the Language column.
```

<span data-ttu-id="cbfdb-117">Die-Flea hat sowohl eine Version als auch eine Sprache. Daher wird keine Warnung oder kein Fehler generiert.</span><span class="sxs-lookup"><span data-stu-id="cbfdb-117">FileA has both a version and a language; therefore no warning or error is generated.</span></span>

<span data-ttu-id="cbfdb-118">FileB hat eine Version, aber keine Sprache.</span><span class="sxs-lookup"><span data-stu-id="cbfdb-118">FileB has a version but no language.</span></span> <span data-ttu-id="cbfdb-119">Es wird jedoch weder eine Warnung noch ein Fehler generiert, da es sich um eine Schriftart handelt.</span><span class="sxs-lookup"><span data-stu-id="cbfdb-119">No warning or error is generated, however, because it is a font.</span></span>

<span data-ttu-id="cbfdb-120">Filec ist eine begleitende Referenz, daher muss keine Sprache vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="cbfdb-120">FileC is a companion reference, so it does not have to have a language.</span></span> <span data-ttu-id="cbfdb-121">Es wird keine Warnung oder kein Fehler generiert.</span><span class="sxs-lookup"><span data-stu-id="cbfdb-121">No warning or error is generated.</span></span>

<span data-ttu-id="cbfdb-122">Das Profil hat keine Version, daher muss es nicht über eine Sprache verfügen.</span><span class="sxs-lookup"><span data-stu-id="cbfdb-122">FileD has no version, so it does not need to have a language.</span></span> <span data-ttu-id="cbfdb-123">Es wird keine Warnung oder kein Fehler generiert.</span><span class="sxs-lookup"><span data-stu-id="cbfdb-123">No warning or error is generated.</span></span>

<span data-ttu-id="cbfdb-124">"Flee" hat eine Version, aber keine Sprache.</span><span class="sxs-lookup"><span data-stu-id="cbfdb-124">FileE has a version but no language.</span></span> <span data-ttu-id="cbfdb-125">Daher wird eine Warnung generiert.</span><span class="sxs-lookup"><span data-stu-id="cbfdb-125">Therefore a warning is generated.</span></span>

<span data-ttu-id="cbfdb-126">Um diese Warnung zu beheben, fügen Sie eine Sprache zu "flee" hinzu.</span><span class="sxs-lookup"><span data-stu-id="cbfdb-126">To fix this warning, add a language to FileE.</span></span>

<span data-ttu-id="cbfdb-127">Dateien sollten nach Möglichkeit in der Versions Ressource gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="cbfdb-127">Files should have language values stored in the version resource whenever possible.</span></span> <span data-ttu-id="cbfdb-128">Wenn eine Datei sprachneutral ist, verwenden Sie die [LangID](column-data-types.md) 0.</span><span class="sxs-lookup"><span data-stu-id="cbfdb-128">If a file is language neutral, use the [LANGID](column-data-types.md) 0.</span></span>

<span data-ttu-id="cbfdb-129">[File Table](file-table.md) (fileB ist eine Schriftart, die anderen Dateien nicht.)</span><span class="sxs-lookup"><span data-stu-id="cbfdb-129">[File Table](file-table.md) (FileB is a font; the other files are not.)</span></span>



| <span data-ttu-id="cbfdb-130">File</span><span class="sxs-lookup"><span data-stu-id="cbfdb-130">File</span></span>  | <span data-ttu-id="cbfdb-131">Version</span><span class="sxs-lookup"><span data-stu-id="cbfdb-131">Version</span></span> | <span data-ttu-id="cbfdb-132">Sprache</span><span class="sxs-lookup"><span data-stu-id="cbfdb-132">Language</span></span> |
|-------|---------|----------|
| <span data-ttu-id="cbfdb-133">Mit der</span><span class="sxs-lookup"><span data-stu-id="cbfdb-133">FileA</span></span> | <span data-ttu-id="cbfdb-134">1.0</span><span class="sxs-lookup"><span data-stu-id="cbfdb-134">1.0</span></span>     | <span data-ttu-id="cbfdb-135">1033</span><span class="sxs-lookup"><span data-stu-id="cbfdb-135">1033</span></span>     |
| <span data-ttu-id="cbfdb-136">FileB</span><span class="sxs-lookup"><span data-stu-id="cbfdb-136">FileB</span></span> | <span data-ttu-id="cbfdb-137">1.0</span><span class="sxs-lookup"><span data-stu-id="cbfdb-137">1.0</span></span>     |          |
| <span data-ttu-id="cbfdb-138">Filec</span><span class="sxs-lookup"><span data-stu-id="cbfdb-138">FileC</span></span> | <span data-ttu-id="cbfdb-139">Mit der</span><span class="sxs-lookup"><span data-stu-id="cbfdb-139">FileA</span></span>   |          |
| <span data-ttu-id="cbfdb-140">Fassung</span><span class="sxs-lookup"><span data-stu-id="cbfdb-140">FileD</span></span> |         |          |
| <span data-ttu-id="cbfdb-141">Mit der</span><span class="sxs-lookup"><span data-stu-id="cbfdb-141">FileE</span></span> | <span data-ttu-id="cbfdb-142">1.0</span><span class="sxs-lookup"><span data-stu-id="cbfdb-142">1.0</span></span>     |          |



 

[<span data-ttu-id="cbfdb-143">Schriftart Tabelle</span><span class="sxs-lookup"><span data-stu-id="cbfdb-143">Font Table</span></span>](font-table.md)



| <span data-ttu-id="cbfdb-144">File</span><span class="sxs-lookup"><span data-stu-id="cbfdb-144">File</span></span>  | <span data-ttu-id="cbfdb-145">FontTitle</span><span class="sxs-lookup"><span data-stu-id="cbfdb-145">FontTitle</span></span>  |
|-------|------------|
| <span data-ttu-id="cbfdb-146">FileB</span><span class="sxs-lookup"><span data-stu-id="cbfdb-146">FileB</span></span> | <span data-ttu-id="cbfdb-147">Schriftart Titel</span><span class="sxs-lookup"><span data-stu-id="cbfdb-147">Font Title</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="cbfdb-148">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="cbfdb-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cbfdb-149">Ice-Referenz</span><span class="sxs-lookup"><span data-stu-id="cbfdb-149">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



