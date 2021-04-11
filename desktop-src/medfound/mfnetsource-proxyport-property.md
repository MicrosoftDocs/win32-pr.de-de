---
description: Gibt die Portnummer des Proxy Servers an.
ms.assetid: cd84911b-3658-489f-b454-23eded0cbfa0
title: MFNETSOURCE_PROXYPORT-Eigenschaft (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 228f7d9390d53f7d8182a198879dcb2d81e3bae7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215134"
---
# <a name="mfnetsource_proxyport-property"></a><span data-ttu-id="7e6c7-103">MF NetSource- \_ ProxyPort (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="7e6c7-103">MFNETSOURCE\_PROXYPORT property</span></span>

<span data-ttu-id="7e6c7-104">Gibt die Portnummer des Proxy Servers an.</span><span class="sxs-lookup"><span data-stu-id="7e6c7-104">Specifies the port number of the proxy server.</span></span>



<span data-ttu-id="7e6c7-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="7e6c7-105">Data type</span></span>

<span data-ttu-id="7e6c7-106">PROPVARIANT-Typ (VT)</span><span class="sxs-lookup"><span data-stu-id="7e6c7-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="7e6c7-107">PROPVARIANT-Member</span><span class="sxs-lookup"><span data-stu-id="7e6c7-107">PROPVARIANT member</span></span>

<span data-ttu-id="7e6c7-108">**DWORD** (als **Long** gespeichert)</span><span class="sxs-lookup"><span data-stu-id="7e6c7-108">**DWORD** (stored as **LONG**)</span></span>

<span data-ttu-id="7e6c7-109">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="7e6c7-109">VT\_I4</span></span>

<span data-ttu-id="7e6c7-110">**LVAL**</span><span class="sxs-lookup"><span data-stu-id="7e6c7-110">**lVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="7e6c7-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7e6c7-111">Remarks</span></span>

<span data-ttu-id="7e6c7-112">Die Konstante **MF-Quelle \_ ProxyPort** definiert die GUID für diesen Eigenschafts Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="7e6c7-112">The constant **MFNETSOURCE\_PROXYPORT** defines the GUID for this property key.</span></span> <span data-ttu-id="7e6c7-113">Der Eigenschaften Bezeichner (PID) ist 0 (null).</span><span class="sxs-lookup"><span data-stu-id="7e6c7-113">The property identifier (PID) is zero.</span></span>

<span data-ttu-id="7e6c7-114">Anwendungen können diese Eigenschaft verwenden, um den proxylocator bei der Erstellung des proxylocator-Objekts zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="7e6c7-114">Applications can use this property to configure the proxy locator when creating the proxy locator object.</span></span> <span data-ttu-id="7e6c7-115">Um die-Eigenschaft festzulegen, übergeben Sie einen **IPropertyStore** -Zeiger im *pproxyconfig* -Parameter der [**mfkreateproxylocator**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateproxylocator) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="7e6c7-115">To set the property, pass an **IPropertyStore** pointer in the *pProxyConfig* parameter of the [**MFCreateProxyLocator**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateproxylocator) function.</span></span> <span data-ttu-id="7e6c7-116">Wenn diese Eigenschaft nicht für http festgelegt ist, verwendet der proxylocator standardmäßig den Wert 80.</span><span class="sxs-lookup"><span data-stu-id="7e6c7-116">If this property is not set for HTTP, then by default the proxy locator uses a value of 80.</span></span>

## <a name="requirements"></a><span data-ttu-id="7e6c7-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7e6c7-117">Requirements</span></span>



| <span data-ttu-id="7e6c7-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7e6c7-118">Requirement</span></span> | <span data-ttu-id="7e6c7-119">Wert</span><span class="sxs-lookup"><span data-stu-id="7e6c7-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="7e6c7-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7e6c7-120">Minimum supported client</span></span><br/> | <span data-ttu-id="7e6c7-121">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7e6c7-121">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="7e6c7-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7e6c7-122">Minimum supported server</span></span><br/> | <span data-ttu-id="7e6c7-123">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7e6c7-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="7e6c7-124">Header</span><span class="sxs-lookup"><span data-stu-id="7e6c7-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="7e6c7-125"><dt>Mspdl. h</dt></span><span class="sxs-lookup"><span data-stu-id="7e6c7-125"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7e6c7-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7e6c7-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7e6c7-127">Eigenschaften von Media Foundation</span><span class="sxs-lookup"><span data-stu-id="7e6c7-127">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="7e6c7-128">Netzwerk in Media Foundation</span><span class="sxs-lookup"><span data-stu-id="7e6c7-128">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> <dt>

[<span data-ttu-id="7e6c7-129">Proxy Unterstützung für Netzwerk Quellen</span><span class="sxs-lookup"><span data-stu-id="7e6c7-129">Proxy Support for Network Sources</span></span>](proxy-support-for-network-sources.md)
</dt> </dl>

 

 




