---
description: Audiodaten Ströme
ms.assetid: 8d361da3-a33a-401c-a750-f9b952022cf6
title: Audiodaten Ströme
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2f5c8c74f7507557f374d690a671b62e8b43343
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104482534"
---
# <a name="audio-and-subpicture-streams"></a><span data-ttu-id="6827c-103">Audiodaten Ströme</span><span class="sxs-lookup"><span data-stu-id="6827c-103">Audio and Subpicture Streams</span></span>

<span data-ttu-id="6827c-104">Eine DVD-Video Platte kann bis zu acht Audiostreams aufweisen, die von 0 bis 7 nummeriert sind und jeweils bis zu sechs diskrete Kanäle enthalten.</span><span class="sxs-lookup"><span data-stu-id="6827c-104">A DVD-Video disc can have up to eight audio streams, numbered zero through seven, each with up to six discrete channels.</span></span> <span data-ttu-id="6827c-105">(Beachten Sie, dass Audiodaten Ströme von 0 (null) nummeriert werden, während Titel, Winkel und Eltern Ebenen von eins nummeriert werden.) Nur einer dieser Streams kann zu einem bestimmten Zeitpunkt ausgewählt werden.</span><span class="sxs-lookup"><span data-stu-id="6827c-105">(Note that audio and subpicture streams are numbered from zero, whereas titles, angles, and parental levels are numbered from one.) Only one of these streams can be selected at any given time.</span></span> <span data-ttu-id="6827c-106">Für untergeordnete Bilder sind bis zu 32 Streams verfügbar, obwohl jeweils nur ein Stream aktiviert werden kann.</span><span class="sxs-lookup"><span data-stu-id="6827c-106">For subpictures, up to 32 streams are available, although only one stream can be activated at any given time.</span></span> <span data-ttu-id="6827c-107">Datenträger werden im Allgemeinen mit standardmäßigen Audiodaten und unter bildstreams erstellt, aber eine Anwendung kann es Benutzern ermöglichen, eine Liste aller verfügbaren Streams anzuzeigen und Sie in der von Ihnen bevorzugten Sprache auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="6827c-107">Discs are generally authored with default audio and subpicture streams, but an application can enable users to view a list of all the available streams, and select the one in the language they prefer.</span></span> <span data-ttu-id="6827c-108">Die grundlegenden Schritte in diesem Prozess sind sowohl für Audiodaten als auch für teilbildstreams identisch.</span><span class="sxs-lookup"><span data-stu-id="6827c-108">The basic steps in this process are the same for both audio and subpicture streams.</span></span>

1.  <span data-ttu-id="6827c-109">Legen Sie die Anzahl der für einen Titel verfügbaren Streams fest.</span><span class="sxs-lookup"><span data-stu-id="6827c-109">Determine the number of streams available for a title.</span></span>
2.  <span data-ttu-id="6827c-110">Iterieren Sie die Streams, und rufen Sie die Datenstrom Attribute für jedes ab.</span><span class="sxs-lookup"><span data-stu-id="6827c-110">Iterate through the streams and retrieve the stream attributes for each.</span></span>
3.  <span data-ttu-id="6827c-111">Rufen Sie den Sprachcode aus dem zurückgegebenen Gebiets Schema Bezeichner (LCID) ab, und erstellen Sie eine lesbare Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="6827c-111">Retrieve the language code from the returned locale identifier (LCID) and create a human-readable string.</span></span>
4.  <span data-ttu-id="6827c-112">Füllt ein Listenfeld oder eine andere Benutzeroberfläche (UI)-Steuerelement auf, um dem Benutzer die Auswahl eines bevorzugten Streams zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="6827c-112">Populate a list box or other user interface (UI) control to enable the user to select a preferred stream.</span></span>

<span data-ttu-id="6827c-113">In der DVD-Beispielanwendung veranschaulicht die caudiolangdlg:: makeaudiostreamlist-Methode in Dialogs. cpp die grundlegenden Schritte.</span><span class="sxs-lookup"><span data-stu-id="6827c-113">In the DVD sample application, the CAudioLangDlg::MakeAudioStreamList method in Dialogs.cpp demonstrates the basic steps.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6827c-114">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="6827c-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6827c-115">DVD-Anwendungen</span><span class="sxs-lookup"><span data-stu-id="6827c-115">DVD Applications</span></span>](dvd-applications.md)
</dt> </dl>

 

 



