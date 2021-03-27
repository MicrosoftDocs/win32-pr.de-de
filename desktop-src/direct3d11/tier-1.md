---
title: Ebene 1
description: In diesem Abschnitt wird die Unterstützung für Ebene 1 beschrieben.
ms.assetid: 8E2907D2-EFCB-4F97-9B40-6835A65D3DE5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4111fa48dafa7f38a26d5ca09f95898eacef6f55
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103729945"
---
# <a name="tier-1"></a>Ebene 1

In diesem Abschnitt wird die Unterstützung für Ebene 1 beschrieben.

-   Hardware auf Featureebene 11,0.
-   Keine Unterstützung für das Durchsuchen.
-   Keine Texture1D-oder Texture3D-Unterstützung.
-   Keine 2, 8 oder 16 Sample Multisampling Antialiasing (MSAA)-Unterstützung. Nur 4X ist erforderlich, außer keine 128 bpp-Formate.
-   Kein standardmäßiges Verhalten (das Layout in Kacheln mit 64 KB und die End-MIP-Komprimierung ist der Hardwarehersteller).
-   Einschränkungen für den Zugriff auf Kacheln, wenn doppelte Zuordnungen vorhanden sind, beschrieben unter [Kachel Zugriffs Einschränkungen mit doppelten](tile-access-limitations-with-duplicate-mappings-.md)Zuordnungen.

### <a name="limitations-affecting-tier-1-only"></a>Einschränkungen, die nur die Ebene 1 betreffen

-   Gekachelte Ressourcen können **null** -Zuordnungen aufweisen, aber das Lesen aus Ihnen oder das Schreiben in Sie erzeugt nicht definierte Ergebnisse, einschließlich des entfernten Geräts. Anwendungen können dies umgehen, indem Sie alle leeren Bereiche einer einzelnen Dummy-Seite Mapping. Achten Sie darauf, dass Sie schreiben und auf eine Seite Renderen, die mehreren renderzielstandorten zugeordnet ist, da die Reihenfolge der Schreibvorgänge nicht definiert ist.
-   Shaderanweisungen zum Einspannen von Lod und zugeordnetem Status Feedback sind nicht verfügbar. Weitere Informationen finden Sie unter Verfügbarkeit von [HLSL-gekachelten Ressourcen](hlsl-tiled-resources-exposure.md).
-   Ausrichtungs Einschränkungen für Standard Kachel Formen: Es wird nur sichergestellt, dass MIPS (beginnend mit dem feinsten), dessen Dimensionen alle Vielfachen der Standard Kachel Größe sind, die Standard Kachel Formen unterstützen und einzelne Kacheln willkürlich zugeordnet/nicht zugeordnet werden können. Die erste MipMap in einer gekachelten Ressource, die eine beliebige Dimension, nicht das Vielfache der Standard Kachel Größe, zusammen mit sämtlichen gröbere-Mipmaps enthält, kann über eine nicht standardmäßige tipeform verfügen, die für diesen Satz von MIPS gleichzeitig (n an die Anwendung gemeldet) angepasst wird. Diese N Kacheln werden als eine Einheit verpackt, die von der Anwendung zu einem beliebigen Zeitpunkt vollständig zugeordnet oder vollständig vollständig zugeordnet werden muss. die Zuordnungen der einzelnen N-Kacheln können sich jedoch an willkürlich nicht zusammenhängenden Positionen in einem Kachel Pool befinden.
-   Für gekachelte Ressourcen mit allen Mipmaps, die nicht ein Vielfaches der Standard Kachel Größe in allen Dimensionen sind, darf die Array Größe nicht größer als 1 sein.
-   Um zwischen verweisenden Kacheln in einem Kachel Pool über eine [Puffer](overviews-direct3d-11-resources-buffers.md) Ressource zu wechseln, um über eine [Textur](overviews-direct3d-11-resources-textures.md) Ressource auf die gleichen Kacheln zu verweisen, oder umgekehrt müssen die letzten Aufrufe von [**updatetilemappings**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-updatetilemappings) oder [**copytilemappings**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-copytilemappings) , die die Zuordnungen für diese Kachel Pool Kacheln definieren, für dieselbe Ressourcen Dimension (Puffer und Textur) wie für die Ressourcen Dimension gelten, die \* für den Zugriff auf die Kacheln verwendet werden. Andernfalls ist das Verhalten nicht definiert, einschließlich der Gefahr, dass das Gerät zurückgesetzt wird. Wenn Sie z. b. **updatetilemappings** aufrufen, um Kachel Zuordnungen für einen Puffer zu definieren, werden **updatetilemappings** über eine [**Texture2D**](/windows/desktop/direct3dhlsl/sm5-object-texture2d) -Ressource zu denselben Kacheln im Kachel Pool, und der Zugriff auf die Kacheln über den Puffer ist ungültig. Die Umgehung von Aufgaben besteht darin, die Kachel Zuordnungen für eine Ressource neu zu definieren, wenn Sie Zwischenpuffer und Textur wechseln (oder umgekehrt), indem Sie Kacheln gemeinsam nutzen oder nur Kacheln in einem Kachel Pool Zwischenpuffer Ressourcen und Textur Ressourcen freigeben.
-   Die minimale/maximale Reduzierungs Filterung wird nicht unterstützt. Informationen zur minimalen/maximalen Reduzierungs Filterung finden Sie unter [Kacheln von Funktionen für Textur Stichproben](tiled-resources-texture-sampling-features.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Tarife der Kachel "Ressourcen"](tiled-resources-features-tiers.md)
</dt> </dl>

 

 