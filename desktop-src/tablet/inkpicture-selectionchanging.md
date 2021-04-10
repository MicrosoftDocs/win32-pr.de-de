---
description: Tritt auf, wenn die Auswahl von frei Hand Eingaben innerhalb des InkPicture-Steuer Elements geändert wird, z. b. durch Änderungen an der Benutzeroberfläche, von Ausschneide-und Einfüge Prozeduren oder von der Selection-Eigenschaft.
ms.assetid: a8ae30ff-fb0d-44cc-a5d3-295117addafd
title: InkPicture. SelectionChanging-Ereignis (msink AUT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 37b8a35d57aeb9367bb9d30647cb074a7e0e6fbd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868288"
---
# <a name="inkpictureselectionchanging-event"></a><span data-ttu-id="4a408-103">InkPicture. SelectionChanging-Ereignis</span><span class="sxs-lookup"><span data-stu-id="4a408-103">InkPicture.SelectionChanging event</span></span>

<span data-ttu-id="4a408-104">Tritt auf, wenn die Auswahl von frei Hand Eingaben innerhalb des [InkPicture](inkpicture-control-reference.md) -Steuer Elements geändert wird, z. b. durch Änderungen an der Benutzeroberfläche, von Ausschneide-und Einfüge Prozeduren oder von der [**Selection**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection) -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="4a408-104">Occurs when the selection of ink within the [InkPicture](inkpicture-control-reference.md) control is about to change, such as through alterations to the user interface, cut-and-paste procedures, or the [**Selection**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection) property.</span></span>

## <a name="syntax"></a><span data-ttu-id="4a408-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="4a408-105">Syntax</span></span>


```C++
void SelectionChanging(
  [in] IInkStrokes *NewSelection
);
```



## <a name="parameters"></a><span data-ttu-id="4a408-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="4a408-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4a408-107">*Neuauswahl* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4a408-107">*NewSelection* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4a408-108">Die neue Sammlung von [inkstrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) , die ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="4a408-108">The new collection of [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) that is being selected.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4a408-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4a408-109">Return value</span></span>

<span data-ttu-id="4a408-110">Dieses Ereignis gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="4a408-110">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="4a408-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4a408-111">Remarks</span></span>

<span data-ttu-id="4a408-112">Diese Ereignismethode wird in den Dispatch-only-Schnittstellen **\_ iinkoverlayevents** und **\_ iinkpictureevents** (Dispinterfaces) mit der ID "DISPID \_ ioeselectionchanging" definiert.</span><span class="sxs-lookup"><span data-stu-id="4a408-112">This event method is defined in the **\_IInkOverlayEvents** and **\_IInkPictureEvents** dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_IOESelectionChanging.</span></span>

## <a name="requirements"></a><span data-ttu-id="4a408-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4a408-113">Requirements</span></span>



| <span data-ttu-id="4a408-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4a408-114">Requirement</span></span> | <span data-ttu-id="4a408-115">Wert</span><span class="sxs-lookup"><span data-stu-id="4a408-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4a408-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="4a408-116">Minimum supported client</span></span><br/> | <span data-ttu-id="4a408-117">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4a408-117">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="4a408-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="4a408-118">Minimum supported server</span></span><br/> | <span data-ttu-id="4a408-119">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="4a408-119">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="4a408-120">Header</span><span class="sxs-lookup"><span data-stu-id="4a408-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="4a408-121"><dt>Msink AUT. h (erfordert auch msink AUT \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="4a408-121"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="4a408-122">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="4a408-122">Library</span></span><br/>                  | <dl> <span data-ttu-id="4a408-123"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4a408-123"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="4a408-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4a408-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4a408-125">InkPicture</span><span class="sxs-lookup"><span data-stu-id="4a408-125">InkPicture</span></span>](inkpicture-control-reference.md)
</dt> <dt>

<span data-ttu-id="4a408-126">[**Bild-Steuerelement für Auswahl Eigenschaften \[\]**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection)</span><span class="sxs-lookup"><span data-stu-id="4a408-126">[**Selection Property \[InkPicture Control\]**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection)</span></span>
</dt> </dl>

 

