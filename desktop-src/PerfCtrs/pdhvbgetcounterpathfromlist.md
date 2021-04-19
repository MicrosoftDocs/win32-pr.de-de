---
description: Die pdhvbgetcounterpathfromlist-Funktion kopiert den Indikator Pfad, auf den der Index-Parameter verweist, aus einer Indikator Pfad Liste, die vom Benutzer beim letzten Aufrufen der pdhvbkreatecounterpathlist-Funktion erstellt wurde.
ms.assetid: e77a022d-42f2-4c48-acb7-36cb013730dd
title: Pdhvbgetcounterpathfromlist-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PdhVbGetCounterPathFromList
api_type:
- DllExport
api_location:
- Pdh.dll
ms.openlocfilehash: 4c5ae4632ede898b7cd323723037ea68d53455b1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106357758"
---
# <a name="pdhvbgetcounterpathfromlist-function"></a><span data-ttu-id="8e8af-103">Pdhvbgetcounterpathfromlist-Funktion</span><span class="sxs-lookup"><span data-stu-id="8e8af-103">PdhVbGetCounterPathFromList function</span></span>

<span data-ttu-id="8e8af-104">Die **pdhvbgetcounterpathfromlist** -Funktion kopiert den Indikator Pfad, auf den der Index-Parameter verweist, aus einer *Indikator* Pfad Liste, die vom Benutzer beim letzten Aufrufen der [**pdhvbkreatecounterpathlist**](pdhvbcreatecounterpathlist.md) -Funktion erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="8e8af-104">The **PdhVbGetCounterPathFromList** function copies the counter path referenced by the *Index* parameter from a counter path list created by the user from the most recent call to the [**PdhVbCreateCounterPathList**](pdhvbcreatecounterpathlist.md) function.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="8e8af-105">Die Funktion, die in diesem Thema beschrieben wird, kann in Zukunft geändert oder nicht mehr verfügbar sein.</span><span class="sxs-lookup"><span data-stu-id="8e8af-105">The function that this topic describes may be altered or unavailable in the future.</span></span> <span data-ttu-id="8e8af-106">Stattdessen empfiehlt Microsoft die Verwendung der Funktionen, die unter [Funktionen von Leistungsindikatoren](performance-counters-functions.md)beschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="8e8af-106">Instead, Microsoft recommends that you use the functions described in [Performance Counters Functions](performance-counters-functions.md).</span></span>

<span data-ttu-id="8e8af-107">Funktion "pdhvbgetcounterpathfromlist" ( \_ ByVal-Index "Long", \_ ByVal-Puffer als Zeichenfolge, \_ ByVal-BufferLength "Long" \_ )</span><span class="sxs-lookup"><span data-stu-id="8e8af-107">Function PdhVbGetCounterPathFromList( \_ ByVal Index As Long, \_ ByVal Buffer As String, \_ ByVal BufferLength As Long \_ ) As Long</span></span>

## <a name="parameters"></a><span data-ttu-id="8e8af-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="8e8af-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8e8af-109">*Index*</span><span class="sxs-lookup"><span data-stu-id="8e8af-109">*Index*</span></span> 
</dt> <dd>

<span data-ttu-id="8e8af-110">Der Index des abzurufenden Indikator Pfads.</span><span class="sxs-lookup"><span data-stu-id="8e8af-110">Index of the counter path to retrieve.</span></span> <span data-ttu-id="8e8af-111">Dies muss ein Wert sein, der größer oder gleich 1 und kleiner oder gleich dem Wert ist, der von der [**pdhvbkreatecounterpathlist**](pdhvbcreatecounterpathlist.md) -Funktion zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="8e8af-111">This must be a value that is greater than or equal to 1, and less than or equal to the value returned by the [**PdhVbCreateCounterPathList**](pdhvbcreatecounterpathlist.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="8e8af-112">*Buffer*</span><span class="sxs-lookup"><span data-stu-id="8e8af-112">*Buffer*</span></span> 
</dt> <dd>

<span data-ttu-id="8e8af-113">Die dimensionierte und initialisierte Zeichenfolge, die den Indikator Pfad empfängt, der dem Wert des Index Parameters entspricht.</span><span class="sxs-lookup"><span data-stu-id="8e8af-113">Dimensioned and initialized string that will receive the counter path that corresponds to the value of the Index parameter.</span></span>

</dd> <dt>

<span data-ttu-id="8e8af-114">*BufferLength*</span><span class="sxs-lookup"><span data-stu-id="8e8af-114">*BufferLength*</span></span> 
</dt> <dd>

<span data-ttu-id="8e8af-115">Maximale Anzahl von Zeichen, die in die Zeichenfolge passt, auf die von Buffer verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="8e8af-115">Maximum number of characters that will fit in the string referenced by Buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8e8af-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8e8af-116">Return value</span></span>

<span data-ttu-id="8e8af-117">Die-Funktion gibt die Anzahl der in den Puffer kopierten Zeichen zurück.</span><span class="sxs-lookup"><span data-stu-id="8e8af-117">The function returns the number of characters copied to Buffer.</span></span>

## <a name="requirements"></a><span data-ttu-id="8e8af-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8e8af-118">Requirements</span></span>



| <span data-ttu-id="8e8af-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8e8af-119">Requirement</span></span> | <span data-ttu-id="8e8af-120">Wert</span><span class="sxs-lookup"><span data-stu-id="8e8af-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="8e8af-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="8e8af-121">Minimum supported client</span></span><br/> | <span data-ttu-id="8e8af-122">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8e8af-122">Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="8e8af-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="8e8af-123">Minimum supported server</span></span><br/> | <span data-ttu-id="8e8af-124">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8e8af-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="8e8af-125">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="8e8af-125">Library</span></span><br/>                  | <dl> <span data-ttu-id="8e8af-126"><dt>PDH. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8e8af-126"><dt>Pdh.lib</dt></span></span> </dl> |
| <span data-ttu-id="8e8af-127">DLL</span><span class="sxs-lookup"><span data-stu-id="8e8af-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8e8af-128"><dt>Pdh.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8e8af-128"><dt>Pdh.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8e8af-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8e8af-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8e8af-130">**Pdhvbkreatecounterpathlist**</span><span class="sxs-lookup"><span data-stu-id="8e8af-130">**PdhVbCreateCounterPathList**</span></span>](pdhvbcreatecounterpathlist.md)
</dt> <dt>

[<span data-ttu-id="8e8af-131">**Pdhvbgetcounterpathelements**</span><span class="sxs-lookup"><span data-stu-id="8e8af-131">**PdhVbGetCounterPathElements**</span></span>](pdhvbgetcounterpathelements.md)
</dt> <dt>

[<span data-ttu-id="8e8af-132">**Pdhvbgetonecounterpath**</span><span class="sxs-lookup"><span data-stu-id="8e8af-132">**PdhVbGetOneCounterPath**</span></span>](pdhvbgetonecounterpath.md)
</dt> </dl>

 

 




