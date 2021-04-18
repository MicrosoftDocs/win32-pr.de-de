---
title: StopAll-Methode
description: StopAll-Methode
ms.assetid: 2ce32ff8-4908-45b1-9b83-4d558f67417c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76c99a687c2481d9686e84b7fa5c198e7a4273a2
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "106337642"
---
# <a name="stopall-method"></a><span data-ttu-id="1bee1-103">StopAll-Methode</span><span class="sxs-lookup"><span data-stu-id="1bee1-103">StopAll Method</span></span>

<span data-ttu-id="1bee1-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="1bee1-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="1bee1-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="1bee1-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="1bee1-106">Beendet alle Animations Anforderungen oder angegebenen Anforderungs Typen für das angegebene Zeichen.</span><span class="sxs-lookup"><span data-stu-id="1bee1-106">Stops all animation requests or specified types of requests for the specified character.</span></span>

</dd> <dt>

<span data-ttu-id="1bee1-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span><span class="sxs-lookup"><span data-stu-id="1bee1-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="1bee1-108">\*Agent ***. Zeichen ("*** Merkmal-ID \* \* *"). StopAll*- \*  \[ *Typ*\]</span><span class="sxs-lookup"><span data-stu-id="1bee1-108">*agent ***.Characters ("*** CharacterID\*\*\*").StopAll*\* \[*Type*\]</span></span>



| <span data-ttu-id="1bee1-109">Teil</span><span class="sxs-lookup"><span data-stu-id="1bee1-109">Part</span></span>   | <span data-ttu-id="1bee1-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1bee1-110">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|--------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1bee1-111">*Type*</span><span class="sxs-lookup"><span data-stu-id="1bee1-111">*Type*</span></span> | <span data-ttu-id="1bee1-112">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="1bee1-112">Optional.</span></span> <span data-ttu-id="1bee1-113">Wenn Sie diesen Parameter verwenden möchten, können Sie einen der folgenden Werte verwenden.</span><span class="sxs-lookup"><span data-stu-id="1bee1-113">To use this parameter you can use any of the following values.</span></span> <span data-ttu-id="1bee1-114">Sie können auch mehrere Typen angeben, indem Sie Sie durch Kommas trennen.</span><span class="sxs-lookup"><span data-stu-id="1bee1-114">You can also specify multiple types by separating them with commas.</span></span> <br/> <span data-ttu-id="1bee1-115">"**Get**"</span><span class="sxs-lookup"><span data-stu-id="1bee1-115">"**Get**"</span></span> <br/> <span data-ttu-id="1bee1-116">, Um alle [**Get**](get-method.md) -Anforderungen in der Warteschlange anzuhalten.</span><span class="sxs-lookup"><span data-stu-id="1bee1-116">To stop all queued [**Get**](get-method.md) requests.</span></span><br/> <span data-ttu-id="1bee1-117">"**Nonqueuedget**"</span><span class="sxs-lookup"><span data-stu-id="1bee1-117">"**NonQueuedGet**"</span></span> <br/> <span data-ttu-id="1bee1-118">Zum Abbrechen aller nicht in die Warteschlange eingereihten [**Get**](get-method.md) -Anforderungen (**Get** -Methode mit **Queue** -Parameter ist auf **false** festgelegt).</span><span class="sxs-lookup"><span data-stu-id="1bee1-118">To stop all non-queued [**Get**](get-method.md) requests (**Get** method with **Queue** parameter set to **False**).</span></span><br/> <span data-ttu-id="1bee1-119">"**Verschieben**"</span><span class="sxs-lookup"><span data-stu-id="1bee1-119">"**Move**"</span></span> <br/> <span data-ttu-id="1bee1-120">, Um alle in der Warteschlange [**befindlichen Anforderungen für**](moveto-method.md) das Anforderungs Wort anzuhalten</span><span class="sxs-lookup"><span data-stu-id="1bee1-120">To stop all queued [**MoveTo**](moveto-method.md) requests.</span></span><br/> <span data-ttu-id="1bee1-121">"**Play**"</span><span class="sxs-lookup"><span data-stu-id="1bee1-121">"**Play**"</span></span> <br/> <span data-ttu-id="1bee1-122">, Um alle [**Wiedergabe**](play-method.md) Anforderungen in der Warteschlange anzuhalten.</span><span class="sxs-lookup"><span data-stu-id="1bee1-122">To stop all queued [**Play**](play-method.md) requests.</span></span><br/> <span data-ttu-id="1bee1-123">"**Sprechen**"</span><span class="sxs-lookup"><span data-stu-id="1bee1-123">"**Speak**"</span></span> <br/> <span data-ttu-id="1bee1-124">, Um alle [**sprach**](speak-method.md) Anforderungen in der Warteschlange zu verhindern.</span><span class="sxs-lookup"><span data-stu-id="1bee1-124">To stop all queued [**Speak**](speak-method.md) requests.</span></span><br/> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1bee1-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1bee1-125">Remarks</span></span>

<span data-ttu-id="1bee1-126">Wenn Sie den **Typparameter** nicht festlegen, hält der Server alle Animationen für das Zeichen an, einschließlich Warteschlangen und nicht in die Warteschlange eingereihte [**Get**](get-method.md) -Anforderungen, und löscht seine Animations Warteschlange.</span><span class="sxs-lookup"><span data-stu-id="1bee1-126">If you don't set the **Type** parameter, the server stops all animations for the character, including queued and non-queued [**Get**](get-method.md) requests, and clears its animation queue.</span></span> <span data-ttu-id="1bee1-127">Außerdem wird die Wiedergabe eines Zeichens zum Ausblenden oder Einblenden der Animation angehalten.</span><span class="sxs-lookup"><span data-stu-id="1bee1-127">It also stops playing a character's Hiding or Showing animation.</span></span>

<span data-ttu-id="1bee1-128">Diese Methode generiert kein [**Anforderungs**](/windows/desktop/lwef/the-request-object) Objekt.</span><span class="sxs-lookup"><span data-stu-id="1bee1-128">This method will not generate a [**Request**](/windows/desktop/lwef/the-request-object) object.</span></span>

## <a name="see-also"></a><span data-ttu-id="1bee1-129">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="1bee1-129">See Also</span></span>

[<span data-ttu-id="1bee1-130">**Stop-Methode**</span><span class="sxs-lookup"><span data-stu-id="1bee1-130">**Stop method**</span></span>](stop-method.md)


 

