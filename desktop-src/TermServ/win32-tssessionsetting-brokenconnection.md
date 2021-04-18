---
title: Brokenconnection-Methode der Win32_TSSessionSetting-Klasse (wtsprodecol. h)
description: Legt die BrokenConnectionAction-Eigenschaft fest. Dies ist die Aktion, die der Server durchführt, wenn das Sitzungszeit Limit erreicht ist, oder, wenn die Verbindung getrennt wird.
ms.assetid: 2422e314-9e1c-4bed-a958-eedd2daeca66
ms.tgt_platform: multiple
keywords:
- Brokenconnection-Methode Remotedesktopdienste
- Brokenconnection-Methode Remotedesktopdienste, Win32_TSSessionSetting-Klasse
- Win32_TSSessionSetting-Klasse Remotedesktopdienste, brokenconnection-Methode
topic_type:
- apiref
api_name:
- Win32_TSSessionSetting.BrokenConnection
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a90b3f6bada75812b37df014cedadfb4e7ff2e83
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106339325"
---
# <a name="brokenconnection-method-of-the-win32_tssessionsetting-class"></a><span data-ttu-id="0f627-106">Brokenconnection-Methode der Win32- \_ Klasse "tssessionsetting"</span><span class="sxs-lookup"><span data-stu-id="0f627-106">BrokenConnection method of the Win32\_TSSessionSetting class</span></span>

<span data-ttu-id="0f627-107">Legt die **BrokenConnectionAction** -Eigenschaft fest. Dies ist die Aktion, die der Server durchführt, wenn das Sitzungszeit Limit erreicht ist, oder, wenn die Verbindung getrennt wird.</span><span class="sxs-lookup"><span data-stu-id="0f627-107">Sets the **BrokenConnectionAction** property, which is the action the server takes if the session time-limit is reached or if the connection is broken.</span></span>

## <a name="syntax"></a><span data-ttu-id="0f627-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="0f627-108">Syntax</span></span>


```mof
uint32 BrokenConnection(
  [in] uint32 BrokenConnectionAction
);
```



## <a name="parameters"></a><span data-ttu-id="0f627-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="0f627-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0f627-110">*BrokenConnectionAction* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0f627-110">*BrokenConnectionAction* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0f627-111">Die auszuführende Aktion.</span><span class="sxs-lookup"><span data-stu-id="0f627-111">The action to take.</span></span>

<dt>

<span id="Disconnect"></span><span id="disconnect"></span><span id="DISCONNECT"></span>

<span data-ttu-id="0f627-112"><span id="Disconnect"></span><span id="disconnect"></span><span id="DISCONNECT"></span>Verbindung **trennen** (0)</span><span class="sxs-lookup"><span data-stu-id="0f627-112"><span id="Disconnect"></span><span id="disconnect"></span><span id="DISCONNECT"></span>**Disconnect** (0)</span></span>


</dt> <dd>

<span data-ttu-id="0f627-113">Der Benutzer ist von der Sitzung getrennt.</span><span class="sxs-lookup"><span data-stu-id="0f627-113">The user is disconnected from the session.</span></span>

</dd> <dt>

<span id="Terminate"></span><span id="terminate"></span><span id="TERMINATE"></span>

<span data-ttu-id="0f627-114"><span id="Terminate"></span><span id="terminate"></span><span id="TERMINATE"></span>**Beenden** (1)</span><span class="sxs-lookup"><span data-stu-id="0f627-114"><span id="Terminate"></span><span id="terminate"></span><span id="TERMINATE"></span>**Terminate** (1)</span></span>


</dt> <dd>

<span data-ttu-id="0f627-115">Die Sitzung wird dauerhaft vom Server gelöscht.</span><span class="sxs-lookup"><span data-stu-id="0f627-115">The session is permanently deleted from the server.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0f627-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0f627-116">Return value</span></span>

<span data-ttu-id="0f627-117">Gibt bei Erfolg 0 zurück, andernfalls wird ein WMI-Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="0f627-117">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="0f627-118">Eine Liste dieser Werte finden Sie unter [Remotedesktopdienste Fehler Codes des WMI-Anbieters](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="0f627-118">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span> <span data-ttu-id="0f627-119">Die-Methode gibt einen Fehler zurück, wenn die Einstellung unter Gruppenrichtlinie-Steuerelement ist.</span><span class="sxs-lookup"><span data-stu-id="0f627-119">The method returns an error if the setting is under Group Policy control.</span></span>

## <a name="remarks"></a><span data-ttu-id="0f627-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0f627-120">Remarks</span></span>

<span data-ttu-id="0f627-121">Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen.</span><span class="sxs-lookup"><span data-stu-id="0f627-121">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="0f627-122">MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert.</span><span class="sxs-lookup"><span data-stu-id="0f627-122">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="0f627-123">Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="0f627-123">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="0f627-124">Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="0f627-124">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="0f627-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0f627-125">Requirements</span></span>



| <span data-ttu-id="0f627-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0f627-126">Requirement</span></span> | <span data-ttu-id="0f627-127">Wert</span><span class="sxs-lookup"><span data-stu-id="0f627-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="0f627-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0f627-128">Minimum supported client</span></span><br/> | <span data-ttu-id="0f627-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0f627-129">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="0f627-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0f627-130">Minimum supported server</span></span><br/> | <span data-ttu-id="0f627-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0f627-131">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="0f627-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="0f627-132">Namespace</span></span><br/>                | <span data-ttu-id="0f627-133">Root \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="0f627-133">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="0f627-134">Header</span><span class="sxs-lookup"><span data-stu-id="0f627-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="0f627-135"><dt>Wtsproum Col. h</dt></span><span class="sxs-lookup"><span data-stu-id="0f627-135"><dt>Wtsprotocol.h</dt></span></span> </dl> |
| <span data-ttu-id="0f627-136">MOF</span><span class="sxs-lookup"><span data-stu-id="0f627-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0f627-137"><dt>Tscsgwmi. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="0f627-137"><dt>TSCfgWmi.mof</dt></span></span> </dl>  |
| <span data-ttu-id="0f627-138">DLL</span><span class="sxs-lookup"><span data-stu-id="0f627-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0f627-139"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0f627-139"><dt>TSCfgWmi.dll</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="0f627-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0f627-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0f627-141">**Win32- \_ tssessionsetting**</span><span class="sxs-lookup"><span data-stu-id="0f627-141">**Win32\_TSSessionSetting**</span></span>](win32-tssessionsetting.md)
</dt> </dl>

 

