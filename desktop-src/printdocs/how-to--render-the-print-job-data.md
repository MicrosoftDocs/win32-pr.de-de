---
description: In diesem Thema wird beschrieben, wie die zu druckenden Programm Daten dargestellt werden.
ms.assetid: D1343C53-6F13-49FF-8C7C-25D5A3C31B22
title: 'Gewusst wie: Rendering von Druckauftrags Daten'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f2d9f8cbf68394fd56ebcf31cfb37ee8f337f90
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868532"
---
# <a name="how-to-render-print-job-data"></a><span data-ttu-id="c236d-103">Gewusst wie: Rendering von Druckauftrags Daten</span><span class="sxs-lookup"><span data-stu-id="c236d-103">How To: Render Print Job Data</span></span>

<span data-ttu-id="c236d-104">In diesem Thema wird beschrieben, wie die zu druckenden Programm Daten dargestellt werden.</span><span class="sxs-lookup"><span data-stu-id="c236d-104">This topic describes how to render the program data to be printed.</span></span> <span data-ttu-id="c236d-105">In diesem Thema wird nicht ausführlich erläutert, wie bestimmte Grafiken oder Text Bilder dargestellt werden.</span><span class="sxs-lookup"><span data-stu-id="c236d-105">This topic does not explain in detail about how to render specific graphics or text images.</span></span> <span data-ttu-id="c236d-106">Stattdessen wird beschrieben, wie die Programm Daten verwaltet und als XPS-Dokument dargestellt werden, das über die [XPS-Druck-API](xps-printing.md)an einen Drucker gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="c236d-106">Instead, it describes how to manage the program data and render it as an XPS document, which it sends to a printer by using the [XPS Print API](xps-printing.md).</span></span>

## <a name="overview"></a><span data-ttu-id="c236d-107">Übersicht</span><span class="sxs-lookup"><span data-stu-id="c236d-107">Overview</span></span>

<span data-ttu-id="c236d-108">Das Rendern von Druckauftrags Daten für den Druck umfasst das übernehmen der Programm spezifischen Daten, z. b. Text, Bilder und Formatierung, und das Einfügen in ein Format, das mit dem Ziel Drucker kompatibel ist.</span><span class="sxs-lookup"><span data-stu-id="c236d-108">Rendering print job data for printing involves taking the program-specific data, such as text, images, and formatting, and converting them into a format that is compatible with the destination printer.</span></span> <span data-ttu-id="c236d-109">Das Programm, das die Daten an den Drucker sendet, muss es in dem Format senden, das der Druckertreiber benötigt.</span><span class="sxs-lookup"><span data-stu-id="c236d-109">The program that sends the data to the printer must send it in the format that the printer driver requires.</span></span>

<span data-ttu-id="c236d-110">Verwenden Sie die [XPS-Druck-API](xps-printing.md) , um die Daten an den Drucker zu senden, und Sie müssen die Daten als XPS-Dokument formatieren.</span><span class="sxs-lookup"><span data-stu-id="c236d-110">Use the [XPS Print API](xps-printing.md) to send the data to the printer and it requires the data to be formatted as an XPS document.</span></span> <span data-ttu-id="c236d-111">Zum Entwickeln des XPS-Dokument Inhalts, den die XPS-Druck-API benötigt, verwendet das Beispielprogramm die [XPS-Dokument-API](/previous-versions/windows/desktop/dd316976(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="c236d-111">To produce the XPS document content that the XPS Print API needs, the sample program uses the [XPS Document API](/previous-versions/windows/desktop/dd316976(v=vs.85)).</span></span>

<span data-ttu-id="c236d-112">Wenn der Programm Inhalt in einem Format vorliegt, das mit einem Drucker nicht kompatibel ist, muss es vor dem Senden an den Drucker gerendert werden.</span><span class="sxs-lookup"><span data-stu-id="c236d-112">If the program content is in a format that is not compatible with a printer, it will need to be rendered before it is sent to the printer.</span></span> <span data-ttu-id="c236d-113">Wenn das Programm den Programm Inhalt mithilfe der [XPS-Dokument-API](/previous-versions/windows/desktop/dd316976(v=vs.85)) verwaltet, wird der Programm Inhalt in einem Format angezeigt, das direkt an die [XPS-Druck-API](xps-printing.md) gesendet werden kann und kein zusätzliches Rendering erfordert, bevor es an den Drucker gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="c236d-113">If the program uses the [XPS Document API](/previous-versions/windows/desktop/dd316976(v=vs.85)) to manage its program content, the program content will be in a format that can be sent directly to the [XPS Print API](xps-printing.md) and will not require any additional rendering before you send it to the printer.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c236d-114">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="c236d-114">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="c236d-115">[XPS-Dokument-API](/previous-versions/windows/desktop/dd316976(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="c236d-115">[XPS Document API](/previous-versions/windows/desktop/dd316976(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="c236d-116">XPS-Druck-API</span><span class="sxs-lookup"><span data-stu-id="c236d-116">XPS Print API</span></span>](xps-printing.md)
</dt> </dl>

 

 
