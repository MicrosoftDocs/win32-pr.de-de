---
title: SV_InnerCoverage
description: SV \_ inputcoverage stellt unterschätzte konservative rasterisierungsinformationen dar (d. h., ob ein Pixel garantiert vollständig abgedeckt ist).
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
ms.openlocfilehash: a2f1393a6a11a95c8c08746f57083fe193791a60
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104993550"
---
# <a name="sv_innercoverage"></a>SV \_ innercoverage

SV \_ inputcoverage stellt unterschätzte konservative rasterisierungsinformationen dar (d. h., ob ein Pixel garantiert vollständig abgedeckt ist).

## <a name="type"></a>Typ



|      |
|------|
| Typ |
| uint |



 

## <a name="remarks"></a>Bemerkungen

Dieser vom systemgenerierte Wert ist für die Unterstützung der Ebene 3 erforderlich und nur in dieser Ebene verfügbar. Diese Eingabe schließt sich mit der SV \_ -Abdeckung gegenseitig aus. beide können nicht verwendet werden.

Für den Zugriff auf die SV \_ innercoverage muss Sie als einzelne Komponente aus einem der Pixel-Shader-Eingabe Register deklariert werden. Der Interpolations Modus für die Deklaration muss konstant sein (Interpolation ist nicht anwendbar).

Die konservative rasterisierung ist in D3D 11.3 und D3D12 verfügbar. Weitere Informationen finden Sie unter:

-   [D3D 11.3 konservative rasterisierung](/windows/desktop/direct3d11/conservative-rasterization)
-   [D3D12 konservative rasterisierung](/windows/desktop/direct3d12/conservative-rasterization)

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Shader-Modell 5](d3d11-graphics-reference-sm5.md)
</dt> <dt>

[Shader-Modell 5,1 System Werte](shader-model-5-1-system-values.md)
</dt> </dl>

 

 