---
description: Einführung (WIC-Richtlinien für Kamera Rohbild Formate)
ms.assetid: 3c588386-1d4d-4ee0-b633-bfc94ca751ea
title: Einführung (WIC-Richtlinien für Kamera Rohbild Formate)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec6ee2607326afe289e0a3e54b254dcf581cbf86
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217372"
---
# <a name="introduction-wic-guidelines-for-camera-raw-image-formats"></a><span data-ttu-id="b0d8f-103">Einführung (WIC-Richtlinien für Kamera Rohbild Formate)</span><span class="sxs-lookup"><span data-stu-id="b0d8f-103">Introduction (WIC Guidelines for Camera RAW Image Formats)</span></span>

<span data-ttu-id="b0d8f-104">Die Windows Imaging Component (WIC) stellt ein erweiterbares Framework zum Arbeiten mit Bildern und Bild Metadaten bereit.</span><span class="sxs-lookup"><span data-stu-id="b0d8f-104">The Windows Imaging Component (WIC) provides an extensible framework for working with images and image metadata.</span></span> <span data-ttu-id="b0d8f-105">Mit WIC können Software-und Hardwarehersteller Codecs entwickeln, sodass Ihre eigenen Bildformate die gleiche Platt Form Unterstützung wie Native Image Formate wie z. b. TIFF (Tagged Image File Format), Joint Photographic Experts Group (JPEG) oder HD-Foto erhalten.</span><span class="sxs-lookup"><span data-stu-id="b0d8f-105">WIC makes it possible for software and hardware vendors to develop codecs so that their own image formats can obtain the same platform support as native image formats such as tagged image file format (TIFF), Joint Photographic Experts Group (JPEG), or HD Photo.</span></span>

<span data-ttu-id="b0d8f-106">WIC stellt unabhängig vom Bildformat einen einzelnen, konsistenten Satz von Schnittstellen für die gesamte Bildverarbeitung bereit.</span><span class="sxs-lookup"><span data-stu-id="b0d8f-106">WIC provides a single, consistent set of interfaces for all image processing, regardless of image format.</span></span> <span data-ttu-id="b0d8f-107">Daher erhält jede Anwendung, die WIC verwendet, automatische Unterstützung für neue Bildformate, sobald der Codec installiert ist.</span><span class="sxs-lookup"><span data-stu-id="b0d8f-107">Therefore, any application that uses WIC receives automatic support for new image formats as soon as the codec is installed.</span></span> <span data-ttu-id="b0d8f-108">WIC bietet auch ein erweiterbares metadatenframework, das es Anwendungen ermöglicht, eigene proprietäre Metadaten direkt in Bilddateien zu lesen und zu schreiben, sodass die Metadaten niemals verloren gehen oder von dem Image getrennt werden.</span><span class="sxs-lookup"><span data-stu-id="b0d8f-108">WIC also provides an extensible metadata framework that makes it possible for applications to read and write their own proprietary metadata directly to image files, so the metadata is never lost or separated from the image.</span></span>

<span data-ttu-id="b0d8f-109">WIC ist in Windows Presentation Foundation (WPF) enthalten und ist in Windows Vista und spätere Windows-Versionen integriert.</span><span class="sxs-lookup"><span data-stu-id="b0d8f-109">WIC is included with Windows Presentation Foundation (WPF) and is built into Windows Vista and later Windows versions.</span></span> <span data-ttu-id="b0d8f-110">Es ist auch als eigenständige verteilbare Komponente für Windows XP verfügbar.</span><span class="sxs-lookup"><span data-stu-id="b0d8f-110">It is also available as a stand-alone redistributable component for Windows XP.</span></span>

<span data-ttu-id="b0d8f-111">Diese Richtlinien sind so konzipiert, dass Sie Rohformat Herstellern bei der Entwicklung von WIC-Codecs unterstützen.</span><span class="sxs-lookup"><span data-stu-id="b0d8f-111">These guidelines are designed to help RAW format manufacturers in their development of WIC codecs.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b0d8f-112">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="b0d8f-112">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="b0d8f-113">**Licher**</span><span class="sxs-lookup"><span data-stu-id="b0d8f-113">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="b0d8f-114">Übersicht über die Windows Imaging-Komponente</span><span class="sxs-lookup"><span data-stu-id="b0d8f-114">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[<span data-ttu-id="b0d8f-115">WIC-Richtlinien für Kamera Rohbild Formate</span><span class="sxs-lookup"><span data-stu-id="b0d8f-115">WIC Guidelines for Camera RAW Image Formats</span></span>](-wic-rawguidelines.md)
</dt> <dt>

[<span data-ttu-id="b0d8f-116">Schreiben eines WIC-Enabled Codecs</span><span class="sxs-lookup"><span data-stu-id="b0d8f-116">How to Write a WIC-Enabled CODEC</span></span>](-wic-howtowriteacodec.md)
</dt> </dl>

 

 



