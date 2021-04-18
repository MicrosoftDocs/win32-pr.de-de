---
description: Wenn Sie Ihren Codec auf der WIC-Plattform (Windows Imaging Component, Windows Imaging Component) erstellen, können alle auf WIC basierenden Anwendungen die gleiche Platt Form Unterstützung für Ihr Bildformat erhalten, das Sie für die allgemeinen Bildformate der Plattform erhalten.
ms.assetid: 4f25f0f4-246c-4cbd-bd11-d061dbc7de45
title: Schlussfolgerung (Schreiben eines WIC-Enabled Codecs)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de165f20ff81094c3b64d7e9667795f0bf80cef8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106358501"
---
# <a name="conclusion-how-to-write-a-wic-enabled-codec"></a><span data-ttu-id="62fc7-103">Schlussfolgerung (Schreiben eines WIC-Enabled Codecs)</span><span class="sxs-lookup"><span data-stu-id="62fc7-103">Conclusion (How to Write a WIC-Enabled Codec)</span></span>

<span data-ttu-id="62fc7-104">Wenn Sie Ihren Codec auf der WIC-Plattform (Windows Imaging Component, Windows Imaging Component) erstellen, können alle auf WIC basierenden Anwendungen die gleiche Platt Form Unterstützung für Ihr Bildformat erhalten, das Sie für die allgemeinen Bildformate der Plattform erhalten.</span><span class="sxs-lookup"><span data-stu-id="62fc7-104">Building your codec on the Windows Imaging Component (WIC) platform makes it possible for all applications built on WIC to get the same platform support for your image format that they get for the common image formats shipped with the platform.</span></span> <span data-ttu-id="62fc7-105">Außerdem ermöglicht es der Windows Vista-Fotogalerie, Windows-Explorer und der Photo Viewer, mit dem von Ihnen bereitgestellten Decoder Miniaturansichten und Vorschau Bilder in Ihrem Format anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="62fc7-105">It also enables the Windows Vista Photo Gallery, Windows Explorer, and Photo Viewer to display thumbnails and previews of images in your format using the decoder that you provide.</span></span> <span data-ttu-id="62fc7-106">Bei Rohdaten Formaten können anspruchsvollere Abbild Erstellungs Anwendungen die rohverarbeitungs Funktionen Ihres Decoders nutzen.</span><span class="sxs-lookup"><span data-stu-id="62fc7-106">For raw formats, it enables more sophisticated imaging applications to take advantage of your decoder’s raw processing capabilities.</span></span> <span data-ttu-id="62fc7-107">Abhängig von den von Ihnen unterstützten Codierungsoptionen können Sie auch eindeutige Funktionen Ihres Encoders verfügbar machen, damit Anwendungen die erweiterten Features Ihres Bildformats voll ausschöpfen können.</span><span class="sxs-lookup"><span data-stu-id="62fc7-107">Depending on the encoder options you support, you can also expose unique capabilities of your encoder to enable applications to take full advantage of the advanced features of your image format.</span></span>

<span data-ttu-id="62fc7-108">Zum Entwickeln eines WIC-fähigen Codecs müssen Sie einige neue Schnittstellen implementieren.</span><span class="sxs-lookup"><span data-stu-id="62fc7-108">Developing a WIC-enabled codec requires you to implement some new interfaces.</span></span> <span data-ttu-id="62fc7-109">In vielen Fällen können Sie einen Wrapper für Ihren vorhandenen Codec schreiben, der diese Schnittstellen implementiert.</span><span class="sxs-lookup"><span data-stu-id="62fc7-109">In many cases, you can write a wrapper for your existing codec that implements these interfaces.</span></span> <span data-ttu-id="62fc7-110">Wenn Sie Ihren CODEC installieren, müssen Sie einige Registrierungseinträge vornehmen, damit der Codec von der WIC-Plattform erkennbar ist und den entsprechenden metadatenhandlern zugeordnet wird.</span><span class="sxs-lookup"><span data-stu-id="62fc7-110">When you install your codec, you must make some registry entries to make your codec discoverable by the WIC platform and associate it with the appropriate metadata handlers.</span></span> <span data-ttu-id="62fc7-111">Sie müssen auch eine API aufrufen, um den Miniatur Ansichts Cache aller standardmäßigen (leeren) Miniaturansichten zu löschen, die möglicherweise bereits mit Bildern in Ihrem Format verknüpft sind.</span><span class="sxs-lookup"><span data-stu-id="62fc7-111">You also need to invoke an API to clear the thumbnail cache of any default (empty) thumbnails that may have previously associated with images in your format.</span></span> <span data-ttu-id="62fc7-112">Wenn Sie möchten, können Sie die Windows Vista-Fotogalerie aktivieren, um Benutzern einen Link zum Herunterladen Ihres Codecs bereitzustellen, wenn in der Fotogalerie ein Bild mit der Dateinamenerweiterung gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="62fc7-112">If you want, you can enable the Windows Vista Photo Gallery to provide users with a link to download your codec when the Photo Gallery encounters an image with your file name extension.</span></span> <span data-ttu-id="62fc7-113">Zu diesem Zweck müssen Sie Microsoft Informationen über die Dateinamenerweiterung Ihres Codecs und die URL für die Download Website bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="62fc7-113">To do this, you must provide Microsoft with information about your codec’s file name extension and the URL for your download site.</span></span>

## <a name="related-topics"></a><span data-ttu-id="62fc7-114">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="62fc7-114">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="62fc7-115">**Licher**</span><span class="sxs-lookup"><span data-stu-id="62fc7-115">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="62fc7-116">Codec-Installation und-Registrierung</span><span class="sxs-lookup"><span data-stu-id="62fc7-116">CODEC Installation and Registration</span></span>](-wic-codecinstallandreg.md)
</dt> <dt>

[<span data-ttu-id="62fc7-117">Schreiben eines WIC-Enabled Codecs</span><span class="sxs-lookup"><span data-stu-id="62fc7-117">How to Write a WIC-Enabled CODEC</span></span>](-wic-howtowriteacodec.md)
</dt> <dt>

[<span data-ttu-id="62fc7-118">Übersicht über die Windows Imaging-Komponente</span><span class="sxs-lookup"><span data-stu-id="62fc7-118">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 



