---
title: Tarife der Kachel "Ressourcen"
description: Direct3D 11,2 macht Unterstützung für gekachelte Ressourcen in zwei Stufen mit den Werten der D3D11- \_ Kachel \_ Ressourcen \_ Ebene verfügbar.
ms.assetid: E6A6565B-079B-47DB-A80C-CA5B5413BA32
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2282cde1dfc8c4249672d18e303a4529338d4fbf
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947470"
---
# <a name="tiled-resources-features-tiers"></a>Tarife der Kachel "Ressourcen"

Direct3D 11,2 macht Unterstützung für gekachelte Ressourcen in zwei Stufen mit den Werten der [**D3D11- \_ Kachel \_ Ressourcen \_ Ebene**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_tiled_resources_tier) verfügbar.

Um abzufragen, ob die Hardware und der Treiber gekachelte Ressourcen unterstützen und auf welcher Ebene, übergeben Sie den Wert [**D3D11 \_ Feature \_ D3D11 \_ OPTIONS1**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_feature) an den *Funktions* Parameter von [**ID3D11Device:: checkfeaturesupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport). Übergeben Sie außerdem einen Zeiger an die [**D3D11 \_ Feature \_ Data \_ D3D11 \_ OPTIONS1**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options1) -Struktur an den *pfeaturesupportdata* -Parameter, und übergeben Sie die Größe der **D3D11 \_ Feature \_ Data \_ D3D11 \_ OPTIONS1** -Struktur an den Parameter " *featuresupportdatasize* ". **Checkfeaturesupport** gibt die Ebene der Ebene als Wert der [**D3D11- \_ Kachel \_ Ressourcen \_ Ebene**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_tiled_resources_tier) im **tiledresourcestier** -Member von **D3D11 \_ Feature \_ Data \_ D3D11 \_ OPTIONS1** zurück.

In diesem Abschnitt werden diese beiden Ebenen beschrieben.

## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                           | BESCHREIBUNG                                       |
|---------------------------------|---------------------------------------------------|
| [Ebene 1](tier-1.md)<br/> | In diesem Abschnitt wird die Unterstützung für Ebene 1 beschrieben.<br/> |
| [Ebene 2](tier-2.md)<br/> | In diesem Abschnitt wird die Unterstützung der Ebene 2 beschrieben.<br/> |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Gekachelte Ressourcen](tiled-resources.md)
</dt> </dl>

 

 





