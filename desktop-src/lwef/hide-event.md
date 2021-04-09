---
title: Ereignis ausblenden
description: Ereignis ausblenden
ms.assetid: vs|msagent|~\pacontrol_9yuk.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87d396fb0985cd4c3c2e9647dfe0e7c9126ad9c5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856228"
---
# <a name="hide-event"></a><span data-ttu-id="3f48d-103">Ereignis ausblenden</span><span class="sxs-lookup"><span data-stu-id="3f48d-103">Hide Event</span></span>

<span data-ttu-id="3f48d-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="3f48d-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="3f48d-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="3f48d-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="3f48d-106">Tritt ein, wenn ein Zeichen ausgeblendet ist.</span><span class="sxs-lookup"><span data-stu-id="3f48d-106">Occurs when a character is hidden.</span></span>

</dd> <dt>

<span data-ttu-id="3f48d-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span><span class="sxs-lookup"><span data-stu-id="3f48d-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="3f48d-108">**Sub** - *Agent \* \* \* \_ Ausblenden (* \*  **ByVal** - *Kenn zeichenkennung*, **ByVal** - *Ursache \* \* *)**</span><span class="sxs-lookup"><span data-stu-id="3f48d-108">**Sub** *agent\*\*\*\_Hide(*\* **ByVal** *CharacterID*, **ByVal** *Cause\*\*\*)*\*</span></span>



| <span data-ttu-id="3f48d-109">Teil</span><span class="sxs-lookup"><span data-stu-id="3f48d-109">Part</span></span>          | <span data-ttu-id="3f48d-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3f48d-110">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                       |
|---------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3f48d-111">*Merkmal-ID*</span><span class="sxs-lookup"><span data-stu-id="3f48d-111">*CharacterID*</span></span> | <span data-ttu-id="3f48d-112">Gibt die ID des verborgenen Zeichens als Zeichenfolge zurück.</span><span class="sxs-lookup"><span data-stu-id="3f48d-112">Returns the ID of the hidden character as a string.</span></span>                                                                                                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="3f48d-113">*Ursache*</span><span class="sxs-lookup"><span data-stu-id="3f48d-113">*Cause*</span></span>       | <span data-ttu-id="3f48d-114">Gibt einen Wert zurück, der angibt, was das Ausblenden des Zeichens bewirkt hat.</span><span class="sxs-lookup"><span data-stu-id="3f48d-114">Returns a value that indicates what caused the character to hide.</span></span> <span data-ttu-id="3f48d-115">1 Benutzer hat das Zeichen verborgen, indem er den Befehl im Popup Menü des Task leisten Symbols des Zeichens oder mithilfe von Spracheingaben ausgewählt hat.</span><span class="sxs-lookup"><span data-stu-id="3f48d-115">1 User hid the character by selecting the command on the character's taskbar icon pop-up menu or using speech input.</span></span><br/> <span data-ttu-id="3f48d-116">3 die Client Anwendung hat das Zeichen verborgen.</span><span class="sxs-lookup"><span data-stu-id="3f48d-116">3 Your client application hid the character.</span></span><br/> <span data-ttu-id="3f48d-117">5 eine andere Client Anwendung hat das Zeichen verborgen.</span><span class="sxs-lookup"><span data-stu-id="3f48d-117">5 Another client application hid the character.</span></span><br/> <span data-ttu-id="3f48d-118">7 Benutzer hat das Zeichen verborgen, indem er den Befehl im Popup Menü des Zeichens ausgewählt hat.</span><span class="sxs-lookup"><span data-stu-id="3f48d-118">7 User hid the character by selecting the command on the character's pop-up menu.</span></span><br/> |



 

</dd> </dl>

### <a name="remarks"></a><span data-ttu-id="3f48d-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3f48d-119">Remarks</span></span>

<span data-ttu-id="3f48d-120">Der Server sendet dieses Ereignis an alle Clients des Zeichens.</span><span class="sxs-lookup"><span data-stu-id="3f48d-120">The server sends this event to all clients of the character.</span></span> <span data-ttu-id="3f48d-121">Um den aktuellen Status des Zeichens abzufragen, verwenden Sie die [**Visible**](visible-property.md) -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="3f48d-121">To query the current state of the character, use the [**Visible**](visible-property.md) property.</span></span>

### <a name="see-also"></a><span data-ttu-id="3f48d-122">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="3f48d-122">See Also</span></span>

<span data-ttu-id="3f48d-123">[**Ereignis anzeigen**](show-event.md), [ **visibilitycause**](visibilitycause-property.md)</span><span class="sxs-lookup"><span data-stu-id="3f48d-123">[**Show event**](show-event.md), [**VisibilityCause**](visibilitycause-property.md)</span></span>


 

 





