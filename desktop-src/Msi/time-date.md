---
description: Der Datums-/Uhrzeittyp verfügt über die Uhrzeit und das Datum, das einzeln gespeichert wird. dabei werden Ganzzahlen ohne Vorzeichen als Bitfelder verwendet, die wie folgt verpackt werden.
ms.assetid: 02c6076e-7f81-489c-9997-1435dec81852
title: Time/Date
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b973143c2043419e4a54348917aa5d38fa97ff67
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106360599"
---
# <a name="timedate"></a><span data-ttu-id="fa807-103">Time/Date</span><span class="sxs-lookup"><span data-stu-id="fa807-103">Time/Date</span></span>

<span data-ttu-id="fa807-104">Der Datums-/Uhrzeittyp verfügt über die Uhrzeit und das Datum, das einzeln gespeichert wird. dabei werden Ganzzahlen ohne Vorzeichen als Bitfelder verwendet, die wie folgt verpackt werden.</span><span class="sxs-lookup"><span data-stu-id="fa807-104">The Time/Date data type has the time and the date stored individually, using unsigned integers as bit fields, packed as follows.</span></span>

## <a name="time"></a><span data-ttu-id="fa807-105">Time</span><span class="sxs-lookup"><span data-stu-id="fa807-105">Time</span></span>

<span data-ttu-id="fa807-106">Die Zeit wird in einer nicht signierten 2-Byte-Ganzzahl mit den folgenden Bitfeldern codiert.</span><span class="sxs-lookup"><span data-stu-id="fa807-106">Time is encoded in an unsigned 2-byte integer with the following bit fields.</span></span>



| <span data-ttu-id="fa807-107">Inhalte</span><span class="sxs-lookup"><span data-stu-id="fa807-107">Contents</span></span>           | <span data-ttu-id="fa807-108">Bits</span><span class="sxs-lookup"><span data-stu-id="fa807-108">Bits</span></span>        | <span data-ttu-id="fa807-109">Wertebereich</span><span class="sxs-lookup"><span data-stu-id="fa807-109">Value range</span></span> |
|--------------------|-------------|-------------|
| <span data-ttu-id="fa807-110">Stunden</span><span class="sxs-lookup"><span data-stu-id="fa807-110">hours</span></span>              | <span data-ttu-id="fa807-111">0 1 2 3 4</span><span class="sxs-lookup"><span data-stu-id="fa807-111">0 1 2 3 4</span></span>   | <span data-ttu-id="fa807-112">0–23</span><span class="sxs-lookup"><span data-stu-id="fa807-112">0–23</span></span>        |
| <span data-ttu-id="fa807-113">minutes</span><span class="sxs-lookup"><span data-stu-id="fa807-113">minutes</span></span>            | <span data-ttu-id="fa807-114">5 6 7 8 9 A</span><span class="sxs-lookup"><span data-stu-id="fa807-114">5 6 7 8 9 A</span></span> | <span data-ttu-id="fa807-115">0–59</span><span class="sxs-lookup"><span data-stu-id="fa807-115">0–59</span></span>        |
| <span data-ttu-id="fa807-116">2-Sekunden-Intervalle</span><span class="sxs-lookup"><span data-stu-id="fa807-116">2-second intervals</span></span> | <span data-ttu-id="fa807-117">B C D E F</span><span class="sxs-lookup"><span data-stu-id="fa807-117">B C D E F</span></span>   | <span data-ttu-id="fa807-118">0 – 29</span><span class="sxs-lookup"><span data-stu-id="fa807-118">0–29</span></span>        |



 

## <a name="date"></a><span data-ttu-id="fa807-119">Date</span><span class="sxs-lookup"><span data-stu-id="fa807-119">Date</span></span>

<span data-ttu-id="fa807-120">Das Datum wird in einer nicht signierten 2-Byte-Ganzzahl mit den folgenden Bitfeldern codiert.</span><span class="sxs-lookup"><span data-stu-id="fa807-120">Date is encoded in an unsigned 2-byte integer with the following bit fields.</span></span>



| <span data-ttu-id="fa807-121">Inhalte</span><span class="sxs-lookup"><span data-stu-id="fa807-121">Contents</span></span> | <span data-ttu-id="fa807-122">Bits</span><span class="sxs-lookup"><span data-stu-id="fa807-122">Bits</span></span>          | <span data-ttu-id="fa807-123">Wertebereich</span><span class="sxs-lookup"><span data-stu-id="fa807-123">Value range</span></span>              |
|----------|---------------|--------------------------|
| <span data-ttu-id="fa807-124">year</span><span class="sxs-lookup"><span data-stu-id="fa807-124">year</span></span>     | <span data-ttu-id="fa807-125">0 1 2 3 4 5 6</span><span class="sxs-lookup"><span data-stu-id="fa807-125">0 1 2 3 4 5 6</span></span> | <span data-ttu-id="fa807-126">0 – 119 (relativ zu 1980)</span><span class="sxs-lookup"><span data-stu-id="fa807-126">0–119 (relative to 1980)</span></span> |
| <span data-ttu-id="fa807-127">month</span><span class="sxs-lookup"><span data-stu-id="fa807-127">month</span></span>    | <span data-ttu-id="fa807-128">7 8 9 A</span><span class="sxs-lookup"><span data-stu-id="fa807-128">7 8 9 A</span></span>       | <span data-ttu-id="fa807-129">1–12</span><span class="sxs-lookup"><span data-stu-id="fa807-129">1–12</span></span>                     |
| <span data-ttu-id="fa807-130">day</span><span class="sxs-lookup"><span data-stu-id="fa807-130">day</span></span>      | <span data-ttu-id="fa807-131">B C D E F</span><span class="sxs-lookup"><span data-stu-id="fa807-131">B C D E F</span></span>     | <span data-ttu-id="fa807-132">1–31</span><span class="sxs-lookup"><span data-stu-id="fa807-132">1–31</span></span>                     |



 

 

 



