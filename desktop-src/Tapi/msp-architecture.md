---
description: In der TAPI-Architektur werden alle TSPS im Kontext von tapisrv ausgeführt, der als Dienst Prozess in svchost implementiert ist.
ms.assetid: f47662f9-2fca-4044-ab26-617e5b1f9eae
title: MSP-Architektur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8c1229ddce90f79c122c47572b4567d230b0b4e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104393334"
---
# <a name="msp-architecture"></a>MSP-Architektur

In der TAPI-Architektur werden alle TSPS im Kontext von tapisrv ausgeführt, der als Dienst Prozess in svchost implementiert ist. TAPI-Anwendungen Leben in Ihrem eigenen Prozess. TAPI-Anwendungen laden Tapi3.dll und alle benötigten MSPs in ihren eigenen Prozess, und die TAPI-dll kommuniziert mit tapisrv über eine private RPC-Schnittstelle. Im folgenden Diagramm wird die Interaktion dieser Komponenten veranschaulicht.

![Interaktionen zwischen tapisrv, TAPI-Anwendungen und MSPs](images/tsp-msp1.png)

Ein Medien Dienstanbieter (MSP) stellt Medien Streaming mithilfe der Abstraktionen von Terminals, Streams und unter strömen bereit.

Ein Terminal ist eine Senke oder Quelle für einen Mediendaten Strom. Dabei kann es sich um ein physisches Objekt handeln, z. b. einen Redner oder ein Mikrofon, oder es kann eine Abstraktion eines Geräts sein, z. b. ein Videofenster. Das [Terminal Objekt](terminal-object.md) macht die [**itterminal**](/windows/win32/api/tapi3if/nn-tapi3if-itterminal) -Schnittstelle verfügbar. Die Terminal Klasse wird durch die GUID der [**Terminal Klasse**](terminal-class.md) beschrieben. Ein MSP kann seine eigenen Terminal Klassen definieren.

Streams dividiert die Medien eines Aufrufes basierend auf dem [**Medientyp**](tapimediatype--constants.md) oder-Typ, der [**Richtung**](/windows/desktop/api/Tapi3if/ne-tapi3if-terminal_direction)des Streams und der Zieladresse des Mediums. Ein eingehender Audiostream von einem Modem ist beispielsweise ein Streamobjekt, ein ausgehender Videostream zu einer IP-Adresse und ein Port ist ein Datenstrom Objekt. die Videostreams aus einer IP-Multicast Gruppe werden ebenfalls als ein Streamobjekt betrachtet. Das Stream-Objekt wird durch die [**itstreamcontrol**](/windows/win32/api/tapi3if/nn-tapi3if-itstreamcontrol) -Schnittstelle dargestellt.

Unter Ströme ermöglichen eine präzisere Steuerung des Mediums. Im Fall von IP-Multicast könnte das eingehende videostreamobjekt beispielsweise mehrere Personen darstellen. Die Anwendung möchte wahrscheinlich, dass jeder Teilnehmer über einen separaten Renderer verfügt. Der eingehende Videostream kann in mehrere unter Ströme aufgeteilt werden, eine für jede Person. Ein untergeordneter Stream würde einer Person entsprechen und kann separat konfiguriert und gesteuert werden. Das substream-Objekt wird durch die [**itsubstreamcontrol**](/windows/win32/api/tapi3if/nn-tapi3if-itsubstreamcontrol) -Schnittstelle dargestellt.

Wenn eine Anwendung [**itaddress:: anatecall**](/windows/desktop/api/tapi3if/nf-tapi3if-itaddress-createcall) aufruft, um einen Aufruf einzurichten, muss Sie den Typ des erforderlichen Mediums angeben. Bei einem ausgehenden-Befehl weist er nur TAPI an, wenn der-Befehl erstellt wird. Beispiel:

``` syntax
HRESULT hr = pAddress->CreateCall( 
       pszDestAddress, 
       lAddressType, 
       TAPIMEDIATYPE_AUDIO | TAPIMEDIATYPE_VIDEO, 
       &pCall 
       ); 
// If (hr != S_OK ) process the error here
```

In diesem Fall erstellt die Anwendung einen ausgehenden audiovideobefehl.

Die übergebenen Medientypen geben das Medium an, an dem die Anwendung über die Lebensdauer des Aufrufes interessiert ist. Die Anwendung kann z. b. Audioinformationen und Videos beim Erstellen des Aufrufes angeben. Wählen Sie jedoch am Anfang nur audioterminals aus. Das MSP startet nur Streaming-Audiodaten, lehnt jedoch eine lokale oder Remote-Video Anforderung ab, die zu einem späteren Zeitpunkt während der Lebensdauer des Aufrufes ausgeführt wird.

Wenn die Anwendung dann [**itbasiccallcontrol:: Connect**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-connect)aufruft, ruft TAPI 3 [**TSPI \_ linemakecall**](/windows/win32/api/tspi/nf-tspi-tspi_linemakecall) im TSP auf. Nachdem ein-Rückruf eingerichtet wurde, können MSP und TSP bei Bedarf kommunizieren.

Wenn eine Verbindung getrennt wird, liegt es an den MSP-und TSP, um über das Beenden des Aufrufens zu kommunizieren. Tapi3.dll wird [**TSPI \_ linedrop**](/windows/win32/api/tspi/nf-tspi-tspi_linedrop) aufrufen, wenn die Anwendung [**Disconnect**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-disconnect)aufruft.

 

 
