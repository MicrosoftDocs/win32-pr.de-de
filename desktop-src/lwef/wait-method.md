---
title: Wait-Methode
description: Wait-Methode
ms.assetid: 968a3f19-6953-473b-ba98-0dc93696e703
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f2e94b0f765a9861c30b254761fbc4dc2e72763
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "106341923"
---
# <a name="wait-method"></a><span data-ttu-id="0fea3-103">Wait-Methode</span><span class="sxs-lookup"><span data-stu-id="0fea3-103">Wait Method</span></span>

<span data-ttu-id="0fea3-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="0fea3-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="0fea3-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="0fea3-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="0fea3-106">Bewirkt, dass die Animations Warteschlange für das angegebene Zeichen wartet, bis die angegebene Animations Anforderung abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="0fea3-106">Causes the animation queue for the specified character to wait until the specified animation request completes.</span></span>

</dd> <dt>

<span data-ttu-id="0fea3-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span><span class="sxs-lookup"><span data-stu-id="0fea3-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="0fea3-108">*Agent ***. Zeichen ("*** Merkmal-ID ***"). Warte*** Anforderung*</span><span class="sxs-lookup"><span data-stu-id="0fea3-108">*agent ***.Characters ("*** CharacterID ***").Wait*** Request*</span></span>



| <span data-ttu-id="0fea3-109">Teil</span><span class="sxs-lookup"><span data-stu-id="0fea3-109">Part</span></span>      | <span data-ttu-id="0fea3-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0fea3-110">Description</span></span>                                                                     |
|-----------|---------------------------------------------------------------------------------|
| <span data-ttu-id="0fea3-111">*Anforderung*</span><span class="sxs-lookup"><span data-stu-id="0fea3-111">*Request*</span></span> | <span data-ttu-id="0fea3-112">Ein [**Anforderungs**](/windows/desktop/lwef/the-request-object) Objekt, das eine bestimmte Animation angibt.</span><span class="sxs-lookup"><span data-stu-id="0fea3-112">A [**Request**](/windows/desktop/lwef/the-request-object) object specifying a particular animation..</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0fea3-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0fea3-113">Remarks</span></span>

<span data-ttu-id="0fea3-114">Verwenden Sie diese Methode nur, wenn Sie mehrere (gleichzeitige) Zeichen unterstützen und versuchen, die Interaktion von Zeichen zu sequenzieren.</span><span class="sxs-lookup"><span data-stu-id="0fea3-114">Use this method only when you support multiple (simultaneous) characters and are trying to sequence the interaction of characters.</span></span> <span data-ttu-id="0fea3-115">(Bei einem einzelnen Zeichen wird jede Animations Anforderung sequenziell wiedergegeben, nachdem die vorherige Anforderung abgeschlossen wurde.) Wenn Sie zwei Zeichen haben und die Animations Anforderung eines Zeichens warten soll, bis die Animation des anderen Zeichens abgeschlossen ist, legen Sie die **Wait** -Methode auf das Animations [**Anforderungs**](/windows/desktop/lwef/the-request-object) Objekt für das andere Zeichen fest.</span><span class="sxs-lookup"><span data-stu-id="0fea3-115">(For a single character, each animation request is played sequentially--after the previous request completes.) If you have two characters and you want a character's animation request to wait until the other character's animation completes, set the **Wait** method to the other character's animation [**Request**](/windows/desktop/lwef/the-request-object) object.</span></span> <span data-ttu-id="0fea3-116">Um den Anforderungs Parameter anzugeben, müssen Sie eine Variable erstellen und die Animations Anforderung zuweisen, die Sie unterbrechen möchten:</span><span class="sxs-lookup"><span data-stu-id="0fea3-116">To specify the request parameter, you must create a variable and assign the animation request you want to interrupt:</span></span>


```
   Dim GenieRequest 
   Dim RobbyRequest 
   Dim Genie 
   Dim Robby 

   Sub window_Onload

   Agent1.Characters.Load "Genie", "https://agent.microsoft.com/characters/v2/genie/genie.acf"
   Agent1.Characters.Load "Robby", "https://agent.microsoft.com/characters/v2/robby/robby.acf"

   Set Genie = Agent1.Characters("Genie")
   Set Robby = Agent1.Characters("Robby")

   Genie.Get "State", "Showing"
   Robby.Get "State", "Showing"

   Genie.Get "Animation", "Announce, AnnounceReturn, Pleased, _ 
      PleasedReturn"
   
   Robby.Get "Animation", "Confused, ConfusedReturn, Sad, SadReturn"

   Set Genie = Agent1.Characters ("Genie")
   Set Robby = Agent1.Characters ("Robby")

   Genie.MoveTo 100,100
   Genie.Show

   Robby.MoveTo 250,100
   Robby.Show

   Genie.Play "Announce"
   Set GenieRequest = Genie.Speak ("Why did the chicken cross the road?")
   
   Robby.Wait GenieRequest
   Robby.Play "Confused"
   Set RobbyRequest = Robby.Speak ("I don't know. Why did the chicken _
      cross the road?")
   
   Genie.Wait RobbyRequest
   Genie.Play "Pleased"
   Set GenieRequest = Genie.Speak ("To get to the other side.")
   
   Robby.Wait GenieRequest
   Robby.Play "Sad"
   Robby.Speak "I never should have asked."

   End Sub
```



<span data-ttu-id="0fea3-117">Sie können den Code auch optimieren, indem Sie einfach **Wait** direkt aufrufen, indem Sie eine bestimmte Animations Anforderung verwenden.</span><span class="sxs-lookup"><span data-stu-id="0fea3-117">You can also streamline your code by just calling **Wait** directly, using a specific animation request.</span></span>


```
   Robby.Wait Genie.Play "GestureRight"
```



<span data-ttu-id="0fea3-118">Dadurch ist es nicht erforderlich, ein [**Anforderungs**](/windows/desktop/lwef/the-request-object) Objekt explizit zu deklarieren.</span><span class="sxs-lookup"><span data-stu-id="0fea3-118">This avoids having to explicitly declare a [**Request**](/windows/desktop/lwef/the-request-object) object.</span></span>

 

 