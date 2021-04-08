---
title: XML-Puffer
description: Ein XML-Puffer stellt einen effizienten Speicher internen Speicher für beliebige XML-Daten bereit.
ms.assetid: e379628b-c6f8-48b1-8109-59fb604f2bcb
keywords:
- XML-Puffer-Webdienste für Windows
- Wwsapi
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab71121dc451c9ccb186c754d537836f9e899fa9
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/04/2020
ms.locfileid: "103949233"
---
# <a name="xml-buffer"></a>XML-Puffer

Ein XML-Puffer stellt einen effizienten Speicher internen Speicher für beliebige XML-Daten bereit.


Verwenden Sie zum Lesen von Daten aus einem XML-Puffer einen [XML-Reader](xml-reader.md) , und nennen Sie [**wssetinputesbuffer**](/windows/desktop/api/WebServices/nf-webservices-wssetinputtobuffer) mit dem XML-Puffer. Der Reader wird am Anfang des Dokuments positioniert.

Verwenden Sie zum Einfügen von Daten in einen Puffer einen [XML-Writer](xml-writer.md) , und nennen Sie [**wssetoutputstobuffer**](/windows/desktop/api/WebServices/nf-webservices-wssetoutputtobuffer) mit dem XML-Puffer. Der Writer wird am Ende des Dokuments positioniert.

Nachdem ein Reader auf einen XML-Puffer festgelegt wurde, kann er zusätzlich zu allen XML-Reader-APIs [**verwendet werden,**](/windows/desktop/api/WebServices/nf-webservices-wsmovereader) um den Reader durch das Dokument zu navigieren. [**Wsgetreaderposition**](/windows/desktop/api/WebServices/nf-webservices-wsgetreaderposition) und [**wssetreaderposition**](/windows/desktop/api/WebServices/nf-webservices-wssetreaderposition) können auch verwendet werden, um eine Position im Dokument aufzuzeichnen und zu einem späteren Zeitpunkt zurückzukehren.

Nachdem ein Writer auf einen XML-Puffer festgelegt wurde, kann [**wsmovewriter**](/windows/desktop/api/WebServices/nf-webservices-wsmovewriter) zusätzlich zu allen XML-Writer-APIs verwendet werden, um im Writer durch das Dokument zu navigieren. [**Wsgetschreiterposition**](/windows/desktop/api/WebServices/nf-webservices-wsgetwriterposition) und [**wssetschreiterposition**](/windows/desktop/api/WebServices/nf-webservices-wssetwriterposition) können auch verwendet werden, um eine Position im Dokument aufzuzeichnen und zu einem späteren Zeitpunkt zurückzukehren. Der Writer fügt immer Daten vor dem Knoten ein, auf dem er positioniert ist.

Knoten können aus dem XML-Puffer gelöscht werden, indem Sie die Position des Knotens mithilfe von [**wsgetreaderposition**](/windows/desktop/api/WebServices/nf-webservices-wsgetreaderposition) oder [**wsgetschreiterposition**](/windows/desktop/api/WebServices/nf-webservices-wsgetwriterposition) abrufen und dann [**wsremovenode**](/windows/desktop/api/WebServices/nf-webservices-wsremovenode) mit dieser Position aufrufen. Bei-Elementen wird dadurch das-Element, alle seine untergeordneten Elemente einschließlich des entsprechenden End-Elements gelöscht.

Eine Position wird durch die Position des Werts der [**WS- \_ XML- \_ Knoten \_**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_node_position)dargestellt. Positionen sind spezifisch für einen bestimmten XML-Puffer und sind nur gültig, solange der XML-Puffer gültig ist.

Die folgenden Enumerationen werden mit XML-Puffern verwendet:

-   [**WS- \_ Verschiebung \_ zu**](/windows/desktop/api/WebServices/ne-webservices-ws_move_to)
-   [**Eigenschaften-ID der WS XML- \_ \_ Puffer \_ \_**](/windows/win32/api/webservices/ne-webservices-ws_xml_reader_property_id)

Die folgenden Funktionen werden für XML-Puffer verwendet:

-   [**Wscreatexmlbuffer**](/windows/desktop/api/WebServices/nf-webservices-wscreatexmlbuffer)
-   [**Wsremovenode**](/windows/desktop/api/WebServices/nf-webservices-wsremovenode)

Das folgende Handle wird für XML-Puffer verwendet:

-   [WS- \_ XML- \_ Puffer](ws-xml-buffer.md)

Die folgenden Strukturen werden mit XML-Puffern verwendet:

-   [**WS \_ XML- \_ Puffer ( \_ Eigenschaft)**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_buffer_property)
-   [**WS- \_ XML- \_ Knoten \_ Position**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_node_position)

 

 




