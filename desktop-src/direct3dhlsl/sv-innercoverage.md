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
ms.openlocfilehash: e1ac278f0524446b5171ef278e169fbe7c3a082f
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/26/2021
ms.locfileid: "107996967"
---
# <a name="sv_innercoverage"></a>SV \_ InnerCoverage

SV InputCoverage stellt verdeckte konservative Rasterungsinformationen dar (d. h., ob ein Pixel garantiert vollständig \_ abgedeckt ist).

## <a name="type"></a>Typ



|      |
|------|
| Typ |
| uint |



 

## <a name="remarks"></a>Hinweise

Dieser vom System generierte Wert ist für die Unterstützung der Ebene 3 erforderlich und nur in dieser Ebene verfügbar. Diese Eingabe schließen sich mit SV \_ Coverage gegenseitig aus. Beides kann nicht verwendet werden.

Für den Zugriff auf SV InnerCoverage muss es als einzelne Komponente aus einem der \_ Pixel-Shader-Eingaberegister deklariert werden. Der Interpolationsmodus für die Deklaration muss konstant sein (interpolation does not apply).

Die konservative Rasterung ist sowohl in D3D11.3 als auch in D3D12 verfügbar. Weitere Informationen finden Sie unter:

-   [D3D11.3 Konservative Rasterung](/windows/desktop/direct3d11/conservative-rasterization)
-   [D3D12 Konservative Rasterung](/windows/desktop/direct3d12/conservative-rasterization)

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Shadermodell 5](d3d11-graphics-reference-sm5.md)
</dt> <dt>

[Shadermodell 5.1 Systemwerte](shader-model-5-1-system-values.md)
</dt> </dl>

 

 
