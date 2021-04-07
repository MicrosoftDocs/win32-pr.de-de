---
description: Alpha Setter-Effekt
ms.assetid: dd3ab119-328b-4782-811a-f06909c17dec
title: Alpha Setter-Effekt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 372ec018a9cfb8fe15307ae44f5a905bf1eb3440
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103746369"
---
# <a name="alpha-setter-effect"></a>Alpha Setter-Effekt

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]

 

Der Alpha Setter-Effekt legt die Alpha Bits eines Video Bilds fest.

Klassen-ID (CLSID): {506d89ae-909a-44f 7-9444-abd575896e35}

CLSID-Variablen Name: CLSID \_ dxtalphasetter

Anzeige Name: "dxtalphasetter"

### <a name="properties"></a>Eigenschaften



| Eigenschaft  | type   | Standard | BESCHREIBUNG                                                 |
|-----------|--------|---------|-------------------------------------------------------------|
| Alpha     | BYTE   | -1      | Legt das Alpha für das gesamte Bild fest.                        |
| Alpharamp | double | -1.0    | Legt das Alpha als Prozentsatz des ursprünglichen Alpha Werts fest. |



 

## <a name="remarks"></a>Bemerkungen

Eine Eigenschaft mit einem negativen Wert wird ignoriert. Nur eine Eigenschaft kann einen nicht negativen Wert aufweisen. Die Alpha-Eigenschaft gibt einen konstanten Alpha Wert für jedes Pixel im Bild an. Diese Eigenschaft überschreibt die Alpha Werte aus dem ursprünglichen Bild. Die alpharamp-Eigenschaft gibt den Alpha Wert jedes Pixels als Prozentsatz des ursprünglichen Werts des Pixels an, von 0,0 bis 1,0.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Alpha Blending](alpha-blending.md)
</dt> </dl>

 

 



