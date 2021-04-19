---
description: Aktiviert oder deaktiviert den Vorschaumodus, der es der Anwendung ermöglicht, die anfängliche pufferlogik zu überschreiben.
ms.assetid: 8aa8c6ac-8746-4bf6-9f57-b1426495a275
title: MFNETSOURCE_PREVIEWMODEENABLED-Eigenschaft (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1170135b0feb90a79bf5e26d36a02e262fdc1977
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362604"
---
# <a name="mfnetsource_previewmodeenabled-property"></a><span data-ttu-id="2efc4-103">Eigenschaft "previewmodeaktivierte" für MF NetSource \_</span><span class="sxs-lookup"><span data-stu-id="2efc4-103">MFNETSOURCE\_PREVIEWMODEENABLED property</span></span>

<span data-ttu-id="2efc4-104">Aktiviert oder deaktiviert den Vorschaumodus, der es der Anwendung ermöglicht, die anfängliche pufferlogik zu überschreiben.</span><span class="sxs-lookup"><span data-stu-id="2efc4-104">Enables or disables preview mode, which enables the application to overwrite the initial buffering logic.</span></span>



<span data-ttu-id="2efc4-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="2efc4-105">Data type</span></span>

<span data-ttu-id="2efc4-106">PROPVARIANT-Typ (VT)</span><span class="sxs-lookup"><span data-stu-id="2efc4-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="2efc4-107">PROPVARIANT-Member</span><span class="sxs-lookup"><span data-stu-id="2efc4-107">PROPVARIANT member</span></span>

<span data-ttu-id="2efc4-108">**BOOL**</span><span class="sxs-lookup"><span data-stu-id="2efc4-108">**BOOL**</span></span>

<span data-ttu-id="2efc4-109">VT \_ bool</span><span class="sxs-lookup"><span data-stu-id="2efc4-109">VT\_BOOL</span></span>

<span data-ttu-id="2efc4-110">**LVAL**</span><span class="sxs-lookup"><span data-stu-id="2efc4-110">**lVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="2efc4-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2efc4-111">Remarks</span></span>

<span data-ttu-id="2efc4-112">Die Konstante " **MF NetSource \_ previewmodeaktivi"** definiert die GUID für den Eigenschafts Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="2efc4-112">The constant **MFNETSOURCE\_PREVIEWMODEENABLED** defines the GUID for the property key.</span></span> <span data-ttu-id="2efc4-113">Der Eigenschaften Bezeichner (PID) ist 0 (null).</span><span class="sxs-lookup"><span data-stu-id="2efc4-113">The property identifier (PID) is zero.</span></span> <span data-ttu-id="2efc4-114">Diese Eigenschaft wird für die Netzwerkquelle festgelegt, indem ein **IPropertyStore** -Zeiger an den quellresolver übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="2efc4-114">This property is set on the network source by passing an **IPropertyStore** pointer to the source resolver.</span></span> <span data-ttu-id="2efc4-115">Weitere Informationen finden Sie unter [Konfigurieren einer Medienquelle](configuring-a-media-source.md).</span><span class="sxs-lookup"><span data-stu-id="2efc4-115">For more information, see [Configuring a Media Source](configuring-a-media-source.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="2efc4-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2efc4-116">Requirements</span></span>



| <span data-ttu-id="2efc4-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2efc4-117">Requirement</span></span> | <span data-ttu-id="2efc4-118">Wert</span><span class="sxs-lookup"><span data-stu-id="2efc4-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="2efc4-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2efc4-119">Minimum supported client</span></span><br/> | <span data-ttu-id="2efc4-120">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2efc4-120">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="2efc4-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2efc4-121">Minimum supported server</span></span><br/> | <span data-ttu-id="2efc4-122">Nur Windows Server 2008 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2efc4-122">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="2efc4-123">Header</span><span class="sxs-lookup"><span data-stu-id="2efc4-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="2efc4-124"><dt>Mspdl. h</dt></span><span class="sxs-lookup"><span data-stu-id="2efc4-124"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2efc4-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2efc4-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2efc4-126">Eigenschaften von Media Foundation</span><span class="sxs-lookup"><span data-stu-id="2efc4-126">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="2efc4-127">Netzwerk in Media Foundation</span><span class="sxs-lookup"><span data-stu-id="2efc4-127">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> </dl>

 

 




