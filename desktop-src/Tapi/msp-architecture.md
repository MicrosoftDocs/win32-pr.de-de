---
description: In der TAPI-Architektur werden alle TSPs im Kontext von TAPISRV ausgeführt, das als Dienstprozess in SVCHOST implementiert wird.
ms.assetid: f47662f9-2fca-4044-ab26-617e5b1f9eae
title: MSP-Architektur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7cf5d95cf568e17b53c575f6c2f8963baa4b698cc69243ee1a23e9306ad6b31
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119002848"
---
# <a name="msp-architecture"></a>MSP-Architektur

In der TAPI-Architektur werden alle TSPs im Kontext von TAPISRV ausgeführt, das als Dienstprozess in SVCHOST implementiert wird. TAPI-Anwendungen werden in einem eigenen Prozess verwendet. TAPI-Anwendungen laden Tapi3.dll und alle erforderlichen MSPs in ihren eigenen Prozess, und die TAPI-DLL kommuniziert über eine private RPC-Schnittstelle mit TAPISRV. Das folgende Diagramm veranschaulicht die Interaktion dieser Komponenten.

![Interaktionen zwischen tapisrv, tapi-Anwendungen und msps](images/tsp-msp1.png)

Ein Mediendienstanbieter (Media Service Provider, MSP) stellt Medienstreaming mithilfe der Abstraktionen von Terminals, Streams und SubStreams bereit.

Ein Terminal ist eine Senke oder Quelle für einen Medienstream. Es kann sich um ein physisches Objekt, z. B. einen Lautsprecher oder ein Mikrofon, oder um eine Abstraktion eines Geräts, z. B. ein Videofenster, sein. Das [Terminalobjekt](terminal-object.md) macht die [**ITTerminal-Schnittstelle**](/windows/win32/api/tapi3if/nn-tapi3if-itterminal) verfügbar. Die Terminalklasse wird durch [](terminal-class.md) die Terminalklassen-GUID beschrieben. Ein MSP kann eigene Terminalklassen definieren.

Streams Die Medien eines Aufrufs werden [](tapimediatype--constants.md) basierend auf dem Medientyp [](/windows/desktop/api/Tapi3if/ne-tapi3if-terminal_direction)oder -typ, der Streamrichtung und der Zieladresse des Mediums dividiert. Beispielsweise ist ein eingehender Audiostream von einem Modem ein Datenstromobjekt, ein ausgehender Videodatenstrom an eine IP-Adresse und port ist ein Streamobjekt. Die Videostreams, die aus einer IP-Multicastgruppe kommen, werden ebenfalls als ein Streamobjekt betrachtet. Das Stream-Objekt wird durch die [**ITStreamControl-Schnittstelle**](/windows/win32/api/tapi3if/nn-tapi3if-itstreamcontrol) dargestellt.

SubStreams ermöglichen eine feineren Kontrolle über die Medien. Im Fall von IP-Multicast kann das eingehende Videostreamobjekt beispielsweise mehrere Personen darstellen. Die Anwendung möchte wahrscheinlich, dass jeder Teilnehmer über einen separaten Renderer verfügen soll. Der eingehende Videostream kann in mehrere Unterstreams unterteilt werden, einen für jede Person. Ein Unterstream würde einer Person entsprechen und kann separat konfiguriert und gesteuert werden. Das SubStream-Objekt wird durch die [**ITSubStreamControl-Schnittstelle**](/windows/win32/api/tapi3if/nn-tapi3if-itsubstreamcontrol) dargestellt.

Wenn eine Anwendung [**ITAddress::CreateCall**](/windows/desktop/api/tapi3if/nf-tapi3if-itaddress-createcall) aufruft, um einen Aufruf festzulegen, muss sie den erforderlichen Medientyp angeben. Bei einem ausgehenden Anruf wird TAPI einfach informiert, wenn der Aufruf erstellt wird. Beispiel:

``` syntax
HRESULT hr = pAddress->CreateCall( 
       pszDestAddress, 
       lAddressType, 
       TAPIMEDIATYPE_AUDIO | TAPIMEDIATYPE_VIDEO, 
       &pCall 
       ); 
// If (hr != S_OK ) process the error here
```

In diesem Fall erstellt die Anwendung einen ausgehenden Audiovideoaufruf.

Die übergebenen Medientypen geben die Medien an, an denen die Anwendung während der Lebensdauer des Aufrufs interessiert ist. Beispielsweise kann die Anwendung Audio- und Videodaten beim Erstellen des Anrufs angeben, aber nur Audioterminals am Anfang auswählen. Der MSP startet nur das Streaming von Audiodaten, lehnt jedoch keine lokale oder Remotevideoanforderung ab, die später während der Lebensdauer des Aufrufs erfolgt ist.

Wenn die Anwendung dann [**ITBasicCallControl::Verbinden aufruft,**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-connect)ruft TAPI 3 [**TSPI \_ lineMakeCall**](/windows/win32/api/tspi/nf-tspi-tspi_linemakecall) im TSP auf. Nachdem ein Aufruf eingerichtet wurde, können MSP und TSP nach Bedarf kommunizieren.

Wenn die Verbindung eines Anrufs getrennt wird, müssen der MSP und der TSP über das Entfernen des Anrufs kommunizieren. Tapi3.dll wird [**TSPI \_ lineDrop aufrufen,**](/windows/win32/api/tspi/nf-tspi-tspi_linedrop) wenn die Anwendung [**Disconnect aufruft.**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-disconnect)

 

 
