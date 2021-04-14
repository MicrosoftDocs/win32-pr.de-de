---
title: Die Methode "stenessiondirectoryactive" der Win32_TSSessionDirectory-Klasse
description: Die sezessiondirectoryactive-Methode legt die sessiondirectoryactive-Eigenschaft fest.
ms.assetid: b2175d1a-b62f-4bdf-9122-76e85233fba4
ms.tgt_platform: multiple
keywords:
- Remotedesktopdienste der Methode "
- Methode Remotedesktopdienste der Methode "Win32_TSSessionDirectory"
- Win32_TSSessionDirectory-Klasse Remotedesktopdienste, Methode "-Klasse"
topic_type:
- apiref
api_name:
- Win32_TSSessionDirectory.SetSessionDirectoryActive
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ca8709028ee90db549c7cdeb053b04dc88b52ab
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391803"
---
# <a name="setsessiondirectoryactive-method-of-the-win32_tssessiondirectory-class"></a><span data-ttu-id="de4f0-106">Die Methode "c-essiondirectoryactive" der Win32- \_ Klasse "tssessiondirectory"</span><span class="sxs-lookup"><span data-stu-id="de4f0-106">SetSessionDirectoryActive method of the Win32\_TSSessionDirectory class</span></span>

<span data-ttu-id="de4f0-107">Die **sezessiondirectoryactive** -Methode legt die **sessiondirectoryactive** -Eigenschaft fest.</span><span class="sxs-lookup"><span data-stu-id="de4f0-107">The **SetSessionDirectoryActive** method sets the **SessionDirectoryActive** property.</span></span>

## <a name="syntax"></a><span data-ttu-id="de4f0-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="de4f0-108">Syntax</span></span>


```mof
uint32 SetSessionDirectoryActive(
  [in] uint32 SessionDirectoryActive
);
```



## <a name="parameters"></a><span data-ttu-id="de4f0-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="de4f0-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="de4f0-110">*Sessiondirectorialactive* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="de4f0-110">*SessionDirectoryActive* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="de4f0-111">Typ: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="de4f0-111">Type: **uint32**</span></span>

<span data-ttu-id="de4f0-112">Flag zum Deaktivieren oder Aktivieren des Sitzungs Verzeichnis dienstanzen.</span><span class="sxs-lookup"><span data-stu-id="de4f0-112">Flag disabling or enabling the Session Directory service.</span></span>

<dt>

<span id="0"></span>

<span data-ttu-id="de4f0-113"><span id="0"></span>**1,0**</span><span class="sxs-lookup"><span data-stu-id="de4f0-113"><span id="0"></span>**0**</span></span>


</dt> <dd>

<span data-ttu-id="de4f0-114">Deaktivieren Sie den Sitzungs Verzeichnisdienst.</span><span class="sxs-lookup"><span data-stu-id="de4f0-114">Disable the Session Directory service.</span></span>

</dd> <dt>

<span id="1"></span>

<span data-ttu-id="de4f0-115"><span id="1"></span>**1**</span><span class="sxs-lookup"><span data-stu-id="de4f0-115"><span id="1"></span>**1**</span></span>


</dt> <dd>

<span data-ttu-id="de4f0-116">Aktivieren Sie den Sitzungs Verzeichnisdienst.</span><span class="sxs-lookup"><span data-stu-id="de4f0-116">Enable the Session Directory service.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="de4f0-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="de4f0-117">Return value</span></span>

<span data-ttu-id="de4f0-118">Typ: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="de4f0-118">Type: **uint32**</span></span>

<span data-ttu-id="de4f0-119">Gibt bei Erfolg 0 zurück, andernfalls wird ein WMI-Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="de4f0-119">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="de4f0-120">Eine Liste dieser Werte finden Sie unter [Remotedesktopdienste Fehler Codes des WMI-Anbieters](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="de4f0-120">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span> <span data-ttu-id="de4f0-121">Die-Methode gibt einen Fehler zurück, wenn die Einstellung Untergruppen Richtlinien Steuerung liegt.</span><span class="sxs-lookup"><span data-stu-id="de4f0-121">The method returns an error if the setting is under group policy control.</span></span>

## <a name="remarks"></a><span data-ttu-id="de4f0-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="de4f0-122">Remarks</span></span>

<span data-ttu-id="de4f0-123">Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen.</span><span class="sxs-lookup"><span data-stu-id="de4f0-123">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="de4f0-124">MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert.</span><span class="sxs-lookup"><span data-stu-id="de4f0-124">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="de4f0-125">Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="de4f0-125">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="de4f0-126">Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="de4f0-126">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="de4f0-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="de4f0-127">Requirements</span></span>



| <span data-ttu-id="de4f0-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="de4f0-128">Requirement</span></span> | <span data-ttu-id="de4f0-129">Wert</span><span class="sxs-lookup"><span data-stu-id="de4f0-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="de4f0-130">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="de4f0-130">Minimum supported client</span></span><br/> | <span data-ttu-id="de4f0-131">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="de4f0-131">None supported</span></span><br/>                                                               |
| <span data-ttu-id="de4f0-132">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="de4f0-132">Minimum supported server</span></span><br/> | <span data-ttu-id="de4f0-133">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="de4f0-133">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="de4f0-134">Namespace</span><span class="sxs-lookup"><span data-stu-id="de4f0-134">Namespace</span></span><br/>                | <span data-ttu-id="de4f0-135">Root \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="de4f0-135">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="de4f0-136">MOF</span><span class="sxs-lookup"><span data-stu-id="de4f0-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="de4f0-137"><dt>Tscsgwmi. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="de4f0-137"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="de4f0-138">DLL</span><span class="sxs-lookup"><span data-stu-id="de4f0-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="de4f0-139"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="de4f0-139"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="de4f0-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="de4f0-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="de4f0-141">**Win32- \_ tssessiondirectory**</span><span class="sxs-lookup"><span data-stu-id="de4f0-141">**Win32\_TSSessionDirectory**</span></span>](win32-tssessiondirectory.md)
</dt> </dl>

 

