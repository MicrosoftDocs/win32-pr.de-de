---
description: Entfernt die Anbieter Registrierung.
ms.assetid: e52c1ee0-140a-4277-bddd-d93338a512bc
title: Countercleanup-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CounterCleanup
api_type:
- NA
api_location: ''
ms.openlocfilehash: eb768d3152aad5401c30b18a3f1ff13d1ef2397d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106368749"
---
# <a name="countercleanup-function"></a><span data-ttu-id="17d5d-103">Countercleanup-Funktion</span><span class="sxs-lookup"><span data-stu-id="17d5d-103">CounterCleanup function</span></span>

<span data-ttu-id="17d5d-104">Entfernt die Anbieter Registrierung.</span><span class="sxs-lookup"><span data-stu-id="17d5d-104">Removes the provider's registration.</span></span>

## <a name="syntax"></a><span data-ttu-id="17d5d-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="17d5d-105">Syntax</span></span>


```C++
void WINAPI CounterCleanup(void);
```



## <a name="parameters"></a><span data-ttu-id="17d5d-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="17d5d-106">Parameters</span></span>

<span data-ttu-id="17d5d-107">Diese Funktion besitzt keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="17d5d-107">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="17d5d-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="17d5d-108">Return value</span></span>

<span data-ttu-id="17d5d-109">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="17d5d-109">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="17d5d-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="17d5d-110">Remarks</span></span>

<span data-ttu-id="17d5d-111">Der Anbieter ruft diese Funktion auf.</span><span class="sxs-lookup"><span data-stu-id="17d5d-111">Your provider calls this function.</span></span> <span data-ttu-id="17d5d-112">Die-Funktion Ruft die [**perfstopprovider**](/windows/desktop/api/Perflib/nf-perflib-perfstopprovider) -Funktion auf, um die Registrierung des Anbieters zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="17d5d-112">The function calls the [**PerfStopProvider**](/windows/desktop/api/Perflib/nf-perflib-perfstopprovider) function to remove the provider's registration.</span></span>

<span data-ttu-id="17d5d-113">Das [**ctrpp**](ctrpp.md) -Tool generiert diese Inline Funktion, wenn Sie das **-o-** Argument angeben.</span><span class="sxs-lookup"><span data-stu-id="17d5d-113">The [**CTRPP**](ctrpp.md) tool generates this inline function when you specify the **-o** argument.</span></span> <span data-ttu-id="17d5d-114">Der Name der Funktion enthält eine *Präfix* Zeichenfolge, wenn Sie das Argument **-prefix** angeben (z. b. **_prefix_CounterCleanup**.</span><span class="sxs-lookup"><span data-stu-id="17d5d-114">The function's name includes a *prefix* string if you specify the **-prefix** argument (for example, **_prefix_CounterCleanup**.</span></span>

## <a name="requirements"></a><span data-ttu-id="17d5d-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="17d5d-115">Requirements</span></span>



| <span data-ttu-id="17d5d-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="17d5d-116">Requirement</span></span> | <span data-ttu-id="17d5d-117">Wert</span><span class="sxs-lookup"><span data-stu-id="17d5d-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="17d5d-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="17d5d-118">Minimum supported client</span></span><br/> | <span data-ttu-id="17d5d-119">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="17d5d-119">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="17d5d-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="17d5d-120">Minimum supported server</span></span><br/> | <span data-ttu-id="17d5d-121">Nur Windows Server 2008 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="17d5d-121">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



 

 




