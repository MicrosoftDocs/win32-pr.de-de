---
title: Graustufeneffekt
description: Konvertiert ein Bild in ein monochromes Graustufenbild.
ms.assetid: 4e0b26ed-ba71-5f8f-db1e-f1b4e28fbd11
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03b74e553074b3ee0c9ad4e0d5121b9b084884ddb030c75308eb9964531fc6b7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119075333"
---
# <a name="grayscale-effect"></a>Graustufeneffekt

Konvertiert ein Bild in ein monochromes Graustufenbild.

Grayscale verwendet den Farbmatrixeffekt, um mithilfe der folgenden Matrix in Graustufen zu konvertieren:

![Konvertierungsmatrix](images/grayscale-effect-matrix.png)

Die CLSID für diesen Effekt ist CLSID \_ D2D1Grayscale.

-   [Beispielbild](#example-image)
-   [Effekteigenschaften](#effect-properties)
-   [Requirements](#requirements)
-   [Zugehörige Themen](#related-topics)

## <a name="example-image"></a>Beispielbild

![Beispiel für die Effektausgabe](images/grayscale-effect.png)

## <a name="effect-properties"></a>Effect-Eigenschaften

Dieser Effekt hat keine Eigenschaften.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------------|---------------------------------------------------|
| Unterstützte Mindestversion (Client) | \[Windows 10 Desktop-Apps \| Windows Store Apps\] |
| Unterstützte Mindestversion (Server) | \[Windows 10 Desktop-Apps \| Windows Store Apps\] |
| Header                   | d2d1effects \_ 2.h                                  |
| Bibliothek                  | d2d1.lib, dxguid.lib                              |


## <a name="related-topics"></a>Zugehörige Themen

* [ID2D1Effect-Schnittstelle](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)
