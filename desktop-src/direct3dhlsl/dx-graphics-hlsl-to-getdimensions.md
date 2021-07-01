---
title: GetDimensions (DirectX HLSL-Texturobjekt)
description: Ruft Texturgrößeninformationen ab. Der Syntaxblock zeigt alle Parameter an, die in der Methodendeklaration möglich sind. Die Tabelle im Abschnitt "Hinweise" zeigt, welche Parameter für jeden Texturobjekttyp implementiert werden.
ms.assetid: b72e54da-382a-4b90-bbfe-0b32effc7c05
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: bb6ef3c35af60ea776622718099acdedb5188ba8
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119836"
---
# <a name="getdimensions-directx-hlsl-texture-object"></a>GetDimensions (DirectX HLSL-Texturobjekt)

Ruft Texturgrößeninformationen ab. Der Syntaxblock zeigt alle Parameter an, die in der Methodendeklaration möglich sind. Die Tabelle im Abschnitt "Hinweise" zeigt, welche Parameter für jeden Texturobjekttyp implementiert werden.

void Object.GetDimensions( UINT MipLevel, typeX Width, typeX Height, typeX Elements, typeX Depth, typeX NumberOfLevels, typeX NumberOfSamples );



 

typeX gibt an, dass es zwei mögliche Typen gibt: **uint** oder **float**.

## <a name="parameters"></a>Parameter



| Element                                                                                                                               | Beschreibung                                                                                                                          |
|------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Object"></span><span id="object"></span><span id="OBJECT"></span>*Objekt*<br/>                                     | Beliebiger [Texturobjekttyp](dx-graphics-hlsl-to-type.md) mit Ausnahme eines **Buffer-Objekts.**<br/>                                       |
| <span id="MipLevel"></span><span id="miplevel"></span><span id="MIPLEVEL"></span>*MipLevel*<br/>                             | \[in \] Ein nullbasierter Index, der die Mipmapebene identifiziert. Wenn dieses Argument nicht verwendet wird, wird die erste MIP-Ebene angenommen.<br/> |
| <span id="Width"></span><span id="width"></span><span id="WIDTH"></span>*Breite*<br/>                                         | \[out \] Die Texturbreite in Texeln.<br/>                                                                                     |
| <span id="Height"></span><span id="height"></span><span id="HEIGHT"></span>*Höhe*<br/>                                     | \[out \] Die Texturhöhe in Texeln.<br/>                                                                                    |
| <span id="Elements"></span><span id="elements"></span><span id="ELEMENTS"></span>*Elemente*<br/>                             | \[out \] Die Anzahl der Elemente in einem Array.<br/>                                                                               |
| <span id="Depth"></span><span id="depth"></span><span id="DEPTH"></span>*Tiefe*<br/>                                         | \[out \] Die Texturtiefe in Texeln.<br/>                                                                                     |
| <span id="NumberOfLevels"></span><span id="numberoflevels"></span><span id="NUMBEROFLEVELS"></span>*NumberOfLevels*<br/>     | \[out \] Die Anzahl der Mipmap-Ebenen.<br/>                                                                                      |
| <span id="NumberOfSamples"></span><span id="numberofsamples"></span><span id="NUMBEROFSAMPLES"></span>*NumberOfSamples*<br/> | \[out \] Die Anzahl der Beispiele.<br/>                                                                                            |



 

## <a name="return-value"></a>Rückgabewert

Keiner

## <a name="overloaded-methods"></a>Überladene Methoden

In dieser Tabelle werden alle verschiedenen Versionen der -Methode aufgeführt. -Versionen unterscheiden sich durch die Anzahl der Eingabeparameter. Beachten Sie, dass es für jede Methode, die ganzzahlige Parameter angibt, eine überladene Methode gibt, die Gleitkommaparameter verwendet.



| Texture-Object Typ | Eingabeparameter                                                               |
|---------------------|--------------------------------------------------------------------------------|
| Texture1D           | UINT MipLevel, UINT Width, UINT NumberOfLevels                                 |
| Texture1D           | UINT-Breite                                                                     |
| Texture1D           | UINT MipLevel, float Width, float NumberOfLevels                               |
| Texture1D           | float Width                                                                    |
| Texture1DArray      | UINT MipLevel, UINT Width, UINT Elements, UINT NumberOfLevels                  |
| Texture1DArray      | UINT-Breite, UINT-Elemente                                                      |
| Texture1DArray      | UINT MipLevel, float Width, float Elements, float NumberOfLevels               |
| Texture1DArray      | float Width, float Elements                                                    |
| Texture2D           | UINT MipLevel, UINT Width, UINT Height, UINT NumberOfLevels                    |
| Texture2D           | UINT-Breite, UINT-Höhe                                                        |
| Texture2D           | UINT MipLevel, float Width, float Height, float NumberOfLevels                 |
| Texture2D           | float Width, float Height                                                      |
| Texture2DArray      | UINT MipLevel, UINT Width, UINT Height, UINT Elements, UINT NumberOfLevels     |
| Texture2DArray      | UINT-Breite, UINT-Höhe, UINT-Elemente                                         |
| Texture2DArray      | UINT MipLevel, float Width, float Height, float Elements, float NumberOfLevels |
| Texture2DArray      | float Width, float Height, float Elements                                      |
| Texture3D           | UINT MipLevel, UINT Width, UINT Height, UINT Depth, UINT NumberOfLevels        |
| Texture3D           | UINT-Breite, UINT-Höhe, UINT-Tiefe                                            |
| Texture3D           | UINT MipLevel, float Width, float Height, float Depth, float NumberOfLevels    |
| Texture3D           | float Width, float Height, float Depth                                         |
| TextureCube         | UINT MipLevel, UINT Width, UINT Height, UINT NumberOfLevels                    |
| TextureCube         | UINT-Breite, UINT-Höhe                                                        |
| TextureCube         | UINT MipLevel, float Width, float Height, UINT NumberOfLevels                  |
| TextureCube         | float Width, float Height                                                      |
| TextureCubeArray    | UINT MipLevel, UINT Width, UINT Height, UINT Elements, UINT NumberOfLevels     |
| TextureCubeArray    | UINT-Breite, UINT-Höhe, UINT-Elemente                                         |
| TextureCubeArray    | UINT MipLevel, float Width, float Height, float Elements, float NumberOfLevels |
| TextureCubeArray    | float Width, float Height, float Elements                                      |
| Texture2DMS         | UINT-Breite, UINT-Höhe, UINT-Beispiele                                          |
| Texture2DMS         | float Width, float Height, float Samples                                       |
| Texture2DMSArray    | UINT-Breite, UINT-Höhe, UINT-Elemente, UINT-Beispiele                           |
| Texture2DMSArray    | float Width, float Height, float Elements, float Samples                       |



 

## <a name="minimum-shader-model"></a>Shader-Mindestmodell

Diese Funktion wird in den folgenden Shadermodellen unterstützt.



| Vs \_ 4 \_ 0 | Vs \_ 4 \_ 1  | ps \_ 4 \_ 0 | ps \_ 4 \_ 1  | gs \_ 4 \_ 0 | gs \_ 4 \_ 1  |
|----------|-----------|----------|-----------|----------|-----------|
| x        | x         | x        | x         | x        | x         |



 

1.  Gibt Dimensionen für die größte (nullth) mipmap-Ebene zurück.
2.  TextureCubeArray ist im Shadermodell 4.1 oder höher verfügbar.
3.  Shadermodell 4.1 ist in Direct3D 10.1 oder höher verfügbar.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Texturobjekt](dx-graphics-hlsl-to-type.md)
</dt> </dl>

 

 





