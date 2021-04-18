---
description: Ermöglicht der Erfassungs-Engine die Verwendung eines Decoders mit Einschränkungen für das Feld.
ms.assetid: EDE6D207-FD84-4DEB-9BF5-0952C454B00F
title: MF_CAPTURE_ENGINE_DECODER_MFT_FIELDOFUSE_UNLOCK_Attribute-Attribut (MF. Engine. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d858d4382b669621f6dc43cbfee77b62e9d1124
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347056"
---
# <a name="mf_capture_engine_decoder_mft_fieldofuse_unlock_attribute-attribute"></a><span data-ttu-id="6c7cd-103">MF- \_ Erfassungs- \_ Engine- \_ Decoder \_ MFT \_ fieldofuse \_ Unlock \_ Attribute-Attribut</span><span class="sxs-lookup"><span data-stu-id="6c7cd-103">MF\_CAPTURE\_ENGINE\_DECODER\_MFT\_FIELDOFUSE\_UNLOCK\_Attribute attribute</span></span>

<span data-ttu-id="6c7cd-104">Ermöglicht der Erfassungs-Engine die Verwendung eines Decoders mit Einschränkungen für das Feld.</span><span class="sxs-lookup"><span data-stu-id="6c7cd-104">Enables the capture engine to use a decoder that has field-of-use restrictions.</span></span>

## <a name="data-type"></a><span data-ttu-id="6c7cd-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="6c7cd-105">Data type</span></span>

<span data-ttu-id="6c7cd-106">\**IUnknown \** _</span><span class="sxs-lookup"><span data-stu-id="6c7cd-106">\**IUnknown\** _</span></span>

## <a name="remarks"></a><span data-ttu-id="6c7cd-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6c7cd-107">Remarks</span></span>

<span data-ttu-id="6c7cd-108">Der Wert dieses Attributs ist ein Zeiger auf die [_ *imffieldofusemftunlock* \*](/windows/desktop/api/mfidl/nn-mfidl-imffieldofusemftunlock) -Schnittstelle, die vom Aufrufer implementiert wird.</span><span class="sxs-lookup"><span data-stu-id="6c7cd-108">The value of this attribute is a pointer to the [_ *IMFFieldOfUseMFTUnlock*\*](/windows/desktop/api/mfidl/nn-mfidl-imffieldofusemftunlock) interface, implemented by the caller.</span></span> <span data-ttu-id="6c7cd-109">Es wird erwartet, dass die Implementierung dieser Schnittstelle des Aufrufers einen Hand Shake mit dem Decoder durchführt, wie im [Feld Use Restrictions](field-of-use-restrictions.md)beschrieben.</span><span class="sxs-lookup"><span data-stu-id="6c7cd-109">The caller's implementation of this interface is expected to perform a handshake with the decoder, as described in [Field of Use Restrictions](field-of-use-restrictions.md).</span></span> <span data-ttu-id="6c7cd-110">Microsoft Media Foundation definiert nicht den Handshake – in der Regel würde es sich um eine Art kryptografieaustausch handeln.</span><span class="sxs-lookup"><span data-stu-id="6c7cd-110">Microsoft Media Foundation does not define the handshake—typically, it would involve some sort of cryptographic exchange.</span></span>

<span data-ttu-id="6c7cd-111">Intern legt die Aufzeichnungs-Engine den [**imffieldofusemftunlock**](/windows/desktop/api/mfidl/nn-mfidl-imffieldofusemftunlock) -Zeiger auf den Decoder fest, indem er das [MFT \_ fieldofuse \_ Unlock \_ Attribute](mft-fieldofuse-unlock-attribute.md) -Attribut des Decoders festlegt.</span><span class="sxs-lookup"><span data-stu-id="6c7cd-111">Internally, the capture engine sets the [**IMFFieldOfUseMFTUnlock**](/windows/desktop/api/mfidl/nn-mfidl-imffieldofusemftunlock) pointer on the decoder by setting the decoder's [MFT\_FIELDOFUSE\_UNLOCK\_Attribute](mft-fieldofuse-unlock-attribute.md) attribute.</span></span>

## <a name="requirements"></a><span data-ttu-id="6c7cd-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6c7cd-112">Requirements</span></span>



| <span data-ttu-id="6c7cd-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6c7cd-113">Requirement</span></span> | <span data-ttu-id="6c7cd-114">Wert</span><span class="sxs-lookup"><span data-stu-id="6c7cd-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="6c7cd-115">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6c7cd-115">Minimum supported client</span></span><br/> | <span data-ttu-id="6c7cd-116">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6c7cd-116">Windows 8 \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="6c7cd-117">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6c7cd-117">Minimum supported server</span></span><br/> | <span data-ttu-id="6c7cd-118">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6c7cd-118">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="6c7cd-119">Header</span><span class="sxs-lookup"><span data-stu-id="6c7cd-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="6c7cd-120"><dt>"MF"-Engine. h</dt></span><span class="sxs-lookup"><span data-stu-id="6c7cd-120"><dt>Mfcaptureengine.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6c7cd-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6c7cd-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6c7cd-122">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="6c7cd-122">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="6c7cd-123">Attribute der Aufzeichnungs-Engine</span><span class="sxs-lookup"><span data-stu-id="6c7cd-123">Capture Engine Attributes</span></span>](capture-engine-attributes.md)
</dt> <dt>

[<span data-ttu-id="6c7cd-124">**IMF captureengine:: Initialize**</span><span class="sxs-lookup"><span data-stu-id="6c7cd-124">**IMFCaptureEngine::Initialize**</span></span>](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengine-initialize)
</dt> </dl>

 

 




