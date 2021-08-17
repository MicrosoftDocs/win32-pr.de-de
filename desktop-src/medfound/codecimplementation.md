---
description: Codecimplementierung.
ms.assetid: 5ec23f95-cc7d-4c16-979a-f1d2cc485bb0
title: Codecimplementierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd1bb9c51788526d68b370dec782b433e6f8d7114ece2b4f5a735ef7662f869d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118974859"
---
# <a name="codec-implementation"></a>Codecimplementierung

Die Windows Medienaudio- und Videocodecs werden als COM-Objekte implementiert. In der Regel wird ein Codec als Paar von COM-Objekten implementiert: eines für den Encoder und eines für den Decoder. Der Encoder verfügt über einen Klassenbezeichner (CLSID), und der Decoder hat eine andere CLSID. Beispielsweise verfügt der Encoderteil des Windows Media Audio 9-Codecs über eine CLSID, die durch die Konstante **CLSID \_ CWMAEncMediaObject** dargestellt wird, und der Decoderteil desselben Codecs verfügt über eine CLSID, die durch die Konstante **CLSID \_ CWMADecMediaObject** dargestellt wird.

In einigen Fällen ist mehr als ein Encoder in einem einzelnen COM-Objekt enthalten. Beispielsweise sind der Windows Media Video 9-Encoder und der Windows Media Video 9.1-Encoder Teil desselben COM-Objekts. Folglich verfügen beide über die gleiche CLSID, die durch die Konstante **CLSID \_ CWMV9EncMediaObject dargestellt wird.** Auf ähnliche Weise enthalten einige COM-Objekte mehr als einen Decoder.

Jedes Encoder- oder Decoderobjekt macht die [**IMediaObject-Schnittstelle**](/previous-versions/ms785953%28v%3dvs.85%29) verfügbar, sodass das Objekt als DirectX-Medienobjekt (DMO) und als [**EINETRANSFORM-Schnittstelle**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) verwendet werden kann, sodass das Objekt als Media Foundation Transform (MFT) verwendet werden kann.

Für die meisten Encoder verwenden Sie die gleiche CLSID, unabhängig davon, ob Sie den Encoder als DMO oder MFT verwenden, um eine Instanz des Encoders zu erstellen. Um beispielsweise eine Instanz des Windows Media Video 9-Encoders zu erstellen, verwenden Sie **CLSID \_ CWMV9EncMediaObject,** unabhängig davon, ob Sie den Encoder als DMO oder MFT verwenden möchten. Auf ähnliche Weise verfügt jeder Decoder für die meisten Decoder über eine einzelne CLSID, unabhängig davon, ob Sie den Decoder als DMO oder MFT verwenden.

> [!Note]  
> Es gibt einige Ausnahmen von der vorherigen Anweisung zur Verwendung einer einzelnen CLSID sowohl für DMO als auch für MFT. Beispielsweise verfügt der MPEG-4 Part 2-Decoder über eine CLSID, wenn er als DMO und eine andere CLSID agiert, wenn er als MFT agiert.

 

Zusätzlich zu den Kernschnittstellen implementiert jedes Encoder- oder Decoderobjekt zwei ähnliche Schnittstellen für die Arbeit mit Codeceigenschaften: **IPropertyBag** und **IPropertyStore.** In älteren Versionen der Encoder- und Decoderobjekte wurde **IPropertyBag** verwendet, wodurch jede Eigenschaft durch einen Zeichenfolgenwert identifiziert wird, der einen Eigenschaftennamen enthält. **IPropertyStore** ist eine neuere Schnittstelle, die Eigenschaften mit einem eindeutigen Eigenschaftsschlüsselwert identifiziert. Unterstützung für **IPropertyStore wurde** hinzugefügt, um Unterstützung für MFTs zu bieten. Die **meisten IPropertyBag-Eigenschaftennamenszeichenfolgen** verfügen über eine entsprechende **IPropertyStore-Eigenschaftsschlüssel-GUID,** und die meisten GUIDs verfügen über eine entsprechende **IPropertyBag-Namenszeichenfolge,** mit einigen Ausnahmen.

In dieser Dokumentation werden die Eigenschaften nach Eigenschaftsschlüsselkonst constant aufgeführt, aber jeder Eintrag enthält die Eigenschaftsnamen-Zeichenfolgenkonst constant für die Verwendung **mit IPropertyBag,** falls zutreffend.

## <a name="related-topics"></a>Zugehörige Themen

[Windows Media-Codecs](windows-media-codecs.md)
