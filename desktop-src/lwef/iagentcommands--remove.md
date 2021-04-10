---
title: Iagentcommands entfernen
description: Iagentcommands entfernen
ms.assetid: 1f41aa2d-e50b-48a8-87fc-fda4730b035a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d0c3321de3d06b5e2ebea873a4bace91482d8c5
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104208947"
---
# <a name="iagentcommandsremove"></a><span data-ttu-id="95b92-103">Iagentcommands:: Remove</span><span class="sxs-lookup"><span data-stu-id="95b92-103">IAgentCommands::Remove</span></span>

<span data-ttu-id="95b92-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="95b92-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT Remove(
   long dwID  // Command ID
);
```

<span data-ttu-id="95b92-105">Entfernt den angegebenen [**Befehl**](/windows/desktop/lwef/the-command-object) aus einer [**Befehls**](/windows/desktop/lwef/the-commands-collection-object) Auflistung.</span><span class="sxs-lookup"><span data-stu-id="95b92-105">Removes the specified [**Command**](/windows/desktop/lwef/the-command-object) from a [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection.</span></span>

-   <span data-ttu-id="95b92-106">Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="95b92-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="95b92-107"><span id="dwID"></span><span id="dwid"></span><span id="DWID"></span>*dwID*</span><span class="sxs-lookup"><span data-stu-id="95b92-107"><span id="dwID"></span><span id="dwid"></span><span id="DWID"></span>*dwID*</span></span>
</dt> <dd>

<span data-ttu-id="95b92-108">Die ID eines [**Befehls**](/windows/desktop/lwef/the-command-object) , der aus der [**Commands**](/windows/desktop/lwef/the-commands-collection-object) -Auflistung entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="95b92-108">The ID of a [**Command**](/windows/desktop/lwef/the-command-object) to remove from the [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection.</span></span>

</dd> </dl>

<span data-ttu-id="95b92-109">Wenn Sie einen [**Befehl**](/windows/desktop/lwef/the-command-object) aus [**einer Befehls**](/windows/desktop/lwef/the-commands-collection-object) Auflistung entfernen, wird dieser auch aus dem Popupmenü und dem **Fenster "Sprachbefehle** " entfernt, wenn die Anwendung aktiv ist.</span><span class="sxs-lookup"><span data-stu-id="95b92-109">Removing a [**Command**](/windows/desktop/lwef/the-command-object) from a [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection also removes it from the pop-up menu and the **Voice Commands Window** when your application is input-active.</span></span>

## <a name="see-also"></a><span data-ttu-id="95b92-110">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="95b92-110">See Also</span></span>

<span data-ttu-id="95b92-111">[**Iagentcommands:: Add**](iagentcommands--add.md), [**iagentcommands:: Insert**](iagentcommands--insert.md), [**iagentcommands:: RemoveAll**](iagentcommands--removeall.md)</span><span class="sxs-lookup"><span data-stu-id="95b92-111">[**IAgentCommands::Add**](iagentcommands--add.md), [**IAgentCommands::Insert**](iagentcommands--insert.md), [**IAgentCommands::RemoveAll**](iagentcommands--removeall.md)</span></span>


 

 