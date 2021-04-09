---
title: Ereignis anzeigen
description: Ereignis anzeigen
ms.assetid: vs|msagent|~\pacontrol_7wrw.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6964164e14c759a971e5ceeda542a5c27131663
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855771"
---
# <a name="show-event"></a><span data-ttu-id="8187c-103">Ereignis anzeigen</span><span class="sxs-lookup"><span data-stu-id="8187c-103">Show Event</span></span>

<span data-ttu-id="8187c-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="8187c-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="8187c-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="8187c-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="8187c-106">Tritt ein, wenn ein Zeichen angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="8187c-106">Occurs when a character is displayed.</span></span>

</dd> <dt>

<span data-ttu-id="8187c-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span><span class="sxs-lookup"><span data-stu-id="8187c-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="8187c-108">**Sub** *Agent \* \* \* \_ Show (ByVal*- \*  *Kenn zeichenkennung*, **ByVal** - *Ursache \* \* *)**</span><span class="sxs-lookup"><span data-stu-id="8187c-108">**Sub** *agent\*\*\*\_Show (ByVal*\* *CharacterID*, **ByVal** *Cause\*\*\*)*\*</span></span>



| <span data-ttu-id="8187c-109">Teil</span><span class="sxs-lookup"><span data-stu-id="8187c-109">Part</span></span>          | <span data-ttu-id="8187c-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8187c-110">Description</span></span>                                                                                                                                                                                                                                                                 |
|---------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8187c-111">*Merkmal-ID*</span><span class="sxs-lookup"><span data-stu-id="8187c-111">*CharacterID*</span></span> | <span data-ttu-id="8187c-112">Gibt die ID des Zeichens zurück, das als Zeichenfolge angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="8187c-112">Returns the ID of the character shown as a string.</span></span>                                                                                                                                                                                                                          |
| <span data-ttu-id="8187c-113">*Ursache*</span><span class="sxs-lookup"><span data-stu-id="8187c-113">*Cause*</span></span>       | <span data-ttu-id="8187c-114">Gibt einen Wert zurück, der angibt, wodurch das Zeichen angezeigt wurde.</span><span class="sxs-lookup"><span data-stu-id="8187c-114">Returns a value that indicates what caused the character to display.</span></span> <span data-ttu-id="8187c-115">2 der Benutzer hat das Zeichen (mit dem Menü-oder Sprachbefehl) angezeigt.</span><span class="sxs-lookup"><span data-stu-id="8187c-115">2 The user showed the character (using the menu or voice command).</span></span><br/> <span data-ttu-id="8187c-116">4 Ihre Client Anwendung hat das Zeichen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="8187c-116">4 Your client application showed the character.</span></span><br/> <span data-ttu-id="8187c-117">6 eine andere Client Anwendung hat das Zeichen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="8187c-117">6 Another client application showed the character.</span></span><br/> |



 

</dd> </dl>

### <a name="remarks"></a><span data-ttu-id="8187c-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8187c-118">Remarks</span></span>

<span data-ttu-id="8187c-119">Der Server sendet dieses Ereignis an alle Clients des Zeichens.</span><span class="sxs-lookup"><span data-stu-id="8187c-119">The server sends this event to all clients of the character.</span></span> <span data-ttu-id="8187c-120">Um den aktuellen Status des Zeichens abzufragen, verwenden Sie die [**Visible**](visible-property.md) -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="8187c-120">To query the current state of the character, use the [**Visible**](visible-property.md) property.</span></span>

### <a name="see-also"></a><span data-ttu-id="8187c-121">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="8187c-121">See Also</span></span>

<span data-ttu-id="8187c-122">[**Ereignis ausblenden**](hide-event.md), [ **visibilitycause**](visibilitycause-property.md)</span><span class="sxs-lookup"><span data-stu-id="8187c-122">[**Hide event**](hide-event.md), [**VisibilityCause**](visibilitycause-property.md)</span></span>


 

 





