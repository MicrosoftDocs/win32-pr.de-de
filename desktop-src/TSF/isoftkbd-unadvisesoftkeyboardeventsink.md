---
title: ISOFT kbd unadvisesoftkeyboardeventsink-Methode (Software-BDC. h)
description: Die Methode isoftkbd unadvisesoftkeyboardeventsink entfernt eine weiche Tastaturereignis Senke.
ms.assetid: 785340bd-c4f6-4c80-a492-6e60d1c1d552
keywords:
- Unadvisesoftkeyboardeventsink-Methode, Text Dienste-Framework
- Unadvisesoftkeyboardeventsink-Methode Text Dienst Framework, iSOFT kbd-Schnittstelle
- ISOFT kbd Interface Text Services Framework, unadvisesoftkeyboardeventsink-Methode
topic_type:
- apiref
api_name:
- ISoftKbd.UnadviseSoftKeyboardEventSink
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2a77129d1b5df024964af4ab19318963708d4b3d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742785"
---
# <a name="isoftkbdunadvisesoftkeyboardeventsink-method"></a><span data-ttu-id="661ad-106">Iweichkbd:: unadvisesoftkeyboardeventsink-Methode</span><span class="sxs-lookup"><span data-stu-id="661ad-106">ISoftKbd::UnadviseSoftKeyboardEventSink method</span></span>

<span data-ttu-id="661ad-107">Die **isoftkbd:: unadvisesoftkeyboardeventsink** -Methode entfernt eine weiche Tastaturereignis Senke.</span><span class="sxs-lookup"><span data-stu-id="661ad-107">The **ISoftKbd::UnadviseSoftKeyboardEventSink** method removes a soft keyboard event sink.</span></span>

## <a name="syntax"></a><span data-ttu-id="661ad-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="661ad-108">Syntax</span></span>


```C++
HRESULT UnadviseSoftKeyboardEventSink(
  [in] TfClientId tid
);
```



## <a name="parameters"></a><span data-ttu-id="661ad-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="661ad-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="661ad-110">*TID* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="661ad-110">*tid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="661ad-111">Der Bezeichner des Clients, der die weiche Tastaturereignis Senke besitzt.</span><span class="sxs-lookup"><span data-stu-id="661ad-111">Identifier of the client that owns the soft keyboard event sink.</span></span> <span data-ttu-id="661ad-112">Dieser Wert wurde übermittelt, als die Ereignis Senke mithilfe von iSoftware installiert wurde: [: advisesoftkeyboarabventsink](isoftkbd-advisesoftkeyboardeventsink.md).</span><span class="sxs-lookup"><span data-stu-id="661ad-112">This value was passed when the event sink was installed using [ISoftKbd::AdviseSoftKeyboardEventSink](isoftkbd-advisesoftkeyboardeventsink.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="661ad-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="661ad-113">Return value</span></span>

<span data-ttu-id="661ad-114">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="661ad-114">This method can return one of these values.</span></span>



| <span data-ttu-id="661ad-115">Wert</span><span class="sxs-lookup"><span data-stu-id="661ad-115">Value</span></span>                                                                                                   | <span data-ttu-id="661ad-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="661ad-116">Description</span></span>                                                   |
|---------------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <dl> <span data-ttu-id="661ad-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="661ad-117"><dt>**S\_OK**</dt></span></span> </dl>                    | <span data-ttu-id="661ad-118">Die Methode war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="661ad-118">The method was successful.</span></span><br/>                         |
| <dl> <span data-ttu-id="661ad-119"><dt>**E \_ invalidArg**</dt></span><span class="sxs-lookup"><span data-stu-id="661ad-119"><dt>**E\_INVALIDARG**</dt></span></span> </dl>            | <span data-ttu-id="661ad-120">Der *TID* -Parameter ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="661ad-120">The *tid* parameter is invalid.</span></span><br/>                    |
| <dl> <span data-ttu-id="661ad-121"><dt>**\_E \_ NOCONNECTION verbinden**</dt></span><span class="sxs-lookup"><span data-stu-id="661ad-121"><dt>**CONNECT\_E\_NOCONNECTION**</dt></span></span> </dl> | <span data-ttu-id="661ad-122">Die von *TID* identifizierte Benachrichtigungs Senke wurde nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="661ad-122">The advise sink identified by *tid* was not found.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="661ad-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="661ad-123">Requirements</span></span>



| <span data-ttu-id="661ad-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="661ad-124">Requirement</span></span> | <span data-ttu-id="661ad-125">Wert</span><span class="sxs-lookup"><span data-stu-id="661ad-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="661ad-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="661ad-126">Minimum supported client</span></span><br/> | <span data-ttu-id="661ad-127">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="661ad-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="661ad-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="661ad-128">Minimum supported server</span></span><br/> | <span data-ttu-id="661ad-129">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="661ad-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="661ad-130">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="661ad-130">Redistributable</span></span><br/>          | <span data-ttu-id="661ad-131">TSF 1,0 unter Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="661ad-131">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                        |
| <span data-ttu-id="661ad-132">Header</span><span class="sxs-lookup"><span data-stu-id="661ad-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="661ad-133"><dt>Software-Domänen Controller. h</dt></span><span class="sxs-lookup"><span data-stu-id="661ad-133"><dt>Softkbdc.h</dt></span></span> </dl>  |
| <span data-ttu-id="661ad-134">IDL</span><span class="sxs-lookup"><span data-stu-id="661ad-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="661ad-135"><dt>Software. idl</dt></span><span class="sxs-lookup"><span data-stu-id="661ad-135"><dt>Softkbd.idl</dt></span></span> </dl> |
| <span data-ttu-id="661ad-136">DLL</span><span class="sxs-lookup"><span data-stu-id="661ad-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="661ad-137"><dt>Softkbd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="661ad-137"><dt>Softkbd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="661ad-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="661ad-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="661ad-139">**Iweichkbd**</span><span class="sxs-lookup"><span data-stu-id="661ad-139">**ISoftKbd**</span></span>](isoftkbd.md)
</dt> <dt>

[<span data-ttu-id="661ad-140">Iweichkbd:: advisesoftkeyboarabventsink</span><span class="sxs-lookup"><span data-stu-id="661ad-140">ISoftKbd::AdviseSoftKeyboardEventSink</span></span>](isoftkbd-advisesoftkeyboardeventsink.md)
</dt> </dl>

 

 





