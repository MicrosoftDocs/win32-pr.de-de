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
# <a name="dxgi-15-improvements"></a><span data-ttu-id="32e87-103">DXGI 1,5-Verbesserungen</span><span class="sxs-lookup"><span data-stu-id="32e87-103">DXGI 1.5 Improvements</span></span>

<span data-ttu-id="32e87-104">Die folgenden Funktionen wurden der Microsoft DirectX Graphics Infrastructure (DXGI) 1,5 hinzugefügt, um eine flexiblere Angabe und Duplizierung von Ausgabeformaten zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="32e87-104">The following functionality has been added to Microsoft DirectX Graphics Infrastructure (DXGI) 1.5, to support more flexible specifying and duplication of output formats.</span></span>

## <a name="high-dynamic-range-and-wide-color-gamut"></a><span data-ttu-id="32e87-105">Hoher dynamischer Bereich und breite Farbpalette</span><span class="sxs-lookup"><span data-stu-id="32e87-105">High Dynamic Range and Wide Color Gamut</span></span>

<span data-ttu-id="32e87-106">Weitere Informationen finden Sie unter [Verwenden von DirectX mit dynamischen Bereichs anzeigen und](../direct3darticles/high-dynamic-range.md)erweiterter Farbe.</span><span class="sxs-lookup"><span data-stu-id="32e87-106">Refer to [Using DirectX with high dynamic range displays and advanced color](../direct3darticles/high-dynamic-range.md).</span></span>

## <a name="variable-refresh-rate-displays"></a><span data-ttu-id="32e87-107">Variable Aktualisierungsrate anzeigen</span><span class="sxs-lookup"><span data-stu-id="32e87-107">Variable refresh rate displays</span></span>

<span data-ttu-id="32e87-108">Weitere Informationen finden Sie unter [Variable Aktualisierungsrate anzeigen](variable-refresh-rate-displays.md).</span><span class="sxs-lookup"><span data-stu-id="32e87-108">Refer to [Variable refresh rate displays](variable-refresh-rate-displays.md).</span></span>

## <a name="duplicating-output"></a><span data-ttu-id="32e87-109">Duplizieren der Ausgabe</span><span class="sxs-lookup"><span data-stu-id="32e87-109">Duplicating output</span></span>

<span data-ttu-id="32e87-110">Eine einzelne Schnittstelle, [**IDXGIOutput5**](/windows/win32/api/DXGI1_5/nn-dxgi1_5-idxgioutput5), mit einer einzigen Methode [**DuplicateOutput1**](/windows/win32/api/DXGI1_5/nf-dxgi1_5-idxgioutput5-duplicateoutput1), wurde DXGI 1,5 hinzugefügt, um eine flexiblere und höhere Leistungs Version der ursprünglichen [**duplicateoutput**](/windows/win32/api/DXGI1_2/nf-dxgi1_2-idxgioutput1-duplicateoutput) -Methode bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="32e87-110">A single interface, [**IDXGIOutput5**](/windows/win32/api/DXGI1_5/nn-dxgi1_5-idxgioutput5), with a single method, [**DuplicateOutput1**](/windows/win32/api/DXGI1_5/nf-dxgi1_5-idxgioutput5-duplicateoutput1), has been added to DXGI 1.5 to provide a more flexible and higher performance version of the original [**DuplicateOutput**](/windows/win32/api/DXGI1_2/nf-dxgi1_2-idxgioutput1-duplicateoutput) method.</span></span> <span data-ttu-id="32e87-111">**DuplicateOutput1** ermöglicht das Angeben einer Liste unterstützter Formate für Vollbildschirm Oberflächen, die vom [**idxgioutputduplikatobjekt**](/windows/win32/api/DXGI1_2/nn-dxgi1_2-idxgioutputduplication) zurückgegeben werden können, und ermöglicht das Erfassen von HDR-und WCG-Inhalten.</span><span class="sxs-lookup"><span data-stu-id="32e87-111">**DuplicateOutput1** allows specifying a list of supported formats for fullscreen surfaces that can be returned by the [**IDXGIOutputDuplication**](/windows/win32/api/DXGI1_2/nn-dxgi1_2-idxgioutputduplication) object, and enables capturing HDR and WCG content.</span></span>

## <a name="offering-and-reclaiming-resources"></a><span data-ttu-id="32e87-112">Anbieten und Freigeben von Ressourcen</span><span class="sxs-lookup"><span data-stu-id="32e87-112">Offering and Reclaiming Resources</span></span>

<span data-ttu-id="32e87-113">Die aktualisierten Methoden [**OfferResources1**](/windows/win32/api/dxgi1_5/nf-dxgi1_5-idxgidevice4-offerresources1) und [**ReclaimResources1**](/windows/win32/api/dxgi1_5/nf-dxgi1_5-idxgidevice4-reclaimresources1) wurden einer neuen Schnittstelle hinzugefügt, [**IDXGIDevice4**](/windows/win32/api/dxgi1_5/nn-dxgi1_5-idxgidevice4), um das Decommit des Arbeitsspeichers zusätzlich zum Verwerfen von Ressourcen zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="32e87-113">Updated methods [**OfferResources1**](/windows/win32/api/dxgi1_5/nf-dxgi1_5-idxgidevice4-offerresources1) and [**ReclaimResources1**](/windows/win32/api/dxgi1_5/nf-dxgi1_5-idxgidevice4-reclaimresources1) have been added to a new interface, [**IDXGIDevice4**](/windows/win32/api/dxgi1_5/nn-dxgi1_5-idxgidevice4), to allow de-committing of memory in addition to discarding resources.</span></span> <span data-ttu-id="32e87-114">Wenn Sie ein neues [**DXGI- \_ \_ \_ ressourcenflag \_ " \_ Decommit zulassen**](/windows/win32/api/dxgi1_5/ne-dxgi1_5-dxgi_offer_resource_flags) " abonnieren, bedeutet dies, dass die neuen Freigabe Ergebnisse ordnungsgemäß behandelt werden müssen.</span><span class="sxs-lookup"><span data-stu-id="32e87-114">Opting in to the new [**DXGI\_OFFER\_RESOURCE\_FLAG\_ALLOW\_DECOMMIT**](/windows/win32/api/dxgi1_5/ne-dxgi1_5-dxgi_offer_resource_flags) flag means the new reclaim results must be properly handled.</span></span>

## <a name="related-topics"></a><span data-ttu-id="32e87-115">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="32e87-115">Related topics</span></span>

[<span data-ttu-id="32e87-116">Programmier Handbuch für DXGI</span><span class="sxs-lookup"><span data-stu-id="32e87-116">Programming Guide for DXGI</span></span>](dx-graphics-dxgi-overviews.md)
