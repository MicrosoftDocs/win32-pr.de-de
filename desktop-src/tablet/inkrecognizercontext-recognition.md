---
description: Tritt auf, wenn der inkrecognizercontext Ergebnisse aus der backgrounderkennmethode generiert hat.
ms.assetid: 0cc319af-cd0b-4089-928b-cae6c86f6f61
title: Inkrecognizercontext. Recognition-Ereignis (msink AUT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 86da1a7470169f9f978e92a87f3e32f7e63acb42
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106350059"
---
# <a name="inkrecognizercontextrecognition-event"></a><span data-ttu-id="85358-103">Inkrecognizercontext. Recognition-Ereignis</span><span class="sxs-lookup"><span data-stu-id="85358-103">InkRecognizerContext.Recognition event</span></span>

<span data-ttu-id="85358-104">Tritt auf, wenn der [**inkrecognizercontext**](inkrecognizercontext-class.md) Ergebnisse aus der [**backgrounderkennmethode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-backgroundrecognize) generiert hat.</span><span class="sxs-lookup"><span data-stu-id="85358-104">Occurs when the [**InkRecognizerContext**](inkrecognizercontext-class.md) has generated results from the [**BackgroundRecognize**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-backgroundrecognize) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="85358-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="85358-105">Syntax</span></span>


```C++
void Recognition(
  [in] BSTR                 RecognizedString,
  [in] VARIANT              CustomData,
  [in] InkRecognitionStatus RecognitionStatus
);
```



## <a name="parameters"></a><span data-ttu-id="85358-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="85358-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="85358-107">*Erkennungs Zeichenfolge* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="85358-107">*RecognizedString* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="85358-108">Der Erkennungs Ergebnis Text mit dem höchsten Vertrauen.</span><span class="sxs-lookup"><span data-stu-id="85358-108">The recognition result text with the highest confidence.</span></span>

<span data-ttu-id="85358-109">Weitere Informationen zum BSTR-Datentyp finden [Sie unter Verwenden der com-Bibliothek](using-the-com-library.md).</span><span class="sxs-lookup"><span data-stu-id="85358-109">For more information about the BSTR data type, see the [Using the COM Library](using-the-com-library.md).</span></span>

</dd> <dt>

<span data-ttu-id="85358-110">*CustomData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="85358-110">*CustomData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="85358-111">Das-Objekt, das die benutzerdefinierten Daten für das Erkennungs Ergebnis enthält.</span><span class="sxs-lookup"><span data-stu-id="85358-111">The object that contains the custom data for the recognition result.</span></span>

<span data-ttu-id="85358-112">Weitere Informationen zur VARIANT-Struktur finden [Sie unter Verwenden der com-Bibliothek](using-the-com-library.md).</span><span class="sxs-lookup"><span data-stu-id="85358-112">For more information about the VARIANT structure, see the [Using the COM Library](using-the-com-library.md).</span></span>

</dd> <dt>

<span data-ttu-id="85358-113">*Erkennungs Status* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="85358-113">*RecognitionStatus* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="85358-114">Der Erkennungs Status für das letzte Erkennungs Ergebnis.</span><span class="sxs-lookup"><span data-stu-id="85358-114">The recognition status as of the most recent recognition result.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="85358-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="85358-115">Return value</span></span>

<span data-ttu-id="85358-116">Dieses Ereignis gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="85358-116">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="85358-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="85358-117">Remarks</span></span>

<span data-ttu-id="85358-118">Das Verhalten der Anwendungsprogrammierschnittstelle (Application Programming Interface, API) ist unvorhersehbar, wenn Sie versuchen, vom Erkennungs Ereignishandler auf das ursprüngliche [**inkrecognizercontext**](inkrecognizercontext-class.md) -Objekt zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="85358-118">The behavior of the application programming interface (API) is unpredictable if you try to gain access to the original [**InkRecognizerContext**](inkrecognizercontext-class.md) object from the recognition event handler.</span></span> <span data-ttu-id="85358-119">Versuchen Sie nicht, dies zu tun.</span><span class="sxs-lookup"><span data-stu-id="85358-119">Do not attempt to do this.</span></span> <span data-ttu-id="85358-120">Wenn Sie dies tun müssen, erstellen Sie stattdessen ein Flag, und legen Sie es im [Erkennungs](ink-recognition.md) Ereignishandler fest.</span><span class="sxs-lookup"><span data-stu-id="85358-120">Instead, if you need to do this, create a flag and set it in the [Recognition](ink-recognition.md) event handler.</span></span> <span data-ttu-id="85358-121">Anschließend können Sie dieses Flag Abfragen, um zu bestimmen, wann die **inkrecognizercontext** -Eigenschaften außerhalb des Ereignis Handlers geändert werden müssen.</span><span class="sxs-lookup"><span data-stu-id="85358-121">Then you can poll that flag to determine when to change the **InkRecognizerContext** properties outside of the event handler.</span></span>

<span data-ttu-id="85358-122">Diese Ereignismethode wird in der \_ iinkevents-Schnittstelle definiert.</span><span class="sxs-lookup"><span data-stu-id="85358-122">This event method is defined in the \_IInkEvents interface.</span></span> <span data-ttu-id="85358-123">Die \_ iinkevents-Schnittstelle implementiert die [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) -Schnittstelle mit dem Bezeichner "DISPID \_ unerekognition".</span><span class="sxs-lookup"><span data-stu-id="85358-123">The \_IInkEvents interface implements the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface with an identifier of DISPID\_IRERecognition.</span></span>

## <a name="requirements"></a><span data-ttu-id="85358-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="85358-124">Requirements</span></span>



| <span data-ttu-id="85358-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="85358-125">Requirement</span></span> | <span data-ttu-id="85358-126">Wert</span><span class="sxs-lookup"><span data-stu-id="85358-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="85358-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="85358-127">Minimum supported client</span></span><br/> | <span data-ttu-id="85358-128">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="85358-128">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="85358-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="85358-129">Minimum supported server</span></span><br/> | <span data-ttu-id="85358-130">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="85358-130">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="85358-131">Header</span><span class="sxs-lookup"><span data-stu-id="85358-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="85358-132"><dt>Msink AUT. h (erfordert auch msink AUT \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="85358-132"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="85358-133">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="85358-133">Library</span></span><br/>                  | <dl> <span data-ttu-id="85358-134"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="85358-134"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="85358-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="85358-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="85358-136">**Inkrecognizercontext-Klasse**</span><span class="sxs-lookup"><span data-stu-id="85358-136">**InkRecognizerContext Class**</span></span>](inkrecognizercontext-class.md)
</dt> <dt>

[<span data-ttu-id="85358-137">**Backgrounderkenungsmethode**</span><span class="sxs-lookup"><span data-stu-id="85358-137">**BackgroundRecognize Method**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-backgroundrecognize)
</dt> <dt>

[<span data-ttu-id="85358-138">**Inkrecognitionstatus-Enumeration**</span><span class="sxs-lookup"><span data-stu-id="85358-138">**InkRecognitionStatus Enumeration**</span></span>](/windows/desktop/api/msinkaut/ne-msinkaut-inkrecognitionstatus)
</dt> <dt>

[<span data-ttu-id="85358-139">**Methode erkennen**</span><span class="sxs-lookup"><span data-stu-id="85358-139">**Recognize Method**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-recognize)
</dt> <dt>

[<span data-ttu-id="85358-140">**Iinkrecognitionresult-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="85358-140">**IInkRecognitionResult Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionresult)
</dt> </dl>

 

