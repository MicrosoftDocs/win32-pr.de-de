---
description: Xps&\# 160; Druck&\# 160; Die API stellt eine Schnittstelle für den Druckspooler bereit, mit der Anwendungen Aufträge drucken können, die XPS-Dokumente an einen Drucker senden.
ms.assetid: d3bf7b1d-df21-4e7b-803b-45b65d46b2ca
title: Informationen zur XPS-Druck-API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e43c0bde59424c220e3d3ea9eab4b4780ace425cab28882013853a72d422815
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119950860"
---
# <a name="about-the-xps-print-api"></a>Informationen zur XPS-Druck-API

Die [XPS-Druck-API](xps-printing.md) stellt eine Schnittstelle für den Druckspooler bereit, mit dem Anwendungen Aufträge drucken können, die XPS-Dokumente an einen Drucker senden.

Wenn der Zieldrucker einen XPSDrv-Druckertreiber verwendet, ermöglicht die XPS-Druck-API dem XPSDrv-Druckertreiber das Empfangen von Dokumentereignissen, während der Druckspooler einen Druckauftrag verarbeitet. Eine Beschreibung der Dokumentereignisse, die an den XPSDrv-Druckertreiber gesendet werden, finden Sie unter [XPS Driver Document Events](/windows-hardware/drivers/print/xps-driver-document-events).

Wenn der Zieldrucker einen GDI-Druckertreiber verwendet, kann das System mit der [XPS-Druck-API](xps-printing.md) die erforderliche Konvertierung der Druckauftragsdaten vom XPS-Format in das EMF-Format (Enhanced Metafile) verarbeiten, das vom GDI-Druckertreiber verwendet wird. Eine Beschreibung der Dokumentereignisse des GDI-Druckertreibers finden Sie unter [DocumentEvent-Funktion](documentevent.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden der XPS-Druck-API](using-the-xps-print-api.md)
</dt> <dt>

[XPS-Druck-API-Referenz](xpsprint-api.md)
</dt> </dl>

 

 
