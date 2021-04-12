---
description: Gibt an, ob der standardproxylocator die automatische Proxy Erkennung erzwingen soll.
ms.assetid: ab547a92-94a2-482e-b7ac-aeb3fdfb6b91
title: MFNETSOURCE_PROXYRERUNAUTODETECTION-Eigenschaft (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 37021c7e96b135389f0dffa2f8c26b8067df2b7a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528226"
---
# <a name="mfnetsource_proxyrerunautodetection-property"></a><span data-ttu-id="041fc-103">MF-Quelle \_ proxyrerunautoerkennungs (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="041fc-103">MFNETSOURCE\_PROXYRERUNAUTODETECTION property</span></span>

<span data-ttu-id="041fc-104">Gibt an, ob der standardproxylocator die automatische Proxy Erkennung erzwingen soll.</span><span class="sxs-lookup"><span data-stu-id="041fc-104">Specifies whether the default proxy locator should force proxy auto-detection.</span></span>



<span data-ttu-id="041fc-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="041fc-105">Data type</span></span>

<span data-ttu-id="041fc-106">PROPVARIANT-Typ (VT)</span><span class="sxs-lookup"><span data-stu-id="041fc-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="041fc-107">PROPVARIANT-Member</span><span class="sxs-lookup"><span data-stu-id="041fc-107">PROPVARIANT member</span></span>

<span data-ttu-id="041fc-108">Boolescher Wert (**Long**)</span><span class="sxs-lookup"><span data-stu-id="041fc-108">Boolean (**LONG**)</span></span>

<span data-ttu-id="041fc-109">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="041fc-109">VT\_I4</span></span>

<span data-ttu-id="041fc-110">**LVAL**</span><span class="sxs-lookup"><span data-stu-id="041fc-110">**lVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="041fc-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="041fc-111">Remarks</span></span>

<span data-ttu-id="041fc-112">Die Konstante " **MF NetSource"- \_ Proxy Settings** definiert die GUID für diesen Eigenschafts Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="041fc-112">The constant **MFNETSOURCE\_PROXYSETTINGS** defines the GUID for this property key.</span></span> <span data-ttu-id="041fc-113">Der Eigenschaften Bezeichner (PID) ist 0 (null).</span><span class="sxs-lookup"><span data-stu-id="041fc-113">The property identifier (PID) is zero.</span></span>

<span data-ttu-id="041fc-114">Anwendungen können diese Eigenschaft verwenden, um den proxylocator bei der Erstellung des proxylocator-Objekts zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="041fc-114">Applications can use this property to configure the proxy locator when creating the proxy locator object.</span></span> <span data-ttu-id="041fc-115">Um die-Eigenschaft festzulegen, übergeben Sie einen **IPropertyStore** -Zeiger im *pproxyconfig* -Parameter der [**mfkreateproxylocator**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateproxylocator) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="041fc-115">To set the property, pass an **IPropertyStore** pointer in the *pProxyConfig* parameter of the [**MFCreateProxyLocator**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateproxylocator) function.</span></span> <span data-ttu-id="041fc-116">Im Modus für die automatische Erkennung verwendet der proxylocator den Mechanismus zum Erkennen von WinInet-Proxys.</span><span class="sxs-lookup"><span data-stu-id="041fc-116">In auto-detect mode, the proxy locator uses the WinInet proxy detection mechanism.</span></span> <span data-ttu-id="041fc-117">Legen Sie den Wert auf 0 fest, um die automatische Erkennung zu erzwingen.</span><span class="sxs-lookup"><span data-stu-id="041fc-117">To force auto-detection, set the value to 0.</span></span>

## <a name="requirements"></a><span data-ttu-id="041fc-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="041fc-118">Requirements</span></span>



| <span data-ttu-id="041fc-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="041fc-119">Requirement</span></span> | <span data-ttu-id="041fc-120">Wert</span><span class="sxs-lookup"><span data-stu-id="041fc-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="041fc-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="041fc-121">Minimum supported client</span></span><br/> | <span data-ttu-id="041fc-122">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="041fc-122">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="041fc-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="041fc-123">Minimum supported server</span></span><br/> | <span data-ttu-id="041fc-124">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="041fc-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="041fc-125">Header</span><span class="sxs-lookup"><span data-stu-id="041fc-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="041fc-126"><dt>Mspdl. h</dt></span><span class="sxs-lookup"><span data-stu-id="041fc-126"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="041fc-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="041fc-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="041fc-128">Eigenschaften von Media Foundation</span><span class="sxs-lookup"><span data-stu-id="041fc-128">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="041fc-129">Netzwerk in Media Foundation</span><span class="sxs-lookup"><span data-stu-id="041fc-129">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> <dt>

[<span data-ttu-id="041fc-130">Proxy Unterstützung für Netzwerk Quellen</span><span class="sxs-lookup"><span data-stu-id="041fc-130">Proxy Support for Network Sources</span></span>](proxy-support-for-network-sources.md)
</dt> </dl>

 

 




