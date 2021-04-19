---
title: Currentbitrate
description: Das currentbitrate-Attribut enthält die aktuelle gesamte Bitrate der aktiven Datenströme in der Datei.
ms.assetid: 961f36d5-a408-40d9-9ca1-0ed7c484858f
keywords:
- Currentbitrate Windows Media-Format
topic_type:
- apiref
api_name:
- CurrentBitrate
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bdcd8db7d60c65bcb7ceedcac4498ac650f90d9a
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "106339031"
---
# <a name="currentbitrate"></a><span data-ttu-id="ba91e-104">Currentbitrate</span><span class="sxs-lookup"><span data-stu-id="ba91e-104">CurrentBitrate</span></span>

<span data-ttu-id="ba91e-105">Das currentbitrate-Attribut enthält die aktuelle gesamte Bitrate der aktiven Datenströme in der Datei.</span><span class="sxs-lookup"><span data-stu-id="ba91e-105">The CurrentBitrate attribute contains the current total bit rate of the active streams in the file.</span></span>

## <a name="global-constant"></a><span data-ttu-id="ba91e-106">Globale Konstante</span><span class="sxs-lookup"><span data-stu-id="ba91e-106">Global Constant</span></span>

<span data-ttu-id="ba91e-107">g \_ wszwmcurrentbitrate</span><span class="sxs-lookup"><span data-stu-id="ba91e-107">g\_wszWMCurrentBitrate</span></span>

## <a name="data-type"></a><span data-ttu-id="ba91e-108">Datentyp</span><span class="sxs-lookup"><span data-stu-id="ba91e-108">Data Type</span></span>

<span data-ttu-id="ba91e-109">**WMT- \_ Typ \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="ba91e-109">**WMT\_TYPE\_DWORD**</span></span>

## <a name="remarks"></a><span data-ttu-id="ba91e-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ba91e-110">Remarks</span></span>

<span data-ttu-id="ba91e-111">Dies ist ein codiertes Attribut.</span><span class="sxs-lookup"><span data-stu-id="ba91e-111">This is a coded attribute.</span></span>

<span data-ttu-id="ba91e-112">Der Wert, der für **currentbitrate** abgerufen wird, unterscheidet sich je nach verwendetem Objekt.</span><span class="sxs-lookup"><span data-stu-id="ba91e-112">The value retrieved for **CurrentBitrate** is different depending upon the object used.</span></span> <span data-ttu-id="ba91e-113">Im Reader-oder synchronen Reader-Objekt ist der Wert die tatsächliche Bitrate zum Zeitpunkt des Aufrufes.</span><span class="sxs-lookup"><span data-stu-id="ba91e-113">In the reader or synchronous reader object, the value is the actual bit rate at the time of the call.</span></span> <span data-ttu-id="ba91e-114">Im Metadateneditor-Objekt ist der Wert die durchschnittliche Bitrate der Datei.</span><span class="sxs-lookup"><span data-stu-id="ba91e-114">In the metadata editor object, the value is the average bit rate of the file.</span></span>

<span data-ttu-id="ba91e-115">Die tatsächliche Bitrate einer Datei entspricht den Bitraten aller aktiven Streams plus einem gewissen Verwaltungsaufwand.</span><span class="sxs-lookup"><span data-stu-id="ba91e-115">The actual bit rate of a file is equal to the bit rates of all active streams plus some overhead.</span></span> <span data-ttu-id="ba91e-116">Dies ist der Wert, der beispielsweise angezeigt wird, wenn eine Datei mit dem Windows-Media Player wiedergegeben wird.</span><span class="sxs-lookup"><span data-stu-id="ba91e-116">This is the value that is, for example, displayed when playing a file with the Windows Media Player.</span></span>

<span data-ttu-id="ba91e-117">Dieses Attribut kann nicht auf Dateiebene dupliziert werden.</span><span class="sxs-lookup"><span data-stu-id="ba91e-117">This attribute cannot be duplicated at the file level.</span></span> <span data-ttu-id="ba91e-118">Wenn dieses Attribut für einen einzelnen Stream verwendet wird, wird es als benutzerdefinierte Metadaten behandelt und gibt seine normale Bedeutung nicht an die Objekte des Windows Media Format SDK aus.</span><span class="sxs-lookup"><span data-stu-id="ba91e-118">If this attribute is used for an individual stream, it will be treated as custom metadata and will not convey its normal meaning to the objects of the Windows Media Format SDK.</span></span>

## <a name="see-also"></a><span data-ttu-id="ba91e-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ba91e-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ba91e-120">**Attributliste**</span><span class="sxs-lookup"><span data-stu-id="ba91e-120">**Attribute List**</span></span>](attribute-list.md)
</dt> </dl>

 

 




