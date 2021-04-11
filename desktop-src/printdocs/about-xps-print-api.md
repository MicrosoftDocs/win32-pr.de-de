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
# <a name="about-the-xps-print-api"></a>Informationen zur XPS-Druck-API

Die [XPS-Druck-API](xps-printing.md) stellt eine Schnittstelle zum Druck Spooler bereit, mit der Anwendungen Aufträge drucken können, die XPS-Dokumente an einen Drucker senden.

Wenn der Ziel Drucker einen XPSDrv-Druckertreiber verwendet, ermöglicht die XPS-Druck-API dem XPSDrv-Druckertreiber, Dokument Ereignisse zu empfangen, während der Druck Spooler einen Druckauftrag verarbeitet. Eine Beschreibung der Dokument Ereignisse, die an den XPSDrv-Druckertreiber gesendet werden, finden Sie unter [XPS-Treiber Dokument Ereignisse](/windows-hardware/drivers/print/xps-driver-document-events).

Wenn der Ziel Drucker einen GDI-Druckertreiber verwendet, ermöglicht die [XPS-Druck-API](xps-printing.md) dem System, die erforderliche Konvertierung der Druckauftrags Daten aus dem XPS-Format in das EMF-Format (Enhanced Metafile), das der GDI-Druckertreiber verwendet, zu verarbeiten. Eine Beschreibung der GDI-Druckertreiber-Dokument Ereignisse finden Sie unter [DocumentEvent-Funktion](documentevent.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden der XPS-Druck-API](using-the-xps-print-api.md)
</dt> <dt>

[XPS-Druck-API-Referenz](xpsprint-api.md)
</dt> </dl>

 

 
