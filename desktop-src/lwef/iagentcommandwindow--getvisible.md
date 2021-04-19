---
title: Iagentcommandwindow getVisible
description: Iagentcommandwindow getVisible
ms.assetid: a69a2aaa-5a3a-46b8-b505-49609a2aa5ba
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c66c6d7bf2ee59512f478fd8daa7cee882515690
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106341648"
---
# <a name="iagentcommandwindowgetvisible"></a><span data-ttu-id="2caef-103">Iagentcommandwindow:: getVisible</span><span class="sxs-lookup"><span data-stu-id="2caef-103">IAgentCommandWindow::GetVisible</span></span>

<span data-ttu-id="2caef-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="2caef-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetVisible(
   long * pbVisible  // address of variable for Visible setting for 
);                   // Voice Commands Window
```

<span data-ttu-id="2caef-105">Bestimmt, ob das Sprachbefehle Fenster sichtbar oder ausgeblendet ist.</span><span class="sxs-lookup"><span data-stu-id="2caef-105">Determines whether the Voice Commands Window is visible or hidden.</span></span>

-   <span data-ttu-id="2caef-106">Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="2caef-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="2caef-107"><span id="pbVisible"></span><span id="pbvisible"></span><span id="PBVISIBLE"></span>*pbvisible*</span><span class="sxs-lookup"><span data-stu-id="2caef-107"><span id="pbVisible"></span><span id="pbvisible"></span><span id="PBVISIBLE"></span>*pbVisible*</span></span>
</dt> <dd>

<span data-ttu-id="2caef-108">Adresse einer Variablen, die **true** erhält, wenn das Sprachbefehle Fenster sichtbar ist, oder **false** , wenn Sie ausgeblendet ist.</span><span class="sxs-lookup"><span data-stu-id="2caef-108">Address of a variable that receives **True** if the Voice Commands Window is visible, or **False** if hidden.</span></span>

</dd> </dl>

## <a name="see-also"></a><span data-ttu-id="2caef-109">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="2caef-109">See Also</span></span>

[<span data-ttu-id="2caef-110">**Iagentcommandwindow:: setVisible**</span><span class="sxs-lookup"><span data-stu-id="2caef-110">**IAgentCommandWindow::SetVisible**</span></span>](iagentcommandwindow--setvisible.md)


 

 




