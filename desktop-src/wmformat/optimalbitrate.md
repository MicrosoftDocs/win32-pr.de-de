---
title: Optimalbitrate
description: Das optimalbitrate-Attribut enthält die Bitrate, in der die Datei am besten wiedergegeben wird.
ms.assetid: cd13b9b5-34d2-4ebb-9f10-3bf42dd9de81
keywords:
- Optimalbitrate Windows Media-Format
topic_type:
- apiref
api_name:
- OptimalBitrate
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff71c6b64cbc4bf4ccc4f346e62a5eae066e78ce
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "106341898"
---
# <a name="optimalbitrate"></a><span data-ttu-id="c751e-104">Optimalbitrate</span><span class="sxs-lookup"><span data-stu-id="c751e-104">OptimalBitrate</span></span>

<span data-ttu-id="c751e-105">Das **optimalbitrate** -Attribut enthält die Bitrate, in der die Datei am besten wiedergegeben wird.</span><span class="sxs-lookup"><span data-stu-id="c751e-105">The **OptimalBitrate** attribute contains the bit rate at which the file is best played.</span></span>

## <a name="global-constant"></a><span data-ttu-id="c751e-106">Globale Konstante</span><span class="sxs-lookup"><span data-stu-id="c751e-106">Global Constant</span></span>

<span data-ttu-id="c751e-107">g \_ wszwmoptimalbitrate</span><span class="sxs-lookup"><span data-stu-id="c751e-107">g\_wszWMOptimalBitrate</span></span>

## <a name="data-type"></a><span data-ttu-id="c751e-108">Datentyp</span><span class="sxs-lookup"><span data-stu-id="c751e-108">Data Type</span></span>

<span data-ttu-id="c751e-109">**WMT- \_ Typ \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="c751e-109">**WMT\_TYPE\_DWORD**</span></span>

## <a name="remarks"></a><span data-ttu-id="c751e-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c751e-110">Remarks</span></span>

<span data-ttu-id="c751e-111">Dies ist ein codiertes Attribut.</span><span class="sxs-lookup"><span data-stu-id="c751e-111">This is a coded attribute.</span></span>

<span data-ttu-id="c751e-112">Bei Dateien, die VBR-Streams (Variable Bitrate) enthalten, ist dieser Wert die Spitzen Bitrate für die Datenströme in der Datei.</span><span class="sxs-lookup"><span data-stu-id="c751e-112">For files that contain variable bit rate (VBR) streams, this value is the peak bit rate for the streams in the file.</span></span> <span data-ttu-id="c751e-113">Bei Dateien ohne VBR ist dieser Wert mit der [**Bitrate**](bit-rate.md)identisch.</span><span class="sxs-lookup"><span data-stu-id="c751e-113">For files without VBR, this value is the same as [**Bitrate**](bit-rate.md).</span></span>

<span data-ttu-id="c751e-114">Dieses Attribut kann nicht auf Dateiebene dupliziert werden.</span><span class="sxs-lookup"><span data-stu-id="c751e-114">This attribute cannot be duplicated at the file level.</span></span> <span data-ttu-id="c751e-115">Wenn dieses Attribut für einen einzelnen Stream verwendet wird, wird es als benutzerdefinierte Metadaten behandelt und gibt seine normale Bedeutung nicht an die Objekte des Windows Media Format SDK aus.</span><span class="sxs-lookup"><span data-stu-id="c751e-115">If this attribute is used for an individual stream, it will be treated as custom metadata and will not convey its normal meaning to the objects of the Windows Media Format SDK.</span></span>

## <a name="see-also"></a><span data-ttu-id="c751e-116">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c751e-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c751e-117">**Attributliste**</span><span class="sxs-lookup"><span data-stu-id="c751e-117">**Attribute List**</span></span>](attribute-list.md)
</dt> </dl>

 

 




