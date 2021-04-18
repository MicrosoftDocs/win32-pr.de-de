---
description: Extrahiert die Header Informationen aus einem Delta.
title: Extractpatchheaderabflea/W-Funktion
ms.topic: reference
ms.date: 04/17/2020
ms.keywords: ExtractPatchHeaderToFileA, ExtractPatchHeaderToFileW
req.header: patchapi.h
req.dll: mspatchc.dll
topic_type:
- APIRef
- kbSyntax
api_name:
- ExtractPatchHeaderToFileW
api_type:
- DllExport
api_location:
- mspatchc.dll
ms.openlocfilehash: 40835a0b88558046ff9086ffcd7ec4609d1ed863
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106357666"
---
# <a name="extractpatchheadertofileaw-function"></a><span data-ttu-id="d90d0-103">Extractpatchheaderabflea/W-Funktion</span><span class="sxs-lookup"><span data-stu-id="d90d0-103">ExtractPatchHeaderToFileA/W function</span></span>

<span data-ttu-id="d90d0-104">Die Funktionen **extractpatchheaderdefilea** und **extractpatchheaderdefilew** extrahieren die Header Informationen aus einem Delta.</span><span class="sxs-lookup"><span data-stu-id="d90d0-104">The **ExtractPatchHeaderToFileA** and **ExtractPatchHeaderToFileW** functions extract the header information from a delta.</span></span> <span data-ttu-id="d90d0-105">Das Delta wird als Dateipfad bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="d90d0-105">The delta is provided as a file path.</span></span> <span data-ttu-id="d90d0-106">Der Ausgabe Header wird auch in einen bereitgestellten Pfad geschrieben.</span><span class="sxs-lookup"><span data-stu-id="d90d0-106">The output header is also written to a provided path.</span></span>

## <a name="syntax"></a><span data-ttu-id="d90d0-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="d90d0-107">Syntax</span></span>

```cpp
BOOL  PATCHAPI  ExtractPatchHeaderToFileA(
    LPCTSTR  PatchFileName,
    LPCTSTR  PatchHeaderFileName
    );

BOOL  PATCHAPI  ExtractPatchHeaderToFileW(
    LPCWSTR  PatchFileName,
    LPCWSTR  PatchHeaderFileName
    );
```

## <a name="parameters"></a><span data-ttu-id="d90d0-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="d90d0-108">Parameters</span></span>

<span data-ttu-id="d90d0-109">*Patchdateiname*</span><span class="sxs-lookup"><span data-stu-id="d90d0-109">*PatchFileName*</span></span>

<span data-ttu-id="d90d0-110">Der Name des Deltas, das den Header enthält.</span><span class="sxs-lookup"><span data-stu-id="d90d0-110">The name of the delta containing the header.</span></span>

<span data-ttu-id="d90d0-111">*Patchheaderfilename*</span><span class="sxs-lookup"><span data-stu-id="d90d0-111">*PatchHeaderFileName*</span></span>

<span data-ttu-id="d90d0-112">Der Name der Header Datei, die erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="d90d0-112">The name of the header file that is to be created.</span></span>

## <a name="return-value"></a><span data-ttu-id="d90d0-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d90d0-113">Return value</span></span>

<span data-ttu-id="d90d0-114">Diese Funktion gibt **true** zurück, wenn Sie erfolgreich ist. Andernfalls wird **false** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="d90d0-114">This function returns **TRUE** if it succeeds; otherwise, it returns **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="d90d0-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d90d0-115">Requirements</span></span>

| <span data-ttu-id="d90d0-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d90d0-116">Requirement</span></span> | <span data-ttu-id="d90d0-117">Wert</span><span class="sxs-lookup"><span data-stu-id="d90d0-117">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d90d0-118">Header</span><span class="sxs-lookup"><span data-stu-id="d90d0-118">Header</span></span> | <span data-ttu-id="d90d0-119">PatchAPI. h</span><span class="sxs-lookup"><span data-stu-id="d90d0-119">patchapi.h</span></span> |
| <span data-ttu-id="d90d0-120">DLL</span><span class="sxs-lookup"><span data-stu-id="d90d0-120">DLL</span></span> | <span data-ttu-id="d90d0-121">mspatchc.dll</span><span class="sxs-lookup"><span data-stu-id="d90d0-121">mspatchc.dll</span></span> |
| <span data-ttu-id="d90d0-122">Unicode</span><span class="sxs-lookup"><span data-stu-id="d90d0-122">Unicode</span></span> | <span data-ttu-id="d90d0-123">Implementiert als extractpatchheaderpatfilew (Unicode) und extractpatchheaderumfilea (ANSI)</span><span class="sxs-lookup"><span data-stu-id="d90d0-123">Implemented as ExtractPatchHeaderToFileW (Unicode) and ExtractPatchHeaderToFileA (ANSI)</span></span> |

## <a name="see-also"></a><span data-ttu-id="d90d0-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d90d0-124">See also</span></span>

[<span data-ttu-id="d90d0-125">PatchAPI</span><span class="sxs-lookup"><span data-stu-id="d90d0-125">PatchAPI</span></span>](patchapi.md)
