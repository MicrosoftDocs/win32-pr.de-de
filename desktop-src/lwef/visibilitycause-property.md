---
title: Visibilitycause (Eigenschaft)
description: Visibilitycause (Eigenschaft)
ms.assetid: 106574ef-af5f-44cf-9efb-9e6da19ebc1f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a6e21e2cda201f8d04837d2b10efc757b93f824
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388345"
---
# <a name="visibilitycause-property"></a><span data-ttu-id="12fdd-103">Visibilitycause (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="12fdd-103">VisibilityCause Property</span></span>

<span data-ttu-id="12fdd-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="12fdd-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="12fdd-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="12fdd-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="12fdd-106">Gibt einen ganzzahligen Wert zurück, der angibt, wodurch der sichtbare Zustand des Zeichens verursacht wurde.</span><span class="sxs-lookup"><span data-stu-id="12fdd-106">Returns an integer value that specifies what caused the character's visible state.</span></span>

</dd> <dt>

<span data-ttu-id="12fdd-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span><span class="sxs-lookup"><span data-stu-id="12fdd-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="12fdd-108">*Agent*. **Zeichen ("***Merkmal-ID***"). Visibilitycause**</span><span class="sxs-lookup"><span data-stu-id="12fdd-108">*agent*.**Characters("***CharacterID***").VisibilityCause**</span></span>



| <span data-ttu-id="12fdd-109">Wert</span><span class="sxs-lookup"><span data-stu-id="12fdd-109">Value</span></span> | <span data-ttu-id="12fdd-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="12fdd-110">Description</span></span>                                                                                                  |
|-------|--------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="12fdd-111">0</span><span class="sxs-lookup"><span data-stu-id="12fdd-111">0</span></span>     | <span data-ttu-id="12fdd-112">Das Zeichen wurde nicht angezeigt.</span><span class="sxs-lookup"><span data-stu-id="12fdd-112">The character has not been shown.</span></span>                                                                            |
| <span data-ttu-id="12fdd-113">1</span><span class="sxs-lookup"><span data-stu-id="12fdd-113">1</span></span>     | <span data-ttu-id="12fdd-114">Der Benutzer hat das Zeichen mit dem Befehl im Popup Menü des Task leisten Symbols des Zeichens oder mithilfe der Spracheingabe ausgeblendet.</span><span class="sxs-lookup"><span data-stu-id="12fdd-114">User hid the character using the command on the character's taskbar icon pop-up menu or using speech input..</span></span> |
| <span data-ttu-id="12fdd-115">2</span><span class="sxs-lookup"><span data-stu-id="12fdd-115">2</span></span>     | <span data-ttu-id="12fdd-116">Der Benutzer hat das Zeichen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="12fdd-116">The user showed the character.</span></span>                                                                               |
| <span data-ttu-id="12fdd-117">3</span><span class="sxs-lookup"><span data-stu-id="12fdd-117">3</span></span>     | <span data-ttu-id="12fdd-118">Die Anwendung hat das Zeichen verborgen.</span><span class="sxs-lookup"><span data-stu-id="12fdd-118">Your application hid the character.</span></span>                                                                          |
| <span data-ttu-id="12fdd-119">4</span><span class="sxs-lookup"><span data-stu-id="12fdd-119">4</span></span>     | <span data-ttu-id="12fdd-120">Die Anwendung hat das Zeichen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="12fdd-120">Your application showed the character.</span></span>                                                                       |
| <span data-ttu-id="12fdd-121">5</span><span class="sxs-lookup"><span data-stu-id="12fdd-121">5</span></span>     | <span data-ttu-id="12fdd-122">Eine andere Client Anwendung hat das Zeichen verborgen.</span><span class="sxs-lookup"><span data-stu-id="12fdd-122">Another client application hid the character.</span></span>                                                                |
| <span data-ttu-id="12fdd-123">6</span><span class="sxs-lookup"><span data-stu-id="12fdd-123">6</span></span>     | <span data-ttu-id="12fdd-124">Das Zeichen wurde in einer anderen Client Anwendung angezeigt.</span><span class="sxs-lookup"><span data-stu-id="12fdd-124">Another client application showed the character.</span></span>                                                             |
| <span data-ttu-id="12fdd-125">7</span><span class="sxs-lookup"><span data-stu-id="12fdd-125">7</span></span>     | <span data-ttu-id="12fdd-126">Der Benutzer hat das Zeichen mit dem Befehl im Popup Menü des Zeichens ausgeblendet.</span><span class="sxs-lookup"><span data-stu-id="12fdd-126">The user hid the character using the command on the character's pop-up menu.</span></span>                                 |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="12fdd-127">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="12fdd-127">Remarks</span></span>

<span data-ttu-id="12fdd-128">Sie können diese Eigenschaft verwenden, um zu bestimmen, was bewirkt hat, dass das Zeichen verschoben wird, wenn mehr als eine Anwendung das gleiche Zeichen gemeinsam nutzt (hat geladen).</span><span class="sxs-lookup"><span data-stu-id="12fdd-128">You can use this property to determine what caused the character to move when more than one application is sharing (has loaded) the same character.</span></span> <span data-ttu-id="12fdd-129">Diese Werte sind identisch mit denen, die von den [**Show**](show-event.md) -und [**Hide**](hide-event.md) -Ereignissen zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="12fdd-129">These values are the same as those returned by the [**Show**](show-event.md) and [**Hide**](hide-event.md) events.</span></span>

## <a name="see-also"></a><span data-ttu-id="12fdd-130">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="12fdd-130">See Also</span></span>

<span data-ttu-id="12fdd-131">[**Ereignis ausblenden**](hide-event.md), [**Ereignis anzeigen**](show-event.md), [**Methode ausblenden**](hide-method.md), [**Methode anzeigen**](show-method.md)</span><span class="sxs-lookup"><span data-stu-id="12fdd-131">[**Hide event**](hide-event.md), [**Show event**](show-event.md), [**Hide method**](hide-method.md), [**Show method**](show-method.md)</span></span>


 

 




