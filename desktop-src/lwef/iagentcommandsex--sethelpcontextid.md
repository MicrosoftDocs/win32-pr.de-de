---
title: Iagentcommandsex * thelpcontextid
description: Iagentcommandsex * thelpcontextid
ms.assetid: b49d8184-f8dd-4359-9d45-3f038af18da5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14ed692185adbd60a73085b367b30b14fb646ab6
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "103725921"
---
# <a name="iagentcommandsexsethelpcontextid"></a><span data-ttu-id="e749d-103">Iagentcommandsex:: Setup Element-ID</span><span class="sxs-lookup"><span data-stu-id="e749d-103">IAgentCommandsEx::SetHelpContextID</span></span>

<span data-ttu-id="e749d-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="e749d-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT SetHelpContextID(
   long ulHelpID  // ID for help topic
);
```

<span data-ttu-id="e749d-105">Legt die [**HelpContextID**](helpcontextid-property.md) für ein [**Command**](/windows/desktop/lwef/the-command-object) -Objekt fest.</span><span class="sxs-lookup"><span data-stu-id="e749d-105">Sets the [**HelpContextID**](helpcontextid-property.md) for a [**Command**](/windows/desktop/lwef/the-command-object) object.</span></span>

-   <span data-ttu-id="e749d-106">Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="e749d-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="e749d-107"><span id="ulHelpID"></span><span id="ulhelpid"></span><span id="ULHELPID"></span>*ulhelpid*</span><span class="sxs-lookup"><span data-stu-id="e749d-107"><span id="ulHelpID"></span><span id="ulhelpid"></span><span id="ULHELPID"></span>*ulHelpID*</span></span>
</dt> <dd>

<span data-ttu-id="e749d-108">Die Kontext Nummer des Hilfe Themas, das dem [**Befehls**](/windows/desktop/lwef/the-command-object) Objekt zugeordnet ist. wird verwendet, um kontextbezogene Hilfe für den Befehl bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="e749d-108">The context number of the help topic associated with the [**Command**](/windows/desktop/lwef/the-command-object) object; used to provide context-sensitive Help for the command.</span></span>

</dd> </dl>

<span data-ttu-id="e749d-109">Wenn Sie eine Windows-Hilfedatei für Ihre Anwendung erstellt und diese in der [**HelpFile**](helpfile-property.md) -Eigenschaft des Zeichens festgelegt haben.</span><span class="sxs-lookup"><span data-stu-id="e749d-109">If you've created a Windows Help file for your application and set this in the character's [**HelpFile**](helpfile-property.md) property.</span></span> <span data-ttu-id="e749d-110">Der-Agent ruft automatisch die Hilfe auf, wenn [**helpmudeon**](helpmodeon-property.md) auf **true** festgelegt ist und der Benutzer den Befehl auswählt.</span><span class="sxs-lookup"><span data-stu-id="e749d-110">Agent automatically calls Help when [**HelpModeOn**](helpmodeon-property.md) is set to **True** and the user selects the command.</span></span> <span data-ttu-id="e749d-111">Wenn in [**HelpContextID**](helpcontextid-property.md)eine Kontext Nummer vorhanden ist, ruft der-Agent Hilfe auf und sucht nach dem Thema, das durch die aktuelle Kontext Nummer identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="e749d-111">If there is a context number in the [**HelpContextID**](helpcontextid-property.md), Agent calls Help and searches for the topic identified by the current context number.</span></span> <span data-ttu-id="e749d-112">Die aktuelle Kontext Nummer ist der Wert von **HelpContextID** für den Befehl.</span><span class="sxs-lookup"><span data-stu-id="e749d-112">The current context number is the value of **HelpContextID** for the command.</span></span> <span data-ttu-id="e749d-113">Wenn in der **HelpContextID** -Eigenschaft des ausgewählten Befehls eine Kontext Nummer vorhanden ist, wird in der Hilfe ein Thema angezeigt, das dem aktuellen Hilfe Kontext entspricht. Andernfalls wird "kein Hilfethema mit diesem Element verknüpft" angezeigt.</span><span class="sxs-lookup"><span data-stu-id="e749d-113">If there is a context number in the selected command's **HelpContextID** property, Help displays a topic corresponding to the current Help context; otherwise it displays "No Help topic associated with this item."</span></span>

<span data-ttu-id="e749d-114">Diese Eigenschaft gilt nur für die Verwendung des Zeichens durch die Client Anwendung. Diese Einstellung wirkt sich nicht auf andere Clients des Zeichens oder andere Zeichen ihrer Client Anwendung aus.</span><span class="sxs-lookup"><span data-stu-id="e749d-114">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

> [!Note]  
> <span data-ttu-id="e749d-115">Das Entwickeln einer Hilfedatei erfordert den Microsoft Windows Help Compiler.</span><span class="sxs-lookup"><span data-stu-id="e749d-115">Building a Help file requires the Microsoft Windows Help Compiler.</span></span>

 

## <a name="see-also"></a><span data-ttu-id="e749d-116">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="e749d-116">See Also</span></span>

<span data-ttu-id="e749d-117">[**Iagentcommandsex:: gethelpcontextid**](iagentcommandsex--gethelpcontextid.md), [**iagentcharakteriex::**](iagentcharacterex--sethelpmodeon.md)Setup Elementname, [**iagentcharakteriex::**](iagentcharacterex--sethelpfilename.md) Setup Name</span><span class="sxs-lookup"><span data-stu-id="e749d-117">[**IAgentCommandsEx::GetHelpContextID**](iagentcommandsex--gethelpcontextid.md), [**IAgentCharacterEx::SetHelpModeOn**](iagentcharacterex--sethelpmodeon.md), [**IAgentCharacterEx::SetHelpFileName**](iagentcharacterex--sethelpfilename.md)</span></span>


 

 