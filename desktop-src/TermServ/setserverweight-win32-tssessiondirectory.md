---
title: Setserverweight-Methode der Win32_TSSessionDirectory-Klasse
description: Legt den Server Gewichtungswert für den Lastenausgleich von Remotedesktopverbindung Broker (RD-Verbindungsbroker) fest.
ms.assetid: 9c7563e5-bb45-495d-90b0-43170b58581e
ms.tgt_platform: multiple
keywords:
- Setserverweight-Methode Remotedesktopdienste
- Setserverweight-Methode Remotedesktopdienste, Win32_TSSessionDirectory-Klasse
- Win32_TSSessionDirectory-Klasse Remotedesktopdienste, setserverweight-Methode
topic_type:
- apiref
api_name:
- Win32_TSSessionDirectory.SetServerWeight
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 46e8456fa590de0c9d6236f96f3b09c16087d730
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477715"
---
# <a name="setserverweight-method-of-the-win32_tssessiondirectory-class"></a><span data-ttu-id="e407d-106">Setserverweight-Methode der Win32- \_ Klasse "tssessiondirectory"</span><span class="sxs-lookup"><span data-stu-id="e407d-106">SetServerWeight method of the Win32\_TSSessionDirectory class</span></span>

<span data-ttu-id="e407d-107">Legt den Server Gewichtungswert für den Lastenausgleich von Remotedesktopverbindung Broker (RD-Verbindungsbroker) fest.</span><span class="sxs-lookup"><span data-stu-id="e407d-107">Sets the server weight value for Remote Desktop Connection Broker (RD Connection Broker) load balancing.</span></span>

## <a name="syntax"></a><span data-ttu-id="e407d-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="e407d-108">Syntax</span></span>


```mof
uint32 SetServerWeight(
  [in] uint32 ServerWeightValue
);
```



## <a name="parameters"></a><span data-ttu-id="e407d-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="e407d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e407d-110">*Serverweightvalue* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e407d-110">*ServerWeightValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e407d-111">Typ: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e407d-111">Type: **uint32**</span></span>

<span data-ttu-id="e407d-112">Der Server Gewichtungswert.</span><span class="sxs-lookup"><span data-stu-id="e407d-112">The server weight value.</span></span> <span data-ttu-id="e407d-113">Der gültige Bereich liegt zwischen 1 und 10000.</span><span class="sxs-lookup"><span data-stu-id="e407d-113">The valid range is 1 to 10000.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e407d-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e407d-114">Remarks</span></span>

<span data-ttu-id="e407d-115">Standardmäßig ist der Server Gewichtungswert in der Benutzeroberfläche Remotedesktopdienste Konfiguration 100.</span><span class="sxs-lookup"><span data-stu-id="e407d-115">By default in the user interface of Remote Desktop Services Configuration, the server weight value is 100.</span></span> <span data-ttu-id="e407d-116">Die Server Gewichtung ist relativ.</span><span class="sxs-lookup"><span data-stu-id="e407d-116">The server weight is relative.</span></span> <span data-ttu-id="e407d-117">Wenn Sie einen Server mit einem Wert von 100 und einem Wert von 200 zuweisen, erhält der Server mit der relativen Gewichtung 200 die doppelte Anzahl von Sitzungen.</span><span class="sxs-lookup"><span data-stu-id="e407d-117">Therefore, if you assign one server a value of 100, and one a value of 200, the server with a relative weight of 200 will receive twice the number of sessions.</span></span>

<span data-ttu-id="e407d-118">Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen.</span><span class="sxs-lookup"><span data-stu-id="e407d-118">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="e407d-119">MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert.</span><span class="sxs-lookup"><span data-stu-id="e407d-119">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="e407d-120">Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="e407d-120">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="e407d-121">Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="e407d-121">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="e407d-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e407d-122">Requirements</span></span>



| <span data-ttu-id="e407d-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e407d-123">Requirement</span></span> | <span data-ttu-id="e407d-124">Wert</span><span class="sxs-lookup"><span data-stu-id="e407d-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e407d-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e407d-125">Minimum supported client</span></span><br/> | <span data-ttu-id="e407d-126">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="e407d-126">None supported</span></span><br/>                                                               |
| <span data-ttu-id="e407d-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e407d-127">Minimum supported server</span></span><br/> | <span data-ttu-id="e407d-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e407d-128">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="e407d-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="e407d-129">Namespace</span></span><br/>                | <span data-ttu-id="e407d-130">Root \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="e407d-130">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="e407d-131">MOF</span><span class="sxs-lookup"><span data-stu-id="e407d-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e407d-132"><dt>Tscsgwmi. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="e407d-132"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="e407d-133">DLL</span><span class="sxs-lookup"><span data-stu-id="e407d-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e407d-134"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e407d-134"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e407d-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e407d-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e407d-136">**Win32- \_ tssessiondirectory**</span><span class="sxs-lookup"><span data-stu-id="e407d-136">**Win32\_TSSessionDirectory**</span></span>](win32-tssessiondirectory.md)
</dt> </dl>

 

