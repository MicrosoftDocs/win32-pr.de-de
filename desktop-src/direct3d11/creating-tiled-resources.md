---
title: Erstellen von Kachel Ressourcen
description: Gekachelte Ressourcen werden erstellt, indem \_ \_ beim Erstellen einer Ressource das D3D11 Resource misc-Kachel Kennzeichen angegeben wird \_ .
ms.assetid: DED2B70C-1E95-4A85-A818-FD32165FBF6C
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd6e2c0e457bfd8534d3a42c6f658095b3349572
ms.sourcegitcommit: 4dcafeb002cbee4f6028b32a956ec22cb95cbc44
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/13/2019
ms.locfileid: "104389479"
---
# <a name="creating-tiled-resources"></a>Erstellen von Kachel Ressourcen

Gekachelte Ressourcen werden erstellt, indem beim Erstellen einer Ressource das [**D3D11 \_ Resource \_ misc- \_ Kachel**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag) Kennzeichen angegeben wird.

Einschränkungen für die Verwendung von [**D3D11 \_ Resource \_ misc \_**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag) , die zum Erstellen einer Ressource verwendet werden können, werden unter Parameter für die [Kachel Ressourcen Erstellung](tiled-resource-creation-parameters.md)beschrieben.

Wenn die Ressource erstellt wird, wird im Grafiksystem ein nicht gekachelter Ressourcen Speicher zugeordnet. Wenn Sie z. b. [**ID3D11Device:: CreateTexture2D**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createtexture2d) zum Erstellen eines Arrays von 2D-Texturen aufgerufen haben, ordnet das Grafiksystem Speicher für diese 2D-Texturen zu. Wenn eine Kachel Ressource erstellt wird, weist das Grafiksystem den Speicher für den Ressourcen Inhalt nicht zu. Wenn eine Anwendung eine Kachel Ressource erstellt, stellt das Grafiksystem stattdessen eine Adressraum Reservierung für den Bereich der Kachel Fläche dar und ermöglicht dann die Zuordnung der Kacheln, die von der Anwendung gesteuert werden. Die Zuordnung einer Kachel ist einfach der physische Speicherort im Speicher, auf den eine logische Kachel in einer Ressource zeigt (oder **null** für eine nicht zugeordnete Kachel). Verwechseln Sie dieses Konzept nicht mit dem Konzept der Zuordnung einer Direct3D-Ressource für den CPU-Zugriff, die trotz der vollständigen Verwendung des gleichen Namens ganz unabhängig ist. Sie können die Zuordnung jeder Kachel bei Bedarf einzeln definieren und ändern. dabei ist zu beachten, dass alle Kacheln für eine Oberfläche nicht gleichzeitig zugeordnet werden müssen, wodurch die verfügbare Menge an Arbeitsspeicher effektiv genutzt wird.

In diesem Abschnitt finden Sie weitere Informationen zum Erstellen von gekachelten Ressourcen.

## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                                                                             | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                   |
|-------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Zuordnungen in einen Kachelpool](mappings-are-into-a-tile-pool.md)<br/>                                     | Wenn eine Ressource mit dem [**D3D11 \_ \_ ressourcenmisc- \_ Kachel**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag) Kennzeichen erstellt wird, stammen die Kacheln, die die Ressource bilden, von den Positionen in einem Kachel Pool. Ein Kachel Pool ist ein Arbeitsspeicher Pool (gestützt durch eine oder mehrere Zuordnungen im Hintergrund, die von der Anwendung nicht gesehen werden). <br/> |
| [Parameter für die Kachel Ressourcen Erstellung](tiled-resource-creation-parameters.md)<br/>                           | Es gibt einige Einschränkungen für den Typ der Direct3D-Ressourcen, die Sie mit dem [**D3D11 \_ - \_ ressourcenmisc- \_ Kachel**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag) Kennzeichen erstellen können. Dieser Abschnitt enthält die gültigen Parameter zum Erstellen von gekachelten Ressourcen.<br/>                                                |
| [Für Kachel Ressourcen verfügbarer Adressraum](address-space-available-for-tiled-resources.md)<br/>         | In diesem Abschnitt wird der virtuelle Adressraum angegeben, der für Kachel Ressourcen verfügbar ist. <br/>                                                                                                                                                                                                                           |
| [Parameter zum Erstellen des Kachelpools](tile-pool-creation-parameters.md)<br/>                                     | Verwenden Sie die Parameter in diesem Abschnitt, um Kachel Pools über die [**ID3D11Device::**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createbuffer) -API zu definieren. <br/>                                                                                                                                                                              |
| [Prozessübergreifende Ressourcen übergreifende und Geräte Freigabe](tiled-resource-cross-process-and-device-sharing.md)<br/> | Kachel Pools können ebenso wie herkömmliche Ressourcen für andere Prozesse freigegeben werden. Kachel Ressourcen, die auf Kachel Pools verweisen, können nicht für Geräte und Prozesse freigegeben werden. Separate Prozesse können jedoch eigene Kachel Ressourcen erstellen, die Kachel Pools zugeordnet sind, die von diesen Kachel Ressourcen gemeinsam genutzt werden. <br/>          |
| [Auf gekachelten Ressourcen verfügbare Vorgänge](operations-available-on-tiled-resources.md)<br/>                 | In diesem Abschnitt werden Vorgänge aufgelistet, die Sie für gekachelte Ressourcen ausführen können.<br/>                                                                                                                                                                                                                                             |
| [Vorgänge für Kachelpools](operations-available-on-tile-pools.md)<br/>                           | In diesem Abschnitt werden Vorgänge aufgelistet, die Sie für Kachel Pools ausführen können.<br/>                                                                                                                                                                                                                                                  |
| [Kacheln eines gekachelten Ressourcenbereichs](how-a-tiled-resource-s-area-is-tiled.md)<br/>                       | Wenn Sie eine Kachel Ressource erstellen, bestimmen Dimensionen, Format Elementgröße und Anzahl von Mipmaps und/oder Array Slices (falls zutreffend) die Anzahl der Kacheln, die für die gesamte Oberfläche benötigt werden. <br/>                                                                                                 |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Gekachelte Ressourcen](tiled-resources.md)
</dt> </dl>

 

 





