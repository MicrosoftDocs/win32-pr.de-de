---
title: XML-Puffer
description: Ein XML-Puffer bietet effizienten In-Memory-Speicher für beliebige XML-Daten.
ms.assetid: e379628b-c6f8-48b1-8109-59fb604f2bcb
keywords:
- XML-Pufferwebdienste für Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3bcd4e4725f2ad3345dcef7c33b694a8e327f4d8a6c43fbce39f9c57babfa467
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118192336"
---
# <a name="xml-buffer"></a>XML-Puffer

Ein XML-Puffer bietet effizienten In-Memory-Speicher für beliebige XML-Daten.


Verwenden Sie zum Lesen von Daten aus einem XML-Puffer einen [XML-Reader,](xml-reader.md) und rufen [**Sie WsSetInputToBuffer**](/windows/desktop/api/WebServices/nf-webservices-wssetinputtobuffer) mit dem XML-Puffer auf. Der Reader wird am Anfang des Dokuments positioniert.

Verwenden Sie zum Einfügen von Daten in einen Puffer einen [XML-Writer,](xml-writer.md) und rufen [**Sie WsSetOutputToBuffer**](/windows/desktop/api/WebServices/nf-webservices-wssetoutputtobuffer) mit dem XML-Puffer auf. Der Writer wird am Ende des Dokuments positioniert.

Sobald ein Reader auf einen XML-Puffer festgelegt wurde, kann zusätzlich zu allen XML-Reader-APIs [**WsMoveReader**](/windows/desktop/api/WebServices/nf-webservices-wsmovereader) verwendet werden, um den Reader durch das Dokument zu navigieren. [**WsGetReaderPosition**](/windows/desktop/api/WebServices/nf-webservices-wsgetreaderposition) und [**WsSetReaderPosition**](/windows/desktop/api/WebServices/nf-webservices-wssetreaderposition) können auch verwendet werden, um eine Position im Dokument zu erfassen und später wieder zu ihr zurückzukehren.

Sobald ein Writer auf einen XML-Puffer festgelegt wurde, kann zusätzlich zu allen XML Writer-APIs [**WsMoveWriter**](/windows/desktop/api/WebServices/nf-webservices-wsmovewriter) verwendet werden, um den Writer durch das Dokument zu navigieren. [**WsGetWriterPosition**](/windows/desktop/api/WebServices/nf-webservices-wsgetwriterposition) und [**WsSetWriterPosition**](/windows/desktop/api/WebServices/nf-webservices-wssetwriterposition) können auch verwendet werden, um eine Position im Dokument zu erfassen und später wieder zu ihr zurückzukehren. Der Writer fügt Daten immer vor dem Knoten ein, auf dem er positioniert ist.

Knoten können aus dem XML-Puffer gelöscht werden, indem sie die Position des Knotens mit [**WsGetReaderPosition**](/windows/desktop/api/WebServices/nf-webservices-wsgetreaderposition) oder [**WsGetWriterPosition**](/windows/desktop/api/WebServices/nf-webservices-wsgetwriterposition) abrufen und [**dann WsRemoveNode**](/windows/desktop/api/WebServices/nf-webservices-wsremovenode) mit dieser Position aufrufen. Bei -Elementen löscht dies das -Element, alle seine unteren Elemente, einschließlich des übereinstimmenden Endelements.

Eine Position wird durch den Wert [**WS \_ XML NODE \_ POSITION \_ dargestellt.**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_node_position) Positionen sind spezifisch für einen bestimmten XML-Puffer und nur gültig, solange der XML-Puffer gültig ist.

Die folgenden Enumerationen werden mit XML-Puffern verwendet:

-   [**WS \_ MOVE \_ TO**](/windows/desktop/api/WebServices/ne-webservices-ws_move_to)
-   [**\_ \_ \_ WS-XML-PUFFEREIGENSCHAFTS-ID \_**](/windows/win32/api/webservices/ne-webservices-ws_xml_reader_property_id)

Die folgenden Funktionen werden mit XML-Puffern verwendet:

-   [**WsCreateXmlBuffer**](/windows/desktop/api/WebServices/nf-webservices-wscreatexmlbuffer)
-   [**WsRemoveNode**](/windows/desktop/api/WebServices/nf-webservices-wsremovenode)

Das folgende Handle wird mit XML-Puffern verwendet:

-   [WS \_ XML \_ BUFFER](ws-xml-buffer.md)

Die folgenden Strukturen werden mit XML-Puffern verwendet:

-   [**WS \_ XML \_ \_ BUFFER-EIGENSCHAFT**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_buffer_property)
-   [**\_WS-XML-KNOTENPOSITION \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_node_position)

 

 




