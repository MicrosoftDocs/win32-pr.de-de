---
title: Idlestart-Ereignis
description: Idlestart-Ereignis
ms.assetid: 3d97c26b-b88a-42e3-9072-0bc65510efc2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 706aafc13cb1639484539e3d08b305df217ecec8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106338991"
---
# <a name="idlestart-event"></a><span data-ttu-id="8363e-103">Idlestart-Ereignis</span><span class="sxs-lookup"><span data-stu-id="8363e-103">IdleStart Event</span></span>

<span data-ttu-id="8363e-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="8363e-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="8363e-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="8363e-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="8363e-106">Tritt auf, wenn der Server ein Zeichen auf den **idck** -Zustand festlegt.</span><span class="sxs-lookup"><span data-stu-id="8363e-106">Occurs when the server sets a character to the **Idling** state.</span></span>

</dd> <dt>

<span data-ttu-id="8363e-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span><span class="sxs-lookup"><span data-stu-id="8363e-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="8363e-108">**Sub** - *Agent \* \* \* \_ idlestart* \*  **(ByVal** -Merkmal- *ID \* \* *)**</span><span class="sxs-lookup"><span data-stu-id="8363e-108">**Sub** *agent\*\*\*\_IdleStart*\* **(ByVal** *CharacterID\*\*\*)*\*</span></span>



| <span data-ttu-id="8363e-109">Teil</span><span class="sxs-lookup"><span data-stu-id="8363e-109">Part</span></span>          | <span data-ttu-id="8363e-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8363e-110">Description</span></span>                                         |
|---------------|-----------------------------------------------------|
| <span data-ttu-id="8363e-111">*Merkmal-ID*</span><span class="sxs-lookup"><span data-stu-id="8363e-111">*CharacterID*</span></span> | <span data-ttu-id="8363e-112">Gibt die ID des idult-Zeichens als Zeichenfolge zurück.</span><span class="sxs-lookup"><span data-stu-id="8363e-112">Returns the ID of the idling character as a string.</span></span> |



 

</dd> </dl>

### <a name="remarks"></a><span data-ttu-id="8363e-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8363e-113">Remarks</span></span>

<span data-ttu-id="8363e-114">Der Server sendet dieses Ereignis an alle Clients des Zeichens.</span><span class="sxs-lookup"><span data-stu-id="8363e-114">The server sends this event to all clients of the character.</span></span>

### <a name="see-also"></a><span data-ttu-id="8363e-115">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="8363e-115">See Also</span></span>

[<span data-ttu-id="8363e-116">**Idlecomplete-Ereignis**</span><span class="sxs-lookup"><span data-stu-id="8363e-116">**IdleComplete event**</span></span>](idlecomplete-event.md)


 

 




