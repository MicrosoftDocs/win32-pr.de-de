---
description: Ermöglicht zwei Instanzen der Medien Sitzung, den gleichen PMP-Prozess (Protected Media Path) gemeinsam zu nutzen.
ms.assetid: a922c79b-d6c1-447d-b6fa-993970169a3f
title: MF_SESSION_SERVER_CONTEXT-Attribut (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b1ce68d1dcd4318f68c4547845e6ce12d2f3aaca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104131957"
---
# <a name="mf_session_server_context-attribute"></a><span data-ttu-id="9905a-103">Kontext Attribut des MF- \_ Sitzungs \_ Servers \_</span><span class="sxs-lookup"><span data-stu-id="9905a-103">MF\_SESSION\_SERVER\_CONTEXT attribute</span></span>

<span data-ttu-id="9905a-104">Ermöglicht zwei Instanzen der Medien Sitzung, den gleichen PMP-Prozess (Protected Media Path) gemeinsam zu nutzen.</span><span class="sxs-lookup"><span data-stu-id="9905a-104">Enables two instances of the Media Session to share the same Protected Media Path (PMP) process.</span></span>

## <a name="data-type"></a><span data-ttu-id="9905a-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="9905a-105">Data type</span></span>

<span data-ttu-id="9905a-106">\**IUnknown \** _</span><span class="sxs-lookup"><span data-stu-id="9905a-106">\**IUnknown\** _</span></span>

## <a name="remarks"></a><span data-ttu-id="9905a-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9905a-107">Remarks</span></span>

<span data-ttu-id="9905a-108">Verwenden Sie dieses Attribut, wenn Sie die PMP-Medien Sitzung in einem vorhandenen PMP-Prozess erstellen möchten.</span><span class="sxs-lookup"><span data-stu-id="9905a-108">Use this attribute if you want to create the PMP Media Session in an existing PMP process.</span></span> <span data-ttu-id="9905a-109">Der Wert des-Attributs ist ein Zeiger auf die [_ *imfpmpserver* \*](/windows/desktop/api/mfidl/nn-mfidl-imfpmpserver) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="9905a-109">The value of the attribute is a pointer to the [_ *IMFPMPServer*\*](/windows/desktop/api/mfidl/nn-mfidl-imfpmpserver) interface.</span></span>

<span data-ttu-id="9905a-110">Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.</span><span class="sxs-lookup"><span data-stu-id="9905a-110">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="9905a-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9905a-111">Requirements</span></span>



| <span data-ttu-id="9905a-112">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9905a-112">Requirement</span></span> | <span data-ttu-id="9905a-113">Wert</span><span class="sxs-lookup"><span data-stu-id="9905a-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="9905a-114">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9905a-114">Minimum supported client</span></span><br/> | <span data-ttu-id="9905a-115">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9905a-115">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="9905a-116">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9905a-116">Minimum supported server</span></span><br/> | <span data-ttu-id="9905a-117">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9905a-117">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="9905a-118">Header</span><span class="sxs-lookup"><span data-stu-id="9905a-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="9905a-119"><dt>Mspdl. h</dt></span><span class="sxs-lookup"><span data-stu-id="9905a-119"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9905a-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9905a-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9905a-121">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="9905a-121">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="9905a-122">**Imfattributes:: getunknown**</span><span class="sxs-lookup"><span data-stu-id="9905a-122">**IMFAttributes::GetUnknown**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown)
</dt> <dt>

[<span data-ttu-id="9905a-123">\**Imfattributes:: *-Known**</span><span class="sxs-lookup"><span data-stu-id="9905a-123">**IMFAttributes::SetUnknown**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown)
</dt> <dt>

[<span data-ttu-id="9905a-124">Medien Sitzungs Attribute</span><span class="sxs-lookup"><span data-stu-id="9905a-124">Media Session Attributes</span></span>](media-session-attributes.md)
</dt> </dl>

 

 




