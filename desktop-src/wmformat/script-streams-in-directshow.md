---
title: Skript Streams in DirectShow
description: Skript Streams in DirectShow
ms.assetid: ad467897-1d25-4bb0-a0ec-84560fe7063b
keywords:
- Windows Medienformat-SDK, DirectShow
- Windows Medienformat-SDK, Skriptstreams
- Advanced Systems Format (ASF),DirectShow
- ASF (Advanced Systems Format), DirectShow
- Advanced Systems Format (ASF), Skriptstreams
- ASF (Advanced Systems Format), Skriptstreams
- DirectShow,Skriptstreams
- Skriptstreams,DirectShow
- Streams,Skriptstreams in DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e30e832928b84ab0e1e755dcfdb8c79893c5d942e15e4beb9925f852251614bb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119929619"
---
# <a name="script-streams-in-directshow"></a>Skript Streams in DirectShow

Wenn der WM ASF-Readerfilter eine Datei erhält, die einen Stream vom Typ WMMEDIATYPE Script enthält, erstellt er einen Ausgabepin dafür, der mit dem \_ DirectShow Internal Script Command Renderer-Filter verbunden werden kann. Wenn Sie **IGraphBuilder::RenderFile** aufrufen, wird dieser Filter automatisch dem Diagramm hinzugefügt und verbunden. Wenn der Renderer für interne Skriptbefehle ein Beispiel empfängt, das einen Skriptbefehl enthält, wird ein **EC \_ OLE \_ EVENT-Ereignis** mit **dem LParam-Skript** ausgeführt. Die Anwendung ist vollständig für die Behandlung dieses Ereignisses verantwortlich. Weitere Informationen zu **EC OLE EVENT finden \_ \_ Sie** in der DirectShow SDK-Dokumentation.

 

 




