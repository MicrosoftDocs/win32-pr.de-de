---
description: Gibt an, ob der Encoder für doppelte Frames Dummy-Frame-Einträge im Bitdaten Strom erzeugt.
ms.assetid: dc09cecb-98c0-40bb-9e5d-f4661bf98522
title: MFPKEY_PRODUCEDUMMYFRAMES-Eigenschaft (wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1b40bdaa54b3dc14a2b4ef44235d7f87cab5b905
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215501"
---
# <a name="mfpkey_producedummyframes-property"></a><span data-ttu-id="712fc-103">Mfpkey \_ producedummyframes (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="712fc-103">MFPKEY\_PRODUCEDUMMYFRAMES Property</span></span>

<span data-ttu-id="712fc-104">Gibt an, ob der Encoder für doppelte Frames Dummy-Frame-Einträge im Bitdaten Strom erzeugt.</span><span class="sxs-lookup"><span data-stu-id="712fc-104">Specifies whether the encoder produces dummy frame entries in the bit stream for duplicate frames.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="712fc-105">Konstante für IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="712fc-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="712fc-106">g \_ wszwmvcproducedummyframes</span><span class="sxs-lookup"><span data-stu-id="712fc-106">g\_wszWMVCProduceDummyFrames</span></span>

## <a name="data-type"></a><span data-ttu-id="712fc-107">Datentyp</span><span class="sxs-lookup"><span data-stu-id="712fc-107">Data Type</span></span>

<span data-ttu-id="712fc-108">VT \_ bool</span><span class="sxs-lookup"><span data-stu-id="712fc-108">VT\_BOOL</span></span>

## <a name="default-value"></a><span data-ttu-id="712fc-109">Standardwert</span><span class="sxs-lookup"><span data-stu-id="712fc-109">Default Value</span></span>

<span data-ttu-id="712fc-110">Variant \_ false</span><span class="sxs-lookup"><span data-stu-id="712fc-110">VARIANT\_FALSE</span></span>

## <a name="remarks"></a><span data-ttu-id="712fc-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="712fc-111">Remarks</span></span>

<span data-ttu-id="712fc-112">Wenn dieser Wert Variant \_ false ist, werden vom Codec keine Daten für doppelte Frames im Bitdaten Strom abgelegt.</span><span class="sxs-lookup"><span data-stu-id="712fc-112">If this value is VARIANT\_FALSE, the codec will not put any data in the bit stream for duplicate frames.</span></span>

<span data-ttu-id="712fc-113">Pseudo Rahmen können für Anwendungen wichtig sein, bei denen Frame Nummern persistent sind.</span><span class="sxs-lookup"><span data-stu-id="712fc-113">Dummy frames can be important in applications where frame numbers are persisted.</span></span> <span data-ttu-id="712fc-114">Ein gängiges Beispiel ist die Beibehaltung von SMPTE-Zeit Codes für codierten Inhalt.</span><span class="sxs-lookup"><span data-stu-id="712fc-114">A common example is when SMPTE time codes are maintained for encoded content.</span></span>

## <a name="requirements"></a><span data-ttu-id="712fc-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="712fc-115">Requirements</span></span>



| <span data-ttu-id="712fc-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="712fc-116">Requirement</span></span> | <span data-ttu-id="712fc-117">Wert</span><span class="sxs-lookup"><span data-stu-id="712fc-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="712fc-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="712fc-118">Minimum supported client</span></span><br/> | <span data-ttu-id="712fc-119">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="712fc-119">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="712fc-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="712fc-120">Minimum supported server</span></span><br/> | <span data-ttu-id="712fc-121">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="712fc-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="712fc-122">Header</span><span class="sxs-lookup"><span data-stu-id="712fc-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="712fc-123"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="712fc-123"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="712fc-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="712fc-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="712fc-125">Eigenschaften von Media Foundation</span><span class="sxs-lookup"><span data-stu-id="712fc-125">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




