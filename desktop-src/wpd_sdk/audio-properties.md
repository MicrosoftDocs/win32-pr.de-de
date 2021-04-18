---
description: Tragbare Windows-Geräte unterstützen die folgenden Audioeigenschaften.
ms.assetid: 5d6c6a95-abb7-4191-a961-bcb30ca96bb6
title: Audioeigenschaften (portabledevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Audio
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 1bdab201fc987d5bc1aff3638fbb57358115fdce
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106357995"
---
# <a name="audio-properties"></a><span data-ttu-id="847a2-103">Audioeigenschaften</span><span class="sxs-lookup"><span data-stu-id="847a2-103">Audio Properties</span></span>

<span data-ttu-id="847a2-104">Tragbare Windows-Geräte unterstützen die folgenden Audioeigenschaften.</span><span class="sxs-lookup"><span data-stu-id="847a2-104">Windows Portable Devices supports the following audio properties.</span></span>



| <span data-ttu-id="847a2-105">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="847a2-105">Property</span></span>                         | <span data-ttu-id="847a2-106">VarType</span><span class="sxs-lookup"><span data-stu-id="847a2-106">VarType</span></span>     | <span data-ttu-id="847a2-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="847a2-107">Description</span></span>                                                                                                                                                                                                        |
|----------------------------------|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="847a2-108">**WPD \_ - \_ \_ audiobittiefe**</span><span class="sxs-lookup"><span data-stu-id="847a2-108">**WPD\_AUDIO\_BIT\_DEPTH**</span></span>       | <span data-ttu-id="847a2-109">**VT \_ UI4**</span><span class="sxs-lookup"><span data-stu-id="847a2-109">**VT\_UI4**</span></span> | <span data-ttu-id="847a2-110">Die Bittiefe der Audiodatei.</span><span class="sxs-lookup"><span data-stu-id="847a2-110">The bit-depth of the audio.</span></span>                                                                                                                                                                                        |
| <span data-ttu-id="847a2-111">**WPD \_ - \_ Audiobitrate**</span><span class="sxs-lookup"><span data-stu-id="847a2-111">**WPD\_AUDIO\_BITRATE**</span></span>          | <span data-ttu-id="847a2-112">**VT \_ UI4**</span><span class="sxs-lookup"><span data-stu-id="847a2-112">**VT\_UI4**</span></span> | <span data-ttu-id="847a2-113">Die Bitrate der Audiodaten (in Bits pro Sekunde).</span><span class="sxs-lookup"><span data-stu-id="847a2-113">The bit rate of the audio, in bits per second.</span></span>                                                                                                                                                                     |
| <span data-ttu-id="847a2-114">**WPD \_ - \_ Audioblock \_ Ausrichtung**</span><span class="sxs-lookup"><span data-stu-id="847a2-114">**WPD\_AUDIO\_BLOCK\_ALIGNMENT**</span></span> | <span data-ttu-id="847a2-115">**VT \_ UI4**</span><span class="sxs-lookup"><span data-stu-id="847a2-115">**VT\_UI4**</span></span> | <span data-ttu-id="847a2-116">Die Block Ausrichtung der Audiodatei in Bytes.</span><span class="sxs-lookup"><span data-stu-id="847a2-116">The block alignment of the audio file, in bytes.</span></span>                                                                                                                                                                   |
| <span data-ttu-id="847a2-117">**Anzahl von WPD \_ - \_ Audiokanälen \_**</span><span class="sxs-lookup"><span data-stu-id="847a2-117">**WPD\_AUDIO\_CHANNEL\_COUNT**</span></span>   | <span data-ttu-id="847a2-118">**VT \_ R4**</span><span class="sxs-lookup"><span data-stu-id="847a2-118">**VT\_R4**</span></span>  | <span data-ttu-id="847a2-119">Die Anzahl der Kanäle in dieser Audiodatei, z. b. 1, 2 oder 5,1.</span><span class="sxs-lookup"><span data-stu-id="847a2-119">The number of channels in this audio file, for example, 1, 2, or 5.1.</span></span>                                                                                                                                              |
| <span data-ttu-id="847a2-120">**WPD \_ - \_ \_ audioformatcode**</span><span class="sxs-lookup"><span data-stu-id="847a2-120">**WPD\_AUDIO\_FORMAT\_CODE**</span></span>     | <span data-ttu-id="847a2-121">**VT \_ UI4**</span><span class="sxs-lookup"><span data-stu-id="847a2-121">**VT\_UI4**</span></span> | <span data-ttu-id="847a2-122">Die registrierte Wave-Format-Codenummer.</span><span class="sxs-lookup"><span data-stu-id="847a2-122">The registered WAVE format code number.</span></span> <span data-ttu-id="847a2-123">Eine Auflistung registrierter Wellen Formate finden Sie im Artikel [registrierte FOURCC Codes und Wave Formats](https://msdn2.microsoft.com/library/ms867195.aspx) auf der MSDN-Website.</span><span class="sxs-lookup"><span data-stu-id="847a2-123">For a listing of registered WAVE formats, see the article [Registered FOURCC Codes and WAVE Formats](https://msdn2.microsoft.com/library/ms867195.aspx) on the MSDN Web site.</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="847a2-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="847a2-124">Requirements</span></span>



| <span data-ttu-id="847a2-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="847a2-125">Requirement</span></span> | <span data-ttu-id="847a2-126">Wert</span><span class="sxs-lookup"><span data-stu-id="847a2-126">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="847a2-127">Header</span><span class="sxs-lookup"><span data-stu-id="847a2-127">Header</span></span><br/> | <dl> <span data-ttu-id="847a2-128"><dt>Portabledevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="847a2-128"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="847a2-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="847a2-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="847a2-130">**WPD-Eigenschaften und-Attribute**</span><span class="sxs-lookup"><span data-stu-id="847a2-130">**WPD Properties and Attributes**</span></span>](properties-and-attributes.md)
</dt> </dl>

 

 




