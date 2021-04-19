---
description: Die Balance-Eigenschaft legt den Lautsprecher Saldo für die audiostreamausgabe fest oder ruft ihn ab.
ms.assetid: b0e6bf16-b1d1-453d-8b58-272565c3d6e6
title: Balance (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f1334fcc51695f04ab0026ded8c68c17cb07aa0b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106345410"
---
# <a name="balance-property"></a><span data-ttu-id="2a2e2-103">Balance (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="2a2e2-103">Balance Property</span></span>

> [!Note]  
> <span data-ttu-id="2a2e2-104">Diese Komponente ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="2a2e2-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="2a2e2-105">Es kann in nachfolgenden Versionen geändert oder entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="2a2e2-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="2a2e2-106">Die `Balance` -Eigenschaft legt den Referenten Saldo für die audiostreamausgabe fest oder ruft ihn ab.</span><span class="sxs-lookup"><span data-stu-id="2a2e2-106">The `Balance` property sets or retrieves the speaker balance for the audio stream output.</span></span>

``` syntax
[ iBalance = ] MSWebDVD.Balance
```

## <a name="return-value"></a><span data-ttu-id="2a2e2-107">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2a2e2-107">Return Value</span></span>

<span data-ttu-id="2a2e2-108">Gibt einen ganzzahligen Wert zurück, der die Ausgleichs Ebenen darstellt.</span><span class="sxs-lookup"><span data-stu-id="2a2e2-108">Returns an integer value representing the balance levels.</span></span> <span data-ttu-id="2a2e2-109">Der zulässige Eingabebereich ist-10.000 bis 10.000.</span><span class="sxs-lookup"><span data-stu-id="2a2e2-109">The allowable input range is -10,000 to 10,000.</span></span> <span data-ttu-id="2a2e2-110">Bei einem Wert von 0 wird ein neutrales Gleichgewicht festgelegt, d. h., der linke und der Rechte Sprecher erhalten dasselbe Amplitude-Audiosignal.</span><span class="sxs-lookup"><span data-stu-id="2a2e2-110">A value of 0 sets a neutral balance, that is both left and right speakers are given the same amplitude audio signal.</span></span>

## <a name="remarks"></a><span data-ttu-id="2a2e2-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2a2e2-111">Remarks</span></span>

<span data-ttu-id="2a2e2-112">Diese Eigenschaft ist Lese-/Schreibzugriff mit einem Standardwert von 0. Dies bedeutet, dass beide Redner äquivalente Audiosignale erhalten.</span><span class="sxs-lookup"><span data-stu-id="2a2e2-112">This property is read/write with a default value of 0, meaning that both speakers receive equivalent audio signals.</span></span> <span data-ttu-id="2a2e2-113">Wie bei der [**Volume**](volume-property.md) -Eigenschaft entsprechen Einheiten 01 Dezibel (multipliziert mit-1, wenn</span><span class="sxs-lookup"><span data-stu-id="2a2e2-113">As with the [**Volume**](volume-property.md) property, units correspond to .01 decibels (multiplied by -1 when</span></span>


```
iBalance
```



<span data-ttu-id="2a2e2-114">ist ein positiver Wert).</span><span class="sxs-lookup"><span data-stu-id="2a2e2-114">is a positive value).</span></span> <span data-ttu-id="2a2e2-115">Der Wert 1000 gibt z. b. 10 dB auf dem rechten Kanal und 90 dB im linken Kanal an.</span><span class="sxs-lookup"><span data-stu-id="2a2e2-115">For example, a value of 1000 indicates 10 dB on the right channel and 90 dB on the left channel.</span></span>

 

 



