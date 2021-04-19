---
title: Listeningtip (Eigenschaft)
description: Listeningtip (Eigenschaft)
ms.assetid: 02a678bb-5eb6-495f-b339-35170a44b15e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 402fd970bf902f034fd6ffb713029e3a27095c8e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106340857"
---
# <a name="listeningtip-property"></a><span data-ttu-id="b9c46-103">Listeningtip (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="b9c46-103">ListeningTip Property</span></span>

<span data-ttu-id="b9c46-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="b9c46-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="b9c46-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="b9c46-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="b9c46-106">Gibt einen booleschen Wert zurück, der die aktuelle Benutzereinstellung für den hörenden Tipp angibt.</span><span class="sxs-lookup"><span data-stu-id="b9c46-106">Returns a Boolean indicating the current user setting for the Listening Tip.</span></span>

</dd> <dt>

<span data-ttu-id="b9c46-107"><span id="Syntax_"></span><span id="syntax_"></span><span id="SYNTAX_"></span>**Syntax**</span><span class="sxs-lookup"><span data-stu-id="b9c46-107"><span id="Syntax_"></span><span id="syntax_"></span><span id="SYNTAX_"></span>**Syntax**</span></span> 
</dt> <dd>

<span data-ttu-id="b9c46-108">*Agent \* \* *. Speechinput. listeningtip**</span><span class="sxs-lookup"><span data-stu-id="b9c46-108">*agent\*\*\*.SpeechInput.ListeningTip*\*</span></span>



| <span data-ttu-id="b9c46-109">Wert</span><span class="sxs-lookup"><span data-stu-id="b9c46-109">Value</span></span>     | <span data-ttu-id="b9c46-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b9c46-110">Description</span></span>                    |
|-----------|--------------------------------|
| <span data-ttu-id="b9c46-111">**True**</span><span class="sxs-lookup"><span data-stu-id="b9c46-111">**True**</span></span>  | <span data-ttu-id="b9c46-112">Der Abhör Tipp ist aktiviert.</span><span class="sxs-lookup"><span data-stu-id="b9c46-112">The Listening Tip is enabled.</span></span>  |
| <span data-ttu-id="b9c46-113">**False**</span><span class="sxs-lookup"><span data-stu-id="b9c46-113">**False**</span></span> | <span data-ttu-id="b9c46-114">Der Abhör Tipp ist deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="b9c46-114">The Listening Tip is disabled.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b9c46-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b9c46-115">Remarks</span></span>

<span data-ttu-id="b9c46-116">Die **listeningtip** -Eigenschaft gibt an, ob die Option zum Anzeigen von Abhör Tipps auf der Eigenschaften Seite des Microsoft-Agents (erweiterte Zeichen Optionen) aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="b9c46-116">The **ListeningTip** property indicates whether the Display Listening Tip option in the Microsoft Agent property sheet (Advanced Character Options) is enabled.</span></span> <span data-ttu-id="b9c46-117">Wenn **listeningtip** **true** zurückgibt und die Spracheingabe aktiviert ist, zeigt der Server das Tip-Fenster an, wenn der Benutzer die Abhör Taste drückt.</span><span class="sxs-lookup"><span data-stu-id="b9c46-117">When **ListeningTip** returns **True** and speech input is enabled, the server displays the tip window when the user presses the Listening key.</span></span>

## <a name="see-also"></a><span data-ttu-id="b9c46-118">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="b9c46-118">See Also</span></span>

[<span data-ttu-id="b9c46-119">**Agentpropertychange-Ereignis**</span><span class="sxs-lookup"><span data-stu-id="b9c46-119">**AgentPropertyChange event**</span></span>](agentpropertychange-event.md)


 

 




