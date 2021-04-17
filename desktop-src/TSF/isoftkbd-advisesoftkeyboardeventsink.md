---
title: ISOFT kbd advisesoftkeyboardeventsink-Methode (Software BDC. h)
description: Die isoftkbd advisesoftkeyboardeventsink-Methode installiert eine weiche Tastaturereignis Senke, um onkeyselection-Benachrichtigungen von der Soft Tastatur zu verarbeiten.
ms.assetid: f7a441dc-7bef-4fc0-bc62-c153a55a844c
keywords:
- Advisesoftkeyboardeventsink-Methode, Text Dienste-Framework
- Advisesoftkeyboardeventsink-Methode, Text Dienste-Framework, iSOFT kbd-Schnittstelle
- ISOFT kbd Interface Text Services-Framework, advisesoftkeyboardeventsink-Methode
topic_type:
- apiref
api_name:
- ISoftKbd.AdviseSoftKeyboardEventSink
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6ab17de2104c6104b044f027152cfc45cca968b6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104392107"
---
# <a name="isoftkbdadvisesoftkeyboardeventsink-method"></a><span data-ttu-id="c099c-106">ISOFT kbd:: advisesoftkeyboardeventsink-Methode</span><span class="sxs-lookup"><span data-stu-id="c099c-106">ISoftKbd::AdviseSoftKeyboardEventSink method</span></span>

<span data-ttu-id="c099c-107">Die **isoftkbd:: advisesoftkeyboardeventsink** -Methode installiert eine weiche Tastaturereignis Senke, um onkeyselection-Benachrichtigungen von der Soft Tastatur zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="c099c-107">The **ISoftKbd::AdviseSoftKeyboardEventSink** method installs a soft keyboard event sink to handle OnKeySelection notifications from the soft keyboard.</span></span>

## <a name="syntax"></a><span data-ttu-id="c099c-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="c099c-108">Syntax</span></span>


```C++
HRESULT AdviseSoftKeyboardEventSink(
  [in]  DWORD    dwKeyboardId,
  [in]  REFIID   riid,
  [in]  IUnknown *punk,
  [out] DWORD    *pdwCookie
);
```



## <a name="parameters"></a><span data-ttu-id="c099c-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="c099c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c099c-110">*dwkeyboardid* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c099c-110">*dwKeyboardId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c099c-111">Der Bezeichner der Soft Tastatur.</span><span class="sxs-lookup"><span data-stu-id="c099c-111">Identifier of the soft keyboard.</span></span>

</dd> <dt>

<span data-ttu-id="c099c-112">*riid* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c099c-112">*riid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c099c-113">Der Schnittstellen Bezeichner für die Sink-Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="c099c-113">Interface identifier for the sink interface.</span></span>

</dd> <dt>

<span data-ttu-id="c099c-114">*Punk* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c099c-114">*punk* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c099c-115">Zeiger auf [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) für die Senke-Schnittstelle, die von *riid* angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="c099c-115">Pointer to [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) for the sink interface specified by *riid*.</span></span> <span data-ttu-id="c099c-116">Dieser Parameter kann nicht auf **null** festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="c099c-116">This parameter cannot be set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="c099c-117">*pdwcookie* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="c099c-117">*pdwCookie* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c099c-118">Zeiger auf den Puffer, in dem diese Methode das weiche Tastatur-"Cookie" abruft, das für die Verbindung mit dem Client verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="c099c-118">Pointer to the buffer in which this method retrieves the soft keyboard "cookie" used for connection to the client.</span></span> <span data-ttu-id="c099c-119">Das Cookie muss für jede Verbindung eindeutig sein.</span><span class="sxs-lookup"><span data-stu-id="c099c-119">The cookie must be unique for each connection.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c099c-120">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c099c-120">Return value</span></span>

<span data-ttu-id="c099c-121">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="c099c-121">This method can return one of these values.</span></span>



| <span data-ttu-id="c099c-122">Wert</span><span class="sxs-lookup"><span data-stu-id="c099c-122">Value</span></span>                                                                                        | <span data-ttu-id="c099c-123">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c099c-123">Description</span></span>                                    |
|----------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <span data-ttu-id="c099c-124"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="c099c-124"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="c099c-125">Die Methode war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="c099c-125">The method was successful.</span></span><br/>          |
| <dl> <span data-ttu-id="c099c-126"><dt>**E \_ invalidArg**</dt></span><span class="sxs-lookup"><span data-stu-id="c099c-126"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="c099c-127">Mindestens ein Parameter ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="c099c-127">One or more parameters are invalid.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="c099c-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c099c-128">Requirements</span></span>



| <span data-ttu-id="c099c-129">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c099c-129">Requirement</span></span> | <span data-ttu-id="c099c-130">Wert</span><span class="sxs-lookup"><span data-stu-id="c099c-130">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c099c-131">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c099c-131">Minimum supported client</span></span><br/> | <span data-ttu-id="c099c-132">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c099c-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="c099c-133">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c099c-133">Minimum supported server</span></span><br/> | <span data-ttu-id="c099c-134">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c099c-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="c099c-135">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="c099c-135">Redistributable</span></span><br/>          | <span data-ttu-id="c099c-136">TSF 1,0 unter Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="c099c-136">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                        |
| <span data-ttu-id="c099c-137">Header</span><span class="sxs-lookup"><span data-stu-id="c099c-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="c099c-138"><dt>Software-Domänen Controller. h</dt></span><span class="sxs-lookup"><span data-stu-id="c099c-138"><dt>Softkbdc.h</dt></span></span> </dl>  |
| <span data-ttu-id="c099c-139">IDL</span><span class="sxs-lookup"><span data-stu-id="c099c-139">IDL</span></span><br/>                      | <dl> <span data-ttu-id="c099c-140"><dt>Software. idl</dt></span><span class="sxs-lookup"><span data-stu-id="c099c-140"><dt>Softkbd.idl</dt></span></span> </dl> |
| <span data-ttu-id="c099c-141">DLL</span><span class="sxs-lookup"><span data-stu-id="c099c-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c099c-142"><dt>Softkbd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c099c-142"><dt>Softkbd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c099c-143">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c099c-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c099c-144">**Iweichkbd**</span><span class="sxs-lookup"><span data-stu-id="c099c-144">**ISoftKbd**</span></span>](isoftkbd.md)
</dt> <dt>

[<span data-ttu-id="c099c-145">**Iweichkbd:: unadvisesoftkeyboarabventsink**</span><span class="sxs-lookup"><span data-stu-id="c099c-145">**ISoftKbd::UnadviseSoftKeyboardEventSink**</span></span>](isoftkbd-unadvisesoftkeyboardeventsink.md)
</dt> </dl>

 

