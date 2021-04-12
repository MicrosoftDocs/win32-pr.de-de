---
title: Portieren von Akkumulations Puffer aufrufen
description: Sie müssen ihren Akkumulations Puffer zuordnen, indem Sie das entsprechende Pixel Format mit der OpenGL-Funktion "-"
ms.assetid: 523728ce-4aae-4247-a3dc-23864231cad1
keywords:
- IRIS GL portieren, Akkumulations Puffer
- Portieren von IRIS GL, Akkumulations Puffer
- Portieren auf OpenGL von IRIS GL, Akkumulations Puffer
- OpenGL-Portierung von IRIS GL, Akkumulations Puffer
- Akkumulations Puffer OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91ca91cb3ba35535ba2470297070dffc932a1c33
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104207411"
---
# <a name="porting-accumulation-buffer-calls"></a><span data-ttu-id="715fb-108">Portieren von Akkumulations Puffer aufrufen</span><span class="sxs-lookup"><span data-stu-id="715fb-108">Porting Accumulation Buffer Calls</span></span>

<span data-ttu-id="715fb-109">Sie müssen ihren Akkumulations Puffer zuordnen, indem Sie das entsprechende Pixel Format mit **der OpenGL-** [**Funktion "**](/windows/desktop/api/wingdi/nf-wingdi-choosepixelformat) -"</span><span class="sxs-lookup"><span data-stu-id="715fb-109">You must allocate your accumulation buffer by requesting the appropriate pixel format with the OpenGL **auxInitDisplayMode** or [**ChoosePixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-choosepixelformat) function.</span></span> <span data-ttu-id="715fb-110">In der folgenden Tabelle sind IRIS GL-Funktionen aufgelistet, die sich auf den Akkumulations Puffer und ihre entsprechenden OpenGL-Funktionen auswirken</span><span class="sxs-lookup"><span data-stu-id="715fb-110">The following table lists IRIS GL functions that affect the accumulation buffer and their equivalent OpenGL functions.</span></span>



| <span data-ttu-id="715fb-111">IRIS GL-Funktion</span><span class="sxs-lookup"><span data-stu-id="715fb-111">IRIS GL function</span></span>       | <span data-ttu-id="715fb-112">OpenGL-Funktion</span><span class="sxs-lookup"><span data-stu-id="715fb-112">OpenGL function</span></span>                                       | <span data-ttu-id="715fb-113">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="715fb-113">Meaning</span></span>                                                                       |
|------------------------|-------------------------------------------------------|-------------------------------------------------------------------------------|
| <span data-ttu-id="715fb-114">**acsize**</span><span class="sxs-lookup"><span data-stu-id="715fb-114">**acsize**</span></span>             | <span data-ttu-id="715fb-115"> "" "" "" "  " "" "" "" ""</span><span class="sxs-lookup"><span data-stu-id="715fb-115">**auxInitDisplayMode** or **ChoosePixelFormat**</span></span>       | <span data-ttu-id="715fb-116">Gibt die Anzahl der bitplane pro Farbkomponente im Akkumulations Puffer an.</span><span class="sxs-lookup"><span data-stu-id="715fb-116">Specifies number of bitplanes per color component in the accumulation buffer.</span></span> |
| <span data-ttu-id="715fb-117">**acbuf**</span><span class="sxs-lookup"><span data-stu-id="715fb-117">**acbuf**</span></span>              | [<span data-ttu-id="715fb-118">**glaccum**</span><span class="sxs-lookup"><span data-stu-id="715fb-118">**glAccum**</span></span>](glaccum.md)                            | <span data-ttu-id="715fb-119">Arbeitet auf dem Akkumulations Puffer.</span><span class="sxs-lookup"><span data-stu-id="715fb-119">Operates on the accumulation buffer.</span></span>                                          |
|                        | [<span data-ttu-id="715fb-120">**glclearaccum**</span><span class="sxs-lookup"><span data-stu-id="715fb-120">**glClearAccum**</span></span>](glclearaccum.md)                  | <span data-ttu-id="715fb-121">Legt eindeutige Werte für den Akkumulations Puffer fest.</span><span class="sxs-lookup"><span data-stu-id="715fb-121">Sets clear values for accumulation buffer.</span></span>                                    |
| <span data-ttu-id="715fb-122">**acbuf**(AC \_ Clear)</span><span class="sxs-lookup"><span data-stu-id="715fb-122">**acbuf**( AC\_CLEAR )</span></span> | <span data-ttu-id="715fb-123">[**glClear**](glclear.md) (GL- \_ Accum- \_ Puffer \_ Bit)</span><span class="sxs-lookup"><span data-stu-id="715fb-123">[**glClear**](glclear.md) ( GL\_ACCUM\_BUFFER\_BIT )</span></span> | <span data-ttu-id="715fb-124">Löscht den Akkumulations Puffer.</span><span class="sxs-lookup"><span data-stu-id="715fb-124">Clears the accumulation buffer.</span></span>                                               |



 

<span data-ttu-id="715fb-125">In der folgenden Tabelle werden die Iris GL- **acbuf** -Parameter zusammen mit den entsprechenden OpenGL- [**glaccum**](glaccum.md) -Parametern aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="715fb-125">The following table lists the IRIS GL **acbuf** parameters along with the equivalent OpenGL [**glAccum**](glaccum.md) parameters.</span></span>



| <span data-ttu-id="715fb-126">IRIS GL-Parameter</span><span class="sxs-lookup"><span data-stu-id="715fb-126">IRIS GL parameter</span></span>     | <span data-ttu-id="715fb-127">OpenGL-Parameter</span><span class="sxs-lookup"><span data-stu-id="715fb-127">OpenGL parameter</span></span> |
|-----------------------|------------------|
| <span data-ttu-id="715fb-128">\_Akkumulierung</span><span class="sxs-lookup"><span data-stu-id="715fb-128">AC\_ACCUMULATE</span></span>        | <span data-ttu-id="715fb-129">GL- \_ Accum</span><span class="sxs-lookup"><span data-stu-id="715fb-129">GL\_ACCUM</span></span>        |
| <span data-ttu-id="715fb-130">Wechsel \_ Stromversorgung \_</span><span class="sxs-lookup"><span data-stu-id="715fb-130">AC\_CLEAR\_ACCUMULATE</span></span> | <span data-ttu-id="715fb-131">GL \_ Laden</span><span class="sxs-lookup"><span data-stu-id="715fb-131">GL\_LOAD</span></span>         |
| <span data-ttu-id="715fb-132">AC- \_ Rückgabe</span><span class="sxs-lookup"><span data-stu-id="715fb-132">AC\_RETURN</span></span>            | <span data-ttu-id="715fb-133">GL- \_ Rückgabe</span><span class="sxs-lookup"><span data-stu-id="715fb-133">GL\_RETURN</span></span>       |
| <span data-ttu-id="715fb-134">AC- \_ mult</span><span class="sxs-lookup"><span data-stu-id="715fb-134">AC\_MULT</span></span>              | <span data-ttu-id="715fb-135">GL \_ .</span><span class="sxs-lookup"><span data-stu-id="715fb-135">GL\_MULT</span></span>         |
| <span data-ttu-id="715fb-136">AC \_ Hinzufügen</span><span class="sxs-lookup"><span data-stu-id="715fb-136">AC\_ADD</span></span>               | <span data-ttu-id="715fb-137">GL \_ Hinzufügen</span><span class="sxs-lookup"><span data-stu-id="715fb-137">GL\_ADD</span></span>          |



 

 

 




