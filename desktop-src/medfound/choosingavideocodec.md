---
description: Auswählen eines Videocodecs
ms.assetid: 3a4b925a-4fb4-4189-a571-8083454fed0e
title: Auswählen eines Videocodecs (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9186c7e7e60f5822ec2e50e3e5c7e16e96b91839
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214339"
---
# <a name="choosing-a-video-codec-microsoft-media-foundation"></a><span data-ttu-id="02901-103">Auswählen eines Videocodecs (Microsoft Media Foundation)</span><span class="sxs-lookup"><span data-stu-id="02901-103">Choosing a Video Codec (Microsoft Media Foundation)</span></span>

<span data-ttu-id="02901-104">Der Windows Media Video 9-Encoder unterstützt drei Kategorien codierter Ausgabe: Hauptprofil, erweitertes Profil und Image.</span><span class="sxs-lookup"><span data-stu-id="02901-104">The Windows Media Video 9 Encoder supports three categories of encoded output: Main Profile, Advanced Profile, and Image.</span></span> <span data-ttu-id="02901-105">Die Hauptprofil Kategorie bietet allgemeine Video Komprimierung für komplexe Videoinhalte, z. b. Filme oder Musikvideos.</span><span class="sxs-lookup"><span data-stu-id="02901-105">The Main Profile category provides general video compression for complex video content, such as movies or music videos.</span></span> <span data-ttu-id="02901-106">Die Features des Haupt Profils bieten eine große Bandbreite an Codierungs Einstellungen.</span><span class="sxs-lookup"><span data-stu-id="02901-106">The features of the Main Profile provide for a wide range of encoding settings.</span></span> <span data-ttu-id="02901-107">Sie können das Hauptprofil verwenden, um Videos mit sehr niedrigen Bitraten für die Übermittlung auf handgehaltenen Geräten zu erstellen, oder am anderen Ende des Spektrums können Sie es verwenden, um Videos mit hoher Definition für digitales Kino zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="02901-107">You can use the Main Profile to create video with very low bit rates for delivery on handheld devices or, at the other end of the spectrum, you can use it to create high-definition video for digital cinema.</span></span>

<span data-ttu-id="02901-108">Der Schwerpunkt der Codierungs Algorithmen im Hauptprofil liegt auf dynamischen Videoinhalten, Sie sind jedoch auch für andere Videoinhalte geeignet.</span><span class="sxs-lookup"><span data-stu-id="02901-108">The emphasis of the encoding algorithms in the Main Profile is on dynamic video content, but they are suitable for other video content as well.</span></span> <span data-ttu-id="02901-109">Das Hauptprofil sollte die Standard Kategorie für Videoinhalte sein.</span><span class="sxs-lookup"><span data-stu-id="02901-109">The Main Profile should be your default category for video content.</span></span> <span data-ttu-id="02901-110">Um bestimmte Anforderungen zu erfüllen, können Sie die Kategorie "Erweiterter Profil", die Kategorie "Image" oder einen separaten Encoder namens "Windows Media Video 9 Screen Encoder" verwenden.</span><span class="sxs-lookup"><span data-stu-id="02901-110">To meet specific needs, you can use the Advanced Profile category, the Image category, or a separate encoder called the Windows Media Video 9 Screen encoder.</span></span> <span data-ttu-id="02901-111">In der folgenden Tabelle sind die vier Optionen aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="02901-111">The following table lists the four options.</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="02901-112">Zweck</span><span class="sxs-lookup"><span data-stu-id="02901-112">Purpose</span></span></th>
<th><span data-ttu-id="02901-113">Codec</span><span class="sxs-lookup"><span data-stu-id="02901-113">Codec</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="02901-114">Allgemeine Videocodierung</span><span class="sxs-lookup"><span data-stu-id="02901-114">General-purpose video encoding</span></span></td>
<td><span data-ttu-id="02901-115"><a href="windowsmediavideo9encoder.md">Windows Media Video 9-Encoder</a></span><span class="sxs-lookup"><span data-stu-id="02901-115"><a href="windowsmediavideo9encoder.md">Windows Media Video 9 Encoder</a></span></span><dl> <span data-ttu-id="02901-116">Profil: Main</span><span class="sxs-lookup"><span data-stu-id="02901-116">Main Profile</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="02901-117">Codieren von High Definition-Videos oder-Videos, die dem SMPTE-Standard von VC-1 Advanced Profile entsprechen</span><span class="sxs-lookup"><span data-stu-id="02901-117">Encoding high definition video or video that conforms to the VC-1 Advanced Profile SMPTE standard</span></span></td>
<td><span data-ttu-id="02901-118"><a href="windowsmediavideo9encoder.md">Windows Media Video 9-Encoder</a></span><span class="sxs-lookup"><span data-stu-id="02901-118"><a href="windowsmediavideo9encoder.md">Windows Media Video 9 Encoder</a></span></span><dl> <span data-ttu-id="02901-119">Erweitertes Profil</span><span class="sxs-lookup"><span data-stu-id="02901-119">Advanced Profile</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="02901-120">Wandeln von Bitmapbildern in dynamisches Video</span><span class="sxs-lookup"><span data-stu-id="02901-120">Converting bitmapped images to dynamic video</span></span></td>
<td><span data-ttu-id="02901-121"><a href="windowsmediavideo9encoder.md">Windows Media Video 9-Encoder</a></span><span class="sxs-lookup"><span data-stu-id="02901-121"><a href="windowsmediavideo9encoder.md">Windows Media Video 9 Encoder</a></span></span><dl> <span data-ttu-id="02901-122">Image</span><span class="sxs-lookup"><span data-stu-id="02901-122">Image</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="02901-123">Codieren von Computern: Anwendungs Video (Bildschirmaufnahme) oder andere hoch statische Videos</span><span class="sxs-lookup"><span data-stu-id="02901-123">Encoding computer-application video (screen capture) or other highly static video</span></span></td>
<td><span data-ttu-id="02901-124"><a href="windowsmediavideo9screenencoder.md"><strong>Windows Media Video 9-Bildschirm Encoder</strong></a></span><span class="sxs-lookup"><span data-stu-id="02901-124"><a href="windowsmediavideo9screenencoder.md"><strong>Windows Media Video 9 Screen Encoder</strong></a></span></span></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="02901-125">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="02901-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="02901-126">Arbeiten mit Videos</span><span class="sxs-lookup"><span data-stu-id="02901-126">Working with Video</span></span>](workingwithvideo.md)
</dt> </dl>

 

 



