---
title: IAgentCharacter GetMoveCause
description: IAgentCharacter GetMoveCause
ms.assetid: 36cdd3bc-65b6-469f-9344-93403c1d24e0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be943cf3b25b789838215f0209b16e67d5b50659
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119684"
---
# <a name="iagentcharactergetmovecause"></a><span data-ttu-id="aa689-103">IAgentCharacter::GetMoveCause</span><span class="sxs-lookup"><span data-stu-id="aa689-103">IAgentCharacter::GetMoveCause</span></span>

<span data-ttu-id="aa689-104">\[Microsoft Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht mehr verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="aa689-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetMoveCause(
   long * pdwCause  // address of variable for cause of character move
);
```

<span data-ttu-id="aa689-105">Ruft die Ursache der letzten Bewegung des Zeichens ab.</span><span class="sxs-lookup"><span data-stu-id="aa689-105">Retrieves the cause of the character's last move.</span></span>

-   <span data-ttu-id="aa689-106">Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="aa689-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="aa689-107"><span id="pdwCause"></span><span id="pdwcause"></span><span id="PDWCAUSE"></span>*pdwCause*</span><span class="sxs-lookup"><span data-stu-id="aa689-107"><span id="pdwCause"></span><span id="pdwcause"></span><span id="PDWCAUSE"></span>*pdwCause*</span></span>
</dt> <dd>

<span data-ttu-id="aa689-108">Die Adresse einer Variablen, die die Ursache für die letzte Bewegung des Zeichens empfängt und eine der folgenden Variablen ist:</span><span class="sxs-lookup"><span data-stu-id="aa689-108">Address of a variable that receives the cause of the character's last move and will be one of the following:</span></span>



| <span data-ttu-id="aa689-109">Wert</span><span class="sxs-lookup"><span data-stu-id="aa689-109">Value</span></span>                                                               | <span data-ttu-id="aa689-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="aa689-110">Description</span></span>                                                                                     |
|----------------------------------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="aa689-111">**const unsigned short** **NeverMoved = 0;**</span><span class="sxs-lookup"><span data-stu-id="aa689-111">**const unsigned short** **NeverMoved = 0;**</span></span><br/>        | <span data-ttu-id="aa689-112">Das Zeichen wurde nicht verschoben.</span><span class="sxs-lookup"><span data-stu-id="aa689-112">Character has not been moved.</span></span>                                                        |
| <span data-ttu-id="aa689-113">**const unsigned short** **UserMoved = 1;**</span><span class="sxs-lookup"><span data-stu-id="aa689-113">**const unsigned short** **UserMoved = 1;**</span></span><br/>         | <span data-ttu-id="aa689-114">Der Benutzer hat das Zeichen gezogen.</span><span class="sxs-lookup"><span data-stu-id="aa689-114">User dragged the character.</span></span>                                                          |
| <span data-ttu-id="aa689-115">**const unsigned short** **ProgramMoved = 2;**</span><span class="sxs-lookup"><span data-stu-id="aa689-115">**const unsigned short** **ProgramMoved = 2;**</span></span><br/>      | <span data-ttu-id="aa689-116">Die Anwendung hat das Zeichen verschoben.</span><span class="sxs-lookup"><span data-stu-id="aa689-116">Your application moved the character.</span></span>                                                |
| <span data-ttu-id="aa689-117">**const unsigned short** **OtherProgramMoved = 3;**</span><span class="sxs-lookup"><span data-stu-id="aa689-117">**const unsigned short** **OtherProgramMoved = 3;**</span></span><br/> | <span data-ttu-id="aa689-118">Das Zeichen wurde von einer anderen Anwendung verschoben.</span><span class="sxs-lookup"><span data-stu-id="aa689-118">Another application moved the character.</span></span>                                             |
| <span data-ttu-id="aa689-119">**const unsigned short** **SystemMoved = 4**</span><span class="sxs-lookup"><span data-stu-id="aa689-119">**const unsigned short** **SystemMoved = 4**</span></span><br/>        | <span data-ttu-id="aa689-120">Der Server hat das Zeichen verschoben, um es nach einer Änderung der Bildschirmauflösung auf dem Bildschirm zu halten.</span><span class="sxs-lookup"><span data-stu-id="aa689-120">The server moved the character to keep it onscreen after a screen resolution change.</span></span> |



 

</dd> </dl>

## <a name="see-also"></a><span data-ttu-id="aa689-121">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="aa689-121">See Also</span></span>

[<span data-ttu-id="aa689-122">**IAgentNotifySink::Move**</span><span class="sxs-lookup"><span data-stu-id="aa689-122">**IAgentNotifySink::Move**</span></span>](iagentnotifysink--move.md)


 

 





