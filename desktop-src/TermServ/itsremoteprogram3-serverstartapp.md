---
title: ITSRemoteProgram3 serverstartapp-Methode
description: Gibt eine APP an, die in der Remote Sitzung gestartet werden soll.
ms.assetid: 55a05d05-66d5-48a1-b3a6-f087aeb62925
ms.tgt_platform: multiple
keywords:
- Serverstartapp-Methode Remotedesktopdienste
- Serverstartapp-Methode Remotedesktopdienste, ITSRemoteProgram3-Schnittstelle
- ITSRemoteProgram3 Interface Remotedesktopdienste, serverstartapp-Methode
topic_type:
- apiref
api_name:
- ITSRemoteProgram3.ServerStartApp
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ef1822fa98094870ebebe607528cdc69a8a201f5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106343881"
---
# <a name="itsremoteprogram3serverstartapp-method"></a><span data-ttu-id="0835a-106">ITSRemoteProgram3:: serverstartapp-Methode</span><span class="sxs-lookup"><span data-stu-id="0835a-106">ITSRemoteProgram3::ServerStartApp method</span></span>

<span data-ttu-id="0835a-107">Gibt eine APP an, die in der Remote Sitzung gestartet werden soll.</span><span class="sxs-lookup"><span data-stu-id="0835a-107">Specifies an App to start in the remote session.</span></span>

## <a name="syntax"></a><span data-ttu-id="0835a-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="0835a-108">Syntax</span></span>


```C++
HRESULT ServerStartApp(
  [in] BSTR         bstrAppUserModelId,
  [in] BSTR         bstrArguments,
  [in] VARIANT_BOOL vbExpandEnvVarInArgumentsOnServer
);
```



## <a name="parameters"></a><span data-ttu-id="0835a-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="0835a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0835a-110">*bstrappusermodelid* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0835a-110">*bstrAppUserModelId* \[in\]</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="0835a-111">*bstrauarguments* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0835a-111">*bstrArguments* \[in\]</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="0835a-112">*vbexpandeinvvarinargumentsonserver* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0835a-112">*vbExpandEnvVarInArgumentsOnServer* \[in\]</span></span>
<span data-ttu-id="0835a-113"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="0835a-113"></dt> <dd></dd> </dl></span></span>

## <a name="return-value"></a><span data-ttu-id="0835a-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0835a-114">Return value</span></span>

<span data-ttu-id="0835a-115">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="0835a-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="0835a-116">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="0835a-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="0835a-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0835a-117">Requirements</span></span>



| <span data-ttu-id="0835a-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0835a-118">Requirement</span></span> | <span data-ttu-id="0835a-119">Wert</span><span class="sxs-lookup"><span data-stu-id="0835a-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0835a-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0835a-120">Minimum supported client</span></span><br/> | <span data-ttu-id="0835a-121">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0835a-121">Windows 10 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="0835a-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0835a-122">Minimum supported server</span></span><br/> | <span data-ttu-id="0835a-123">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="0835a-123">Windows Server 2016</span></span><br/>                                                         |
| <span data-ttu-id="0835a-124">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="0835a-124">Type library</span></span><br/>             | <dl> <span data-ttu-id="0835a-125"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0835a-125"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="0835a-126">DLL</span><span class="sxs-lookup"><span data-stu-id="0835a-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0835a-127"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0835a-127"><dt>MsTscAx.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0835a-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0835a-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0835a-129">**ITSRemoteProgram3**</span><span class="sxs-lookup"><span data-stu-id="0835a-129">**ITSRemoteProgram3**</span></span>](itsremoteprogram3.md)
</dt> </dl>

 

 





