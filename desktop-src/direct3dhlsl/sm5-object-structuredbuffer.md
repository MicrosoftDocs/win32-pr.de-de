---
title: Structuredbuffer
description: Ein Schreib geschützter Puffer, der einen T-Typ, der eine Struktur ist, annehmen kann.
ms.assetid: fe2ec0b8-0e19-42b6-9dad-c992ecdeb19e
keywords:
- Structuredbuffer HLSL
topic_type:
- apiref
api_name:
- StructuredBuffer
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 524078780ac28d691c4999491bed146a04d34439
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104993407"
---
# <a name="structuredbuffer"></a>Structuredbuffer

Ein Schreib geschützter Puffer, der einen T-Typ, der eine Struktur ist, annehmen kann.



| Methode                                                             | BESCHREIBUNG                            |
|--------------------------------------------------------------------|----------------------------------------|
| [**GetDimensions**](sm5-object-structuredbuffer-getdimensions.md) | Ruft die Ressourcen Dimensionen ab.          |
| [**Laden**](structuredbuffer-load.md)                              | Liest Puffer Daten.                     |
| [**KOM\[\]**](sm5-object-structuredbuffer-operatorindex.md)  | Gibt eine schreibgeschützte Ressourcen Variable zurück. |



 

Das an diese Ressource gebundene UAV-Format muss mit dem \_ unbekanntem DXGI-Format erstellt werden \_ .

Weitere Informationen über [strukturierte Puffer](/windows/desktop/direct3d11/direct3d-11-advanced-stages-cs-resources)finden Sie im Übersichts Material.

## <a name="minimum-shader-model"></a>Minimaler Shader-Modell

Dieses Objekt wird in den folgenden shadermodellen unterstützt.



| Shadermodell                                                                                                                                                                                                            | Unterstützt |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------|
| Shader [Model 5](d3d11-graphics-reference-sm5.md) und höhere Shader-Modelle Shader [Model 4](dx-graphics-hlsl-sm4.md) (verfügbar für Compute-und Pixel-Shader in Direct3D 11 auf einigen Direct3D 10-Geräten)<br/> | ja       |



 

Dieses Objekt wird für die folgenden Typen von Shadern unterstützt.



| Scheitelpunkt | Hülle | Domain | Geometrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Shader Model 5-Objekte](d3d11-graphics-reference-sm5-objects.md)
</dt> </dl>

 

