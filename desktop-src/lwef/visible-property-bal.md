---
title: Visible-Eigenschaft (Balloon-Objekt)
description: Erfahren Sie mehr über die Visible-Eigenschaft des Balloon-Objekts, die die sichtbare Einstellung für das Wort balloon für das angegebene Zeichen zurückgibt oder legt.
ms.assetid: cbda7f69-889a-45a0-9549-d27eddfcec57
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93ac587fa649f2a8ccb5ea83ddc077050a8548d2
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112396325"
---
# <a name="visible-property-balloon-object"></a><span data-ttu-id="96da2-103">Visible-Eigenschaft (Balloon-Objekt)</span><span class="sxs-lookup"><span data-stu-id="96da2-103">Visible Property (Balloon Object)</span></span>

<span data-ttu-id="96da2-104">\[Microsoft Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht mehr verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="96da2-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="96da2-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="96da2-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="96da2-106">Gibt die sichtbare Einstellung für das Wort balloon für das angegebene Zeichen zurück oder legt diese fest.</span><span class="sxs-lookup"><span data-stu-id="96da2-106">Returns or sets the visible setting for the word balloon for the specified character.</span></span>

</dd> <dt>

<span data-ttu-id="96da2-107"><span id="Syntax_"></span><span id="syntax_"></span><span id="SYNTAX_"></span>**Syntax**</span><span class="sxs-lookup"><span data-stu-id="96da2-107"><span id="Syntax_"></span><span id="syntax_"></span><span id="SYNTAX_"></span>**Syntax**</span></span> 
</dt> <dd>

<span data-ttu-id="96da2-108">*agent\***. Characters(**"* CharacterID *"\*\*). Balloon.Visible* \*  \[  =  *boolean*\]</span><span class="sxs-lookup"><span data-stu-id="96da2-108">*agent\***.Characters(**"* CharacterID *"\*\*).Balloon.Visible*\* \[ = *boolean*\]</span></span>



| <span data-ttu-id="96da2-109">Teil</span><span class="sxs-lookup"><span data-stu-id="96da2-109">Part</span></span>      | <span data-ttu-id="96da2-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="96da2-110">Description</span></span>                                                                                                                                                             |
|-----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="96da2-111">*boolean*</span><span class="sxs-lookup"><span data-stu-id="96da2-111">*boolean*</span></span> | <span data-ttu-id="96da2-112">Ein boolescher Ausdruck, der an gibt, ob das Wort Balloon sichtbar ist.</span><span class="sxs-lookup"><span data-stu-id="96da2-112">A Boolean expression specifying whether the word balloon is visible.</span></span><br/> <span data-ttu-id="96da2-113">**True** Die Sprechblase ist sichtbar.</span><span class="sxs-lookup"><span data-stu-id="96da2-113">**True** The balloon is visible.</span></span><br/> <span data-ttu-id="96da2-114">**False** Die Sprechblase ist ausgeblendet.</span><span class="sxs-lookup"><span data-stu-id="96da2-114">**False** The balloon is hidden.</span></span><br/> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="96da2-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="96da2-115">Remarks</span></span>

<span data-ttu-id="96da2-116">Wenn Sie [](speak-method.md) einem Speak- oder [**Think-Aufruf**](think-method.md) mit einer -Anweisung folgen, um zu versuchen, die -Eigenschaft des Sprechblasens zu ändern, wirkt sich dies möglicherweise nicht auf den Sichtbar-Zustand des Balloons aus, da der **Speak-** oder **Think-Aufruf** in die Warteschlange gestellt wird, aber der Aufruf, der den sichtbaren Zustand des Balloons ansteuert, nicht.</span><span class="sxs-lookup"><span data-stu-id="96da2-116">If you follow a [**Speak**](speak-method.md) or [**Think**](think-method.md) call with a statement to attempt to change the balloon's property, it may not affect the balloon's Visible state because the **Speak** or **Think** call gets queued, but the call setting the balloon's visible state does not.</span></span> <span data-ttu-id="96da2-117">Legen Sie diesen Wert daher nur fest, wenn **sich keine Speak-** oder **Think-Aufrufe** in der Warteschlange des Zeichens befinden.</span><span class="sxs-lookup"><span data-stu-id="96da2-117">Therefore, only set this value when no **Speak** or **Think** calls are in the character's queue.</span></span>

<span data-ttu-id="96da2-118">Wenn Sie versuchen, diese Eigenschaft während des Sprechens, Verschiebens oder Ziehens des Zeichens zu setzen, wird die Eigenschafteneinstellung erst wirksam, wenn der vorherige Vorgang abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="96da2-118">If you attempt to set this property while the character is speaking, moving, or being dragged, the property setting does not take effect until the preceding operation is completed.</span></span>

<span data-ttu-id="96da2-119">Durch Aufrufen [**der Speak-**](speak-method.md) [**und Think-Methoden**](think-method.md) wird der Balloon automatisch sichtbar, und die [**Visible-Eigenschaft**](visible-property.md) wird auf **True (Wahr) festlegen.**</span><span class="sxs-lookup"><span data-stu-id="96da2-119">Calling the [**Speak**](speak-method.md) and [**Think**](think-method.md) methods automatically makes the balloon visible, setting the [**Visible**](visible-property.md) property to **True**.</span></span> <span data-ttu-id="96da2-120">Wenn die AutoHide-Eigenschaft des Zeichens aktiviert ist, wird die Sprechblase automatisch ausgeblendet, nachdem der Ausgabetext gesprochen wurde.</span><span class="sxs-lookup"><span data-stu-id="96da2-120">If the character's balloon AutoHide property is enabled, the balloon is automatically hidden after the output text is spoken.</span></span> <span data-ttu-id="96da2-121">Wenn Sie auf ein Zeichen klicken oder ziehen, das derzeit nicht spricht, wird der Balloon auch dann automatisch ausblendet, wenn die Einstellung AutoHide deaktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="96da2-121">Clicking or dragging a character that is not currently speaking also automatically hides the balloon even if its AutoHide setting is disabled.</span></span> <span data-ttu-id="96da2-122">Sie können die Einstellung AutoHide des Zeichens ändern, indem Sie die [**Style-Eigenschaft**](style-property.md) des Balloons verwenden.</span><span class="sxs-lookup"><span data-stu-id="96da2-122">You can change the character's AutoHide setting using the balloon's [**Style**](style-property.md) property.</span></span>

### <a name="see-also"></a><span data-ttu-id="96da2-123">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="96da2-123">See Also</span></span>

[<span data-ttu-id="96da2-124">**Style-Eigenschaft**</span><span class="sxs-lookup"><span data-stu-id="96da2-124">**Style property**</span></span>](style-property.md)


 

 





