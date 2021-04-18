---
description: Gibt die Kanal Matrix an, die verwendet wird, um die Quell Kanäle in die Ziel Kanäle zu konvertieren (z. b. um 5,1 in Stereo umzuwandeln).
ms.assetid: 2f2a82bd-f051-4b05-a9c8-37aa4403fab4
title: MFPKEY_WMRESAMP_CHANNELMTX-Eigenschaft (wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e39f9a9344dd080362859592fcf1f71657ee8f7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106354623"
---
# <a name="mfpkey_wmresamp_channelmtx-property"></a><span data-ttu-id="675f6-103">Mfpkey \_ wmresamp \_ channelmtx-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="675f6-103">MFPKEY\_WMRESAMP\_CHANNELMTX Property</span></span>

<span data-ttu-id="675f6-104">Gibt die Kanal Matrix an, die verwendet wird, um die Quell Kanäle in die Ziel Kanäle zu konvertieren (z. b. um 5,1 in Stereo umzuwandeln).</span><span class="sxs-lookup"><span data-stu-id="675f6-104">Specifies the channel matrix, which is used to convert the source channels into the destination channels (for example, to convert 5.1 to stereo).</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="675f6-105">Konstante für IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="675f6-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="675f6-106">Nur mit [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)verfügbar.</span><span class="sxs-lookup"><span data-stu-id="675f6-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="675f6-107">Datentyp</span><span class="sxs-lookup"><span data-stu-id="675f6-107">Data Type</span></span>

<span data-ttu-id="675f6-108">VT \_ I4 \| VT- \_ Array</span><span class="sxs-lookup"><span data-stu-id="675f6-108">VT\_I4 \| VT\_ARRAY</span></span>

## <a name="applies-to"></a><span data-ttu-id="675f6-109">Gilt für</span><span class="sxs-lookup"><span data-stu-id="675f6-109">Applies To</span></span>

-   [<span data-ttu-id="675f6-110">Audioresampler-DSP</span><span class="sxs-lookup"><span data-stu-id="675f6-110">Audio Resampler DSP</span></span>](audioresampler.md)

## <a name="remarks"></a><span data-ttu-id="675f6-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="675f6-111">Remarks</span></span>

<span data-ttu-id="675f6-112">Der Wert der-Eigenschaft ist eine Matrix aus NS x-Koeffizienten, wobei "NS" die Anzahl der Quell Kanäle und "ND" die Anzahl der Ziel Kanäle ist.</span><span class="sxs-lookup"><span data-stu-id="675f6-112">The value of the property is a matrix of Ns x Nd coefficients, where Ns is the number of source channels and Nd is the number of destination channels.</span></span> <span data-ttu-id="675f6-113">Koeffizienten werden mithilfe der folgenden Formel in Dezibel angegeben:</span><span class="sxs-lookup"><span data-stu-id="675f6-113">Coefficients are specified in decibels using the following formula:</span></span>

<span data-ttu-id="675f6-114">wartenden (65536 \* 20 \* log10 (DB))</span><span class="sxs-lookup"><span data-stu-id="675f6-114">(int)(65536\*20\*log10(dB))</span></span>

<span data-ttu-id="675f6-115">Die Matrix wird als Array in der Reihenfolge der Zeilen in der Reihenfolge gespeichert, in der die Zeilennummer der Quell Kanal und die Spaltennummer der Zielchannel ist.</span><span class="sxs-lookup"><span data-stu-id="675f6-115">The matrix is stored as an array in row-major order where the row number is the source channel and the column number is the destination channel.</span></span>

<span data-ttu-id="675f6-116">Wenn die Matrix beispielsweise folgendermaßen lautet:</span><span class="sxs-lookup"><span data-stu-id="675f6-116">Thus, if the matrix is the following:</span></span>

``` syntax
00       01       ...      0(Ns-1)
10       11       ...      1(Ns-1)
...      ...      ...      ...
(Nd-1)0 (Nd-1)1 ... (Nd-1)(Ns-1)
```

<span data-ttu-id="675f6-117">Anschließend geben Sie das Array wie folgt an:</span><span class="sxs-lookup"><span data-stu-id="675f6-117">then you would specify the array as:</span></span>

``` syntax
[ 00, 01, ..., 0(Ns-1), 10, 11, ..., 1(Ns-1), ..., (Nd-1)0, (Nd-1)1, ..., (Nd-1)(Ns-1) ]
```

## <a name="requirements"></a><span data-ttu-id="675f6-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="675f6-118">Requirements</span></span>



| <span data-ttu-id="675f6-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="675f6-119">Requirement</span></span> | <span data-ttu-id="675f6-120">Wert</span><span class="sxs-lookup"><span data-stu-id="675f6-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="675f6-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="675f6-121">Minimum supported client</span></span><br/> | <span data-ttu-id="675f6-122">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="675f6-122">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="675f6-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="675f6-123">Minimum supported server</span></span><br/> | <span data-ttu-id="675f6-124">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="675f6-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="675f6-125">Header</span><span class="sxs-lookup"><span data-stu-id="675f6-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="675f6-126"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="675f6-126"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="675f6-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="675f6-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="675f6-128">Eigenschaften von Media Foundation</span><span class="sxs-lookup"><span data-stu-id="675f6-128">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
