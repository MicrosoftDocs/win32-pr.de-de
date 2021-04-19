---
title: Status-Eigenschaft
description: Status-Eigenschaft
ms.assetid: vs|msagent|~\pacontrol_8xd6.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 402e88185e1024aa5958d06936a6529ae4012622
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106341867"
---
# <a name="status-property"></a><span data-ttu-id="28e5d-103">Status-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="28e5d-103">Status Property</span></span>

<span data-ttu-id="28e5d-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="28e5d-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="28e5d-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="28e5d-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="28e5d-106">Gibt den Status des audioausgabekanals zurück.</span><span class="sxs-lookup"><span data-stu-id="28e5d-106">Returns the status of the audio output channel.</span></span>

</dd> <dt>

<span data-ttu-id="28e5d-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span><span class="sxs-lookup"><span data-stu-id="28e5d-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="28e5d-108">*Agent \* \* *. Audiooutput. Status**</span><span class="sxs-lookup"><span data-stu-id="28e5d-108">*agent\*\*\*.AudioOutput.Status*\*</span></span>



| <span data-ttu-id="28e5d-109">Wert</span><span class="sxs-lookup"><span data-stu-id="28e5d-109">Value</span></span> | <span data-ttu-id="28e5d-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="28e5d-110">Description</span></span>                                                                                                       |
|-------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="28e5d-111">0</span><span class="sxs-lookup"><span data-stu-id="28e5d-111">0</span></span>     | <span data-ttu-id="28e5d-112">Der audioausgabechannel ist verfügbar (nicht ausgelastet).</span><span class="sxs-lookup"><span data-stu-id="28e5d-112">The audio output channel is available (not busy).</span></span>                                                                 |
| <span data-ttu-id="28e5d-113">1</span><span class="sxs-lookup"><span data-stu-id="28e5d-113">1</span></span>     | <span data-ttu-id="28e5d-114">Die Audioausgabe wird nicht unterstützt. Dies ist beispielsweise der Fall, weil keine Soundkarte vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="28e5d-114">There is no support for audio output; for example, because there is no sound card.</span></span>                                |
| <span data-ttu-id="28e5d-115">2</span><span class="sxs-lookup"><span data-stu-id="28e5d-115">2</span></span>     | <span data-ttu-id="28e5d-116">Der audioausgabechannel kann nicht geöffnet werden (ist ausgelastet); beispielsweise, weil eine andere Anwendung Audiofunktionen wieder gibt.</span><span class="sxs-lookup"><span data-stu-id="28e5d-116">The audio output channel can't be opened (is busy); for example, because some other application is playing audio.</span></span> |
| <span data-ttu-id="28e5d-117">3</span><span class="sxs-lookup"><span data-stu-id="28e5d-117">3</span></span>     | <span data-ttu-id="28e5d-118">Der audioausgabechannel ist ausgelastet, weil der Server die Benutzer Spracheingabe verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="28e5d-118">The audio output channel is busy because the server is processing user speech input.</span></span>                              |
| <span data-ttu-id="28e5d-119">4</span><span class="sxs-lookup"><span data-stu-id="28e5d-119">4</span></span>     | <span data-ttu-id="28e5d-120">Der audioausgabechannel ist ausgelastet, weil zurzeit ein Zeichen spricht.</span><span class="sxs-lookup"><span data-stu-id="28e5d-120">The audio output channel is busy because a character is currently speaking.</span></span>                                       |
| <span data-ttu-id="28e5d-121">5</span><span class="sxs-lookup"><span data-stu-id="28e5d-121">5</span></span>     | <span data-ttu-id="28e5d-122">Der audioausgabechannel ist nicht ausgelastet, aber er wartet auf die Benutzer Spracheingabe.</span><span class="sxs-lookup"><span data-stu-id="28e5d-122">The audio output channel is not busy, but it is waiting for user speech input.</span></span>                                    |
| <span data-ttu-id="28e5d-123">6</span><span class="sxs-lookup"><span data-stu-id="28e5d-123">6</span></span>     | <span data-ttu-id="28e5d-124">Beim Versuch, auf den audioausgabechannel zuzugreifen, ist ein anderes (Unbekanntes) Problem aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="28e5d-124">There was some other (unknown) problem in attempting to access the audio output channel.</span></span>                          |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="28e5d-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="28e5d-125">Remarks</span></span>

<span data-ttu-id="28e5d-126">Mit dieser Einstellung kann Ihre Client Anwendung den audioausgabechannel Abfragen und einen ganzzahligen Wert zurückgeben, der den Status des audioausgabekanals angibt.</span><span class="sxs-lookup"><span data-stu-id="28e5d-126">This setting enables your client application to query the audio output channel, returning an Integer value that indicates the status of the audio output channel.</span></span> <span data-ttu-id="28e5d-127">Sie können dies verwenden, um zu bestimmen, ob es angemessen ist, das Zeichen zu verwenden, oder ob es sinnvoll ist, den Empfangsmodus zu aktivieren ( [**mithilfe der Abhör**](listen-method.md) Methode).</span><span class="sxs-lookup"><span data-stu-id="28e5d-127">You can use this to determine whether it is appropriate to have your character speak or whether it is appropriate to try to turn on Listening mode (using the [**Listen**](listen-method.md) method).</span></span>

## <a name="see-also"></a><span data-ttu-id="28e5d-128">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="28e5d-128">See Also</span></span>

[<span data-ttu-id="28e5d-129">**Listencomplete-Ereignis**</span><span class="sxs-lookup"><span data-stu-id="28e5d-129">**ListenComplete event**</span></span>](listencomplete-event.md)


 

 




