---
title: Iagentcharakteriex gethelpfilename
description: Iagentcharakteriex gethelpfilename
ms.assetid: 52d5a874-ad3e-4833-9e3e-ff485414c54c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d692de5704f88d14e32231a7d63fc80150f1481a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947917"
---
# <a name="iagentcharacterexgethelpfilename"></a><span data-ttu-id="c8a0a-103">Iagentcharakteriex:: gethelpfilename</span><span class="sxs-lookup"><span data-stu-id="c8a0a-103">IAgentCharacterEx::GetHelpFileName</span></span>

<span data-ttu-id="c8a0a-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="c8a0a-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetHelpFileName(
   BSTR * pbszName  // address of Help filename
);
```

<span data-ttu-id="c8a0a-105">Ruft helpfilename für ein Zeichen ab.</span><span class="sxs-lookup"><span data-stu-id="c8a0a-105">Retrieves the HelpFileName for a character.</span></span>

-   <span data-ttu-id="c8a0a-106">Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="c8a0a-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="c8a0a-107"><span id="pbszName"></span><span id="pbszname"></span><span id="PBSZNAME"></span>*pbszname*</span><span class="sxs-lookup"><span data-stu-id="c8a0a-107"><span id="pbszName"></span><span id="pbszname"></span><span id="PBSZNAME"></span>*pbszName*</span></span>
</dt> <dd>

<span data-ttu-id="c8a0a-108">Adresse einer Variablen, die den Hilfe Dateinamen für das Zeichen empfängt.</span><span class="sxs-lookup"><span data-stu-id="c8a0a-108">Address of a variable that receives the Help filename for the character.</span></span>

</dd> </dl>

<span data-ttu-id="c8a0a-109">Wenn Sie eine Windows-Hilfedatei für Ihre Anwendung erstellt und die [**HelpFile**](helpfile-property.md) -Eigenschaft des Zeichens festgelegt haben, ruft der Microsoft-Agent automatisch Hilfe auf, wenn [**helpmadeon**](helpmodeon-property.md) auf **true** festgelegt ist und der Benutzer auf das Zeichen klickt oder einen Befehl aus dem Popupmenü auswählt.</span><span class="sxs-lookup"><span data-stu-id="c8a0a-109">If you've created a Windows Help file for your application and set the character's [**HelpFile**](helpfile-property.md) property, Microsoft Agent automatically calls Help when [**HelpModeOn**](helpmodeon-property.md) is set to **True** and the user clicks the character or selects a command from its pop-up menu.</span></span> <span data-ttu-id="c8a0a-110">Wenn in der [**HelpContextID**](helpcontextid-property.md) -Eigenschaft des ausgewählten Befehls eine Kontext Nummer vorhanden ist, wird in der Hilfe ein Thema angezeigt, das dem aktuellen Hilfe Kontext entspricht. Andernfalls wird "kein Hilfethema mit diesem Element verknüpft" angezeigt.</span><span class="sxs-lookup"><span data-stu-id="c8a0a-110">If there is a context number in the selected command's [**HelpContextID**](helpcontextid-property.md) property, Help displays a topic corresponding to the current Help context; otherwise it displays "No Help topic associated with this item."</span></span>

<span data-ttu-id="c8a0a-111">Diese Eigenschaft gilt nur für die Verwendung des Zeichens durch die Client Anwendung. Diese Einstellung wirkt sich nicht auf andere Clients des Zeichens oder andere Zeichen ihrer Client Anwendung aus.</span><span class="sxs-lookup"><span data-stu-id="c8a0a-111">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

> [!Note]  
> <span data-ttu-id="c8a0a-112">Das Entwickeln einer Hilfedatei erfordert den Microsoft Windows Help Compiler.</span><span class="sxs-lookup"><span data-stu-id="c8a0a-112">Building a Help file requires the Microsoft Windows Help Compiler.</span></span>

 

## <a name="see-also"></a><span data-ttu-id="c8a0a-113">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="c8a0a-113">See Also</span></span>

<span data-ttu-id="c8a0a-114">[**Iagentcommandsex::**](iagentcommandsex--sethelpcontextid.md)Setup Elementname, [**iagentcharakteriex::**](iagentcharacterex--sethelpmodeon.md)Setup Elementname, [**iagentcharakteriex::**](iagentcharacterex--sethelpfilename.md) Setup Name</span><span class="sxs-lookup"><span data-stu-id="c8a0a-114">[**IAgentCommandsEx::SetHelpContextID**](iagentcommandsex--sethelpcontextid.md), [**IAgentCharacterEx::SetHelpModeOn**](iagentcharacterex--sethelpmodeon.md), [**IAgentCharacterEx::SetHelpFileName**](iagentcharacterex--sethelpfilename.md)</span></span>


 

 




