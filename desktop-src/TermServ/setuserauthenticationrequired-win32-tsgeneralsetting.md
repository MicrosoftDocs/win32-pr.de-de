---
title: Setuserauthenticationrequired-Methode der Win32_TSGeneralSetting-Klasse
description: Aktiviert oder deaktiviert die Anforderung, dass Benutzer zur Verbindungszeit authentifiziert werden müssen, indem der Wert der UserAuthenticationRequired-Eigenschaft festgelegt wird.
ms.assetid: a0581326-fecc-4d23-87bf-3696c93366e8
ms.tgt_platform: multiple
keywords:
- Setuserauthenticationrequired-Methode Remotedesktopdienste
- Setuserauthenticationrequired-Methode Remotedesktopdienste, Win32_TSGeneralSetting-Klasse
- Win32_TSGeneralSetting-Klasse Remotedesktopdienste, setuserauthenticationrequired-Methode
topic_type:
- apiref
api_name:
- Win32_TSGeneralSetting.SetUserAuthenticationRequired
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b39c0eb711d2146130ff0fd879953fc71fcba965
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104341128"
---
# <a name="setuserauthenticationrequired-method-of-the-win32_tsgeneralsetting-class"></a><span data-ttu-id="94bf1-106">Setuserauthenticationrequired-Methode der Win32- \_ Klasse "zgeneralsetting"</span><span class="sxs-lookup"><span data-stu-id="94bf1-106">SetUserAuthenticationRequired method of the Win32\_TSGeneralSetting class</span></span>

<span data-ttu-id="94bf1-107">Aktiviert oder deaktiviert die Anforderung, dass Benutzer zur Verbindungszeit authentifiziert werden müssen, indem der Wert der **UserAuthenticationRequired** -Eigenschaft in der Win32-Klasse " [**\_ tgeneralsetting**](win32-tsgeneralsetting.md) " festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="94bf1-107">Enables or disables the requirement that users must be authenticated at connection time by setting the value of the **UserAuthenticationRequired** property in the [**Win32\_TSGeneralSetting**](win32-tsgeneralsetting.md) class.</span></span> <span data-ttu-id="94bf1-108">Wenn **true**, d. h. aktiviert, erfordert **UserAuthenticationRequired** eine Benutzerauthentifizierung zur Verbindungszeit, um den Server Schutz vor Netzwerk Angriffen zu erhöhen.</span><span class="sxs-lookup"><span data-stu-id="94bf1-108">If **True**, which means enabled, **UserAuthenticationRequired** requires user authentication at connection time to increase server protection against network attacks.</span></span> <span data-ttu-id="94bf1-109">Nur Remotedesktopprotokoll (RDP)-Clients, die RDP-Version 6,0 oder höher unterstützen, können eine Verbindung herstellen.</span><span class="sxs-lookup"><span data-stu-id="94bf1-109">Only Remote Desktop Protocol (RDP) clients that support RDP version 6.0 or higher are able to connect.</span></span> <span data-ttu-id="94bf1-110">Um Unterbrechungen für Remote Benutzer zu vermeiden, wird empfohlen, RDP-Clients bereitzustellen, die die entsprechende Protokollversion unterstützen, bevor Sie die-Eigenschaft aktivieren.</span><span class="sxs-lookup"><span data-stu-id="94bf1-110">To avoid disruptions for remote users, it is recommended that you deploy RDP clients supporting the appropriate protocol version before you enable the property.</span></span>

## <a name="syntax"></a><span data-ttu-id="94bf1-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="94bf1-111">Syntax</span></span>


```mof
uint32 SetUserAuthenticationRequired(
  [in] uint32 UserAuthenticationRequired
);
```



## <a name="parameters"></a><span data-ttu-id="94bf1-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="94bf1-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="94bf1-113">*UserAuthenticationRequired* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="94bf1-113">*UserAuthenticationRequired* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="94bf1-114">Gibt an, ob eine Benutzerauthentifizierung erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="94bf1-114">Indicates whether user authentication is required.</span></span>

<dt>

<span data-ttu-id="94bf1-115">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="94bf1-115">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="94bf1-116">Anforderung deaktivieren, dass der Benutzer authentifiziert werden muss</span><span class="sxs-lookup"><span data-stu-id="94bf1-116">Disable requirement that user must be authenticated</span></span>

</dd> <dt>

<span data-ttu-id="94bf1-117">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="94bf1-117">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="94bf1-118">Aktiviert die Anforderung, dass der Benutzer authentifiziert werden muss.</span><span class="sxs-lookup"><span data-stu-id="94bf1-118">Enables requirement that user must be authenticated.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="94bf1-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="94bf1-119">Return value</span></span>

<span data-ttu-id="94bf1-120">Gibt bei Erfolg 0 zurück, andernfalls wird ein WMI-Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="94bf1-120">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="94bf1-121">Eine Liste dieser Werte finden Sie unter [Remotedesktopdienste Fehler Codes des WMI-Anbieters](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="94bf1-121">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="remarks"></a><span data-ttu-id="94bf1-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="94bf1-122">Remarks</span></span>

<span data-ttu-id="94bf1-123">Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen.</span><span class="sxs-lookup"><span data-stu-id="94bf1-123">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="94bf1-124">MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert.</span><span class="sxs-lookup"><span data-stu-id="94bf1-124">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="94bf1-125">Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="94bf1-125">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="94bf1-126">Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="94bf1-126">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="94bf1-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="94bf1-127">Requirements</span></span>



| <span data-ttu-id="94bf1-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="94bf1-128">Requirement</span></span> | <span data-ttu-id="94bf1-129">Wert</span><span class="sxs-lookup"><span data-stu-id="94bf1-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="94bf1-130">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="94bf1-130">Minimum supported client</span></span><br/> | <span data-ttu-id="94bf1-131">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="94bf1-131">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="94bf1-132">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="94bf1-132">Minimum supported server</span></span><br/> | <span data-ttu-id="94bf1-133">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="94bf1-133">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="94bf1-134">Namespace</span><span class="sxs-lookup"><span data-stu-id="94bf1-134">Namespace</span></span><br/>                | <span data-ttu-id="94bf1-135">Root \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="94bf1-135">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="94bf1-136">MOF</span><span class="sxs-lookup"><span data-stu-id="94bf1-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="94bf1-137"><dt>Tscsgwmi. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="94bf1-137"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="94bf1-138">DLL</span><span class="sxs-lookup"><span data-stu-id="94bf1-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="94bf1-139"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="94bf1-139"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="94bf1-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="94bf1-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="94bf1-141">**Win32-Einstellung für "" \_**</span><span class="sxs-lookup"><span data-stu-id="94bf1-141">**Win32\_TSGeneralSetting**</span></span>](win32-tsgeneralsetting.md)
</dt> </dl>

 

