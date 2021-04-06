---
title: Logfiles. Remove-Methode
description: Entfernt die angegebene logfileitem-Instanz aus der Auflistung.
ms.assetid: d2885ffd-5957-472c-9a67-2f1469d9b48b
keywords:
- Remove-Methode (Sysmon)
- Remove-Methode (Sysmon), Logfiles-Klasse
- Logfiles-Klasse sysmon, Remove-Methode
topic_type:
- apiref
api_name:
- LogFiles.Remove
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 057607c57db600ca7a28c8a5bb6d75d5570829cb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742936"
---
# <a name="logfilesremove-method"></a><span data-ttu-id="69ef5-106">Logfiles. Remove-Methode</span><span class="sxs-lookup"><span data-stu-id="69ef5-106">LogFiles.Remove method</span></span>

<span data-ttu-id="69ef5-107">Entfernt die angegebene [**logfileitem**](logfileitem.md) -Instanz aus der Auflistung.</span><span class="sxs-lookup"><span data-stu-id="69ef5-107">Removes the specified [**LogFileItem**](logfileitem.md) instance from the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="69ef5-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="69ef5-108">Syntax</span></span>


```VB
LogFiles.Remove( _
  ByVal index As Object _
)
```



## <a name="parameters"></a><span data-ttu-id="69ef5-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="69ef5-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="69ef5-110">*Index* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="69ef5-110">*index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="69ef5-111">Ganzzahliger Index der Protokolldatei, der aus der Auflistung entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="69ef5-111">Integer index of the log file to remove from the collection.</span></span> <span data-ttu-id="69ef5-112">Der Index ist 1-basiert.</span><span class="sxs-lookup"><span data-stu-id="69ef5-112">The index is one-based.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="69ef5-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="69ef5-113">Return value</span></span>

<span data-ttu-id="69ef5-114">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="69ef5-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="69ef5-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="69ef5-115">Remarks</span></span>

<span data-ttu-id="69ef5-116">**Vor Windows Vista:** Sie können Protokolldateien nicht aus der [**Protokolldatei Sammlung**](systemmonitor-logfiles.md) entfernen, wenn der Wert von [**Systemmonitor. DataSourceType**](systemmonitor-datasourcetype.md) auf sysmonlogfiles festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="69ef5-116">**Prior to Windows Vista:** You cannot remove log files from the [**log file collection**](systemmonitor-logfiles.md) if the value of [**SystemMonitor.DataSourceType**](systemmonitor-datasourcetype.md) is set to sysmonLogFiles.</span></span>

## <a name="requirements"></a><span data-ttu-id="69ef5-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="69ef5-117">Requirements</span></span>



| <span data-ttu-id="69ef5-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="69ef5-118">Requirement</span></span> | <span data-ttu-id="69ef5-119">Wert</span><span class="sxs-lookup"><span data-stu-id="69ef5-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="69ef5-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="69ef5-120">Minimum supported client</span></span><br/> | <span data-ttu-id="69ef5-121">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="69ef5-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="69ef5-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="69ef5-122">Minimum supported server</span></span><br/> | <span data-ttu-id="69ef5-123">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="69ef5-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="69ef5-124">DLL</span><span class="sxs-lookup"><span data-stu-id="69ef5-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="69ef5-125"><dt>Sysmon. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="69ef5-125"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="69ef5-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="69ef5-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="69ef5-127">LogFiles</span><span class="sxs-lookup"><span data-stu-id="69ef5-127">LogFiles</span></span>](logfiles.md)
</dt> <dt>

[<span data-ttu-id="69ef5-128">**Logfileitem**</span><span class="sxs-lookup"><span data-stu-id="69ef5-128">**LogFileItem**</span></span>](logfileitem.md)
</dt> <dt>

[<span data-ttu-id="69ef5-129">**LogFiles**</span><span class="sxs-lookup"><span data-stu-id="69ef5-129">**LogFiles**</span></span>](systemmonitor-logfiles.md)
</dt> </dl>

 

 





