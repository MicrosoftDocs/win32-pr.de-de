---
title: GetDimensions (DirectX HLSL-Textur Objekt)
description: Ruft Textur Größen Informationen ab. Der Syntax Block zeigt alle Parameter an, die in der Methoden Deklaration möglich sind. Die Tabelle im Abschnitt "Hinweise" zeigt, welche Parameter für jeden Textur Objekttyp implementiert werden.
ms.assetid: b72e54da-382a-4b90-bbfe-0b32effc7c05
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 0ad4be68049c92955c5ddb06a0c5eccfe2c26b77
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "103857763"
---
# <a name="getdimensions-directx-hlsl-texture-object"></a>GetDimensions (DirectX HLSL-Textur Objekt)

Ruft Textur Größen Informationen ab. Der Syntax Block zeigt alle Parameter an, die in der Methoden Deklaration möglich sind. Die Tabelle im Abschnitt "Hinweise" zeigt, welche Parameter für jeden Textur Objekttyp implementiert werden.



|                                                                                                                                                  |
|--------------------------------------------------------------------------------------------------------------------------------------------------|
| void Object. GetDimensions (uint miplevel, Typex Width, Typex Height, Typex-Elemente, Typex-Tiefe, Typex-nummerierer, Typex-nummerierproben); |



 

TypeX gibt an, dass zwei mögliche Typen vorhanden sind: " **uint** " oder " **float**".

## <a name="parameters"></a>Parameter



| Element                                                                                                                               | BESCHREIBUNG                                                                                                                          |
|------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Object"></span><span id="object"></span><span id="OBJECT"></span>*Objekt*<br/>                                     | Ein beliebiger [Textur Objekttyp](dx-graphics-hlsl-to-type.md) mit Ausnahme eines **Puffer** Objekts.<br/>                                       |
| <span id="MipLevel"></span><span id="miplevel"></span><span id="MIPLEVEL"></span>*Miplevel*<br/>                             | \[in \] einem NULL basierten Index, der die MipMap-Ebene identifiziert. Wenn dieses Argument nicht verwendet wird, wird die erste MIP-Ebene angenommen.<br/> |
| <span id="Width"></span><span id="width"></span><span id="WIDTH"></span>*Breite*<br/>                                         | \[\]die Textur Breite in Texels.<br/>                                                                                     |
| <span id="Height"></span><span id="height"></span><span id="HEIGHT"></span>*Flugh*<br/>                                     | \[\]die Textur Höhe in Texels.<br/>                                                                                    |
| <span id="Elements"></span><span id="elements"></span><span id="ELEMENTS"></span>*Aspekte*<br/>                             | \[gibt \] die Anzahl von Elementen in einem Array zurück.<br/>                                                                               |
| <span id="Depth"></span><span id="depth"></span><span id="DEPTH"></span>*Eingeh*<br/>                                         | \[\]die Textur Tiefe in Texels.<br/>                                                                                     |
| <span id="NumberOfLevels"></span><span id="numberoflevels"></span><span id="NUMBEROFLEVELS"></span>*Nummerige*<br/>     | \[\]die Anzahl von MipMap-Ebenen.<br/>                                                                                      |
| <span id="NumberOfSamples"></span><span id="numberofsamples"></span><span id="NUMBEROFSAMPLES"></span>*Anzahl von Beispielen*<br/> | \[gibt \] die Anzahl der Stichproben an.<br/>                                                                                            |



 

## <a name="return-value"></a>Rückgabewert

Keiner

## <a name="overloaded-methods"></a>Überladene Methoden

Diese Tabelle listet alle unterschiedlichen Versionen der-Methode auf. Versionen unterscheiden sich je nach Anzahl der Eingabeparameter. Beachten Sie, dass für jede Methode, die ganzzahlige Parameter annimmt, eine überladene Methode vorhanden ist, die Gleit Komma Parameter annimmt.



| Texture-Object-Typ | Eingabeparameter                                                               |
|---------------------|--------------------------------------------------------------------------------|
| Texture1D           | Uint miplevel, uint Width, uint nummerioflevels                                 |
| Texture1D           | Uint-Breite                                                                     |
| Texture1D           | Uint-miplevel, float-Breite, float-Anzahlungs Zeichen                               |
| Texture1D           | Gleit Komma Breite                                                                    |
| Texture1DArray      | Uint miplevel, uint Width, uint-Elemente, uint-Anzahlungs Elemente                  |
| Texture1DArray      | Uint-Breite, uint-Elemente                                                      |
| Texture1DArray      | Uint miplevel, float width, float-Elemente, float-Anzahlungs Zeichen               |
| Texture1DArray      | float-Breite, float-Elemente                                                    |
| Texture2D           | Uint miplevel, uint Width, uint Height, uint nummerioflevels                    |
| Texture2D           | Uint-Breite, uint-Höhe                                                        |
| Texture2D           | Uint-miplevel, float-Breite, float-Höhe, float-Anzahlungs Zeichen                 |
| Texture2D           | float-Breite, float-Höhe                                                      |
| Texture2DArray      | Uint miplevel, uint Width, uint Height, uint-Elemente, uint-nummerioflevels     |
| Texture2DArray      | Uint-Breite, uint-Höhe, uint-Elemente                                         |
| Texture2DArray      | Uint-miplevel, float-Breite, float-Höhe, float-Elemente, float-anzahloflecken |
| Texture2DArray      | float-Breite, float-Höhe, float-Elemente                                      |
| Texture3D           | Uint miplevel, uint Width, uint Height, uint-Tiefe, uint-nummerioflevels        |
| Texture3D           | Uint-Breite, uint-Höhe, uint-Tiefe                                            |
| Texture3D           | Uint miplevel, float width, float height, float-Tiefe, float-Anzahlungs Zeichen    |
| Texture3D           | float-Breite, float-Höhe, Gleit Komma Tiefe                                         |
| TextureCube         | Uint miplevel, uint Width, uint Height, uint nummerioflevels                    |
| TextureCube         | Uint-Breite, uint-Höhe                                                        |
| TextureCube         | Uint-miplevel, float-Breite, float-Höhe, uint-Anzahlungs Zeichen                  |
| TextureCube         | float-Breite, float-Höhe                                                      |
| Texturecubearray    | Uint miplevel, uint Width, uint Height, uint-Elemente, uint-nummerioflevels     |
| Texturecubearray    | Uint-Breite, uint-Höhe, uint-Elemente                                         |
| Texturecubearray    | Uint-miplevel, float-Breite, float-Höhe, float-Elemente, float-anzahloflecken |
| Texturecubearray    | float-Breite, float-Höhe, float-Elemente                                      |
| Texture2DMS         | Uint-Breite, uint-Höhe, uint-Beispiele                                          |
| Texture2DMS         | float-Breite, float-Höhe, float-Stichproben                                       |
| Texture2DMSArray    | Uint Width, uint Height, uint-Elemente, uint-Beispiele                           |
| Texture2DMSArray    | float-Breite, float-Höhe, float-Elemente, float-Beispiele                       |



 

## <a name="minimum-shader-model"></a>Minimaler Shader-Modell

Diese Funktion wird in den folgenden shadermodellen unterstützt.



| vs \_ 4 \_ 0 | vs \_ 4 \_ 1  | PS \_ 4 \_ 0 | PS \_ 4 \_ 1  | GS \_ 4 \_ 0 | GS \_ 4 \_ 1  |
|----------|-----------|----------|-----------|----------|-----------|
| x        | x         | x        | x         | x        | x         |



 

1.  Gibt Dimensionen für die größte (nullte) MipMap-Ebene zurück.
2.  Texturecubearray ist im Shader-Modell 4,1 oder höher verfügbar.
3.  Das Shader-Modell 4,1 ist in Direct3D 10,1 oder höher verfügbar.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Texture-Objekt](dx-graphics-hlsl-to-type.md)
</dt> </dl>

 

 





