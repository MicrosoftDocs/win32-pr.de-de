---
title: Zuordnungen in einen Kachelpool
description: Wenn eine Ressource mit dem FLAG D3D11 RESOURCE MISC TILED erstellt wird, stammen die Kacheln, aus denen die Ressource besteht, aus dem Zeigen auf Speicherorte \_ \_ in einem \_ Kachelpool.
ms.assetid: 1DBE23B2-A1E6-4491-9B74-4E92508A68FC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d4a31d2e8cd4457281c047db514dd2450d3bf70d85be7e4933cb7e5f5e026a5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119045618"
---
# <a name="mappings-are-into-a-tile-pool"></a>Zuordnungen in einen Kachelpool

Wenn eine Ressource mit dem [**FLAG D3D11 \_ RESOURCE \_ MISC \_ TILED**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag) erstellt wird, stammen die Kacheln, aus denen die Ressource besteht, aus dem Zeigen auf Speicherorte in einem Kachelpool. Ein Kachelpool ist ein Pool mit Arbeitsspeicher (unterstützt durch eine oder mehrere Zuordnungen im Hintergrund – von der Anwendung nicht angezeigt). Das Betriebssystem und der Anzeigetreiber verwalten diesen Speicherpool, und der Speicherbedarf ist für eine Anwendung leicht verständlich. Gekachelte Ressourcen ordnen Regionen mit 64 KB zu, indem sie auf Speicherorte in einem Kachelpool verweisen. Ein Fallout dieses Setups besteht in der Möglichkeit, dass mehrere Ressourcen dieselben Kacheln freigeben und wiederverwenden sowie dieselben Kacheln bei Wunsch an verschiedenen Speicherorten innerhalb einer Ressource wiederverwenden können.

Die Kosten für die Flexibilität des Aufsättigens der Kacheln für eine Ressource aus einem Kachelpool sind, dass die Ressource die Arbeit zum Definieren und Verwalten der Zuordnung der Kacheln im Kachelpool für die für die Ressource erforderlichen Kacheln tun muss. Kachelzuordnungen können geändert werden. Außerdem müssen nicht alle Kacheln in einer Ressource gleichzeitig zugeordnet werden. Eine Ressource kann **NULL-Zuordnungen** haben. Eine **NULL-Zuordnung** definiert, dass eine Kachel aus Sicht der Ressource, die darauf zutritt, nicht verfügbar ist.

Es können mehrere Kachelpools erstellt werden, und eine beliebige Anzahl von gekachelten Ressourcen kann gleichzeitig einem beliebigen Kachelpool zuordnen. Kachelpools können auch wachsen oder verkleinern werden. Weitere Informationen finden Sie unter [Ändern der Größe des Kachelpools.](tile-pool-resizing.md) Eine Einschränkung, die zur Vereinfachung der Implementierung des Anzeigetreibers und der Laufzeit vorhanden ist, ist, dass eine bestimmte gekachelte Ressource nur Zuordnungen zu mindestens einem Kachelpool gleichzeitig haben kann (im Gegensatz zur gleichzeitigen Zuordnung zu mehreren Kachelpools).

Die Speichermenge, die einer gekachelten Ressource selbst zugeordnet ist (d. h. unabhängiger Kachelpoolspeicher), ist ungefähr proportional zur Anzahl der Kacheln, die dem Pool tatsächlich zu einem bestimmten Zeitpunkt zugeordnet sind. Bei der Hardware wird der Speicherbedarf für den Seitentabellenspeicher in etwa mit der Menge der zugeordneten Kacheln skaliert (z. B. mithilfe eines mehrstufigen Seitentabellenschemas).

Der Kachelpool kann als vollständige Softwareabstraktion betrachtet werden, die es Direct3D-Anwendungen ermöglicht, die Seitentabellen effektiv auf der Grafikprozessor (Graphics Processing Unit, GPU) zu programmieren, ohne die Implementierungsdetails auf niedriger Ebene kennen zu müssen (oder zeigeradressen direkt verarbeiten zu müssen). Kachelpools wenden keine zusätzlichen Deskriptionsgrade auf Hardware an. Optimierungen einer Einzelebenen-Seitentabelle mithilfe von Konstrukten wie Seitenverzeichnissen sind unabhängig vom Konzept des Kachelpools.

Sehen wir uns an, welchen Speicher die Seitentabelle selbst im schlimmsten Fall benötigen könnte (implementierungen erfordern jedoch in der Praxis nur Speicher, der ungefähr proportional zu dem ist, was zugeordnet ist).

Angenommen, jeder Seitentabelleneintrag ist 64 Bits.

Für den ungünstigsten Seitentabellengrößentreffer für eine einzelne Oberfläche, wenn die Ressourcenlimits in Direct3D 11 gegeben sind, nehmen wir an, dass eine gekachelte Ressource mit einem 128-Bit-pro-Element-Format erstellt wird (z. B. rgba float), sodass eine Kachel mit 64 KB nur 4096 Pixel enthält. Die maximal unterstützte [**Textur2DArray-Größe**](/windows/desktop/direct3dhlsl/sm5-object-texture2darray) von 16384 \* 16384 2048 (aber nur mit einer einzelnen Mipmap) würde etwa 1 GB Speicher in der Seitentabelle erfordern, wenn sie mithilfe von 64-Bit-Tabelleneinträgen vollständig aufgefüllt \* wird (ohne Mipmaps). Das Hinzufügen von Mipmaps würde den vollständig zugeordneten Seitentabellenspeicher (im schlimmsten Fall) um etwa ein Drittel auf etwa 1,3 GB erweitern.

In diesem Fall erhalten Sie Zugriff auf etwa 10,6 Terabyte adressierbaren Arbeitsspeicher. Es kann jedoch eine Beschränkung für die Menge des adressierbaren Arbeitsspeichers geben, die diese Mengen reduzieren würde, z. B. auf etwa den Terabytebereich.

Ein weiterer zu berücksichtigendes Fall ist eine einzelne kachelgekachelte [**Texture2D-Ressource**](/windows/desktop/direct3dhlsl/sm5-object-texture2d) von 16384 \* 16384 mit einem 32-Bit-pro-Element-Format, einschließlich Mipmaps. Der in einer vollständig aufgefüllten Seitentabelle benötigte Speicherplatz beträgt ungefähr 170 KB mit 64-Bit-Tabelleneinträgen.

Betrachten Sie abschließend ein Beispiel mit einem BC-Format, z. B. BC7 mit 128 Bits pro Kachel von 4 x 4 Pixeln. Dies ist ein Byte pro Pixel. Ein [**Texture2DArray**](/windows/desktop/direct3dhlsl/sm5-object-texture2darray) von 16384 \* 16384 \* 2048 einschließlich mipmaps würde ungefähr 85 MB erfordern, um diesen Arbeitsspeicher in einer Seitentabelle vollständig zu füllen. Dies ist nicht schlecht, da eine gekachelte Ressource 550 Gigapixel (in diesem Fall 512 GB Arbeitsspeicher) umfassen kann.

In der Praxis würden nahezu diese vollständigen Zuordnungen definiert, da die Menge des verfügbaren physischen Arbeitsspeichers nicht zu einer bestimmten Zeit zugeordnet und referenziert werden würde. Mit einem Kachelpool können Anwendungen jedoch Kacheln wiederverwenden (als einfaches Beispiel eine "schwarze" Kachel für große schwarze Bereiche in einem Bild wiederverwenden) – effektiv mithilfe des Kachelpools (d. h. Seitentabellenzuordnungen) als Tool für die Speicherkomprimierung.

Der ursprüngliche Inhalt der Seitentabelle ist **NULL für** alle Einträge. Anwendungen können auch keine anfänglichen Daten für den Arbeitsspeicherinhalt der Oberfläche übergeben, da sie ohne Speicherbewegung beginnen.

## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                                                                   | Beschreibung                                                                                                                                                                                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Erstellung eines Kachelpools](tile-pool-creation.md)<br/>                                                 | Ein Kachelpool wird über die [**ID3D11Device::CreateBuffer-API**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createbuffer) erstellt, indem das [**FLAG D3D11 \_ RESOURCE \_ MISC TILE \_ \_ POOL**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag) im **MiscFlags-Member** der [**D3D11 \_ BUFFER \_ DESC-Struktur**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_desc) übergeben wird, auf die der *pDesc-Parameter* verweist. <br/> |
| [Ändern der Größe des Kachelpools](tile-pool-resizing.md)<br/>                                                 | Verwenden Sie die [**ID3D11DeviceContext2::ResizeTilePool-API,**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-resizetilepool) um einen Kachelpool zu vergrößern, wenn die Anwendung mehr Arbeitssatz für die Zuordnung der gekachelten Ressourcen benötigt oder verkleinert werden soll, wenn weniger Speicherplatz erforderlich ist. <br/>                                                                                                                    |
| [Gefahrennachverfolgung im Vergleich mit den Kachelpoolressourcen](hazard-tracking-versus-tile-pool-resources.md)<br/> | Bei nicht gekachelten Ressourcen kann Direct3D bestimmte Gefährdungsbedingungen während des Renderings verhindern, aber da die Risikonachverfolgung auf Kachelebene für gekachelte Ressourcen liegt, ist die Nachverfolgung von Gefährdungsbedingungen während des Renderings von gekachelten Ressourcen möglicherweise zu teuer. <br/>                                                                                                     |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Erstellen von gekachelten Ressourcen](creating-tiled-resources.md)
</dt> </dl>

 

