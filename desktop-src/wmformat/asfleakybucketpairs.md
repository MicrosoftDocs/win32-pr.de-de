---
title: Asfleakybucketpair
description: Das asfleakybucketpair-Attribut ist ein optionales Attribut, das die Puffer Anforderungen für eine Variable-Bitrate-Datei beschreibt.
ms.assetid: d1b3e8cc-c082-4283-88bc-172f58adf2d9
keywords:
- Asfleakybucketpairs Windows Media-Format
topic_type:
- apiref
api_name:
- ASFLeakyBucketPairs
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e6e94bfa6084c67428fb89e57b9152283cc3d4a3
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "106342097"
---
# <a name="asfleakybucketpairs"></a><span data-ttu-id="74bc1-104">Asfleakybucketpair</span><span class="sxs-lookup"><span data-stu-id="74bc1-104">ASFLeakyBucketPairs</span></span>

<span data-ttu-id="74bc1-105">Das **asfleakybucketpair** -Attribut ist ein optionales Attribut, das die Puffer Anforderungen für eine Variable-Bitrate-Datei beschreibt.</span><span class="sxs-lookup"><span data-stu-id="74bc1-105">The **ASFLeakyBucketPairs** attribute is an optional attribute that describes the buffering requirements for a variable bit rate file.</span></span>

## <a name="global-constant"></a><span data-ttu-id="74bc1-106">Globale Konstante</span><span class="sxs-lookup"><span data-stu-id="74bc1-106">Global Constant</span></span>

<span data-ttu-id="74bc1-107">g \_ wszasfleakybucketpairs</span><span class="sxs-lookup"><span data-stu-id="74bc1-107">g\_wszASFLeakyBucketPairs</span></span>

## <a name="data-type"></a><span data-ttu-id="74bc1-108">Datentyp</span><span class="sxs-lookup"><span data-stu-id="74bc1-108">Data Type</span></span>

<span data-ttu-id="74bc1-109">**WMT \_ - \_ typbinär Datei**</span><span class="sxs-lookup"><span data-stu-id="74bc1-109">**WMT\_TYPE\_BINARY**</span></span>

## <a name="remarks"></a><span data-ttu-id="74bc1-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="74bc1-110">Remarks</span></span>

<span data-ttu-id="74bc1-111">Dieses Attribut weist das folgende Format auf:</span><span class="sxs-lookup"><span data-stu-id="74bc1-111">This attribute has the following format:</span></span>

``` syntax
struct
{
    WORD wReserved;
    WM_LEAKY_BUCKET_PAIR bucket[2];
};
```

<span data-ttu-id="74bc1-112">Dabei muss *wReserved* gleich NULL sein, und *Bucket* ist ein Array von WM-Lecks mit einem [**Bucket- \_ \_ \_ paar**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_leaky_bucket_pair) .</span><span class="sxs-lookup"><span data-stu-id="74bc1-112">Where *wReserved* must equal zero, and *bucket* is an array of [**WM\_LEAKY\_BUCKET\_PAIR**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_leaky_bucket_pair) structures.</span></span> <span data-ttu-id="74bc1-113">Das Array muss mindestens zwei Einträge enthalten, kann jedoch größer sein.</span><span class="sxs-lookup"><span data-stu-id="74bc1-113">The array must contain at least two entries, but can be larger.</span></span> <span data-ttu-id="74bc1-114">Das Reader-Objekt verwendet dieses Attribut, um zu bestimmen, wie viel Inhalt vor der Wiedergabe puffert werden soll.</span><span class="sxs-lookup"><span data-stu-id="74bc1-114">The reader object uses this attribute to determine the amount of content to buffer before playback.</span></span>

## <a name="see-also"></a><span data-ttu-id="74bc1-115">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="74bc1-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="74bc1-116">**Attributliste**</span><span class="sxs-lookup"><span data-stu-id="74bc1-116">**Attribute List**</span></span>](attribute-list.md)
</dt> </dl>

 

 




