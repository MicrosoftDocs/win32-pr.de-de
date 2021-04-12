---
title: Iagentuserinput GetCount
description: Iagentuserinput GetCount
ms.assetid: 9c127387-b680-405a-9a62-ee08cc70813a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ac4b597f7367eff10154bde256698ef371c3619
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104206186"
---
# <a name="iagentuserinputgetcount"></a><span data-ttu-id="ed8b8-103">Iagentuserinput:: GetCount</span><span class="sxs-lookup"><span data-stu-id="ed8b8-103">IAgentUserInput::GetCount</span></span>

<span data-ttu-id="ed8b8-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="ed8b8-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetCount(
   long * pdwCount  // address of a variable for number of alternatives 
);
```

<span data-ttu-id="ed8b8-105">Ruft die Anzahl der [**Befehls**](command-event.md) Alternativen ab, die an einen [**iagentnotifysink:: Command**](iagentnotifysink--command.md) -Rückruf übermittelt werden.</span><span class="sxs-lookup"><span data-stu-id="ed8b8-105">Retrieves the number of [**Command**](command-event.md) alternatives passed to an [**IAgentNotifySink::Command**](iagentnotifysink--command.md) callback.</span></span>

-   <span data-ttu-id="ed8b8-106">Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="ed8b8-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="ed8b8-107"><span id="pdwCount"></span><span id="pdwcount"></span><span id="PDWCOUNT"></span>*pdwCount*</span><span class="sxs-lookup"><span data-stu-id="ed8b8-107"><span id="pdwCount"></span><span id="pdwcount"></span><span id="PDWCOUNT"></span>*pdwCount*</span></span>
</dt> <dd>

<span data-ttu-id="ed8b8-108">Adresse einer Variablen, die die Anzahl der vom Server identifizierten [**Befehle**](command-event.md) empfängt.</span><span class="sxs-lookup"><span data-stu-id="ed8b8-108">Address of a variable that receives the count of [**Commands**](command-event.md) alternatives identified by the server.</span></span>

</dd> </dl>

<span data-ttu-id="ed8b8-109">Wenn die Spracheingabe nicht die Quelle für den Befehl war, z. b. wenn der Benutzer den Befehl aus dem Popupmenü des Zeichens ausgewählt hat, gibt **GetCount** den Wert 1 zurück.</span><span class="sxs-lookup"><span data-stu-id="ed8b8-109">If voice input was not the source for the command, for example, if the user selected the command from the character's pop-up menu, **GetCount** returns 1.</span></span> <span data-ttu-id="ed8b8-110">Wenn **GetCount** NULL (0) zurückgibt, hat die Spracherkennungs-Engine gesprochene Eingaben erkannt, aber festgestellt, dass es keinen übereinstimmenden Befehl gab.</span><span class="sxs-lookup"><span data-stu-id="ed8b8-110">If **GetCount** returns zero (0), the speech recognition engine detected spoken input but determined that there was no matching command.</span></span>

 

 




