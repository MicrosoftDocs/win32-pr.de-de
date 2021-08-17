---
title: SV_InnerCoverage
description: SV \_ InputCoverage stellt zugesicherte konservative Rasterungsinformationen dar (d. h., ob ein Pixel garantiert vollständig abgedeckt wird).
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
ms.openlocfilehash: 172ee60cb85e69568c8cb226aa19fa325686726f42fc27c7aa21231b1a55ef28
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117724378"
---
# <a name="sv_innercoverage"></a>SV \_ InnerCoverage

SV \_ InputCoverage stellt zugesicherte konservative Rasterungsinformationen dar (d. h., ob ein Pixel garantiert vollständig abgedeckt wird).

## <a name="type"></a>Typ



| Typ     |
|------|
| uint |



 

## <a name="remarks"></a>Hinweise

Dieser vom System generierte Wert ist für die Unterstützung der Ebene 3 erforderlich und nur in diesem Tarif verfügbar. Diese Eingabe schließen sich gegenseitig mit SV \_ Coverage aus– beide können nicht verwendet werden.

Um auf SV InnerCoverage zugreifen zu \_ können, muss es als einzelne Komponente aus einem der Pixel-Shader-Eingaberegister deklariert werden. Der Interpolationsmodus für die Deklaration muss konstant sein (die Interpolation gilt nicht).

Die konservative Rasterung ist sowohl in D3D11.3 als auch in D3D12 verfügbar. Weitere Informationen finden Sie unter:

-   [D3D11.3 Konservative Rasterung](/windows/desktop/direct3d11/conservative-rasterization)
-   [D3D12 Konservative Rasterung](/windows/desktop/direct3d12/conservative-rasterization)

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Shadermodell 5](d3d11-graphics-reference-sm5.md)
</dt> <dt>

[Shadermodell 5.1 Systemwerte](shader-model-5-1-system-values.md)
</dt> </dl>

 

 
