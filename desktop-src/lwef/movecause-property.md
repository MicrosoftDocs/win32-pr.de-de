---
title: Eigenschaft "muvecause"
description: Eigenschaft "muvecause"
ms.assetid: 8f78a6da-8498-4a39-a4b9-5ab7a43d97f5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dfc7f91d068befa2b919c04818c46dbc1a48faa0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856211"
---
# <a name="movecause-property"></a><span data-ttu-id="608b4-103">Eigenschaft "muvecause"</span><span class="sxs-lookup"><span data-stu-id="608b4-103">MoveCause Property</span></span>

<span data-ttu-id="608b4-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="608b4-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="608b4-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="608b4-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="608b4-106">Gibt einen ganzzahligen Wert zurück, der angibt, was das letzte Verschieben des Zeichens verursacht hat.</span><span class="sxs-lookup"><span data-stu-id="608b4-106">Returns an integer value that specifies what caused the character's last move.</span></span>

</dd> <dt>

<span data-ttu-id="608b4-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span><span class="sxs-lookup"><span data-stu-id="608b4-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="608b4-108">*Agent*. **Zeichen ("***Merkmal-ID***"). "Muvecause** "</span><span class="sxs-lookup"><span data-stu-id="608b4-108">*agent*.**Characters("***CharacterID***").MoveCause**</span></span>



| <span data-ttu-id="608b4-109">Wert</span><span class="sxs-lookup"><span data-stu-id="608b4-109">Value</span></span> | <span data-ttu-id="608b4-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="608b4-110">Description</span></span>                                                                                |
|-------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="608b4-111">0</span><span class="sxs-lookup"><span data-stu-id="608b4-111">0</span></span>     | <span data-ttu-id="608b4-112">Das Zeichen wurde nicht verschoben.</span><span class="sxs-lookup"><span data-stu-id="608b4-112">The character has not been moved.</span></span>                                                          |
| <span data-ttu-id="608b4-113">1</span><span class="sxs-lookup"><span data-stu-id="608b4-113">1</span></span>     | <span data-ttu-id="608b4-114">Der Benutzer hat das Zeichen verschoben.</span><span class="sxs-lookup"><span data-stu-id="608b4-114">The user moved the character.</span></span>                                                              |
| <span data-ttu-id="608b4-115">2</span><span class="sxs-lookup"><span data-stu-id="608b4-115">2</span></span>     | <span data-ttu-id="608b4-116">Die Anwendung hat das Zeichen verschoben.</span><span class="sxs-lookup"><span data-stu-id="608b4-116">Your application moved the character.</span></span>                                                      |
| <span data-ttu-id="608b4-117">3</span><span class="sxs-lookup"><span data-stu-id="608b4-117">3</span></span>     | <span data-ttu-id="608b4-118">Das Zeichen wurde von einer anderen Client Anwendung verschoben.</span><span class="sxs-lookup"><span data-stu-id="608b4-118">Another client application moved the character.</span></span>                                            |
| <span data-ttu-id="608b4-119">4</span><span class="sxs-lookup"><span data-stu-id="608b4-119">4</span></span>     | <span data-ttu-id="608b4-120">Der Agent-Server hat das Zeichen verschoben, um es nach einer Änderung der Bildschirmauflösung auf dem Bildschirm aufzubewahren.</span><span class="sxs-lookup"><span data-stu-id="608b4-120">The Agent server moved the character to keep it onscreen after a screen resolution change.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="608b4-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="608b4-121">Remarks</span></span>

<span data-ttu-id="608b4-122">Sie können diese Eigenschaft verwenden, um zu bestimmen, was das Zeichen bewegt hat, wenn mehr als eine Anwendung das gleiche Zeichen gemeinsam nutzt (hat geladen).</span><span class="sxs-lookup"><span data-stu-id="608b4-122">You can use this property to determine what caused the character to move, when more than one application is sharing (has loaded) the same character.</span></span> <span data-ttu-id="608b4-123">Diese Werte sind identisch mit denen, die vom [**Move**](move-event.md) -Ereignis zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="608b4-123">These values are the same as those returned by the [**Move**](move-event.md) event.</span></span>

## <a name="see-also"></a><span data-ttu-id="608b4-124">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="608b4-124">See Also</span></span>

<span data-ttu-id="608b4-125">[**Move-Ereignis**](move-event.md), [ **MoveTo-Methode**](moveto-method.md)</span><span class="sxs-lookup"><span data-stu-id="608b4-125">[**Move event**](move-event.md), [**MoveTo method**](moveto-method.md)</span></span>


 

 




