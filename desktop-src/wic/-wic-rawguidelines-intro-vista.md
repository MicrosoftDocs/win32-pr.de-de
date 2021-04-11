---
description: Rohbild Formate in Windows Vista
ms.assetid: e28b642c-03c8-4ecc-b5f5-e3911b8003a7
title: Rohbild Formate in Windows Vista
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c48b4e3ab5b0d373dbc0313267e58177b189538
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217373"
---
# <a name="raw-image-formats-in-windows-vista"></a><span data-ttu-id="90a83-103">Rohbild Formate in Windows Vista</span><span class="sxs-lookup"><span data-stu-id="90a83-103">RAW Image Formats in Windows Vista</span></span>

<span data-ttu-id="90a83-104">Windows Vista Explorer, Windows Vista Photo Gallery, Window Live Photo Gallery und Windows 7 Photo Viewer verwenden Windows Imaging Component (WIC) und unterstützen daher Rohbild Formate, wenn geeignete Codecs auf dem Computer installiert sind.</span><span class="sxs-lookup"><span data-stu-id="90a83-104">Windows Vista Explorer , Windows Vista Photo Gallery, Window Live Photo Gallery, and the Windows 7 Photo Viewer all use Windows Imaging Component (WIC) and therefore support RAW image formats when appropriate codecs are installed on the computer.</span></span>

<span data-ttu-id="90a83-105">Da WIC eine erweiterbare Imaging-Architektur ist, kann jede WIC-Anwendung neue Bildformate nutzen, sobald neue Codecs auf dem System installiert sind.</span><span class="sxs-lookup"><span data-stu-id="90a83-105">Because WIC is an extensible imaging architecture, any WIC application can consume new image formats as soon as new codecs are installed on the system.</span></span> <span data-ttu-id="90a83-106">Dadurch ist WIC ideal als Plug & Play Lösung für die Rohbild Formate, die Digitalkameras erzeugt.</span><span class="sxs-lookup"><span data-stu-id="90a83-106">This makes WIC ideal as a Plug and Play solution for the RAW image formats that digital cameras produce.</span></span> <span data-ttu-id="90a83-107">Mithilfe von WIC können Windows-Anwendungen immer Unterstützung für neue Kameramodelle erhalten, wenn aktualisierte Codecs verfügbar gemacht werden (im Idealfall mit neuen Kameras).</span><span class="sxs-lookup"><span data-stu-id="90a83-107">Through WIC, Windows applications can gain support for new camera models whenever updated codecs are made available (ideally in-box with new cameras).</span></span> <span data-ttu-id="90a83-108">Die Codec-Autoren können diese Szenarios unterstützen, indem Sie WIC-Schnittstellen implementieren, die allen Image Typen gemeinsam sind, wie in diesem Dokument ausführlicher beschrieben.</span><span class="sxs-lookup"><span data-stu-id="90a83-108">Codec authors can support these scenarios by implementing WIC interfaces that are common to all image types, as described in more detail in this document.</span></span>

<span data-ttu-id="90a83-109">Heutzutage haben die meisten gängigen Consumeranwendungen keine besonderen Kenntnisse von Rohbild Formaten und machen keine Benutzeroberfläche für die Anpassung der rohverarbeitungs Einstellungen verfügbar.</span><span class="sxs-lookup"><span data-stu-id="90a83-109">Today, most mainstream consumer applications have no special knowledge of RAW image formats and do not expose a user interface for adjusting RAW processing settings.</span></span>

<span data-ttu-id="90a83-110">Zur Unterstützung spezieller Abbild Erstellungs Anwendungen müssen auch unformatierte Codec-Autoren die [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) -Schnittstelle implementieren.</span><span class="sxs-lookup"><span data-stu-id="90a83-110">However, to support specialized imaging applications, RAW codec authors must also implement the [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) interface.</span></span> <span data-ttu-id="90a83-111">Diese Schnittstelle stellt besondere Features für unformatierte Images zur Verfügung, z. b. die Möglichkeit, gängige Bild Anpassungen vorzunehmen und unformatierte Bilder in angegebene Farben in rot-grün-blau (RGB) zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="90a83-111">This interface exposes special features for RAW images, such as the ability to make common image adjustments and to process (develop) RAW images into specified red-green-blue (RGB) color spaces.</span></span>

<span data-ttu-id="90a83-112">Einige andere WIC-Schnittstellen sind wichtig für unformatierte Codec-Autoren zur Implementierung von.</span><span class="sxs-lookup"><span data-stu-id="90a83-112">Several other WIC interfaces are important for RAW codec authors to implement.</span></span> <span data-ttu-id="90a83-113">Diese werden in dieser Reihe von Themen ausführlicher erläutert.</span><span class="sxs-lookup"><span data-stu-id="90a83-113">These are discussed in more detail in this series of topics.</span></span>

## <a name="related-topics"></a><span data-ttu-id="90a83-114">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="90a83-114">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="90a83-115">**Licher**</span><span class="sxs-lookup"><span data-stu-id="90a83-115">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="90a83-116">Übersicht über die Windows Imaging-Komponente</span><span class="sxs-lookup"><span data-stu-id="90a83-116">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[<span data-ttu-id="90a83-117">WIC-Richtlinien für Kamera Rohbild Formate</span><span class="sxs-lookup"><span data-stu-id="90a83-117">WIC Guidelines for Camera RAW Image Formats</span></span>](-wic-rawguidelines.md)
</dt> <dt>

[<span data-ttu-id="90a83-118">Schreiben eines WIC-Enabled Codecs</span><span class="sxs-lookup"><span data-stu-id="90a83-118">How to Write a WIC-Enabled CODEC</span></span>](-wic-howtowriteacodec.md)
</dt> </dl>

 

 



