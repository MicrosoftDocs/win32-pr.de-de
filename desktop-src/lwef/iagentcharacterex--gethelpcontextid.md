---
title: Iagentcharakteriex gethelpcontextid
description: Iagentcharakteriex gethelpcontextid
ms.assetid: 9dec5b0c-4758-4859-9aa6-6db3ef0d6b56
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bfec03a217745838b88a592433defae01529ed50
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103713181"
---
# <a name="iagentcharacterexgethelpcontextid"></a><span data-ttu-id="40d33-103">Iagentcharakteriex:: gethelpcontextid</span><span class="sxs-lookup"><span data-stu-id="40d33-103">IAgentCharacterEx::GetHelpContextID</span></span>

<span data-ttu-id="40d33-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="40d33-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetHelpContextID(
   long * pulHelpID  // address of character's help topic ID
);
```

<span data-ttu-id="40d33-105">Ruft [**HelpContextID**](helpcontextid-property.md) für das Zeichen ab.</span><span class="sxs-lookup"><span data-stu-id="40d33-105">Retrieves the [**HelpContextID**](helpcontextid-property.md) for the character.</span></span>

-   <span data-ttu-id="40d33-106">Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="40d33-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="40d33-107"><span id="pulHelpID"></span><span id="pulhelpid"></span><span id="PULHELPID"></span>*pulhelpid*</span><span class="sxs-lookup"><span data-stu-id="40d33-107"><span id="pulHelpID"></span><span id="pulhelpid"></span><span id="PULHELPID"></span>*pulHelpID*</span></span>
</dt> <dd>

<span data-ttu-id="40d33-108">Adresse einer Variablen, die die Kontext Nummer des Hilfe Themas für das Zeichen empfängt.</span><span class="sxs-lookup"><span data-stu-id="40d33-108">Address of a variable that receives the context number of the help topic for the character.</span></span>

</dd> </dl>

<span data-ttu-id="40d33-109">Wenn Sie eine Windows-Hilfedatei für Ihre Anwendung erstellt und die [**HelpFile**](helpfile-property.md) -Eigenschaft des Zeichens festgelegt haben, ruft der Microsoft-Agent automatisch die Hilfe auf, wenn [**helpmudeon**](helpmodeon-property.md) auf **true** festgelegt ist und der Benutzer das Zeichen auswählt.</span><span class="sxs-lookup"><span data-stu-id="40d33-109">If you've created a Windows Help file for your application and set the character's [**HelpFile**](helpfile-property.md) property, Microsoft Agent automatically calls Help when [**HelpModeOn**](helpmodeon-property.md) is set to **True** and the user selects the character.</span></span> <span data-ttu-id="40d33-110">Wenn in [**HelpContextID**](helpcontextid-property.md)eine Kontext Nummer vorhanden ist, ruft der-Agent Hilfe auf und sucht nach dem Thema, das durch die aktuelle Kontext Nummer identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="40d33-110">If there is a context number in the [**HelpContextID**](helpcontextid-property.md), Agent calls Help and searches for the topic identified by the current context number.</span></span> <span data-ttu-id="40d33-111">Die aktuelle Kontext Nummer ist der Wert von **HelpContextID** für das Zeichen.</span><span class="sxs-lookup"><span data-stu-id="40d33-111">The current context number is the value of **HelpContextID** for the character.</span></span>

<span data-ttu-id="40d33-112">**Iagentcharakteriex:: gethelpcontextid** gibt die [**HelpContextID**](helpcontextid-property.md) zurück, die Sie für das Zeichen festgelegt haben.</span><span class="sxs-lookup"><span data-stu-id="40d33-112">**IAgentCharacterEx::GetHelpContextID** returns the [**HelpContextID**](helpcontextid-property.md) you set for the character.</span></span> <span data-ttu-id="40d33-113">Die von anderen Clients festgelegte **HelpContextID** wird nicht zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="40d33-113">It does not return the **HelpContextID** set by other clients.</span></span>

> [!Note]  
> <span data-ttu-id="40d33-114">Das Entwickeln einer Hilfedatei erfordert den Microsoft Windows Help Compiler.</span><span class="sxs-lookup"><span data-stu-id="40d33-114">Building a Help file requires the Microsoft Windows Help Compiler.</span></span>

 

## <a name="see-also"></a><span data-ttu-id="40d33-115">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="40d33-115">See Also</span></span>

<span data-ttu-id="40d33-116">[**Iagentcharakteriex::**](iagentcharacterex--sethelpcontextid.md)Setup Element-ID, [**iagentcharakteriex::**](iagentcharacterex--sethelpmodeon.md)Setup Elementname, iagentcharakteriex: [**:**](iagentcharacterex--sethelpfilename.md) Setup Name</span><span class="sxs-lookup"><span data-stu-id="40d33-116">[**IAgentCharacterEx::SetHelpContextID**](iagentcharacterex--sethelpcontextid.md), [**IAgentCharacterEx::SetHelpModeOn**](iagentcharacterex--sethelpmodeon.md), [**IAgentCharacterEx::SetHelpFileName**](iagentcharacterex--sethelpfilename.md)</span></span>


 

 




