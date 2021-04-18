---
description: Wiedergabe von Karaoke-Audiostreams
ms.assetid: 1a8d0f42-35b8-4743-9ae7-619b99936f76
title: Wiedergabe von Karaoke-Audiostreams
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 907bfa3e359915cf537de75cdc739630fe607d97
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106343564"
---
# <a name="playing-karaoke-audio-streams"></a><span data-ttu-id="31d0b-103">Wiedergabe von Karaoke-Audiostreams</span><span class="sxs-lookup"><span data-stu-id="31d0b-103">Playing Karaoke Audio Streams</span></span>

<span data-ttu-id="31d0b-104">Der DVD-Navigator kann DVD-Video-CDs mit Karaoke-Audiostreams wiedergeben, aber die Karaoke-Wiedergabe erfordert auch einen Decoder, der eine Multichannel-Karaoke-Mischung</span><span class="sxs-lookup"><span data-stu-id="31d0b-104">The DVD Navigator can play DVD-Video discs with karaoke audio streams, but karaoke playback also requires a decoder that supports multichannel karaoke mixing.</span></span> <span data-ttu-id="31d0b-105">Insbesondere muss der Decoder den DVD- [**Karaoke-Eigenschaften Satz**](dvd-karaoke-property-set.md) unterstützen (am \_ Eigenschaft \_ dvdkaraoke).</span><span class="sxs-lookup"><span data-stu-id="31d0b-105">Specifically, the decoder must support the [**DVD Karaoke Property Set**](dvd-karaoke-property-set.md) (AM\_PROPERTY\_DVDKARAOKE).</span></span>

<span data-ttu-id="31d0b-106">Bei den Karaoke-Festplatten handelt es sich um einen Typ von DVD-Video-CD und die gleiche Navigationsstruktur.</span><span class="sxs-lookup"><span data-stu-id="31d0b-106">Karaoke discs are a type of DVD-Video disc and have the same navigation structure.</span></span> <span data-ttu-id="31d0b-107">Lieder werden im Allgemeinen als Titel formatiert, und Titel können auf der Grundlage von Interpreten, musikalischem Stil oder anderen Kriterien in Titel Gruppen gruppiert werden.</span><span class="sxs-lookup"><span data-stu-id="31d0b-107">Songs are generally formatted as titles, and titles can be grouped into title sets based on performer, musical style, or other criteria.</span></span> <span data-ttu-id="31d0b-108">Der Hauptunterschied zwischen Karaoke und anderen Typen von DVD-Videos ist der Audiodatenstrom.</span><span class="sxs-lookup"><span data-stu-id="31d0b-108">The main difference between karaoke and other types of DVD-Videos is the audio stream.</span></span> <span data-ttu-id="31d0b-109">Alle Karaoke-Datenträger enthalten Multichannel-Audiodaten, normalerweise Dolby AC-3.</span><span class="sxs-lookup"><span data-stu-id="31d0b-109">Karaoke discs all contain multichannel audio, usually Dolby AC-3.</span></span> <span data-ttu-id="31d0b-110">Die Kanäle 0 und 1 enthalten immer die Hintergrund Instrumentalmusik, während die Kanäle 2 bis 5 jede beliebige Kombination aus Führungs Gesang, Führungs Melodien und Soundeffekten enthalten können.</span><span class="sxs-lookup"><span data-stu-id="31d0b-110">Channels 0 and 1 always contain the background instrumental music, while channels 2 through 5 can each contain any combination of guide vocals, guide melodies, and sound effects.</span></span> <span data-ttu-id="31d0b-111">Eine Karaoke-Anwendung kann das Volume und den Ziel Sprecher für jeden hilfsanchannel steuern.</span><span class="sxs-lookup"><span data-stu-id="31d0b-111">A karaoke application can control the volume and destination speaker for each auxiliary channel.</span></span>

<span data-ttu-id="31d0b-112">Wenn der DVD-Navigator einen Karaoke-Inhalt auf einer CD erkennt und in den Karaoke-Modus wechselt, wird der Decoder informiert, der die oberen drei Kanäle (die zusätzlichen Kanäle) stumm schalten sollte, bis eine oder alle davon explizit von einer Anwendung aktiviert werden.</span><span class="sxs-lookup"><span data-stu-id="31d0b-112">When the DVD Navigator detects karaoke content on a disc and goes into karaoke mode, it informs the decoder, which then should mute the upper three channels (the auxiliary channels) until any or all of them are explicitly turned on by an application.</span></span> <span data-ttu-id="31d0b-113">Die grundlegenden Aufgaben einer Karaoke-Anwendung sind:</span><span class="sxs-lookup"><span data-stu-id="31d0b-113">The basic tasks of a karaoke application are to:</span></span>

1.  <span data-ttu-id="31d0b-114">Bestimmen Sie die Anzahl von zusätzlichen Kanälen und deren Inhalt mithilfe der [**IDvdInfo2**](/windows/desktop/api/Strmif/nn-strmif-idvdinfo2) -Methoden.</span><span class="sxs-lookup"><span data-stu-id="31d0b-114">Determine the number of auxiliary channels and their contents using [**IDvdInfo2**](/windows/desktop/api/Strmif/nn-strmif-idvdinfo2) methods.</span></span>
2.  <span data-ttu-id="31d0b-115">Stellen Sie eine Benutzeroberfläche bereit, auf der der Kanal Inhalt angezeigt wird, und ermöglichen Sie es Benutzern, mithilfe von [**IDvdControl2:: selectkaraokeaudiopresentationmode**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-selectkaraokeaudiopresentationmode)jederzeit einen beliebigen hilfsanchannel zu aktivieren bzw. zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="31d0b-115">Provide a user interface that displays the channel contents and enables users to turn any auxiliary channel on or off at any time, using [**IDvdControl2::SelectKaraokeAudioPresentationMode**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-selectkaraokeaudiopresentationmode).</span></span>

<span data-ttu-id="31d0b-116">Diese Schritte werden in der Anwendung "DVD-Beispiel" in "dvdcore. cpp" in der Methode " **getaudioattributs** " veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="31d0b-116">These steps are illustrated in the DVD Sample application in DVDCore.cpp in the **GetAudioAttributes** method.</span></span>

## <a name="related-topics"></a><span data-ttu-id="31d0b-117">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="31d0b-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="31d0b-118">DVD-Anwendungen</span><span class="sxs-lookup"><span data-stu-id="31d0b-118">DVD Applications</span></span>](dvd-applications.md)
</dt> </dl>

 

 



