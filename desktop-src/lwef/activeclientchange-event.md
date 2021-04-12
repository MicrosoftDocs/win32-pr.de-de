---
title: Activeclientchange-Ereignis
description: Activeclientchange-Ereignis
ms.assetid: 617b40e6-cafb-463e-8b36-2a12c468d3ae
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8137edd559d934fd1a478350cd1185885c7dc148
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104206754"
---
# <a name="activeclientchange-event"></a><span data-ttu-id="8917f-103">Activeclientchange-Ereignis</span><span class="sxs-lookup"><span data-stu-id="8917f-103">ActiveClientChange Event</span></span>

<span data-ttu-id="8917f-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="8917f-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="8917f-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="8917f-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="8917f-106">Tritt auf, wenn sich der aktive Client des Zeichens ändert.</span><span class="sxs-lookup"><span data-stu-id="8917f-106">Occurs when the active client of the character changes.</span></span>

</dd> <dt>

<span data-ttu-id="8917f-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span><span class="sxs-lookup"><span data-stu-id="8917f-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="8917f-108">**Unter** geordneter *Agent.* Activeclientchange (ByVal- *Kenn Zeichnerkennung*, ByVal *aktiv* **)**</span><span class="sxs-lookup"><span data-stu-id="8917f-108">**Sub** *agent.* ActiveClientChange (ByVal *CharacterID*, ByVal *Active* **)**</span></span>



| <span data-ttu-id="8917f-109">Teil</span><span class="sxs-lookup"><span data-stu-id="8917f-109">Part</span></span>          | <span data-ttu-id="8917f-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8917f-110">Description</span></span>                                                                                                                                                                                                                                                        |
|---------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8917f-111">*Merkmal-ID*</span><span class="sxs-lookup"><span data-stu-id="8917f-111">*CharacterID*</span></span> | <span data-ttu-id="8917f-112">Gibt die ID des Zeichens zurück, für das das Ereignis aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="8917f-112">Returns the ID of the character for which the event occurred.</span></span>                                                                                                                                                                                                      |
| <span data-ttu-id="8917f-113">*Aktiv*</span><span class="sxs-lookup"><span data-stu-id="8917f-113">*Active*</span></span>      | <span data-ttu-id="8917f-114">Ein boolescher Wert, der angibt, ob der Client aktiv oder nicht aktiv geworden ist.</span><span class="sxs-lookup"><span data-stu-id="8917f-114">A Boolean value that indicates whether the client became active or not active.</span></span> <span data-ttu-id="8917f-115">**True** Die Client Anwendung wurde zum aktiven Client des Zeichens.</span><span class="sxs-lookup"><span data-stu-id="8917f-115">**True** The client application became the active client of the character.</span></span> <br/> <span data-ttu-id="8917f-116">**False** Die Client Anwendung ist nicht mehr der aktive Client des Zeichens.</span><span class="sxs-lookup"><span data-stu-id="8917f-116">**False** The client application is no longer the active client of the character.</span></span><br/> |



 

</dd> </dl>

### <a name="remarks"></a><span data-ttu-id="8917f-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8917f-117">Remarks</span></span>

<span data-ttu-id="8917f-118">Wenn mehrere Client Anwendungen dasselbe Zeichen gemeinsam verwenden, empfängt der aktive Client des Zeichens Maus Eingaben (z. b. Click-oder Drag-Ereignisse der Microsoft-agentsteuerung).</span><span class="sxs-lookup"><span data-stu-id="8917f-118">When multiple client applications share the same character, the active client of the character receives mouse input (for example, Microsoft Agent control click or drag events).</span></span> <span data-ttu-id="8917f-119">Wenn mehrere Zeichen angezeigt werden, empfängt der aktive Client des obersten Zeichens (auch als Input-Active Client bezeichnet) [Befehls](command-event.md) Ereignisse.</span><span class="sxs-lookup"><span data-stu-id="8917f-119">Similarly, when multiple characters are displayed, the active client of the topmost character (also known as the input-active client) receives [Command](command-event.md) events.</span></span>

<span data-ttu-id="8917f-120">Wenn sich der aktive Client eines Zeichens ändert, übergibt dieses Ereignis die ID dieses Zeichens und **true** , wenn die Anwendung zum aktiven Client des Zeichens geworden ist, oder **false** , wenn es nicht mehr der aktive Client des Zeichens ist.</span><span class="sxs-lookup"><span data-stu-id="8917f-120">When the active client of a character changes, this event passes back the ID of that character and **True** if your application has become the active client of the character or **False** if it is no longer the active client of the character.</span></span>

<span data-ttu-id="8917f-121">Eine Client Anwendung empfängt dieses Ereignis möglicherweise, wenn der Benutzer den Eintrag einer Client Anwendung im Popupmenü des Zeichens oder per Sprachbefehl auswählt, wenn die Client Anwendung ihren aktiven Status ändert oder wenn eine andere Client Anwendung die Verbindung mit dem-Agent beendet.</span><span class="sxs-lookup"><span data-stu-id="8917f-121">A client application may receive this event when the user selects a client application's entry in character's pop-up menu or by voice command, when the client application changes its active status, or when another client application quits its connection to Agent.</span></span> <span data-ttu-id="8917f-122">Der-Agent sendet dieses Ereignis nur an die Client Anwendungen, die direkt betroffen sind. , die entweder zum aktiven Client werden oder den aktiven Client beendet.</span><span class="sxs-lookup"><span data-stu-id="8917f-122">Agent sends this event only to the client applications that are directly affected; that either become the active client or stop being the active client.</span></span>

### <a name="see-also"></a><span data-ttu-id="8917f-123">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="8917f-123">See Also</span></span>

<span data-ttu-id="8917f-124">[\* \* \* \* Activateinput \* \* Ereignis \* \*](activateinput-event.md), [\* \* \* \* aktiv \* \* Eigenschaft \* \*](active-property.md), \* \* \* \* [deactivateinput \* \* Ereignis \* \*](deactivateinput-event.md), [\* \* \* \* aktivieren \* \* Methode \* \*](activate-method.md)</span><span class="sxs-lookup"><span data-stu-id="8917f-124">[\*\*\*\*ActivateInput\*\* event\*\*](activateinput-event.md), [\*\*\*\*Active\*\* property\*\*](active-property.md), [\*\*\*\*DeactivateInput\*\* event\*\*](deactivateinput-event.md), [\*\*\*\*Activate\*\* method\*\*](activate-method.md)</span></span>


 

 





