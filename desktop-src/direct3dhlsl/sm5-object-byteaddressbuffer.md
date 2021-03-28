---
title: Byteaddressbuffer
description: Byteaddressbuffer
ms.assetid: 809b5ee8-0a25-402e-8cf2-f5e7a8094ec6
keywords:
- Byteaddressbuffer HLSL
topic_type:
- apiref
api_name:
- ByteAddressBuffer
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 03e89f56522d941db4447b33b55cbedc7c73303f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104976825"
---
# <a name="byteaddressbuffer"></a>Byteaddressbuffer

Ein Schreib geschützter Puffer, der in Bytes indiziert ist.



| Methode                                                              | BESCHREIBUNG                   |
|---------------------------------------------------------------------|-------------------------------|
| [**GetDimensions**](sm5-object-byteaddressbuffer-getdimensions.md) | Ruft die Ressourcen Dimensionen ab. |
| [**Laden**](byteaddressbuffer-load.md)                              | Ruft einen Wert ab.               |
| [**Load2**](byteaddressbuffer-load2.md)                            | Ruft zwei Werte ab.              |
| [**Load3**](byteaddressbuffer-load3.md)                            | Ruft drei Werte ab.            |
| [**Load4**](byteaddressbuffer-load4.md)                            | Ruft vier Werte ab.             |



 

Sie können den **byteaddressbuffer** -Objekttyp verwenden, wenn Sie mit Rohdaten Puffer arbeiten. Weitere Informationen zur unformatierten Anzeige von Puffern finden Sie unter unformatierte [Ansichten von Puffern](/windows/desktop/direct3d11/overviews-direct3d-11-resources-intro).

## <a name="minimum-shader-model"></a>Minimaler Shader-Modell

Dieses Objekt wird in den folgenden shadermodellen unterstützt.



| Shadermodell                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               | Unterstützt |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------|
| Shader [Model 5](d3d11-graphics-reference-sm5.md) und höhere Shader-Modelle [Shader Model 4](dx-graphics-hlsl-sm4.md) (verfügbar über die Direct3D 11-API mithilfe der 10,0-oder 10,1-Featureebene ([**D3D \_ Feature \_ Level**](/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_feature_level) \_ 10 \_ X) auf Geräten, die Compute-Shader unterstützen. Weitere Informationen zur Unterstützung von Compute-Shadern bei downlevelhardware finden Sie unter Compute-Shader [auf downlevelhardware](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-compute-shaders).)<br/> | ja       |



 

Dieses Objekt wird für die folgenden Typen von Shadern unterstützt:



| Scheitelpunkt | Hülle | Domain | Geometrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

Weitere Informationen zu einem Byte Adress Puffer finden Sie unter der [Byte adressierbare Ressourcentyp](/windows/desktop/direct3d11/direct3d-11-advanced-stages-cs-resources).

Shader Model 5 implementiert auch einen [Lese-/Schreib-Byte-Adress Puffer](sm5-object-rwbyteaddressbuffer.md).

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Shader Model 5-Objekte](d3d11-graphics-reference-sm5-objects.md)
</dt> </dl>

 

