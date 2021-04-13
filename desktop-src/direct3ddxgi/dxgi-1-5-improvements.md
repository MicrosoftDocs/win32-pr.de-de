---
description: Die folgenden Funktionen wurden der Microsoft DirectX Graphics Infrastructure (DXGI) 1,5 hinzugefügt, um eine flexiblere Angabe und Duplizierung von Ausgabeformaten zu unterstützen.
ms.assetid: DD7401E1-9991-48D8-AD23-4D34238EA4AF
title: DXGI 1,5-Verbesserungen
ms.topic: article
ms.date: 03/05/2021
ms.openlocfilehash: 58df3ef78781437ee033530a2ed2179bb9a132d8
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/06/2021
ms.locfileid: "104351928"
---
# <a name="dxgi-15-improvements"></a>DXGI 1,5-Verbesserungen

Die folgenden Funktionen wurden der Microsoft DirectX Graphics Infrastructure (DXGI) 1,5 hinzugefügt, um eine flexiblere Angabe und Duplizierung von Ausgabeformaten zu unterstützen.

## <a name="high-dynamic-range-and-wide-color-gamut"></a>Hoher dynamischer Bereich und breite Farbpalette

Weitere Informationen finden Sie unter [Verwenden von DirectX mit dynamischen Bereichs anzeigen und](../direct3darticles/high-dynamic-range.md)erweiterter Farbe.

## <a name="variable-refresh-rate-displays"></a>Variable Aktualisierungsrate anzeigen

Weitere Informationen finden Sie unter [Variable Aktualisierungsrate anzeigen](variable-refresh-rate-displays.md).

## <a name="duplicating-output"></a>Duplizieren der Ausgabe

Eine einzelne Schnittstelle, [**IDXGIOutput5**](/windows/win32/api/DXGI1_5/nn-dxgi1_5-idxgioutput5), mit einer einzigen Methode [**DuplicateOutput1**](/windows/win32/api/DXGI1_5/nf-dxgi1_5-idxgioutput5-duplicateoutput1), wurde DXGI 1,5 hinzugefügt, um eine flexiblere und höhere Leistungs Version der ursprünglichen [**duplicateoutput**](/windows/win32/api/DXGI1_2/nf-dxgi1_2-idxgioutput1-duplicateoutput) -Methode bereitzustellen. **DuplicateOutput1** ermöglicht das Angeben einer Liste unterstützter Formate für Vollbildschirm Oberflächen, die vom [**idxgioutputduplikatobjekt**](/windows/win32/api/DXGI1_2/nn-dxgi1_2-idxgioutputduplication) zurückgegeben werden können, und ermöglicht das Erfassen von HDR-und WCG-Inhalten.

## <a name="offering-and-reclaiming-resources"></a>Anbieten und Freigeben von Ressourcen

Die aktualisierten Methoden [**OfferResources1**](/windows/win32/api/dxgi1_5/nf-dxgi1_5-idxgidevice4-offerresources1) und [**ReclaimResources1**](/windows/win32/api/dxgi1_5/nf-dxgi1_5-idxgidevice4-reclaimresources1) wurden einer neuen Schnittstelle hinzugefügt, [**IDXGIDevice4**](/windows/win32/api/dxgi1_5/nn-dxgi1_5-idxgidevice4), um das Decommit des Arbeitsspeichers zusätzlich zum Verwerfen von Ressourcen zu ermöglichen. Wenn Sie ein neues [**DXGI- \_ \_ \_ ressourcenflag \_ " \_ Decommit zulassen**](/windows/win32/api/dxgi1_5/ne-dxgi1_5-dxgi_offer_resource_flags) " abonnieren, bedeutet dies, dass die neuen Freigabe Ergebnisse ordnungsgemäß behandelt werden müssen.

## <a name="related-topics"></a>Zugehörige Themen

[Programmier Handbuch für DXGI](dx-graphics-dxgi-overviews.md)
