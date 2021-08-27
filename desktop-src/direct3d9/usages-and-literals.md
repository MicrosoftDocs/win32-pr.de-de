---
description: Die Verwendung ähnelt dem Bereich eines Parameters, da er den Bereich definiert, in dem der Parameter gültig ist.
ms.assetid: 9ba10dba-626f-4cb8-8dc2-1419329b199e
title: Verwendungen und Literale (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b8c9fa8eb30726e783ce763ec8700f715dbd5d2b85ff3bf98340cf604e8e2f8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120026010"
---
# <a name="usages-and-literals-direct3d-9"></a>Verwendungen und Literale (Direct3D 9)

Die Verwendung ähnelt dem Bereich eines Parameters, da er den Bereich definiert, in dem der Parameter gültig ist.



| Wert  | BESCHREIBUNG                                                                                                                                                                                                                                                                         |
|--------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| const  | Der Parameter ist innerhalb des Bereichs aller Funktionen konstant. (Beachten Sie, dass solche Parameter weiterhin mit [**ID3DXEffect**](id3dxeffect.md) oder [**ID3DXEffectCompiler geschrieben**](id3dxeffectcompiler.md)werden können, da dies außerhalb des Bereichs aller Funktionen auftritt.) |
| Freigegeben | Der Parameter wird im Effektpool freigegeben.                                                                                                                                                                                                                                    |
| static | The parameter will be invisible to the application, that is, you cannot access them from [**ID3DXEffect**](id3dxeffect.md) or [**ID3DXEffectCompiler**](id3dxeffectcompiler.md).                                                                                                  |



 

Das Markieren eines Parameters als Literal gibt an, dass sich sein Wert nie ändert. Dadurch kann der Effektcompiler zusätzliche Optimierungen durchführen.

Nur nicht freigegebene Parameter der obersten Ebene können als Literal markiert werden. Parameter können nur mit [**ID3DXEffectCompiler**](id3dxeffectcompiler.md)als Literal markiert werden. Literalwerte können nicht mit [**ID3DXEffect festgelegt werden.**](id3dxeffect.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Effect-Format](dx9-graphics-reference-effects-file-format.md)
</dt> </dl>

 

 



