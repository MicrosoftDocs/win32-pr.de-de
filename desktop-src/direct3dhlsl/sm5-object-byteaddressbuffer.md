---
title: ByteAddressBuffer
description: ByteAddressBuffer
ms.assetid: 809b5ee8-0a25-402e-8cf2-f5e7a8094ec6
keywords:
- ByteAddressBuffer HLSL
topic_type:
- apiref
api_name:
- ByteAddressBuffer
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: bdb7a22570e92945df8ab599f8c95bdffa1d03dd9ac83e35dfc7bb849bd42d99
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119853330"
---
# <a name="byteaddressbuffer"></a>ByteAddressBuffer

Ein schreibgeschützter Puffer, der in Bytes indiziert wird.



| Methode                                                              | BESCHREIBUNG                   |
|---------------------------------------------------------------------|-------------------------------|
| [**GetDimensions**](sm5-object-byteaddressbuffer-getdimensions.md) | Ruft die Ressourcendimensionen ab. |
| [**Laden**](byteaddressbuffer-load.md)                              | Ruft einen Wert ab.               |
| [**Load2**](byteaddressbuffer-load2.md)                            | Ruft zwei Werte ab.              |
| [**Load3**](byteaddressbuffer-load3.md)                            | Ruft drei Werte ab.            |
| [**Load4**](byteaddressbuffer-load4.md)                            | Ruft vier Werte ab.             |



 

Sie können den **ByteAddressBuffer-Objekttyp verwenden,** wenn Sie mit unformatierten Puffern arbeiten. Weitere Informationen zur Unformatiertanzeige von Puffern finden Sie unter [Unformatiert Ansichten von Puffern.](/windows/desktop/direct3d11/overviews-direct3d-11-resources-intro)

## <a name="minimum-shader-model"></a>Minimales Shadermodell

Dieses Objekt wird in den folgenden Shadermodellen unterstützt.



| Shadermodell                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               | Unterstützt |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------|
| [Shadermodell 5](d3d11-graphics-reference-sm5.md) und höhere [Shadermodelle Shader Model 4](dx-graphics-hlsl-sm4.md) (verfügbar über die Direct3D 11-API mit der Featureebene 10.0 oder 10.1 ([**D3D \_ FEATURE \_ LEVEL**](/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_feature_level)10 X) auf Geräten, die \_ \_ Compute-Shader unterstützen. Weitere Informationen zur Unterstützung von Compute-Shadern auf hardware downlevelr Hardware finden Sie unter [Compute Shaders on Downlevel Hardware](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-compute-shaders).)<br/> | Ja       |



 

Dieses Objekt wird für die folgenden Shadertypen unterstützt:



| Scheitelpunkt | Rumpf | Domain | Geometrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

Weitere Informationen zu einem Byteadressenpuffer finden Sie unter dem [adressierbaren Byteressourcentyp](/windows/desktop/direct3d11/direct3d-11-advanced-stages-cs-resources).

ShaderModell 5 implementiert auch einen [Byte-Adresspuffer mit Lese-/Schreibzugriff.](sm5-object-rwbyteaddressbuffer.md)

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ShaderModell 5-Objekte](d3d11-graphics-reference-sm5-objects.md)
</dt> </dl>

 

