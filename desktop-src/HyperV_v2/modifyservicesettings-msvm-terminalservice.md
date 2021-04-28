---
description: ModifyServiceSettings-Methode der Msvm_TerminalService - Ändert die Einstellungsdaten für den Dienst.
ms.assetid: 76669180-fa95-4d6e-b89a-53e45da664c4
title: ModifyServiceSettings-Methode der Msvm_TerminalService Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_TerminalService.ModifyServiceSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 930b29c5c07c755b493a0aabad88ae776c0803e0
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108119328"
---
# <a name="modifyservicesettings-method-of-the-msvm_terminalservice-class"></a><span data-ttu-id="ad676-103">ModifyServiceSettings-Methode der Msvm \_ TerminalService-Klasse</span><span class="sxs-lookup"><span data-stu-id="ad676-103">ModifyServiceSettings method of the Msvm\_TerminalService class</span></span>

<span data-ttu-id="ad676-104">Ändert die Einstellungsdaten für den Dienst.</span><span class="sxs-lookup"><span data-stu-id="ad676-104">Modifies the setting data for the service.</span></span>

## <a name="syntax"></a><span data-ttu-id="ad676-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="ad676-105">Syntax</span></span>


```mof
uint32 ModifyServiceSettings(
  [in]  string              ServiceSettingData,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="ad676-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="ad676-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ad676-107">*ServiceSettingData* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="ad676-107">*ServiceSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ad676-108">Eine Zeichenfolgendarstellung der [**Msvm \_ TerminalServiceSettingData-Klasse,**](msvm-terminalservicesettingdata.md) die die geänderten Einstellungsdaten für den Dienst enthält.</span><span class="sxs-lookup"><span data-stu-id="ad676-108">A string representation of the [**Msvm\_TerminalServiceSettingData**](msvm-terminalservicesettingdata.md) class that contains the modified setting data for the service.</span></span>

</dd> <dt>

<span data-ttu-id="ad676-109">*Auftrag* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="ad676-109">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ad676-110">Wenn der Vorgang asynchron ausgeführt wird, gibt diese Methode 4096 zurück, und dieser Parameter enthält einen Verweis auf ein Objekt, das von [**CIM \_ ConcreteJob abgeleitet wurde.**](/previous-versions//cc136808(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="ad676-110">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ad676-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ad676-111">Return value</span></span>

<span data-ttu-id="ad676-112">Diese Methode gibt einen der folgenden Werte zurück.</span><span class="sxs-lookup"><span data-stu-id="ad676-112">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="ad676-113">**Abgeschlossen ohne Fehler** (0)</span><span class="sxs-lookup"><span data-stu-id="ad676-113">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="ad676-114">**Überprüfte Methodenparameter – Auftrag gestartet** (4096)</span><span class="sxs-lookup"><span data-stu-id="ad676-114">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="ad676-115">**Fehler** (32768)</span><span class="sxs-lookup"><span data-stu-id="ad676-115">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="ad676-116">**Zugriff verweigert** (32769)</span><span class="sxs-lookup"><span data-stu-id="ad676-116">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="ad676-117">**Nicht unterstützt** (32770)</span><span class="sxs-lookup"><span data-stu-id="ad676-117">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="ad676-118">**Status ist unbekannt** (32771)</span><span class="sxs-lookup"><span data-stu-id="ad676-118">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="ad676-119">**Timeout** (32772)</span><span class="sxs-lookup"><span data-stu-id="ad676-119">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="ad676-120">**Ungültiger** Parameter (32773)</span><span class="sxs-lookup"><span data-stu-id="ad676-120">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="ad676-121">**System wird verwendet** (32774)</span><span class="sxs-lookup"><span data-stu-id="ad676-121">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="ad676-122">**Ungültiger Zustand für diesen Vorgang** (32775)</span><span class="sxs-lookup"><span data-stu-id="ad676-122">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="ad676-123">**Falscher Datentyp** (32776)</span><span class="sxs-lookup"><span data-stu-id="ad676-123">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="ad676-124">**System ist nicht verfügbar** (32777)</span><span class="sxs-lookup"><span data-stu-id="ad676-124">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="ad676-125">**Nicht genügend Arbeitsspeicher** (32778)</span><span class="sxs-lookup"><span data-stu-id="ad676-125">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="ad676-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ad676-126">Requirements</span></span>



| <span data-ttu-id="ad676-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ad676-127">Requirement</span></span> | <span data-ttu-id="ad676-128">Wert</span><span class="sxs-lookup"><span data-stu-id="ad676-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ad676-129">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ad676-129">Minimum supported client</span></span><br/> | <span data-ttu-id="ad676-130">nur Windows 8 \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ad676-130">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="ad676-131">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ad676-131">Minimum supported server</span></span><br/> | <span data-ttu-id="ad676-132">Nur Windows Server \[ 2012-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ad676-132">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="ad676-133">Namespace</span><span class="sxs-lookup"><span data-stu-id="ad676-133">Namespace</span></span><br/>                | <span data-ttu-id="ad676-134">Root \\ Virtualization \\ V2</span><span class="sxs-lookup"><span data-stu-id="ad676-134">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="ad676-135">MOF</span><span class="sxs-lookup"><span data-stu-id="ad676-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ad676-136"><dt>WindowsVirtualization.V2.mof</dt></span><span class="sxs-lookup"><span data-stu-id="ad676-136"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="ad676-137">DLL</span><span class="sxs-lookup"><span data-stu-id="ad676-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ad676-138"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="ad676-138"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="ad676-139">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="ad676-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ad676-140">**Msvm \_ TerminalService**</span><span class="sxs-lookup"><span data-stu-id="ad676-140">**Msvm\_TerminalService**</span></span>](msvm-terminalservice.md)
</dt> </dl>

 

