---
title: Gekachelte Ressourcen
description: Gekachelte Ressourcen können sich als große logische Ressourcen vorstellen, die kleine Mengen an physischem Arbeitsspeicher verwenden.
ms.assetid: 03083460-192b-40cb-8ee1-76df6d95f72b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7c7e6aaf60f58f55274c9d7a135b9107933f640
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855548"
---
# <a name="tiled-resources"></a>Gekachelte Ressourcen

Gekachelte Ressourcen können sich als große logische Ressourcen vorstellen, die kleine Mengen an physischem Arbeitsspeicher verwenden.

In diesem Abschnitt wird beschrieben, warum Kachel Ressourcen benötigt werden und wie Sie gekachelte Ressourcen erstellen und verwenden.

## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                                                   | BESCHREIBUNG                                                                                                                                                                                                                                         |
|-----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Warum werden Kachel Ressourcen benötigt?](why-are-tiled-resources-needed-.md)<br/>       | Gekachelte Ressourcen werden benötigt, sodass weniger GPU-Speicher (Graphics Processing Unit) verschwendet wird, um Bereiche von Oberflächen zu speichern, auf die die Anwendung keinen Zugriff hat, und die Hardware weiß, wie Sie über angrenzende Kacheln filtern kann.<br/>     |
| [Erstellen von Kachel Ressourcen](creating-tiled-resources.md)<br/>                     | Gekachelte Ressourcen werden erstellt, indem beim Erstellen einer Ressource das [**D3D11 \_ Resource \_ misc- \_ Kachel**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag) Kennzeichen angegeben wird.<br/>                                                                                          |
| [Ressourcen-APIs mit Kachel](tiled-resource-apis.md)<br/>                               | Die in diesem Abschnitt beschriebenen APIs funktionieren mit gekachelten Ressourcen und einem Kachel Pool.<br/>                                                                                                                                                              |
| [Pipeline Zugriff auf gekachelte Ressourcen](pipeline-access-to-tiled-resources.md)<br/> | Gekachelte Ressourcen können in Shader-Ressourcen Ansichten (SRV), renderzielsichten (RTV), Datenquellen Sichten (Datenquellen Sicht) und unsortierter Zugriffs Ansichten (UAV) sowie einigen Bindungs Punkten verwendet werden, bei denen Sichten nicht verwendet werden, wie z. b. Vertex-Puffer Bindungen. <br/> |
| [Tarife der Kachel "Ressourcen"](tiled-resources-features-tiers.md)<br/>         | Direct3D 11,2 macht Unterstützung für gekachelte Ressourcen in zwei Stufen mit den Werten der [**D3D11- \_ Kachel \_ Ressourcen \_ Ebene**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_tiled_resources_tier) verfügbar. <br/>                                                                                         |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Ressourcen](overviews-direct3d-11-resources.md)
</dt> </dl>

 

 





