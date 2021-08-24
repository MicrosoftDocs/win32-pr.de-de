---
title: Erstellen von gekachelten Ressourcen
description: Gekachelte Ressourcen werden erstellt, indem beim Erstellen einer Ressource das FLAG D3D11 \_ RESOURCE \_ MISC \_ TILED angegeben wird.
ms.assetid: DED2B70C-1E95-4A85-A818-FD32165FBF6C
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 657fc2cca4d5c1d8fce9efba2013d3cd04291efc7f40d44b4ed325e40f843358
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119752580"
---
# <a name="creating-tiled-resources"></a>Erstellen von gekachelten Ressourcen

Gekachelte Ressourcen werden erstellt, indem beim Erstellen einer Ressource das [**Flag D3D11 \_ RESOURCE \_ MISC \_ TILED**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag) angegeben wird.

Einschränkungen für die Verwendung von [**D3D11 \_ RESOURCE \_ MISC \_ TILED**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag) zum Erstellen einer Ressource werden unter Parameter für die Erstellung von [gekachelten Ressourcen beschrieben.](tiled-resource-creation-parameters.md)

Der Speicher einer nicht gekachelten Ressource wird beim Erstellen der Ressource im Grafiksystem zugeordnet. Wenn Sie beispielsweise [**ID3D11Device::CreateTexture2D**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createtexture2d) aufrufen, um ein Array von 2D-Texturen zu erstellen, ordnet das Grafiksystem Speicher für diese 2D-Texturen zu. Wenn eine gekachelte Ressource erstellt wird, ordnet das Grafiksystem den Speicher für den Ressourceninhalt nicht zu. Wenn eine Anwendung stattdessen eine gekachelte Ressource erstellt, erstellt das Grafiksystem eine Adressraumreservierung nur für den Bereich der kachelierten Oberfläche und ermöglicht dann die Zuordnung der Kacheln, die von der Anwendung gesteuert werden können. Die "Zuordnung" einer Kachel ist einfach der physische Speicherort im Arbeitsspeicher, auf den eine logische Kachel in einer Ressource verweist (oder **NULL** für eine nicht zugeordnete Kachel). Verwechseln Sie dieses Konzept nicht mit dem Konzept der Zuordnung einer Direct3D-Ressource für den CPU-Zugriff, die trotz der Verwendung desselben Namens vollständig unabhängig ist. Sie können die Zuordnung der einzelnen Kacheln nach Bedarf einzeln definieren und ändern. Dabei wissen Sie, dass nicht alle Kacheln für eine Oberfläche gleichzeitig zugeordnet werden müssen, wodurch die verfügbare Arbeitsspeichermenge effektiv verwendet wird.

Dieser Abschnitt enthält weitere Informationen zum Erstellen von gekachelten Ressourcen.

## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                                                                             | Beschreibung                                                                                                                                                                                                                                                                                                                   |
|-------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Zuordnungen in einen Kachelpool](mappings-are-into-a-tile-pool.md)<br/>                                     | Wenn eine Ressource mit dem [**FLAG D3D11 \_ RESOURCE \_ MISC \_ TILED**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag) erstellt wird, stammen die Kacheln, aus denen die Ressource besteht, aus dem Zeigen auf Speicherorte in einem Kachelpool. Ein Kachelpool ist ein Speicherpool (unterstützt durch eine oder mehrere Zuordnungen im Hintergrund – von der Anwendung nicht angezeigt). <br/> |
| [Parameter für die Erstellung von gekachelten Ressourcen](tiled-resource-creation-parameters.md)<br/>                           | Es gibt einige Einschränkungen für den Typ der Direct3D-Ressourcen, die Sie mit dem [**FLAG D3D11 \_ RESOURCE \_ MISC \_ TILED erstellen**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag) können. Dieser Abschnitt enthält die gültigen Parameter zum Erstellen von gekachelten Ressourcen.<br/>                                                |
| [Verfügbarer Adressraum für gekachelte Ressourcen](address-space-available-for-tiled-resources.md)<br/>         | In diesem Abschnitt wird der virtuelle Adressraum angegeben, der für gekachelte Ressourcen verfügbar ist. <br/>                                                                                                                                                                                                                           |
| [Parameter zum Erstellen des Kachelpools](tile-pool-creation-parameters.md)<br/>                                     | Verwenden Sie die Parameter in diesem Abschnitt, um Kachelpools über die [**ID3D11Device::CreateBuffer-API zu**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createbuffer) definieren. <br/>                                                                                                                                                                              |
| [Prozessübergreifende und Gerätefreigabe gekachelte Ressourcen](tiled-resource-cross-process-and-device-sharing.md)<br/> | Kachelpools können wie herkömmliche Ressourcen für andere Prozesse freigegeben werden. Gekachelte Ressourcen, die auf Kachelpools verweisen, können nicht geräte- und prozessübergreifend freigegeben werden. Separate Prozesse können jedoch eigene gekachelte Ressourcen erstellen, die Kachelpools zuordnen, die von diesen gekachelten Ressourcen gemeinsam genutzt werden. <br/>          |
| [Vorgänge, die für gekachelte Ressourcen verfügbar sind](operations-available-on-tiled-resources.md)<br/>                 | In diesem Abschnitt werden Vorgänge aufgeführt, die Sie für gekachelte Ressourcen ausführen können.<br/>                                                                                                                                                                                                                                             |
| [Vorgänge für Kachelpools](operations-available-on-tile-pools.md)<br/>                           | In diesem Abschnitt werden Vorgänge aufgeführt, die Sie für Kachelpools ausführen können.<br/>                                                                                                                                                                                                                                                  |
| [Kacheln des Bereichs einer gekachelten Ressource](how-a-tiled-resource-s-area-is-tiled.md)<br/>                       | Wenn Sie eine gekachelte Ressource erstellen, bestimmen die Dimensionen, die Formatelementgröße und die Anzahl der Mipmaps und/oder Arrayslices (falls zutreffend) die Anzahl der Kacheln, die zum Sichern der gesamten Oberfläche erforderlich sind. <br/>                                                                                                 |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Gekachelte Ressourcen](tiled-resources.md)
</dt> </dl>

 

 





