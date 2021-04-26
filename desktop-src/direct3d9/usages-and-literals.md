---
description: Die Verwendung ähnelt dem Bereich eines Parameters, da er den Bereich definiert, in dem der Parameter gültig ist.
ms.assetid: 9ba10dba-626f-4cb8-8dc2-1419329b199e
title: Verwendungen und Literale (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62dc1d7b40e66aaa6499dd2aa00c37d4564df2ab
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/26/2021
ms.locfileid: "107998537"
---
# <a name="usages-and-literals-direct3d-9"></a>Verwendungen und Literale (Direct3D 9)

Die Verwendung ähnelt dem Gültigkeitsbereich eines Parameters, da er den Bereich definiert, in dem der Parameter gültig ist.



| Wert  | BESCHREIBUNG                                                                                                                                                                                                                                                                         |
|--------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| const  | Der Parameter ist innerhalb des Bereichs aller Funktionen konstant. (Beachten Sie, dass solche Parameter weiterhin mit [**ID3DXEffect**](id3dxeffect.md) oder [**ID3DXEffectCompiler**](id3dxeffectcompiler.md)in geschrieben werden können, da dies außerhalb des Bereichs aller Funktionen auftritt.) |
| Freigegeben | Der Parameter wird im Auswirkungspool freigegeben.                                                                                                                                                                                                                                    |
| static | Der -Parameter ist für die Anwendung unsichtbar, d. h., Sie können nicht über [**ID3DXEffect**](id3dxeffect.md) oder [**ID3DXEffectCompiler**](id3dxeffectcompiler.md)darauf zugreifen.                                                                                                  |



 

Das Markieren eines Parameters als Literal gibt an, dass sich sein Wert nie ändert. Dies ermöglicht dem Effektcompiler eine zusätzliche Optimierung.

Nur nicht freigegebene Parameter der obersten Ebene können als Literal markiert werden. Parameter können nur mit [**ID3DXEffectCompiler**](id3dxeffectcompiler.md)als Literal markiert werden. Literalwerte können nicht mit [**ID3DXEffect**](id3dxeffect.md)festgelegt werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Effektformat](dx9-graphics-reference-effects-file-format.md)
</dt> </dl>

 

 



