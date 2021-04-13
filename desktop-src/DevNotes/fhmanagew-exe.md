---
description: Das FhManagew.exe Programm löscht Dateiversionen, die ein bestimmtes Alter überschreiten, aus dem momentan zugewiesenen Datei Versionsverlauf-Zielgerät.
ms.assetid: 31A6E1AC-492A-4080-9095-3180FD60A575
title: FhManagew.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f7c7cdaa5ddba46dc2ead3e4e9a462416758e1e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483243"
---
# <a name="fhmanagewexe"></a><span data-ttu-id="7bb1a-103">FhManagew.exe</span><span class="sxs-lookup"><span data-stu-id="7bb1a-103">FhManagew.exe</span></span>

<span data-ttu-id="7bb1a-104">Das FhManagew.exe Programm löscht Dateiversionen, die ein bestimmtes Alter überschreiten, aus dem momentan zugewiesenen Datei Versionsverlauf-Zielgerät.</span><span class="sxs-lookup"><span data-stu-id="7bb1a-104">The FhManagew.exe program deletes file versions that exceed a specified age from the currently assigned File History target device.</span></span>

<span data-ttu-id="7bb1a-105">Dieses Programm ist in Windows 8 und Windows Server 2012 und höher verfügbar.</span><span class="sxs-lookup"><span data-stu-id="7bb1a-105">This program is available in Windows 8 and Windows Server 2012 and later.</span></span>

<span data-ttu-id="7bb1a-106">Wechseln Sie zum Ausführen dieses Programms zum **Startmenü** , klicken Sie auf **Ausführen**, und geben Sie den folgenden Befehl ein.</span><span class="sxs-lookup"><span data-stu-id="7bb1a-106">To execute this program, go to the **Start** menu, click **Run**, and type the following command.</span></span>

<span data-ttu-id="7bb1a-107">**FhManagew.exe Bereinigungs** *Alter*</span><span class="sxs-lookup"><span data-stu-id="7bb1a-107">**FhManagew.exe -cleanup** *age*</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="7bb1a-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="7bb1a-108">Parameter</span></span></th>
<th><span data-ttu-id="7bb1a-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7bb1a-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="7bb1a-110"><span id="age"></span><span id="AGE"></span><em>Eder</em></span><span class="sxs-lookup"><span data-stu-id="7bb1a-110"><span id="age"></span><span id="AGE"></span><em>age</em></span></span><br/></td>
<td><span data-ttu-id="7bb1a-111">Dieser Parameter gibt das minimale Alter (in Tagen) von Dateiversionen an, die gelöscht werden können.</span><span class="sxs-lookup"><span data-stu-id="7bb1a-111">This parameter specifies the minimum age, in days, of file versions that can be deleted.</span></span> <span data-ttu-id="7bb1a-112">Eine Dateiversion wird gelöscht, wenn beide der folgenden Bedingungen zutreffen:</span><span class="sxs-lookup"><span data-stu-id="7bb1a-112">A file version is deleted if both of the following conditions are true:</span></span><br/>
<ul>
<li><span data-ttu-id="7bb1a-113">Die Dateiversion ist älter als das angegebene Alter.</span><span class="sxs-lookup"><span data-stu-id="7bb1a-113">The file version is older than the specified age.</span></span></li>
<li><span data-ttu-id="7bb1a-114">Die Datei ist nicht mehr im Schutzbereich enthalten, oder es gibt eine neuere Version derselben Datei auf dem Zielgerät.</span><span class="sxs-lookup"><span data-stu-id="7bb1a-114">The file is no longer included in the protection scope, or there is a newer version of the same file on the target device.</span></span></li>
</ul>
<span data-ttu-id="7bb1a-115">Wenn der <em>Age</em> -Parameter auf 0 (null) festgelegt ist, werden alle Dateiversionen gelöscht, mit Ausnahme der neuesten Version der einzelnen Dateien, die derzeit im Schutzbereich vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="7bb1a-115">If the <em>age</em> parameter is set to zero, all file versions are deleted, except for the newest version of each file that is currently present in the protection scope.</span></span><br/></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="7bb1a-116">Um die gesamte Ausgabe dieses Programms zu unterdrücken, verwenden Sie die **-quiet-** Befehlszeilenoption wie folgt.</span><span class="sxs-lookup"><span data-stu-id="7bb1a-116">To suppress all output from this program, use the **-quiet** command-line option as follows.</span></span>

<span data-ttu-id="7bb1a-117">**FhManagew.exe-Cleanup** *Age* **-quiet**</span><span class="sxs-lookup"><span data-stu-id="7bb1a-117">**FhManagew.exe -cleanup** *age* **-quiet**</span></span>

## <a name="examples"></a><span data-ttu-id="7bb1a-118">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7bb1a-118">Examples</span></span>



| <span data-ttu-id="7bb1a-119">Beispiel</span><span class="sxs-lookup"><span data-stu-id="7bb1a-119">Example</span></span>                                                                                                                                                                                                      | <span data-ttu-id="7bb1a-120">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7bb1a-120">Description</span></span>                                                                               |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="7bb1a-121"><span id="FhManagew.exe_-cleanup_30"></span><span id="fhmanagew.exe_-cleanup_30"></span><span id="FHMANAGEW.EXE_-CLEANUP_30"></span>**FhManagew.exe-Bereinigung 30**</span><span class="sxs-lookup"><span data-stu-id="7bb1a-121"><span id="FhManagew.exe_-cleanup_30"></span><span id="fhmanagew.exe_-cleanup_30"></span><span id="FHMANAGEW.EXE_-CLEANUP_30"></span>**FhManagew.exe -cleanup 30**</span></span><br/>                                 | <span data-ttu-id="7bb1a-122">Löschen Sie alle Dateiversionen, die älter als ein Monat sind.</span><span class="sxs-lookup"><span data-stu-id="7bb1a-122">Delete all file versions that are older than one month.</span></span><br/>                        |
| <span data-ttu-id="7bb1a-123"><span id="FhManagew.exe_-cleanup_365_-quiet"></span><span id="fhmanagew.exe_-cleanup_365_-quiet"></span><span id="FHMANAGEW.EXE_-CLEANUP_365_-QUIET"></span>**FhManagew.exe-Bereinigung 365-quiet**</span><span class="sxs-lookup"><span data-stu-id="7bb1a-123"><span id="FhManagew.exe_-cleanup_365_-quiet"></span><span id="fhmanagew.exe_-cleanup_365_-quiet"></span><span id="FHMANAGEW.EXE_-CLEANUP_365_-QUIET"></span>**FhManagew.exe -cleanup 365 -quiet**</span></span><br/> | <span data-ttu-id="7bb1a-124">Löschen Sie alle Dateiversionen, die älter als ein Jahr sind, und unterdrücken Sie die gesamte Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="7bb1a-124">Delete all file versions that are older than one year and suppress all output.</span></span><br/> |



 

 

 




