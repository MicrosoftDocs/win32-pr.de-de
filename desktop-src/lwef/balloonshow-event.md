---
title: Balloonshow-Ereignis
description: Balloonshow-Ereignis
ms.assetid: 8a73e883-c003-480b-8a0a-e699caffe54c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de67318b02775619332fe60ea47fb27edb893c8b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388573"
---
# <a name="balloonshow-event"></a><span data-ttu-id="dea38-103">Balloonshow-Ereignis</span><span class="sxs-lookup"><span data-stu-id="dea38-103">BalloonShow Event</span></span>

<span data-ttu-id="dea38-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="dea38-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="dea38-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="dea38-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="dea38-106">Tritt auf, wenn die Wort Sprechblase eines Zeichens angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="dea38-106">Occurs when a character's word balloon is shown.</span></span>

</dd> <dt>

<span data-ttu-id="dea38-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span><span class="sxs-lookup"><span data-stu-id="dea38-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="dea38-108">**Unter-** *Agent*- \_ **aufballungs Anzeige** **(ByVal** - *Merkmal-ID \* \* *)**</span><span class="sxs-lookup"><span data-stu-id="dea38-108">**Sub** *agent*\_**BalloonShow** **(ByVal** *CharacterID\*\*\*)*\*</span></span>



| <span data-ttu-id="dea38-109">Teil</span><span class="sxs-lookup"><span data-stu-id="dea38-109">Part</span></span>          | <span data-ttu-id="dea38-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="dea38-110">Description</span></span>                                                       |
|---------------|-------------------------------------------------------------------|
| <span data-ttu-id="dea38-111">*Merkmal-ID*</span><span class="sxs-lookup"><span data-stu-id="dea38-111">*CharacterID*</span></span> | <span data-ttu-id="dea38-112">Gibt die ID des der Wort Sprechblase zugeordneten Zeichens zurück.</span><span class="sxs-lookup"><span data-stu-id="dea38-112">Returns the ID of the character associated with the word balloon.</span></span> |



 

</dd> </dl>

### <a name="remarks"></a><span data-ttu-id="dea38-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="dea38-113">Remarks</span></span>

<span data-ttu-id="dea38-114">Der Server sendet dieses Ereignis nur an die Clients des Zeichens (Anwendungen, die das Zeichen geladen haben), das die Word-Sprechblase verwendet.</span><span class="sxs-lookup"><span data-stu-id="dea38-114">The server sends this event only to the clients of the character (applications that have loaded the character) that uses the word balloon.</span></span>

### <a name="see-also"></a><span data-ttu-id="dea38-115">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="dea38-115">See Also</span></span>

[<span data-ttu-id="dea38-116">**Balloonhide-Ereignis**</span><span class="sxs-lookup"><span data-stu-id="dea38-116">**BalloonHide event**</span></span>](balloonhide-event.md)


 

 




