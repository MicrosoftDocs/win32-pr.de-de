---
title: Erstellung eines Kachelpools
description: Ein Kachel Pool wird mithilfe der ID3D11Device-API von "" erstellt, indem das Flag "D3D11 \_ \_ ressourcenmisc- \_ Kachel \_ Pool" im Fehlerflags-Member der D3D11-Puffer-Debug- \_ \_ Struktur, auf die der pdebug-Parameter verweist, übergeben wird.
ms.assetid: 751A64A6-C9B6-4797-BA1C-B3BEF655DF32
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f3b66a9a548d27382f8cbb4e447516beea6eca8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104992734"
---
# <a name="tile-pool-creation"></a>Erstellung eines Kachelpools

Ein Kachel Pool wird über die [**ID3D11Device:: featebuffer**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createbuffer) -API erstellt, indem das Flag für den [**D3D11- \_ \_ ressourcenmisc- \_ Kachel \_ Pool**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag) im **Fehlerflags** -Member der [**D3D11- \_ Puffer- \_**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_desc) Debug-Struktur, auf die der *PDE SC* -Parameter verweist, übergeben wird.

Anwendungen können einen oder mehrere Kachel Pools pro Direct3D-Gerät erstellen. Die Gesamtgröße jedes Kachel Pools ist auf die Ressourcen Größenbeschränkung von Direct3D 11 beschränkt, was ungefähr 1/4 des GPU-RAM (Graphics Processing Unit) entspricht.

Ein Kachel Pool besteht aus 64 KB-Kacheln, aber das Betriebssystem (Anzeigetreiber) verwaltet den gesamten Pool als eine oder mehrere Zuordnungen hinter den Kulissen – die Aufschlüsselung ist für Anwendungen nicht sichtbar. Gekachelte Ressourcen definieren Inhalt, indem Sie auf Kacheln innerhalb eines Kachel Pools zeigen. Wenn Sie die Zuordnung einer Kachel aus einer gekachelten Ressource entordnen, wird die Kachel auf **null** verwiesen. Solche nicht zugeordneten Kacheln verfügen über Regeln zum Verhalten von Lese-oder Schreibvorgängen. Weitere Informationen finden Sie unter [Gefahren Nachverfolgung im Vergleich zu Kachel Pool Ressourcen](hazard-tracking-versus-tile-pool-resources.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Zuordnungen in einen Kachelpool](mappings-are-into-a-tile-pool.md)
</dt> </dl>

 

 




