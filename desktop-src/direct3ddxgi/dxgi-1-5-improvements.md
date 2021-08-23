---
description: Die folgenden Funktionen wurden microsoft DirectX Graphic Infrastructure (DXGI) 1.5 hinzugefügt, um eine flexiblere Angabe und Duplizierung von Ausgabeformaten zu unterstützen.
ms.assetid: DD7401E1-9991-48D8-AD23-4D34238EA4AF
title: DXGI 1.5-Verbesserungen
ms.topic: article
ms.date: 03/05/2021
ms.openlocfilehash: 52661018941f84a14f45c112ba7ed68800d0cf0f2fb69f7a1d3333651fb17787
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118987130"
---
# <a name="dxgi-15-improvements"></a>DXGI 1.5-Verbesserungen

Die folgenden Funktionen wurden microsoft DirectX Graphic Infrastructure (DXGI) 1.5 hinzugefügt, um eine flexiblere Angabe und Duplizierung von Ausgabeformaten zu unterstützen.

## <a name="high-dynamic-range-and-wide-color-gamut"></a>High Dynamic Range und Breite Farbpalette

Weitere Informationen finden Sie unter [Using DirectX with high dynamic range displays and advanced color (Verwenden von DirectX mit Anzeige mit hohem dynamischen Bereich und erweiterter Farbe).](../direct3darticles/high-dynamic-range.md)

## <a name="variable-refresh-rate-displays"></a>Variable Aktualisierungsrate wird angezeigt

Weitere Informationen finden Sie unter [Variable Aktualisierungsrate zeigt an.](variable-refresh-rate-displays.md)

## <a name="duplicating-output"></a>Duplizieren der Ausgabe

Eine einzelne Schnittstelle, [**IDXGIOutput5,**](/windows/win32/api/DXGI1_5/nn-dxgi1_5-idxgioutput5)mit einer einzelnen Methode, [**DuplicateOutput1,**](/windows/win32/api/DXGI1_5/nf-dxgi1_5-idxgioutput5-duplicateoutput1)wurde dxgi 1.5 hinzugefügt, um eine flexiblere und höhere Leistungsversion der ursprünglichen [**DuplicateOutput-Methode**](/windows/win32/api/DXGI1_2/nf-dxgi1_2-idxgioutput1-duplicateoutput) bereitzustellen. **DuplicateOutput1** ermöglicht das Angeben einer Liste unterstützter Formate für Vollbildoberflächen, die vom [**IDXGIOutputDuplication-Objekt**](/windows/win32/api/DXGI1_2/nn-dxgi1_2-idxgioutputduplication) zurückgegeben werden können, und ermöglicht die Erfassung von HDR- und WCG-Inhalten.

## <a name="offering-and-reclaiming-resources"></a>Anbieten und Reclaiming von Ressourcen

Die [**aktualisierten Methoden OfferResources1**](/windows/win32/api/dxgi1_5/nf-dxgi1_5-idxgidevice4-offerresources1) und [**ReclaimResources1**](/windows/win32/api/dxgi1_5/nf-dxgi1_5-idxgidevice4-reclaimresources1) wurden der neuen Schnittstelle [**IDXGIDevice4**](/windows/win32/api/dxgi1_5/nn-dxgi1_5-idxgidevice4)hinzugefügt, um das Entfernen des Arbeitsspeichers sowie das Verwerfen von Ressourcen zu ermöglichen. Wenn Sie sich für das neue [**DXGI \_ OFFER RESOURCE FLAG ALLOW \_ \_ \_ \_ DECOMMIT-Flag**](/windows/win32/api/dxgi1_5/ne-dxgi1_5-dxgi_offer_resource_flags) entscheiden, müssen die neuen Ergebnisse der Wiederverwendung ordnungsgemäß verarbeitet werden.

## <a name="related-topics"></a>Zugehörige Themen

[Programmierhandbuch für DXGI](dx-graphics-dxgi-overviews.md)
