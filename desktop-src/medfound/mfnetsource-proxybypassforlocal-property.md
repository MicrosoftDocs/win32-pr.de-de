---
description: Gibt an, ob der proxylocator einen Proxy Server für lokale Adressen verwenden soll.
ms.assetid: 384343f5-5919-44da-b8ea-0c994b4743a8
title: MFNETSOURCE_PROXYBYPASSFORLOCAL-Eigenschaft (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9476571ddd593b7930be1aa4376a836de3d75206
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103749193"
---
# <a name="mfnetsource_proxybypassforlocal-property"></a><span data-ttu-id="03a5c-103">MF-Quelle \_ proxybypassforlocal (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="03a5c-103">MFNETSOURCE\_PROXYBYPASSFORLOCAL property</span></span>

<span data-ttu-id="03a5c-104">Gibt an, ob der proxylocator einen Proxy Server für lokale Adressen verwenden soll.</span><span class="sxs-lookup"><span data-stu-id="03a5c-104">Specifies whether the proxy locator should use a proxy server for local addresses.</span></span>



<span data-ttu-id="03a5c-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="03a5c-105">Data type</span></span>

<span data-ttu-id="03a5c-106">PROPVARIANT-Typ (VT)</span><span class="sxs-lookup"><span data-stu-id="03a5c-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="03a5c-107">PROPVARIANT-Member</span><span class="sxs-lookup"><span data-stu-id="03a5c-107">PROPVARIANT member</span></span>

<span data-ttu-id="03a5c-108">Boolescher Wert (**Long**)</span><span class="sxs-lookup"><span data-stu-id="03a5c-108">Boolean (**LONG**)</span></span>

<span data-ttu-id="03a5c-109">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="03a5c-109">VT\_I4</span></span>

<span data-ttu-id="03a5c-110">**LVAL**</span><span class="sxs-lookup"><span data-stu-id="03a5c-110">**lVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="03a5c-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="03a5c-111">Remarks</span></span>

<span data-ttu-id="03a5c-112">Die Konstante **MF-Quelle \_ proxybypassforlocal** definiert die GUID für diesen Eigenschafts Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="03a5c-112">The constant **MFNETSOURCE\_PROXYBYPASSFORLOCAL** defines the GUID for this property key.</span></span> <span data-ttu-id="03a5c-113">Der Eigenschaften Bezeichner (PID) ist 0 (null).</span><span class="sxs-lookup"><span data-stu-id="03a5c-113">The property identifier (PID) is zero.</span></span>

<span data-ttu-id="03a5c-114">Anwendungen können diese Eigenschaft verwenden, um den proxylocator bei der Erstellung des proxylocator-Objekts zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="03a5c-114">Applications can use this property to configure the proxy locator when creating the proxy locator object.</span></span> <span data-ttu-id="03a5c-115">Um die-Eigenschaft festzulegen, übergeben Sie einen **IPropertyStore** -Zeiger im *pproxyconfig* -Parameter der [**mfkreateproxylocator**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateproxylocator) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="03a5c-115">To set the property, pass an **IPropertyStore** pointer in the *pProxyConfig* parameter of the [**MFCreateProxyLocator**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateproxylocator) function.</span></span> <span data-ttu-id="03a5c-116">Der Wert muss auf 0 festgelegt werden, wenn der Proxy Server für lokale Adressen verwendet werden soll. Andernfalls konfiguriert ein Wert ungleich NULL den standardproxylocator, um den Proxy Server für lokale Adressen zu überspringen.</span><span class="sxs-lookup"><span data-stu-id="03a5c-116">The value must be set to 0 if the proxy server is to be used for local addresses; otherwise a nonzero value configures the default proxy locator to skip the proxy server for local addresses.</span></span>

## <a name="requirements"></a><span data-ttu-id="03a5c-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="03a5c-117">Requirements</span></span>



| <span data-ttu-id="03a5c-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="03a5c-118">Requirement</span></span> | <span data-ttu-id="03a5c-119">Wert</span><span class="sxs-lookup"><span data-stu-id="03a5c-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="03a5c-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="03a5c-120">Minimum supported client</span></span><br/> | <span data-ttu-id="03a5c-121">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="03a5c-121">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="03a5c-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="03a5c-122">Minimum supported server</span></span><br/> | <span data-ttu-id="03a5c-123">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="03a5c-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="03a5c-124">Header</span><span class="sxs-lookup"><span data-stu-id="03a5c-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="03a5c-125"><dt>Mspdl. h</dt></span><span class="sxs-lookup"><span data-stu-id="03a5c-125"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="03a5c-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="03a5c-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="03a5c-127">Eigenschaften von Media Foundation</span><span class="sxs-lookup"><span data-stu-id="03a5c-127">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="03a5c-128">Netzwerk in Media Foundation</span><span class="sxs-lookup"><span data-stu-id="03a5c-128">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> <dt>

[<span data-ttu-id="03a5c-129">Proxy Unterstützung für Netzwerk Quellen</span><span class="sxs-lookup"><span data-stu-id="03a5c-129">Proxy Support for Network Sources</span></span>](proxy-support-for-network-sources.md)
</dt> </dl>

 

 




