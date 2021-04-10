---
title: Visible-Eigenschaft (Sprechblasen Objekt)
description: Visible-Eigenschaft
ms.assetid: cbda7f69-889a-45a0-9549-d27eddfcec57
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba58993a3328a4c99dbe7da43b43460f6048bf57
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "104039909"
---
# <a name="visible-property-balloon-object"></a><span data-ttu-id="f817d-103">Visible-Eigenschaft (Sprechblasen Objekt)</span><span class="sxs-lookup"><span data-stu-id="f817d-103">Visible Property (Balloon Object)</span></span>

<span data-ttu-id="f817d-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="f817d-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="f817d-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="f817d-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="f817d-106">Gibt die sichtbare Einstellung für die Word-Sprechblase für das angegebene Zeichen zurück oder legt diese fest.</span><span class="sxs-lookup"><span data-stu-id="f817d-106">Returns or sets the visible setting for the word balloon for the specified character.</span></span>

</dd> <dt>

<span data-ttu-id="f817d-107"><span id="Syntax_"></span><span id="syntax_"></span><span id="SYNTAX_"></span>**Syntax**</span><span class="sxs-lookup"><span data-stu-id="f817d-107"><span id="Syntax_"></span><span id="syntax_"></span><span id="SYNTAX_"></span>**Syntax**</span></span> 
</dt> <dd>

<span data-ttu-id="f817d-108">\*Agent \***. Zeichen (**"\* Merkmal-ID \*" \* *). Sprechblase. sichtbarer* \*  \[  =  *boolescher* Wert\]</span><span class="sxs-lookup"><span data-stu-id="f817d-108">*agent\***.Characters(**"* CharacterID *"\*\*).Balloon.Visible*\* \[ = *boolean*\]</span></span>



| <span data-ttu-id="f817d-109">Teil</span><span class="sxs-lookup"><span data-stu-id="f817d-109">Part</span></span>      | <span data-ttu-id="f817d-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f817d-110">Description</span></span>                                                                                                                                                             |
|-----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f817d-111">*boolean*</span><span class="sxs-lookup"><span data-stu-id="f817d-111">*boolean*</span></span> | <span data-ttu-id="f817d-112">Ein boolescher Ausdruck, der angibt, ob die Wort Sprechblase sichtbar ist.</span><span class="sxs-lookup"><span data-stu-id="f817d-112">A Boolean expression specifying whether the word balloon is visible.</span></span><br/> <span data-ttu-id="f817d-113">**True** Die Sprechblase ist sichtbar.</span><span class="sxs-lookup"><span data-stu-id="f817d-113">**True** The balloon is visible.</span></span><br/> <span data-ttu-id="f817d-114">**False** Die Sprechblase ist ausgeblendet.</span><span class="sxs-lookup"><span data-stu-id="f817d-114">**False** The balloon is hidden.</span></span><br/> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f817d-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f817d-115">Remarks</span></span>

<span data-ttu-id="f817d-116">Wenn Sie einen Gespräch [**oder einen**](speak-method.md) Ansichts Versuch mit einer-Anweisung befolgen, um zu versuchen, die-Eigenschaft der Sprechblase zu ändern, wirkt sich dies möglicherweise nicht auf den sichtbaren Zustand **der Sprechblase** aus, da der **Sprech** -oder [**der Ansichts**](think-method.md) Rückruf in die Warteschlange eingereiht wird</span><span class="sxs-lookup"><span data-stu-id="f817d-116">If you follow a [**Speak**](speak-method.md) or [**Think**](think-method.md) call with a statement to attempt to change the balloon's property, it may not affect the balloon's Visible state because the **Speak** or **Think** call gets queued, but the call setting the balloon's visible state does not.</span></span> <span data-ttu-id="f817d-117">Legen Sie diesen Wert daher nur dann fest, wenn sich keine **Sprech** **-oder Aufruf** Anrufe in der Warteschlange des Zeichens befinden.</span><span class="sxs-lookup"><span data-stu-id="f817d-117">Therefore, only set this value when no **Speak** or **Think** calls are in the character's queue.</span></span>

<span data-ttu-id="f817d-118">Wenn Sie versuchen, diese Eigenschaft festzulegen, während das Zeichen gerade gesprochen, bewegt oder gezogen wird, wird die Einstellung der Eigenschaft erst wirksam, wenn der vorherige Vorgang abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="f817d-118">If you attempt to set this property while the character is speaking, moving, or being dragged, the property setting does not take effect until the preceding operation is completed.</span></span>

<span data-ttu-id="f817d-119">Durch [**das Aufrufen**](visible-property.md) der Methoden "sprechen" und " [**Think**](think-method.md) " wird der [**Sprech**](speak-method.md) Blasen automatisch angezeigt</span><span class="sxs-lookup"><span data-stu-id="f817d-119">Calling the [**Speak**](speak-method.md) and [**Think**](think-method.md) methods automatically makes the balloon visible, setting the [**Visible**](visible-property.md) property to **True**.</span></span> <span data-ttu-id="f817d-120">Wenn die Eigenschaft für das automatische Ausblenden des Sprechers des Zeichens aktiviert ist, wird die Sprechblase automatisch ausgeblendet, nachdem der Ausgabetext gesprochen wurde.</span><span class="sxs-lookup"><span data-stu-id="f817d-120">If the character's balloon AutoHide property is enabled, the balloon is automatically hidden after the output text is spoken.</span></span> <span data-ttu-id="f817d-121">Durch Klicken oder Ziehen eines Zeichens, das derzeit nicht gesprochen wird, wird auch dann automatisch die Sprechblase ausgeblendet, wenn die Einstellung für das automatische ausblenden deaktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="f817d-121">Clicking or dragging a character that is not currently speaking also automatically hides the balloon even if its AutoHide setting is disabled.</span></span> <span data-ttu-id="f817d-122">Sie können die Einstellung für das automatische Ausblenden des Zeichens mithilfe der [**Style**](style-property.md) -Eigenschaft des sprechenden-Objekts ändern.</span><span class="sxs-lookup"><span data-stu-id="f817d-122">You can change the character's AutoHide setting using the balloon's [**Style**](style-property.md) property.</span></span>

### <a name="see-also"></a><span data-ttu-id="f817d-123">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="f817d-123">See Also</span></span>

[<span data-ttu-id="f817d-124">**Style-Eigenschaft**</span><span class="sxs-lookup"><span data-stu-id="f817d-124">**Style property**</span></span>](style-property.md)


 

 





