---
description: Enthält einen Zeiger auf die imfsourceopenmonitor-Schnittstelle der Anwendungen.
ms.assetid: 5b94ae87-91fc-49d6-9355-83327cfdb3f3
title: MFPKEY_SourceOpenMonitor-Eigenschaft (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9a49826ee16a733993b9052e12d9e6fcd5003410
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131225"
---
# <a name="mfpkey_sourceopenmonitor-property"></a><span data-ttu-id="a9d28-103">Mfpkey \_ sourceopenmonitor (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="a9d28-103">MFPKEY\_SourceOpenMonitor property</span></span>

<span data-ttu-id="a9d28-104">Enthält einen Zeiger auf die [**imfsourceopenmonitor**](/windows/desktop/api/mfidl/nn-mfidl-imfsourceopenmonitor) -Schnittstelle der Anwendung.</span><span class="sxs-lookup"><span data-stu-id="a9d28-104">Contains a pointer to the application's [**IMFSourceOpenMonitor**](/windows/desktop/api/mfidl/nn-mfidl-imfsourceopenmonitor) interface.</span></span>



<span data-ttu-id="a9d28-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="a9d28-105">Data type</span></span>

<span data-ttu-id="a9d28-106">PROPVARIANT-Typ (VT)</span><span class="sxs-lookup"><span data-stu-id="a9d28-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="a9d28-107">PROPVARIANT-Member</span><span class="sxs-lookup"><span data-stu-id="a9d28-107">PROPVARIANT member</span></span>

<span data-ttu-id="a9d28-108">**IUnknown** -Zeiger</span><span class="sxs-lookup"><span data-stu-id="a9d28-108">**IUnknown** pointer</span></span>

<span data-ttu-id="a9d28-109">VT \_ unbekannt</span><span class="sxs-lookup"><span data-stu-id="a9d28-109">VT\_UNKNOWN</span></span>

<span data-ttu-id="a9d28-110">**punkVal**</span><span class="sxs-lookup"><span data-stu-id="a9d28-110">**punkVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="a9d28-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a9d28-111">Remarks</span></span>

<span data-ttu-id="a9d28-112">Anwendungen können diese Eigenschaft an den quellresolver übergeben, um Ereignis Benachrichtigungen von der Netzwerkquelle zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="a9d28-112">Applications can pass this property to the source resolver to get event notifications from the network source.</span></span>

## <a name="requirements"></a><span data-ttu-id="a9d28-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a9d28-113">Requirements</span></span>



| <span data-ttu-id="a9d28-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a9d28-114">Requirement</span></span> | <span data-ttu-id="a9d28-115">Wert</span><span class="sxs-lookup"><span data-stu-id="a9d28-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="a9d28-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a9d28-116">Minimum supported client</span></span><br/> | <span data-ttu-id="a9d28-117">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a9d28-117">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="a9d28-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a9d28-118">Minimum supported server</span></span><br/> | <span data-ttu-id="a9d28-119">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a9d28-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="a9d28-120">Header</span><span class="sxs-lookup"><span data-stu-id="a9d28-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="a9d28-121"><dt>Mspdl. h</dt></span><span class="sxs-lookup"><span data-stu-id="a9d28-121"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a9d28-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a9d28-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a9d28-123">Eigenschaften von Media Foundation</span><span class="sxs-lookup"><span data-stu-id="a9d28-123">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




