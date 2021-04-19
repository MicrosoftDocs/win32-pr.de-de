---
description: Erstellt ein Delta zwischen der angegebenen Quelldatei und der angegebenen Zieldatei.
title: Funktion "featepatchfileexa/W"
ms.topic: reference
ms.date: 04/17/2020
ms.keywords: CreatePatchFileExA, CreatePatchFileExW
req.header: patchapi.h
req.dll: mspatchc.dll
topic_type:
- APIRef
- kbSyntax
api_name:
- CreatePatchFileExW
api_type:
- DllExport
api_location:
- mspatchc.dll
ms.openlocfilehash: c84be2d859a780e46e7e940aa4a7e7da5296f0e7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106355268"
---
# <a name="createpatchfileexaw-function"></a><span data-ttu-id="d7245-103">Funktion "featepatchfileexa/W"</span><span class="sxs-lookup"><span data-stu-id="d7245-103">CreatePatchFileExA/W function</span></span>

<span data-ttu-id="d7245-104">Die Funktionen " **epatepatchfileexa** " und " **upatepatchfileexw** " erstellen ein Delta zwischen der angegebenen Quelldatei und der angegebenen Zieldatei.</span><span class="sxs-lookup"><span data-stu-id="d7245-104">The **CreatePatchFileExA** and **CreatePatchFileExW** functions create a delta between the specified source file and the specified target file.</span></span> <span data-ttu-id="d7245-105">Sowohl die Quell-als auch die Zieldateien werden als Pfade bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="d7245-105">Both the source and the target files are provided as paths.</span></span> <span data-ttu-id="d7245-106">Das Ausgabe Delta wird auch in einen bereitgestellten Pfad geschrieben.</span><span class="sxs-lookup"><span data-stu-id="d7245-106">The output delta is also written to a provided path.</span></span> <span data-ttu-id="d7245-107">Diese Funktionen stellen während des Erstellungs Vorgangs Statusberichte bereit.</span><span class="sxs-lookup"><span data-stu-id="d7245-107">These functions provide progress reporting during the create process.</span></span>

## <a name="syntax"></a><span data-ttu-id="d7245-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="d7245-108">Syntax</span></span>

```cpp
BOOL  PATCHAPI  CreatePatchFileExA(
    ULONG                     OldFileCount,
    PPATCH_OLD_FILE_INFO_A    OldFileInfoArray,
    LPCTSTR                   NewFileName,
    LPCTSTR                   PatchFileName,
    ULONG                     OptionFlags,
    PPATCH_OPTION_DATA        OptionData,
    PPATCH_PROGRESS_CALLBACK  ProgressCallback,
    PVOID                     CallbackContext
    );

BOOL  PATCHAPI  CreatePatchFileExW(
    ULONG                     OldFileCount,
    PPATCH_OLD_FILE_INFO_A    OldFileInfoArray,
    LPCWSTR                   NewFileName,
    LPCWSTR                   PatchFileName,
    ULONG                     OptionFlags,
    PPATCH_OPTION_DATA        OptionData,
    PPATCH_PROGRESS_CALLBACK  ProgressCallback,
    PVOID                     CallbackContext
    );
```

## <a name="parameters"></a><span data-ttu-id="d7245-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="d7245-109">Parameters</span></span>

<span data-ttu-id="d7245-110">*Oldfilecount*</span><span class="sxs-lookup"><span data-stu-id="d7245-110">*OldFileCount*</span></span>

<span data-ttu-id="d7245-111">Die Gesamtanzahl der Quelldateien.</span><span class="sxs-lookup"><span data-stu-id="d7245-111">The total number of source files.</span></span> <span data-ttu-id="d7245-112">Wird verwendet, um Delta-Dateien für mehrere Quelldateien (maximal 255) zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="d7245-112">Used to create deltas against multiple source files (maximum 255).</span></span>

<span data-ttu-id="d7245-113">*Oldfileingefoarray*</span><span class="sxs-lookup"><span data-stu-id="d7245-113">*OldFileInfoArray*</span></span>

<span data-ttu-id="d7245-114">Ein Zeiger auf das Quelldatei Informations Array.</span><span class="sxs-lookup"><span data-stu-id="d7245-114">Pointer to source file information array.</span></span>

<span data-ttu-id="d7245-115">*NewFileName*</span><span class="sxs-lookup"><span data-stu-id="d7245-115">*NewFileName*</span></span>

<span data-ttu-id="d7245-116">Der Name der Zieldatei.</span><span class="sxs-lookup"><span data-stu-id="d7245-116">The name of the target file.</span></span>

<span data-ttu-id="d7245-117">*Patchdateiname*</span><span class="sxs-lookup"><span data-stu-id="d7245-117">*PatchFileName*</span></span>

<span data-ttu-id="d7245-118">Der Name des Deltas, das erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="d7245-118">The name of the delta that is created.</span></span>

<span data-ttu-id="d7245-119">*Optionflags*</span><span class="sxs-lookup"><span data-stu-id="d7245-119">*OptionFlags*</span></span>

<span data-ttu-id="d7245-120">Erstellungsflags.</span><span class="sxs-lookup"><span data-stu-id="d7245-120">Creation flags.</span></span>

<span data-ttu-id="d7245-121">*ProgressCallback*</span><span class="sxs-lookup"><span data-stu-id="d7245-121">*ProgressCallback*</span></span>

<span data-ttu-id="d7245-122">Zeiger auf einen Anwendungs definierten Fortschritts Rückruf.</span><span class="sxs-lookup"><span data-stu-id="d7245-122">Pointer to application-defined progress callback.</span></span>

<span data-ttu-id="d7245-123">*CallbackContext*</span><span class="sxs-lookup"><span data-stu-id="d7245-123">*CallbackContext*</span></span>

<span data-ttu-id="d7245-124">Zeiger auf einen Anwendungs definierten Kontext.</span><span class="sxs-lookup"><span data-stu-id="d7245-124">Pointer to application-defined context.</span></span>

## <a name="return-value"></a><span data-ttu-id="d7245-125">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d7245-125">Return value</span></span>

<span data-ttu-id="d7245-126">Diese Funktion gibt **true** zurück, wenn Sie erfolgreich ist. Andernfalls wird **false** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="d7245-126">This function returns **TRUE** if it succeeds; otherwise, it returns **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="d7245-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d7245-127">Requirements</span></span>

| <span data-ttu-id="d7245-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d7245-128">Requirement</span></span> | <span data-ttu-id="d7245-129">Wert</span><span class="sxs-lookup"><span data-stu-id="d7245-129">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d7245-130">Header</span><span class="sxs-lookup"><span data-stu-id="d7245-130">Header</span></span> | <span data-ttu-id="d7245-131">PatchAPI. h</span><span class="sxs-lookup"><span data-stu-id="d7245-131">patchapi.h</span></span> |
| <span data-ttu-id="d7245-132">DLL</span><span class="sxs-lookup"><span data-stu-id="d7245-132">DLL</span></span> | <span data-ttu-id="d7245-133">mspatchc.dll</span><span class="sxs-lookup"><span data-stu-id="d7245-133">mspatchc.dll</span></span> |
| <span data-ttu-id="d7245-134">Unicode</span><span class="sxs-lookup"><span data-stu-id="d7245-134">Unicode</span></span> | <span data-ttu-id="d7245-135">Implementiert als "kreatepatchfileexw (Unicode)" und "kreatepatchfileexa" (ANSI)</span><span class="sxs-lookup"><span data-stu-id="d7245-135">Implemented as CreatePatchFileExW (Unicode) and CreatePatchFileExA (ANSI)</span></span> |

## <a name="see-also"></a><span data-ttu-id="d7245-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d7245-136">See also</span></span>

[<span data-ttu-id="d7245-137">PatchAPI</span><span class="sxs-lookup"><span data-stu-id="d7245-137">PatchAPI</span></span>](patchapi.md)
