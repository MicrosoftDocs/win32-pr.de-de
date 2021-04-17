---
title: Standard Textur Zuordnung
description: Die Verwendung der standardtextur Zuordnung reduziert das Kopieren und die Arbeitsspeicher Auslastung bei der Freigabe von Bilddaten zwischen GPU und CPU.
ms.assetid: 77AF4BFA-09B5-4181-9408-002764F2A923
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f203c7590c3673d30315250b2b4ce2663e48c9c3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388317"
---
# <a name="default-texture-mapping"></a>Standard Textur Zuordnung

Die Verwendung der standardtextur Zuordnung reduziert das Kopieren und die Arbeitsspeicher Auslastung bei der Freigabe von Bilddaten zwischen GPU und CPU. Es sollte jedoch nur in bestimmten Situationen verwendet werden. Das standardmäßige Swizzle-Layout vermeidet das Kopieren oder Schwenken von Daten in mehreren Layouts.

-   [Übersicht](#overview)
-   [D3D 11.3-APIs](#d3d113-apis)
-   [Zugehörige Themen](#related-topics)

## <a name="overview"></a>Übersicht

Die Zuordnung von Standard Texturen sollte für Entwickler nicht die erste Wahl sein. Entwickler sollten zuerst in einer diskreten GPU-Methode programmieren (d. h., Sie haben keinen CPU-Zugriff für die Mehrzahl der Texturen und hochladen mit [**CopySubresourceRegion1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-copysubresourceregion1)). In bestimmten Fällen können die CPU und die GPU jedoch so häufig auf denselben Daten interagieren, dass die Zuordnung von Standard Texturen hilfreich ist, um Energie zu sparen oder einen bestimmten Entwurf für bestimmte Adapter oder Architekturen zu beschleunigen. Anwendungen sollten diese Fälle erkennen und die unnötigen Kopien optimieren.

In D3D 11.3 sind Texturen, die mit \_ \_ dem D3D11-Textur Layout definiert wurden \_ (ein Member der [**D3D11 \_ Textur \_ Layout**](/windows/desktop/api/D3D11_3/ne-d3d11_3-d3d11_texture_layout) -Enumeration) und kein CPU-Zugriff, die effizienteste für häufiges GPU-Rendering und Sampling. Beim Testen der Leistung sollten diese Texturen mit dem D3D11- \_ Textur \_ Layout verglichen werden, das mit dem \_ CPU-Zugriff nicht definiert ist, und dem D3D11- \_ Textur \_ Layout \_ 64K-Standard- \_ \_ Swizzle mit CPU-Zugriff und D3D11 \_ Textur \_ Layout \_ Row \_ Major für Adapter übergreifende Unterstützung.

Bei Verwendung \_ \_ des D3D11-Textur Layouts, \_ das mit dem CPU-Zugriff [**nicht**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-unmap)definiert ist, werden die Methoden " [**Beschreib tedesubresource**](/windows/desktop/api/d3d11_3/nf-d3d11_3-id3d11device3-writetosubresource)", "read [**fromsubresource**](/windows/desktop/api/d3d11_3/nf-d3d11_3-id3d11device3-readfromsubresource)", " [**map**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map) " (Ausschluss des Anwendungs Zugriffs auf Zeiger) und die Zuordnung aufgehoben. Die Verwendung des D3D11 \_ Texture \_ Layout \_ 64K \_ Standard- \_ Swizzle mit dem CPU-Zugriff ermöglicht das Schreiben von "Write- **desubresource**", "read **fromsubresource**", " **map** " (gibt einen gültigen Zeiger auf die Anwendung zurück) und die Zuordnung Außerdem kann die Effizienz des GPU-Zugriffs mehr als das D3D11- \_ Textur \_ Layout \_ mit dem CPU-Zugriff nicht definiert werden.

Im Allgemeinen sollten Anwendungen die Mehrzahl der Texturen als nur GPU-Zugriff und mit nicht definiertem D3D11- \_ Textur \_ Layout erstellen \_ .

Vor dem Feature für die Zuordnung von Standard Texturen gab es nur ein standardisiertes Layout für mehrdimensionale Daten: "Linear", auch bekannt als "Row-Major". Anwendungen sollten Verwendungs \_ -und Verwendungs \_ dynamische Texturen vermeiden, wenn der Karten Standard verfügbar ist. Die \_ dynamischen Texturen Verwendungs Staging und Verwendung \_ verwenden das lineare Layout.

D3D 11.3 (und D3D12) stellen ein Standardmäßiges mehrdimensionales Datenlayout dar. Dies erfolgt, damit mehrere Verarbeitungseinheiten mit denselben Daten arbeiten können, ohne die Daten zu kopieren oder die Daten zwischen mehreren Layouts zu schwenken. Ein standardisiertes Layout ermöglicht Effizienzsteigerungen durch Netzwerkeffekte und ermöglicht es Algorithmen, kurze Einschnitte bei einem bestimmten Muster zu ermöglichen.

Beachten Sie, dass es sich bei diesem Standard-Swizzle um eine Hardware Funktion handelt, die möglicherweise nicht von allen GPUs unterstützt wird.

## <a name="d3d113-apis"></a>D3D 11.3-APIs

Im Gegensatz zu D3D12 unterstützt D3D 11.3 standardmäßig keine Textur Zuordnung. Daher müssen Sie [**D3D11 \_ Feature \_ Data \_ D3D11 \_ OPTIONS2**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options2)Abfragen. Standard-Swizzle muss auch mit einem [**ID3D11Device:: checkfeaturesupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport) -Befehl abgefragt und das `StandardSwizzle64KBSupported` Feld von **D3D11 \_ Feature \_ Data \_ D3D11 \_ OPTIONS2** überprüft werden.

Die folgenden APIs verweisen auf die Textur Zuordnung:

Enumerationen

-   [**D3D11 \_ Textur \_ Layout**](/windows/desktop/api/D3D11_3/ne-d3d11_3-d3d11_texture_layout) : steuert das swidingmuster von Standard Texturen und ermöglicht die Unterstützung von Zuordnungen auf Standard Texturen.
-   [**D3D11 \_ Feature**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_feature) : References [**D3D11 \_ Feature \_ Data \_ D3D11 \_ OPTIONS2**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options2).
-   [**D3D11 \_ Kachel \_ \_ kopierungsflag**](/windows/desktop/api/D3D11_2/ne-d3d11_2-d3d11_tile_copy_flag) : enthält Flags zum Kopieren von gekachelten gekachelten Ressourcen in und aus linearen Puffern.

Strukturen

-   [**D3D11 \_ TEXTURE2D \_ DESC1**](/windows/desktop/api/D3D11_3/ns-d3d11_3-cd3d11_texture2d_desc1) : Beschreibt eine 2D-Textur. Beachten Sie die CD3D11 \_ TEXTURE2D \_ DESC1 Helper-Struktur.
-   [**D3D11 \_ TEXTURE3D \_ DESC1**](/windows/desktop/api/D3D11_3/ns-d3d11_3-cd3d11_texture3d_desc1) : Beschreibt eine 3D-Textur. Beachten Sie die CD3D11 \_ TEXTURE3D \_ DESC1 Helper-Struktur.

Methoden

-   [**ID3D11Device3:: CreateTexture2D1**](/windows/desktop/api/D3D11_3/nf-d3d11_3-id3d11device3-createtexture2d1) : erstellt ein Array von 2D-Texturen.
-   [**ID3D11Device3:: CreateTexture3D1**](/windows/desktop/api/D3D11_3/nf-d3d11_3-id3d11device3-createtexture3d1) : erstellt eine einzelne 3D-Textur.
-   [**ID3D11Device3:: Write-in-subresource**](/windows/desktop/api/d3d11_3/nf-d3d11_3-id3d11device3-writetosubresource) : kopiert Daten in eine \_ Standard Textur für die D3D11-Verwendung \_ , die mithilfe von [**map**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map)zugeordnet wurde.
-   [**ID3D11Device3:: Read fromsubresource**](/windows/desktop/api/d3d11_3/nf-d3d11_3-id3d11device3-readfromsubresource) : kopiert Daten aus einer \_ Standard Textur für die D3D11-Verwendung \_ , die mithilfe von [**map**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map)zugeordnet wurde.
-   [**Verknüpfung id3d11devicecontext aus:: Map**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map) : Ruft einen Zeiger auf die in einer untergeordneten Quelle enthaltenen Daten ab und verweigert den GPU-Zugriff auf diese untergeordnete Quelle.
-   [**Verknüpfung id3d11devicecontext aus:: unmap**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-unmap) : macht den Zeiger auf eine Ressource ungültig und aktiviert den GPU-Zugriff auf diese Ressource erneut.
-   [**ID3D11Texture2D1:: GetDesc1**](/windows/desktop/api/D3D11_3/nf-d3d11_3-id3d11texture2d1-getdesc1) : Ruft die Eigenschaften einer 2D-Textur Ressource ab.
-   [**ID3D11Texture3D1:: GetDesc1**](/windows/desktop/api/D3D11_3/nf-d3d11_3-id3d11texture3d1-getdesc1) : Ruft die Eigenschaften einer 3D-Textur Ressource ab.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Direct3D 11,3-Features](direct3d-11-3-features.md)
</dt> </dl>

 

 




