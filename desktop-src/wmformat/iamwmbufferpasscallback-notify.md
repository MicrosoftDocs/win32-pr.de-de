---
title: Iamwmbufferpasscallback-Benachrichtigungs Methode
description: Die Notify-Methode wird von der PIN für jeden Puffer aufgerufen, der beim Streaming zugestellt wird.
ms.assetid: 3f252754-c784-4ffd-bcfc-fab73fa02b9a
keywords:
- Notify-Methode Windows Media-Format
- Notify-Methode Windows Media-Format, iamwmbufferpasscallback-Schnittstelle
- Iamwmbufferpasscallback-Schnittstelle Windows Media-Format, Notify-Methode
topic_type:
- apiref
api_name:
- IAMWMBufferPassCallback.Notify
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e8f362262b36dee0bfc9a18e57010d102b2fa2cb
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104102143"
---
# <a name="iamwmbufferpasscallbacknotify-method"></a><span data-ttu-id="ed6e1-106">Iamwmbufferpasscallback:: Notify-Methode</span><span class="sxs-lookup"><span data-stu-id="ed6e1-106">IAMWMBufferPassCallback::Notify method</span></span>

<span data-ttu-id="ed6e1-107">Die **Notify** -Methode wird von der PIN für jeden Puffer aufgerufen, der beim Streaming zugestellt wird.</span><span class="sxs-lookup"><span data-stu-id="ed6e1-107">The **Notify** method is called by the pin for each buffer that is delivered during streaming.</span></span>

## <a name="syntax"></a><span data-ttu-id="ed6e1-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="ed6e1-108">Syntax</span></span>


```C++
HRESULT Notify(
  [in] INSSBuffer3    *pNSSBuffer3,
  [in] IPin           *pPin,
  [in] REFERENCE_TIME *prtStart,
  [in] REFERENCE_TIME *prtEnd
);
```



## <a name="parameters"></a><span data-ttu-id="ed6e1-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="ed6e1-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ed6e1-110">*pNSSBuffer3* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ed6e1-110">*pNSSBuffer3* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ed6e1-111">Zeiger auf die [**INSSBuffer3**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer3) -Schnittstelle, die für das Medien Beispiel verfügbar gemacht wird</span><span class="sxs-lookup"><span data-stu-id="ed6e1-111">Pointer to the [**INSSBuffer3**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer3) interface exposed on the media sample.</span></span>

</dd> <dt>

<span data-ttu-id="ed6e1-112">*ppin* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ed6e1-112">*pPin* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ed6e1-113">Ein Zeiger auf die PIN, die dem Mediendaten Strom zugeordnet ist, zu dem das Beispiel gehört.</span><span class="sxs-lookup"><span data-stu-id="ed6e1-113">Pointer to the pin associated with the media stream that the sample belongs to.</span></span>

</dd> <dt>

<span data-ttu-id="ed6e1-114">*prtstart* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ed6e1-114">*prtStart* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ed6e1-115">Die Startzeit des Beispiels.</span><span class="sxs-lookup"><span data-stu-id="ed6e1-115">Start time of the sample.</span></span>

</dd> <dt>

<span data-ttu-id="ed6e1-116">*prtend* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ed6e1-116">*prtEnd* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ed6e1-117">Endzeit des Beispiels.</span><span class="sxs-lookup"><span data-stu-id="ed6e1-117">End time of the sample.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ed6e1-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ed6e1-118">Return value</span></span>

<span data-ttu-id="ed6e1-119">Es ist kein bestimmter Rückgabewert angegeben.</span><span class="sxs-lookup"><span data-stu-id="ed6e1-119">No particular return value is specified.</span></span> <span data-ttu-id="ed6e1-120">Die aufrufenden Pin ignoriert das **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="ed6e1-120">The calling pin ignores the **HRESULT**.</span></span>

## <a name="remarks"></a><span data-ttu-id="ed6e1-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ed6e1-121">Remarks</span></span>

<span data-ttu-id="ed6e1-122">Diese Methode ermöglicht es einer Anwendung, Informationen im Medien Puffer zu überprüfen und zu bearbeiten, bevor die Puffer Inhalte verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="ed6e1-122">This method enables an application to examine and act on information in the media buffer before the buffer contents are processed.</span></span> <span data-ttu-id="ed6e1-123">Die Anwendung ist dafür verantwortlich, den Medientyp in der PIN zu kennen.</span><span class="sxs-lookup"><span data-stu-id="ed6e1-123">The application is responsible for knowing the media type on the pin.</span></span> <span data-ttu-id="ed6e1-124">Diese Informationen können abgerufen werden, indem zuerst die streaminformationen aus dem Profil abgerufen und anschließend die [**IConfigAsfWriter2:: streamnumfrompin**](iconfigasfwriter2-streamnumfrompin.md) -Methode aufgerufen wird, um zu bestimmen, welche Pin den einzelnen Datenströmen zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="ed6e1-124">This information can be obtained by first getting the stream information from the profile and then calling [**IConfigAsfWriter2::StreamNumFromPin**](iconfigasfwriter2-streamnumfrompin.md) method to determine which pin is associated with each stream.</span></span>

## <a name="see-also"></a><span data-ttu-id="ed6e1-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ed6e1-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ed6e1-126">**DirectShow-qasf-Referenz**</span><span class="sxs-lookup"><span data-stu-id="ed6e1-126">**DirectShow QASF Reference**</span></span>](directshow-qasf-reference.md)
</dt> <dt>

[<span data-ttu-id="ed6e1-127">**Iamwmbufferpasscallback-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="ed6e1-127">**IAMWMBufferPassCallback Interface**</span></span>](/previous-versions/windows/desktop/api/dshowasf/nn-dshowasf-iamwmbufferpasscallback)
</dt> <dt>

[<span data-ttu-id="ed6e1-128">**INSSBuffer3-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="ed6e1-128">**INSSBuffer3 Interface**</span></span>](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer3)
</dt> </dl>

 

 