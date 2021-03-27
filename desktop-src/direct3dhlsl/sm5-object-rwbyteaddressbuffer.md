---
title: Rwbyteaddressbuffer
description: Ein Lese-/Schreibpuffer, der in Bytes indiziert.
ms.assetid: 8370c14c-5822-4240-942d-565aa223d48c
keywords:
- Rwbyteaddressbuffer HLSL
topic_type:
- apiref
api_name:
- RWByteAddressBuffer
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4d065926b0769e15284cbe705783be012d82554b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390345"
---
# <a name="rwbyteaddressbuffer"></a>Rwbyteaddressbuffer

Ein Lese-/Schreibpuffer, der in Bytes indiziert.



| Methode                                                                                          | BESCHREIBUNG                         |
|-------------------------------------------------------------------------------------------------|-------------------------------------|
| [**GetDimensions**](sm5-object-rwbyteaddressbuffer-getdimensions.md)                           | Ruft die Ressourcen Dimensionen ab.       |
| [**Interlockedadd**](sm5-object-rwbyteaddressbuffer-interlockedadd.md)                         | Fügt atomisch hinzu.                   |
| [**Interlockedand**](sm5-object-rwbyteaddressbuffer-interlockedand.md)                         | , Atomisch.                   |
| [**InterlockedCompareExchange**](sm5-object-rwbyteaddressbuffer-interlockedcompareexchange.md) | Vergleicht und tauscht atomarisch aus. |
| [**Interlockedcomparestore**](sm5-object-rwbyteaddressbuffer-interlockedcomparestore.md)       | Vergleicht und speichert atomisch.    |
| [**InterlockedExchange**](sm5-object-rwbyteaddressbuffer-interlockedexchange.md)               | Tauscht atomarisch aus.              |
| [**Interlockedmax**](sm5-object-rwbyteaddressbuffer-interlockedmax.md)                         | Sucht den maximalen, atomisch.          |
| [**Interlockedmin**](sm5-object-rwbyteaddressbuffer-interlockedmin.md)                         | Suchen Sie den Mindestwert atomarisch.           |
| [**Interlockedor**](sm5-object-rwbyteaddressbuffer-interlockedor.md)                           | , Atomarisch.                    |
| [**Interlockedxor**](sm5-object-rwbyteaddressbuffer-interlockedxor.md)                         | Xors, atomisch.                   |
| [**Laden**](rwbyteaddressbuffer-load.md)                                                        | Ruft einen Wert ab.                     |
| [**Load2**](rwbyteaddressbuffer-load2.md)                                                      | Ruft zwei Werte ab.                    |
| [**Load3**](rwbyteaddressbuffer-load3.md)                                                      | Ruft drei Werte ab.                  |
| [**Load4**](rwbyteaddressbuffer-load4.md)                                                      | Ruft vier Werte ab.                   |
| [**Speicher**](sm5-object-rwbyteaddressbuffer-store.md)                                           | Legt einen Wert fest.                     |
| [**Store2**](sm5-object-rwbyteaddressbuffer-store2.md)                                         | Legt zwei Werte fest.                    |
| [**Store3**](sm5-object-rwbyteaddressbuffer-store3.md)                                         | Legt drei Werte fest.                  |
| [**Store4**](sm5-object-rwbyteaddressbuffer-store4.md)                                         | Legt vier Werte fest.                   |



 

Rwbyteaddressbuffer-Objekten kann die Speicher Klasse **globallycoherent** vorangestellt werden. Diese Speicher Klasse bewirkt, dass Speicherbarrieren und Synchronisierungen Daten über die gesamte GPU leeren, sodass andere Gruppen Schreibvorgänge sehen können. Ohne diesen Spezifizierer leert eine Speicherbarriere oder Synchronisierung eine UAV nur innerhalb der aktuellen Gruppe.

Das an diese Ressource gebundene UAV-Format muss mit dem typlosen DXGI-Format (Format) erstellt werden \_ \_ \_ .

Die an diese Ressource gebundene UAV muss mit dem [**D3D11-Puffer- \_ \_ UAV- \_ Flag \_ RAW**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_buffer_uav_flag)erstellt werden.

Sie können den **rwbyteaddressbuffer** -Objekttyp verwenden, wenn Sie mit Rohdaten Puffer arbeiten. Weitere Informationen zur unformatierten Anzeige von Puffern finden Sie unter unformatierte [Ansichten von Puffern](/windows/desktop/direct3d11/overviews-direct3d-11-resources-intro).

## <a name="minimum-shader-model"></a>Minimaler Shader-Modell

Dieses Objekt wird in den folgenden shadermodellen unterstützt.



| Shadermodell                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      | Unterstützt |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------|
| Shader [Model 5](d3d11-graphics-reference-sm5.md) und höhere Shader-Modelle [Shader Model 4](dx-graphics-hlsl-sm4.md) (verfügbar über die Direct3D 11-API mithilfe der 10,0-oder 10,1-Featureebene ([**D3D \_ Feature \_ Level**](/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_feature_level) \_ 10 \_ X) auf Geräten, die Compute-Shader unterstützen. Weitere Informationen zur Unterstützung von Compute-Shadern auf downlevelhardware finden Sie unter Compute-Shader [auf downlevelhardware](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-compute-shaders).)<br/> | ja       |



 

Dieses Objekt wird für die folgenden Typen von Shadern unterstützt:



| Scheitelpunkt | Hülle | Domain | Geometrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     | x       |



 

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Shader Model 5-Objekte](d3d11-graphics-reference-sm5-objects.md)
</dt> </dl>

 

