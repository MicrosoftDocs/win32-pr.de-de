---
description: Enthält einen Zeiger auf die imfnetkredentialmanager-Schnittstelle.
ms.assetid: c0826956-9df1-40ec-8ad1-9e0dca34d847
title: MFNETSOURCE_CREDENTIAL_MANAGER-Eigenschaft (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3447369cedfa5c516e1d7696aae70834c6ce89a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130116"
---
# <a name="mfnetsource_credential_manager-property"></a><span data-ttu-id="28b2e-103">MF-Quelle \_ Credential \_ Manager (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="28b2e-103">MFNETSOURCE\_CREDENTIAL\_MANAGER property</span></span>

<span data-ttu-id="28b2e-104">Enthält einen Zeiger auf die [**imfnetkredentialmanager**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredentialmanager) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="28b2e-104">Contains a pointer to the [**IMFNetCredentialManager**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredentialmanager) interface.</span></span> <span data-ttu-id="28b2e-105">Verwenden Sie diese Eigenschaft, um die Implementierung von [**imfnetkredentialmanager**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredentialmanager) der Anwendung an die Netzwerkquelle zu übergeben.</span><span class="sxs-lookup"><span data-stu-id="28b2e-105">Use this property to pass the application's implementation of [**IMFNetCredentialManager**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredentialmanager) to the network source.</span></span>



<span data-ttu-id="28b2e-106">Datentyp</span><span class="sxs-lookup"><span data-stu-id="28b2e-106">Data type</span></span>

<span data-ttu-id="28b2e-107">PROPVARIANT-Typ (VT)</span><span class="sxs-lookup"><span data-stu-id="28b2e-107">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="28b2e-108">PROPVARIANT-Member</span><span class="sxs-lookup"><span data-stu-id="28b2e-108">PROPVARIANT member</span></span>

<span data-ttu-id="28b2e-109">**IUnknown** -Zeiger</span><span class="sxs-lookup"><span data-stu-id="28b2e-109">**IUnknown** pointer</span></span>

<span data-ttu-id="28b2e-110">VT \_ unbekannt</span><span class="sxs-lookup"><span data-stu-id="28b2e-110">VT\_UNKNOWN</span></span>

<span data-ttu-id="28b2e-111">**punkVal**</span><span class="sxs-lookup"><span data-stu-id="28b2e-111">**punkVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="28b2e-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="28b2e-112">Remarks</span></span>

<span data-ttu-id="28b2e-113">Der Konstante **MF-Quell Anmelde Informations \_ \_ Manager** definiert die **GUID** für den Eigenschafts Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="28b2e-113">The constant **MFNETSOURCE\_CREDENTIAL\_MANAGER** defines the **GUID** for the property key.</span></span> <span data-ttu-id="28b2e-114">Der Eigenschaften Bezeichner (PID) ist 0 (null).</span><span class="sxs-lookup"><span data-stu-id="28b2e-114">The property identifier (PID) is zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="28b2e-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="28b2e-115">Requirements</span></span>



| <span data-ttu-id="28b2e-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="28b2e-116">Requirement</span></span> | <span data-ttu-id="28b2e-117">Wert</span><span class="sxs-lookup"><span data-stu-id="28b2e-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="28b2e-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="28b2e-118">Minimum supported client</span></span><br/> | <span data-ttu-id="28b2e-119">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="28b2e-119">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="28b2e-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="28b2e-120">Minimum supported server</span></span><br/> | <span data-ttu-id="28b2e-121">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="28b2e-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="28b2e-122">Header</span><span class="sxs-lookup"><span data-stu-id="28b2e-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="28b2e-123"><dt>Mspdl. h</dt></span><span class="sxs-lookup"><span data-stu-id="28b2e-123"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="28b2e-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="28b2e-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="28b2e-125">Eigenschaften von Media Foundation</span><span class="sxs-lookup"><span data-stu-id="28b2e-125">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="28b2e-126">Netzwerk Quellen Authentifizierung</span><span class="sxs-lookup"><span data-stu-id="28b2e-126">Network Source Authentication</span></span>](network-source-authentication.md)
</dt> <dt>

[<span data-ttu-id="28b2e-127">Netzwerk in Media Foundation</span><span class="sxs-lookup"><span data-stu-id="28b2e-127">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> </dl>

 

 




