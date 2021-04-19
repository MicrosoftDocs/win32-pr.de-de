---
title: Peer Value
description: Das peakvalue-Attribut enthält einen 16-Bit-Amplitude-Wert, der die maximale Volumeebene von Audioinhalten festlegt.
ms.assetid: 885f6d4c-661a-4681-96b6-c1a282c8bf18
keywords:
- Windows Media-Format von "Peer Value"
topic_type:
- apiref
api_name:
- PeakValue
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 37ef933ec1b10555aa4c88a24261313abb261163
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "106341895"
---
# <a name="peakvalue"></a><span data-ttu-id="8b353-104">Peer Value</span><span class="sxs-lookup"><span data-stu-id="8b353-104">PeakValue</span></span>

<span data-ttu-id="8b353-105">Das **peakvalue** -Attribut enthält einen 16-Bit-Amplitude-Wert, der die maximale Volumeebene von Audioinhalten festlegt.</span><span class="sxs-lookup"><span data-stu-id="8b353-105">The **PeakValue** attribute contains contains a 16-bit amplitude value designating the peak volume level of audio content.</span></span> <span data-ttu-id="8b353-106">Bei [**averagelevel**](averagelevel.md)wird dieses Attribut für die Normalisierung verwendet.</span><span class="sxs-lookup"><span data-stu-id="8b353-106">With [**AverageLevel**](averagelevel.md), this attribute is used for normalization.</span></span> <span data-ttu-id="8b353-107">Normalisierung ist der Prozess, bei dem die Wiedergabe Volume-Ebene von Audiodateien angepasst wird, sodass die laugsten Teile von Dateien, die auf derselben Ebene wiedergegeben werden, und das durchschnittliche Volume für die beiden identisch sind.</span><span class="sxs-lookup"><span data-stu-id="8b353-107">Normalization is the process of adjusting the playback volume level of audio files so that the loudest parts of files playback at the same level and the average volume for each is the same..</span></span>

## <a name="global-constant"></a><span data-ttu-id="8b353-108">Globale Konstante</span><span class="sxs-lookup"><span data-stu-id="8b353-108">Global Constant</span></span>

<span data-ttu-id="8b353-109">g \_ wszpeer Value</span><span class="sxs-lookup"><span data-stu-id="8b353-109">g\_wszPeakValue</span></span>

## <a name="data-type"></a><span data-ttu-id="8b353-110">Datentyp</span><span class="sxs-lookup"><span data-stu-id="8b353-110">Data Type</span></span>

<span data-ttu-id="8b353-111">**WMT- \_ Typ \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="8b353-111">**WMT\_TYPE\_DWORD**</span></span>

## <a name="remarks"></a><span data-ttu-id="8b353-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8b353-112">Remarks</span></span>

<span data-ttu-id="8b353-113">Dieses Attribut wird durch das Writer-Objekt auf der Grundlage von Informationen aus dem Codec festgelegt.</span><span class="sxs-lookup"><span data-stu-id="8b353-113">This attribute is set by the writer object based on information from the codec.</span></span> <span data-ttu-id="8b353-114">Nur mit einem der Windows Media Audio Codecs komprimierte Streams haben einen automatisch festgelegten Wert.</span><span class="sxs-lookup"><span data-stu-id="8b353-114">Only streams compressed with one of the Windows Media Audio codecs have an automatically set value.</span></span>

<span data-ttu-id="8b353-115">" **Peer Value** " ist nicht schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="8b353-115">**PeakValue** is not read-only.</span></span> <span data-ttu-id="8b353-116">Wenn die Datei jedoch vom Windows-Media Player abgespielt wird, sollten Sie diesen Wert nicht ändern.</span><span class="sxs-lookup"><span data-stu-id="8b353-116">However, if the file will be played by the Windows Media Player, you should not alter this value.</span></span> <span data-ttu-id="8b353-117">Der Windows-Media Player verwendet diese, um die Ebenen von Dateien in einer Wiedergabeliste zu normalisieren.</span><span class="sxs-lookup"><span data-stu-id="8b353-117">The Windows Media Player uses this for normalizing the levels of files in a playlist.</span></span>

## <a name="see-also"></a><span data-ttu-id="8b353-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8b353-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8b353-119">**Attributliste**</span><span class="sxs-lookup"><span data-stu-id="8b353-119">**Attribute List**</span></span>](attribute-list.md)
</dt> </dl>

 

 




