---
title: Iagentcharakteriex "einhalbpcontextid"
description: Iagentcharakteriex "einhalbpcontextid"
ms.assetid: 218e970e-825e-441d-8947-30ec6a2845bd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 500187bf04babbecf7577ff933dd0adcc53609f4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103708963"
---
# <a name="iagentcharacterexsethelpcontextid"></a><span data-ttu-id="88ee3-103">Iagentcharakteriex:: Setup Element-ID</span><span class="sxs-lookup"><span data-stu-id="88ee3-103">IAgentCharacterEx::SetHelpContextID</span></span>

<span data-ttu-id="88ee3-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="88ee3-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT SetHelpContextID(
   long ulHelpID  // ID for help topic
);
```

<span data-ttu-id="88ee3-105">Legt die [**HelpContextID**](helpcontextid-property.md) für das Zeichen fest.</span><span class="sxs-lookup"><span data-stu-id="88ee3-105">Sets the [**HelpContextID**](helpcontextid-property.md) for the character.</span></span>

-   <span data-ttu-id="88ee3-106">Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="88ee3-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="88ee3-107"><span id="ulHelpID"></span><span id="ulhelpid"></span><span id="ULHELPID"></span>*ulhelpid*</span><span class="sxs-lookup"><span data-stu-id="88ee3-107"><span id="ulHelpID"></span><span id="ulhelpid"></span><span id="ULHELPID"></span>*ulHelpID*</span></span>
</dt> <dd>

<span data-ttu-id="88ee3-108">Die Kontext Nummer des Hilfe Themas, das einem Zeichen zugeordnet ist. wird verwendet, um die kontextbezogene Hilfe für das Zeichen bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="88ee3-108">The context number of the help topic for associated with a character; used to provide context-sensitive Help for the character.</span></span>

</dd> </dl>

<span data-ttu-id="88ee3-109">Wenn Sie eine Windows-Hilfedatei für Ihre Anwendung erstellt und diese in der [**HelpFile**](helpfile-property.md) -Eigenschaft des Zeichens festgelegt haben, ruft der Microsoft-Agent automatisch Hilfe auf, wenn [**helpmadeon**](helpmodeon-property.md) auf **true** festgelegt ist und der Benutzer das Zeichen auswählt.</span><span class="sxs-lookup"><span data-stu-id="88ee3-109">If you've created a Windows Help file for your application and set this in the character's [**HelpFile**](helpfile-property.md) property, Microsoft Agent automatically calls Help when [**HelpModeOn**](helpmodeon-property.md) is set to **True** and the user selects the character.</span></span> <span data-ttu-id="88ee3-110">Wenn in [**HelpContextID**](helpcontextid-property.md)eine Kontext Nummer vorhanden ist, ruft der-Agent Hilfe auf und sucht nach dem Thema, das durch die aktuelle Kontext Nummer identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="88ee3-110">If there is a context number in the [**HelpContextID**](helpcontextid-property.md), Agent calls Help and searches for the topic identified by the current context number.</span></span> <span data-ttu-id="88ee3-111">Die aktuelle Kontext Nummer ist der Wert von **HelpContextID** für das Zeichen.</span><span class="sxs-lookup"><span data-stu-id="88ee3-111">The current context number is the value of **HelpContextID** for the character.</span></span> <span data-ttu-id="88ee3-112">Wenn in der **HelpContextID** -Eigenschaft eine Kontext Nummer vorhanden ist, wird in der Hilfe ein Thema angezeigt, das dem aktuellen Hilfe Kontext entspricht. Andernfalls wird "kein Hilfethema mit diesem Element verknüpft" angezeigt.</span><span class="sxs-lookup"><span data-stu-id="88ee3-112">If there is a context number in the **HelpContextID** property, Help displays a topic corresponding to the current Help context; otherwise it displays "No Help topic associated with this item."</span></span>

<span data-ttu-id="88ee3-113">Diese Einstellung gilt nur, wenn die Client Anwendung der aktive Client des obersten Zeichens ist.</span><span class="sxs-lookup"><span data-stu-id="88ee3-113">This setting applies only when your client application is the active client of the topmost character.</span></span> <span data-ttu-id="88ee3-114">Es wirkt sich nicht auf andere Clients des Zeichens oder anderer Zeichen aus, die von der Client Anwendung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="88ee3-114">It does not affect other clients of the character or other characters that your client application is using.</span></span>

> [!Note]  
> <span data-ttu-id="88ee3-115">Das Entwickeln einer Hilfedatei erfordert den Microsoft Windows Help Compiler.</span><span class="sxs-lookup"><span data-stu-id="88ee3-115">Building a Help file requires the Microsoft Windows Help Compiler.</span></span>

 

## <a name="see-also"></a><span data-ttu-id="88ee3-116">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="88ee3-116">See Also</span></span>

<span data-ttu-id="88ee3-117">[**Iagentcharakteriex:: gethelpcontextid**](iagentcharacterex--gethelpcontextid.md), [**iagentcharakteriex::**](iagentcharacterex--sethelpmodeon.md)Setup Elementname, iagentcharakteriex: [**:**](iagentcharacterex--sethelpfilename.md) Setup Name</span><span class="sxs-lookup"><span data-stu-id="88ee3-117">[**IAgentCharacterEx::GetHelpContextID**](iagentcharacterex--gethelpcontextid.md), [**IAgentCharacterEx::SetHelpModeOn**](iagentcharacterex--sethelpmodeon.md), [**IAgentCharacterEx::SetHelpFileName**](iagentcharacterex--sethelpfilename.md)</span></span>


 

 




