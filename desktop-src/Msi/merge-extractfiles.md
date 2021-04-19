---
description: Die ExtractFiles-Methode des Merge-Objekts extrahiert die eingebettete CAB-Datei aus einem Modul und schreibt diese Dateien dann in das Zielverzeichnis.
ms.assetid: 846355d6-32f2-4b04-91dc-acd60445fbd9
title: Merge. ExtractFiles-Methode (advpub. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Merge.ExtractFiles
- IMsmMerge.ExtractFiles
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: 3869dc37b841d386891eb70940054bd78805bf94
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106360427"
---
# <a name="mergeextractfiles-method"></a><span data-ttu-id="db223-103">Merge. ExtractFiles-Methode</span><span class="sxs-lookup"><span data-stu-id="db223-103">Merge.ExtractFiles method</span></span>

<span data-ttu-id="db223-104">Die **ExtractFiles** -Methode des [**Merge**](merge-object.md) -Objekts extrahiert die eingebettete CAB-Datei aus einem Modul und schreibt diese Dateien dann in das Zielverzeichnis.</span><span class="sxs-lookup"><span data-stu-id="db223-104">The **ExtractFiles** method of the [**Merge**](merge-object.md) object extracts the embedded .cab file from a module and then writes those files to the destination directory.</span></span>

## <a name="syntax"></a><span data-ttu-id="db223-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="db223-105">Syntax</span></span>


```JScript
Merge.ExtractFiles(
  Path
)
```



## <a name="parameters"></a><span data-ttu-id="db223-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="db223-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="db223-107">*Pfad*</span><span class="sxs-lookup"><span data-stu-id="db223-107">*Path*</span></span> 
</dt> <dd>

<span data-ttu-id="db223-108">Das voll qualifizierte Zielverzeichnis.</span><span class="sxs-lookup"><span data-stu-id="db223-108">The fully qualified destination directory.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="db223-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="db223-109">Return value</span></span>

<span data-ttu-id="db223-110">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="db223-110">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="db223-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="db223-111">Remarks</span></span>

<span data-ttu-id="db223-112">Alle Dateien im Zielverzeichnis mit demselben Namen werden überschrieben.</span><span class="sxs-lookup"><span data-stu-id="db223-112">Any files in the destination directory with the same name are overwritten.</span></span> <span data-ttu-id="db223-113">Der Pfad wird erstellt, wenn er nicht bereits vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="db223-113">The path is created if it does not already exist.</span></span>

<span data-ttu-id="db223-114">**ExtractFiles** extrahiert Dateien immer mit kurzen Dateinamen für den Pfad.</span><span class="sxs-lookup"><span data-stu-id="db223-114">**ExtractFiles** always extracts files using short file names for the path.</span></span> <span data-ttu-id="db223-115">Verwenden Sie die [**extractfilesex-Methode**](merge-extractfilesex.md), um lange Dateinamen für den Pfad zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="db223-115">To use long file names for the path, use the [**ExtractFilesEx method**](merge-extractfilesex.md).</span></span>

### <a name="c"></a><span data-ttu-id="db223-116">C++</span><span class="sxs-lookup"><span data-stu-id="db223-116">C++</span></span>

<span data-ttu-id="db223-117">Siehe [**ExtractFiles**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-extractfiles) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="db223-117">See [**ExtractFiles**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-extractfiles) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="db223-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="db223-118">Requirements</span></span>



| <span data-ttu-id="db223-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="db223-119">Requirement</span></span> | <span data-ttu-id="db223-120">Wert</span><span class="sxs-lookup"><span data-stu-id="db223-120">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="db223-121">Version</span><span class="sxs-lookup"><span data-stu-id="db223-121">Version</span></span><br/> | <span data-ttu-id="db223-122">Mergemod.dll 1,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="db223-122">Mergemod.dll 1.0 or later</span></span><br/>                                                                     |
| <span data-ttu-id="db223-123">Header</span><span class="sxs-lookup"><span data-stu-id="db223-123">Header</span></span><br/>  | <dl> <span data-ttu-id="db223-124"><dt>Advpub. h (Include Mergemod. h)</dt></span><span class="sxs-lookup"><span data-stu-id="db223-124"><dt>Advpub.h (include Mergemod.h)</dt></span></span> </dl> |
| <span data-ttu-id="db223-125">DLL</span><span class="sxs-lookup"><span data-stu-id="db223-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="db223-126"><dt>Mergemod.dll</dt></span><span class="sxs-lookup"><span data-stu-id="db223-126"><dt>Mergemod.dll</dt></span></span> </dl>                  |



 

 
