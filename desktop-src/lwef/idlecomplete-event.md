---
title: Idlecomplete-Ereignis
description: Idlecomplete-Ereignis
ms.assetid: 1d684f75-f23e-4ed8-a60a-5e6792332103
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01782825dc880dc4d214a8d0e682d69a9f842e22
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036223"
---
# <a name="idlecomplete-event"></a><span data-ttu-id="686be-103">Idlecomplete-Ereignis</span><span class="sxs-lookup"><span data-stu-id="686be-103">IdleComplete Event</span></span>

<span data-ttu-id="686be-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="686be-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="686be-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="686be-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="686be-106">Tritt auf, wenn der Server den **Leerlauf** Zustand eines Zeichens beendet.</span><span class="sxs-lookup"><span data-stu-id="686be-106">Occurs when the server ends the **Idling** state of a character.</span></span>

</dd> <dt>

<span data-ttu-id="686be-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span><span class="sxs-lookup"><span data-stu-id="686be-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="686be-108">**Sub** - *Agent \* \* \* \_ idlecomplete* \*  **(ByVal** -Merkmal- *ID \* \* *)**</span><span class="sxs-lookup"><span data-stu-id="686be-108">**Sub** *agent\*\*\*\_IdleComplete*\* **(ByVal** *CharacterID\*\*\*)*\*</span></span>



| <span data-ttu-id="686be-109">Teil</span><span class="sxs-lookup"><span data-stu-id="686be-109">Part</span></span>          | <span data-ttu-id="686be-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="686be-110">Description</span></span>                                         |
|---------------|-----------------------------------------------------|
| <span data-ttu-id="686be-111">*Merkmal-ID*</span><span class="sxs-lookup"><span data-stu-id="686be-111">*CharacterID*</span></span> | <span data-ttu-id="686be-112">Gibt die ID des idult-Zeichens als Zeichenfolge zurück.</span><span class="sxs-lookup"><span data-stu-id="686be-112">Returns the ID of the idling character as a string.</span></span> |



 

</dd> </dl>

### <a name="remarks"></a><span data-ttu-id="686be-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="686be-113">Remarks</span></span>

<span data-ttu-id="686be-114">Der Server sendet dieses Ereignis an alle Clients des Zeichens.</span><span class="sxs-lookup"><span data-stu-id="686be-114">The server sends this event to all clients of the character.</span></span>

### <a name="see-also"></a><span data-ttu-id="686be-115">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="686be-115">See Also</span></span>

[<span data-ttu-id="686be-116">**Idlestart-Ereignis**</span><span class="sxs-lookup"><span data-stu-id="686be-116">**IdleStart event**</span></span>](idlestart-event.md)


 

 




