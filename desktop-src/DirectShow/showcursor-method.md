---
description: Die ShowCursor-Methode macht den Cursor sichtbar, wenn sich das mswebdvd-Objekt im Vollbildmodus befindet.
ms.assetid: 3a611cc8-7979-473d-bd0f-f4ca43701c63
title: ShowCursor-Methode
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 917c1d0d2724259fc19baf72ab6b3844cddc3419
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103860315"
---
# <a name="showcursor-method"></a><span data-ttu-id="7d6a7-103">ShowCursor-Methode</span><span class="sxs-lookup"><span data-stu-id="7d6a7-103">ShowCursor Method</span></span>

> [!Note]  
> <span data-ttu-id="7d6a7-104">Diese Komponente ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="7d6a7-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="7d6a7-105">Es kann in nachfolgenden Versionen geändert oder entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="7d6a7-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="7d6a7-106">Die- `ShowCursor` Methode macht den Cursor sichtbar, wenn sich das **mswebdvd** -Objekt im Vollbildmodus befindet.</span><span class="sxs-lookup"><span data-stu-id="7d6a7-106">The `ShowCursor` method makes the cursor visible when the **MSWebDVD** object is in full-screen mode.</span></span>

``` syntax
MSWebDVD.ShowCursor(bShow)
```

## <a name="parameters"></a><span data-ttu-id="7d6a7-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="7d6a7-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7d6a7-108"><span id="bShow"></span><span id="bshow"></span><span id="BSHOW"></span>*bShow*</span><span class="sxs-lookup"><span data-stu-id="7d6a7-108"><span id="bShow"></span><span id="bshow"></span><span id="BSHOW"></span>*bShow*</span></span>
</dt> <dd>

<span data-ttu-id="7d6a7-109">Gibt an, ob der Cursor als boolescher Wert angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="7d6a7-109">Specifies whether to show the cursor as a Boolean.</span></span>



| <span data-ttu-id="7d6a7-110">Wert</span><span class="sxs-lookup"><span data-stu-id="7d6a7-110">Value</span></span> | <span data-ttu-id="7d6a7-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7d6a7-111">Description</span></span>            |
|-------|------------------------|
| <span data-ttu-id="7d6a7-112">true</span><span class="sxs-lookup"><span data-stu-id="7d6a7-112">true</span></span>  | <span data-ttu-id="7d6a7-113">Cursor wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="7d6a7-113">Show the cursor</span></span>        |
| <span data-ttu-id="7d6a7-114">false</span><span class="sxs-lookup"><span data-stu-id="7d6a7-114">false</span></span> | <span data-ttu-id="7d6a7-115">Cursor nicht anzeigen</span><span class="sxs-lookup"><span data-stu-id="7d6a7-115">Do not show the cursor</span></span> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7d6a7-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7d6a7-116">Return Value</span></span>

<span data-ttu-id="7d6a7-117">Kein Rückgabewert.</span><span class="sxs-lookup"><span data-stu-id="7d6a7-117">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="7d6a7-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7d6a7-118">Remarks</span></span>

<span data-ttu-id="7d6a7-119">Wenn die DVD-Anzeige in den Vollbildmodus wechselt, verschwindet der Cursor innerhalb von 3 bis 5 Sekunden.</span><span class="sxs-lookup"><span data-stu-id="7d6a7-119">When the DVD display goes into full-screen mode, the cursor disappears within 3 to 5 seconds.</span></span> <span data-ttu-id="7d6a7-120">Verwenden Sie diese Methode, um den Cursor wieder sichtbar zu machen, wenn die Steuerelemente der Anwendung im Vollbildmodus sichtbar sind.</span><span class="sxs-lookup"><span data-stu-id="7d6a7-120">Use this method to make the cursor visible again if your application's control buttons are visible in full-screen mode.</span></span>

 

 



