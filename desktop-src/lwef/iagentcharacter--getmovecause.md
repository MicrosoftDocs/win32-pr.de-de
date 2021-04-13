---
title: Iagentcharacter getmuvecause
description: Iagentcharacter getmuvecause
ms.assetid: 36cdd3bc-65b6-469f-9344-93403c1d24e0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 612fcbfd4470d17e2365373458a8ded899a8180a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388813"
---
# <a name="iagentcharactergetmovecause"></a><span data-ttu-id="01925-103">Iagentcharacter:: getmuvecause</span><span class="sxs-lookup"><span data-stu-id="01925-103">IAgentCharacter::GetMoveCause</span></span>

<span data-ttu-id="01925-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="01925-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetMoveCause(
   long * pdwCause  // address of variable for cause of character move
);
```

<span data-ttu-id="01925-105">Ruft die Ursache für den letzten Verschiebe Vorgang des Zeichens ab.</span><span class="sxs-lookup"><span data-stu-id="01925-105">Retrieves the cause of the character's last move.</span></span>

-   <span data-ttu-id="01925-106">Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="01925-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="01925-107"><span id="pdwCause"></span><span id="pdwcause"></span><span id="PDWCAUSE"></span>*pdwcause*</span><span class="sxs-lookup"><span data-stu-id="01925-107"><span id="pdwCause"></span><span id="pdwcause"></span><span id="PDWCAUSE"></span>*pdwCause*</span></span>
</dt> <dd>

<span data-ttu-id="01925-108">Adresse einer Variablen, die die Ursache des letzten Verschiebens des Zeichens empfängt und eine der folgenden ist:</span><span class="sxs-lookup"><span data-stu-id="01925-108">Address of a variable that receives the cause of the character's last move and will be one of the following:</span></span>



|                                                                |                                                                                      |
|----------------------------------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="01925-109">Konstante **Ganzzahl ohne Vorzeichen Short neververschost** **= 0;**</span><span class="sxs-lookup"><span data-stu-id="01925-109">**const unsigned short** **NeverMoved = 0;**</span></span><br/>        | <span data-ttu-id="01925-110">Das Zeichen wurde nicht verschoben.</span><span class="sxs-lookup"><span data-stu-id="01925-110">Character has not been moved.</span></span>                                                        |
| <span data-ttu-id="01925-111">" **Ganzzahl ohne Vorzeichen Short userverschost** " **= 1;**</span><span class="sxs-lookup"><span data-stu-id="01925-111">**const unsigned short** **UserMoved = 1;**</span></span><br/>         | <span data-ttu-id="01925-112">Der Benutzer hat das Zeichen gezogen.</span><span class="sxs-lookup"><span data-stu-id="01925-112">User dragged the character.</span></span>                                                          |
| <span data-ttu-id="01925-113">" **Ganzzahl ohne Vorzeichen Short Program verschost** " **= 2;**</span><span class="sxs-lookup"><span data-stu-id="01925-113">**const unsigned short** **ProgramMoved = 2;**</span></span><br/>      | <span data-ttu-id="01925-114">Die Anwendung hat das Zeichen verschoben.</span><span class="sxs-lookup"><span data-stu-id="01925-114">Your application moved the character.</span></span>                                                |
| <span data-ttu-id="01925-115">Konstante **Ganzzahl ohne Vorzeichen Short** **otherprogrambewegt = 3;**</span><span class="sxs-lookup"><span data-stu-id="01925-115">**const unsigned short** **OtherProgramMoved = 3;**</span></span><br/> | <span data-ttu-id="01925-116">Das Zeichen wurde von einer anderen Anwendung verschoben.</span><span class="sxs-lookup"><span data-stu-id="01925-116">Another application moved the character.</span></span>                                             |
| <span data-ttu-id="01925-117">**Ganzzahl ohne Vorzeichen Short** **systemverschost = 4**</span><span class="sxs-lookup"><span data-stu-id="01925-117">**const unsigned short** **SystemMoved = 4**</span></span><br/>        | <span data-ttu-id="01925-118">Der Server hat das Zeichen verschoben, um es nach einer Änderung der Bildschirmauflösung auf dem Bildschirm aufzubewahren.</span><span class="sxs-lookup"><span data-stu-id="01925-118">The server moved the character to keep it onscreen after a screen resolution change.</span></span> |



 

</dd> </dl>

## <a name="see-also"></a><span data-ttu-id="01925-119">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="01925-119">See Also</span></span>

[<span data-ttu-id="01925-120">**Iagentnotifysink:: Move**</span><span class="sxs-lookup"><span data-stu-id="01925-120">**IAgentNotifySink::Move**</span></span>](iagentnotifysink--move.md)


 

 





