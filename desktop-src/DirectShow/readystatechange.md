---
description: Das Ereignis "Read ystatechange" wird gesendet, wenn sich die Eigenschaft "Read-State" des mswebdvd-Steuer Elements geändert hat.
ms.assetid: 814a09e1-2e85-4ea3-9135-8377dc2acf64
title: "\"Leserystatechange\""
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 46cc8d7ffdee650aac48839d49ed8162e10bb955
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104522048"
---
# <a name="readystatechange"></a><span data-ttu-id="7a8c5-103">"Leserystatechange"</span><span class="sxs-lookup"><span data-stu-id="7a8c5-103">ReadyStateChange</span></span>

> [!Note]  
> <span data-ttu-id="7a8c5-104">Diese Komponente ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="7a8c5-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="7a8c5-105">Es kann in nachfolgenden Versionen geändert oder entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="7a8c5-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="7a8c5-106">Das `ReadyStateChange` Ereignis wird gesendet, wenn die Eigenschaft "read- **State** " des mswebdvd-Steuer Elements geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="7a8c5-106">The `ReadyStateChange` event is sent when the **ReadyState** property of the MSWebDVD control has changed.</span></span>

``` syntax
ReadyStateChange(ReadyState)
```

## <a name="parameters"></a><span data-ttu-id="7a8c5-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="7a8c5-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7a8c5-108"><span id="ReadyState"></span><span id="readystate"></span><span id="READYSTATE"></span>*ReadyState*</span><span class="sxs-lookup"><span data-stu-id="7a8c5-108"><span id="ReadyState"></span><span id="readystate"></span><span id="READYSTATE"></span>*ReadyState*</span></span>
</dt> <dd>

<span data-ttu-id="7a8c5-109">Gibt den neuen Wert der Eigenschaft " [**leserystate**](readystate-property.md) " an.</span><span class="sxs-lookup"><span data-stu-id="7a8c5-109">Specifies the new value of the [**ReadyState**](readystate-property.md) property.</span></span>



| <span data-ttu-id="7a8c5-110">Wert</span><span class="sxs-lookup"><span data-stu-id="7a8c5-110">Value</span></span> | <span data-ttu-id="7a8c5-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7a8c5-111">Description</span></span>               |
|-------|---------------------------|
| <span data-ttu-id="7a8c5-112">0</span><span class="sxs-lookup"><span data-stu-id="7a8c5-112">0</span></span>     | <span data-ttu-id="7a8c5-113">"Read ystate" ist \_ nicht initialisiert.</span><span class="sxs-lookup"><span data-stu-id="7a8c5-113">READYSTATE\_UNINITIALIZED</span></span> |
| <span data-ttu-id="7a8c5-114">1</span><span class="sxs-lookup"><span data-stu-id="7a8c5-114">1</span></span>     | <span data-ttu-id="7a8c5-115">Laden von "Read ystate" \_</span><span class="sxs-lookup"><span data-stu-id="7a8c5-115">READYSTATE\_LOADING</span></span>       |
| <span data-ttu-id="7a8c5-116">2</span><span class="sxs-lookup"><span data-stu-id="7a8c5-116">2</span></span>     | <span data-ttu-id="7a8c5-117">"Read ystate" \_ geladen</span><span class="sxs-lookup"><span data-stu-id="7a8c5-117">READYSTATE\_LOADED</span></span>        |
| <span data-ttu-id="7a8c5-118">3</span><span class="sxs-lookup"><span data-stu-id="7a8c5-118">3</span></span>     | <span data-ttu-id="7a8c5-119">Read-State \_ interaktiv</span><span class="sxs-lookup"><span data-stu-id="7a8c5-119">READYSTATE\_INTERACTIVE</span></span>   |
| <span data-ttu-id="7a8c5-120">4</span><span class="sxs-lookup"><span data-stu-id="7a8c5-120">4</span></span>     | <span data-ttu-id="7a8c5-121">Read-State ist fertiggestellt. \_</span><span class="sxs-lookup"><span data-stu-id="7a8c5-121">READYSTATE\_COMPLETE</span></span>      |



 

</dd> </dl>

 

 



