---
title: Aktive Eigenschaft
description: Aktive Eigenschaft
ms.assetid: 76ada073-782a-4355-b4e8-42dd84d0139b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 061fe5fea7d94586c9f9d5c12b3a3b11ffbd7c3f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104206753"
---
# <a name="active-property"></a><span data-ttu-id="bb787-103">Aktive Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="bb787-103">Active Property</span></span>

<span data-ttu-id="bb787-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="bb787-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="bb787-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="bb787-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="bb787-106">Gibt zurück, ob es sich bei der Anwendung um den aktiven Client des Zeichens handelt und ob es sich um das oberste Zeichen handelt.</span><span class="sxs-lookup"><span data-stu-id="bb787-106">Returns whether your application is the active client of the character and whether the character is topmost.</span></span>

</dd> <dt>

<span data-ttu-id="bb787-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span><span class="sxs-lookup"><span data-stu-id="bb787-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="bb787-108">\*Agent. ***Zeichen \* \* \* \* ("*** Merkmal-ID \* \* *"). Aktiver* \*  \[  =  *Status*\]</span><span class="sxs-lookup"><span data-stu-id="bb787-108">*agent.\*\*\*Characters\*\*\*\*("*\*\* CharacterID\***").Active** \[ = *State*\]</span></span>



| <span data-ttu-id="bb787-109">Teil</span><span class="sxs-lookup"><span data-stu-id="bb787-109">Part</span></span>    | <span data-ttu-id="bb787-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="bb787-110">Description</span></span>                                                                                                                                                                                                |
|---------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bb787-111">*state*</span><span class="sxs-lookup"><span data-stu-id="bb787-111">*state*</span></span> | <span data-ttu-id="bb787-112">Ein ganzzahliger Ausdruck, der den Zustand der Client Anwendung angibt.</span><span class="sxs-lookup"><span data-stu-id="bb787-112">An integer expression specifying the state of your client application.</span></span> <span data-ttu-id="bb787-113">0 nicht der aktive Client.</span><span class="sxs-lookup"><span data-stu-id="bb787-113">0 Not the active client.</span></span><br/> <span data-ttu-id="bb787-114">1 der aktive Client.</span><span class="sxs-lookup"><span data-stu-id="bb787-114">1 The active client.</span></span> <br/> <span data-ttu-id="bb787-115">2 der Eingabe-aktiv-Client.</span><span class="sxs-lookup"><span data-stu-id="bb787-115">2 The input-active client.</span></span> <span data-ttu-id="bb787-116">(Das oberste Zeichen.)</span><span class="sxs-lookup"><span data-stu-id="bb787-116">(The topmost character.)</span></span><br/> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="bb787-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bb787-117">Remarks</span></span>

<span data-ttu-id="bb787-118">Wenn mehrere Client Anwendungen dasselbe Zeichen gemeinsam verwenden, empfängt der aktive Client des Zeichens Maus Eingaben (z. b. Microsoft Agent Control [**Click**](click-event.md) -oder [DragStart](dragstart-event.md) -Ereignisse).</span><span class="sxs-lookup"><span data-stu-id="bb787-118">When multiple client applications share the same character, the active client of the character receives mouse input (for example, Microsoft Agent control [**Click**](click-event.md) or [DragStart](dragstart-event.md) events).</span></span> <span data-ttu-id="bb787-119">Wenn mehrere Zeichen angezeigt werden, empfängt der aktive Client des obersten Zeichens (auch als Input-Active Client bezeichnet) Befehls Ereignisse.</span><span class="sxs-lookup"><span data-stu-id="bb787-119">Similarly, when multiple characters are displayed, the active client of the topmost character (also known as the input-active client) receives Command events.</span></span>

<span data-ttu-id="bb787-120">Mit der Methode " [**aktivieren**](activate-method.md)" können Sie festlegen, ob Ihre Anwendung der aktive Client des Zeichens ist, oder ob Sie die Anwendung als aktiven Client für die Anwendung festlegen möchten (wodurch das Zeichen auch am höchsten ist).</span><span class="sxs-lookup"><span data-stu-id="bb787-120">You can use the [**Activate**](activate-method.md)method to set whether your application is the active client of the character or to make your application the input active client (which also makes the character topmost).</span></span>

## <a name="see-also"></a><span data-ttu-id="bb787-121">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="bb787-121">See Also</span></span>

[<span data-ttu-id="bb787-122">Methode \* \* aktivieren \* \*</span><span class="sxs-lookup"><span data-stu-id="bb787-122">\*\*\*\*Activate\*\* method\*\*</span></span>](activate-method.md)


 

 





