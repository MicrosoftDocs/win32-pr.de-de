---
title: Standardtexturzuordnung
description: Die Verwendung der Standardtexturzuordnung reduziert die Kopier- und Arbeitsspeicherauslastung, während Bilddaten zwischen GPU und CPU freigegeben werden.
ms.assetid: 77AF4BFA-09B5-4181-9408-002764F2A923
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: edc81fc1bf59a974f9bd901fc96d43afc16019edce68fbaabfbf3259c0d4a3b9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119752290"
---
# <a name="default-texture-mapping"></a>Standardtexturzuordnung

Die Verwendung der Standardtexturzuordnung reduziert die Kopier- und Arbeitsspeicherauslastung, während Bilddaten zwischen GPU und CPU freigegeben werden. Sie sollte jedoch nur in bestimmten Situationen verwendet werden. Das standardmäßige Swizzlelayout vermeidet das Kopieren oder Wischen von Daten in mehreren Layouts.

-   [Übersicht](#overview)
-   [D3D11.3-APIs](#d3d113-apis)
-   [Zugehörige Themen](#related-topics)

## <a name="overview"></a>Übersicht

Das Zuordnen von Standardtexturen sollte für Entwickler nicht die erste Wahl sein. Entwickler sollten zuerst diskret-GPU-freundlichen Code erstellen (d.amp;n.b. keinen CPU-Zugriff für den Großteil der Texturen haben und mit [**CopySubresourceRegion1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-copysubresourceregion1)hochladen). In bestimmten Fällen interagieren CPU und GPU jedoch möglicherweise so häufig mit denselben Daten, dass die Zuordnung von Standardtexturen hilfreich ist, um Energie zu sparen oder ein bestimmtes Design auf bestimmten Adaptern oder Architekturen zu beschleunigen. Anwendungen sollten diese Fälle erkennen und die unnötigen Kopien optimieren.

In D3D11.3 sind Texturen, die mit D3D11 \_ TEXTURE \_ LAYOUT \_ UNDEFINED (einem Member der [**D3D11 \_ TEXTURE \_ LAYOUT-Enumeration)**](/windows/desktop/api/D3D11_3/ne-d3d11_3-d3d11_texture_layout) und ohne CPU-Zugriff erstellt wurden, die effizienteste Für häufige GPU-Renderings und Samplings. Bei Leistungstests sollten diese Texturen mit D3D11 \_ TEXTURE \_ LAYOUT \_ UNDEFINED mit CPU-Zugriff und D3D11 \_ TEXTURE LAYOUT \_ \_ 64K \_ STANDARD \_ SWIZZLE mit \_ \_ \_ CPU-Zugriff und D3D11 TEXTURE LAYOUT ROW \_ MAJOR für adapterübergreifende Unterstützung verglichen werden.

Die Verwendung von D3D11 \_ TEXTURE \_ LAYOUT \_ UNDEFINED mit CPU-Zugriff ermöglicht die Methoden [**WriteToSubresource,**](/windows/desktop/api/d3d11_3/nf-d3d11_3-id3d11device3-writetosubresource) [**ReadFromSubresource,**](/windows/desktop/api/d3d11_3/nf-d3d11_3-id3d11device3-readfromsubresource) [**Map**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map) (ohne Anwendungszugriff auf Zeiger) und [**Unmap;**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-unmap)kann jedoch die Effizienz des GPU-Zugriffs beeinträchtigen. Die Verwendung von D3D11 \_ TEXTURE \_ LAYOUT \_ 64K \_ STANDARD \_ SWIZZLE mit CPU-Zugriff ermöglicht **WriteToSubresource,** **ReadFromSubresource,** **Map** (gibt einen gültigen Zeiger auf die Anwendung zurück) und **Unmap**. Sie kann auch die Effizienz des GPU-Zugriffs mehr als D3D11 \_ TEXTURE \_ LAYOUT \_ UNDEFINED mit CPU-Zugriff abkraften.

Im Allgemeinen sollten Anwendungen den Großteil der Texturen als nur gpu-zugänglich und mit D3D11 \_ TEXTURE \_ LAYOUT \_ UNDEFINED erstellen.

Vor der Standardtexturfunktion der Zuordnung gab es nur ein standardisiertes Layout für mehrdimensionale Daten: "linear", auch als "Zeilen-Hauptversion" bezeichnet. Anwendungen sollten USAGE \_ STAGING- und USAGE \_ DYNAMIC-Texturen vermeiden, wenn die Kartenstandardeinstellung verfügbar ist. Die \_ TEXTUREn USAGE STAGING und USAGE DYNAMIC verwenden das \_ lineare Layout.

D3D11.3 (und D3D12) führen ein standardmäßiges mehrdimensionales Datenlayout ein. Dadurch können mehrere Verarbeitungseinheiten mit denselben Daten arbeiten, ohne die Daten zu kopieren oder zwischen mehreren Layouts zu wischen. Ein standardisiertes Layout ermöglicht Effizienzsteigerungen durch Netzwerkeffekte und ermöglicht es Algorithmen, kurze Schnitte unter Der Annahme eines bestimmten Musters vorzunehmen.

Beachten Sie jedoch, dass diese Standardmäßig-Swizzle ein Hardwarefeature ist und möglicherweise nicht von allen GPUs unterstützt wird.

## <a name="d3d113-apis"></a>D3D11.3-APIs

Im Gegensatz zu D3D12 unterstützt D3D11.3 standardmäßig keine Texturzuordnung. Daher müssen Sie [**D3D11 \_ FEATURE \_ DATA \_ D3D11 \_ OPTIONS2**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options2)abfragen. Standard-Swizzle muss auch mit einem Aufruf von [**ID3D11Device::CheckFeatureSupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport) abgefragt und das `StandardSwizzle64KBSupported` Feld von **D3D11 \_ FEATURE DATA \_ \_ D3D11 \_ OPTIONS2** überprüft werden.

Die folgenden APIs verweisen auf die Texturzuordnung:

Enumerationen

-   [**D3D11 \_ \_TEXTURLAYOUT:**](/windows/desktop/api/D3D11_3/ne-d3d11_3-d3d11_texture_layout) Steuert das Swizzlemuster von Standardtexturen und aktiviert die Kartenunterstützung für Standardtexturen.
-   [**D3D11 \_ FEATURE:**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_feature) verweist auf [**D3D11 \_ FEATURE DATA \_ \_ D3D11 \_ OPTIONS2**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options2).
-   [**D3D11 \_ TILE \_ COPY \_ FLAG:**](/windows/desktop/api/D3D11_2/ne-d3d11_2-d3d11_tile_copy_flag) Enthält Flags zum Kopieren von gezischen Kachelressourcen in und aus linearen Puffern.

Strukturen

-   [**D3D11 \_ TEXTURE2D \_ DESC1:**](/windows/desktop/api/D3D11_3/ns-d3d11_3-cd3d11_texture2d_desc1) Beschreibt eine 2D-Textur. Beachten Sie die CD3D11 \_ TEXTURE2D \_ DESC1-Hilfsstruktur.
-   [**D3D11 \_ TEXTURE3D \_ DESC1:**](/windows/desktop/api/D3D11_3/ns-d3d11_3-cd3d11_texture3d_desc1) Beschreibt eine 3D-Textur. Beachten Sie die HILFSSTRUKTUR CD3D11 \_ TEXTURE3D \_ DESC1.

Methoden

-   [**ID3D11Device3::CreateTexture2D1:**](/windows/desktop/api/D3D11_3/nf-d3d11_3-id3d11device3-createtexture2d1) erstellt ein Array von 2D-Texturen.
-   [**ID3D11Device3::CreateTexture3D1**](/windows/desktop/api/D3D11_3/nf-d3d11_3-id3d11device3-createtexture3d1) : erstellt eine einzelne 3D-Textur.
-   [**ID3D11Device3::WriteToSubresource:**](/windows/desktop/api/d3d11_3/nf-d3d11_3-id3d11device3-writetosubresource) kopiert Daten in eine D3D11 \_ USAGE \_ DEFAULT-Textur, die mit [**map**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map)zugeordnet wurde.
-   [**ID3D11Device3::ReadFromSubresource:**](/windows/desktop/api/d3d11_3/nf-d3d11_3-id3d11device3-readfromsubresource) kopiert Daten aus einer D3D11 \_ USAGE \_ DEFAULT-Textur, die mit [**map**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map)zugeordnet wurde.
-   [**ID3D11DeviceContext::Map:**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map) Ruft einen Zeiger auf die in einer Unterressource enthaltenen Daten ab und verweigert der GPU den Zugriff auf diese Unterressource.
-   [**ID3D11DeviceContext::Unmap**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-unmap) : Macht den Zeiger auf eine Ressource ungültig und gibt den GPU-Zugriff auf diese Ressource erneut frei.
-   [**ID3D11Texture2D1::GetDesc1**](/windows/desktop/api/D3D11_3/nf-d3d11_3-id3d11texture2d1-getdesc1) : Ruft die Eigenschaften einer 2D-Texturressource ab.
-   [**ID3D11Texture3D1::GetDesc1**](/windows/desktop/api/D3D11_3/nf-d3d11_3-id3d11texture3d1-getdesc1) : Ruft die Eigenschaften einer 3D-Texturressource ab.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Direct3D 11.3-Features](direct3d-11-3-features.md)
</dt> </dl>

 

 




