---
title: Methode "undvtaskplugin Initialize"
description: Wird aufgerufen, um den Task-Agent zu initialisieren.
ms.assetid: eef813e6-ecca-400a-a9f3-efca6bd81161
ms.tgt_platform: multiple
keywords:
- Initialize-Methode Remotedesktopdienste
- Initialize-Methode Remotedesktopdienste, undvtaskplugin-Schnittstelle
- Undvtaskplugin-Schnittstelle Remotedesktopdienste, Initialize-Methode
topic_type:
- apiref
api_name:
- IRDVTaskPlugin.Initialize
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9530be7334e1f3fefa7f73007334e448362a95ed
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391661"
---
# <a name="irdvtaskplugininitialize-method"></a><span data-ttu-id="f5353-106">Undvtaskplugin:: Initialize-Methode</span><span class="sxs-lookup"><span data-stu-id="f5353-106">IRDVTaskPlugin::Initialize method</span></span>

<span data-ttu-id="f5353-107">Wird aufgerufen, um den Task-Agent zu initialisieren.</span><span class="sxs-lookup"><span data-stu-id="f5353-107">Called to initialize the task agent.</span></span>

## <a name="syntax"></a><span data-ttu-id="f5353-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="f5353-108">Syntax</span></span>


```C++
HRESULT Initialize(
  [in] IRDVTaskPluginNotifySink *pNotifySink
);
```



## <a name="parameters"></a><span data-ttu-id="f5353-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="f5353-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f5353-110">*pnotifysink* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f5353-110">*pNotifySink* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f5353-111">Geben Sie Folgendes ein: \**[**undvtaskpluginnotifysink**](irdvtaskpluginnotifysink.md) \** _</span><span class="sxs-lookup"><span data-stu-id="f5353-111">Type: \**[**IRDVTaskPluginNotifySink**](irdvtaskpluginnotifysink.md)\** _</span></span>

<span data-ttu-id="f5353-112">Ein Zeiger auf eine [_ *undvtaskpluginnotifysink* \*](irdvtaskpluginnotifysink.md) -Schnittstelle, die der Task-Agent für die Kommunikation mit dem Auslöse-Agent verwendet.</span><span class="sxs-lookup"><span data-stu-id="f5353-112">A pointer to an [_ *IRDVTaskPluginNotifySink*\*](irdvtaskpluginnotifysink.md) interface that the task agent uses to communicate with the trigger agent.</span></span> <span data-ttu-id="f5353-113">Sie müssen diese Schnittstelle freigeben, wenn Sie nicht mehr benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="f5353-113">You must release this interface when it is no longer needed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f5353-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f5353-114">Return value</span></span>

<span data-ttu-id="f5353-115">Typ: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="f5353-115">Type: **HRESULT**</span></span>

<span data-ttu-id="f5353-116">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="f5353-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="f5353-117">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="f5353-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="f5353-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f5353-118">Requirements</span></span>



| <span data-ttu-id="f5353-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f5353-119">Requirement</span></span> | <span data-ttu-id="f5353-120">Wert</span><span class="sxs-lookup"><span data-stu-id="f5353-120">Value</span></span> |
|-------------------------------------|-----------------------------------|
| <span data-ttu-id="f5353-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f5353-121">Minimum supported client</span></span><br/> | <span data-ttu-id="f5353-122">Windows 7 Enterprise</span><span class="sxs-lookup"><span data-stu-id="f5353-122">Windows 7 Enterprise</span></span><br/>   |
| <span data-ttu-id="f5353-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f5353-123">Minimum supported server</span></span><br/> | <span data-ttu-id="f5353-124">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="f5353-124">Windows Server 2008 R2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f5353-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f5353-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f5353-126">**"Undvtaskplugin"**</span><span class="sxs-lookup"><span data-stu-id="f5353-126">**IRDVTaskPlugin**</span></span>](irdvtaskplugin.md)
</dt> </dl>

 

 





