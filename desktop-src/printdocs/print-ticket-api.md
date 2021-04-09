---
description: Die-Druck Ticket-API ermöglicht es Anwendungen, Druck Tickets zu verwalten und zu konvertieren.
ms.assetid: 4f854c1a-f2e1-48c4-9cc1-8a0fcf1bebed
title: Print Ticket-API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e19cfd8d624a1390b8afacd625e92fcee2704dd
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2021
ms.locfileid: "104050726"
---
# <a name="print-ticket-api"></a><span data-ttu-id="e2306-103">Print Ticket-API</span><span class="sxs-lookup"><span data-stu-id="e2306-103">Print Ticket API</span></span>

<span data-ttu-id="e2306-104">Die-Druck Ticket-API ermöglicht es Anwendungen, Druck Tickets zu verwalten und zu konvertieren.</span><span class="sxs-lookup"><span data-stu-id="e2306-104">The Print Ticket API provides enables applications to manage and convert print tickets.</span></span>

<span data-ttu-id="e2306-105">Ein Druck Ticket ist eine XPS-Dokument Komponente, die die bevorzugten Druckereinstellungen für eine Seite in einem Dokument, ein gesamtes Dokument oder einen Druckauftrag enthält, der ein oder mehrere Dokumente enthält.</span><span class="sxs-lookup"><span data-stu-id="e2306-105">A print ticket is an XPS document component that contains the preferred printer settings for a page in a document, or for an entire document, or for a print job that contains one or more documents.</span></span> <span data-ttu-id="e2306-106">Beachten Sie, dass Druck Tickets nur in XPS-Dokumenten gefunden werden.</span><span class="sxs-lookup"><span data-stu-id="e2306-106">Note that print tickets are only found in XPS documents.</span></span>

<span data-ttu-id="e2306-107">Bevor der Drucker das Druck Ticket verwenden kann, muss das Druck Ticket anhand der Merkmale des Druckers überprüft werden, die in den Druckfunktionen des Druckers definiert sind.</span><span class="sxs-lookup"><span data-stu-id="e2306-107">Before the printer can use the print ticket, the print ticket must be validated against the printer's characteristics, which are defined in the printer's Print Capabilities.</span></span> <span data-ttu-id="e2306-108">Die Anwendung führt diese Überprüfung durch Aufrufen der Druck Ticket-API durch.</span><span class="sxs-lookup"><span data-stu-id="e2306-108">The application performs that validation by calling the Print Ticket API.</span></span>

<span data-ttu-id="e2306-109">Die Funktionen PrintTicket und printwerden mithilfe von Elementen des Druck Schemas beschrieben, das durch die [Druck Schema Spezifikation](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)definiert wird.</span><span class="sxs-lookup"><span data-stu-id="e2306-109">The PrintTicket and PrintCapabilities are described by using elements of the Print Schema, which is defined by the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="e2306-110">Dieses Thema enthält Informationen über die folgenden API-Elemente:</span><span class="sxs-lookup"><span data-stu-id="e2306-110">This topic contains information about the following API elements:</span></span>

-   [<span data-ttu-id="e2306-111">Druckticket-API-Funktionen</span><span class="sxs-lookup"><span data-stu-id="e2306-111">Print Ticket API Functions</span></span>](print-ticket-api-functions.md)
-   [<span data-ttu-id="e2306-112">API-Enumerationen der Druck Ticket</span><span class="sxs-lookup"><span data-stu-id="e2306-112">Print Ticket API Enumerations</span></span>](print-ticket-api-enumerations.md)

<span data-ttu-id="e2306-113">Das folgende Diagramm zeigt die Beziehung zwischen der Druck Ticket-API und den anderen Druck-APIs, die von einer systemeigenen Windows-Anwendung verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="e2306-113">The following diagram shows the relationship of the Print Ticket API to the other Print APIs that a native Windows application can use.</span></span>

![ein Diagramm, das die Beziehung zwischen der Druck Ticket-API und den anderen Druck-APIs anzeigt, die eine systemeigene Windows-Anwendung verwenden kann](images/print-apis-pt.png)

## <a name="related-topics"></a><span data-ttu-id="e2306-115">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="e2306-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e2306-116">XPS-Druck-API</span><span class="sxs-lookup"><span data-stu-id="e2306-116">XPS Print API</span></span>](xps-printing.md)
</dt> <dt>

[<span data-ttu-id="e2306-117">Druckspoolerapi</span><span class="sxs-lookup"><span data-stu-id="e2306-117">Print Spooler API</span></span>](print-spooler-api.md)
</dt> <dt>

[<span data-ttu-id="e2306-118">GDI-Druck-API</span><span class="sxs-lookup"><span data-stu-id="e2306-118">GDI Print API</span></span>](gdi-printing.md)
</dt> <dt>

[<span data-ttu-id="e2306-119">Druck Schema Spezifikation</span><span class="sxs-lookup"><span data-stu-id="e2306-119">Print Schema Specification</span></span>](https://go.microsoft.com/fwlink/?linkid=2022117)
</dt> <dt>

[<span data-ttu-id="e2306-120">XML Paper Specification</span><span class="sxs-lookup"><span data-stu-id="e2306-120">XML Paper Specification</span></span>](https://go.microsoft.com/fwlink/?linkid=2022122)
</dt> </dl>

 

 



