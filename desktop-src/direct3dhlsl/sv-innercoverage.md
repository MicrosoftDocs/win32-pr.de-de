---
title: SV_InnerCoverage
description: SV InputCoverage stellt verdeckte konservative Rasterungsinformationen dar (d. h., ob ein Pixel garantiert vollständig \_ abgedeckt ist).
ms.assetid: 5BB3C3FB-E5ED-4395-B389-300DE67C984B
keywords:
- SV_InnerCoverage HLSL
topic_type:
- apiref
api_name:
- SV_InnerCoverage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 168f90c17c9e6837d696ebb6dac8f39dc6dfb366
ms.sourcegitcommit: adba238660d8a5f4fe98fc6f5d105d56aac3a400
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/09/2021
ms.locfileid: "111826624"
---
# <a name="sv_innercoverage"></a>SV \_ InnerCoverage

SV InputCoverage stellt verdeckte konservative Rasterungsinformationen dar (d. h., ob ein Pixel garantiert vollständig \_ abgedeckt ist).

## <a name="type"></a>Typ



| Typ     |
|------|
| uint |



 

## <a name="remarks"></a>Hinweise

Dieser vom System generierte Wert ist für die Unterstützung der Ebene 3 erforderlich und nur in dieser Ebene verfügbar. Diese Eingabe schließen sich mit SV \_ Coverage gegenseitig aus. Beides kann nicht verwendet werden.

Für den Zugriff auf SV InnerCoverage muss es als einzelne Komponente aus einem der \_ Pixel-Shader-Eingaberegister deklariert werden. Der Interpolationsmodus für die Deklaration muss konstant sein (interpolation does not apply).

Die konservative Rasterung ist sowohl in D3D11.3 als auch in D3D12 verfügbar. Weitere Informationen finden Sie unter:

-   [D3D11.3 Konservative Rasterung](/windows/desktop/direct3d11/conservative-rasterization)
-   [D3D12 Konservative Rasterung](/windows/desktop/direct3d12/conservative-rasterization)

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Shadermodell 5](d3d11-graphics-reference-sm5.md)
</dt> <dt>

[Shadermodell 5.1 Systemwerte](shader-model-5-1-system-values.md)
</dt> </dl>

 

 
