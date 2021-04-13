---
title: Defaultcharacters-Änderungs Ereignis
description: Defaultcharacters-Änderungs Ereignis
ms.assetid: 14b86a44-8fd2-4719-b7b5-cdcc618d27cd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab92fe04f9c42466d559e9b4610eafc8490556d6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388503"
---
# <a name="defaultcharacterchange-event"></a><span data-ttu-id="e4dc3-103">Defaultcharacters-Änderungs Ereignis</span><span class="sxs-lookup"><span data-stu-id="e4dc3-103">DefaultCharacterChange Event</span></span>

<span data-ttu-id="e4dc3-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="e4dc3-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="e4dc3-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="e4dc3-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="e4dc3-106">Tritt ein, wenn der Benutzer das Standard Zeichen ändert.</span><span class="sxs-lookup"><span data-stu-id="e4dc3-106">Occurs when the user changes the default character.</span></span>

</dd> <dt>

<span data-ttu-id="e4dc3-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span><span class="sxs-lookup"><span data-stu-id="e4dc3-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="e4dc3-108">**Sub** - *Agent. \* \* \* defaultcharakterienänderung* \*  **(ByVal** - *GUID \* \* *)**</span><span class="sxs-lookup"><span data-stu-id="e4dc3-108">**Sub** *agent.\*\*\*DefaultCharacterChange*\* **(ByVal** *GUID\*\*\*)*\*</span></span>



| <span data-ttu-id="e4dc3-109">Teil</span><span class="sxs-lookup"><span data-stu-id="e4dc3-109">Part</span></span>   | <span data-ttu-id="e4dc3-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e4dc3-110">Description</span></span>                                      |
|--------|--------------------------------------------------|
| <span data-ttu-id="e4dc3-111">*GUID*</span><span class="sxs-lookup"><span data-stu-id="e4dc3-111">*GUID*</span></span> | <span data-ttu-id="e4dc3-112">Gibt den eindeutigen Bezeichner für das Zeichen zurück.</span><span class="sxs-lookup"><span data-stu-id="e4dc3-112">Returns the unique identifier for the character.</span></span> |



 

</dd> </dl>

### <a name="remarks"></a><span data-ttu-id="e4dc3-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e4dc3-113">Remarks</span></span>

<span data-ttu-id="e4dc3-114">Dieses Ereignis zeigt an, dass der Benutzer das als Standard Zeichen des Benutzers zugewiesene Zeichen geändert hat.</span><span class="sxs-lookup"><span data-stu-id="e4dc3-114">This event indicates when the user has changed the character assigned as the user's default character.</span></span> <span data-ttu-id="e4dc3-115">Der Server sendet dies nur an Clients, die das Standard Zeichen geladen haben.</span><span class="sxs-lookup"><span data-stu-id="e4dc3-115">The server sends this only to clients that have loaded the default character.</span></span>

<span data-ttu-id="e4dc3-116">Wenn das neue Zeichen angezeigt wird, wird die gleiche Größe wie jede bereits geladene Instanz des Zeichens oder das vorherige Standard Zeichen (in dieser Reihenfolge) angenommen.</span><span class="sxs-lookup"><span data-stu-id="e4dc3-116">When the new character appears, it assumes the same size as any already loaded instance of the character or the previous default character (in that order).</span></span>

### <a name="see-also"></a><span data-ttu-id="e4dc3-117">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="e4dc3-117">See Also</span></span>

<span data-ttu-id="e4dc3-118">[**Showdefaultcharakteriproperties-Methode**](showdefaultcharacterproperties-method.md), [ **Load-Methode**](load-method.md)</span><span class="sxs-lookup"><span data-stu-id="e4dc3-118">[**ShowDefaultCharacterProperties method**](showdefaultcharacterproperties-method.md), [**Load method**](load-method.md)</span></span>


 

 




