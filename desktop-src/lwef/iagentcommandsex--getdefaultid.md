---
title: Iagentcommandsex getdefaultid
description: Iagentcommandsex getdefaultid
ms.assetid: 14079ae0-ad2c-4f38-9371-9914f8402e49
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e4380eca62a65758979a94fb23511348b11acdf
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104390316"
---
# <a name="iagentcommandsexgetdefaultid"></a><span data-ttu-id="e18f5-103">Iagentcommandsex:: getdefaultid</span><span class="sxs-lookup"><span data-stu-id="e18f5-103">IAgentCommandsEx::GetDefaultID</span></span>

<span data-ttu-id="e18f5-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="e18f5-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetDefaultID(
   long * pdwID  // address of default command's ID
);
```

<span data-ttu-id="e18f5-105">Ruft die ID des Standard Befehls in einer [**Commands**](/windows/desktop/lwef/the-commands-collection-object) -Auflistung ab.</span><span class="sxs-lookup"><span data-stu-id="e18f5-105">Retrieves the ID of the default command in a [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection.</span></span>

-   <span data-ttu-id="e18f5-106">Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="e18f5-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="e18f5-107"><span id="pdwID"></span><span id="pdwid"></span><span id="PDWID"></span>*pdwid*</span><span class="sxs-lookup"><span data-stu-id="e18f5-107"><span id="pdwID"></span><span id="pdwid"></span><span id="PDWID"></span>*pdwID*</span></span>
</dt> <dd>

<span data-ttu-id="e18f5-108">Adresse einer Variablen, die die ID des [**Befehls**](/windows/desktop/lwef/the-command-object) Satzes als Standardwert empfängt.</span><span class="sxs-lookup"><span data-stu-id="e18f5-108">Address of a variable that receives the ID of the [**Command**](/windows/desktop/lwef/the-command-object) set as the default.</span></span>

</dd> </dl>

<span data-ttu-id="e18f5-109">Diese Eigenschaft gibt das aktuelle Standard [**Befehls**](/windows/desktop/lwef/the-command-object) Objekt in der [**Commands**](/windows/desktop/lwef/the-commands-collection-object) -Auflistung zurück.</span><span class="sxs-lookup"><span data-stu-id="e18f5-109">This property returns the current default [**Command**](/windows/desktop/lwef/the-command-object) object in your [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection.</span></span> <span data-ttu-id="e18f5-110">Der Standardbefehl ist im Popupmenü des Zeichens fett formatiert.</span><span class="sxs-lookup"><span data-stu-id="e18f5-110">The default command is bold in the character's pop-up menu.</span></span> <span data-ttu-id="e18f5-111">Wenn Sie jedoch den Standardbefehl festlegen, werden die Befehle zur Behandlung von Befehlen oder zum Doppelklicken nicht geändert.</span><span class="sxs-lookup"><span data-stu-id="e18f5-111">However, setting the default command does not change command handling or double-click events.</span></span>

<span data-ttu-id="e18f5-112">Diese Eigenschaft gilt nur für die Verwendung des Zeichens durch die Client Anwendung. Diese Einstellung wirkt sich nicht auf andere Clients des Zeichens oder andere Zeichen ihrer Client Anwendung aus.</span><span class="sxs-lookup"><span data-stu-id="e18f5-112">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

## <a name="see-also"></a><span data-ttu-id="e18f5-113">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="e18f5-113">See Also</span></span>

[<span data-ttu-id="e18f5-114">**Iagentcommandsex:: setdefaultid**</span><span class="sxs-lookup"><span data-stu-id="e18f5-114">**IAgentCommandsEx::SetDefaultID**</span></span>](iagentcommandsex--setdefaultid.md)


 

 