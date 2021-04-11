---
description: Die GDI-Druck-API stellt Anwendungen eine geräteunabhängige Druck Schnittstelle bereit.
ms.assetid: 3115c9e0-05c9-462d-8238-fc035ea32d4e
title: GDI-Druck-API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0239282543a68c6fe8b5d6503d085582fd9c20db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215974"
---
# <a name="gdi-print-api"></a><span data-ttu-id="df382-103">GDI-Druck-API</span><span class="sxs-lookup"><span data-stu-id="df382-103">GDI Print API</span></span>

<span data-ttu-id="df382-104">Die GDI-Druck-API stellt Anwendungen eine geräteunabhängige Druck Schnittstelle bereit.</span><span class="sxs-lookup"><span data-stu-id="df382-104">The GDI Print API provides applications with a device-independent printing interface.</span></span> <span data-ttu-id="df382-105">Verwenden Sie diese Schnittstelle, wenn die Anwendung GDI zum Renderen von Text und Grafiken verwendet.</span><span class="sxs-lookup"><span data-stu-id="df382-105">Use this interface if the application uses GDI to render text and graphics.</span></span>

<span data-ttu-id="df382-106">Wenn Sie Anwendungen für Windows Vista oder spätere Versionen von Windows schreiben, sollten Sie die [XPS-Dokument-API](/previous-versions/windows/desktop/dd316976(v=vs.85)) und die [XPS-Druck-API](xps-printing.md) verwenden, um die leistungsstarken Grafik Schnittstellen zu verwenden, die von XPSDrv-Druckertreibern unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="df382-106">If you write applications for Windows Vista or later versions of Windows, consider using the [XPS Document API](/previous-versions/windows/desktop/dd316976(v=vs.85)) and the [XPS Print API](xps-printing.md) to use the higher-performance graphics interfaces that are supported by XPSDrv print drivers.</span></span>

<span data-ttu-id="df382-107">Dieser Abschnitt enthält Informationen zu den folgenden Themen.</span><span class="sxs-lookup"><span data-stu-id="df382-107">This section provides information about the following topics.</span></span>



| <span data-ttu-id="df382-108">Thema</span><span class="sxs-lookup"><span data-stu-id="df382-108">Topic</span></span>                                                                                             | <span data-ttu-id="df382-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="df382-109">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|---------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="df382-110">Informationen zur GDI-Druck-API</span><span class="sxs-lookup"><span data-stu-id="df382-110">About the GDI Print API</span></span>](about-the-gdi-print-api.md)<br/>                                 | <span data-ttu-id="df382-111">Eine Übersicht über die GDI-Druck Funktionalität.</span><span class="sxs-lookup"><span data-stu-id="df382-111">An overview of the GDI printing functionality.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [<span data-ttu-id="df382-112">Verwenden der GDI-Druck-API</span><span class="sxs-lookup"><span data-stu-id="df382-112">Using the GDI Print API</span></span>](using-the-printing-functions.md)<br/>                            | <span data-ttu-id="df382-113">Informationen zur Verwendung der GDI-Druck-API in einer Anwendung.</span><span class="sxs-lookup"><span data-stu-id="df382-113">Information about using the GDI Print API in an application.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| [<span data-ttu-id="df382-114">Referenz zur GDI-Druck-API</span><span class="sxs-lookup"><span data-stu-id="df382-114">GDI Print API Reference</span></span>](gdi-print-api-reference.md)<br/>                                 | <span data-ttu-id="df382-115">Ausführliche Beschreibungen der Funktionen, Strukturen und anderen Elemente der GDI-Druck-API.</span><span class="sxs-lookup"><span data-stu-id="df382-115">Detailed descriptions of the functions, structures, and other elements of the GDI Print API.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                               |
| [<span data-ttu-id="df382-116">Microsoft XPS Document Converter (mxdc)</span><span class="sxs-lookup"><span data-stu-id="df382-116">Microsoft XPS Document Converter (MXDC)</span></span>](microsoft-xps-document-converter--mxdc-.md)<br/> | <span data-ttu-id="df382-117">Der [Microsoft XPS Document Converter (mxdc)](microsoft-xps-document-converter--mxdc-.md) ist eine Komponente, die es Anwendungen ermöglicht, die GDI-Druck-API mit Druckern zu verwenden, die über einen XPSDrv-Druckertreiber verfügen.</span><span class="sxs-lookup"><span data-stu-id="df382-117">The [Microsoft XPS Document Converter (MXDC)](microsoft-xps-document-converter--mxdc-.md) is a component that enables applications to use the GDI Print API with printers that have an XPSDrv Print Driver.</span></span><br/>                                                                                                                                                                                                                                                                                               |
| [<span data-ttu-id="df382-118">Microsoft XPS Document Writer (MXDW)</span><span class="sxs-lookup"><span data-stu-id="df382-118">Microsoft XPS Document Writer (MXDW)</span></span>](microsoft-xps-document-writer.md)<br/>              | <span data-ttu-id="df382-119">Der [Microsoft XPS Document Writer (MXDW)](microsoft-xps-document-writer.md) bietet Anwendungen die Funktion "als XPS speichern" oder "in XPS exportieren".</span><span class="sxs-lookup"><span data-stu-id="df382-119">The [Microsoft XPS Document Writer (MXDW)](microsoft-xps-document-writer.md) provides applications with "save as XPS" or "export to XPS" functionality.</span></span> <span data-ttu-id="df382-120">Anwendungen, die keinen nativ XPS-Dokumentinhalt erstellen, können MXDW zum Erstellen von XPS-Dokument Dateien verwenden, ohne die [XPS-Dokument-API](/previous-versions/windows/desktop/dd316976(v=vs.85))zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="df382-120">Applications that do not natively create XPS document content can use the MXDW to create XPS document files without using the [XPS Document API](/previous-versions/windows/desktop/dd316976(v=vs.85)).</span></span> <span data-ttu-id="df382-121">Die XPS-Dokument-API bietet jedoch eine Anwendung mit der Möglichkeit, die von XPSDrv-Druckertreibern unterstützten Grafik Schnittstellen mit höherer Leistung zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="df382-121">The XPS Document API, however, provides an application with the ability to use the higher-performance graphics interfaces that are supported by XPSDrv print drivers.</span></span><br/> |



 

<span data-ttu-id="df382-122">Das folgende Diagramm zeigt die Beziehung zwischen der GDI-Druck-API und den anderen Druck-APIs, die von einer Anwendung verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="df382-122">The following diagram shows the relationship of the GDI Print API to the other print APIs that an application can use.</span></span>

![ein Diagramm, das die Beziehung zwischen der GDI-Druck-API und den anderen Druck-APIs anzeigt, die eine Win32-Anwendung verwenden kann](images/print-apis-gdi.png)

## <a name="related-topics"></a><span data-ttu-id="df382-124">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="df382-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="df382-125">**AddJob**</span><span class="sxs-lookup"><span data-stu-id="df382-125">**AddJob**</span></span>](addjob.md)
</dt> <dt>

<span data-ttu-id="df382-126">[XPS-Dokument-API](/previous-versions/windows/desktop/dd316976(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="df382-126">[XPS Document API](/previous-versions/windows/desktop/dd316976(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="df382-127">XPS-Druck-API</span><span class="sxs-lookup"><span data-stu-id="df382-127">XPS Print API</span></span>](xps-printing.md)
</dt> <dt>

[<span data-ttu-id="df382-128">Druckspoolerapi</span><span class="sxs-lookup"><span data-stu-id="df382-128">Print Spooler API</span></span>](print-spooler-api.md)
</dt> <dt>

[<span data-ttu-id="df382-129">Print Ticket-API</span><span class="sxs-lookup"><span data-stu-id="df382-129">Print Ticket API</span></span>](print-ticket-api.md)
</dt> </dl>

 

