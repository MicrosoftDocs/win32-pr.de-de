---
title: Configure-Methode der Win32_TSGatewayServerSettings-Klasse
description: Konfiguriert die IIS-und RPC-Einstellungen, die vom Remotedesktop Gateway-Dienst (RD-Gateway) benötigt werden.
ms.assetid: 12d7264e-46aa-457f-b89d-547231573db8
ms.tgt_platform: multiple
keywords:
- Configure-Methode Remotedesktopdienste
- Configure Method Remotedesktopdienste, Win32_TSGatewayServerSettings-Klasse
- Win32_TSGatewayServerSettings-Klasse Remotedesktopdienste, Methode konfigurieren
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.Configure
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1880e1a9811c8aab2660993c6c8ab05061163e1a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040275"
---
# <a name="configure-method-of-the-win32_tsgatewayserversettings-class"></a><span data-ttu-id="8f650-106">Configure-Methode der Win32-Klasse "t- \_ gatewayserversettings"</span><span class="sxs-lookup"><span data-stu-id="8f650-106">Configure method of the Win32\_TSGatewayServerSettings class</span></span>

<span data-ttu-id="8f650-107">Konfiguriert die IIS-und RPC-Einstellungen, die vom Remotedesktop Gateway-Dienst (RD-Gateway) benötigt werden.</span><span class="sxs-lookup"><span data-stu-id="8f650-107">Configures the IIS and RPC settings required by the Remote Desktop Gateway (RD Gateway) service.</span></span>

## <a name="syntax"></a><span data-ttu-id="8f650-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="8f650-108">Syntax</span></span>


```mof
uint32 Configure();
```



## <a name="parameters"></a><span data-ttu-id="8f650-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="8f650-109">Parameters</span></span>

<span data-ttu-id="8f650-110">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="8f650-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="8f650-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8f650-111">Return value</span></span>

<span data-ttu-id="8f650-112">Typ: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8f650-112">Type: **uint32**</span></span>

<span data-ttu-id="8f650-113">Wenn die Methode erfolgreich ist, gibt Sie 0 (null) zurück.</span><span class="sxs-lookup"><span data-stu-id="8f650-113">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="8f650-114">Wenn die Methode nicht erfolgreich ist, wird ein Wert ungleich 0 (null) zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="8f650-114">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="8f650-115">Eine Liste der Fehlercodes finden Sie unter [Remotedesktopdienste Fehlercodes des WMI-Anbieters](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="8f650-115">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="8f650-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8f650-116">Remarks</span></span>

<span data-ttu-id="8f650-117">Sie müssen Mitglied der Gruppe "Administratoren" sein, um diese Methode aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="8f650-117">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="8f650-118">Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen.</span><span class="sxs-lookup"><span data-stu-id="8f650-118">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="8f650-119">MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert.</span><span class="sxs-lookup"><span data-stu-id="8f650-119">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="8f650-120">Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="8f650-120">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="8f650-121">Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="8f650-121">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="8f650-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8f650-122">Requirements</span></span>



| <span data-ttu-id="8f650-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8f650-123">Requirement</span></span> | <span data-ttu-id="8f650-124">Wert</span><span class="sxs-lookup"><span data-stu-id="8f650-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="8f650-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="8f650-125">Minimum supported client</span></span><br/> | <span data-ttu-id="8f650-126">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="8f650-126">None supported</span></span><br/>                                                                |
| <span data-ttu-id="8f650-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="8f650-127">Minimum supported server</span></span><br/> | <span data-ttu-id="8f650-128">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="8f650-128">Windows Server 2008 R2</span></span><br/>                                                        |
| <span data-ttu-id="8f650-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="8f650-129">Namespace</span></span><br/>                | <span data-ttu-id="8f650-130">Root \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="8f650-130">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="8f650-131">MOF</span><span class="sxs-lookup"><span data-stu-id="8f650-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8f650-132"><dt>"T-Gateway. mof"</dt></span><span class="sxs-lookup"><span data-stu-id="8f650-132"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="8f650-133">DLL</span><span class="sxs-lookup"><span data-stu-id="8f650-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8f650-134"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8f650-134"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="8f650-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8f650-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8f650-136">**Win32-Datei- \_ gatewayserversettings**</span><span class="sxs-lookup"><span data-stu-id="8f650-136">**Win32\_TSGatewayServerSettings**</span></span>](win32-tsgatewayserversettings.md)
</dt> </dl>

 

