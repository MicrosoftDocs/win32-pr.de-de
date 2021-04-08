---
description: Codec-Implementierung.
ms.assetid: 5ec23f95-cc7d-4c16-979a-f1d2cc485bb0
title: Codecimplementierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 201c0cb46fc61f117c9b45d059b102560986d5b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861824"
---
# <a name="codec-implementation"></a>Codecimplementierung

Die Windows Media Audio-und Video Codecs werden als COM-Objekte implementiert. In der Regel wird ein Codec als Paar von COM-Objekten implementiert: eine für den Encoder und eine für den Decoder. Der Encoder verfügt über einen Klassen Bezeichner (CLSID), und der Decoder hat eine andere CLSID. Der Encoder-Teil des Windows Media Audio 9-Codecs hat z. b. eine CLSID, die durch die Konstante **CLSID \_ cwmaencmediaobject** dargestellt wird, und der Decoder-Teil desselben Codecs hat eine CLSID, die durch die Konstante **CLSID \_ cwmadecmediaobject** dargestellt wird.

In einigen Fällen sind mehrere Encoder in einem einzelnen COM-Objekt enthalten. Beispielsweise sind der Windows Media Video 9-Encoder und der Windows Media Video 9,1-Encoder beide Teil desselben com-Objekts. Folglich haben beide die gleiche CLSID, die durch die Konstante **CLSID \_ CWMV9EncMediaObject** dargestellt wird. Ebenso enthalten einige COM-Objekte mehr als einen Decoder.

Jedes Encoder-oder Decoderobjekt macht die [**imediaobject**](/previous-versions/ms785953%28v%3dvs.85%29) -Schnittstelle verfügbar, sodass das Objekt als DirectX-Medienobjekt (DMO) und die [**imftransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) -Schnittstelle verwendet werden kann, sodass das Objekt als Media Foundation Transformation (MFT) verwendet werden kann.

Bei den meisten Encodern verwenden Sie unabhängig davon, ob Sie den Encoder als DMO oder MFT verwenden, dieselbe CLSID, um eine Instanz des Encoders zu erstellen. Wenn Sie z. b. eine Instanz des Windows Media Video 9-Encoders erstellen möchten, verwenden Sie **CLSID \_ CWMV9EncMediaObject**, unabhängig davon, ob Sie den Encoder als DMO oder MFT verwenden möchten. Ebenso verfügt jeder Decoder bei den meisten Decodern über eine einzelne CLSID, unabhängig davon, ob Sie den Decoder als DMO oder MFT verwenden.

> [!Note]  
> Es gibt einige Ausnahmen von der vorangehenden Anweisung zur Verwendung einer einzelnen CLSID sowohl für DMO als auch für MFT. Der MPEG-4 Part 2-Decoder hat z. b. eine CLSID, wenn er als DMO und eine andere CLSID fungiert, wenn er als MFT fungiert.

 

Zusätzlich zu den Kern Schnittstellen implementiert jedes Encoder-oder Decoder-Objekt zwei ähnliche Schnittstellen zum Arbeiten mit den Codec-Eigenschaften **IPropertyBag** und **IPropertyStore**. Ältere Versionen der Encoder-und Decoder-Objekte verwendeten **IPropertyBag**, das jede Eigenschaft durch einen Zeichen folgen Wert identifiziert, der einen Eigenschaftsnamen enthält. **IPropertyStore** ist eine neuere Schnittstelle, die Eigenschaften mit einem eindeutigen Eigenschafts Schlüsselwert identifiziert. Unterstützung für " **IPropertyStore** " wurde hinzugefügt, um Unterstützung für MFTs bereitzustellen. Die meisten **IPropertyBag** -Eigenschaftsnamen Zeichenfolgen weisen eine entsprechende **IPropertyStore** -Eigenschafts Schlüssel-GUID auf, und die meisten GUIDs verfügen über eine entsprechende **IPropertyBag** -namens Zeichenfolge mit wenigen Ausnahmen.

In dieser Dokumentation werden die Eigenschaften nach Eigenschafts Schlüssel konstant aufgelistet, aber jeder Eintrag enthält die Eigenschaftsname-Zeichen folgen Konstante für die Verwendung mit **IPropertyBag** , wenn dies angebracht ist.

## <a name="related-topics"></a>Zugehörige Themen

[Windows Media-Codecs](windows-media-codecs.md)
