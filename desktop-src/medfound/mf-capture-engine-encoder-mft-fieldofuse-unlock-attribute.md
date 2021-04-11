---
description: Ermöglicht der Erfassungs-Engine die Verwendung eines Encoders mit Einschränkungen für das Feld.
ms.assetid: 28421875-9629-4F14-8159-2D86012F517F
title: MF_CAPTURE_ENGINE_ENCODER_MFT_FIELDOFUSE_UNLOCK_Attribute-Attribut (MF. Engine. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b29a9466162ff5551ee155343800d938276823ff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215156"
---
# <a name="mf_capture_engine_encoder_mft_fieldofuse_unlock_attribute-attribute"></a><span data-ttu-id="10fbd-103">MF- \_ Erfassungs- \_ Engine- \_ Encoder \_ MFT \_ fieldofuse \_ Unlock Attribute- \_ Attribut</span><span class="sxs-lookup"><span data-stu-id="10fbd-103">MF\_CAPTURE\_ENGINE\_ENCODER\_MFT\_FIELDOFUSE\_UNLOCK\_Attribute attribute</span></span>

<span data-ttu-id="10fbd-104">Ermöglicht der Erfassungs-Engine die Verwendung eines Encoders mit Einschränkungen für das Feld.</span><span class="sxs-lookup"><span data-stu-id="10fbd-104">Enables the capture engine to use an encoder that has field-of-use restrictions.</span></span>

## <a name="data-type"></a><span data-ttu-id="10fbd-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="10fbd-105">Data type</span></span>

<span data-ttu-id="10fbd-106">\**IUnknown \** _</span><span class="sxs-lookup"><span data-stu-id="10fbd-106">\**IUnknown\** _</span></span>

## <a name="remarks"></a><span data-ttu-id="10fbd-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="10fbd-107">Remarks</span></span>

<span data-ttu-id="10fbd-108">Der Wert dieses Attributs ist ein Zeiger auf die [_ *imffieldofusemftunlock* \*](/windows/desktop/api/mfidl/nn-mfidl-imffieldofusemftunlock) -Schnittstelle, die vom Aufrufer implementiert wird.</span><span class="sxs-lookup"><span data-stu-id="10fbd-108">The value of this attribute is a pointer to the [_ *IMFFieldOfUseMFTUnlock*\*](/windows/desktop/api/mfidl/nn-mfidl-imffieldofusemftunlock) interface, implemented by the caller.</span></span> <span data-ttu-id="10fbd-109">Es wird erwartet, dass die Implementierung dieser Schnittstelle des Aufrufers einen Hand Shake mit dem Encoder durchführt, wie im [Feld Use Restrictions](field-of-use-restrictions.md)beschrieben.</span><span class="sxs-lookup"><span data-stu-id="10fbd-109">The caller's implementation of this interface is expected to perform a handshake with the encoder, as described in [Field of Use Restrictions](field-of-use-restrictions.md).</span></span> <span data-ttu-id="10fbd-110">Microsoft Media Foundation definiert nicht den Handshake – in der Regel würde es sich um eine Art kryptografieaustausch handeln.</span><span class="sxs-lookup"><span data-stu-id="10fbd-110">Microsoft Media Foundation does not define the handshake—typically, it would involve some sort of cryptographic exchange.</span></span>

<span data-ttu-id="10fbd-111">Intern legt die Aufzeichnungs-Engine den [**imffieldofusemftunlock**](/windows/desktop/api/mfidl/nn-mfidl-imffieldofusemftunlock) -Zeiger auf den Encoder fest, indem er das [MFT \_ fieldofuse \_ Unlock \_ Attribute](mft-fieldofuse-unlock-attribute.md) -Attribut des Encoders festlegt.</span><span class="sxs-lookup"><span data-stu-id="10fbd-111">Internally, the capture engine sets the [**IMFFieldOfUseMFTUnlock**](/windows/desktop/api/mfidl/nn-mfidl-imffieldofusemftunlock) pointer on the encoder by setting the encoder's [MFT\_FIELDOFUSE\_UNLOCK\_Attribute](mft-fieldofuse-unlock-attribute.md) attribute.</span></span>

## <a name="requirements"></a><span data-ttu-id="10fbd-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="10fbd-112">Requirements</span></span>



| <span data-ttu-id="10fbd-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="10fbd-113">Requirement</span></span> | <span data-ttu-id="10fbd-114">Wert</span><span class="sxs-lookup"><span data-stu-id="10fbd-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="10fbd-115">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="10fbd-115">Minimum supported client</span></span><br/> | <span data-ttu-id="10fbd-116">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="10fbd-116">Windows 8 \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="10fbd-117">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="10fbd-117">Minimum supported server</span></span><br/> | <span data-ttu-id="10fbd-118">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="10fbd-118">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="10fbd-119">Header</span><span class="sxs-lookup"><span data-stu-id="10fbd-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="10fbd-120"><dt>"MF"-Engine. h</dt></span><span class="sxs-lookup"><span data-stu-id="10fbd-120"><dt>Mfcaptureengine.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="10fbd-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="10fbd-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="10fbd-122">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="10fbd-122">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="10fbd-123">Attribute der Aufzeichnungs-Engine</span><span class="sxs-lookup"><span data-stu-id="10fbd-123">Capture Engine Attributes</span></span>](capture-engine-attributes.md)
</dt> <dt>

[<span data-ttu-id="10fbd-124">**IMF captureengine:: Initialize**</span><span class="sxs-lookup"><span data-stu-id="10fbd-124">**IMFCaptureEngine::Initialize**</span></span>](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengine-initialize)
</dt> </dl>

 

 




