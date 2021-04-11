---
title: Auswirkungen der Deckkraft-Metadaten
description: Mit diesem Effekt können Sie einen Bereich eines Eingabe Bilds als nicht transparent markieren, sodass interne renderinoptimierungen für das Diagramm möglich sind.
ms.assetid: 25B34A31-8533-4339-BBF7-2D7E5488E301
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d84d90ba1c4b1186e3e682ec94a0c9c17bdfc73e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105447"
---
# <a name="opacity-metadata-effect"></a>Auswirkungen der Deckkraft-Metadaten

Mit diesem Effekt können Sie einen Bereich eines Eingabe Bilds als nicht transparent markieren, sodass interne renderinoptimierungen für das Diagramm möglich sind.

> [!Note]  
> Durch diesen Effekt wird das Abbild nicht als nicht transparent geändert. Er ändert die dem Bild zugeordneten Daten, sodass der Renderer annimmt, dass der angegebene Bereich nicht transparent ist.

 

Die CLSID für diesen Effekt ist CLSID \_ D2D1OpacityMetadata.

## <a name="effect-properties"></a>Effekt Eigenschaften



| Anzeige Name und indexenumeration                                                 | Typ und Standardwert                                                             | BESCHREIBUNG                                                                                       |
|------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| Outputrect<br/> D2D1 \_ opacitymetadata \_ Prop \_ Input nicht transparent \_ \_ Rect <br/> | D2D1 \_ Vector \_ 4f<br/> (-F \_ Max,-f Max, maximal zulässige Anzahl, maximal zulässige Größe \_ \_ \_ ) <br/> | Der Teil des Quell Bilds, der nicht transparent ist. Der Standardwert ist das gesamte Eingabebild.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client) | Windows 8 und Platt Form Update für Windows 7 \[ -Desktop-Apps für \| Windows Store-Apps\] |
| Unterstützte Mindestversion (Server) | Windows 8 und Platt Form Update für Windows 7 \[ -Desktop-Apps für \| Windows Store-Apps\] |
| Header                   | d2d1effects. h                                                                      |
| Bibliothek                  | d2d1. lib, dxguid. lib                                                               |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

