---
description: Alpha-Settereffekt
ms.assetid: dd3ab119-328b-4782-811a-f06909c17dec
title: Alpha-Settereffekt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e599b314dced175188d77dad1ae93259a23b8eb892471d047afab218add9a664
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119586760"
---
# <a name="alpha-setter-effect"></a>Alpha-Settereffekt

> [!Note]  
> \[Veraltet. Diese API wird möglicherweise aus zukünftigen Releases von Windows.\]

 

Der Alpha-Setter-Effekt legt die Alphabits auf einem Videobild fest.

Klassen-ID (CLSID): {506D89AE-909A-44f7-9444-ABD575896E35}

CLSID-Variablenname: CLSID \_ DxtAlphaSetter

Name der Beschriftung: "DxtAlphaSetter"

### <a name="properties"></a>Eigenschaften



| Eigenschaft  | type   | Standard | BESCHREIBUNG                                                 |
|-----------|--------|---------|-------------------------------------------------------------|
| Alpha     | BYTE   | –1      | Legt das Alpha für das gesamte Bild fest.                        |
| AlphaRamp | double | -1.0    | Legt das Alpha als Prozentsatz des ursprünglichen Alphawerts fest. |



 

## <a name="remarks"></a>Hinweise

Eine Eigenschaft mit einem negativen Wert wird ignoriert. Nur eine Eigenschaft kann einen nicht negativen Wert haben. Die Alpha-Eigenschaft gibt einen konstanten Alphawert für jedes Pixel im Bild an. Diese Eigenschaft überschreibt die Alphawerte aus dem ursprünglichen Bild. Die AlphaRamp-Eigenschaft gibt den Alphawert jedes Pixels als Prozentsatz des ursprünglichen Werts des Pixels von 0,0 bis 1,0 an.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Alphablending](alpha-blending.md)
</dt> </dl>

 

 



