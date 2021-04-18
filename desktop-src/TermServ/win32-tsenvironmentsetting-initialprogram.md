---
title: InitialProgram-Methode der Win32_TSEnvironmentSetting-Klasse
description: Mit der InitialProgram-Methode werden Start Programm Eigenschaften wie Name, Arbeitsverzeichnis und Pfad des Programms so festgelegt, dass Sie sofort nach der Anmeldung auf dem Remotedesktop-Sitzungshost-Server (RD-Sitzungshost) gestartet werden.
ms.assetid: e53621cf-ade8-4301-acc0-232866e88488
ms.tgt_platform: multiple
keywords:
- InitialProgram-Methode Remotedesktopdienste
- InitialProgram-Methode Remotedesktopdienste, Win32_TSEnvironmentSetting-Klasse
- Win32_TSEnvironmentSetting-Klasse Remotedesktopdienste, InitialProgram-Methode
topic_type:
- apiref
api_name:
- Win32_TSEnvironmentSetting.InitialProgram
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ccd41e1af990e37b8458431106bc2ec9a8489b14
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106337508"
---
# <a name="initialprogram-method-of-the-win32_tsenvironmentsetting-class"></a><span data-ttu-id="da092-106">InitialProgram-Methode der Win32- \_ Klasse tsenvironmentsetting</span><span class="sxs-lookup"><span data-stu-id="da092-106">InitialProgram method of the Win32\_TSEnvironmentSetting class</span></span>

<span data-ttu-id="da092-107">Mit der **InitialProgram** -Methode werden Start Programm Eigenschaften wie Name, Arbeitsverzeichnis und Pfad des Programms so festgelegt, dass Sie sofort nach der Anmeldung auf dem Remotedesktop-Sitzungshost-Server (RD-Sitzungshost) gestartet werden.</span><span class="sxs-lookup"><span data-stu-id="da092-107">The **InitialProgram** method sets startup program properties such as the name, working directory, and path of the program to start immediately after logon to the Remote Desktop Session Host (RD Session Host) server.</span></span>

## <a name="syntax"></a><span data-ttu-id="da092-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="da092-108">Syntax</span></span>


```mof
uint32 InitialProgram(
  [in] string InitialProgramPath,
  [in] string Startin
);
```



## <a name="parameters"></a><span data-ttu-id="da092-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="da092-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="da092-110">*Initialprogrampath* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="da092-110">*InitialProgramPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="da092-111">Der Name und der Pfad des Start Programms.</span><span class="sxs-lookup"><span data-stu-id="da092-111">The name and path of the startup program.</span></span>

</dd> <dt>

<span data-ttu-id="da092-112">*Startin* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="da092-112">*Startin* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="da092-113">Der Pfad zum Arbeitsverzeichnis des Start Programms.</span><span class="sxs-lookup"><span data-stu-id="da092-113">The path to the working directory of the startup program.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="da092-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="da092-114">Return value</span></span>

<span data-ttu-id="da092-115">Gibt bei Erfolg 0 zurück, andernfalls wird ein WMI-Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="da092-115">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="da092-116">Eine Liste dieser Werte finden Sie unter [Remotedesktopdienste Fehler Codes des WMI-Anbieters](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="da092-116">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span> <span data-ttu-id="da092-117">Die-Methode gibt einen Fehler zurück, wenn die Einstellung Untergruppen Richtlinien Steuerung liegt.</span><span class="sxs-lookup"><span data-stu-id="da092-117">The method returns an error if the setting is under group policy control.</span></span>

## <a name="remarks"></a><span data-ttu-id="da092-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="da092-118">Remarks</span></span>

<span data-ttu-id="da092-119">Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen.</span><span class="sxs-lookup"><span data-stu-id="da092-119">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="da092-120">MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert.</span><span class="sxs-lookup"><span data-stu-id="da092-120">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="da092-121">Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="da092-121">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="da092-122">Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="da092-122">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="da092-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="da092-123">Requirements</span></span>



| <span data-ttu-id="da092-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="da092-124">Requirement</span></span> | <span data-ttu-id="da092-125">Wert</span><span class="sxs-lookup"><span data-stu-id="da092-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="da092-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="da092-126">Minimum supported client</span></span><br/> | <span data-ttu-id="da092-127">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="da092-127">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="da092-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="da092-128">Minimum supported server</span></span><br/> | <span data-ttu-id="da092-129">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="da092-129">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="da092-130">Namespace</span><span class="sxs-lookup"><span data-stu-id="da092-130">Namespace</span></span><br/>                | <span data-ttu-id="da092-131">Root \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="da092-131">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="da092-132">MOF</span><span class="sxs-lookup"><span data-stu-id="da092-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="da092-133"><dt>Tscsgwmi. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="da092-133"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="da092-134">DLL</span><span class="sxs-lookup"><span data-stu-id="da092-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="da092-135"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="da092-135"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="da092-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="da092-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="da092-137">**Win32- \_ tsenvironmentsetting**</span><span class="sxs-lookup"><span data-stu-id="da092-137">**Win32\_TSEnvironmentSetting**</span></span>](win32-tsenvironmentsetting.md)
</dt> </dl>

 

