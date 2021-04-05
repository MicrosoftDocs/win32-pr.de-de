---
title: Settsredirectormode-Methode der Win32_TSSessionDirectory-Klasse
description: Legt den Wert fest, mit dem angegeben wird, ob der Server als Remotedesktopdienste Redirector fungiert.
ms.assetid: abdb92df-1e49-4445-ba02-bb83fd1ca541
ms.tgt_platform: multiple
keywords:
- Settsredirectormode-Methode Remotedesktopdienste
- Settsredirectormode-Methode Remotedesktopdienste, Win32_TSSessionDirectory-Klasse
- Win32_TSSessionDirectory-Klasse Remotedesktopdienste, settsredirectormode-Methode
topic_type:
- apiref
api_name:
- Win32_TSSessionDirectory.SetTSRedirectorMode
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 95e3195a83a32dca0c8e4a96de211a72a66a8f3a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103859216"
---
# <a name="settsredirectormode-method-of-the-win32_tssessiondirectory-class"></a><span data-ttu-id="f62b0-106">Settsredirectormode-Methode der Win32- \_ Klasse "tssessiondirectory"</span><span class="sxs-lookup"><span data-stu-id="f62b0-106">SetTSRedirectorMode method of the Win32\_TSSessionDirectory class</span></span>

<span data-ttu-id="f62b0-107">Legt den Wert fest, mit dem angegeben wird, ob der Server als Remotedesktopdienste Redirector fungiert.</span><span class="sxs-lookup"><span data-stu-id="f62b0-107">Sets the value to indicate whether the server will act as a Remote Desktop Services redirector.</span></span>

## <a name="syntax"></a><span data-ttu-id="f62b0-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="f62b0-108">Syntax</span></span>


```mof
uint32 SetTSRedirectorMode(
  [in] uint32 TSRedirValue
);
```



## <a name="parameters"></a><span data-ttu-id="f62b0-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="f62b0-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f62b0-110">" *Sredirvalue* \[ " in\]</span><span class="sxs-lookup"><span data-stu-id="f62b0-110">*TSRedirValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f62b0-111">Typ: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f62b0-111">Type: **uint32**</span></span>

<span data-ttu-id="f62b0-112">Gibt an, ob der Server als Remotedesktopdienste Redirector fungieren soll.</span><span class="sxs-lookup"><span data-stu-id="f62b0-112">Specifies if the server will act as a Remote Desktop Services redirector.</span></span> <span data-ttu-id="f62b0-113">Dies kann einer der folgenden Werte sein:</span><span class="sxs-lookup"><span data-stu-id="f62b0-113">This can be one of the following values.</span></span>

<dt>

<span data-ttu-id="f62b0-114">0</span><span class="sxs-lookup"><span data-stu-id="f62b0-114">0</span></span>
</dt> <dd>

<span data-ttu-id="f62b0-115">Der Server fungiert als Remotedesktopdienste Redirector.</span><span class="sxs-lookup"><span data-stu-id="f62b0-115">The server will act as a Remote Desktop Services redirector.</span></span>

</dd> <dt>

<span data-ttu-id="f62b0-116">1</span><span class="sxs-lookup"><span data-stu-id="f62b0-116">1</span></span>
</dt> <dd>

<span data-ttu-id="f62b0-117">Der Server fungiert nicht als Remotedesktopdienste Redirector.</span><span class="sxs-lookup"><span data-stu-id="f62b0-117">The server will not act as a Remote Desktop Services redirector.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f62b0-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f62b0-118">Return value</span></span>

<span data-ttu-id="f62b0-119">Typ: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f62b0-119">Type: **uint32**</span></span>

<span data-ttu-id="f62b0-120">Gibt bei Erfolg 0 zurück, andernfalls wird ein WMI-Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="f62b0-120">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="f62b0-121">Eine Liste dieser Werte finden Sie unter [Remotedesktopdienste Fehler Codes des WMI-Anbieters](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="f62b0-121">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span> <span data-ttu-id="f62b0-122">Die-Methode gibt einen Fehler zurück, wenn die Einstellung Untergruppen Richtlinien Steuerung liegt.</span><span class="sxs-lookup"><span data-stu-id="f62b0-122">The method returns an error if the setting is under group policy control.</span></span>

## <a name="remarks"></a><span data-ttu-id="f62b0-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f62b0-123">Remarks</span></span>

<span data-ttu-id="f62b0-124">Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen.</span><span class="sxs-lookup"><span data-stu-id="f62b0-124">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="f62b0-125">MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert.</span><span class="sxs-lookup"><span data-stu-id="f62b0-125">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="f62b0-126">Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="f62b0-126">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="f62b0-127">Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="f62b0-127">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="f62b0-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f62b0-128">Requirements</span></span>



| <span data-ttu-id="f62b0-129">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f62b0-129">Requirement</span></span> | <span data-ttu-id="f62b0-130">Wert</span><span class="sxs-lookup"><span data-stu-id="f62b0-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f62b0-131">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f62b0-131">Minimum supported client</span></span><br/> | <span data-ttu-id="f62b0-132">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="f62b0-132">None supported</span></span><br/>                                                               |
| <span data-ttu-id="f62b0-133">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f62b0-133">Minimum supported server</span></span><br/> | <span data-ttu-id="f62b0-134">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="f62b0-134">Windows Server 2008 R2</span></span><br/>                                                       |
| <span data-ttu-id="f62b0-135">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="f62b0-135">End of client support</span></span><br/>    | <span data-ttu-id="f62b0-136">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="f62b0-136">None supported</span></span><br/>                                                               |
| <span data-ttu-id="f62b0-137">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="f62b0-137">End of server support</span></span><br/>    | <span data-ttu-id="f62b0-138">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="f62b0-138">Windows Server 2008 R2</span></span><br/>                                                       |
| <span data-ttu-id="f62b0-139">Namespace</span><span class="sxs-lookup"><span data-stu-id="f62b0-139">Namespace</span></span><br/>                | <span data-ttu-id="f62b0-140">Root \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="f62b0-140">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="f62b0-141">MOF</span><span class="sxs-lookup"><span data-stu-id="f62b0-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f62b0-142"><dt>Tscsgwmi. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="f62b0-142"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="f62b0-143">DLL</span><span class="sxs-lookup"><span data-stu-id="f62b0-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f62b0-144"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f62b0-144"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f62b0-145">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f62b0-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f62b0-146">**Win32- \_ tssessiondirectory**</span><span class="sxs-lookup"><span data-stu-id="f62b0-146">**Win32\_TSSessionDirectory**</span></span>](win32-tssessiondirectory.md)
</dt> </dl>

 

