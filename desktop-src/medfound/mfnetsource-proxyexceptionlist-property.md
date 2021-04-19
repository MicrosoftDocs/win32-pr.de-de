---
description: Gibt eine durch Semikolons getrennte Liste von Medienservern an, die Verbindungen von Client Anwendungen akzeptieren können, ohne einen Proxy Server zu verwenden.
ms.assetid: 218883c5-9a26-4733-8308-1827cf1f2cd7
title: MFNETSOURCE_PROXYEXCEPTIONLIST-Eigenschaft (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 591f7036491964928937f2b48b0656e60f9a20f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106362215"
---
# <a name="mfnetsource_proxyexceptionlist-property"></a><span data-ttu-id="f4100-103">MF-Quelle \_ proxyexceptionlist (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="f4100-103">MFNETSOURCE\_PROXYEXCEPTIONLIST property</span></span>

<span data-ttu-id="f4100-104">Gibt eine durch Semikolons getrennte Liste von Medienservern an, die Verbindungen von Client Anwendungen akzeptieren können, ohne einen Proxy Server zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="f4100-104">Specifies a semicolon-delimited list of media servers that can accept connections from client applications without using a proxy server.</span></span>



<span data-ttu-id="f4100-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="f4100-105">Data type</span></span>

<span data-ttu-id="f4100-106">PROPVARIANT-Typ (VT)</span><span class="sxs-lookup"><span data-stu-id="f4100-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="f4100-107">PROPVARIANT-Member</span><span class="sxs-lookup"><span data-stu-id="f4100-107">PROPVARIANT member</span></span>

<span data-ttu-id="f4100-108">Breit Zeichen-Zeichenfolge (**WCHAR** \* )</span><span class="sxs-lookup"><span data-stu-id="f4100-108">Wide-character string (**WCHAR**\*)</span></span>

<span data-ttu-id="f4100-109">VT \_ LPWSTR</span><span class="sxs-lookup"><span data-stu-id="f4100-109">VT\_LPWSTR</span></span>

<span data-ttu-id="f4100-110">**pwszval**</span><span class="sxs-lookup"><span data-stu-id="f4100-110">**pwszVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="f4100-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f4100-111">Remarks</span></span>

<span data-ttu-id="f4100-112">Die Konstante " **MF NetSource \_ proxyexceptionlist** " definiert die GUID für diesen Eigenschafts Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="f4100-112">The constant **MFNETSOURCE\_PROXYEXCEPTIONLIST** defines the GUID for this property key.</span></span> <span data-ttu-id="f4100-113">Der Eigenschaften Bezeichner (PID) ist 0 (null).</span><span class="sxs-lookup"><span data-stu-id="f4100-113">The property identifier (PID) is zero.</span></span>

<span data-ttu-id="f4100-114">Anwendungen können diese Eigenschaft verwenden, um den proxylocator bei der Erstellung des proxylocator-Objekts zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="f4100-114">Applications can use this property to configure the proxy locator when creating the proxy locator object.</span></span> <span data-ttu-id="f4100-115">Um die-Eigenschaft festzulegen, übergeben Sie einen **IPropertyStore** -Zeiger im *pproxyconfig* -Parameter der [**mfkreateproxylocator**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateproxylocator) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="f4100-115">To set the property, pass an **IPropertyStore** pointer in the *pProxyConfig* parameter of the [**MFCreateProxyLocator**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateproxylocator) function.</span></span> <span data-ttu-id="f4100-116">Der proxylocator führt keine Proxy Erkennung für diese Adressen aus.</span><span class="sxs-lookup"><span data-stu-id="f4100-116">The proxy locator does not perform proxy detection for these addresses.</span></span>

## <a name="requirements"></a><span data-ttu-id="f4100-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f4100-117">Requirements</span></span>



| <span data-ttu-id="f4100-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f4100-118">Requirement</span></span> | <span data-ttu-id="f4100-119">Wert</span><span class="sxs-lookup"><span data-stu-id="f4100-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="f4100-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f4100-120">Minimum supported client</span></span><br/> | <span data-ttu-id="f4100-121">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f4100-121">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="f4100-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f4100-122">Minimum supported server</span></span><br/> | <span data-ttu-id="f4100-123">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f4100-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="f4100-124">Header</span><span class="sxs-lookup"><span data-stu-id="f4100-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="f4100-125"><dt>Mspdl. h</dt></span><span class="sxs-lookup"><span data-stu-id="f4100-125"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f4100-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f4100-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f4100-127">Eigenschaften von Media Foundation</span><span class="sxs-lookup"><span data-stu-id="f4100-127">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="f4100-128">Netzwerk in Media Foundation</span><span class="sxs-lookup"><span data-stu-id="f4100-128">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> <dt>

[<span data-ttu-id="f4100-129">Proxy Unterstützung für Netzwerk Quellen</span><span class="sxs-lookup"><span data-stu-id="f4100-129">Proxy Support for Network Sources</span></span>](proxy-support-for-network-sources.md)
</dt> </dl>

 

 




