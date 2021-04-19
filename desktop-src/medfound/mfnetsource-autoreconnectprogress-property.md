---
description: Gibt an, wie oft die Netzwerkquelle versucht hat, eine erneute Verbindung mit dem Netzwerk herzustellen.
ms.assetid: e3410e68-6358-4f00-8039-833a4ccdf7fa
title: MFNETSOURCE_AUTORECONNECTPROGRESS-Eigenschaft (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 05ade09bd425988cb0a64b258ff0887f8e79d4c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106353143"
---
# <a name="mfnetsource_autoreconnectprogress-property"></a><span data-ttu-id="da6a5-103">MF-Quelle \_ autoreconnectprogress (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="da6a5-103">MFNETSOURCE\_AUTORECONNECTPROGRESS property</span></span>

<span data-ttu-id="da6a5-104">Gibt an, wie oft die Netzwerkquelle versucht hat, eine erneute Verbindung mit dem Netzwerk herzustellen.</span><span class="sxs-lookup"><span data-stu-id="da6a5-104">The number of times the network source has attempted to reconnect to the network.</span></span>



<span data-ttu-id="da6a5-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="da6a5-105">Data type</span></span>

<span data-ttu-id="da6a5-106">PROPVARIANT-Typ (VT)</span><span class="sxs-lookup"><span data-stu-id="da6a5-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="da6a5-107">PROPVARIANT-Member</span><span class="sxs-lookup"><span data-stu-id="da6a5-107">PROPVARIANT member</span></span>

<span data-ttu-id="da6a5-108">**DWORD** (als **Long** gespeichert)</span><span class="sxs-lookup"><span data-stu-id="da6a5-108">**DWORD** (stored as **LONG**)</span></span>

<span data-ttu-id="da6a5-109">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="da6a5-109">VT\_I4</span></span>

<span data-ttu-id="da6a5-110">**LVAL**</span><span class="sxs-lookup"><span data-stu-id="da6a5-110">**lVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="da6a5-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="da6a5-111">Remarks</span></span>

<span data-ttu-id="da6a5-112">Die Konstante " **MF NetSource \_ autoreconnectprogress** " definiert die GUID für diesen Eigenschafts Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="da6a5-112">The constant **MFNETSOURCE\_AUTORECONNECTPROGRESS** defines the GUID for this property key.</span></span> <span data-ttu-id="da6a5-113">Der Eigenschaften Bezeichner (PID) ist 0 (null).</span><span class="sxs-lookup"><span data-stu-id="da6a5-113">The property identifier (PID) is zero.</span></span>

<span data-ttu-id="da6a5-114">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="da6a5-114">This property is read-only.</span></span> <span data-ttu-id="da6a5-115">Um diese Eigenschaft abzurufen, Fragen Sie die Netzwerkquelle nach der **IPropertyStore** -Schnittstelle ab, und rufen Sie **IPropertyStore:: GetValue** auf.</span><span class="sxs-lookup"><span data-stu-id="da6a5-115">To retrieve this property, query the network source for the **IPropertyStore** interface and call **IPropertyStore::GetValue**.</span></span>

## <a name="requirements"></a><span data-ttu-id="da6a5-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="da6a5-116">Requirements</span></span>



| <span data-ttu-id="da6a5-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="da6a5-117">Requirement</span></span> | <span data-ttu-id="da6a5-118">Wert</span><span class="sxs-lookup"><span data-stu-id="da6a5-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="da6a5-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="da6a5-119">Minimum supported client</span></span><br/> | <span data-ttu-id="da6a5-120">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="da6a5-120">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="da6a5-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="da6a5-121">Minimum supported server</span></span><br/> | <span data-ttu-id="da6a5-122">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="da6a5-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="da6a5-123">Header</span><span class="sxs-lookup"><span data-stu-id="da6a5-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="da6a5-124"><dt>Mspdl. h</dt></span><span class="sxs-lookup"><span data-stu-id="da6a5-124"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="da6a5-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="da6a5-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="da6a5-126">Eigenschaften von Media Foundation</span><span class="sxs-lookup"><span data-stu-id="da6a5-126">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="da6a5-127">Netzwerk Quell Features</span><span class="sxs-lookup"><span data-stu-id="da6a5-127">Network Source Features</span></span>](network-source-features.md)
</dt> <dt>

[<span data-ttu-id="da6a5-128">Netzwerk in Media Foundation</span><span class="sxs-lookup"><span data-stu-id="da6a5-128">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> </dl>

 

 




