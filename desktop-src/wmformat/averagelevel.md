---
title: Averagelevel
description: Das averagelevel-Attribut enthält einen 16-Bit-Amplitude-Wert, der die durchschnittliche Volumeebene von Audioinhalten festlegt.
ms.assetid: e6270ac8-5de3-4dee-824c-ba25fdd272c8
keywords:
- Averagelevel-Windows Media-Format
topic_type:
- apiref
api_name:
- AverageLevel
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 632379e42fa6c64e44018173b9d40340add4ee61
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "104037963"
---
# <a name="averagelevel"></a><span data-ttu-id="6e0c7-104">Averagelevel</span><span class="sxs-lookup"><span data-stu-id="6e0c7-104">AverageLevel</span></span>

<span data-ttu-id="6e0c7-105">Das **averagelevel** -Attribut enthält einen 16-Bit-Amplitude-Wert, der die durchschnittliche Volumeebene von Audioinhalten festlegt.</span><span class="sxs-lookup"><span data-stu-id="6e0c7-105">The **AverageLevel** attribute contains a 16-bit amplitude value designating the average volume level of audio content.</span></span> <span data-ttu-id="6e0c7-106">Mit " [**Peer Value**](peakvalue.md)" wird dieses Attribut für die Normalisierung verwendet.</span><span class="sxs-lookup"><span data-stu-id="6e0c7-106">With [**PeakValue**](peakvalue.md), this attribute is used for normalization.</span></span> <span data-ttu-id="6e0c7-107">Normalisierung ist der Prozess, bei dem die Wiedergabe Volume-Ebene von Audiodateien angepasst wird, sodass die laugsten Teile der Dateien wiedergegeben werden, die auf derselben Ebene wiedergegeben werden, und das durchschnittliche Volume.</span><span class="sxs-lookup"><span data-stu-id="6e0c7-107">Normalization is the process of adjusting the playback volume level of audio files so that the loudest parts of files playback at the same level and the average volume for each is the same.</span></span>

## <a name="global-constant"></a><span data-ttu-id="6e0c7-108">Globale Konstante</span><span class="sxs-lookup"><span data-stu-id="6e0c7-108">Global Constant</span></span>

<span data-ttu-id="6e0c7-109">g \_ wszaveragelevel</span><span class="sxs-lookup"><span data-stu-id="6e0c7-109">g\_wszAverageLevel</span></span>

## <a name="data-type"></a><span data-ttu-id="6e0c7-110">Datentyp</span><span class="sxs-lookup"><span data-stu-id="6e0c7-110">Data Type</span></span>

<span data-ttu-id="6e0c7-111">**WMT- \_ Typ \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="6e0c7-111">**WMT\_TYPE\_DWORD**</span></span>

## <a name="remarks"></a><span data-ttu-id="6e0c7-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6e0c7-112">Remarks</span></span>

<span data-ttu-id="6e0c7-113">Dieses Attribut wird durch das Writer-Objekt auf der Grundlage von Informationen aus dem Codec festgelegt.</span><span class="sxs-lookup"><span data-stu-id="6e0c7-113">This attribute is set by the writer object based on information from the codec.</span></span> <span data-ttu-id="6e0c7-114">Nur mit einem der Windows Media Audio Codecs komprimierte Streams haben einen automatisch festgelegten Wert.</span><span class="sxs-lookup"><span data-stu-id="6e0c7-114">Only streams compressed with one of the Windows Media Audio codecs have an automatically set value.</span></span>

<span data-ttu-id="6e0c7-115">**Averagelevel** ist nicht schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="6e0c7-115">**AverageLevel** is not read-only.</span></span> <span data-ttu-id="6e0c7-116">Wenn die Datei jedoch vom Windows-Media Player abgespielt wird, sollten Sie diesen Wert nicht ändern.</span><span class="sxs-lookup"><span data-stu-id="6e0c7-116">However, if the file will be played by the Windows Media Player, you should not alter this value.</span></span> <span data-ttu-id="6e0c7-117">Der Windows-Media Player verwendet diese, um die Ebenen von Dateien in einer Wiedergabeliste zu normalisieren.</span><span class="sxs-lookup"><span data-stu-id="6e0c7-117">The Windows Media Player uses this for normalizing the levels of files in a playlist.</span></span>

## <a name="see-also"></a><span data-ttu-id="6e0c7-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6e0c7-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6e0c7-119">**Attributliste**</span><span class="sxs-lookup"><span data-stu-id="6e0c7-119">**Attribute List**</span></span>](attribute-list.md)
</dt> </dl>

 

 




