---
description: Ruft die Bibliothek auf, um zu überprüfen, ob eine bestimmte CLSID sicher aufgerufen werden kann.
ms.assetid: 94C8731B-88FD-4240-BF5D-2CD67C41B063
title: Wldpisclassinapprovedlist-Funktion (wldp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WldpIsClassInApprovedList
api_type:
- DllExport
api_location:
- wldp.dll
ms.openlocfilehash: 01762c60a3f1aef1574cc218ace9988669175efe
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104125857"
---
# <a name="wldpisclassinapprovedlist-function"></a><span data-ttu-id="a2c93-103">Wldpisclassinapprovedlist-Funktion</span><span class="sxs-lookup"><span data-stu-id="a2c93-103">WldpIsClassInApprovedList function</span></span>

<span data-ttu-id="a2c93-104">Ruft die Bibliothek auf, um zu überprüfen, ob eine bestimmte **CLSID** sicher aufgerufen werden kann.</span><span class="sxs-lookup"><span data-stu-id="a2c93-104">Calls the library to validate if a particular **CLSID** is safe to be called.</span></span> <span data-ttu-id="a2c93-105">Die Funktion verfügt über keine zugeordnete Import Bibliothek.</span><span class="sxs-lookup"><span data-stu-id="a2c93-105">The function has no associated import library.</span></span> <span data-ttu-id="a2c93-106">Sie müssen die LoadLibrary-Funktion und die GetProcAddress-Funktion verwenden, um dynamisch mit wldp.dll zu verknüpfen.</span><span class="sxs-lookup"><span data-stu-id="a2c93-106">You must use the LoadLibrary and GetProcAddress functions to dynamically link to wldp.dll.</span></span>

## <a name="syntax"></a><span data-ttu-id="a2c93-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="a2c93-107">Syntax</span></span>


```C++
HRESULT WINAPI WldpIsClassInApprovedList(
        REFCLSID               classID,
  _In_  PWLDP_HOST_INFORMATION hostInformation,
  _Out_ PBOOL                  isApproved,
        DWORD                  optionalFlags
);
```



## <a name="parameters"></a><span data-ttu-id="a2c93-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="a2c93-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a2c93-109">*ClassID*</span><span class="sxs-lookup"><span data-stu-id="a2c93-109">*classID*</span></span> 
</dt> <dd>

<span data-ttu-id="a2c93-110">Die com-Klassen-ID, die auf Genehmigung überprüft werden soll.</span><span class="sxs-lookup"><span data-stu-id="a2c93-110">The COM class ID to check for approval.</span></span>

</dd> <dt>

<span data-ttu-id="a2c93-111">*Hostinformationen* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a2c93-111">*hostInformation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a2c93-112">Eine [**wldp- \_ Host \_ Informations**](wldp-host-information.md) Struktur, die den zu bewertenden Host identifiziert.</span><span class="sxs-lookup"><span data-stu-id="a2c93-112">A [**WLDP\_HOST\_INFORMATION**](wldp-host-information.md) structure identifying the host to be evaluated.</span></span>

</dd> <dt>

<span data-ttu-id="a2c93-113">*IsApproved* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="a2c93-113">*isApproved* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a2c93-114">Nach erfolgreichem Abschluss enthält **true** , wenn die Klassen-ID genehmigt ist. andernfalls **false**.</span><span class="sxs-lookup"><span data-stu-id="a2c93-114">On successful completion, contains **TRUE** if the class ID is approved; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="a2c93-115">*optionalflags*</span><span class="sxs-lookup"><span data-stu-id="a2c93-115">*optionalFlags*</span></span> 
</dt> <dd>

<span data-ttu-id="a2c93-116">Dieser Parameter ist reserviert und muss auf 0 (null) festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="a2c93-116">This parameter is reserved and must be set to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a2c93-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a2c93-117">Return value</span></span>

<span data-ttu-id="a2c93-118">Diese Methode gibt bei Erfolg **S \_ OK** zurück oder andernfalls einen Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="a2c93-118">This method returns **S\_OK** if successful or a failure code otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="a2c93-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a2c93-119">Requirements</span></span>



| <span data-ttu-id="a2c93-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a2c93-120">Requirement</span></span> | <span data-ttu-id="a2c93-121">Wert</span><span class="sxs-lookup"><span data-stu-id="a2c93-121">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="a2c93-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a2c93-122">Minimum supported client</span></span><br/> | <span data-ttu-id="a2c93-123">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a2c93-123">Windows 10 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="a2c93-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a2c93-124">Minimum supported server</span></span><br/> | <span data-ttu-id="a2c93-125">Nur Windows Server 2016 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a2c93-125">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="a2c93-126">Header</span><span class="sxs-lookup"><span data-stu-id="a2c93-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="a2c93-127"><dt>Wldp. h</dt></span><span class="sxs-lookup"><span data-stu-id="a2c93-127"><dt>Wldp.h</dt></span></span> </dl>   |
| <span data-ttu-id="a2c93-128">DLL</span><span class="sxs-lookup"><span data-stu-id="a2c93-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a2c93-129"><dt>Wldp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a2c93-129"><dt>Wldp.dll</dt></span></span> </dl> |



 

 




