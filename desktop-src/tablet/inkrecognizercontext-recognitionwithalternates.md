---
description: Tritt auf, wenn die inkrecognizercontext-Klasse Ergebnisse generiert hat, nachdem die backgrounderkennzewithalternativen-Methoden Methode aufgerufen wurde.
ms.assetid: 5e86a4d5-c0a7-4283-81cc-ec3a26f74880
title: Inkrecognizercontext. erkentionwithalternativen-Ereignis (msink AUT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e4a7d35d8281305b0cb5f84114bb2f2fa0e718c8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216979"
---
# <a name="inkrecognizercontextrecognitionwithalternates-event"></a><span data-ttu-id="629c0-103">Inkrecognizercontext. erkentionwithalternativen-Ereignis</span><span class="sxs-lookup"><span data-stu-id="629c0-103">InkRecognizerContext.RecognitionWithAlternates event</span></span>

<span data-ttu-id="629c0-104">Tritt auf, wenn die [**inkrecognizercontext-Klasse**](inkrecognizercontext-class.md) Ergebnisse generiert hat, nachdem die [**backgrounderkennzewithalternativen-Methoden**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-backgroundrecognizewithalternates) Methode aufgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="629c0-104">Occurs when the [**InkRecognizerContext Class**](inkrecognizercontext-class.md) has generated results after calling the [**BackgroundRecognizeWithAlternates Method**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-backgroundrecognizewithalternates) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="629c0-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="629c0-105">Syntax</span></span>


```C++
void RecognitionWithAlternates(
  [in] IInkRecognitionResult *RecognitionResult,
  [in] VARIANT               CustomData,
  [in] InkRecognitionStatus  RecognitionStatus
);
```



## <a name="parameters"></a><span data-ttu-id="629c0-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="629c0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="629c0-107">*Erkennungs Ergebnis* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="629c0-107">*RecognitionResult* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="629c0-108">Das Erkennungs Ergebnis des Ereignisses.</span><span class="sxs-lookup"><span data-stu-id="629c0-108">The recognition result from the event.</span></span>

</dd> <dt>

<span data-ttu-id="629c0-109">*CustomData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="629c0-109">*CustomData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="629c0-110">Die benutzerdefinierten Daten für das Erkennungs Ergebnis.</span><span class="sxs-lookup"><span data-stu-id="629c0-110">The custom data for the recognition result.</span></span>

<span data-ttu-id="629c0-111">Weitere Informationen zur VARIANT-Struktur finden Sie unter [Verwenden der com-Bibliothek](using-the-com-library.md).</span><span class="sxs-lookup"><span data-stu-id="629c0-111">For more information about the VARIANT structure, see [Using the COM Library](using-the-com-library.md).</span></span>

</dd> <dt>

<span data-ttu-id="629c0-112">*Erkennungs Status* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="629c0-112">*RecognitionStatus* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="629c0-113">Der Erkennungs Status für das letzte Erkennungs Ergebnis.</span><span class="sxs-lookup"><span data-stu-id="629c0-113">The recognition status as of the most recent recognition result.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="629c0-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="629c0-114">Return value</span></span>

<span data-ttu-id="629c0-115">Dieses Ereignis gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="629c0-115">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="629c0-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="629c0-116">Remarks</span></span>

<span data-ttu-id="629c0-117">Das Verhalten der Anwendungsprogrammierschnittstelle (Application Programming Interface, API) ist unvorhersehbar, wenn Sie versuchen, vom Erkennungs Ereignishandler auf das ursprüngliche [**inkrecognizercontext**](inkrecognizercontext-class.md) -Objekt zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="629c0-117">The behavior of the application programming interface (API) is unpredictable if you try to gain access to the original [**InkRecognizerContext**](inkrecognizercontext-class.md) object from the recognition event handler.</span></span> <span data-ttu-id="629c0-118">Versuchen Sie nicht, dies zu tun.</span><span class="sxs-lookup"><span data-stu-id="629c0-118">Do not attempt to do this.</span></span> <span data-ttu-id="629c0-119">Wenn Sie dies tun müssen, erstellen Sie stattdessen ein Flag, und legen Sie es im [**Erkennungs**](inkrecognizercontext-recognition.md) Ereignishandler fest.</span><span class="sxs-lookup"><span data-stu-id="629c0-119">Instead, if you need to do this, create a flag and set it in the [**Recognition**](inkrecognizercontext-recognition.md) event handler.</span></span> <span data-ttu-id="629c0-120">Anschließend können Sie dieses Flag Abfragen, um zu bestimmen, wann die **inkrecognizercontext** -Eigenschaften außerhalb des Ereignis Handlers geändert werden müssen.</span><span class="sxs-lookup"><span data-stu-id="629c0-120">Then you can poll that flag to determine when to change the **InkRecognizerContext** properties outside of the event handler.</span></span>

<span data-ttu-id="629c0-121">Diese Ereignismethode wird in der \_ iinkevents-Schnittstelle definiert.</span><span class="sxs-lookup"><span data-stu-id="629c0-121">This event method is defined in the \_IInkEvents interface.</span></span> <span data-ttu-id="629c0-122">Die \_ iinkevents-Schnittstelle implementiert die [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) -Schnittstelle mit dem Bezeichner "DISPID", " \_ unerecognitionwithalternativen".</span><span class="sxs-lookup"><span data-stu-id="629c0-122">The \_IInkEvents interface implements the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface with an identifier of DISPID\_IRERecognitionWithAlternates.</span></span>

## <a name="requirements"></a><span data-ttu-id="629c0-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="629c0-123">Requirements</span></span>



| <span data-ttu-id="629c0-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="629c0-124">Requirement</span></span> | <span data-ttu-id="629c0-125">Wert</span><span class="sxs-lookup"><span data-stu-id="629c0-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="629c0-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="629c0-126">Minimum supported client</span></span><br/> | <span data-ttu-id="629c0-127">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="629c0-127">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="629c0-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="629c0-128">Minimum supported server</span></span><br/> | <span data-ttu-id="629c0-129">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="629c0-129">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="629c0-130">Header</span><span class="sxs-lookup"><span data-stu-id="629c0-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="629c0-131"><dt>Msink AUT. h (erfordert auch msink AUT \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="629c0-131"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="629c0-132">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="629c0-132">Library</span></span><br/>                  | <dl> <span data-ttu-id="629c0-133"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="629c0-133"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="629c0-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="629c0-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="629c0-135">**Inkrecognizercontext-Klasse**</span><span class="sxs-lookup"><span data-stu-id="629c0-135">**InkRecognizerContext Class**</span></span>](inkrecognizercontext-class.md)
</dt> <dt>

[<span data-ttu-id="629c0-136">**Backgrounderkenzewithalternativen-Methode**</span><span class="sxs-lookup"><span data-stu-id="629c0-136">**BackgroundRecognizeWithAlternates Method**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-backgroundrecognizewithalternates)
</dt> <dt>

[<span data-ttu-id="629c0-137">**Methode erkennen**</span><span class="sxs-lookup"><span data-stu-id="629c0-137">**Recognize Method**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-recognize)
</dt> <dt>

[<span data-ttu-id="629c0-138">**Iinkrecognitionresult-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="629c0-138">**IInkRecognitionResult Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionresult)
</dt> </dl>

 

