---
title: Writer-Netzwerksenkenobjekt
description: Writer-Netzwerksenkenobjekt
ms.assetid: f7765b42-693a-4f48-b750-17579e860b6d
keywords:
- Windows Medienformat-SDK, Writer-Netzwerksenkenobjekte
- Advanced Systems Format (ASF),Writer-Netzwerksenkenobjekte
- ASF (Advanced Systems Format), Writer-Netzwerksenkenobjekte
- Objekte,Writer-Netzwerksenkenobjekte
- Writer-Netzwerksenkenobjekte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2011fd161fc4ac5e1cd03d955f06259e6499e343970cc309b1e8c41db051a32
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117843725"
---
# <a name="writer-network-sink-object"></a>Writer-Netzwerksenkenobjekt

Das Writer-Netzwerksenkenobjekt wird verwendet, um digitale Medien in ein Netzwerk zu schreiben.

Das Writer-Netzwerksenkenobjekt wird von der [**Funktion WMCreateWriterNetworkSink**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatewriternetworksink)erstellt, die einen Zeiger auf eine **IWMWriterNetworkSink-Schnittstelle** legt. Die anderen Schnittstellen des Writer-Netzwerksenkenobjekts können durch Aufrufen der **QueryInterface-Methode ermittelt** werden.



| Schnittstelle                                              | Beschreibung                                                                                                                                                                                                     |
|--------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IWMClientConnections**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmclientconnections)   | Sammelt Informationen zu verbundenen Clients.                                                                                                                                                                      |
| [**IWMClientConnections2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmclientconnections2) | Ruft erweiterte Clientinformationen ab.                                                                                                                                                                          |
| [**IWMRegisterCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmregistercallback)     | Ermöglicht es der Anwendung, Statusmeldungen aus dem -Objekt zu erhalten.                                                                                                                                                 |
| [**IWMWriterNetworkSink**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriternetworksink)   | Öffnet und schließt Ports, legt die maximale Anzahl von Clients fest, die eine Verbindung mit dem Senkenobjekt herstellen können, legt das Netzwerkprotokoll fest, das vom Writerobjekt verwendet werden soll, und führt andere erweiterte Funktionen aus. |
| [**IWMWriterSink**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwritersink)                 | Weist Arbeitsspeicher zu, bestimmt, ob die Senke in Echtzeit ausgeführt wird, und verarbeitet mehrere Rückruffunktionen.                                                                                                |



 

Die folgende Rückrufschnittstelle kann von der Anwendung implementiert werden, um den Fortschritt eines Writernetzwerksenkenobjekts zu verfolgen.



| Schnittstelle                                      | Beschreibung                                                                    |
|------------------------------------------------|--------------------------------------------------------------------------------|
| [**IWMStatusCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstatuscallback) | Erforderlich, wenn Statusinformationen an die Hostanwendung übermittelt werden müssen. |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Übertragungen von ASF-Daten**](broadcasting-asf-data.md)
</dt> <dt>

[**Objekte**](objects.md)
</dt> <dt>

[**Arbeiten mit Writer-Senken**](working-with-writer-sinks.md)
</dt> </dl>

 

 




