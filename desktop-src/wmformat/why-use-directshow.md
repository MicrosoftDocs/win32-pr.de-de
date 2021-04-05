---
title: Gründe für die Verwendung von DirectShow
description: Gründe für die Verwendung von DirectShow
ms.assetid: 0ab33526-73d0-425e-a03f-29c74555f578
keywords:
- Windows Media-Format-SDK, DirectShow
- Windows Media-Format-SDK, Hardware
- Windows Media-Format-SDK, Windows-Treibermodell (WDM)
- Advanced Systems Format (ASF), DirectShow
- ASF (Advanced Systems Format), DirectShow
- Advanced Systems Format (ASF), Hardware
- ASF (Advanced Systems Format), Hardware
- Advanced Systems Format (ASF), Windows-Treibermodell (WDM)
- ASF (Advanced Systems Format), Windows-Treibermodell (WDM)
- DirectShow, Informationen
- DirectShow, Hardware
- DirectShow, Windows-Treibermodell (WDM)
- Windows-Treibermodell (WDM)
- WDM (Windows-Treibermodell)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f90fa1de01a7b136b938f9b09cc7fb2b3c229fad
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103710373"
---
# <a name="why-use-directshow"></a>Gründe für die Verwendung von DirectShow

Es gibt zwei Hauptgründe, warum eine Anwendung DirectShow anstelle des Windows Media Format SDK direkt verwenden kann: aus Gründen der Bedienung der DirectShow-streamingarchitektur und für den Zugriff auf die Hardware.

## <a name="convenience"></a>Komfort

Mit der DirectShow-streamingarchitektur werden nur einige Methodenaufrufe zum Abspielen von Windows Media Audio-oder Windows Media Video Dateien benötigt. Das Erstellen von Dateien wird ebenfalls vereinfacht. Sie geben einfach ein Profil mithilfe der **iconfigasfwriter** -Schnittstelle für den Filter an, und DirectShow lädt automatisch die erforderlichen Komponenten zum Rendern oder Schreiben der Streams und stellt die Mechanismen für die Übertragung und Synchronisierung des Datenflusses von Mediendaten bereit. DirectShow ist besonders nützlich, wenn Inhalte aus verschiedenen Formaten in das Windows Media-Format umgewandelt werden. Sie können DirectShow-Filter Diagramme erstellen, die eine Vielzahl von Datei-und Komprimierungs Typen decodieren, und dann die decodierten Streams in den [WM-ASF-Writer](wm-asf-writer-filter.md) -Filter einblenden. Im Vergleich dazu funktioniert das uncompavitowmv-Beispiel in diesem SDK nur mit nicht komprimierten AVI-Dateien. Textstreams und beliebige Datenströme können auch über DirectShow erstellt und/oder gerendert werden. Dies erfordert jedoch möglicherweise die Erstellung benutzerdefinierter DirectShow-Filter für die Verarbeitung dieser Streams.

## <a name="access-to-hardware"></a>Zugriff auf Hardware

DirectShow ist die einzige Möglichkeit für den Anwendungscode, auf Windows-Treibermodell (WDM) – basierte Hardware Geräte wie 1394 DV-Kameras, TV-Tuners und USB-Webcams zuzugreifen. Wenn Ihre Anwendung Daten direkt von einem WDM-basierten Hardware Gerät erfassen und in das Windows Media-Format transcodieren muss und das Windows Media Encoder SDK nicht Ihren Anforderungen entspricht, ist DirectShow die einzige Alternative. DirectShow kann auch für den Zugriff auf ältere Geräte auf der Grundlage von Video für Windows verwendet werden.

 

 




