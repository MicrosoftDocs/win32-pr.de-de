---
title: WM/encodingtime
description: Das WM/encodingtime-Attribut enthält einen Zeitstempel der Zeit, zu der der Inhalt codiert wurde.
ms.assetid: 63da9392-264d-40bb-99fd-56db93801941
keywords:
- WM/encodingtime Windows Media-Format
topic_type:
- apiref
api_name:
- WM/EncodingTime
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9d27119a9b54e3de22fe620f556c672bd4fe1a17
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "104038177"
---
# <a name="wmencodingtime"></a><span data-ttu-id="79f68-104">WM/encodingtime</span><span class="sxs-lookup"><span data-stu-id="79f68-104">WM/EncodingTime</span></span>

<span data-ttu-id="79f68-105">Das **WM/encodingtime-** Attribut enthält einen Zeitstempel der Zeit, zu der der Inhalt codiert wurde.</span><span class="sxs-lookup"><span data-stu-id="79f68-105">The **WM/EncodingTime** attribute contains a time stamp of the time at which the content was encoded.</span></span>

## <a name="global-constant"></a><span data-ttu-id="79f68-106">Globale Konstante</span><span class="sxs-lookup"><span data-stu-id="79f68-106">Global Constant</span></span>

<span data-ttu-id="79f68-107">g \_ wszwmencodingtime</span><span class="sxs-lookup"><span data-stu-id="79f68-107">g\_wszWMEncodingTime</span></span>

## <a name="data-type"></a><span data-ttu-id="79f68-108">Datentyp</span><span class="sxs-lookup"><span data-stu-id="79f68-108">Data Type</span></span>

<span data-ttu-id="79f68-109">**FILETIME** (**WMT- \_ Typ \_ QWORD**)</span><span class="sxs-lookup"><span data-stu-id="79f68-109">**FILETIME** (**WMT\_TYPE\_QWORD**)</span></span>

## <a name="remarks"></a><span data-ttu-id="79f68-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="79f68-110">Remarks</span></span>

<span data-ttu-id="79f68-111">Dieses Attribut verwendet einen FILETIME-Wert. dabei handelt es sich um einen 64-Bit-Wert, der die Anzahl der seit dem 1. Januar 1601 verstrichenen 100-Nanosecond-Zeiteinheiten darstellt.</span><span class="sxs-lookup"><span data-stu-id="79f68-111">This attribute uses a FILETIME value, which is a 64-bit value representing the number of 100-nanosecond time units elapsed since January 1, 1601.</span></span> <span data-ttu-id="79f68-112">Weitere Informationen zur FILETIME finden Sie im Abschnitt Windows-System Informationen des Platform SDK.</span><span class="sxs-lookup"><span data-stu-id="79f68-112">For more information about the FILETIME, see the Windows System Information section of the Platform SDK.</span></span>

<span data-ttu-id="79f68-113">Dabei handelt es sich nicht um ein codiertes Attribut.</span><span class="sxs-lookup"><span data-stu-id="79f68-113">This is not a coded attribute.</span></span> <span data-ttu-id="79f68-114">Sie müssen es manuell festlegen, wenn Sie es in Ihre Dateien einschließen möchten.</span><span class="sxs-lookup"><span data-stu-id="79f68-114">You must set it manually if you want to include it in your files.</span></span>

## <a name="see-also"></a><span data-ttu-id="79f68-115">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="79f68-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="79f68-116">**Attributliste**</span><span class="sxs-lookup"><span data-stu-id="79f68-116">**Attribute List**</span></span>](attribute-list.md)
</dt> </dl>

 

 




