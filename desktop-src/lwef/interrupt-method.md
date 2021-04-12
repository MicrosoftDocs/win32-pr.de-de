---
title: Interrupt-Methode
description: Interrupt-Methode
ms.assetid: b8442e25-a629-47c7-acdd-1d28e74d78a2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d58050e181525cc4a4b9f35ec169e92d91ab28e7
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104390323"
---
# <a name="interrupt-method"></a><span data-ttu-id="32430-103">Interrupt-Methode</span><span class="sxs-lookup"><span data-stu-id="32430-103">Interrupt Method</span></span>

<span data-ttu-id="32430-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="32430-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="32430-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="32430-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="32430-106">Unterbricht die Animation für das angegebene Zeichen.</span><span class="sxs-lookup"><span data-stu-id="32430-106">Interrupts the animation for the specified character.</span></span>

</dd> <dt>

<span data-ttu-id="32430-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span><span class="sxs-lookup"><span data-stu-id="32430-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="32430-108">\*Agent ***. Zeichen ("*** Merkmal-ID \* \* *"). Interrupt*- \*  *Anforderung*</span><span class="sxs-lookup"><span data-stu-id="32430-108">*agent ***.Characters ("*** CharacterID\*\*\*").Interrupt*\* *Request*</span></span>



| <span data-ttu-id="32430-109">Teil</span><span class="sxs-lookup"><span data-stu-id="32430-109">Part</span></span>      | <span data-ttu-id="32430-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="32430-110">Description</span></span>                                                                  |
|-----------|------------------------------------------------------------------------------|
| <span data-ttu-id="32430-111">*Anforderung*</span><span class="sxs-lookup"><span data-stu-id="32430-111">*Request*</span></span> | <span data-ttu-id="32430-112">Ein [**Anforderungs**](/windows/desktop/lwef/the-request-object) Objekt für einen bestimmten Animations Aufruf.</span><span class="sxs-lookup"><span data-stu-id="32430-112">A [**Request**](/windows/desktop/lwef/the-request-object) object for a particular animation call.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="32430-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="32430-113">Remarks</span></span>

<span data-ttu-id="32430-114">Damit können Sie die Animation zwischen Zeichen synchronisieren.</span><span class="sxs-lookup"><span data-stu-id="32430-114">You can use this to sync up animation between characters.</span></span> <span data-ttu-id="32430-115">Wenn sich z. b. ein anderes Zeichen in einer Schleifen Animation befindet, beendet diese Methode die Schleife und wechselt zur nächsten Animation in der Warteschlange des Zeichens.</span><span class="sxs-lookup"><span data-stu-id="32430-115">For example, if another character is in a looping animation, this method will stop the loop and move to the next animation in the character's queue.</span></span> <span data-ttu-id="32430-116">Eine Zeichen Animation, die Sie nicht verwenden (die Sie nicht geladen haben), kann nicht unterbrochen werden.</span><span class="sxs-lookup"><span data-stu-id="32430-116">You cannot interrupt a character animation that you are not using (that you have not loaded).</span></span>

<span data-ttu-id="32430-117">Um den Anforderungs Parameter anzugeben, müssen Sie eine Variable erstellen und die Animations Anforderung zuweisen, die Sie unterbrechen möchten:</span><span class="sxs-lookup"><span data-stu-id="32430-117">To specify the request parameter, you must create a variable and assign the animation request you want to interrupt:</span></span>


```
   Dim GenieRequest as Object
   Dim RobbyRequest as Object
   Dim Genie as Object
   Dim Robby as Object

   Sub FormLoad()

      MyAgent1.Characters.Load "Genie", "Genie.acs"

      MyAgent1.Characters.Load "Robby", "Robby.acs"

      Set Genie = MyAgent1.Characters ("Genie")
      Set Robby = MyAgent1.Characters ("Robby")

      Genie.Show

      Genie.Speak "Just a moment"

      Set GenieRequest = Genie.Play ("Processing")

      Robby.Show
      Robby.Play "confused"
      Robby.Speak "Hey, Genie. What are you doing?"
      Robby.Interrupt GenieRequest

      Genie.Speak "I was just checking on something."

   End Sub
```



<span data-ttu-id="32430-118">Sie können die Animation desselben Zeichen, das Sie in dieser Methode angeben, nicht unterbrechen, da der Server die **Interrupt** -Methode in die Animations Warteschlange dieses Zeichens eingereiht.</span><span class="sxs-lookup"><span data-stu-id="32430-118">You cannot interrupt the animation of the same character you specify in this method because the server queues the **Interrupt** method in that character's animation queue.</span></span> <span data-ttu-id="32430-119">Daher können Sie nur **Interrupt** verwenden, um die Animation eines anderen Zeichens anzuhalten, das Sie geladen haben.</span><span class="sxs-lookup"><span data-stu-id="32430-119">Therefore, you can only use **Interrupt** to halt the animation of another character you have loaded.</span></span>

<span data-ttu-id="32430-120">Wenn Sie einen Objekt Verweis deklarieren und diesen auf diese Methode festlegen, wird ein [**Anforderungs**](/windows/desktop/lwef/the-request-object) Objekt zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="32430-120">If you declare an object reference and set it to this method, it returns a [**Request**](/windows/desktop/lwef/the-request-object) object.</span></span>

> [!Note]  
> <span data-ttu-id="32430-121">Der **Interrupt** leert die Warteschlange des Zeichens nicht. Sie hält die vorhandene Animation an und wechselt zur nächsten Animation in der Warteschlange des Zeichens.</span><span class="sxs-lookup"><span data-stu-id="32430-121">**Interrupt** does not flush the character's queue; it halts the existing animation and moves on to the next animation in the character's queue.</span></span> <span data-ttu-id="32430-122">Verwenden Sie die Stop-Methode, um die Warteschlange eines Zeichens [**anzuhalten**](stop-method.md) und zu leeren.</span><span class="sxs-lookup"><span data-stu-id="32430-122">To halt and flush a character's queue, use the [**Stop**](stop-method.md) method.</span></span>

 

## <a name="see-also"></a><span data-ttu-id="32430-123">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="32430-123">See Also</span></span>

[<span data-ttu-id="32430-124">**Stop-Methode**</span><span class="sxs-lookup"><span data-stu-id="32430-124">**Stop method**</span></span>](stop-method.md)


 

 