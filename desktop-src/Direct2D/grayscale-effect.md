---
title: Graustufen Effekt
description: Konvertiert ein Bild in ein monochromes Graustufenbild.
ms.assetid: 4e0b26ed-ba71-5f8f-db1e-f1b4e28fbd11
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0dc3cb6a807d282649a2826713cdf48fa966d9f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741969"
---
# <a name="grayscale-effect"></a>Graustufen Effekt

Konvertiert ein Bild in ein monochromes Graustufenbild.

Grayscale verwendet den Farbmatrix Effekt für die Konvertierung in Graustufen mithilfe der folgenden Matrix:

![Konvertierungs Matrix](images/grayscale-effect-matrix.png)

Die CLSID für diesen Effekt ist CLSID \_ D2D1Grayscale.

-   [Beispielbild](#example-image)
-   [Effekt Eigenschaften](#effect-properties)
-   [Anforderungen](#requirements)
-   [Zugehörige Themen](#related-topics)

## <a name="example-image"></a>Beispielbild

![Beispiel für Effekte Ausgabe](images/grayscale-effect.png)

## <a name="effect-properties"></a>Effekt Eigenschaften

Dieser Effekt hat keine Eigenschaften.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------------|---------------------------------------------------|
| Unterstützte Mindestversion (Client) | Windows 10 \[ Desktop Apps- \| Windows Store-Apps\] |
| Unterstützte Mindestversion (Server) | Windows 10 \[ Desktop Apps- \| Windows Store-Apps\] |
| Header                   | d2d1effects \_ 2. h                                  |
| Bibliothek                  | d2d1. lib, dxguid. lib                              |


## <a name="related-topics"></a>Zugehörige Themen

* [ID2D1Effect-Schnittstelle](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)
