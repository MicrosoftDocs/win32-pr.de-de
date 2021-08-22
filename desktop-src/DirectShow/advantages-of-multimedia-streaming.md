---
description: Vorteile des Multimediastreamings
ms.assetid: 01020ad5-430d-4b4d-8de3-bcc81270e132
title: Vorteile des Multimediastreamings
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06df23ce833462aee9b7d4b3840c1fae2d4f3b15c4ee6daee2e4a421259493a6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119537540"
---
# <a name="advantages-of-multimedia-streaming"></a>Vorteile des Multimediastreamings

> [!Note]  
> Diese APIs sind veraltet. Anwendungen sollten den [**Sample Grabber-Filter**](sample-grabber-filter.md) verwenden oder einen benutzerdefinierten Filter implementieren, um Daten aus einem DirectShow-Filterdiagramm zu erhalten.

 

Wenn Entwickler Multimediastreaming in ihren Anwendungen verwenden, reduziert dies die Menge der erforderlichen formatspezifischen Programmierung deutlich. In der Regel muss eine Anwendung, die Mediendaten aus einer Datei oder Hardwarequelle abrufen muss, alles über das Datenformat und das Hardwaregerät wissen. Die Anwendung muss die Verbindung, die Übertragung von Daten, die erforderliche Datenkonvertierung und das tatsächliche Datenrendering oder die Dateispeicherung verarbeiten. Da sich jedes Format und Gerät leicht unterscheiden, ist dieser Prozess oft komplex und umständlich. Multimediastreaming hingegen handelt automatisch die Übertragung und Konvertierung von Daten von der Quelle in die Anwendung aus. Die Streamingschnittstellen bieten eine einheitliche und vorhersagbare Methode für den Datenzugriff und die Datensteuerung, die es einer Anwendung erleichtert, die Daten unabhängig von der ursprünglichen Quelle oder dem ursprünglichen Format wieder zu verwenden.

In den folgenden Schritten wird gezeigt, wie Sie das Streaming vom Hardwaregerät zur gerenderten Wiedergabe implementieren.

1.  Eine Quelle von Videodaten, z. B. DirectShow, macht die Streamingschnittstellen verfügbar.
2.  Der Anwendungsentwickler verwendet die Multimediastreamingschnittstellen, um die Datenformatkonvertierung zu verarbeiten.
3.  Der Anwendungsentwickler verwendet die DirectDraw-Schnittstellen, um die resultierenden Daten zu rendern.

Die Spezifikation für Multimediastreams umfasst mehrere Schnittstellen. Jede Schnittstelle enthält Methoden, die einen bestimmten Aspekt des Streamingprozesses steuern oder einen bestimmten Datentyp verarbeiten. Weitere [Informationen finden Sie unter Liste der Multimedia-Streamingschnittstellen.](list-of-multimedia-streaming-interfaces.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Informationen zur Multimediastreamingarchitektur](about-the-multimedia-streaming-architecture.md)
</dt> </dl>

 

 



