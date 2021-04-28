---
description: Zeichenfolge des Benutzer-Agents
ms.assetid: bcf0a534-c123-40c4-91b4-645c4912f31a
title: Zeichenfolge des Benutzer-Agents
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d227eead5c02f50b689779bd0a8f0ba4b031d06
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084178"
---
# <a name="user-agent-string"></a><span data-ttu-id="24e1c-103">Zeichenfolge des Benutzer-Agents</span><span class="sxs-lookup"><span data-stu-id="24e1c-103">User Agent String</span></span>

<span data-ttu-id="24e1c-104">Die *Benutzer-Agent-Zeichenfolge* enthält Informationen zur Identität eines Browsers.</span><span class="sxs-lookup"><span data-stu-id="24e1c-104">The *User Agent String* contains information about a browser's identity.</span></span> <span data-ttu-id="24e1c-105">Die Zeichenfolge des Benutzer-Agents wird dem Webserver jedes Mal als HTTP-Header gemeldet, wenn ein Browser eine Anforderung an einen Webserver stellt.</span><span class="sxs-lookup"><span data-stu-id="24e1c-105">The User Agent String is reported to the web server as an HTTP header every time that a browser makes a request to a web server.</span></span> <span data-ttu-id="24e1c-106">Sie können auch über ein clientseitiges Skript darauf zugreifen.</span><span class="sxs-lookup"><span data-stu-id="24e1c-106">You can also access it through a client-side script.</span></span> <span data-ttu-id="24e1c-107">Beispielsweise können Sie die Zeichenfolge des Benutzer-Agents anzeigen, indem Sie die folgende URL in die Adressleiste von Windows Internet Explorer 8 eingeben: "javascript:alert(navigator.userAgent)".</span><span class="sxs-lookup"><span data-stu-id="24e1c-107">For example, you can display the User Agent String by typing the following URL into the Windows Internet Explorer 8 address bar: "javascript:alert(navigator.userAgent)".</span></span> <span data-ttu-id="24e1c-108">Die folgende Abbildung zeigt das typische resultierende Dialogfeld aus Internet Explorer 8 unter Windows 7.</span><span class="sxs-lookup"><span data-stu-id="24e1c-108">The following illustration shows the typical resulting dialog box from Internet Explorer 8 running on Windows 7.</span></span>

![Screenshot des Internet Explorer-Diaogfelds mit der Zeichenfolge des Benutzer-Agents](images/useragent-alert.png)

<span data-ttu-id="24e1c-110">In der Regel wird die Zeichenfolge des Benutzer-Agents speziell für die MSIE-Teilzeichenfolge analysiert.</span><span class="sxs-lookup"><span data-stu-id="24e1c-110">Typically, the User Agent String is parsed specifically for the MSIE substring.</span></span> <span data-ttu-id="24e1c-111">Basierend auf der gemeldeten Version des Browsers führt die clientseitige oder serverseitige Programmierlogik eine andere Aktion aus.</span><span class="sxs-lookup"><span data-stu-id="24e1c-111">Based on the reported version of the browser, the client-side or server-side programming logic takes a different action.</span></span> <span data-ttu-id="24e1c-112">Weitere Informationen zur Zeichenfolge des Benutzer-Agents finden Sie unter [Was wird Windows Internet Explorer Bericht als User-Agent Zeichenfolge?](/previous-versions/cc817582(v=msdn.10)) in der MSDN Library.</span><span class="sxs-lookup"><span data-stu-id="24e1c-112">For more information about the User Agent String, see [What Will Windows Internet Explorer Report as the User-Agent String?](/previous-versions/cc817582(v=msdn.10)) in the MSDN Library.</span></span>

## <a name="related-topics"></a><span data-ttu-id="24e1c-113">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="24e1c-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="24e1c-114">Beheben von Kompatibilitätsproblemen in Webanwendungen mithilfe von Kompatibilitätsansicht</span><span class="sxs-lookup"><span data-stu-id="24e1c-114">Fixing Compatibility Issues in Web Applications by Using Compatibility View</span></span>](remediating-web-applications-and-add-ons.md)
</dt> </dl>

 

 



