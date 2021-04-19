---
description: Gibt an, ob in der Topologie hardwarebasierte Microsoft Media Foundation Transformationen (MFTs) geladen werden sollen.
ms.assetid: f7ac3c9b-c163-412f-84c0-27bf551091d8
title: MF_TOPOLOGY_HARDWARE_MODE-Attribut (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec7933e9a380bbf5e66f4030a214f3f4aa93abc7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346875"
---
# <a name="mf_topology_hardware_mode-attribute"></a><span data-ttu-id="4fe0e-103">MF- \_ topologieattribut für \_ Hardware \_ Modus</span><span class="sxs-lookup"><span data-stu-id="4fe0e-103">MF\_TOPOLOGY\_HARDWARE\_MODE attribute</span></span>

<span data-ttu-id="4fe0e-104">Gibt an, ob in der Topologie hardwarebasierte Microsoft Media Foundation Transformationen (MFTs) geladen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="4fe0e-104">Specifies whether to load hardware-based Microsoft Media Foundation transforms (MFTs) in the topology.</span></span>

## <a name="data-type"></a><span data-ttu-id="4fe0e-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="4fe0e-105">Data type</span></span>

<span data-ttu-id="4fe0e-106">**[**Mftopology \_ Als \_**](/windows/desktop/api/mfidl/ne-mfidl-mftopology_hardware_mode)** **UInt32** gespeicherter Hardware Modus</span><span class="sxs-lookup"><span data-stu-id="4fe0e-106">**[**MFTOPOLOGY\_HARDWARE\_MODE**](/windows/desktop/api/mfidl/ne-mfidl-mftopology_hardware_mode)** stored as **UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="4fe0e-107">Abrufen/Festlegen</span><span class="sxs-lookup"><span data-stu-id="4fe0e-107">Get/set</span></span>

<span data-ttu-id="4fe0e-108">Um dieses Attribut abzurufen, nennen Sie [**imfattributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="4fe0e-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="4fe0e-109">Um dieses Attribut festzulegen, nennen Sie [**imfattributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="4fe0e-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="applies-to"></a><span data-ttu-id="4fe0e-110">Gilt für:</span><span class="sxs-lookup"><span data-stu-id="4fe0e-110">Applies to</span></span>

[<span data-ttu-id="4fe0e-111">**Imftopology**</span><span class="sxs-lookup"><span data-stu-id="4fe0e-111">**IMFTopology**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopology)

## <a name="remarks"></a><span data-ttu-id="4fe0e-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4fe0e-112">Remarks</span></span>

<span data-ttu-id="4fe0e-113">Dieses Attribut ist optional.</span><span class="sxs-lookup"><span data-stu-id="4fe0e-113">This attribute is optional.</span></span> <span data-ttu-id="4fe0e-114">Legen Sie das-Attribut fest, bevor Sie die Topologie auflösen.</span><span class="sxs-lookup"><span data-stu-id="4fe0e-114">Set the attribute before resolving the topology.</span></span>



| <span data-ttu-id="4fe0e-115">Wert</span><span class="sxs-lookup"><span data-stu-id="4fe0e-115">Value</span></span>                                  | <span data-ttu-id="4fe0e-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4fe0e-116">Description</span></span>                                                                                                                                                                                                                                                                       |
|----------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4fe0e-117">**mftopology \_ hwmode \_ \_ Hardware verwenden**</span><span class="sxs-lookup"><span data-stu-id="4fe0e-117">**MFTOPOLOGY\_HWMODE\_USE\_HARDWARE**</span></span>  | <span data-ttu-id="4fe0e-118">Das topologielader lädt hardwarebasierte MFTs (z. b. Hardware Decoder), wenn diese verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="4fe0e-118">The Topology Loader will load hardware-based MFTs, such as hardware decoders, when available.</span></span><br/> <span data-ttu-id="4fe0e-119">Das topologielader greift automatisch auf Software Decodierung zurück, wenn kein Hardware Decoder gefunden wird oder wenn ein Hardware Decoder aus irgendeinem Grund keine Verbindung herstellen kann.</span><span class="sxs-lookup"><span data-stu-id="4fe0e-119">The Topology Loader automatically falls back to software decoding if no hardware decoder is found, or if a hardware decoder fails to connect for some reason.</span></span><br/> |
| <span data-ttu-id="4fe0e-120">**nur mftopology \_ hwmode- \_ Software \_**</span><span class="sxs-lookup"><span data-stu-id="4fe0e-120">**MFTOPOLOGY\_HWMODE\_SOFTWARE\_ONLY**</span></span> | <span data-ttu-id="4fe0e-121">Das topologielader lädt nur Software-MFTs, einschließlich Software Decoder.</span><span class="sxs-lookup"><span data-stu-id="4fe0e-121">The Topology Loader will load only software MFTs, including software decoders.</span></span>                                                                                                                                                                                                    |



 

<span data-ttu-id="4fe0e-122">Der Standardwert ist **nur mftopology \_ hwmode- \_ Software \_**, um Kompatibilität mit vorhandenen Anwendungen zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="4fe0e-122">The default value is **MFTOPOLOGY\_HWMODE\_SOFTWARE\_ONLY**, for compatibility with existing applications.</span></span> <span data-ttu-id="4fe0e-123">Der empfohlene Wert ist **mftopology \_ hwmode \_ use \_ Hardware**.</span><span class="sxs-lookup"><span data-stu-id="4fe0e-123">The recommended value is **MFTOPOLOGY\_HWMODE\_USE\_HARDWARE**.</span></span>

<span data-ttu-id="4fe0e-124">Wenn das topologielader eine Hardware-MFT in die Topologie einfügt, wird das Attribut Attribut der [MFT- \_ Enum- \_ Hardware- \_ \_ URL](mft-enum-hardware-url-attribute.md) für den topologieknoten festgelegt.</span><span class="sxs-lookup"><span data-stu-id="4fe0e-124">If the Topology Loader inserts a hardware MFT into the topology, it sets the [MFT\_ENUM\_HARDWARE\_URL\_Attribute](mft-enum-hardware-url-attribute.md) attribute on the topology node.</span></span> <span data-ttu-id="4fe0e-125">Um zu überprüfen, ob eine Hardware-MFT vorhanden ist, müssen Sie die Knoten in der aufgelösten Topologie auflisten und überprüfen, ob dieses Attribut vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="4fe0e-125">To check whether a hardware MFT is present, enumerate the nodes in the resolved topology and check whether this attribute is present.</span></span>

<span data-ttu-id="4fe0e-126">Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.</span><span class="sxs-lookup"><span data-stu-id="4fe0e-126">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="4fe0e-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4fe0e-127">Requirements</span></span>



| <span data-ttu-id="4fe0e-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4fe0e-128">Requirement</span></span> | <span data-ttu-id="4fe0e-129">Wert</span><span class="sxs-lookup"><span data-stu-id="4fe0e-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="4fe0e-130">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="4fe0e-130">Minimum supported client</span></span><br/> | <span data-ttu-id="4fe0e-131">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4fe0e-131">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="4fe0e-132">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="4fe0e-132">Minimum supported server</span></span><br/> | <span data-ttu-id="4fe0e-133">Nur Windows Server 2008 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4fe0e-133">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="4fe0e-134">Header</span><span class="sxs-lookup"><span data-stu-id="4fe0e-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="4fe0e-135"><dt>Mspdl. h</dt></span><span class="sxs-lookup"><span data-stu-id="4fe0e-135"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4fe0e-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4fe0e-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4fe0e-137">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="4fe0e-137">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="4fe0e-138">Topologieattribute</span><span class="sxs-lookup"><span data-stu-id="4fe0e-138">Topology Attributes</span></span>](topology-attributes.md)
</dt> </dl>

 

 




