---
description: Die "Read-State"-Eigenschaft ruft den "Read ystate" des mswebdvd-Objekts ab.
ms.assetid: e43b0fa4-4a5a-4492-a6a9-bf271f58e11b
title: "\"Leserystate\"-Eigenschaft (\"ocidl. h\")"
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- READYSTATE
api_type:
- HeaderDef
api_location:
- ocidl.h
ms.openlocfilehash: a52b20349c58e8bd44458266da6a0a33ea149c98
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106366978"
---
# <a name="readystate-property"></a><span data-ttu-id="991d4-103">Eigenschaft "leserystate"</span><span class="sxs-lookup"><span data-stu-id="991d4-103">ReadyState Property</span></span>

> [!Note]  
> <span data-ttu-id="991d4-104">Diese Komponente ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="991d4-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="991d4-105">Es kann in nachfolgenden Versionen geändert oder entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="991d4-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="991d4-106">Die- `ReadyState` Eigenschaft ruft den "Read ystate" des **mswebdvd** -Objekts ab.</span><span class="sxs-lookup"><span data-stu-id="991d4-106">The `ReadyState` property retrieves the ReadyState of the **MSWebDVD** object.</span></span>

``` syntax
[ iReadyState = ] MSWebDVD.ReadyState
```

## <a name="return-value"></a><span data-ttu-id="991d4-107">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="991d4-107">Return Value</span></span>

<span data-ttu-id="991d4-108">Gibt einen ganzzahligen Wert zurück, der den Read-State des Steuer Elements darstellt.</span><span class="sxs-lookup"><span data-stu-id="991d4-108">Returns an integer value representing the control's ReadyState.</span></span>



| <span data-ttu-id="991d4-109">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="991d4-109">Return code</span></span> | <span data-ttu-id="991d4-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="991d4-110">Description</span></span>                                               |
|-------------|-----------------------------------------------------------|
| <span data-ttu-id="991d4-111">0</span><span class="sxs-lookup"><span data-stu-id="991d4-111">0</span></span>           | <span data-ttu-id="991d4-112">Standard Initialisierungs Zustand.</span><span class="sxs-lookup"><span data-stu-id="991d4-112">Default initialization state.</span></span>                             |
| <span data-ttu-id="991d4-113">1</span><span class="sxs-lookup"><span data-stu-id="991d4-113">1</span></span>           | <span data-ttu-id="991d4-114">Das Objekt lädt seine Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="991d4-114">Object is loading its properties.</span></span>                         |
| <span data-ttu-id="991d4-115">2</span><span class="sxs-lookup"><span data-stu-id="991d4-115">2</span></span>           | <span data-ttu-id="991d4-116">Das Objekt wurde initialisiert.</span><span class="sxs-lookup"><span data-stu-id="991d4-116">Object has been initialized.</span></span>                              |
| <span data-ttu-id="991d4-117">3</span><span class="sxs-lookup"><span data-stu-id="991d4-117">3</span></span>           | <span data-ttu-id="991d4-118">Das Objekt ist interaktiv, aber nicht alle Daten sind verfügbar.</span><span class="sxs-lookup"><span data-stu-id="991d4-118">Object is interactive, but not all its data is available.</span></span> |
| <span data-ttu-id="991d4-119">4</span><span class="sxs-lookup"><span data-stu-id="991d4-119">4</span></span>           | <span data-ttu-id="991d4-120">Das Objekt hat alle zugehörigen Daten empfangen.</span><span class="sxs-lookup"><span data-stu-id="991d4-120">Object has received all its data.</span></span>                         |



 

## <a name="remarks"></a><span data-ttu-id="991d4-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="991d4-121">Remarks</span></span>

<span data-ttu-id="991d4-122">Diese Eigenschaft ist schreibgeschützt und weist keinen Standardwert auf.</span><span class="sxs-lookup"><span data-stu-id="991d4-122">This property is read-only with no default value.</span></span>

<span data-ttu-id="991d4-123">Jedes in eine Webseite eingebettete Objekt macht die- `ReadyState` Eigenschaft verfügbar.</span><span class="sxs-lookup"><span data-stu-id="991d4-123">Any object embedded in a Web page exposes the `ReadyState` property.</span></span>

## <a name="requirements"></a><span data-ttu-id="991d4-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="991d4-124">Requirements</span></span>



| <span data-ttu-id="991d4-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="991d4-125">Requirement</span></span> | <span data-ttu-id="991d4-126">Wert</span><span class="sxs-lookup"><span data-stu-id="991d4-126">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="991d4-127">Header</span><span class="sxs-lookup"><span data-stu-id="991d4-127">Header</span></span><br/> | <dl> <span data-ttu-id="991d4-128"><dt>"Ocidl. h"</dt></span><span class="sxs-lookup"><span data-stu-id="991d4-128"><dt>Ocidl.h</dt></span></span> </dl> |



 

 




