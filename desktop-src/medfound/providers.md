---
description: Enthält eine Liste der Ablauf Verfolgungs Anbieter für MF Trace.
ms.assetid: ee483f0a-5a90-4150-ada4-0b63ae312523
title: providers-Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 04e5aaedcd14d840cfdc0d85559f6a7981943593
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215016"
---
# <a name="providers-element"></a><span data-ttu-id="d517a-103">providers-Element</span><span class="sxs-lookup"><span data-stu-id="d517a-103">providers element</span></span>

<span data-ttu-id="d517a-104">Enthält eine Liste der Ablauf Verfolgungs Anbieter für [MF Trace](mftrace.md).</span><span class="sxs-lookup"><span data-stu-id="d517a-104">Contains a list of trace providers for [MFTrace](mftrace.md).</span></span>

## <a name="usage"></a><span data-ttu-id="d517a-105">Verbrauch</span><span class="sxs-lookup"><span data-stu-id="d517a-105">Usage</span></span>

``` syntax
<providers>
  child elements
</providers>
```

## <a name="attributes"></a><span data-ttu-id="d517a-106">Attribute</span><span class="sxs-lookup"><span data-stu-id="d517a-106">Attributes</span></span>

<span data-ttu-id="d517a-107">Es gibt keine Attribute.</span><span class="sxs-lookup"><span data-stu-id="d517a-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="d517a-108">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d517a-108">Child elements</span></span>



| <span data-ttu-id="d517a-109">Element</span><span class="sxs-lookup"><span data-stu-id="d517a-109">Element</span></span>                                   | <span data-ttu-id="d517a-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d517a-110">Description</span></span>                                                                                                      |
|-------------------------------------------|------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d517a-111">**MF-Umleitungen**</span><span class="sxs-lookup"><span data-stu-id="d517a-111">**mfdetours**</span></span>](mfdetours.md)<br/> | <span data-ttu-id="d517a-112">Gibt den Media Foundation umleitet-Anbieter an, der Media Foundation API-Aufrufe verfolgt.</span><span class="sxs-lookup"><span data-stu-id="d517a-112">Specifies the Media Foundation Detours provider, which traces Media Foundation API calls.</span></span><br/> <br/> |
| [<span data-ttu-id="d517a-113">**ab**</span><span class="sxs-lookup"><span data-stu-id="d517a-113">**provider**</span></span>](provider.md)<br/>   | <span data-ttu-id="d517a-114">Gibt einen Ablauf Verfolgungs Anbieter (ETW oder WPP) an.</span><span class="sxs-lookup"><span data-stu-id="d517a-114">Specifies a trace provider (ETW or WPP).</span></span><br/> <br/>                                                  |



### <a name="child-element-sequence"></a><span data-ttu-id="d517a-115">Sequenz untergeordneter Elemente</span><span class="sxs-lookup"><span data-stu-id="d517a-115">Child element sequence</span></span>

``` syntax
(
  mfdetours?, 
  provider*
)
```

## <a name="parent-elements"></a><span data-ttu-id="d517a-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d517a-116">Parent elements</span></span>

<span data-ttu-id="d517a-117">Es gibt keine übergeordneten Elemente.</span><span class="sxs-lookup"><span data-stu-id="d517a-117">There are no parent elements.</span></span>

## <a name="element-information"></a><span data-ttu-id="d517a-118">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="d517a-118">Element information</span></span>



|              |     |
|--------------|-----|
| <span data-ttu-id="d517a-119">Kann leer bleiben</span><span class="sxs-lookup"><span data-stu-id="d517a-119">Can be empty</span></span> | <span data-ttu-id="d517a-120">Ja</span><span class="sxs-lookup"><span data-stu-id="d517a-120">Yes</span></span> |



## <a name="see-also"></a><span data-ttu-id="d517a-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d517a-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d517a-122">MF-Ablauf Verfolgungs Konfigurationsdatei</span><span class="sxs-lookup"><span data-stu-id="d517a-122">MFTrace Configuration File</span></span>](mftrace-configuration-file.md)
</dt> </dl>

 

 




