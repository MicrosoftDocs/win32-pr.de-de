---
title: Genaues Erfassungs Steuerelement
description: Genaues Erfassungs Steuerelement
ms.assetid: 497c9d77-f392-4cbb-88f3-8418e1e9fc6b
keywords:
- Avicap-Rückruf Funktionen, präzises Erfassungs Steuerelement
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0749d420d7a1999d074546a0cf577fdaceb72483
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104515699"
---
# <a name="precise-capture-control"></a><span data-ttu-id="051a3-104">Genaues Erfassungs Steuerelement</span><span class="sxs-lookup"><span data-stu-id="051a3-104">Precise Capture Control</span></span>

<span data-ttu-id="051a3-105">Ein Aufzeichnungs Fenster kann der Capture-Control-Rückruffunktion eine genaue Kontrolle über die Momente bieten, in denen die Erfassung von streamingvorhalten beginnt und endet.</span><span class="sxs-lookup"><span data-stu-id="051a3-105">A capture window can provide the capture-control callback function with precise control over the moments that streaming capture begin and end.</span></span> <span data-ttu-id="051a3-106">Die erste Meldung, die vom Aufzeichnungs Treiber an die Rückruf Prozedur gesendet wird, legt den *nState* -Parameter auf "controlcallback Preroll" fest, \_ nachdem alle Puffer zugeordnet wurden und alle anderen Aufzeichnungs Vorbereitungen vollständig sind.</span><span class="sxs-lookup"><span data-stu-id="051a3-106">The first message sent from the capture driver to the callback procedure sets the *nState* parameter to CONTROLCALLBACK\_PREROLL after allocating all buffers and all other capture preparations are complete.</span></span> <span data-ttu-id="051a3-107">Diese Meldung gibt der Anwendung die Möglichkeit, die Videoquellen vorab zu überstehen.</span><span class="sxs-lookup"><span data-stu-id="051a3-107">This message gives the application the ability to preroll the video sources.</span></span> <span data-ttu-id="051a3-108">(Die Rückruffunktion gibt *nState* als zweiten Parameter an.) Die Rückruffunktion gibt dann zu dem Zeitpunkt zurück, zu dem die Aufzeichnung beginnt.</span><span class="sxs-lookup"><span data-stu-id="051a3-108">(The callback function specifies *nState* as its second parameter.) The callback function then returns at the exact moment recording is to begin.</span></span> <span data-ttu-id="051a3-109">Der Rückgabewert **true** von der Rückruffunktion setzt die Erfassung fort.</span><span class="sxs-lookup"><span data-stu-id="051a3-109">A return value of **TRUE** from the callback function continues capture.</span></span> <span data-ttu-id="051a3-110">Der Rückgabewert **false** bricht Capture ab.</span><span class="sxs-lookup"><span data-stu-id="051a3-110">A return value of **FALSE** aborts capture.</span></span> <span data-ttu-id="051a3-111">Sobald die Erfassung beginnt, wird die Rückruffunktion häufig aufgerufen, wobei *nState* auf controlcallback Capture festgelegt ist, \_ damit die Anwendung die Erfassung beenden kann, indem **false** zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="051a3-111">Once capture begins, the callback function is called frequently with *nState* set to CONTROLCALLBACK\_CAPTURING to allow the application to end capture by returning **FALSE**.</span></span>

 

 




