---
title: Iagentcommands RemoveAll
description: Iagentcommands RemoveAll
ms.assetid: fab43363-6325-4566-b7bb-599591f67321
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8bd374b7c5767c416d2c3bb2281e651ba71acd8
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "103727040"
---
# <a name="iagentcommandsremoveall"></a><span data-ttu-id="32240-103">Iagentcommands:: RemoveAll</span><span class="sxs-lookup"><span data-stu-id="32240-103">IAgentCommands::RemoveAll</span></span>

<span data-ttu-id="32240-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="32240-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT Remove();
```

<span data-ttu-id="32240-105">Entfernt alle [**Befehle**](/windows/desktop/lwef/the-command-object) aus einer [**Befehls**](/windows/desktop/lwef/the-commands-collection-object) Auflistung.</span><span class="sxs-lookup"><span data-stu-id="32240-105">Removes all [**Commands**](/windows/desktop/lwef/the-command-object) from a [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection.</span></span>

-   <span data-ttu-id="32240-106">Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="32240-106">Returns S\_OK to indicate the operation was successful.</span></span>

<span data-ttu-id="32240-107">Wenn Sie alle [**Befehle**](/windows/desktop/lwef/the-command-object) aus einer [**Befehls**](/windows/desktop/lwef/the-commands-collection-object) Auflistung entfernen, werden diese auch aus dem Popupmenü und dem **Fenster "Sprachbefehle** " entfernt, wenn die Anwendung aktiv ist.</span><span class="sxs-lookup"><span data-stu-id="32240-107">Removing all [**Commands**](/windows/desktop/lwef/the-command-object) from a [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection also removes them from the pop-up menu and the **Voice Commands Window** when your application is input-active.</span></span> <span data-ttu-id="32240-108">**RemoveAll** entfernt keine Server-oder andere Client Einträge.</span><span class="sxs-lookup"><span data-stu-id="32240-108">**RemoveAll** does not remove server or other client's entries.</span></span>

## <a name="see-also"></a><span data-ttu-id="32240-109">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="32240-109">See Also</span></span>

<span data-ttu-id="32240-110">[**Iagentcommands:: Add**](iagentcommands--add.md), [**iagentcommands:: Insert**](iagentcommands--insert.md), [**iagentcommands:: Remove**](iagentcommands--remove.md)</span><span class="sxs-lookup"><span data-stu-id="32240-110">[**IAgentCommands::Add**](iagentcommands--add.md), [**IAgentCommands::Insert**](iagentcommands--insert.md), [**IAgentCommands::Remove**](iagentcommands--remove.md)</span></span>


 

 