---
title: Allgemeine Konfiguration für alle Streams
description: Allgemeine Konfiguration für alle Streams
ms.assetid: 63e655b7-a4ef-4580-a0f3-03cedd2cbf9a
keywords:
- Profile, Konfigurationen, die für alle Streams gemeinsam sind
- Streams, allgemeine Konfigurationen
- Streams, Namen
- Streams, Verbindungs Namen
- Streams, Zahlen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f1a398256da99092da45e83ebc91de713f9ab71
ms.sourcegitcommit: c2a1c4314550ea9bd202d28adfcc7bfe6180932f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2020
ms.locfileid: "104390080"
---
# <a name="configuration-common-to-all-streams"></a><span data-ttu-id="1326c-108">Allgemeine Konfiguration für alle Streams</span><span class="sxs-lookup"><span data-stu-id="1326c-108">Configuration Common to All Streams</span></span>

<span data-ttu-id="1326c-109">Allen Streams sollten unabhängig vom Typ ein Datenstrom Name, ein Verbindungs Name und eine streamnummer zugewiesen werden.</span><span class="sxs-lookup"><span data-stu-id="1326c-109">All streams, regardless of type, should be assigned a stream name, a connection name, and a stream number.</span></span>

<span data-ttu-id="1326c-110">Der Datenstrom Name ist einfach ein beschreibender Name, den Sie dem Stream zuweisen.</span><span class="sxs-lookup"><span data-stu-id="1326c-110">The stream name is simply a descriptive name you assign to the stream.</span></span> <span data-ttu-id="1326c-111">Ein Datenstrom benötigt keinen Datenstrom Namen, aber er hilft Ihnen, den Stream zu identifizieren, wenn er das Profil zu einem späteren Zeitpunkt bearbeitet.</span><span class="sxs-lookup"><span data-stu-id="1326c-111">A stream does not need to have a stream name, but it helps you to identify the stream when editing the profile at a later time.</span></span> <span data-ttu-id="1326c-112">Sie können einen Namen für den Stream durch Aufrufen von [**iwmstreamconfig:: setstreamname**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig-setstreamname)festlegen.</span><span class="sxs-lookup"><span data-stu-id="1326c-112">You can set a name for the stream by calling [**IWMStreamConfig::SetStreamName**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig-setstreamname).</span></span>

<span data-ttu-id="1326c-113">Jeder Stream sollte über einen Verbindungs Namen verfügen, der auch als Eingabe Name bezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="1326c-113">Every stream should have a connection name, also called an input name.</span></span> <span data-ttu-id="1326c-114">Wenn Sie das Profil im Writer-Objekt so festlegen, dass eine Datei geschrieben wird, ordnet der Writer jeden Verbindungs Namen einer Eingabe zu.</span><span class="sxs-lookup"><span data-stu-id="1326c-114">When you set the profile in the writer object to write a file, the writer will associate each connection name with an input.</span></span> <span data-ttu-id="1326c-115">Zum Identifizieren der Eingaben müssen Sie [**iwminputmediarequi:: getConnectionName**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwminputmediaprops-getconnectionname) aufrufen, um den Verbindungs Namen abzurufen.</span><span class="sxs-lookup"><span data-stu-id="1326c-115">To identify the inputs, you must call [**IWMInputMediaProps::GetConnectionName**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwminputmediaprops-getconnectionname) to retrieve the connection name.</span></span> <span data-ttu-id="1326c-116">Typische Verbindungs Namen sind einfache Beschreibungen der Inhalte, z. b. "Audiodaten".</span><span class="sxs-lookup"><span data-stu-id="1326c-116">Typical connection names are simple descriptions of the content, such as "audio".</span></span> <span data-ttu-id="1326c-117">Wenn Ihr Profildaten Ströme enthält, die sich durch die Bitrate gegenseitig ausschließen, muss jeder der sich gegenseitig ausschließenden Datenströme denselben Verbindungs Namen aufweisen.</span><span class="sxs-lookup"><span data-stu-id="1326c-117">If your profile contains streams that are mutually exclusive by bit rate, each of the mutually exclusive streams must have the same connection name.</span></span> <span data-ttu-id="1326c-118">Wenn dies nicht der Fall ist, ist das Profil ungültig und wird vom Writer abgelehnt.</span><span class="sxs-lookup"><span data-stu-id="1326c-118">If they do not, the profile is invalid and will be rejected by the writer.</span></span> <span data-ttu-id="1326c-119">Sie können einen Verbindungs Namen durch Aufrufen von [**iwmstreamconfig:: setconnectionname**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig-setconnectionname)festlegen.</span><span class="sxs-lookup"><span data-stu-id="1326c-119">You can set a connection name by calling [**IWMStreamConfig::SetConnectionName**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig-setconnectionname).</span></span>

<span data-ttu-id="1326c-120">Die streamnummer identifiziert den Stream innerhalb der Datei.</span><span class="sxs-lookup"><span data-stu-id="1326c-120">The stream number identifies the stream within the file.</span></span> <span data-ttu-id="1326c-121">Im Unterschied zu Eingabe-und Ausgabe Nummern beginnen streamnummern bei 1 und nicht bei 0.</span><span class="sxs-lookup"><span data-stu-id="1326c-121">Unlike input numbers and output numbers, stream numbers start at 1, not 0.</span></span> <span data-ttu-id="1326c-122">Eine streamnummer unterscheidet sich von einem streamindex, den Sie verwenden, wenn Sie Datenströme in einem Profil mithilfe von [**iwmprofile:: GetStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-getstream)erhalten.</span><span class="sxs-lookup"><span data-stu-id="1326c-122">A stream number is different than a stream index, which you use when getting streams in a profile by using [**IWMProfile::GetStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-getstream).</span></span> <span data-ttu-id="1326c-123">Der streamindex ist eine Zahl, die dem Stream vom Profil Objekt zugewiesen wird.</span><span class="sxs-lookup"><span data-stu-id="1326c-123">The stream index is a number assigned to the stream by the profile object.</span></span> <span data-ttu-id="1326c-124">Streamindexe liegen zwischen 0 und eins kleiner als die Anzahl von Datenströmen, die von [**iwmprofile:: getstreamcount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmprofile-getstreamcount)abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="1326c-124">Stream indexes range between 0 and one less than the number of streams retrieved by [**IWMProfile::GetStreamCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmprofile-getstreamcount).</span></span> <span data-ttu-id="1326c-125">Streamnummern müssen nicht sequenziell sein, Sie sind jedoch in der Regel gleich und können zwischen 1 und 63 liegen.</span><span class="sxs-lookup"><span data-stu-id="1326c-125">Stream numbers need not be sequential, though they usually are, and can range from 1 to 63.</span></span> <span data-ttu-id="1326c-126">Sie können eine streamnummer festlegen, indem Sie [**iwmstreamconfig:: setstreamnumber**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig-setstreamnumber)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="1326c-126">You can set a stream number by calling [**IWMStreamConfig::SetStreamNumber**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig-setstreamnumber).</span></span>

## <a name="related-topics"></a><span data-ttu-id="1326c-127">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="1326c-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1326c-128">**Konfigurieren von Streams**</span><span class="sxs-lookup"><span data-stu-id="1326c-128">**Configuring Streams**</span></span>](configuring-streams.md)
</dt> <dt>

[<span data-ttu-id="1326c-129">**Eingaben, Streams und Ausgaben**</span><span class="sxs-lookup"><span data-stu-id="1326c-129">**Inputs, Streams and Outputs**</span></span>](inputs-streams-and-outputs.md)
</dt> </dl>

 

 




