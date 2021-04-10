---
description: Erstellen eines audioerfassungs Diagramms mit Vorschau
ms.assetid: 73c0b799-060b-4b20-b072-6a0c5c30de20
title: Erstellen eines audioerfassungs Diagramms mit Vorschau
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2962dc0ffa08e19618d81a03515e970dcb439913
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103958104"
---
# <a name="creating-an-audio-capture-graph-with-preview"></a>Erstellen eines audioerfassungs Diagramms mit Vorschau

Das in [Erstellen eines audioerfassungs Diagramms](creating-an-audio-capture-graph.md) beschriebene Filter Diagramm führt nur die Erfassung durch und ohne Vorschau. Um gleichzeitig eine Vorschau und Erfassung durchführen zu können, muss das Filter Diagramm den [unendlichen Pin-Tee-Filter](infinite-pin-tee-filter.md)verwenden. Dieser Filter verfügt über eine Eingabe-PIN und erstellt bei Bedarf beliebig viele Ausgabe Pins. (Er beginnt mit einer Ausgabe-PIN. Jedes Mal, wenn Sie eine Ausgabe-PIN verbinden, wird eine andere erstellt.) Der Filter für unendliche Pin-Empfänger übermittelt alle empfangenen Stichproben, unverändert, über alle Ausgabe Pins.

Verbinden Sie den audioerfassungs Filter mit dem unendlichen Pin-Tee, und verbinden Sie den unbegrenzten Pin-Empfänger mit dem Multiplexer und dem [DirectSound-rendererfilter](directsound-renderer-filter.md). Verbinden Sie den Multiplexer wie zuvor mit dem dateiwriter. Das folgende Diagramm veranschaulicht das resultierende Filter Diagramm für eine AVI-Datei.

![audioerfassungs Diagramm mit Vorschau](images/audio-capture-graph.png)

Da der DirectSound-Renderer der Standardaudiorenderer ist, können Sie einfach die [**igraphbuilder:: Rendering**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-render) -Methode für die Ausgabepin des unendlichen Pin-Ausstellers aufzurufen. Der Filter Graph-Manager verwendet [Intelligent Connect](intelligent-connect.md) , um den Renderer zu erstellen, ihn dem Filter Diagramm hinzuzufügen und die Pins zu verbinden.

> [!Note]  
> Wenn Sie Audiodaten von einem Mikrofon erfassen und eine Vorschau von einem Redner auf demselben Computer anzeigen, können Sie Audiofeedback erstellen.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Audioerfassung](audio-capture.md)
</dt> </dl>

 

 



