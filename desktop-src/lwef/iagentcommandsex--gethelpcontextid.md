---
title: Iagentcommandsex gethelpcontextid
description: Iagentcommandsex gethelpcontextid
ms.assetid: db5f93e9-8cd3-4147-94b4-50cfe12033c4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a49a633a66622626973e450b9566033b1ad96e7
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104038908"
---
# <a name="iagentcommandsexgethelpcontextid"></a><span data-ttu-id="6d400-103">Iagentcommandsex:: gethelpcontextid</span><span class="sxs-lookup"><span data-stu-id="6d400-103">IAgentCommandsEx::GetHelpContextID</span></span>

<span data-ttu-id="6d400-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="6d400-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetHelpContextID(
   long * pulHelpID  // address of Commands object help topic ID
);
```

<span data-ttu-id="6d400-105">Ruft die [**HelpContextID**](helpcontextid-property.md) für ein [**Command**](/windows/desktop/lwef/the-command-object) -Objekt ab.</span><span class="sxs-lookup"><span data-stu-id="6d400-105">Retrieves the [**HelpContextID**](helpcontextid-property.md) for a [**Command**](/windows/desktop/lwef/the-command-object) object.</span></span>

-   <span data-ttu-id="6d400-106">Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="6d400-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="6d400-107"><span id="pulHelpID"></span><span id="pulhelpid"></span><span id="PULHELPID"></span>*pulhelpid*</span><span class="sxs-lookup"><span data-stu-id="6d400-107"><span id="pulHelpID"></span><span id="pulhelpid"></span><span id="PULHELPID"></span>*pulHelpID*</span></span>
</dt> <dd>

<span data-ttu-id="6d400-108">Adresse einer Variablen, die die Kontext Nummer des Hilfe Themas für das [**Befehls**](/windows/desktop/lwef/the-command-object) Objekt empfängt.</span><span class="sxs-lookup"><span data-stu-id="6d400-108">Address of a variable that receives the context number of the help topic for the [**Command**](/windows/desktop/lwef/the-command-object) object.</span></span>

</dd> </dl>

<span data-ttu-id="6d400-109">Wenn Sie eine Windows-Hilfedatei für Ihre Anwendung erstellt und die [**HelpFile**](helpfile-property.md) -Eigenschaft des Zeichens festgelegt haben, ruft der Microsoft-Agent automatisch die Hilfe auf, wenn [**helpmudeon**](helpmodeon-property.md) auf **true** festgelegt ist und der Benutzer Ihr [**Befehls**](/windows/desktop/lwef/the-command-object) Objekt auswählt.</span><span class="sxs-lookup"><span data-stu-id="6d400-109">If you've created a Windows Help file for your application and set the character's [**HelpFile**](helpfile-property.md) property, Microsoft Agent automatically calls Help when [**HelpModeOn**](helpmodeon-property.md) is set to **True** and the user selects your [**Command**](/windows/desktop/lwef/the-command-object) object.</span></span> <span data-ttu-id="6d400-110">Wenn in [**HelpContextID**](helpcontextid-property.md)eine Kontext Nummer vorhanden ist, ruft der-Agent Hilfe auf und sucht nach dem Thema, das durch die aktuelle Kontext Nummer identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="6d400-110">If there is a context number in the [**HelpContextID**](helpcontextid-property.md), Agent calls Help and searches for the topic identified by the current context number.</span></span> <span data-ttu-id="6d400-111">Die aktuelle Kontext Nummer ist der Wert von **HelpContextID** für das **Command** -Objekt.</span><span class="sxs-lookup"><span data-stu-id="6d400-111">The current context number is the value of **HelpContextID** for the **Command** object.</span></span>

<span data-ttu-id="6d400-112">Diese Eigenschaft gilt nur für die Verwendung des Zeichens durch die Client Anwendung. Diese Einstellung wirkt sich nicht auf andere Clients des Zeichens oder andere Zeichen ihrer Client Anwendung aus.</span><span class="sxs-lookup"><span data-stu-id="6d400-112">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

> [!Note]  
> <span data-ttu-id="6d400-113">Das Entwickeln einer Hilfedatei erfordert den Microsoft Windows Help Compiler.</span><span class="sxs-lookup"><span data-stu-id="6d400-113">Building a Help file requires the Microsoft Windows Help Compiler.</span></span>

 

## <a name="see-also"></a><span data-ttu-id="6d400-114">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="6d400-114">See Also</span></span>

<span data-ttu-id="6d400-115">[**Iagentcommandsex::**](iagentcommandsex--sethelpcontextid.md)Setup Elementname, [**iagentcharakteriex::**](iagentcharacterex--sethelpmodeon.md)Setup Elementname, [**iagentcharakteriex::**](iagentcharacterex--sethelpfilename.md) Setup Name</span><span class="sxs-lookup"><span data-stu-id="6d400-115">[**IAgentCommandsEx::SetHelpContextID**](iagentcommandsex--sethelpcontextid.md), [**IAgentCharacterEx::SetHelpModeOn**](iagentcharacterex--sethelpmodeon.md), [**IAgentCharacterEx::SetHelpFileName**](iagentcharacterex--sethelpfilename.md)</span></span>


 

 