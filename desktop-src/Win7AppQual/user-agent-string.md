---
description: .
ms.assetid: bcf0a534-c123-40c4-91b4-645c4912f31a
title: Zeichenfolge des Benutzer-Agents
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d2d9b25863fbc89ee88e24e3f98b8facad6a59f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960989"
---
# <a name="user-agent-string"></a><span data-ttu-id="f9d90-103">Zeichenfolge des Benutzer-Agents</span><span class="sxs-lookup"><span data-stu-id="f9d90-103">User Agent String</span></span>

<span data-ttu-id="f9d90-104">Die *Zeichenfolge des Benutzer-Agents* enthält Informationen zur Identität eines Browsers.</span><span class="sxs-lookup"><span data-stu-id="f9d90-104">The *User Agent String* contains information about a browser's identity.</span></span> <span data-ttu-id="f9d90-105">Die Zeichenfolge des Benutzer-Agents wird bei jeder Anforderung eines Webservers als HTTP-Header an den Webserver gemeldet.</span><span class="sxs-lookup"><span data-stu-id="f9d90-105">The User Agent String is reported to the web server as an HTTP header every time that a browser makes a request to a web server.</span></span> <span data-ttu-id="f9d90-106">Sie können auch über ein Client seitiges Skript darauf zugreifen.</span><span class="sxs-lookup"><span data-stu-id="f9d90-106">You can also access it through a client-side script.</span></span> <span data-ttu-id="f9d90-107">Beispielsweise können Sie die Zeichenfolge des Benutzer-Agents anzeigen, indem Sie die folgende URL in die Adressleiste von Windows Internet Explorer 8 eingeben: "JavaScript: Alert (Navigator. UserAgent)".</span><span class="sxs-lookup"><span data-stu-id="f9d90-107">For example, you can display the User Agent String by typing the following URL into the Windows Internet Explorer 8 address bar: "javascript:alert(navigator.userAgent)".</span></span> <span data-ttu-id="f9d90-108">Die folgende Abbildung zeigt das typische resultierende Dialogfeld aus Internet Explorer 8 unter Windows 7.</span><span class="sxs-lookup"><span data-stu-id="f9d90-108">The following illustration shows the typical resulting dialog box from Internet Explorer 8 running on Windows 7.</span></span>

![Screenshot des Fensters "Internet Explorer diaog" mit der Zeichenfolge "User Agent"](images/useragent-alert.png)

<span data-ttu-id="f9d90-110">In der Regel wird die Zeichenfolge des Benutzer-Agents speziell für die MSIE-Teil Zeichenfolge analysiert.</span><span class="sxs-lookup"><span data-stu-id="f9d90-110">Typically, the User Agent String is parsed specifically for the MSIE substring.</span></span> <span data-ttu-id="f9d90-111">Basierend auf der gemeldeten Version des Browsers führt die Client seitige oder serverseitige Programmierlogik eine andere Aktion aus.</span><span class="sxs-lookup"><span data-stu-id="f9d90-111">Based on the reported version of the browser, the client-side or server-side programming logic takes a different action.</span></span> <span data-ttu-id="f9d90-112">Weitere Informationen zur Benutzer-Agent-Zeichenfolge finden Sie unter [Was wird Windows Internet Explorer als User-Agent Zeichenfolge melden?](/previous-versions/cc817582(v=msdn.10)) in der MSDN Library.</span><span class="sxs-lookup"><span data-stu-id="f9d90-112">For more information about the User Agent String, see [What Will Windows Internet Explorer Report as the User-Agent String?](/previous-versions/cc817582(v=msdn.10)) in the MSDN Library.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f9d90-113">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="f9d90-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f9d90-114">Beheben von Kompatibilitätsproblemen in Webanwendungen mithilfe der Kompatibilitäts Ansicht</span><span class="sxs-lookup"><span data-stu-id="f9d90-114">Fixing Compatibility Issues in Web Applications by Using Compatibility View</span></span>](remediating-web-applications-and-add-ons.md)
</dt> </dl>

 

 



