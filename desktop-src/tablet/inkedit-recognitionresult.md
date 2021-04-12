---
description: 'Tritt auf, wenn das InkEdit-Steuerelement Ergebnisse manuell von einem Rückruf der InkEdit:: Recognition-Methode oder automatisch nach dem Auslösen des Erkennungs Timeouts abruft.'
ms.assetid: 09618be0-fe49-494f-940f-79ff8352097e
title: InkEdit. erkentionresult-Ereignis (Inked. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 40d6206293b604e5540b5e6d0271e1ebe984a987
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218053"
---
# <a name="inkeditrecognitionresult-event"></a><span data-ttu-id="9a6c4-103">InkEdit. erkentionresult-Ereignis</span><span class="sxs-lookup"><span data-stu-id="9a6c4-103">InkEdit.RecognitionResult event</span></span>

<span data-ttu-id="9a6c4-104">Tritt auf, wenn das [InkEdit](inkedit-control-reference.md) -Steuerelement Ergebnisse manuell von einem Rückruf der [**InkEdit::**](/windows/desktop/api/inked/nf-inked-iinkedit-recognize) Recognition-Methode oder automatisch nach dem Auslösen des Erkennungs Timeouts abruft.</span><span class="sxs-lookup"><span data-stu-id="9a6c4-104">Occurs when the [InkEdit](inkedit-control-reference.md) control gets results manually from a call to the [**InkEdit::Recognize**](/windows/desktop/api/inked/nf-inked-iinkedit-recognize) method or automatically after the recognition timeout fires.</span></span>

## <a name="syntax"></a><span data-ttu-id="9a6c4-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="9a6c4-105">Syntax</span></span>


```C++
void RecognitionResult(
  [in] IInkRecognitionResult *RecognitionResult
);
```



## <a name="parameters"></a><span data-ttu-id="9a6c4-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="9a6c4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9a6c4-107">*Erkennungs Ergebnis* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9a6c4-107">*RecognitionResult* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9a6c4-108">Ein [**iinkrecognitionresult**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionresult) -Objekt, das das Ergebnis der Erkennung enthält.</span><span class="sxs-lookup"><span data-stu-id="9a6c4-108">An [**IInkRecognitionResult**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionresult) object that contains the result of the recognition.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9a6c4-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9a6c4-109">Return value</span></span>

<span data-ttu-id="9a6c4-110">Dieses Ereignis gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="9a6c4-110">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="9a6c4-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9a6c4-111">Remarks</span></span>

<span data-ttu-id="9a6c4-112">Diese Ereignismethode wird in der **\_ iinkeditevents** -Schnittstelle definiert.</span><span class="sxs-lookup"><span data-stu-id="9a6c4-112">This event method is defined in the **\_IInkEditEvents** interface.</span></span> <span data-ttu-id="9a6c4-113">Die **\_ iinkeditevents** -Schnittstelle implementiert die [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) -Schnittstelle mit dem Bezeichner DISPID \_ ieerecognitionresult.</span><span class="sxs-lookup"><span data-stu-id="9a6c4-113">The **\_IInkEditEvents** interface implements the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface with an identifier of DISPID\_IeeRecognitionResult.</span></span>

## <a name="requirements"></a><span data-ttu-id="9a6c4-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9a6c4-114">Requirements</span></span>



| <span data-ttu-id="9a6c4-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9a6c4-115">Requirement</span></span> | <span data-ttu-id="9a6c4-116">Wert</span><span class="sxs-lookup"><span data-stu-id="9a6c4-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9a6c4-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9a6c4-117">Minimum supported client</span></span><br/> | <span data-ttu-id="9a6c4-118">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9a6c4-118">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="9a6c4-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9a6c4-119">Minimum supported server</span></span><br/> | <span data-ttu-id="9a6c4-120">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="9a6c4-120">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="9a6c4-121">Header</span><span class="sxs-lookup"><span data-stu-id="9a6c4-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="9a6c4-122"><dt>In "-. h" (auch als "gezeichneten \_ i. c" erforderlich)</dt></span><span class="sxs-lookup"><span data-stu-id="9a6c4-122"><dt>Inked.h (also requires inked\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="9a6c4-123">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="9a6c4-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="9a6c4-124"><dt>InkEd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9a6c4-124"><dt>InkEd.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="9a6c4-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9a6c4-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9a6c4-126">InkEdit</span><span class="sxs-lookup"><span data-stu-id="9a6c4-126">InkEdit</span></span>](inkedit-control-reference.md)
</dt> <dt>

<span data-ttu-id="9a6c4-127">[**Methode " \[ InkEdit-Steuerelement" erkennen\]**](/windows/desktop/api/inked/nf-inked-iinkedit-recognize)</span><span class="sxs-lookup"><span data-stu-id="9a6c4-127">[**Recognize Method \[InkEdit Control\]**](/windows/desktop/api/inked/nf-inked-iinkedit-recognize)</span></span>
</dt> </dl>

 

