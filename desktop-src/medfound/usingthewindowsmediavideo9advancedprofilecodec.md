---
description: Verwenden des erweiterten Profils Windows Media Video 9
ms.assetid: 2abc0efc-dd11-4921-897c-209a26f8ba1d
title: Verwenden des erweiterten Profils Windows Media Video 9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 692243117cde3b4b5f1179c5f7324d25842191b6
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "106366545"
---
# <a name="using-the-windows-media-video-9-advanced-profile"></a><span data-ttu-id="72b9e-103">Verwenden des erweiterten Profils Windows Media Video 9</span><span class="sxs-lookup"><span data-stu-id="72b9e-103">Using the Windows Media Video 9 Advanced Profile</span></span>

<span data-ttu-id="72b9e-104">Die grundlegenden Video Prozeduren, die im Abschnitt [Arbeiten mit Videos](workingwithvideo.md) beschrieben werden, gelten auch direkt für das erweiterte Profil Windows Media Video 9.</span><span class="sxs-lookup"><span data-stu-id="72b9e-104">The basic video procedures described in the [Working with Video](workingwithvideo.md) section also apply directly to the Windows Media Video 9 Advanced Profile.</span></span> <span data-ttu-id="72b9e-105">Es sind keine speziellen Prozeduren erforderlich.</span><span class="sxs-lookup"><span data-stu-id="72b9e-105">No special procedures are required.</span></span>

<span data-ttu-id="72b9e-106">Das erweiterte Profil Windows Media Video 9 ist mit den Klassen Bezeichner CLSID \_ CWMV9EncMediaObject und CLSID \_ cwmvdecmediaobject verknüpft.</span><span class="sxs-lookup"><span data-stu-id="72b9e-106">The Windows Media Video 9 Advanced Profile is associated with the class identifiers CLSID\_CWMV9EncMediaObject and CLSID\_CWMVDecMediaObject.</span></span> <span data-ttu-id="72b9e-107">Der FourCC-Wert für Medientypen, die diesen Codec verwenden, ist "WVC1".</span><span class="sxs-lookup"><span data-stu-id="72b9e-107">The FOURCC value for media types using this codec is "WVC1".</span></span>

<span data-ttu-id="72b9e-108">Das erweiterte Profil Windows Media Video 9 unterstützt alle gängigen Codierungs Modi sowie die Zeilen Sprung Codierung, gemischte und Progressive Codierung, Auflösungen, die sich von der Anzeige unterscheiden, sowie Bereichs Reduzierungs Features.</span><span class="sxs-lookup"><span data-stu-id="72b9e-108">The Windows Media Video 9 Advanced Profile supports all common encoding modes as well interlaced encoding, mixed interlaced and progressive encoding, resolutions that are different than the display, and range reduction features.</span></span> <span data-ttu-id="72b9e-109">Ein weiteres Feature ist die Möglichkeit, Sequenz-und Frame Metadaten im Bitstream selbst zu speichern. zuvor war hierfür die Verwendung der ASF-und der Dateneinheiten Erweiterungen-API erforderlich.</span><span class="sxs-lookup"><span data-stu-id="72b9e-109">Another feature is the ability to store sequence and frame metadata in the bit-stream itself; previously this had required use of the ASF and Data Unit Extensions API.</span></span>

<span data-ttu-id="72b9e-110">Die folgenden Eigenschaften des erweiterten Profils Windows Media Video 9, die mithilfe von Registrierungs Einstellungen gesteuert werden können, verfügen nicht über die entsprechenden **IPropertyBag** -oder **IPropertyStore** -Zeichen folgen:</span><span class="sxs-lookup"><span data-stu-id="72b9e-110">The following properties of the Windows Media Video 9 Advanced Profile, which can be controlled using registry settings, do not have corresponding **IPropertyBag** or **IPropertyStore** strings:</span></span>

-   <span data-ttu-id="72b9e-111">DQuant-Option.</span><span class="sxs-lookup"><span data-stu-id="72b9e-111">Dquant Option.</span></span>
-   <span data-ttu-id="72b9e-112">Die DQuant-Stärke.</span><span class="sxs-lookup"><span data-stu-id="72b9e-112">Dquant Strength.</span></span>
-   <span data-ttu-id="72b9e-113">Überlappende erzwingen.</span><span class="sxs-lookup"><span data-stu-id="72b9e-113">Force Overlap.</span></span>
-   <span data-ttu-id="72b9e-114">Bewegungsvektor kostenmethode.</span><span class="sxs-lookup"><span data-stu-id="72b9e-114">Motion Vector Cost Method.</span></span>

## <a name="achieving-optimal-visual-quality"></a><span data-ttu-id="72b9e-115">Erzielen optimaler visueller Qualität</span><span class="sxs-lookup"><span data-stu-id="72b9e-115">Achieving Optimal Visual Quality</span></span>

<span data-ttu-id="72b9e-116">Für die meisten Videodaten können Sie die Eigenschaft " [ \_ compressionoptimizationtype" von "mfpkey](mfpkey-compressionoptimizationtypeproperty.md) " auf "1" festlegen, um eine optimale visuelle Windows Media Video Qualität zu erzielen.</span><span class="sxs-lookup"><span data-stu-id="72b9e-116">For most video data, to achieve optimal visual quality using the Windows Media Video 9 Advanced Profile, you can set the [MFPKEY\_COMPRESSIONOPTIMIZATIONTYPE](mfpkey-compressionoptimizationtypeproperty.md) property to 1.</span></span>

## <a name="about-the-previous-windows-media-video-9-advanced-profile-codecs"></a><span data-ttu-id="72b9e-117">Informationen zu den vorherigen Windows Media Video 9 Advanced Profile Codecs</span><span class="sxs-lookup"><span data-stu-id="72b9e-117">About the Previous Windows Media Video 9 Advanced Profile Codecs</span></span>

<span data-ttu-id="72b9e-118">Die aktuelle Version von Windows Media Video 9 Advanced Profile Codec basiert auf dem erweiterten Profil "Society of Motion Picture and TV Engineers (SMPTE) Standard for VC-1 (SMPTE 421m)".</span><span class="sxs-lookup"><span data-stu-id="72b9e-118">The current version of the Windows Media Video 9 Advanced Profile codec is based on the Society of Motion Picture and Television Engineers (SMPTE) standard for VC-1 (SMPTE 421M) Advanced Profile.</span></span> <span data-ttu-id="72b9e-119">Dieser Codec ersetzt den früheren Codec von Windows, der auch als "Windows Media Video 9 Advanced Profile Codec" bezeichnet wird, der durch den FourCC-Code "wmva" identifiziert wurde.</span><span class="sxs-lookup"><span data-stu-id="72b9e-119">This codec replaces the earlier codec from Windows also called the Windows Media Video 9 Advanced Profile codec which was identified by the FOURCC code "WMVA".</span></span> <span data-ttu-id="72b9e-120">Die vorherige Version des VC-1-Codecs wurde implementiert, bevor der erweiterte VC-1-Profil-Standard fertiggestellt wurde, und wird nicht mehr unterstützt.</span><span class="sxs-lookup"><span data-stu-id="72b9e-120">The previous version of the VC-1 codec was implemented before the VC-1 advanced profile standard was finalized, and is no longer supported.</span></span>

## <a name="related-topics"></a><span data-ttu-id="72b9e-121">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="72b9e-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="72b9e-122">Arbeiten mit Videos</span><span class="sxs-lookup"><span data-stu-id="72b9e-122">Working with Video</span></span>](workingwithvideo.md)
</dt> 
<dt>

[<span data-ttu-id="72b9e-123">Verwenden der erweiterten Einstellungen von Windows Media Video 9 Advanced Profile Codec</span><span class="sxs-lookup"><span data-stu-id="72b9e-123">Using the Advanced Settings of the Windows Media Video 9 Advanced Profile Codec</span></span>](https://www.microsoft.com/windows/windowsmedia/howto/articles/codecadvancedsettings.aspx)
</dt> </dl>

 

 



