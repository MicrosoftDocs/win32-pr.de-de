---
description: Die extractfilesex-Methode des Merge-Objekts extrahiert die eingebettete CAB-Datei aus einem Modul und schreibt diese Dateien dann in das Zielverzeichnis.
ms.assetid: 8b063052-4f92-466a-9c52-bda26ed13d5c
title: Merge. extractfilesex-Methode (Mergemod. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Merge.ExtractFilesEx
- IMsmMerge.ExtractFilesEx
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: be6aa1001be0d3ecd6cbb9c4cd1d8c04b4649f10
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359803"
---
# <a name="mergeextractfilesex-method"></a><span data-ttu-id="7f6f6-103">Merge. extractfilesex-Methode</span><span class="sxs-lookup"><span data-stu-id="7f6f6-103">Merge.ExtractFilesEx method</span></span>

<span data-ttu-id="7f6f6-104">Die **extractfilesex** -Methode des [**Merge**](merge-object.md) -Objekts extrahiert die eingebettete CAB-Datei aus einem Modul und schreibt diese Dateien dann in das Zielverzeichnis.</span><span class="sxs-lookup"><span data-stu-id="7f6f6-104">The **ExtractFilesEx** method of the [**Merge**](merge-object.md) object extracts the embedded .cab file from a module and then writes those files to the destination directory.</span></span>

## <a name="syntax"></a><span data-ttu-id="7f6f6-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="7f6f6-105">Syntax</span></span>


```JScript
Merge.ExtractFilesEx(
  Path,
  fLongFileNames,
  pFilePaths
)
```



## <a name="parameters"></a><span data-ttu-id="7f6f6-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="7f6f6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7f6f6-107">*Pfad*</span><span class="sxs-lookup"><span data-stu-id="7f6f6-107">*Path*</span></span> 
</dt> <dd>

<span data-ttu-id="7f6f6-108">Das voll qualifizierte Zielverzeichnis.</span><span class="sxs-lookup"><span data-stu-id="7f6f6-108">The fully qualified destination directory.</span></span>

</dd> <dt>

<span data-ttu-id="7f6f6-109">*flongfile Ames*</span><span class="sxs-lookup"><span data-stu-id="7f6f6-109">*fLongFileNames*</span></span> 
</dt> <dd>

<span data-ttu-id="7f6f6-110">Legen Sie fest, um die Verwendung von langen Dateinamen für Pfadsegmente und endgültige Dateinamen anzugeben.</span><span class="sxs-lookup"><span data-stu-id="7f6f6-110">Set to specify using long file names for path segments and final file names.</span></span>

</dd> <dt>

<span data-ttu-id="7f6f6-111">*pfilepath*</span><span class="sxs-lookup"><span data-stu-id="7f6f6-111">*pFilePaths*</span></span> 
</dt> <dd>

<span data-ttu-id="7f6f6-112">Dies ist eine Liste der voll qualifizierten Pfade für die Dateien, die erfolgreich extrahiert wurden.</span><span class="sxs-lookup"><span data-stu-id="7f6f6-112">This is a list of fully qualified paths for the files that were successfully extracted.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7f6f6-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7f6f6-113">Return value</span></span>

<span data-ttu-id="7f6f6-114">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="7f6f6-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="7f6f6-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7f6f6-115">Remarks</span></span>

<span data-ttu-id="7f6f6-116">Alle Dateien im Zielverzeichnis mit demselben Namen werden überschrieben.</span><span class="sxs-lookup"><span data-stu-id="7f6f6-116">Any files in the destination directory with the same name are overwritten.</span></span> <span data-ttu-id="7f6f6-117">Der Pfad wird erstellt, wenn er nicht bereits vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="7f6f6-117">The path is created if it does not already exist.</span></span>

### <a name="c"></a><span data-ttu-id="7f6f6-118">C++</span><span class="sxs-lookup"><span data-stu-id="7f6f6-118">C++</span></span>

<span data-ttu-id="7f6f6-119">Siehe [**extractfilesex**](/windows/desktop/api/Mergemod/nf-mergemod-imsmmerge2-extractfilesex) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="7f6f6-119">See [**ExtractFilesEx**](/windows/desktop/api/Mergemod/nf-mergemod-imsmmerge2-extractfilesex) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="7f6f6-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7f6f6-120">Requirements</span></span>



| <span data-ttu-id="7f6f6-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7f6f6-121">Requirement</span></span> | <span data-ttu-id="7f6f6-122">Wert</span><span class="sxs-lookup"><span data-stu-id="7f6f6-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7f6f6-123">Version</span><span class="sxs-lookup"><span data-stu-id="7f6f6-123">Version</span></span><br/> | <span data-ttu-id="7f6f6-124">Mergemod.dll 2,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="7f6f6-124">Mergemod.dll 2.0 or later</span></span><br/>                                                    |
| <span data-ttu-id="7f6f6-125">Header</span><span class="sxs-lookup"><span data-stu-id="7f6f6-125">Header</span></span><br/>  | <dl> <span data-ttu-id="7f6f6-126"><dt>Mergemod. h</dt></span><span class="sxs-lookup"><span data-stu-id="7f6f6-126"><dt>Mergemod.h</dt></span></span> </dl>   |
| <span data-ttu-id="7f6f6-127">DLL</span><span class="sxs-lookup"><span data-stu-id="7f6f6-127">DLL</span></span><br/>     | <dl> <span data-ttu-id="7f6f6-128"><dt>Mergemod.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7f6f6-128"><dt>Mergemod.dll</dt></span></span> </dl> |



 

 




