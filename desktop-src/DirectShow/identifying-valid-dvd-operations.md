---
description: Identifizieren gültiger DVD-Vorgänge
ms.assetid: d368b552-7ed3-4334-b97b-ff49d6c331c3
title: Identifizieren gültiger DVD-Vorgänge
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 444595e402dc73a3468946b820f031dabaecc2f2
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104392769"
---
# <a name="identifying-valid-dvd-operations"></a><span data-ttu-id="288b6-103">Identifizieren gültiger DVD-Vorgänge</span><span class="sxs-lookup"><span data-stu-id="288b6-103">Identifying Valid DVD Operations</span></span>

<span data-ttu-id="288b6-104">Verschiedene Faktoren bestimmen, ob ein angegebener DVD-Vorgang durchgeführt werden kann:</span><span class="sxs-lookup"><span data-stu-id="288b6-104">Several factors determine whether you can perform a given DVD operation:</span></span>

-   <span data-ttu-id="288b6-105">Die aktuelle Domäne.</span><span class="sxs-lookup"><span data-stu-id="288b6-105">The current domain.</span></span> <span data-ttu-id="288b6-106">Einige Befehle sind nur in bestimmten Domänen gültig.</span><span class="sxs-lookup"><span data-stu-id="288b6-106">Some commands are only valid in certain domains.</span></span> <span data-ttu-id="288b6-107">Wenn sich die Domäne ändert, sendet der Navigator ein EC- \_ DVD- \_ Domänen \_ Änderungs Ereignis.</span><span class="sxs-lookup"><span data-stu-id="288b6-107">When the domain changes, the navigator sends an EC\_DVD\_DOMAIN\_CHANGE event.</span></span> <span data-ttu-id="288b6-108">Sie können auch [**IDvdInfo2:: GetCurrentDomain**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getcurrentdomain) aufrufen, um die aktuelle Domäne abzurufen.</span><span class="sxs-lookup"><span data-stu-id="288b6-108">You can also call [**IDvdInfo2::GetCurrentDomain**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getcurrentdomain) to get the current domain.</span></span>
-   <span data-ttu-id="288b6-109">UOPs-Flags.</span><span class="sxs-lookup"><span data-stu-id="288b6-109">UOPS flags.</span></span> <span data-ttu-id="288b6-110">Dies sind Flags, die auf die Festplatte geschrieben werden und angeben, welche Vorgänge zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="288b6-110">These are flags written onto the disc that indicate which operations are permitted.</span></span> <span data-ttu-id="288b6-111">Wenn sich die Flags ändern, sendet der Navigator ein \_ gültiges UOPs-Änderungs Ereignis für eine EC-DVD \_ \_ \_ mit den neuen Flags.</span><span class="sxs-lookup"><span data-stu-id="288b6-111">Whenever the flags change, the navigator sends a EC\_DVD\_VALID\_UOPS\_CHANGE event with the new flags.</span></span> <span data-ttu-id="288b6-112">Sie können auch [**IDvdInfo2:: getcurrentuops**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getcurrentuops) aufrufen, um die aktuellen UOPs-Flags zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="288b6-112">You can also call [**IDvdInfo2::GetCurrentUOPS**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getcurrentuops) to get the current UOPS flags.</span></span>
-   <span data-ttu-id="288b6-113">DVD-Inhalt.</span><span class="sxs-lookup"><span data-stu-id="288b6-113">DVD content.</span></span> <span data-ttu-id="288b6-114">Einige Befehle sind möglicherweise auf Grundlage des Inhalts der DVD nicht relevant.</span><span class="sxs-lookup"><span data-stu-id="288b6-114">Some commands may not be relevant based on the content of the DVD.</span></span> <span data-ttu-id="288b6-115">Beispielsweise kann die [**IDvdControl2:: selectangle**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-selectangle) -Methode gemäß der aktuellen Domäne und den UOPs-Flags zulässig sein, aber das Video hat möglicherweise nur einen Winkel.</span><span class="sxs-lookup"><span data-stu-id="288b6-115">For example, the [**IDvdControl2::SelectAngle**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-selectangle) method might be permitted according to the current domain and UOPS flags, yet the video might have only one angle.</span></span> <span data-ttu-id="288b6-116">In diesem Fall ist der **selectangle** -Befehl zulässig, ist jedoch keine sinnvolle Option.</span><span class="sxs-lookup"><span data-stu-id="288b6-116">In that case, the **SelectAngle** call is permitted but is not a meaningful option.</span></span>

<span data-ttu-id="288b6-117">Wenn Sie zweifelhaft sind, gestatten Sie eine Aktion.</span><span class="sxs-lookup"><span data-stu-id="288b6-117">When in doubt, permit an action.</span></span> <span data-ttu-id="288b6-118">Im schlimmsten Fall tritt bei der [**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2) -Methode ein Fehler auf, und Sie können dem Benutzer Feedback geben.</span><span class="sxs-lookup"><span data-stu-id="288b6-118">At worst, the [**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2) method will fail and you can give feedback to the user.</span></span> <span data-ttu-id="288b6-119">Das Feedback sollte relativ unaufdringlich sein.</span><span class="sxs-lookup"><span data-stu-id="288b6-119">The feedback should be relatively unobtrusive.</span></span> <span data-ttu-id="288b6-120">Beispielsweise können Sie ein kleines rotes X blinken, um den Benutzer zu benachrichtigen.</span><span class="sxs-lookup"><span data-stu-id="288b6-120">For example, you might flash a small red X to alert the user.</span></span> <span data-ttu-id="288b6-121">Der DVD-Navigator gibt VFW \_ e \_ DVD \_ invaliddomain zurück, wenn die Domäne einen Vorgang untersagt, und VFW \_ e \_ DVD-Vorgang wird verhindert, \_ \_ Wenn die UOPs-Flags einen Vorgang verbieten.</span><span class="sxs-lookup"><span data-stu-id="288b6-121">The DVD Navigator returns VFW\_E\_DVD\_INVALIDDOMAIN when the domain prohibits an operation, and VFW\_E\_DVD\_OPERATION\_INHIBITED when the UOPS flags prohibit an operation.</span></span>

## <a name="related-topics"></a><span data-ttu-id="288b6-122">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="288b6-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="288b6-123">DVD-Anwendungen</span><span class="sxs-lookup"><span data-stu-id="288b6-123">DVD Applications</span></span>](dvd-applications.md)
</dt> </dl>

 

 



