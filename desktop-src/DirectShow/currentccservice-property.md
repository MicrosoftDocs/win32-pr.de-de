---
description: Die currentccservice-Eigenschaft legt den aktuellen Untertitel Dienst fest oder ruft ihn ab.
ms.assetid: 094cf812-3122-4d5f-af8a-afd1c2264a2b
title: Currentccservice (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb5c1ddf243b0ec943be1f22930a8802d28d1bda
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103860346"
---
# <a name="currentccservice-property"></a><span data-ttu-id="4bfde-103">Currentccservice (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="4bfde-103">CurrentCCService Property</span></span>

> [!Note]  
> <span data-ttu-id="4bfde-104">Diese Komponente ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="4bfde-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="4bfde-105">Es kann in nachfolgenden Versionen geändert oder entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="4bfde-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="4bfde-106">Die- `CurrentCCService` Eigenschaft legt den aktuellen Untertitel Dienst fest oder ruft ihn ab.</span><span class="sxs-lookup"><span data-stu-id="4bfde-106">The `CurrentCCService` property sets or retrieves the current closed captioning service.</span></span>

``` syntax
[ iService = ] MSWebDVD.CurrentCCService
```

## <a name="return-value"></a><span data-ttu-id="4bfde-107">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4bfde-107">Return Value</span></span>

<span data-ttu-id="4bfde-108">Gibt einen ganzzahligen Wert zurück, der den Typ des aktivierten Dienstanbieter dienstanens</span><span class="sxs-lookup"><span data-stu-id="4bfde-108">Returns an integer value indicating the type of closed captioning service enabled.</span></span>

## <a name="remarks"></a><span data-ttu-id="4bfde-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4bfde-109">Remarks</span></span>

<span data-ttu-id="4bfde-110">Mögliche Werte für diese Eigenschaft:</span><span class="sxs-lookup"><span data-stu-id="4bfde-110">The possible values of this property are:</span></span>



| <span data-ttu-id="4bfde-111">Wert</span><span class="sxs-lookup"><span data-stu-id="4bfde-111">Value</span></span> | <span data-ttu-id="4bfde-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4bfde-112">Description</span></span>                                                          |
|-------|----------------------------------------------------------------------|
| <span data-ttu-id="4bfde-113">0x0</span><span class="sxs-lookup"><span data-stu-id="4bfde-113">0x0</span></span>   | <span data-ttu-id="4bfde-114">Kein aktueller Dienst.</span><span class="sxs-lookup"><span data-stu-id="4bfde-114">No current service.</span></span> <span data-ttu-id="4bfde-115">Dies ist der Standardwert.</span><span class="sxs-lookup"><span data-stu-id="4bfde-115">This is the default value.</span></span>                       |
| <span data-ttu-id="4bfde-116">0x1</span><span class="sxs-lookup"><span data-stu-id="4bfde-116">0x1</span></span>   | <span data-ttu-id="4bfde-117">True Untertitel, erstes Feld.</span><span class="sxs-lookup"><span data-stu-id="4bfde-117">True captioning, first field.</span></span> <span data-ttu-id="4bfde-118">Standard Dienst.</span><span class="sxs-lookup"><span data-stu-id="4bfde-118">Default service.</span></span>                       |
| <span data-ttu-id="4bfde-119">0x2</span><span class="sxs-lookup"><span data-stu-id="4bfde-119">0x2</span></span>   | <span data-ttu-id="4bfde-120">Untertitel für sekundäre Sprache, zweites Feld.</span><span class="sxs-lookup"><span data-stu-id="4bfde-120">Captioning for secondary language, second field.</span></span> <span data-ttu-id="4bfde-121">Wird in der Regel nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="4bfde-121">Generally not used.</span></span> |



 

<span data-ttu-id="4bfde-122">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="4bfde-122">This property is read/write.</span></span>

## <a name="see-also"></a><span data-ttu-id="4bfde-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4bfde-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4bfde-124">**Ccactive**</span><span class="sxs-lookup"><span data-stu-id="4bfde-124">**CCActive**</span></span>](ccactive-property.md)
</dt> </dl>

 

 



