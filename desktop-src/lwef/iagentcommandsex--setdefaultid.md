---
title: Iagentcommandsex setdefaultid
description: Iagentcommandsex setdefaultid
ms.assetid: 056ec518-bf0b-403f-adc6-9b53b0c044a7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37754eb61df7879511a03dde705936d36f905376
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104390219"
---
# <a name="iagentcommandsexsetdefaultid"></a><span data-ttu-id="90263-103">Iagentcommandsex:: setdefaultid</span><span class="sxs-lookup"><span data-stu-id="90263-103">IAgentCommandsEx::SetDefaultID</span></span>

<span data-ttu-id="90263-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="90263-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT SetDefaultID(
   long dwID,  // default command's ID
);
```

<span data-ttu-id="90263-105">Legt die ID des Standard Befehls in einer [**Commands**](/windows/desktop/lwef/the-commands-collection-object) -Auflistung fest.</span><span class="sxs-lookup"><span data-stu-id="90263-105">Sets the ID of the default command in a [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection.</span></span>

-   <span data-ttu-id="90263-106">Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="90263-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="90263-107"><span id="dwID"></span><span id="dwid"></span><span id="DWID"></span>*dwID*</span><span class="sxs-lookup"><span data-stu-id="90263-107"><span id="dwID"></span><span id="dwid"></span><span id="DWID"></span>*dwID*</span></span>
</dt> <dd>

<span data-ttu-id="90263-108">Die ID für den [**Befehl**](/windows/desktop/lwef/the-command-object) , der als Standard festgelegt werden soll.</span><span class="sxs-lookup"><span data-stu-id="90263-108">The ID for the [**Command**](/windows/desktop/lwef/the-command-object) to be set as the default.</span></span>

</dd> </dl>

<span data-ttu-id="90263-109">Diese Eigenschaft legt das Standard [**Befehls**](/windows/desktop/lwef/the-command-object) Objekt fest, das in der [**Commands**](/windows/desktop/lwef/the-commands-collection-object) -Auflistung festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="90263-109">This property sets the default [**Command**](/windows/desktop/lwef/the-command-object) object set in your [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection.</span></span> <span data-ttu-id="90263-110">Der Standardbefehl ist im Popupmenü des Zeichens fett formatiert.</span><span class="sxs-lookup"><span data-stu-id="90263-110">The default command is bold in the character's pop-up menu.</span></span> <span data-ttu-id="90263-111">Wenn Sie jedoch den Standardbefehl festlegen, werden die Befehle zur Behandlung von Befehlen oder zum Doppelklicken nicht tatsächlich geändert.</span><span class="sxs-lookup"><span data-stu-id="90263-111">However, setting the default command does not actually change command handling or double-click events.</span></span>

<span data-ttu-id="90263-112">Diese Eigenschaft gilt nur für die Verwendung des Zeichens durch die Client Anwendung. Diese Einstellung wirkt sich nicht auf andere Clients des Zeichens oder andere Zeichen ihrer Client Anwendung aus.</span><span class="sxs-lookup"><span data-stu-id="90263-112">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

## <a name="see-also"></a><span data-ttu-id="90263-113">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="90263-113">See Also</span></span>

[<span data-ttu-id="90263-114">**Iagentcommandsex:: getdefaultid**</span><span class="sxs-lookup"><span data-stu-id="90263-114">**IAgentCommandsEx::GetDefaultID**</span></span>](iagentcommandsex--getdefaultid.md)


 

 