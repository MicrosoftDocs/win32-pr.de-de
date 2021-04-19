---
description: Die playstate-Eigenschaft ruft den aktuellen Zustand des mswebdvd-Objekts ab.
ms.assetid: ffe71c3f-f8c2-45cc-84bf-e937cfbbe7b9
title: Playstate (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9d8c699ce3f232f9afc14472f0308fa65adc6abb
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106346818"
---
# <a name="playstate-property"></a><span data-ttu-id="ab65e-103">Playstate (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="ab65e-103">PlayState Property</span></span>

> [!Note]  
> <span data-ttu-id="ab65e-104">Diese Komponente ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="ab65e-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="ab65e-105">Es kann in nachfolgenden Versionen geändert oder entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="ab65e-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="ab65e-106">Die- `PlayState` Eigenschaft ruft den aktuellen Zustand des **mswebdvd** -Objekts ab.</span><span class="sxs-lookup"><span data-stu-id="ab65e-106">The `PlayState` property retrieves the current state of the **MSWebDVD** object.</span></span>

``` syntax
[ iState = ] MSWebDVD.PlayState
```

## <a name="return-value"></a><span data-ttu-id="ab65e-107">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ab65e-107">Return Value</span></span>

<span data-ttu-id="ab65e-108">Gibt einen ganzzahligen Wert zurück, der den aktuellen Zustand des DVD-Navigators darstellt.</span><span class="sxs-lookup"><span data-stu-id="ab65e-108">Returns an Integer value representing the current state of the DVD Navigator.</span></span>



| <span data-ttu-id="ab65e-109">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="ab65e-109">Return code</span></span> | <span data-ttu-id="ab65e-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ab65e-110">Description</span></span>   |
|-------------|---------------|
| <span data-ttu-id="ab65e-111">-2</span><span class="sxs-lookup"><span data-stu-id="ab65e-111">-2</span></span>          | <span data-ttu-id="ab65e-112">Nicht definiert</span><span class="sxs-lookup"><span data-stu-id="ab65e-112">Undefined</span></span>     |
| <span data-ttu-id="ab65e-113">-1</span><span class="sxs-lookup"><span data-stu-id="ab65e-113">-1</span></span>          | <span data-ttu-id="ab65e-114">Uninitialized</span><span class="sxs-lookup"><span data-stu-id="ab65e-114">Uninitialized</span></span> |
| <span data-ttu-id="ab65e-115">0</span><span class="sxs-lookup"><span data-stu-id="ab65e-115">0</span></span>           | <span data-ttu-id="ab65e-116">Beendet</span><span class="sxs-lookup"><span data-stu-id="ab65e-116">Stopped</span></span>       |
| <span data-ttu-id="ab65e-117">1</span><span class="sxs-lookup"><span data-stu-id="ab65e-117">1</span></span>           | <span data-ttu-id="ab65e-118">Angehalten</span><span class="sxs-lookup"><span data-stu-id="ab65e-118">Paused</span></span>        |
| <span data-ttu-id="ab65e-119">2</span><span class="sxs-lookup"><span data-stu-id="ab65e-119">2</span></span>           | <span data-ttu-id="ab65e-120">Wird ausgeführt</span><span class="sxs-lookup"><span data-stu-id="ab65e-120">Running</span></span>       |



 

## <a name="remarks"></a><span data-ttu-id="ab65e-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ab65e-121">Remarks</span></span>

<span data-ttu-id="ab65e-122">Diese Eigenschaft ist schreibgeschützt und weist keinen Standardwert auf.</span><span class="sxs-lookup"><span data-stu-id="ab65e-122">This property is read-only with no default value.</span></span>

<span data-ttu-id="ab65e-123">Das **mswebdvd** -Objekt steuert den DirectShow-DVD-Navigator-Filter, der die eigentliche Arbeit der DVD-Navigation übernimmt.</span><span class="sxs-lookup"><span data-stu-id="ab65e-123">The **MSWebDVD** object controls the DirectShow DVD Navigator filter, which does the actual work of DVD navigation.</span></span> <span data-ttu-id="ab65e-124">Es handelt sich tatsächlich um den Status des DVD-Navigators, auf den diese Eigenschaft verweist.</span><span class="sxs-lookup"><span data-stu-id="ab65e-124">It is actually the state of the DVD Navigator that this property refers to.</span></span> <span data-ttu-id="ab65e-125">Der DVD-Navigator kann einen von mehreren Zuständen aufweisen, wie oben beschrieben.</span><span class="sxs-lookup"><span data-stu-id="ab65e-125">The DVD Navigator can be in one of several states, as described above.</span></span> <span data-ttu-id="ab65e-126">Die- `PlayState` Eigenschaft kann als Diagnosetool nützlich sein, aber im Allgemeinen sollte es für eine Skript Anwendung keinen Grund geben, den Status des DVD-Navigators zu überwachen.</span><span class="sxs-lookup"><span data-stu-id="ab65e-126">The `PlayState` property can be useful as a diagnostic tool, but generally there should be no reason for a scripting application to monitor the state of the DVD Navigator.</span></span>

 

 



