---
description: Stellt eine Schnittstelle zum Druck Spooler bereit. Anwendungen können diese API verwenden, um XPS-Dokumente an einen Drucker zu senden.
ms.assetid: df06ddcb-e573-461c-99a3-8f108fe2c143
title: XPS-Druck-API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30c53322a8ae6a03c3ac4bb71fc680f719999546
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106359996"
---
# <a name="xps-print-api"></a><span data-ttu-id="9cb23-104">XPS-Druck-API</span><span class="sxs-lookup"><span data-stu-id="9cb23-104">XPS Print API</span></span>

<span data-ttu-id="9cb23-105">\[Die XPS-Druck-API wird nicht unterstützt und kann in Zukunft geändert oder nicht verfügbar sein.</span><span class="sxs-lookup"><span data-stu-id="9cb23-105">\[The XPS Print API is not supported and may be altered or unavailable in the future.</span></span> <span data-ttu-id="9cb23-106">Client Anwendungen sollten stattdessen die [API zum Drucken von Dokument Paketen](./tailored-app-printing-api.md) verwenden.\]</span><span class="sxs-lookup"><span data-stu-id="9cb23-106">Client applications should use the [Print Document Package API](./tailored-app-printing-api.md) instead.\]</span></span>

<span data-ttu-id="9cb23-107">Stellt eine Schnittstelle zum Druck Spooler bereit.</span><span class="sxs-lookup"><span data-stu-id="9cb23-107">Provides an interface to the print spooler.</span></span> <span data-ttu-id="9cb23-108">Anwendungen können diese API verwenden, um XPS-Dokumente an einen Drucker zu senden.</span><span class="sxs-lookup"><span data-stu-id="9cb23-108">Applications can use this API to send XPS documents to a printer.</span></span>

<span data-ttu-id="9cb23-109">Dieser Abschnitt enthält Informationen zu den folgenden Themen.</span><span class="sxs-lookup"><span data-stu-id="9cb23-109">This section contains information about the following topics.</span></span>

<dl>

[<span data-ttu-id="9cb23-110">Informationen zur XPS-Druck-API</span><span class="sxs-lookup"><span data-stu-id="9cb23-110">About the XPS Print API</span></span>](about-xps-print-api.md)  
[<span data-ttu-id="9cb23-111">Verwenden der XPS-Druck-API</span><span class="sxs-lookup"><span data-stu-id="9cb23-111">Using the XPS Print API</span></span>](using-the-xps-print-api.md)  
[<span data-ttu-id="9cb23-112">XPS-Druck-API-Referenz</span><span class="sxs-lookup"><span data-stu-id="9cb23-112">XPS Print API Reference</span></span>](xpsprint-interfaces.md)  
</dl>

<span data-ttu-id="9cb23-113">Native Windows-Anwendungen, die XPS-Dokumente erstellen, z. b. mithilfe der [XPS-Dokument-API](/previous-versions/windows/desktop/dd316976(v=vs.85)), können die XPS-Druck-API verwenden, um XPS-Dokumentinhalte an einen Drucker zu senden.</span><span class="sxs-lookup"><span data-stu-id="9cb23-113">Native Windows applications that create XPS documents, such as by using the [XPS Document API](/previous-versions/windows/desktop/dd316976(v=vs.85)), can use the XPS Print API to send XPS document content to a printer.</span></span>

<span data-ttu-id="9cb23-114">Das folgende Diagramm zeigt die Beziehung der XPS-Druck-API zu den anderen Druck-APIs, die von einer systemeigenen Windows-Anwendung verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="9cb23-114">The following diagram shows the relationship of the XPS Print API to the other Print APIs that a native Windows application can use.</span></span>

![ein Diagramm, das die Beziehung zwischen der XPS-Druck-API und den anderen Druck-APIs anzeigt, die eine systemeigene Windows-Anwendung verwenden kann](images/print-apis-xps.png)

## <a name="related-topics"></a><span data-ttu-id="9cb23-116">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="9cb23-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9cb23-117">**AddJob**</span><span class="sxs-lookup"><span data-stu-id="9cb23-117">**AddJob**</span></span>](addjob.md)
</dt> <dt>

[<span data-ttu-id="9cb23-118">Druckspoolerapi</span><span class="sxs-lookup"><span data-stu-id="9cb23-118">Print Spooler API</span></span>](print-spooler-api.md)
</dt> <dt>

[<span data-ttu-id="9cb23-119">Print Ticket-API</span><span class="sxs-lookup"><span data-stu-id="9cb23-119">Print Ticket API</span></span>](print-ticket-api.md)
</dt> <dt>

[<span data-ttu-id="9cb23-120">GDI-Druck-API</span><span class="sxs-lookup"><span data-stu-id="9cb23-120">GDI Print API</span></span>](gdi-printing.md)
</dt> </dl>

 

 
