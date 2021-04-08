---
title: Iagentcharacter abspielen
description: Iagentcharacter abspielen
ms.assetid: a0158693-ff62-4da4-8b68-402e8d5b1c2a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 996929271156254377f08b9fc41da3932aee9da4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037650"
---
# <a name="iagentcharacterplay"></a><span data-ttu-id="571aa-103">Iagentcharacter::P Lay</span><span class="sxs-lookup"><span data-stu-id="571aa-103">IAgentCharacter::Play</span></span>

<span data-ttu-id="571aa-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="571aa-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT Play(
   BSTR bszAnimation,  // name of an animation
   long * pdwReqID     // address of request ID
);
```

<span data-ttu-id="571aa-105">Gibt die angegebene Animation wieder.</span><span class="sxs-lookup"><span data-stu-id="571aa-105">Plays the specified animation.</span></span>

-   <span data-ttu-id="571aa-106">Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="571aa-106">Returns S\_OK to indicate the operation was successful.</span></span> <span data-ttu-id="571aa-107">Wenn die Funktion zurückgibt, enthält *pdwreqid* die ID der Anforderung.</span><span class="sxs-lookup"><span data-stu-id="571aa-107">When the function returns, *pdwReqID* contains the ID of the request.</span></span>

<dl> <dt>

<span data-ttu-id="571aa-108"><span id="bszAnimation"></span><span id="bszanimation"></span><span id="BSZANIMATION"></span>*bszanimation*</span><span class="sxs-lookup"><span data-stu-id="571aa-108"><span id="bszAnimation"></span><span id="bszanimation"></span><span id="BSZANIMATION"></span>*bszAnimation*</span></span>
</dt> <dd>

<span data-ttu-id="571aa-109">Der Name einer Animation.</span><span class="sxs-lookup"><span data-stu-id="571aa-109">The name of an animation.</span></span>

</dd> <dt>

<span data-ttu-id="571aa-110"><span id="pdwReqID"></span><span id="pdwreqid"></span><span id="PDWREQID"></span>*pdwreqid*</span><span class="sxs-lookup"><span data-stu-id="571aa-110"><span id="pdwReqID"></span><span id="pdwreqid"></span><span id="PDWREQID"></span>*pdwReqID*</span></span>
</dt> <dd>

<span data-ttu-id="571aa-111">Adresse einer Variablen, die das **iagentcharacter-Element empfängt::P Lay** -Anforderungs-ID.</span><span class="sxs-lookup"><span data-stu-id="571aa-111">Address of a variable that receives the **IAgentCharacter::Play** request ID.</span></span>

</dd> </dl>

<span data-ttu-id="571aa-112">Der Name einer Animation wird definiert, wenn das Zeichen mit dem Microsoft-Agent-Zeichen-Editor kompiliert wird.</span><span class="sxs-lookup"><span data-stu-id="571aa-112">An animation's name is defined when the character is compiled with the Microsoft Agent Character Editor.</span></span> <span data-ttu-id="571aa-113">Vor der Wiedergabe der angegebenen Animation versucht der Server, die Rückgabe Animation für die vorherige Animation **wiederzugeben** (sofern eine zugewiesen wurde).</span><span class="sxs-lookup"><span data-stu-id="571aa-113">Before playing the specified animation, the server attempts to play the **Return** animation for the previous animation (if one has been assigned).</span></span>

<span data-ttu-id="571aa-114">Wenn die Animationsdaten eines Zeichens auf dem lokalen Computer des Benutzers gespeichert werden, können Sie die **iagentcharacter::P Lay** -Methode verwenden und den Namen der Animation angeben.</span><span class="sxs-lookup"><span data-stu-id="571aa-114">When a character's animation data is stored on the user's local machine, you can use the **IAgentCharacter::Play** method and specify the name of the animation.</span></span> <span data-ttu-id="571aa-115">Wenn Sie das HTTP-Protokoll für den Zugriff auf Animationsdaten verwenden, verwenden Sie die [**Prepare**](iagentcharacter--prepare.md) -Methode, um die Verfügbarkeit der Animation vor dem Aufrufen dieser Methode sicherzustellen.</span><span class="sxs-lookup"><span data-stu-id="571aa-115">When using the HTTP protocol to access animation data, use the [**Prepare**](iagentcharacter--prepare.md) method to ensure the availability of the animation before calling this method.</span></span>

## <a name="see-also"></a><span data-ttu-id="571aa-116">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="571aa-116">See Also</span></span>

[<span data-ttu-id="571aa-117">**Iagentcharacter::P repare**</span><span class="sxs-lookup"><span data-stu-id="571aa-117">**IAgentCharacter::Prepare**</span></span>](iagentcharacter--prepare.md)


 

 




