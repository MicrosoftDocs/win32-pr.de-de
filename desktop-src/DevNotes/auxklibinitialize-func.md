---
description: Initialisiert die aux \_ KLIB-Bibliothek.
ms.assetid: 516bb359-d3a3-415b-90af-09e544366a12
title: Funktion "auxklibinitialize" (AUX \_ KLIB. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AuxKlibInitialize
api_type:
- LibDef
api_location:
- Aux_klib.lib
ms.openlocfilehash: d16ea418d2012b24ce19ad14afab12e198e7ab2e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369227"
---
# <a name="auxklibinitialize-function"></a><span data-ttu-id="e928e-103">Funktion "auxklibinitialize"</span><span class="sxs-lookup"><span data-stu-id="e928e-103">AuxKlibInitialize function</span></span>

<span data-ttu-id="e928e-104">Initialisiert die aux \_ KLIB-Bibliothek.</span><span class="sxs-lookup"><span data-stu-id="e928e-104">Initializes the Aux\_klib library.</span></span> <span data-ttu-id="e928e-105">Diese Funktion muss aufgerufen werden, bevor eine andere Funktion in der Bibliothek aufgerufen werden kann.</span><span class="sxs-lookup"><span data-stu-id="e928e-105">This function must be called before any other function in the library can be called.</span></span>

## <a name="syntax"></a><span data-ttu-id="e928e-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="e928e-106">Syntax</span></span>


```C++
NTSTATUS _stdcall AuxKlibInitialize(void);
```



## <a name="parameters"></a><span data-ttu-id="e928e-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="e928e-107">Parameters</span></span>

<span data-ttu-id="e928e-108">Diese Funktion besitzt keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="e928e-108">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="e928e-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e928e-109">Return value</span></span>

<span data-ttu-id="e928e-110">Wenn die Funktion erfolgreich ausgeführt wird, lautet der Rückgabewert Status \_ Success.</span><span class="sxs-lookup"><span data-stu-id="e928e-110">If the function succeeds, the return value is STATUS\_SUCCESS.</span></span>

<span data-ttu-id="e928e-111">Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der in "NTSTATUS. h" definierten Statuscodes sein, die im WDK verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="e928e-111">If the function fails, the return value can be one of the status codes defined in Ntstatus.h, which is available in the WDK.</span></span>

## <a name="remarks"></a><span data-ttu-id="e928e-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e928e-112">Remarks</span></span>

<span data-ttu-id="e928e-113">Die Objektbibliothek, die diese API implementiert, kann [hier](https://www.microsoft.com/?ref=go)heruntergeladen werden.</span><span class="sxs-lookup"><span data-stu-id="e928e-113">The object library that implements this API can be downloaded from [here](https://www.microsoft.com/?ref=go).</span></span>

## <a name="requirements"></a><span data-ttu-id="e928e-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e928e-114">Requirements</span></span>



| <span data-ttu-id="e928e-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e928e-115">Requirement</span></span> | <span data-ttu-id="e928e-116">Wert</span><span class="sxs-lookup"><span data-stu-id="e928e-116">Value</span></span> |
|----------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="e928e-117">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="e928e-117">Redistributable</span></span><br/> | <span data-ttu-id="e928e-118">Windows-Erweiterungs-API-Bibliothek, Version 1,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="e928e-118">Windows Auxiliary API library version 1.0 or later</span></span><br/>                            |
| <span data-ttu-id="e928e-119">Header</span><span class="sxs-lookup"><span data-stu-id="e928e-119">Header</span></span><br/>          | <dl> <span data-ttu-id="e928e-120"><dt>AUX \_ KLIB. h</dt></span><span class="sxs-lookup"><span data-stu-id="e928e-120"><dt>Aux\_klib.h</dt></span></span> </dl>   |
| <span data-ttu-id="e928e-121">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="e928e-121">Library</span></span><br/>         | <dl> <span data-ttu-id="e928e-122"><dt>AUX \_ KLIB. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e928e-122"><dt>Aux\_klib.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e928e-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e928e-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e928e-124">**"Auxklibquerymoduleinformation"**</span><span class="sxs-lookup"><span data-stu-id="e928e-124">**AuxKlibQueryModuleInformation**</span></span>](auxklibquerymoduleinformation-func.md)
</dt> </dl>

 

 




