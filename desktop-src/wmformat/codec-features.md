---
title: Codec-Features
description: Codec-Features
ms.assetid: e0bbdf75-2369-4080-ae8e-aabaa8401dcf
keywords:
- Windows Media-Format-SDK, Codec-Features
- Windows Media-Format-SDK, Features
- Codecs, Features
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02e3623bcb6f338fe11bef3089705801dc3ea047
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104206751"
---
# <a name="codec-features"></a><span data-ttu-id="cdeda-106">Codec-Features</span><span class="sxs-lookup"><span data-stu-id="cdeda-106">Codec Features</span></span>

<span data-ttu-id="cdeda-107">Das Windows Media-Format-SDK wird mit verschiedenen Audio-und Video Codecs geliefert.</span><span class="sxs-lookup"><span data-stu-id="cdeda-107">The Windows Media Format SDK is delivered with several audio and video codecs.</span></span> <span data-ttu-id="cdeda-108">Sie können die bereitgestellten Codecs zum Komprimieren und decoden von Inhalten verwenden, um eine Vielzahl von Anforderungen zu erfüllen.</span><span class="sxs-lookup"><span data-stu-id="cdeda-108">You can use the codecs provided to compress and decompress content to suit a variety of needs.</span></span> <span data-ttu-id="cdeda-109">Der Codec, der vom Writer zum Komprimieren von Daten verwendet wird, wird durch Datenstrom-Konfigurationsinformationen im Profil angegeben.</span><span class="sxs-lookup"><span data-stu-id="cdeda-109">The codec that is used by the writer to compress data is specified by stream configuration information in the profile.</span></span> <span data-ttu-id="cdeda-110">Informationen aus dem Profil werden dann in der Kopfzeile der vom Writer erstellten Datei gespeichert.</span><span class="sxs-lookup"><span data-stu-id="cdeda-110">Information from the profile is then stored in the header of the file created by the writer.</span></span> <span data-ttu-id="cdeda-111">Wenn die Datei dann vom Reader oder dem synchronen Reader geöffnet wird, identifiziert die Profilinformationen im Header den Codec, der zum Dekomprimieren der Daten erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="cdeda-111">Then, when the file is opened by the reader or synchronous reader, the profile information in the header identifies the codec needed to decompress the data.</span></span>

<span data-ttu-id="cdeda-112">Die folgenden Funktionen werden in diesem Abschnitt erläutert.</span><span class="sxs-lookup"><span data-stu-id="cdeda-112">The following features are discussed in this section.</span></span>

-   [<span data-ttu-id="cdeda-113">Unterstützte Codecs</span><span class="sxs-lookup"><span data-stu-id="cdeda-113">Supported Codecs</span></span>](supported-codecs.md)
-   [<span data-ttu-id="cdeda-114">Codierung mit konstanter Bitrate (CBR)</span><span class="sxs-lookup"><span data-stu-id="cdeda-114">Constant Bit Rate (CBR) Encoding</span></span>](constant-bit-rate--cbr--encoding.md)
-   [<span data-ttu-id="cdeda-115">Codierung der Variablen Bitrate (VBR)</span><span class="sxs-lookup"><span data-stu-id="cdeda-115">Variable Bit Rate (VBR) Encoding</span></span>](variable-bit-rate--vbr--encoding.md)
-   [<span data-ttu-id="cdeda-116">Zwei-Pass-Codierung</span><span class="sxs-lookup"><span data-stu-id="cdeda-116">Two-Pass Encoding</span></span>](two-pass-encoding.md)
-   [<span data-ttu-id="cdeda-117">Hochauflösende Audiounterstützung</span><span class="sxs-lookup"><span data-stu-id="cdeda-117">High-Resolution Audio Support</span></span>](high-resolution-audio-support.md)
-   [<span data-ttu-id="cdeda-118">Low-Delay-Audiodaten</span><span class="sxs-lookup"><span data-stu-id="cdeda-118">Low-Delay Audio</span></span>](low-delay-audio.md)
-   [<span data-ttu-id="cdeda-119">S/PDIF-Audioausgabe</span><span class="sxs-lookup"><span data-stu-id="cdeda-119">S/PDIF Audio Output</span></span>](s-pdif-audio-output.md)
-   [<span data-ttu-id="cdeda-120">Videobild</span><span class="sxs-lookup"><span data-stu-id="cdeda-120">Video Image</span></span>](video-image.md)
-   [<span data-ttu-id="cdeda-121">Geräte Konformitäts Vorlagen</span><span class="sxs-lookup"><span data-stu-id="cdeda-121">Device Conformance Templates</span></span>](device-conformance-templates.md)
-   [<span data-ttu-id="cdeda-122">Video Komplexitäts Einstellungen</span><span class="sxs-lookup"><span data-stu-id="cdeda-122">Video Complexity Settings</span></span>](video-complexity-settings.md)
-   [<span data-ttu-id="cdeda-123">Frame Interpolation</span><span class="sxs-lookup"><span data-stu-id="cdeda-123">Frame Interpolation</span></span>](frame-interpolation.md)

## <a name="related-topics"></a><span data-ttu-id="cdeda-124">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="cdeda-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cdeda-125">**Features**</span><span class="sxs-lookup"><span data-stu-id="cdeda-125">**Features**</span></span>](features.md)
</dt> </dl>

 

 




