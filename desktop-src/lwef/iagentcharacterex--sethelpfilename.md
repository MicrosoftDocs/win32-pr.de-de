---
title: Iagentcharakteriex "Einstellungs Name"
description: Iagentcharakteriex "Einstellungs Name"
ms.assetid: 1f8d2bd7-5821-46c0-b371-7ecbc526df72
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1342baecc1e059d4fcb5d1323c0c714bd6bf7087
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104100711"
---
# <a name="iagentcharacterexsethelpfilename"></a><span data-ttu-id="b08e9-103">Iagentcharakteriex:: Setup Name</span><span class="sxs-lookup"><span data-stu-id="b08e9-103">IAgentCharacterEx::SetHelpFileName</span></span>

<span data-ttu-id="b08e9-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="b08e9-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT SetHelpFileName(
   BSTR bszName  // Help filename
);
```

<span data-ttu-id="b08e9-105">Legt den helpfilename für ein Zeichen fest.</span><span class="sxs-lookup"><span data-stu-id="b08e9-105">Sets the HelpFileName for a character.</span></span>

-   <span data-ttu-id="b08e9-106">Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="b08e9-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="b08e9-107"><span id="bszName"></span><span id="bszname"></span><span id="BSZNAME"></span>*bszname*</span><span class="sxs-lookup"><span data-stu-id="b08e9-107"><span id="bszName"></span><span id="bszname"></span><span id="BSZNAME"></span>*bszName*</span></span>
</dt> <dd>

<span data-ttu-id="b08e9-108">Der Hilfe Dateiname für das Zeichen.</span><span class="sxs-lookup"><span data-stu-id="b08e9-108">The Help filename for the character.</span></span>

</dd> </dl>

<span data-ttu-id="b08e9-109">Wenn Sie eine Windows-Hilfedatei für Ihre Anwendung erstellt und die [**HelpFile**](helpfile-property.md) -Eigenschaft des Zeichens festgelegt haben, ruft der Microsoft-Agent automatisch Hilfe auf, wenn [**helpmadeon**](helpmodeon-property.md) auf **true** festgelegt ist und der Benutzer auf das Zeichen klickt oder einen Befehl aus dem Popupmenü auswählt.</span><span class="sxs-lookup"><span data-stu-id="b08e9-109">If you've created a Windows Help file for your application and set the character's [**HelpFile**](helpfile-property.md) property, Microsoft Agent automatically calls Help when [**HelpModeOn**](helpmodeon-property.md) is set to **True** and the user clicks the character or selects a command from its pop-up menu.</span></span> <span data-ttu-id="b08e9-110">Wenn in der [**HelpContextID**](helpcontextid-property.md) -Eigenschaft des ausgewählten Befehls eine Kontext Nummer vorhanden ist, wird in der Hilfe ein Thema angezeigt, das dem aktuellen Hilfe Kontext entspricht. Andernfalls wird "kein Hilfethema mit diesem Element verknüpft" angezeigt.</span><span class="sxs-lookup"><span data-stu-id="b08e9-110">If there is a context number in the [**HelpContextID**](helpcontextid-property.md) property of the selected command, Help displays a topic corresponding to the current Help context; otherwise it displays "No Help topic associated with this item."</span></span>

<span data-ttu-id="b08e9-111">Diese Eigenschaft gilt nur für die Verwendung des Zeichens durch die Client Anwendung. Diese Einstellung wirkt sich nicht auf andere Clients des Zeichens oder andere Zeichen ihrer Client Anwendung aus.</span><span class="sxs-lookup"><span data-stu-id="b08e9-111">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

> [!Note]  
> <span data-ttu-id="b08e9-112">Das Entwickeln einer Hilfedatei erfordert den Microsoft Windows Help Compiler.</span><span class="sxs-lookup"><span data-stu-id="b08e9-112">Building a Help file requires the Microsoft Windows Help Compiler.</span></span>

 

## <a name="see-also"></a><span data-ttu-id="b08e9-113">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="b08e9-113">See Also</span></span>

<span data-ttu-id="b08e9-114">[**Iagentcommandsex::**](iagentcommandsex--sethelpcontextid.md)Setup Elementname, [**iagentcharakteriex::**](iagentcharacterex--sethelpmodeon.md)Setup Elementname, [**iagentcharakteriex:: gethelpfilename**](iagentcharacterex--gethelpfilename.md)</span><span class="sxs-lookup"><span data-stu-id="b08e9-114">[**IAgentCommandsEx::SetHelpContextID**](iagentcommandsex--sethelpcontextid.md), [**IAgentCharacterEx::SetHelpModeOn**](iagentcharacterex--sethelpmodeon.md), [**IAgentCharacterEx::GetHelpFileName**](iagentcharacterex--gethelpfilename.md)</span></span>


 

 




