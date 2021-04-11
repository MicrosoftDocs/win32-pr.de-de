---
title: Balloonhide-Ereignis
description: Balloonhide-Ereignis
ms.assetid: dd1f3e83-f3d9-496e-9a54-b3a23b2403da
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 062a82afcabb3597ca8c254e039c231b52033657
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104207284"
---
# <a name="balloonhide-event"></a><span data-ttu-id="68e82-103">Balloonhide-Ereignis</span><span class="sxs-lookup"><span data-stu-id="68e82-103">BalloonHide Event</span></span>

<span data-ttu-id="68e82-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="68e82-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="68e82-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="68e82-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="68e82-106">Tritt auf, wenn die Wort Sprechblase eines Zeichens ausgeblendet ist.</span><span class="sxs-lookup"><span data-stu-id="68e82-106">Occurs when a character's word balloon is hidden.</span></span>

</dd> <dt>

<span data-ttu-id="68e82-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span><span class="sxs-lookup"><span data-stu-id="68e82-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="68e82-108">**Unter-** *Agent*- \_ **aufballungs** Hintergrund **(ByVal** - *Merkmal-ID \* \* *)**</span><span class="sxs-lookup"><span data-stu-id="68e82-108">**Sub** *agent*\_**BalloonHide** **(ByVal** *CharacterID\*\*\*)*\*</span></span>



| <span data-ttu-id="68e82-109">Teil</span><span class="sxs-lookup"><span data-stu-id="68e82-109">Part</span></span>          | <span data-ttu-id="68e82-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="68e82-110">Description</span></span>                                                       |
|---------------|-------------------------------------------------------------------|
| <span data-ttu-id="68e82-111">*Merkmal-ID*</span><span class="sxs-lookup"><span data-stu-id="68e82-111">*CharacterID*</span></span> | <span data-ttu-id="68e82-112">Gibt die ID des der Wort Sprechblase zugeordneten Zeichens zurück.</span><span class="sxs-lookup"><span data-stu-id="68e82-112">Returns the ID of the character associated with the word balloon.</span></span> |



 

</dd> </dl>

### <a name="remarks"></a><span data-ttu-id="68e82-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="68e82-113">Remarks</span></span>

<span data-ttu-id="68e82-114">Der Server sendet dieses Ereignis nur an die Clients des Zeichens (Anwendungen, die das Zeichen geladen haben), das die Word-Sprechblase verwendet.</span><span class="sxs-lookup"><span data-stu-id="68e82-114">The server sends this event only to the clients of the character (applications that have loaded the character) that uses the word balloon.</span></span>

### <a name="see-also"></a><span data-ttu-id="68e82-115">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="68e82-115">See Also</span></span>

[<span data-ttu-id="68e82-116">**Balloonshow-Ereignis**</span><span class="sxs-lookup"><span data-stu-id="68e82-116">**BalloonShow event**</span></span>](balloonshow-event.md)


 

 




