---
description: Die canstep-Methode bestimmt, ob der MPEG-2-Decoder im lokalen System einen Frame Schritt in einer angegebenen Richtung ausführen kann.
ms.assetid: 21721722-0bf4-4cc7-a0e4-96b353888948
title: Canstep-Methode
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 506e7436e5ec79947aceeca69891e52074cf2ea7
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104041157"
---
# <a name="canstep-method"></a><span data-ttu-id="c23bc-103">Canstep-Methode</span><span class="sxs-lookup"><span data-stu-id="c23bc-103">CanStep Method</span></span>

> [!Note]  
> <span data-ttu-id="c23bc-104">Diese Komponente ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="c23bc-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="c23bc-105">Es kann in nachfolgenden Versionen geändert oder entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="c23bc-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="c23bc-106">Die `CanStep` -Methode bestimmt, ob der MPEG-2-Decoder im lokalen System Frame-Step in einer angegebenen Richtung ausführen kann.</span><span class="sxs-lookup"><span data-stu-id="c23bc-106">The `CanStep` method determines whether the MPEG-2 decoder on the local system can perform frame stepping in a specified direction.</span></span>

``` syntax
[ bCanStep = ] MSWebDVD.CanStep(bDirection)
```

## <a name="parameters"></a><span data-ttu-id="c23bc-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="c23bc-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c23bc-108"><span id="bDirection"></span><span id="bdirection"></span><span id="BDIRECTION"></span>*bdirection*</span><span class="sxs-lookup"><span data-stu-id="c23bc-108"><span id="bDirection"></span><span id="bdirection"></span><span id="BDIRECTION"></span>*bDirection*</span></span>
</dt> <dd>

<span data-ttu-id="c23bc-109">Boolescher Wert, der als Flag verwendet wird, um die Richtung (vorwärts oder rückwärts) der Rahmen Schritt Fähigkeit des Decoders anzugeben.</span><span class="sxs-lookup"><span data-stu-id="c23bc-109">Boolean used as a flag to specify the direction, forward or backward, of decoder's frame-stepping ability.</span></span>



| <span data-ttu-id="c23bc-110">Wert</span><span class="sxs-lookup"><span data-stu-id="c23bc-110">Value</span></span> | <span data-ttu-id="c23bc-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c23bc-111">Description</span></span>                                          |
|-------|------------------------------------------------------|
| <span data-ttu-id="c23bc-112">true</span><span class="sxs-lookup"><span data-stu-id="c23bc-112">true</span></span>  | <span data-ttu-id="c23bc-113">Kann der Decoder einen Schritt rückwärts ausführen?</span><span class="sxs-lookup"><span data-stu-id="c23bc-113">Can decoder step backward?</span></span>                           |
| <span data-ttu-id="c23bc-114">false</span><span class="sxs-lookup"><span data-stu-id="c23bc-114">false</span></span> | <span data-ttu-id="c23bc-115">Kann der Decoder einen Schritt vorwärts ausführen?</span><span class="sxs-lookup"><span data-stu-id="c23bc-115">Can decoder step forward?</span></span> <span data-ttu-id="c23bc-116">Dies ist der Standardwert.</span><span class="sxs-lookup"><span data-stu-id="c23bc-116">This is the default value.</span></span> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c23bc-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c23bc-117">Return Value</span></span>

<span data-ttu-id="c23bc-118">Gibt den booleschen Wert true zurück, wenn der Decoder in die angegebene Richtung wechseln kann, andernfalls false.</span><span class="sxs-lookup"><span data-stu-id="c23bc-118">Returns a Boolean value of true if the decoder can step in the specified direction, and false otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="c23bc-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c23bc-119">Remarks</span></span>

<span data-ttu-id="c23bc-120">Nicht alle Hardware-MPEG-2-Decoder unterstützen die neuen Frame Step-Funktionen in DirectShow® 8,0.</span><span class="sxs-lookup"><span data-stu-id="c23bc-120">Not all hardware MPEG-2 decoders support the new frame stepping capabilities in DirectShow® 8.0.</span></span> <span data-ttu-id="c23bc-121">Diese Methode fragt den Decoder nach seinen Frame-Step-Funktionen ab.</span><span class="sxs-lookup"><span data-stu-id="c23bc-121">This method queries the decoder for its frame stepping capabilities.</span></span> <span data-ttu-id="c23bc-122">Wenn der Decoder Frame-Stepping ausführen kann, kann eine Anwendung die [**Step**](step-method.md) -Methode verwenden, um Frames schrittweise zu durchlaufen.</span><span class="sxs-lookup"><span data-stu-id="c23bc-122">If the decoder can perform frame stepping, an application can use the [**Step**](step-method.md) method to step through frames.</span></span> <span data-ttu-id="c23bc-123">Diese Methode gibt immer **true** zurück, wenn ein Software Decoder verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="c23bc-123">This method will always return **true** if a software decoder is being used.</span></span>

 

 



