---
title: Iagentcommandex gethelpcontextid
description: Iagentcommandex gethelpcontextid
ms.assetid: 97b390f3-ab24-4c09-aa87-d76076eba995
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f330e8ae8cd8bdaff5e27ccd00352b41b07be2b6
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104390294"
---
# <a name="iagentcommandexgethelpcontextid"></a><span data-ttu-id="a1bc4-103">Iagentcommandex:: gethelpcontextid</span><span class="sxs-lookup"><span data-stu-id="a1bc4-103">IAgentCommandEx::GetHelpContextID</span></span>

<span data-ttu-id="a1bc4-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="a1bc4-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetHelpContextID(
   long * pulID  //  address of command's help topic ID
);
```

<span data-ttu-id="a1bc4-105">Ruft die [**HelpContextID**](helpcontextid-property-com.md) für ein [**Command**](/windows/desktop/lwef/the-command-object) -Objekt ab.</span><span class="sxs-lookup"><span data-stu-id="a1bc4-105">Retrieves the [**HelpContextID**](helpcontextid-property-com.md) for a [**Command**](/windows/desktop/lwef/the-command-object) object.</span></span>

-   <span data-ttu-id="a1bc4-106">Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="a1bc4-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="a1bc4-107"><span id="pulID"></span><span id="pulid"></span><span id="PULID"></span>*pulid*</span><span class="sxs-lookup"><span data-stu-id="a1bc4-107"><span id="pulID"></span><span id="pulid"></span><span id="PULID"></span>*pulID*</span></span>
</dt> <dd>

<span data-ttu-id="a1bc4-108">Adresse einer Variablen, die die Kontext Nummer des Hilfe Themas empfängt, das dem [**Befehls**](/windows/desktop/lwef/the-command-object) Objekt zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="a1bc4-108">Address of a variable that receives the context number of the help topic associated with the [**Command**](/windows/desktop/lwef/the-command-object) object.</span></span>

</dd> </dl>

<span data-ttu-id="a1bc4-109">Wenn Sie eine Windows-Hilfedatei für Ihre Anwendung erstellt und die [**HelpFile**](helpfile-property.md) -Eigenschaft Ihres Zeichens auf diese Datei festgelegt haben, ruft der Microsoft-Agent automatisch die Hilfe auf, wenn [**helpmudeon**](helpmodeon-property.md) auf **true** festgelegt ist und der Benutzer den Befehl auswählt.</span><span class="sxs-lookup"><span data-stu-id="a1bc4-109">If you've created a Windows Help file for your application and set your character's [**HelpFile**](helpfile-property.md) property to this file, Microsoft Agent automatically calls Help when [**HelpModeOn**](helpmodeon-property.md) is set to **True** and the user selects the command.</span></span> <span data-ttu-id="a1bc4-110">Wenn in [**HelpContextID**](helpcontextid-property-com.md)eine Kontext Nummer vorhanden ist, ruft der-Agent Hilfe auf und sucht nach dem Thema, das durch die aktuelle Kontext Nummer identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="a1bc4-110">If there is a context number in the [**HelpContextID**](helpcontextid-property-com.md), Agent calls Help and searches for the topic identified by the current context number.</span></span> <span data-ttu-id="a1bc4-111">Die aktuelle Kontext Nummer ist der Wert von **HelpContextID** für den Befehl.</span><span class="sxs-lookup"><span data-stu-id="a1bc4-111">The current context number is the value of **HelpContextID** for the command.</span></span>

> [!Note]  
> <span data-ttu-id="a1bc4-112">Das Entwickeln einer Hilfedatei erfordert den Microsoft Windows Help Compiler.</span><span class="sxs-lookup"><span data-stu-id="a1bc4-112">Building a Help file requires the Microsoft Windows Help Compiler.</span></span>

 

## <a name="see-also"></a><span data-ttu-id="a1bc4-113">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="a1bc4-113">See Also</span></span>

<span data-ttu-id="a1bc4-114">[**Iagentcommandex::**](iagentcommandex--sethelpcontextid.md)Setup Element-ID, [**iagentcharakteriex::**](iagentcharacterex--sethelpmodeon.md)Setup Elementname, [**iagentcharakteriex::**](iagentcharacterex--sethelpfilename.md) Setup Name</span><span class="sxs-lookup"><span data-stu-id="a1bc4-114">[**IAgentCommandEx::SetHelpContextID**](iagentcommandex--sethelpcontextid.md), [**IAgentCharacterEx::SetHelpModeOn**](iagentcharacterex--sethelpmodeon.md), [**IAgentCharacterEx::SetHelpFileName**](iagentcharacterex--sethelpfilename.md)</span></span>


 

 