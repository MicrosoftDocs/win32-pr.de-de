---
title: Undvtaskpluginnotifysink onbeendete-Methode (sbtsv. h)
description: Wird vom Task-Agent aufgerufen, um anzufordern, dass der Task-Agent heruntergefahren wird.
ms.assetid: 163e0ce5-f4ee-4242-bdbb-977c5ede3451
ms.tgt_platform: multiple
keywords:
- Onbeendete-Methode Remotedesktopdienste
- Onend-Methode Remotedesktopdienste, undvtaskpluginnotifysink-Schnittstelle
- Undvtaskpluginnotifysink-Schnittstelle Remotedesktopdienste, onend-Methode
topic_type:
- apiref
api_name:
- IRDVTaskPluginNotifySink.OnTerminated
api_location:
- sbtsv.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0b261437425b0b4dce4b2c2e17c52b6e24ea3e0e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518935"
---
# <a name="irdvtaskpluginnotifysinkonterminated-method"></a><span data-ttu-id="f5624-106">Undvtaskpluginnotifysink:: onend-Methode</span><span class="sxs-lookup"><span data-stu-id="f5624-106">IRDVTaskPluginNotifySink::OnTerminated method</span></span>

<span data-ttu-id="f5624-107">Wird vom Task-Agent aufgerufen, um anzufordern, dass der Task-Agent heruntergefahren wird.</span><span class="sxs-lookup"><span data-stu-id="f5624-107">Called by the task agent to request that the task agent be shut down.</span></span>

## <a name="syntax"></a><span data-ttu-id="f5624-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="f5624-108">Syntax</span></span>


```C++
HRESULT OnTerminated(
  [in] HRESULT hr
);
```



## <a name="parameters"></a><span data-ttu-id="f5624-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="f5624-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f5624-110">*Personalabteilung* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f5624-110">*hr* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f5624-111">Gibt an, ob das Herunterfahren auf ein normales Herunterfahren oder einen Fehler zurückzuführen ist.</span><span class="sxs-lookup"><span data-stu-id="f5624-111">Indicates if the shut down is due to a normal shut down or a failure.</span></span> <span data-ttu-id="f5624-112">Wenn das Herunterfahren normal ist, enthält dies **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="f5624-112">If the shut down is normal, this contains **S\_OK**.</span></span> <span data-ttu-id="f5624-113">Andernfalls enthält Sie einen **HRESULT** -Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="f5624-113">Otherwise, it contains an **HRESULT** error code.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f5624-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f5624-114">Return value</span></span>

<span data-ttu-id="f5624-115">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="f5624-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="f5624-116">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="f5624-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="f5624-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f5624-117">Requirements</span></span>



| <span data-ttu-id="f5624-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f5624-118">Requirement</span></span> | <span data-ttu-id="f5624-119">Wert</span><span class="sxs-lookup"><span data-stu-id="f5624-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="f5624-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f5624-120">Minimum supported client</span></span><br/> | <span data-ttu-id="f5624-121">Windows 7 Enterprise</span><span class="sxs-lookup"><span data-stu-id="f5624-121">Windows 7 Enterprise</span></span><br/>                                                    |
| <span data-ttu-id="f5624-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f5624-122">Minimum supported server</span></span><br/> | <span data-ttu-id="f5624-123">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="f5624-123">Windows Server 2008 R2</span></span><br/>                                                  |
| <span data-ttu-id="f5624-124">Header</span><span class="sxs-lookup"><span data-stu-id="f5624-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="f5624-125"><dt>Sbtsv. h</dt></span><span class="sxs-lookup"><span data-stu-id="f5624-125"><dt>Sbtsv.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f5624-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f5624-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f5624-127">**"Undvtaskpluginnotifysink"**</span><span class="sxs-lookup"><span data-stu-id="f5624-127">**IRDVTaskPluginNotifySink**</span></span>](irdvtaskpluginnotifysink.md)
</dt> </dl>

 

 





