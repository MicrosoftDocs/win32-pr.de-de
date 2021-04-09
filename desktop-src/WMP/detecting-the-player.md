---
title: Erkennen des Players
description: Erkennen des Players
ms.assetid: dc034226-578a-45de-9463-e1798fef874e
keywords:
- Windows Media Player Online Stores, erkennen von Playern
- Online Stores, erkennen von Playern
- Typ 1 Online Stores, erkennen von Playern
- Typ 2 Online Stores, erkennen von Playern
- Windows Media Player Online Stores, Player Erkennung
- Online Stores, Player Erkennung
- Typ 1 Online Stores, Player Erkennung
- Typ 2 Online Stores, Player Erkennung
- Spieler Erkennung
- Erkennen von Playern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb919e790b07ccf5d8df587abd63d2344534b16b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947793"
---
# <a name="detecting-the-player"></a><span data-ttu-id="e6e4c-113">Erkennen des Players</span><span class="sxs-lookup"><span data-stu-id="e6e4c-113">Detecting the Player</span></span>

<span data-ttu-id="e6e4c-114">Wenn Sie eine Webseite für den Online Shop erstellen, können Sie festlegen, dass Benutzer in der Lage sein sollen, die Seite in einem Webbrowser oder in Windows Media Player anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="e6e4c-114">When creating a webpage for your online store, you may decide that you want users to be able to view the page in a Web browser or in Windows Media Player.</span></span> <span data-ttu-id="e6e4c-115">Sie können ein ASP-Skript verwenden, um zu bestimmen, ob Ihre Webseite im Player gehostet wird.</span><span class="sxs-lookup"><span data-stu-id="e6e4c-115">You can use an ASP script to determine whether your webpage is hosted in the Player.</span></span>

<span data-ttu-id="e6e4c-116">Der folgende Beispielcode ruft den Versions Parameter aus der URL-Abfrage Zeichenfolge ab, um zu bestimmen, ob die Seite in Windows-Media Player gehostet wird:</span><span class="sxs-lookup"><span data-stu-id="e6e4c-116">The following example code retrieves the version parameter from the URL query string to determine whether the page is hosted in Windows Media Player:</span></span>


```C++
<%
    Dim sVersion

    sVersion = Trim(Request.QueryString("version")) 
 
    If sVersion = "" Then   
        Response.Write "Not hosted in Windows Media Player"
    Else 
        Response.Write "Hosted in Windows Media Player<BR>"
        Response.Write "Version is " & sVersion
    End If
%>
```



<span data-ttu-id="e6e4c-117">Beachten Sie, dass der vorangehende Code davon ausgeht, dass der Versions Parameter in der Abfrage Zeichenfolge vorhanden ist, wenn er in Windows Media Player</span><span class="sxs-lookup"><span data-stu-id="e6e4c-117">Note that the preceding code assumes that the version parameter exists in the query string when hosted in Windows Media Player.</span></span> <span data-ttu-id="e6e4c-118">Dies gilt für Seiten, die vom Benutzer geöffnet werden, aber möglicherweise nicht für Seiten, die mithilfe von " **extern. navigatetaskpaneurl**" geöffnet wurden.</span><span class="sxs-lookup"><span data-stu-id="e6e4c-118">This is true for pages opened by the user, but may not be true for pages opened by using **External.NavigateTaskPaneURL**.</span></span> <span data-ttu-id="e6e4c-119">Damit die Versions Abfrage Zeichenfolge bei Programm gesteuerter Navigation vorhanden ist, müssen Sie den Versions Parameter dem Methodenaufrufe hinzufügen oder die Version dynamisch an die Basis-URL des **Navigate** -Elements des serviceInfo-Dokuments anhängen.</span><span class="sxs-lookup"><span data-stu-id="e6e4c-119">For the version query string to exist when navigating programmatically, you must add the version parameter to the method call or dynamically append the version to the base URL of the **Navigate** element of your ServiceInfo document.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e6e4c-120">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="e6e4c-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e6e4c-121">**Dynamisches Erstellen des serviceingefo-Dokuments**</span><span class="sxs-lookup"><span data-stu-id="e6e4c-121">**Creating the ServiceInfo Document Dynamically**</span></span>](creating-the-serviceinfo-document-dynamically.md)
</dt> <dt>

[<span data-ttu-id="e6e4c-122">**Extern. navigatetaskpaneurl**</span><span class="sxs-lookup"><span data-stu-id="e6e4c-122">**External.NavigateTaskPaneURL**</span></span>](external-navigatetaskpaneurl.md)
</dt> <dt>

[<span data-ttu-id="e6e4c-123">**Informationen, die von Typ 1 und Typ 2 Online Stores gemeinsam sind**</span><span class="sxs-lookup"><span data-stu-id="e6e4c-123">**Information Common to Type 1 and Type 2 Online Stores**</span></span>](information-common-to-type-1-and-type-2-online-stores.md)
</dt> </dl>

 

 




