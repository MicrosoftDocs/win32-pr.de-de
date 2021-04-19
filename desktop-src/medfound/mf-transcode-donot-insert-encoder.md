---
description: Gibt an, ob ein Encoder in der transcodieren-Topologie enthalten sein muss.
ms.assetid: 73f23aed-d1b9-4821-b1ca-0a07f02b6913
title: MF_TRANSCODE_DONOT_INSERT_ENCODER-Attribut (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 92d3f8fc5dabfd3e4c55c6242ba9b8f52b6f5c2b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348234"
---
# <a name="mf_transcode_donot_insert_encoder-attribute"></a><span data-ttu-id="ab043-103">MF- \_ transcode- \_ Attribut zum Einfügen von \_ \_ Encodern</span><span class="sxs-lookup"><span data-stu-id="ab043-103">MF\_TRANSCODE\_DONOT\_INSERT\_ENCODER attribute</span></span>

<span data-ttu-id="ab043-104">Gibt an, ob ein Encoder in der transcodieren-Topologie enthalten sein muss.</span><span class="sxs-lookup"><span data-stu-id="ab043-104">Specifies whether an encoder must be included in the transcode topology.</span></span>

<span data-ttu-id="ab043-105">Die [**MF-atetranscodetopology**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetranscodetopology) -Funktion überprüft dieses Attribut beim Aufbau der Topologie.</span><span class="sxs-lookup"><span data-stu-id="ab043-105">The [**MFCreateTranscodeTopology**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetranscodetopology) function checks this attribute during topology building.</span></span> <span data-ttu-id="ab043-106">Wenn dieses Attribut nicht festgelegt ist, wird ein Encoder in die transcodieren-Topologie eingefügt.</span><span class="sxs-lookup"><span data-stu-id="ab043-106">If this attribute is not set, an encoder is inserted in the transcode topology.</span></span>

## <a name="data-type"></a><span data-ttu-id="ab043-107">Datentyp</span><span class="sxs-lookup"><span data-stu-id="ab043-107">Data type</span></span>

<span data-ttu-id="ab043-108">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="ab043-108">**UINT32**</span></span>



| <span data-ttu-id="ab043-109">Wert</span><span class="sxs-lookup"><span data-stu-id="ab043-109">Value</span></span>                                                                        | <span data-ttu-id="ab043-110">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="ab043-110">Meaning</span></span>                                                                                                           |
|------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="ab043-111"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="ab043-111"><dt>0</dt></span></span> </dl> | <span data-ttu-id="ab043-112">Ein Encoder wird in die transcodieren-Topologie eingefügt.</span><span class="sxs-lookup"><span data-stu-id="ab043-112">An encoder is inserted in the transcode topology.</span></span><br/>                                                      |
| <dl> <span data-ttu-id="ab043-113"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="ab043-113"><dt>1</dt></span></span> </dl> | <span data-ttu-id="ab043-114">Ein Encoder ist nicht in der transcodieren-Topologie enthalten.</span><span class="sxs-lookup"><span data-stu-id="ab043-114">An encoder is not included in the transcode topology.</span></span> <span data-ttu-id="ab043-115">Der Quellknoten ist mit dem Ausgabe Knoten verbunden.</span><span class="sxs-lookup"><span data-stu-id="ab043-115">The source node is connected to the output node.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="ab043-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ab043-116">Remarks</span></span>

<span data-ttu-id="ab043-117">Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.</span><span class="sxs-lookup"><span data-stu-id="ab043-117">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="ab043-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ab043-118">Requirements</span></span>



| <span data-ttu-id="ab043-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ab043-119">Requirement</span></span> | <span data-ttu-id="ab043-120">Wert</span><span class="sxs-lookup"><span data-stu-id="ab043-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="ab043-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ab043-121">Minimum supported client</span></span><br/> | <span data-ttu-id="ab043-122">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ab043-122">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="ab043-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ab043-123">Minimum supported server</span></span><br/> | <span data-ttu-id="ab043-124">Nur Windows Server 2008 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ab043-124">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="ab043-125">Header</span><span class="sxs-lookup"><span data-stu-id="ab043-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="ab043-126"><dt>Mspdl. h</dt></span><span class="sxs-lookup"><span data-stu-id="ab043-126"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ab043-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ab043-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ab043-128">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="ab043-128">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="ab043-129">Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="ab043-129">Media Foundation Attributes</span></span>](media-foundation-attributes.md)
</dt> </dl>

 

 




