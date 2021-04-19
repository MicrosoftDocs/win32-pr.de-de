---
description: Mit der Methode "toourceimage" des Merge-Objekts kann der Client nach einer Zusammenführung die Dateien aus einem Modul in ein Quell Abbild auf dem Datenträger extrahieren, wobei Änderungen an dem Modul berücksichtigt werden, die möglicherweise während der Modulkonfiguration vorgenommen wurden.
ms.assetid: c3e3465a-d5a7-4fcc-b26a-5a8c763c23d9
title: Merge. kreatesourceimage-Methode (Mergemod. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Merge.CreateSourceImage
- IMsmMerge.CreateSourceImage
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: e8d9365a69ff6f33c2989e9102bac7c9c22166aa
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359358"
---
# <a name="mergecreatesourceimage-method"></a><span data-ttu-id="e4c01-103">Merge. kreatesourceimage-Methode</span><span class="sxs-lookup"><span data-stu-id="e4c01-103">Merge.CreateSourceImage method</span></span>

<span data-ttu-id="e4c01-104">Mit der Methode " **toourceimage** " des [**Merge**](merge-object.md) -Objekts kann der Client nach einer Zusammenführung die Dateien aus einem Modul in ein Quell Abbild auf dem Datenträger extrahieren, wobei Änderungen an dem Modul berücksichtigt werden, die möglicherweise während der Modulkonfiguration vorgenommen wurden.</span><span class="sxs-lookup"><span data-stu-id="e4c01-104">The **CreateSourceImage** method of the [**Merge**](merge-object.md) object allows the client to extract the files from a module to a source image on disk after a merge, taking into account changes to the module that might have been made during module configuration.</span></span> <span data-ttu-id="e4c01-105">Die Liste der zu extrahierenden Dateien wird während des Mergeprozesses aus der Dateitabelle des Moduls entnommen.</span><span class="sxs-lookup"><span data-stu-id="e4c01-105">The list of files to be extracted is taken from the file table of the module during the merge process.</span></span> <span data-ttu-id="e4c01-106">Die Liste der Dateien besteht aus jeder Datei, die erfolgreich aus der Dateitabelle des Moduls in die Zieldatenbank kopiert wurde.</span><span class="sxs-lookup"><span data-stu-id="e4c01-106">The list of files consists of every file successfully copied from the file table of the module to the target database.</span></span> <span data-ttu-id="e4c01-107">Datei Tabelleneinträge, die aufgrund von Primärschlüssel Konflikten mit vorhandenen Zeilen in der Datenbank nicht kopiert wurden, sind nicht Teil dieser Liste.</span><span class="sxs-lookup"><span data-stu-id="e4c01-107">File table entries that were not copied due to primary key conflicts with existing rows in the database are not a part of this list.</span></span> <span data-ttu-id="e4c01-108">Zum Zeitpunkt des Erstellens des Bilds stammt das Verzeichnis für jede dieser Dateien aus der geöffneten Datenbank (postmerge).</span><span class="sxs-lookup"><span data-stu-id="e4c01-108">At image creation time, the directory for each of these files comes from the open (post-merge) database.</span></span> <span data-ttu-id="e4c01-109">Der im *path* -Parameter angegebene Pfad ist der Stamm des Quell Bilds für die Installation.</span><span class="sxs-lookup"><span data-stu-id="e4c01-109">The path specified in the *Path* parameter is the root of the source image for the install.</span></span> <span data-ttu-id="e4c01-110">*flongfileames* bestimmt, ob lange Dateinamen sowohl für Pfadsegmente als auch für endgültige Dateinamen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e4c01-110">*fLongFileNames* determines whether or not long file names are used for both path segments and final file names.</span></span> <span data-ttu-id="e4c01-111">Die Funktion schlägt fehl, wenn keine Datenbank geöffnet ist, kein Modul geöffnet ist oder kein Merge ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="e4c01-111">The function fails if no database is open, no module is open, or no merge has been performed.</span></span>

## <a name="syntax"></a><span data-ttu-id="e4c01-112">Syntax</span><span class="sxs-lookup"><span data-stu-id="e4c01-112">Syntax</span></span>


```JScript
Merge.CreateSourceImage(
  Path,
  fLongFileNames,
  pFilePaths
)
```



## <a name="parameters"></a><span data-ttu-id="e4c01-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="e4c01-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e4c01-114">*Pfad*</span><span class="sxs-lookup"><span data-stu-id="e4c01-114">*Path*</span></span> 
</dt> <dd>

<span data-ttu-id="e4c01-115">Der Pfad des Stamms des Quell Bilds für die Installation.</span><span class="sxs-lookup"><span data-stu-id="e4c01-115">The path of the root of the source image for the install.</span></span>

</dd> <dt>

<span data-ttu-id="e4c01-116">*flongfile Ames*</span><span class="sxs-lookup"><span data-stu-id="e4c01-116">*fLongFileNames*</span></span> 
</dt> <dd>

<span data-ttu-id="e4c01-117">*flongfileames* bestimmt, ob lange Dateinamen sowohl für Pfadsegmente als auch für endgültige Dateinamen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e4c01-117">*fLongFileNames* determines whether or not long file names are used for both path segments and final file names.</span></span>

</dd> <dt>

<span data-ttu-id="e4c01-118">*pfilepath*</span><span class="sxs-lookup"><span data-stu-id="e4c01-118">*pFilePaths*</span></span> 
</dt> <dd>

<span data-ttu-id="e4c01-119">Dies ist eine Liste der voll qualifizierten Pfade für die Dateien, die erfolgreich extrahiert wurden.</span><span class="sxs-lookup"><span data-stu-id="e4c01-119">This is a list of fully qualified paths for the files that were successfully extracted.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e4c01-120">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e4c01-120">Return value</span></span>

<span data-ttu-id="e4c01-121">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="e4c01-121">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e4c01-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e4c01-122">Remarks</span></span>

<span data-ttu-id="e4c01-123">Alle Dateien im Zielverzeichnis mit demselben Namen werden überschrieben.</span><span class="sxs-lookup"><span data-stu-id="e4c01-123">Any files in the destination directory with the same name are overwritten.</span></span> <span data-ttu-id="e4c01-124">Der Pfad wird erstellt, wenn er nicht bereits vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="e4c01-124">The path is created if it does not already exist.</span></span>

### <a name="c"></a><span data-ttu-id="e4c01-125">C++</span><span class="sxs-lookup"><span data-stu-id="e4c01-125">C++</span></span>

<span data-ttu-id="e4c01-126">Siehe " [**kreatesourceimage**](/windows/desktop/api/Mergemod/nf-mergemod-imsmmerge2-createsourceimage) "-Funktion.</span><span class="sxs-lookup"><span data-stu-id="e4c01-126">See [**CreateSourceImage**](/windows/desktop/api/Mergemod/nf-mergemod-imsmmerge2-createsourceimage) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="e4c01-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e4c01-127">Requirements</span></span>



| <span data-ttu-id="e4c01-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e4c01-128">Requirement</span></span> | <span data-ttu-id="e4c01-129">Wert</span><span class="sxs-lookup"><span data-stu-id="e4c01-129">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e4c01-130">Version</span><span class="sxs-lookup"><span data-stu-id="e4c01-130">Version</span></span><br/> | <span data-ttu-id="e4c01-131">Mergemod.dll 2,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="e4c01-131">Mergemod.dll 2.0 or later</span></span><br/>                                                    |
| <span data-ttu-id="e4c01-132">Header</span><span class="sxs-lookup"><span data-stu-id="e4c01-132">Header</span></span><br/>  | <dl> <span data-ttu-id="e4c01-133"><dt>Mergemod. h</dt></span><span class="sxs-lookup"><span data-stu-id="e4c01-133"><dt>Mergemod.h</dt></span></span> </dl>   |
| <span data-ttu-id="e4c01-134">DLL</span><span class="sxs-lookup"><span data-stu-id="e4c01-134">DLL</span></span><br/>     | <dl> <span data-ttu-id="e4c01-135"><dt>Mergemod.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e4c01-135"><dt>Mergemod.dll</dt></span></span> </dl> |



 

 




