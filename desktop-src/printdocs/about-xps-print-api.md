---
description: Die XPS-&\# 160; Drucken&\# 160; Die API stellt eine Schnittstelle zum Druck Spooler bereit, mit der Anwendungen Aufträge drucken können, die XPS-Dokumente an einen Drucker senden.
ms.assetid: d3bf7b1d-df21-4e7b-803b-45b65d46b2ca
title: Informationen zur XPS-Druck-API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b1467458a737a6faaddb5ed45c81623207ccdb2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131604"
---
# <a name="about-the-xps-print-api"></a><span data-ttu-id="9620e-103">Informationen zur XPS-Druck-API</span><span class="sxs-lookup"><span data-stu-id="9620e-103">About the XPS Print API</span></span>

<span data-ttu-id="9620e-104">Die [XPS-Druck-API](xps-printing.md) stellt eine Schnittstelle zum Druck Spooler bereit, mit der Anwendungen Aufträge drucken können, die XPS-Dokumente an einen Drucker senden.</span><span class="sxs-lookup"><span data-stu-id="9620e-104">The [XPS Print API](xps-printing.md) provides an interface to the print spooler that applications can use to print jobs that send XPS documents to a printer.</span></span>

<span data-ttu-id="9620e-105">Wenn der Ziel Drucker einen XPSDrv-Druckertreiber verwendet, ermöglicht die XPS-Druck-API dem XPSDrv-Druckertreiber, Dokument Ereignisse zu empfangen, während der Druck Spooler einen Druckauftrag verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="9620e-105">If the destination printer uses an XPSDrv printer driver, the XPS Print API makes it possible for the XPSDrv printer driver to receive document events as the print spooler processes a print job.</span></span> <span data-ttu-id="9620e-106">Eine Beschreibung der Dokument Ereignisse, die an den XPSDrv-Druckertreiber gesendet werden, finden Sie unter [XPS-Treiber Dokument Ereignisse](/windows-hardware/drivers/print/xps-driver-document-events).</span><span class="sxs-lookup"><span data-stu-id="9620e-106">For a description of the document events that are sent to the XPSDrv printer driver see [XPS Driver Document Events](/windows-hardware/drivers/print/xps-driver-document-events).</span></span>

<span data-ttu-id="9620e-107">Wenn der Ziel Drucker einen GDI-Druckertreiber verwendet, ermöglicht die [XPS-Druck-API](xps-printing.md) dem System, die erforderliche Konvertierung der Druckauftrags Daten aus dem XPS-Format in das EMF-Format (Enhanced Metafile), das der GDI-Druckertreiber verwendet, zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="9620e-107">If the destination printer uses a GDI printer driver, the [XPS Print API](xps-printing.md) lets the system handle the necessary conversion of the print job data from XPS format to the Enhanced Metafile (EMF) format that the GDI printer driver uses.</span></span> <span data-ttu-id="9620e-108">Eine Beschreibung der GDI-Druckertreiber-Dokument Ereignisse finden Sie unter [DocumentEvent-Funktion](documentevent.md).</span><span class="sxs-lookup"><span data-stu-id="9620e-108">For a description of the GDI printer driver document events see [DocumentEvent Function](documentevent.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="9620e-109">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="9620e-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9620e-110">Verwenden der XPS-Druck-API</span><span class="sxs-lookup"><span data-stu-id="9620e-110">Using the XPS Print API</span></span>](using-the-xps-print-api.md)
</dt> <dt>

[<span data-ttu-id="9620e-111">XPS-Druck-API-Referenz</span><span class="sxs-lookup"><span data-stu-id="9620e-111">XPS Print API Reference</span></span>](xpsprint-api.md)
</dt> </dl>

 

 
