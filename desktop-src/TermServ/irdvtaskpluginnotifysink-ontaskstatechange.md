---
title: Undvtaskpluginnotifysink ontaskstatechange-Methode
description: Wird verwendet, um den Agent zu benachrichtigen, dass sich der Zustand einer Aufgabe geändert hat.
ms.assetid: 3021ea7a-2627-48d1-8df5-c40e7a9b51c5
ms.tgt_platform: multiple
keywords:
- Ontaskstatechange-Methode Remotedesktopdienste
- Ontaskstatechange-Methode Remotedesktopdienste, undvtaskpluginnotifysink-Schnittstelle
- Undvtaskpluginnotifysink-Schnittstelle Remotedesktopdienste, ontaskstatechange-Methode
topic_type:
- apiref
api_name:
- IRDVTaskPluginNotifySink.OnTaskStateChange
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c3e3acf1a2d47b1721ef90554f7a11714c02e6df
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106342667"
---
# <a name="irdvtaskpluginnotifysinkontaskstatechange-method"></a><span data-ttu-id="f500d-106">Undvtaskpluginnotifysink:: ontaskstatechange-Methode</span><span class="sxs-lookup"><span data-stu-id="f500d-106">IRDVTaskPluginNotifySink::OnTaskStateChange method</span></span>

<span data-ttu-id="f500d-107">Wird verwendet, um den Agent zu benachrichtigen, dass sich der Zustand einer Aufgabe geändert hat.</span><span class="sxs-lookup"><span data-stu-id="f500d-107">Used to notify the trigger agent that the state of a task has changed.</span></span>

## <a name="syntax"></a><span data-ttu-id="f500d-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="f500d-108">Syntax</span></span>


```C++
HRESULT OnTaskStateChange(
  [in] BSTR            bstrIdentifier,
  [in] RDV_TASK_STATUS status
);
```



## <a name="parameters"></a><span data-ttu-id="f500d-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="f500d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f500d-110">*bstridentifier* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f500d-110">*bstrIdentifier* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f500d-111">Typ: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="f500d-111">Type: **BSTR**</span></span>

<span data-ttu-id="f500d-112">Der Bezeichner des Tasks.</span><span class="sxs-lookup"><span data-stu-id="f500d-112">The identifier of the task.</span></span> <span data-ttu-id="f500d-113">Dies ist der Bezeichner, der an die [**Starttask**](irdvtaskplugin-starttask.md) -Methode übermittelt wird.</span><span class="sxs-lookup"><span data-stu-id="f500d-113">This is the identifier passed to the [**StartTask**](irdvtaskplugin-starttask.md) method.</span></span>

</dd> <dt>

<span data-ttu-id="f500d-114">*Status* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f500d-114">*status* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f500d-115">Typ: **[ **RDV- \_ Task \_ Status**](/windows/desktop/api/SessDirPublicTypes/ne-sessdirpublictypes-rdv_task_status)**</span><span class="sxs-lookup"><span data-stu-id="f500d-115">Type: **[**RDV\_TASK\_STATUS**](/windows/desktop/api/SessDirPublicTypes/ne-sessdirpublictypes-rdv_task_status)**</span></span>

<span data-ttu-id="f500d-116">Ein Wert der [**RDV- \_ aufgabenstatusenumeration \_**](/windows/desktop/api/SessDirPublicTypes/ne-sessdirpublictypes-rdv_task_status) , die den neuen Zustand der Aufgabe angibt.</span><span class="sxs-lookup"><span data-stu-id="f500d-116">A value of the [**RDV\_TASK\_STATUS**](/windows/desktop/api/SessDirPublicTypes/ne-sessdirpublictypes-rdv_task_status) enumeration that specifies the new state of the task.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f500d-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f500d-117">Return value</span></span>

<span data-ttu-id="f500d-118">Typ: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="f500d-118">Type: **HRESULT**</span></span>

<span data-ttu-id="f500d-119">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="f500d-119">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="f500d-120">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="f500d-120">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="f500d-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f500d-121">Requirements</span></span>



| <span data-ttu-id="f500d-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f500d-122">Requirement</span></span> | <span data-ttu-id="f500d-123">Wert</span><span class="sxs-lookup"><span data-stu-id="f500d-123">Value</span></span> |
|-------------------------------------|-----------------------------------|
| <span data-ttu-id="f500d-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f500d-124">Minimum supported client</span></span><br/> | <span data-ttu-id="f500d-125">Windows 7 Enterprise</span><span class="sxs-lookup"><span data-stu-id="f500d-125">Windows 7 Enterprise</span></span><br/>   |
| <span data-ttu-id="f500d-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f500d-126">Minimum supported server</span></span><br/> | <span data-ttu-id="f500d-127">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="f500d-127">Windows Server 2008 R2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f500d-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f500d-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f500d-129">**RDV- \_ Task \_ Status**</span><span class="sxs-lookup"><span data-stu-id="f500d-129">**RDV\_TASK\_STATUS**</span></span>](/windows/desktop/api/SessDirPublicTypes/ne-sessdirpublictypes-rdv_task_status)
</dt> <dt>

[<span data-ttu-id="f500d-130">**"Undvtaskpluginnotifysink"**</span><span class="sxs-lookup"><span data-stu-id="f500d-130">**IRDVTaskPluginNotifySink**</span></span>](irdvtaskpluginnotifysink.md)
</dt> </dl>

 

 





