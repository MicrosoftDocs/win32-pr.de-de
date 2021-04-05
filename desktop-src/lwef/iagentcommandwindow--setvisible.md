---
title: Iagentcommandwindow setVisible
description: Iagentcommandwindow setVisible
ms.assetid: 44f3fc2d-937a-4890-8dad-e0f29da4c6b5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a43ddff54f4869cbe36016f30d775eeea017ae6c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037158"
---
# <a name="iagentcommandwindowsetvisible"></a><span data-ttu-id="021ea-103">Iagentcommandwindow:: setVisible</span><span class="sxs-lookup"><span data-stu-id="021ea-103">IAgentCommandWindow::SetVisible</span></span>

<span data-ttu-id="021ea-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="021ea-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT SetVisible(
   long bVisible  // Voice Commands Window Visible setting 
);
```

<span data-ttu-id="021ea-105">Legen Sie die [**Visible**](visible-property.md) -Eigenschaft für das Fenster "Sprachbefehle" fest.</span><span class="sxs-lookup"><span data-stu-id="021ea-105">Set the [**Visible**](visible-property.md) property for the Voice Commands Window.</span></span>

-   <span data-ttu-id="021ea-106">Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="021ea-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="021ea-107"><span id="bVisible"></span><span id="bvisible"></span><span id="BVISIBLE"></span>*bvisible*</span><span class="sxs-lookup"><span data-stu-id="021ea-107"><span id="bVisible"></span><span id="bvisible"></span><span id="BVISIBLE"></span>*bVisible*</span></span>
</dt> <dd>

<span data-ttu-id="021ea-108">[**Sichtbare**](visible-property.md) Eigenschafts Einstellung.</span><span class="sxs-lookup"><span data-stu-id="021ea-108">[**Visible**](visible-property.md) property setting.</span></span> <span data-ttu-id="021ea-109">Der Wert **true** zeigt das Fenster Sprachbefehle an. **False** blendet es aus.</span><span class="sxs-lookup"><span data-stu-id="021ea-109">A value of **True** displays the Voice Commands Window; **False** hides it.</span></span>

</dd> </dl>

<span data-ttu-id="021ea-110">Der Benutzer kann diese Eigenschaft überschreiben.</span><span class="sxs-lookup"><span data-stu-id="021ea-110">The user can override this property.</span></span>

## <a name="see-also"></a><span data-ttu-id="021ea-111">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="021ea-111">See Also</span></span>

[<span data-ttu-id="021ea-112">**Iagentcommandwindow:: getVisible**</span><span class="sxs-lookup"><span data-stu-id="021ea-112">**IAgentCommandWindow::GetVisible**</span></span>](iagentcommandwindow--getvisible.md)


 

 




