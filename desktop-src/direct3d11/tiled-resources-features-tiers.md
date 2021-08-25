---
title: Features-Ebenen für gekachelte Ressourcen
description: Direct3D 11.2 macht die Unterstützung von kachelten Ressourcen in zwei Ebenen mit den Werten des D3D11 \_ TILED \_ RESOURCES TIER \_ verfügbar.
ms.assetid: E6A6565B-079B-47DB-A80C-CA5B5413BA32
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c1b76c1d90cc48210f02983817b317eb830224b8f87bb8b4904ee3e11d6cdd6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119894380"
---
# <a name="tiled-resources-features-tiers"></a>Features-Ebenen für gekachelte Ressourcen

Direct3D 11.2 macht die Unterstützung von kachelten Ressourcen in zwei Ebenen mit den Werten des [**D3D11 \_ TILED \_ RESOURCES TIER \_ verfügbar.**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_tiled_resources_tier)

Übergeben Sie den Wert [**D3D11 \_ FEATURE \_ D3D11 \_ OPTIONS1**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_feature) an den *Feature-Parameter* von [**ID3D11Device::CheckFeatureSupport,**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport)um abzufragen, ob die Hardware und der Treiber gekachelte Ressourcen unterstützen, und auf welcher Ebene. Übergeben Sie außerdem einen Zeiger auf die [**D3D11 \_ FEATURE \_ DATA \_ D3D11 \_ OPTIONS1-Struktur**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options1) an den *Parameter pFeatureSupportData,* und übergeben Sie die Größe der **D3D11 \_ FEATURE DATA \_ \_ D3D11 \_ OPTIONS1-Struktur** an den *Parameter FeatureSupportDataSize.* **CheckFeatureSupport** gibt die Ebenenebene als [**D3D11 \_ TILED \_ RESOURCES \_ TIER-Wert**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_tiled_resources_tier) im **TiledResourcesTier-Element** von **D3D11 \_ FEATURE DATA \_ \_ D3D11 \_ OPTIONS1** zurück.

In diesem Abschnitt werden diese beiden Ebenen beschrieben.

## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                           | BESCHREIBUNG                                       |
|---------------------------------|---------------------------------------------------|
| [Ebene 1](tier-1.md)<br/> | In diesem Abschnitt wird die Unterstützung der Ebene 1 beschrieben.<br/> |
| [Ebene 2](tier-2.md)<br/> | In diesem Abschnitt wird die Unterstützung der Ebene 2 beschrieben.<br/> |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Gekachelte Ressourcen](tiled-resources.md)
</dt> </dl>

 

 





