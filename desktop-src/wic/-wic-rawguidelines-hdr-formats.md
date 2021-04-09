---
description: Hohe dynamische Bereichs Pixel Formate
ms.assetid: 037b6bde-a3e0-401d-9be7-b58c5f74c30a
title: Hohe dynamische Bereichs Pixel Formate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8405a01fa5397dd5681077ac1ac9acc28e7d1003
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867323"
---
# <a name="high-dynamic-range-pixel-formats"></a><span data-ttu-id="7432d-103">Hohe dynamische Bereichs Pixel Formate</span><span class="sxs-lookup"><span data-stu-id="7432d-103">High Dynamic Range Pixel Formats</span></span>

<span data-ttu-id="7432d-104">Codecs sollten Windows Imaging Component (WIC) Pixel Formate verwenden, die den gesamten dynamischen Bereich der zugrunde liegenden Sensordaten beibehalten.</span><span class="sxs-lookup"><span data-stu-id="7432d-104">Codecs should use Windows Imaging Component (WIC) pixel formats that preserve all of the dynamic range of the underlying sensor data.</span></span> <span data-ttu-id="7432d-105">GUID \_ WICPixelFormat48bppRGB ist ein typisches festgelegtes 16-Bit-pro-Channel-Format, das verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="7432d-105">GUID\_WICPixelFormat48bppRGB is a typical fixed-point 16-bit-per-channel format that can be used.</span></span> <span data-ttu-id="7432d-106">Andere Formate mit höherer Genauigkeit können ebenfalls verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7432d-106">Other higher precision formats can be used also.</span></span> <span data-ttu-id="7432d-107">Um die vollständige Unterstützung für das Windows Presentation Foundation Graphics Processing Unit (GPU)-beschleunigte Renderingpipeline zu aktivieren, ermutigt Microsoft dringend die Unterstützung für ein 32-Bit-Gleit Komma-Pixel Format.</span><span class="sxs-lookup"><span data-stu-id="7432d-107">To enable full support for the Windows Presentation Foundation graphics processing unit (GPU)-accelerated rendering pipeline, Microsoft strongly encourages support for a 32-bit floating point pixel format.</span></span>

<span data-ttu-id="7432d-108">High Color Pixel Formats: bei Windows 7 wurden zwei neue WIC-Pixel Formate hinzugefügt, um die neuen Hochleistungs-Anzeige Formate zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="7432d-108">High Color Pixel Formats: With Windows 7, two new WIC pixel formats have been added to support the new High Color display formats.</span></span> <span data-ttu-id="7432d-109">Dies sind die folgenden: GUID \_ WICPixelFormat32bppRGBA1010102 und GUID \_ WICPixelFormat32bppRGBA1010102XR.</span><span class="sxs-lookup"><span data-stu-id="7432d-109">These are: GUID\_WICPixelFormat32bppRGBA1010102 and GUID\_WICPixelFormat32bppRGBA1010102XR.</span></span>

<span data-ttu-id="7432d-110">Das "16 Bit pro Channel (BPC) float High Color Format" wird vom vorhandenen GUID \_ WICPixelFormat64bppRGBAHalf Pixel-Format unterstützt.</span><span class="sxs-lookup"><span data-stu-id="7432d-110">The 16 bit per channel (bpc) float High Color format is supported by the existing GUID\_WICPixelFormat64bppRGBAHalf pixel format.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7432d-111">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="7432d-111">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="7432d-112">**Licher**</span><span class="sxs-lookup"><span data-stu-id="7432d-112">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="7432d-113">Übersicht über die Windows Imaging-Komponente</span><span class="sxs-lookup"><span data-stu-id="7432d-113">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[<span data-ttu-id="7432d-114">WIC-Richtlinien für Kamera Rohbild Formate</span><span class="sxs-lookup"><span data-stu-id="7432d-114">WIC Guidelines for Camera RAW Image Formats</span></span>](-wic-rawguidelines.md)
</dt> <dt>

[<span data-ttu-id="7432d-115">Schreiben eines WIC-Enabled Codecs</span><span class="sxs-lookup"><span data-stu-id="7432d-115">How to Write a WIC-Enabled CODEC</span></span>](-wic-howtowriteacodec.md)
</dt> </dl>

 

 



