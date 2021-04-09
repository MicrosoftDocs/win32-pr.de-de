---
description: Gibt an, ob das HTTP-Protokoll in der Netzwerkquelle aktiviert ist.
ms.assetid: dcc4db5c-0274-4a8a-89a4-66cda62e1520
title: MFNETSOURCE_ENABLE_HTTP-Eigenschaft (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 004868c92962702b774a8f6c0a9b75708c5727b2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959138"
---
# <a name="mfnetsource_enable_http-property"></a><span data-ttu-id="a623a-103">MF-Quell \_ Eigenschaft "http aktivieren" \_</span><span class="sxs-lookup"><span data-stu-id="a623a-103">MFNETSOURCE\_ENABLE\_HTTP property</span></span>

<span data-ttu-id="a623a-104">Gibt an, ob das HTTP-Protokoll in der Netzwerkquelle aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="a623a-104">Specifies whether HTTP protocol is enabled in the network source.</span></span>



<span data-ttu-id="a623a-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="a623a-105">Data type</span></span>

<span data-ttu-id="a623a-106">PROPVARIANT-Typ (VT)</span><span class="sxs-lookup"><span data-stu-id="a623a-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="a623a-107">PROPVARIANT-Member</span><span class="sxs-lookup"><span data-stu-id="a623a-107">PROPVARIANT member</span></span>

<span data-ttu-id="a623a-108">Boolescher Wert (**Long**)</span><span class="sxs-lookup"><span data-stu-id="a623a-108">Boolean (**LONG**)</span></span>

<span data-ttu-id="a623a-109">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="a623a-109">VT\_I4</span></span>

<span data-ttu-id="a623a-110">**LVAL**</span><span class="sxs-lookup"><span data-stu-id="a623a-110">**lVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="a623a-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a623a-111">Remarks</span></span>

<span data-ttu-id="a623a-112">Die Konstante **MF- \_ Aktivierung von \_ http** definiert die GUID für diesen Eigenschafts Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="a623a-112">The constant **MFNETSOURCE\_ENABLE\_HTTP** defines the GUID for this property key.</span></span> <span data-ttu-id="a623a-113">Der Eigenschaften Bezeichner (PID) ist 0 (null).</span><span class="sxs-lookup"><span data-stu-id="a623a-113">The property identifier (PID) is zero.</span></span>

<span data-ttu-id="a623a-114">Anwendungen können diese Eigenschaft verwenden, um die Netzwerkquelle zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="a623a-114">Applications can use this property to configure the network source.</span></span> <span data-ttu-id="a623a-115">Um die-Eigenschaft festzulegen, übergeben Sie einen **IPropertyStore** -Zeiger an den quellresolver.</span><span class="sxs-lookup"><span data-stu-id="a623a-115">To set the property, pass an **IPropertyStore** pointer to the source resolver.</span></span> <span data-ttu-id="a623a-116">Weitere Informationen finden Sie unter [Konfigurieren einer Medienquelle](configuring-a-media-source.md).</span><span class="sxs-lookup"><span data-stu-id="a623a-116">For more information, see [Configuring a Media Source](configuring-a-media-source.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a623a-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a623a-117">Requirements</span></span>



| <span data-ttu-id="a623a-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a623a-118">Requirement</span></span> | <span data-ttu-id="a623a-119">Wert</span><span class="sxs-lookup"><span data-stu-id="a623a-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="a623a-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a623a-120">Minimum supported client</span></span><br/> | <span data-ttu-id="a623a-121">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a623a-121">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="a623a-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a623a-122">Minimum supported server</span></span><br/> | <span data-ttu-id="a623a-123">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a623a-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="a623a-124">Header</span><span class="sxs-lookup"><span data-stu-id="a623a-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="a623a-125"><dt>Mspdl. h</dt></span><span class="sxs-lookup"><span data-stu-id="a623a-125"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a623a-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a623a-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a623a-127">Eigenschaften von Media Foundation</span><span class="sxs-lookup"><span data-stu-id="a623a-127">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="a623a-128">Netzwerk in Media Foundation</span><span class="sxs-lookup"><span data-stu-id="a623a-128">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> <dt>

[<span data-ttu-id="a623a-129">Unterstützte Protokolle</span><span class="sxs-lookup"><span data-stu-id="a623a-129">Supported Protocols</span></span>](supported-protocols.md)
</dt> </dl>

 

 




