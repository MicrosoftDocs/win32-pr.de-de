---
title: INapComponentConfig3 deleteallconfig-Methode (napcommon. h)
description: Wird von System Integritätsprüfungen (SHVs) implementiert, um den SHV-Speicher nach dem Setup in seinen ursprünglichen Zustand zurückzusetzen.
ms.assetid: 7f079743-1c32-430d-a250-b49a96b99f14
keywords:
- Deleteallconfig-Methode NAP
- Deleteallconfig-Methode, NAP, INapComponentConfig3-Schnittstelle
- INapComponentConfig3 Interface NAP, deleteallconfig-Methode
topic_type:
- apiref
api_name:
- INapComponentConfig3.DeleteAllConfig
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 12a766690114db20fb9be5cccbd4508f4565f2cf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103858776"
---
# <a name="inapcomponentconfig3deleteallconfig-method"></a><span data-ttu-id="a9f39-106">INapComponentConfig3::D eleteallconfig-Methode</span><span class="sxs-lookup"><span data-stu-id="a9f39-106">INapComponentConfig3::DeleteAllConfig method</span></span>

> [!Note]  
> <span data-ttu-id="a9f39-107">Die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="a9f39-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="a9f39-108">Die **deleteallconfig** -Methode wird von System Integritätsprüfungen (SHVs) implementiert, um eine Möglichkeit zu bieten, den SHV-Speicher nach dem Setup in seinen ursprünglichen Zustand zurückzusetzen.</span><span class="sxs-lookup"><span data-stu-id="a9f39-108">The **DeleteAllConfig** method is implemented by system health validators (SHVs) to provide a way to reset the SHV store to its original state after setup.</span></span> <span data-ttu-id="a9f39-109">Alle Konfigurationsdaten außer der Standardkonfiguration müssen gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="a9f39-109">All configuration data except for the default configuration must be deleted.</span></span>

## <a name="syntax"></a><span data-ttu-id="a9f39-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="a9f39-110">Syntax</span></span>


```C++
HRESULT DeleteAllConfig();
```



## <a name="parameters"></a><span data-ttu-id="a9f39-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="a9f39-111">Parameters</span></span>

<span data-ttu-id="a9f39-112">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="a9f39-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="a9f39-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a9f39-113">Return value</span></span>

<span data-ttu-id="a9f39-114">Gibt basierend auf dem Ergebnis dieses Vorgangs einen der folgenden Fehlercodes zurück.</span><span class="sxs-lookup"><span data-stu-id="a9f39-114">Returns one of the following error codes based on the result of this operation.</span></span>



| <span data-ttu-id="a9f39-115">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="a9f39-115">Return code</span></span>                                                                           | <span data-ttu-id="a9f39-116">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a9f39-116">Description</span></span>                             |
|---------------------------------------------------------------------------------------|-----------------------------------------|
| <dl> <span data-ttu-id="a9f39-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="a9f39-117"><dt>**S\_OK** </dt></span></span> </dl> | <span data-ttu-id="a9f39-118">Der Vorgang ist erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="a9f39-118">The operation is successful.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="a9f39-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a9f39-119">Requirements</span></span>



| <span data-ttu-id="a9f39-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a9f39-120">Requirement</span></span> | <span data-ttu-id="a9f39-121">Wert</span><span class="sxs-lookup"><span data-stu-id="a9f39-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="a9f39-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a9f39-122">Minimum supported client</span></span><br/> | <span data-ttu-id="a9f39-123">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="a9f39-123">None supported</span></span><br/>                                                                |
| <span data-ttu-id="a9f39-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a9f39-124">Minimum supported server</span></span><br/> | <span data-ttu-id="a9f39-125">Nur Windows Server 2008 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a9f39-125">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a9f39-126">Header</span><span class="sxs-lookup"><span data-stu-id="a9f39-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="a9f39-127"><dt>Napcommon. h</dt></span><span class="sxs-lookup"><span data-stu-id="a9f39-127"><dt>NapCommon.h</dt></span></span> </dl>   |
| <span data-ttu-id="a9f39-128">IDL</span><span class="sxs-lookup"><span data-stu-id="a9f39-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="a9f39-129"><dt>Napcommon. idl</dt></span><span class="sxs-lookup"><span data-stu-id="a9f39-129"><dt>NapCommon.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a9f39-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a9f39-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a9f39-131">**INapComponentConfig3**</span><span class="sxs-lookup"><span data-stu-id="a9f39-131">**INapComponentConfig3**</span></span>](inapcomponentconfig3.md)
</dt> </dl>

 

 





