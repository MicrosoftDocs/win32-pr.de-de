---
title: Iagentcharacter ausblenden
description: Iagentcharacter ausblenden
ms.assetid: a8128fe8-9a3b-41a3-bfe3-82ace1baff6f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bcd0ef91eb4d2738f19fb594ac1ab186efaec6e
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104038913"
---
# <a name="iagentcharacterhide"></a><span data-ttu-id="ec3d9-103">Iagentcharacter:: Hide</span><span class="sxs-lookup"><span data-stu-id="ec3d9-103">IAgentCharacter::Hide</span></span>

<span data-ttu-id="ec3d9-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="ec3d9-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT Hide(
   long bFast,      // play Hiding state animation flag
   long * pdwReqID  // address of request ID
);
```

<span data-ttu-id="ec3d9-105">Blendet das Zeichen aus.</span><span class="sxs-lookup"><span data-stu-id="ec3d9-105">Hides the character.</span></span>

-   <span data-ttu-id="ec3d9-106">Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="ec3d9-106">Returns S\_OK to indicate the operation was successful.</span></span> <span data-ttu-id="ec3d9-107">Wenn die Funktion zurückgibt, enthält *pdwreqid* die ID der Anforderung.</span><span class="sxs-lookup"><span data-stu-id="ec3d9-107">When the function returns, *pdwReqID* contains the ID of the request.</span></span>

<dl> <dt>

<span data-ttu-id="ec3d9-108"><span id="bFast"></span><span id="bfast"></span><span id="BFAST"></span>*BFAST*</span><span class="sxs-lookup"><span data-stu-id="ec3d9-108"><span id="bFast"></span><span id="bfast"></span><span id="BFAST"></span>*bFast*</span></span>
</dt> <dd>

<span data-ttu-id="ec3d9-109">Flag zum Ausblenden **des Zustands der** Animation.</span><span class="sxs-lookup"><span data-stu-id="ec3d9-109">**Hiding** state animation flag.</span></span> <span data-ttu-id="ec3d9-110">Wenn dieser Parameter **true** ist, wird die verborgene Animation nicht abgespielt, **bevor der Zeichen** Rahmen ausgeblendet wird. **false** gibt an, dass die Animation wiedergegeben wird.</span><span class="sxs-lookup"><span data-stu-id="ec3d9-110">If this parameter is **True**, the **Hiding** animation does not play before the character frame is hidden; if **False**, the animation plays.</span></span>

</dd> <dt>

<span data-ttu-id="ec3d9-111"><span id="pdwReqID"></span><span id="pdwreqid"></span><span id="PDWREQID"></span>*pdwreqid*</span><span class="sxs-lookup"><span data-stu-id="ec3d9-111"><span id="pdwReqID"></span><span id="pdwreqid"></span><span id="PDWREQID"></span>*pdwReqID*</span></span>
</dt> <dd>

<span data-ttu-id="ec3d9-112">Adresse einer Variablen, die die **Ausblenden** der Anforderungs-ID empfängt.</span><span class="sxs-lookup"><span data-stu-id="ec3d9-112">Address of a variable that receives the **Hide** request ID.</span></span>

</dd> </dl>

<span data-ttu-id="ec3d9-113">Der Server fügt die Animation, die der **Hide** -Methode zugeordnet ist, in die Warteschlange des Zeichens ein.</span><span class="sxs-lookup"><span data-stu-id="ec3d9-113">The server queues the animation associated with the **Hide** method in the character's queue.</span></span> <span data-ttu-id="ec3d9-114">Dies ermöglicht es Ihnen, das Zeichen nach einer Sequenz von anderen Animationen auszublenden.</span><span class="sxs-lookup"><span data-stu-id="ec3d9-114">This allows you to use it to hide the character after a sequence of other animations.</span></span> <span data-ttu-id="ec3d9-115">Sie können die Aktion sofort wiedergeben, indem Sie die Methode " [**Ende**](iagentcharacter--stop.md) " verwenden, bevor Sie die **Hide** -Methode aufrufen</span><span class="sxs-lookup"><span data-stu-id="ec3d9-115">You can play the action immediately by using the [**Stop**](iagentcharacter--stop.md) method before calling the **Hide** method.</span></span>

<span data-ttu-id="ec3d9-116">Wenn Sie das HTTP-Protokoll für den Zugriff auf Zeichen-und Animationsdaten verwenden, verwenden Sie die [**Prepare**](/windows/desktop/lwef/iagentcharacter--prepare) -Methode, um sicherzustellen, dass die **Animation zum Ausblenden des Zustands verfügbar** ist</span><span class="sxs-lookup"><span data-stu-id="ec3d9-116">When using the HTTP protocol to access character and animation data, use the [**Prepare**](/windows/desktop/lwef/iagentcharacter--prepare) method to ensure the availability of the **Hiding** state animation before calling this method.</span></span>

<span data-ttu-id="ec3d9-117">Das Ausblenden eines Zeichens kann auch dazu führen, dass das [**iagentnotifysink:: activateinputstate**](iagentnotifysink--activateinputstate.md) -Ereignis eines anderen sichtbaren Zeichens ausgelöst wird.</span><span class="sxs-lookup"><span data-stu-id="ec3d9-117">Hiding a character can also result in triggering the [**IAgentNotifySink::ActivateInputState**](iagentnotifysink--activateinputstate.md) event of another visible character.</span></span>

<span data-ttu-id="ec3d9-118">Versteckte Zeichen können nicht auf den Audiokanal zugreifen.</span><span class="sxs-lookup"><span data-stu-id="ec3d9-118">Hidden characters cannot access the audio channel.</span></span> <span data-ttu-id="ec3d9-119">Der Server übergibt einen Fehlerstatus im [**requestcomplete**](iagentnotifysink--requestcomplete.md) -Ereignis zurück, wenn Sie eine Animations Anforderung generieren und das Zeichen ausgeblendet ist.</span><span class="sxs-lookup"><span data-stu-id="ec3d9-119">The server will pass back a failure status in the [**RequestComplete**](iagentnotifysink--requestcomplete.md) event if you generate an animation request and the character is hidden.</span></span>

## <a name="see-also"></a><span data-ttu-id="ec3d9-120">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="ec3d9-120">See Also</span></span>

[<span data-ttu-id="ec3d9-121">**Iagentcharacter:: Show**</span><span class="sxs-lookup"><span data-stu-id="ec3d9-121">**IAgentCharacter::Show**</span></span>](iagentcharacter--show.md)


 

 