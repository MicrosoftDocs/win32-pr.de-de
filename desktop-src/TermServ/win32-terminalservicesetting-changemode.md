---
title: ChangeMode-Methode der Win32_TerminalServiceSetting-Klasse
description: Die ChangeMode-Methode legt den Lizenztyp des aktuellen Remotedesktop-Sitzungshost (RD-Sitzungshost)-Servers fest.
ms.assetid: 293483ee-51ce-4cd4-ba13-6c7c02bbdbbf
ms.tgt_platform: multiple
keywords:
- ChangeMode-Methode Remotedesktopdienste
- ChangeMode-Methode Remotedesktopdienste, Win32_TerminalServiceSetting-Klasse
- Win32_TerminalServiceSetting-Klasse Remotedesktopdienste, ChangeMode-Methode
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.ChangeMode
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 880fcab8aa68e49c6b3c00278b90635686de6168
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391856"
---
# <a name="changemode-method-of-the-win32_terminalservicesetting-class"></a><span data-ttu-id="02598-106">ChangeMode-Methode der Win32 \_ terminalservicesetts-Klasse</span><span class="sxs-lookup"><span data-stu-id="02598-106">ChangeMode method of the Win32\_TerminalServiceSetting class</span></span>

<span data-ttu-id="02598-107">Die **ChangeMode** -Methode legt den Lizenztyp des aktuellen Remotedesktop-Sitzungshost (RD-Sitzungshost)-Servers fest.</span><span class="sxs-lookup"><span data-stu-id="02598-107">The **ChangeMode** method sets the licensing type of the current Remote Desktop Session Host (RD Session Host) server.</span></span>

## <a name="syntax"></a><span data-ttu-id="02598-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="02598-108">Syntax</span></span>


```mof
uint32 ChangeMode(
  [in] uint32 LicensingType
);
```



## <a name="parameters"></a><span data-ttu-id="02598-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="02598-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="02598-110">*LicensingType* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="02598-110">*LicensingType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="02598-111">Der Lizenzierungstyp, der basierend auf dem RD-Sitzungshost Server Modus festgelegt werden soll.</span><span class="sxs-lookup"><span data-stu-id="02598-111">The licensing type to set based on the RD Session Host server mode.</span></span>

<dt>

<span id="0"></span>

<span data-ttu-id="02598-112"><span id="0"></span>**1,0**</span><span class="sxs-lookup"><span data-stu-id="02598-112"><span id="0"></span>**0**</span></span>


</dt> <dd>

<span data-ttu-id="02598-113">Persönlicher RD-Sitzungshost Server.</span><span class="sxs-lookup"><span data-stu-id="02598-113">Personal RD Session Host server.</span></span>

</dd> <dt>

<span id="1"></span>

<span data-ttu-id="02598-114"><span id="1"></span>**1**</span><span class="sxs-lookup"><span data-stu-id="02598-114"><span id="1"></span>**1**</span></span>


</dt> <dd>

<span data-ttu-id="02598-115">Remote Desktop für die Verwaltung.</span><span class="sxs-lookup"><span data-stu-id="02598-115">Remote desktop for administration.</span></span>

</dd> <dt>

<span id="2"></span>

<span data-ttu-id="02598-116"><span id="2"></span>**2**</span><span class="sxs-lookup"><span data-stu-id="02598-116"><span id="2"></span>**2**</span></span>


</dt> <dd>

<span data-ttu-id="02598-117">Pro Gerät/pro Arbeitsplatz.</span><span class="sxs-lookup"><span data-stu-id="02598-117">Per device/per seat.</span></span> <span data-ttu-id="02598-118">Gültig für Anwendungsserver.</span><span class="sxs-lookup"><span data-stu-id="02598-118">Valid for application servers.</span></span>

</dd> <dt>

<span id="4"></span>

<span data-ttu-id="02598-119"><span id="4"></span>**4**</span><span class="sxs-lookup"><span data-stu-id="02598-119"><span id="4"></span>**4**</span></span>


</dt> <dd>

<span data-ttu-id="02598-120">Pro Benutzer.</span><span class="sxs-lookup"><span data-stu-id="02598-120">Per User.</span></span> <span data-ttu-id="02598-121">Gültig für Anwendungsserver.</span><span class="sxs-lookup"><span data-stu-id="02598-121">Valid for application servers.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="02598-122">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="02598-122">Return value</span></span>

<span data-ttu-id="02598-123">Gibt bei Erfolg 0 zurück, andernfalls wird ein WMI-Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="02598-123">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="02598-124">Eine Liste dieser Werte finden Sie unter [Remotedesktopdienste Fehler Codes des WMI-Anbieters](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="02598-124">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="remarks"></a><span data-ttu-id="02598-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="02598-125">Remarks</span></span>

<span data-ttu-id="02598-126">Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen.</span><span class="sxs-lookup"><span data-stu-id="02598-126">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="02598-127">MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert.</span><span class="sxs-lookup"><span data-stu-id="02598-127">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="02598-128">Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="02598-128">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="02598-129">Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="02598-129">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="02598-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="02598-130">Requirements</span></span>



| <span data-ttu-id="02598-131">Anforderung</span><span class="sxs-lookup"><span data-stu-id="02598-131">Requirement</span></span> | <span data-ttu-id="02598-132">Wert</span><span class="sxs-lookup"><span data-stu-id="02598-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="02598-133">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="02598-133">Minimum supported client</span></span><br/> | <span data-ttu-id="02598-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="02598-134">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="02598-135">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="02598-135">Minimum supported server</span></span><br/> | <span data-ttu-id="02598-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="02598-136">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="02598-137">Namespace</span><span class="sxs-lookup"><span data-stu-id="02598-137">Namespace</span></span><br/>                | <span data-ttu-id="02598-138">Root \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="02598-138">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="02598-139">MOF</span><span class="sxs-lookup"><span data-stu-id="02598-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="02598-140"><dt>Tscsgwmi. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="02598-140"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="02598-141">DLL</span><span class="sxs-lookup"><span data-stu-id="02598-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="02598-142"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="02598-142"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="02598-143">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="02598-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="02598-144">**Win32 \_ terminalservicesetts**</span><span class="sxs-lookup"><span data-stu-id="02598-144">**Win32\_TerminalServiceSetting**</span></span>](win32-terminalservicesetting.md)
</dt> </dl>

 

