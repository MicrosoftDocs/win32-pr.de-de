---
description: Die csystemclock-Klasse implementiert eine Uhr, die die Systemzeit zurückgibt.
ms.assetid: 22f8b641-6472-433f-bff4-4e62eae25c9b
title: Csystemclock-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSystemClock
api_type:
- COM
api_location: ''
ms.openlocfilehash: e9cc5e0bde8983cfd8c544d3898d4af628e10f87
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104570079"
---
# <a name="csystemclock-class"></a><span data-ttu-id="11eae-103">Csystemclock-Klasse</span><span class="sxs-lookup"><span data-stu-id="11eae-103">CSystemClock class</span></span>

![csystemclock-Klassenhierarchie](images/sclock01.png)

<span data-ttu-id="11eae-105">Die- `CSystemClock` Klasse implementiert eine Uhr, die die Systemzeit zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="11eae-105">The `CSystemClock` class implements a clock that returns the system time.</span></span>

<span data-ttu-id="11eae-106">Diese Klasse wird von der [**cbasereferenceclock**](cbasereferenceclock.md) -Klasse abgeleitet und fügt Unterstützung für die **ipersistent** -und [**iamclockadjust**](/windows/desktop/api/Strmif/nn-strmif-iamclockadjust) -Schnittstellen hinzu.</span><span class="sxs-lookup"><span data-stu-id="11eae-106">This class derives from the [**CBaseReferenceClock**](cbasereferenceclock.md) class, and adds support for the **IPersist** and [**IAMClockAdjust**](/windows/desktop/api/Strmif/nn-strmif-iamclockadjust) interfaces.</span></span>



| <span data-ttu-id="11eae-107">Öffentliche Methoden</span><span class="sxs-lookup"><span data-stu-id="11eae-107">Public Methods</span></span>                                        | <span data-ttu-id="11eae-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="11eae-108">Description</span></span>                                         |
|-------------------------------------------------------|-----------------------------------------------------|
| [<span data-ttu-id="11eae-109">**CreateInstance**</span><span class="sxs-lookup"><span data-stu-id="11eae-109">**CreateInstance**</span></span>](csystemclock-createinstance.md) | <span data-ttu-id="11eae-110">Erstellt eine neue Instanz dieses Objekts.</span><span class="sxs-lookup"><span data-stu-id="11eae-110">Creates a new instance of this object.</span></span>              |
| [<span data-ttu-id="11eae-111">**Csystemclock**</span><span class="sxs-lookup"><span data-stu-id="11eae-111">**CSystemClock**</span></span>](csystemclock-csystemclock.md)     | <span data-ttu-id="11eae-112">Konstruktormethode.</span><span class="sxs-lookup"><span data-stu-id="11eae-112">Constructor method.</span></span>                                 |
| <span data-ttu-id="11eae-113">Iamclockadjust-Methoden</span><span class="sxs-lookup"><span data-stu-id="11eae-113">IAMClockAdjust Methods</span></span>                                | <span data-ttu-id="11eae-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="11eae-114">Description</span></span>                                         |
| [<span data-ttu-id="11eae-115">**Setclockdelta**</span><span class="sxs-lookup"><span data-stu-id="11eae-115">**SetClockDelta**</span></span>](csystemclock-setclockdelta.md)   | <span data-ttu-id="11eae-116">Passt die Uhrzeit an.</span><span class="sxs-lookup"><span data-stu-id="11eae-116">Adjusts the clock time.</span></span>                             |
| <span data-ttu-id="11eae-117">Ipersistent-Methoden</span><span class="sxs-lookup"><span data-stu-id="11eae-117">IPersist Methods</span></span>                                      | <span data-ttu-id="11eae-118">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="11eae-118">Description</span></span>                                         |
| [<span data-ttu-id="11eae-119">**GetClassID**</span><span class="sxs-lookup"><span data-stu-id="11eae-119">**GetClassID**</span></span>](csystemclock-getclassid.md)         | <span data-ttu-id="11eae-120">Gibt den Klassen Bezeichner (CLSID) des-Objekts zurück.</span><span class="sxs-lookup"><span data-stu-id="11eae-120">Returns the class identifier (CLSID) of the object.</span></span> |



 

 

 



