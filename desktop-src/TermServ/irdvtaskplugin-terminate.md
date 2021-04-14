---
title: Undvtaskplugin-Beendigungs Methode
description: Wird aufgerufen, wenn der Task-Agent heruntergefahren wird.
ms.assetid: b693a318-1da7-4207-8046-a62b7ccca471
ms.tgt_platform: multiple
keywords:
- Beendigungs Methode Remotedesktopdienste
- Methode Remotedesktopdienste beenden, Schnittstelle "iridvtaskplugin"
- Undvtaskplugin-Schnittstelle Remotedesktopdienste, Methode beenden
topic_type:
- apiref
api_name:
- IRDVTaskPlugin.Terminate
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 178f0a7c054169d972acb6b60a9cc80578fd13e9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104392019"
---
# <a name="irdvtaskpluginterminate-method"></a><span data-ttu-id="3f28f-106">Undvtaskplugin:: End-Methode</span><span class="sxs-lookup"><span data-stu-id="3f28f-106">IRDVTaskPlugin::Terminate method</span></span>

<span data-ttu-id="3f28f-107">Wird aufgerufen, wenn der Task-Agent heruntergefahren wird.</span><span class="sxs-lookup"><span data-stu-id="3f28f-107">Called when the task agent is being shut down.</span></span>

## <a name="syntax"></a><span data-ttu-id="3f28f-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="3f28f-108">Syntax</span></span>


```C++
HRESULT Terminate(
  [in] HRESULT hr
);
```



## <a name="parameters"></a><span data-ttu-id="3f28f-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="3f28f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3f28f-110">*Personalabteilung* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3f28f-110">*hr* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3f28f-111">Gibt an, ob das Herunterfahren auf ein normales Herunterfahren oder einen Fehler zurückzuführen ist.</span><span class="sxs-lookup"><span data-stu-id="3f28f-111">Indicates whether the shut down is due to a normal shut down or a failure.</span></span> <span data-ttu-id="3f28f-112">Wenn das Herunterfahren normal ist, enthält dies **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="3f28f-112">If the shut down is normal, this contains **S\_OK**.</span></span> <span data-ttu-id="3f28f-113">Andernfalls enthält Sie einen **HRESULT** -Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="3f28f-113">Otherwise, it contains an **HRESULT** error code.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3f28f-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3f28f-114">Return value</span></span>

<span data-ttu-id="3f28f-115">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="3f28f-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="3f28f-116">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="3f28f-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="3f28f-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3f28f-117">Requirements</span></span>



| <span data-ttu-id="3f28f-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3f28f-118">Requirement</span></span> | <span data-ttu-id="3f28f-119">Wert</span><span class="sxs-lookup"><span data-stu-id="3f28f-119">Value</span></span> |
|-------------------------------------|-----------------------------------|
| <span data-ttu-id="3f28f-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="3f28f-120">Minimum supported client</span></span><br/> | <span data-ttu-id="3f28f-121">Windows 7 Enterprise</span><span class="sxs-lookup"><span data-stu-id="3f28f-121">Windows 7 Enterprise</span></span><br/>   |
| <span data-ttu-id="3f28f-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="3f28f-122">Minimum supported server</span></span><br/> | <span data-ttu-id="3f28f-123">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="3f28f-123">Windows Server 2008 R2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="3f28f-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3f28f-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3f28f-125">**"Undvtaskplugin"**</span><span class="sxs-lookup"><span data-stu-id="3f28f-125">**IRDVTaskPlugin**</span></span>](irdvtaskplugin.md)
</dt> </dl>

 

 





