---
description: Gibt an, ob die Media-Senke der Digital Living Network Alliance (DLNA) den Multimedia Class Scheduler Service (MMCSS) verwendet.
ms.assetid: 4c27e2ec-624a-4b1f-bea9-3aaad1534c9b
title: MF_MP2DLNA_USE_MMCSS-Attribut (Mfmp2dlna. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ccfdaf36ce51f1158e110dcb3682a5b072c060dc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104042340"
---
# <a name="mf_mp2dlna_use_mmcss-attribute"></a><span data-ttu-id="e4e0c-103">MF \_ MP2DLNA \_ Verwenden des \_ MMCSS-Attributs</span><span class="sxs-lookup"><span data-stu-id="e4e0c-103">MF\_MP2DLNA\_USE\_MMCSS attribute</span></span>

<span data-ttu-id="e4e0c-104">Gibt an, ob die Media-Senke der Digital Living Network Alliance (DLNA) den Multimedia Class Scheduler Service (MMCSS) verwendet.</span><span class="sxs-lookup"><span data-stu-id="e4e0c-104">Specifies whether the Digital Living Network Alliance (DLNA) media sink uses the Multimedia Class Scheduler Service (MMCSS).</span></span>

## <a name="data-type"></a><span data-ttu-id="e4e0c-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="e4e0c-105">Data type</span></span>

<span data-ttu-id="e4e0c-106">**Bool** gespeichert als **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e4e0c-106">**BOOL** stored as **UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="e4e0c-107">Abrufen/Festlegen</span><span class="sxs-lookup"><span data-stu-id="e4e0c-107">Get/set</span></span>

<span data-ttu-id="e4e0c-108">Um dieses Attribut abzurufen, nennen Sie [**imfattributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="e4e0c-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="e4e0c-109">Um dieses Attribut festzulegen, nennen Sie [**imfattributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="e4e0c-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="remarks"></a><span data-ttu-id="e4e0c-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e4e0c-110">Remarks</span></span>

<span data-ttu-id="e4e0c-111">Wenn Sie dieses Attribut für die DLNA-Medien Senke festlegen möchten, Fragen Sie die Medien Senke nach der [**imfattributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) -Schnittstelle ab.</span><span class="sxs-lookup"><span data-stu-id="e4e0c-111">To set this attribute on the DLNA media sink, query the media sink for the [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) interface.</span></span> <span data-ttu-id="e4e0c-112">Legen Sie das-Attribut vor Beginn des Streamings fest.</span><span class="sxs-lookup"><span data-stu-id="e4e0c-112">Set the attribute before streaming begins.</span></span>

<span data-ttu-id="e4e0c-113">Wenn dieses Attribut **true** ist, registriert sich die DLNA-Medien Senke bei MMCSS.</span><span class="sxs-lookup"><span data-stu-id="e4e0c-113">If this attribute is **TRUE**, the DLNA media sink registers itself with MMCSS.</span></span>

## <a name="requirements"></a><span data-ttu-id="e4e0c-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e4e0c-114">Requirements</span></span>



| <span data-ttu-id="e4e0c-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e4e0c-115">Requirement</span></span> | <span data-ttu-id="e4e0c-116">Wert</span><span class="sxs-lookup"><span data-stu-id="e4e0c-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e4e0c-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e4e0c-117">Minimum supported client</span></span><br/> | <span data-ttu-id="e4e0c-118">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e4e0c-118">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="e4e0c-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e4e0c-119">Minimum supported server</span></span><br/> | <span data-ttu-id="e4e0c-120">Nur Windows Server 2008 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e4e0c-120">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="e4e0c-121">Header</span><span class="sxs-lookup"><span data-stu-id="e4e0c-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="e4e0c-122"><dt>Mfmp2dlna. h</dt></span><span class="sxs-lookup"><span data-stu-id="e4e0c-122"><dt>Mfmp2dlna.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e4e0c-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e4e0c-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e4e0c-124">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="e4e0c-124">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




