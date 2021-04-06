---
title: Imstscaxevents onservicemess agereceived-Methode
description: Wird aufgerufen, wenn der Client eine Systemmeldung empfängt.
ms.assetid: 9D230AA3-30F8-4BDF-89D6-D33AF42D0E85
ms.tgt_platform: multiple
keywords:
- Onservicemess agereceived-Methode Remotedesktopdienste
- Onservicemess agereceived-Methode Remotedesktopdienste, imstscaxevents-Schnittstelle
- Imstscaxevents-Schnittstelle Remotedesktopdienste, onservicemess agereceived-Methode
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnServiceMessageReceived
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 05a26b78fa31667fb550848d4edd7918aa2bde3e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742089"
---
# <a name="imstscaxeventsonservicemessagereceived-method"></a><span data-ttu-id="bfaab-106">Imstscaxevents:: onservicemess agereceived-Methode</span><span class="sxs-lookup"><span data-stu-id="bfaab-106">IMsTscAxEvents::OnServiceMessageReceived method</span></span>

<span data-ttu-id="bfaab-107">Wird aufgerufen, wenn der Client eine Systemmeldung empfängt.</span><span class="sxs-lookup"><span data-stu-id="bfaab-107">Called when the client receives a system message.</span></span>

## <a name="syntax"></a><span data-ttu-id="bfaab-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="bfaab-108">Syntax</span></span>


```C++
void OnServiceMessageReceived(
  [in] BSTR serviceMessage
);
```



## <a name="parameters"></a><span data-ttu-id="bfaab-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="bfaab-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bfaab-110">*servicemess* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="bfaab-110">*serviceMessage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bfaab-111">Gibt die Systemmeldung an.</span><span class="sxs-lookup"><span data-stu-id="bfaab-111">Specifies the system message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bfaab-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="bfaab-112">Return value</span></span>

<span data-ttu-id="bfaab-113">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="bfaab-113">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="bfaab-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bfaab-114">Remarks</span></span>

<span data-ttu-id="bfaab-115">Weitere Informationen zu Systemnachrichten finden Sie unter [configure Messaging for a Remotedesktop Gateway Server](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/dd834700(v=ws.11)).</span><span class="sxs-lookup"><span data-stu-id="bfaab-115">For more information about system messages, see [Configure Messaging for a Remote Desktop Gateway Server](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/dd834700(v=ws.11)).</span></span>

## <a name="requirements"></a><span data-ttu-id="bfaab-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bfaab-116">Requirements</span></span>



| <span data-ttu-id="bfaab-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="bfaab-117">Requirement</span></span> | <span data-ttu-id="bfaab-118">Wert</span><span class="sxs-lookup"><span data-stu-id="bfaab-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="bfaab-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="bfaab-119">Minimum supported client</span></span><br/> | <span data-ttu-id="bfaab-120">Windows 7</span><span class="sxs-lookup"><span data-stu-id="bfaab-120">Windows 7</span></span><br/>                                                                   |
| <span data-ttu-id="bfaab-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="bfaab-121">Minimum supported server</span></span><br/> | <span data-ttu-id="bfaab-122">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="bfaab-122">Windows Server 2008 R2</span></span><br/>                                                      |
| <span data-ttu-id="bfaab-123">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="bfaab-123">Type library</span></span><br/>             | <dl> <span data-ttu-id="bfaab-124"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bfaab-124"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="bfaab-125">DLL</span><span class="sxs-lookup"><span data-stu-id="bfaab-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bfaab-126"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bfaab-126"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="bfaab-127">IID</span><span class="sxs-lookup"><span data-stu-id="bfaab-127">IID</span></span><br/>                      | <span data-ttu-id="bfaab-128">Imstscaxevents ist als 336d5562-efa8-482e-8cb3-c5c0fc7a7db6 definiert.</span><span class="sxs-lookup"><span data-stu-id="bfaab-128">IMsTscAxEvents is defined as 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="bfaab-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bfaab-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bfaab-130">**Imstscaxevents**</span><span class="sxs-lookup"><span data-stu-id="bfaab-130">**IMsTscAxEvents**</span></span>](imstscaxevents-interface.md)
</dt> </dl>

 

