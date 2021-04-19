---
description: Das updateoverlay-Ereignis wird gesendet, wenn die über Lagerungs Oberfläche verschoben oder die Größe geändert wurde oder der Farbschlüssel geändert wurde.
ms.assetid: 692cbd26-b7b3-4fa3-9157-ca96a33e3a1e
title: Updateoverlay (ddraw. h)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2152e1f58ba161dc8dc3e04c908aaf037f1eed2a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372497"
---
# <a name="updateoverlay"></a><span data-ttu-id="c269d-103">Updateoverlay</span><span class="sxs-lookup"><span data-stu-id="c269d-103">UpdateOverlay</span></span>

> [!Note]  
> <span data-ttu-id="c269d-104">Diese Komponente ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="c269d-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="c269d-105">Es kann in nachfolgenden Versionen geändert oder entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="c269d-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="c269d-106">Das **updateoverlay** -Ereignis wird gesendet, wenn die über Lagerungs Oberfläche verschoben oder die Größe geändert wurde oder der Farbschlüssel geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="c269d-106">The **UpdateOverlay** event is sent when the overlay surface has been moved or resized or its color key has changed.</span></span>

``` syntax
UpdateOverlay()
```

## <a name="remarks"></a><span data-ttu-id="c269d-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c269d-107">Remarks</span></span>

<span data-ttu-id="c269d-108">Anwendungen sollten sich nie Gedanken darüber machen, dass die Größe der Überlagerungs Oberfläche geändert oder verschoben wird.</span><span class="sxs-lookup"><span data-stu-id="c269d-108">Applications should never be concerned about the overlay surface being resized or moved.</span></span> <span data-ttu-id="c269d-109">Alles wird intern behandelt.</span><span class="sxs-lookup"><span data-stu-id="c269d-109">This is all handled internally.</span></span> <span data-ttu-id="c269d-110">Dieses Ereignis wird jedoch auch gesendet, wenn sich der Farbschlüssel ändert.</span><span class="sxs-lookup"><span data-stu-id="c269d-110">But this event is also sent when the color key changes.</span></span> <span data-ttu-id="c269d-111">Dies bedeutet Folgendes: Wenn eine Anwendung mswebdvd als fensterloses Steuerelement und unverankerte Schaltflächen oben auf der Video Oberfläche im Vollbildmodus anzeigt, sollte Sie auf dieses Ereignis reagieren, indem der neue Wert der **Colorkey** -Eigenschaft abgerufen wird, damit die Schaltflächen ordnungsgemäß gezeichnet werden können.</span><span class="sxs-lookup"><span data-stu-id="c269d-111">That means that if an application is hosting MSWebDVD as a windowless control and displaying floating buttons on top of the video surface in full-screen mode, it should respond to this event by getting the new value of the **ColorKey** property so that it can draw the buttons properly.</span></span>

## <a name="requirements"></a><span data-ttu-id="c269d-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c269d-112">Requirements</span></span>



| <span data-ttu-id="c269d-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c269d-113">Requirement</span></span> | <span data-ttu-id="c269d-114">Wert</span><span class="sxs-lookup"><span data-stu-id="c269d-114">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="c269d-115">Header</span><span class="sxs-lookup"><span data-stu-id="c269d-115">Header</span></span><br/> | <dl> <span data-ttu-id="c269d-116"><dt>Ddraw. h</dt></span><span class="sxs-lookup"><span data-stu-id="c269d-116"><dt>Ddraw.h</dt></span></span> </dl> |



 

 




