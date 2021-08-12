---
description: Grundlegende Multimediastreamingschnittstellen
ms.assetid: a94dbb64-dfca-4c24-8c11-761835faf8a8
title: Grundlegende Multimediastreamingschnittstellen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de5268855231169c6c0a7ffab02aa5145a7c1813511421b04b2420773e1588ff
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118662920"
---
# <a name="base-multimedia-streaming-interfaces"></a>Grundlegende Multimediastreamingschnittstellen

> [!Note]  
> Diese APIs sind veraltet. Anwendungen sollten den [**Beispielgrabberfilter**](sample-grabber-filter.md) verwenden oder einen benutzerdefinierten Filter implementieren, um Daten aus einem DirectShow-Filterdiagramm abzurufen.

 

Die grundlegenden Multimediastreamingschnittstellen bieten eine programmgesteuerte Möglichkeit, auf Multimediastreams zuzugreifen. Die Verwendung einer Basisschnittstelle für den Zugriff auf einen bestimmten Datentyp kann jedoch die Kontrolle über die Daten einschränken. Daher sollten Medienentwickler abgeleitete Versionen dieser Schnittstellen erstellen, die eine leistungsfähigere Kontrolle über die eindeutigen Funktionen ihres Medientyps bieten.



| Schnittstelle                                      | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                           |
|------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IMultiMediaStream**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imultimediastream) | Definiert, wie auf das Multimediastreamobjekt der höchsten Ebene zugegriffen wird. Dieses Objekt enthält und ermöglicht den Zugriff auf andere Streamobjekte. [**IMultiMediaStream**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imultimediastream) verfügt über Methoden, die bestimmte Streams aufzählen oder abrufen sowie die Gesamtdauer des Streams überprüfen und innerhalb des Streams suchen.                                                                                                       |
| [**IMediaStream**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imediastream)           | Definiert ein generisches Streamobjekt. Verwenden Sie die zugehörigen Methoden, um einen Zeiger auf den Stream abzurufen, Informationen zum Stream abzurufen und Beispiele aus den Streamdaten zu erstellen. Sie können auch freigegebene Streambeispiele erstellen, auf die mehrere Streams zugreifen können, ohne die Daten des Beispiels zu duplizieren.                                                                                                                                                  |
| [**IStreamSample**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-istreamsample)         | Steuert das Verhalten eines bestimmten Streambeispiels. Sie können den Stream abrufen, der das Beispiel erstellt hat, die Start- und Endzeiten und den Abschlussstatus des Beispiels überprüfen und eine benutzerdefinierte Funktion für das Beispiel selbst (über die [**Update-Methode)**](/previous-versions/windows/desktop/api/mmstream/nf-mmstream-istreamsample-update) ausführen. In der Regel verarbeitet die Update-Methode die Beispieldaten auf geeignete Weise, z. B. das Rendern von Videodaten oder das Wiedergeben von Audiodaten. |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Liste der Multimediastreamingschnittstellen](list-of-multimedia-streaming-interfaces.md)
</dt> </dl>

 

 



