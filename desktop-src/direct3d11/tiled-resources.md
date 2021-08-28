---
title: Gekachelte Ressourcen
description: Gekachelte Ressourcen können als große logische Ressourcen angesehen werden, die kleine Mengen an physischem Arbeitsspeicher verwenden.
ms.assetid: 03083460-192b-40cb-8ee1-76df6d95f72b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e73835d6603d1d8d7e708cd422e3991bb88ac1f91cebf016ccce36f2466270c1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119124088"
---
# <a name="tiled-resources"></a>Gekachelte Ressourcen

Gekachelte Ressourcen können als große logische Ressourcen angesehen werden, die kleine Mengen an physischem Arbeitsspeicher verwenden.

In diesem Abschnitt wird beschrieben, warum gekachelte Ressourcen benötigt werden und wie Sie gekachelte Ressourcen erstellen und verwenden.

## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                                                   | Beschreibung                                                                                                                                                                                                                                         |
|-----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Warum werden gekachelte Ressourcen benötigt?](why-are-tiled-resources-needed-.md)<br/>       | Kachelressourcen sind erforderlich, sodass weniger GPU-Arbeitsspeicher (Graphics Processing Unit) zum Speichern von Oberflächenbereichen verschwendet wird, von denen die Anwendung weiß, dass nicht zugegriffen wird, und die Hardware kann verstehen, wie über angrenzende Kacheln gefiltert wird.<br/>     |
| [Erstellen von gekachelten Ressourcen](creating-tiled-resources.md)<br/>                     | Kachelressourcen werden erstellt, indem beim Erstellen einer Ressource das [**FLAG D3D11 \_ RESOURCE \_ MISC \_ TILED**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag) angegeben wird.<br/>                                                                                          |
| [Gekachelte Ressourcen-APIs](tiled-resource-apis.md)<br/>                               | Die in diesem Abschnitt beschriebenen APIs funktionieren mit gekachelten Ressourcen und Kachelpools.<br/>                                                                                                                                                              |
| [Pipelinezugriff auf gekachelte Ressourcen](pipeline-access-to-tiled-resources.md)<br/> | Kachelressourcen können in Shaderressourcensichten (SRV), Renderzielsichten (RTV), Tiefenschablonenansichten (DSV) und ungeordneten Zugriffsansichten (UAV) sowie in einigen Bindungspunkten verwendet werden, an denen keine Ansichten verwendet werden, z. B. Scheitelpunktpufferbindungen. <br/> |
| [Features-Ebenen für gekachelte Ressourcen](tiled-resources-features-tiers.md)<br/>         | Direct3D 11.2 macht die Unterstützung von kachelten Ressourcen in zwei Ebenen mit den Werten des [**D3D11 \_ TILED \_ RESOURCES TIER \_ verfügbar.**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_tiled_resources_tier) <br/>                                                                                         |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Ressourcen](overviews-direct3d-11-resources.md)
</dt> </dl>

 

 





