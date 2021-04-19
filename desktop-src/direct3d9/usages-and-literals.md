---
description: Die Verwendung ähnelt dem Bereich eines Parameters, da der Bereich definiert wird, in dem der Parameter gültig ist.
ms.assetid: 9ba10dba-626f-4cb8-8dc2-1419329b199e
title: Verwendungen und Literale (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5ca6f010d2c1e05055fd4427b8b5f7d4ab445ae
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106346006"
---
# <a name="usages-and-literals-direct3d-9"></a>Verwendungen und Literale (Direct3D 9)

Die Verwendung ähnelt dem Bereich eines Parameters, da der Bereich definiert wird, in dem der Parameter gültig ist.



|        |                                                                                                                                                                                                                                                                                     |
|--------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Wert  | BESCHREIBUNG                                                                                                                                                                                                                                                                         |
| const  | Der-Parameter ist innerhalb des Bereichs aller Funktionen konstant. (Beachten Sie, dass solche Parameter immer noch in mit [**ID3DXEffect**](id3dxeffect.md) oder [**ID3DXEffectCompiler**](id3dxeffectcompiler.md)geschrieben werden können, da dies außerhalb des Gültigkeits Bereichs aller Funktionen auftritt.) |
| Freigegeben | Der Parameter wird im Effekt Pool freigegeben.                                                                                                                                                                                                                                    |
| static | Der-Parameter ist für die Anwendung unsichtbar, d. h., Sie können nicht über [**ID3DXEffect**](id3dxeffect.md) oder [**ID3DXEffectCompiler**](id3dxeffectcompiler.md)auf Sie zugreifen.                                                                                                  |



 

Das Markieren eines Parameters als Literalwert gibt an, dass sein Wert nie geändert wird. Dadurch kann der Effekt Compiler zusätzliche Optimierungen durchführen.

Nur nicht freigegebene Parameter der obersten Ebene können als Literale gekennzeichnet werden. Parameter können nur mit [**ID3DXEffectCompiler**](id3dxeffectcompiler.md)als Literale gekennzeichnet werden. Literalwerte können nicht mit [**ID3DXEffect**](id3dxeffect.md)festgelegt werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Effekt Format](dx9-graphics-reference-effects-file-format.md)
</dt> </dl>

 

 



