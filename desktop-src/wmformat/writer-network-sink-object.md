---
title: Writer-netzwerksink-Objekt
description: Writer-netzwerksink-Objekt
ms.assetid: f7765b42-693a-4f48-b750-17579e860b6d
keywords:
- Windows Media-Format-SDK, Writer-netzwerksenkenobjekte
- Advanced Systems Format (ASF), Writer-netzwerksenkenobjekte
- ASF (Advanced Systems Format), Writer-netzwerksenkenobjekte
- Objekte, Writer-netzwerksenke-Objekte
- Writer-netzwerksink-Objekte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c85af356c1d326ddaaf3703ca87c3b7bdd1628b9
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/25/2020
ms.locfileid: "104101351"
---
# <a name="writer-network-sink-object"></a>Writer-netzwerksink-Objekt

Das Writer-netzwerksink-Objekt wird verwendet, um digitale Medien in ein Netzwerk zu schreiben.

Das Writer-netzwerksink-Objekt wird von der Funktion [**wmkreateschreiternetworksink**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatewriternetworksink)erstellt, mit der ein Zeiger auf eine **iwmschreiternetworksink** -Schnittstelle festgelegt wird. Die anderen Schnittstellen des Writer-netzwerksink-Objekts können durch Aufrufen der **QueryInterface** -Methode abgerufen werden.



| Schnittstelle                                              | BESCHREIBUNG                                                                                                                                                                                                     |
|--------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Iwmclientconnections**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmclientconnections)   | Sammelt Informationen zu verbundenen Clients.                                                                                                                                                                      |
| [**IWMClientConnections2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmclientconnections2) | Ruft erweiterte Client Informationen ab.                                                                                                                                                                          |
| [**Iwmregistercallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmregistercallback)     | Ermöglicht es der Anwendung, Statusmeldungen aus dem-Objekt zu erhalten.                                                                                                                                                 |
| [**Iwmschreiternetworksink**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriternetworksink)   | Öffnet und schließt Ports, legt die maximale Anzahl von Clients fest und ruft Sie ab, die eine Verbindung mit dem sink-Objekt herstellen können, legt das vom Writer-Objekt zu verwendende Netzwerkprotokoll fest und führt andere erweiterte Funktionen aus. |
| [**Iwmschreibsink**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwritersink)                 | Weist Arbeitsspeicher zu, bestimmt, ob die Senke in Echtzeit ausgeführt wird, und verarbeitet mehrere Rückruf Funktionen.                                                                                                |



 

Die folgende Rückruf Schnittstelle kann von der Anwendung implementiert werden, um den Fortschritt eines Writer-netzwerksink-Objekts zu verfolgen.



| Schnittstelle                                      | BESCHREIBUNG                                                                    |
|------------------------------------------------|--------------------------------------------------------------------------------|
| [**Iwmstatus Callback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstatuscallback) | Erforderlich, wenn Statusinformationen an die Host Anwendung übermittelt werden müssen. |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Übertragungen von ASF-Daten**](broadcasting-asf-data.md)
</dt> <dt>

[**Objekte**](objects.md)
</dt> <dt>

[**Arbeiten mit Writer-senken**](working-with-writer-sinks.md)
</dt> </dl>

 

 




