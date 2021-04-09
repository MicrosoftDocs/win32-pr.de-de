---
description: Gibt die Konfigurationseinstellung für den standardproxylocator an.
ms.assetid: 85f2bd02-8a2f-46b5-b765-1a0bc5b6ccc3
title: MFNETSOURCE_PROXYSETTINGS-Eigenschaft (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f1330773ab33674e58ef07b95a53c4493e6e6f6e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130709"
---
# <a name="mfnetsource_proxysettings-property"></a><span data-ttu-id="77e67-103">MF NetSource- \_ proxysettings-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="77e67-103">MFNETSOURCE\_PROXYSETTINGS property</span></span>

<span data-ttu-id="77e67-104">Gibt die Konfigurationseinstellung für den standardproxylocator an.</span><span class="sxs-lookup"><span data-stu-id="77e67-104">Specifies the configuration setting for the default proxy locator.</span></span> <span data-ttu-id="77e67-105">Der Wert dieser Eigenschaft ist ein Member der [**mfnet \_ proxysettings**](/windows/desktop/api/mfidl/ne-mfidl-mfnet_proxysettings) -Enumeration.</span><span class="sxs-lookup"><span data-stu-id="77e67-105">The value of this property is a member of the [**MFNET\_PROXYSETTINGS**](/windows/desktop/api/mfidl/ne-mfidl-mfnet_proxysettings) enumeration.</span></span>



<span data-ttu-id="77e67-106">Datentyp</span><span class="sxs-lookup"><span data-stu-id="77e67-106">Data type</span></span>

<span data-ttu-id="77e67-107">PROPVARIANT-Typ (VT)</span><span class="sxs-lookup"><span data-stu-id="77e67-107">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="77e67-108">PROPVARIANT-Member</span><span class="sxs-lookup"><span data-stu-id="77e67-108">PROPVARIANT member</span></span>

<span data-ttu-id="77e67-109">**LONG**</span><span class="sxs-lookup"><span data-stu-id="77e67-109">**LONG**</span></span>

<span data-ttu-id="77e67-110">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="77e67-110">VT\_I4</span></span>

<span data-ttu-id="77e67-111">**LVAL**</span><span class="sxs-lookup"><span data-stu-id="77e67-111">**lVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="77e67-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="77e67-112">Remarks</span></span>

<span data-ttu-id="77e67-113">Die Konstante " **MF NetSource"- \_ Proxy Settings** definiert die GUID für diesen Eigenschafts Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="77e67-113">The constant **MFNETSOURCE\_PROXYSETTINGS** defines the GUID for this property key.</span></span> <span data-ttu-id="77e67-114">Der Eigenschaften Bezeichner (PID) ist 0 (null).</span><span class="sxs-lookup"><span data-stu-id="77e67-114">The property identifier (PID) is zero.</span></span>

<span data-ttu-id="77e67-115">Anwendungen können diese Eigenschaft verwenden, um den proxylocator bei der Erstellung des standardproxylocator-Objekts zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="77e67-115">Applications can use this property to configure the proxy locator when creating the default proxy locator object.</span></span> <span data-ttu-id="77e67-116">Um die-Eigenschaft festzulegen, übergeben Sie einen **IPropertyStore** -Zeiger im *pproxyconfig* -Parameter der [**mfkreateproxylocator**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateproxylocator) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="77e67-116">To set the property, pass an **IPropertyStore** pointer in the *pProxyConfig* parameter of the [**MFCreateProxyLocator**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateproxylocator) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="77e67-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="77e67-117">Requirements</span></span>



| <span data-ttu-id="77e67-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="77e67-118">Requirement</span></span> | <span data-ttu-id="77e67-119">Wert</span><span class="sxs-lookup"><span data-stu-id="77e67-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="77e67-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="77e67-120">Minimum supported client</span></span><br/> | <span data-ttu-id="77e67-121">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="77e67-121">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="77e67-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="77e67-122">Minimum supported server</span></span><br/> | <span data-ttu-id="77e67-123">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="77e67-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="77e67-124">Header</span><span class="sxs-lookup"><span data-stu-id="77e67-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="77e67-125"><dt>Mspdl. h</dt></span><span class="sxs-lookup"><span data-stu-id="77e67-125"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="77e67-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="77e67-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="77e67-127">Eigenschaften von Media Foundation</span><span class="sxs-lookup"><span data-stu-id="77e67-127">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="77e67-128">Netzwerk in Media Foundation</span><span class="sxs-lookup"><span data-stu-id="77e67-128">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> <dt>

[<span data-ttu-id="77e67-129">Proxy Unterstützung für Netzwerk Quellen</span><span class="sxs-lookup"><span data-stu-id="77e67-129">Proxy Support for Network Sources</span></span>](proxy-support-for-network-sources.md)
</dt> </dl>

 

 




