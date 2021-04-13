---
title: Parser-Erweiterungen
description: Parser-Erweiterungen
ms.assetid: b520aebe-9182-4e60-9111-49af09cdbd79
keywords:
- Parser-Erweiterungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a22f4b4dced29e25662a6fc521057a055b56f70
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388492"
---
# <a name="parser-enhancements"></a><span data-ttu-id="e1e6e-104">Parser-Erweiterungen</span><span class="sxs-lookup"><span data-stu-id="e1e6e-104">Parser Enhancements</span></span>

<span data-ttu-id="e1e6e-105">In Windows Server 2003 mit Service Pack 1 (SP1) lässt die HTTP-Server-API die folgenden Anforderungen von HTTP-Clients zu.</span><span class="sxs-lookup"><span data-stu-id="e1e6e-105">In Windows Server 2003 with Service Pack 1 (SP1), the HTTP Server API allows the following requests from HTTP clients.</span></span>

-   <span data-ttu-id="e1e6e-106">Anforderungen, die einen Einzel Zeilenvorschub (LF) als Zeilen Abschluss Zeichen verwenden.</span><span class="sxs-lookup"><span data-stu-id="e1e6e-106">Requests that use a single Line Feed (LF) as line terminators.</span></span>
-   <span data-ttu-id="e1e6e-107">Anforderungen, die lineare Leerräume (LWS) zwischen der HTTP-Anforderungs Zeile und dem Start von Headern enthalten.</span><span class="sxs-lookup"><span data-stu-id="e1e6e-107">Requests that contain linear white space (LWS) between the HTTP request line and start of headers.</span></span>

<span data-ttu-id="e1e6e-108">Diese Verhalten sind standardmäßig aktiviert und werden nicht durch Registrierungs Einstellungen gesteuert.</span><span class="sxs-lookup"><span data-stu-id="e1e6e-108">These behaviors are enabled by default and are not controlled by registry settings.</span></span>

 

 




