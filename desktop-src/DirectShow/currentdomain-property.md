---
description: Die CurrentDomain-Eigenschaft ruft die DVD-Domäne ab, in der sich das mswebdvd-Objekt befindet.
ms.assetid: 9d545438-9a3d-4c57-a3df-5e75af2e4d1b
title: CurrentDomain (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ead6d61cd622fceac2a4d133a0297892992e763a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104481862"
---
# <a name="currentdomain-property"></a><span data-ttu-id="1aadd-103">CurrentDomain (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="1aadd-103">CurrentDomain Property</span></span>

> [!Note]  
> <span data-ttu-id="1aadd-104">Diese Komponente ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="1aadd-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="1aadd-105">Es kann in nachfolgenden Versionen geändert oder entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="1aadd-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="1aadd-106">Die- `CurrentDomain` Eigenschaft ruft die DVD-Domäne ab, in der sich das mswebdvd-Objekt befindet.</span><span class="sxs-lookup"><span data-stu-id="1aadd-106">The `CurrentDomain` property retrieves the DVD domain that the MSWebDVD object is in.</span></span>

``` syntax
[ iDomain = ] MSWebDVD.CurrentDomain
```

## <a name="return-value"></a><span data-ttu-id="1aadd-107">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1aadd-107">Return Value</span></span>

<span data-ttu-id="1aadd-108">Gibt einen ganzzahligen Wert zurück, der die aktuelle Domäne darstellt.</span><span class="sxs-lookup"><span data-stu-id="1aadd-108">Returns an integer value representing the current domain.</span></span>

## <a name="remarks"></a><span data-ttu-id="1aadd-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1aadd-109">Remarks</span></span>

<span data-ttu-id="1aadd-110">Die möglichen Werte der-Eigenschaft sind:</span><span class="sxs-lookup"><span data-stu-id="1aadd-110">The possible values of the property are:</span></span>



| <span data-ttu-id="1aadd-111">Wert</span><span class="sxs-lookup"><span data-stu-id="1aadd-111">Value</span></span> | <span data-ttu-id="1aadd-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1aadd-112">Description</span></span>          |
|-------|----------------------|
| <span data-ttu-id="1aadd-113">1</span><span class="sxs-lookup"><span data-stu-id="1aadd-113">1</span></span>     | <span data-ttu-id="1aadd-114">Zuerst abspielen</span><span class="sxs-lookup"><span data-stu-id="1aadd-114">First play</span></span>           |
| <span data-ttu-id="1aadd-115">2</span><span class="sxs-lookup"><span data-stu-id="1aadd-115">2</span></span>     | <span data-ttu-id="1aadd-116">Video-Manager-Menü</span><span class="sxs-lookup"><span data-stu-id="1aadd-116">Video Manager Menu</span></span>   |
| <span data-ttu-id="1aadd-117">3</span><span class="sxs-lookup"><span data-stu-id="1aadd-117">3</span></span>     | <span data-ttu-id="1aadd-118">Menü "Video Titel Satz"</span><span class="sxs-lookup"><span data-stu-id="1aadd-118">Video Title Set Menu</span></span> |
| <span data-ttu-id="1aadd-119">4</span><span class="sxs-lookup"><span data-stu-id="1aadd-119">4</span></span>     | <span data-ttu-id="1aadd-120">Titel</span><span class="sxs-lookup"><span data-stu-id="1aadd-120">Title</span></span>                |
| <span data-ttu-id="1aadd-121">5</span><span class="sxs-lookup"><span data-stu-id="1aadd-121">5</span></span>     | <span data-ttu-id="1aadd-122">Stop</span><span class="sxs-lookup"><span data-stu-id="1aadd-122">Stop</span></span>                 |



 

<span data-ttu-id="1aadd-123">Mit dieser Methode können Sie sicherstellen, dass sich der DVD-Navigator in einer gültigen Domäne für die aufzurufende Methode befindet.</span><span class="sxs-lookup"><span data-stu-id="1aadd-123">Call this method to ensure that the DVD Navigator is in a valid domain for the method you are about to call.</span></span> <span data-ttu-id="1aadd-124">Überprüfen Sie z. b. vor dem Aufrufen von [**playtitle**](playtitle-method.md)die- `CurrentDomain` Eigenschaft, um sicherzustellen, dass sich der DVD-Navigator nicht in der "beendet" oder "erste Wiedergabe"</span><span class="sxs-lookup"><span data-stu-id="1aadd-124">For example, before calling [**PlayTitle**](playtitle-method.md), check the `CurrentDomain` property to make sure that the DVD Navigator is not in the Stop or First Play domain.</span></span>

 

 



