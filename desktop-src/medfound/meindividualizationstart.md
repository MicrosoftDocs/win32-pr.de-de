---
description: Wird von der-Richtlinien-Engine ausgelöst, wenn die Individualisierung beginnt. Die Individualisierung wird mithilfe der Anwendungs Implementierung der IMF contentschutzmanager-Schnittstelle durchgeführt.
ms.assetid: a3ba98ee-4d2e-466d-be9a-c7e3b5f920a7
title: Meindividualizationstart-Ereignis (mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dbb8d50bbc2081c4efa41d8b15cc3e41a14ab5eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106357455"
---
# <a name="meindividualizationstart-event"></a><span data-ttu-id="62063-104">Meindividualizationstart-Ereignis</span><span class="sxs-lookup"><span data-stu-id="62063-104">MEIndividualizationStart event</span></span>

<span data-ttu-id="62063-105">Wird von der-Richtlinien-Engine ausgelöst, wenn die Individualisierung beginnt.</span><span class="sxs-lookup"><span data-stu-id="62063-105">Raised by the policy engine when individualization is about to begin.</span></span> <span data-ttu-id="62063-106">Die Individualisierung erfolgt mithilfe der Implementierung der Anwendung der [**imbocontentschutzmanager**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentprotectionmanager) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="62063-106">Individualization is performed using the application's implementation of the [**IMFContentProtectionManager**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentprotectionmanager) interface.</span></span>

<span data-ttu-id="62063-107">Eine individualisierte Anwendung ist eine Anwendung, die ein Upgrade auf die Digital Rights Management (DRM)-Komponenten erhalten hat, die Sie von allen anderen Kopien derselben Anwendung unterscheiden.</span><span class="sxs-lookup"><span data-stu-id="62063-107">An individualized application is one that has received an upgrade to its digital rights management (DRM) components that differentiates it from all other copies of the same application.</span></span> <span data-ttu-id="62063-108">Inhalts Besitzer können verlangen, dass Ihre geschützten Dateien nur in einer Anwendung wiedergegeben werden, die individuell ist.</span><span class="sxs-lookup"><span data-stu-id="62063-108">Content owners can require that their protected files be played only on an application that has been individualized.</span></span>

## <a name="event-values"></a><span data-ttu-id="62063-109">Ereigniswerte</span><span class="sxs-lookup"><span data-stu-id="62063-109">Event values</span></span>

<span data-ttu-id="62063-110">Mögliche Werte, die von [**imfmediaevent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) abgerufen werden, sind folgende.</span><span class="sxs-lookup"><span data-stu-id="62063-110">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="62063-111">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="62063-111">VARTYPE</span></span>              | <span data-ttu-id="62063-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="62063-112">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="62063-113">VT \_ leer</span><span class="sxs-lookup"><span data-stu-id="62063-113">VT\_EMPTY</span></span><br/> | <span data-ttu-id="62063-114">Keine Ereignisdaten.</span><span class="sxs-lookup"><span data-stu-id="62063-114">No event data.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="62063-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="62063-115">Remarks</span></span>

<span data-ttu-id="62063-116">Wenn die Lizenz Beschaffung abgeschlossen ist, löst die Richtlinien-Engine das Ereignis " [meindividualizationabgeschlossene](meindividualizationcompleted.md) " aus.</span><span class="sxs-lookup"><span data-stu-id="62063-116">When license acquisition is completed, the policy engine raises the [MEIndividualizationCompleted](meindividualizationcompleted.md) event.</span></span>

## <a name="requirements"></a><span data-ttu-id="62063-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="62063-117">Requirements</span></span>



| <span data-ttu-id="62063-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="62063-118">Requirement</span></span> | <span data-ttu-id="62063-119">Wert</span><span class="sxs-lookup"><span data-stu-id="62063-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="62063-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="62063-120">Minimum supported client</span></span><br/> | <span data-ttu-id="62063-121">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="62063-121">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="62063-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="62063-122">Minimum supported server</span></span><br/> | <span data-ttu-id="62063-123">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="62063-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="62063-124">Header</span><span class="sxs-lookup"><span data-stu-id="62063-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="62063-125"><dt>Mfobjects. h (Include mfdl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="62063-125"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="62063-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="62063-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="62063-127">Ereignisse Media Foundation</span><span class="sxs-lookup"><span data-stu-id="62063-127">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




