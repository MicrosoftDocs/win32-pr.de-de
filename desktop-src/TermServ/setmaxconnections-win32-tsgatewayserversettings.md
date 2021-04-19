---
title: Setmaxconnections-Methode der Win32_TSGatewayServerSettings-Klasse
description: Legt die Eigenschaften MaxConnections und UnlimitedConnections fest, die die maximale Anzahl zulässiger Verbindungen mit dem Remotedesktop Gateway-Server (RD-Gateway) steuern.
ms.assetid: cfdbacb7-4969-4ec5-8301-e8020f3af0cd
ms.tgt_platform: multiple
keywords:
- Setmaxconnections-Methode Remotedesktopdienste
- Setmaxconnections-Methode Remotedesktopdienste, Win32_TSGatewayServerSettings-Klasse
- Win32_TSGatewayServerSettings-Klasse Remotedesktopdienste, setmaxconnections-Methode
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.SetMaxConnections
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c7e8a2fa18491232a058913fd338bb871b0a98aa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106341401"
---
# <a name="setmaxconnections-method-of-the-win32_tsgatewayserversettings-class"></a><span data-ttu-id="cda9b-106">Setmaxconnections-Methode der Win32-Klasse "t- \_ gatewayserversettings"</span><span class="sxs-lookup"><span data-stu-id="cda9b-106">SetMaxConnections method of the Win32\_TSGatewayServerSettings class</span></span>

<span data-ttu-id="cda9b-107">Legt die Eigenschaften **MaxConnections** und **UnlimitedConnections** fest, die die maximale Anzahl zulässiger Verbindungen mit dem Remotedesktop Gateway-Server (RD-Gateway) steuern.</span><span class="sxs-lookup"><span data-stu-id="cda9b-107">Sets the **MaxConnections** and **UnlimitedConnections** properties, which control the maximum number of allowed connections to the Remote Desktop Gateway (RD Gateway) server.</span></span>

## <a name="syntax"></a><span data-ttu-id="cda9b-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="cda9b-108">Syntax</span></span>


```mof
uint32 SetMaxConnections(
  [in] uint32  Connections,
  [in] boolean IsUnlimited
);
```



## <a name="parameters"></a><span data-ttu-id="cda9b-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="cda9b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cda9b-110">*Verbindungen* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="cda9b-110">*Connections* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cda9b-111">Anzahl von Verbindungen, die von diesem Server akzeptiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="cda9b-111">Number of connections that this server should accept.</span></span> <span data-ttu-id="cda9b-112">Legen Sie für eine unbegrenzte Anzahl von Verbindungen den *isunlimited* -Parameter auf " **true**" fest.</span><span class="sxs-lookup"><span data-stu-id="cda9b-112">For an unlimited number of connections, set the *IsUnlimited* parameter to **True**.</span></span>

</dd> <dt>

<span data-ttu-id="cda9b-113">*Isunbegrenzt* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="cda9b-113">*IsUnlimited* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cda9b-114">**True** gibt an, dass Verbindungen mit dem Dienst nicht auf eine bestimmte Anzahl beschränkt sind.</span><span class="sxs-lookup"><span data-stu-id="cda9b-114">If **True**, connections to the service are not limited to a specific number.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cda9b-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="cda9b-115">Return value</span></span>

<span data-ttu-id="cda9b-116">Wenn die Methode erfolgreich ist, gibt Sie 0 (null) zurück.</span><span class="sxs-lookup"><span data-stu-id="cda9b-116">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="cda9b-117">Wenn die Methode nicht erfolgreich ist, wird ein Wert ungleich 0 (null) zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="cda9b-117">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="cda9b-118">Eine Liste der Fehlercodes finden Sie unter [Remotedesktopdienste Fehlercodes des WMI-Anbieters](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="cda9b-118">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="cda9b-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="cda9b-119">Remarks</span></span>

<span data-ttu-id="cda9b-120">Sie müssen Mitglied der Gruppe "Administratoren" sein, um diese Methode aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="cda9b-120">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="cda9b-121">Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen.</span><span class="sxs-lookup"><span data-stu-id="cda9b-121">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="cda9b-122">MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert.</span><span class="sxs-lookup"><span data-stu-id="cda9b-122">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="cda9b-123">Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="cda9b-123">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="cda9b-124">Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="cda9b-124">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="cda9b-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cda9b-125">Requirements</span></span>



| <span data-ttu-id="cda9b-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="cda9b-126">Requirement</span></span> | <span data-ttu-id="cda9b-127">Wert</span><span class="sxs-lookup"><span data-stu-id="cda9b-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="cda9b-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="cda9b-128">Minimum supported client</span></span><br/> | <span data-ttu-id="cda9b-129">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="cda9b-129">None supported</span></span><br/>                                                                |
| <span data-ttu-id="cda9b-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="cda9b-130">Minimum supported server</span></span><br/> | <span data-ttu-id="cda9b-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="cda9b-131">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="cda9b-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="cda9b-132">Namespace</span></span><br/>                | <span data-ttu-id="cda9b-133">Root \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="cda9b-133">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="cda9b-134">MOF</span><span class="sxs-lookup"><span data-stu-id="cda9b-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="cda9b-135"><dt>"T-Gateway. mof"</dt></span><span class="sxs-lookup"><span data-stu-id="cda9b-135"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="cda9b-136">DLL</span><span class="sxs-lookup"><span data-stu-id="cda9b-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cda9b-137"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cda9b-137"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="cda9b-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cda9b-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cda9b-139">**Win32-Datei- \_ gatewayserversettings**</span><span class="sxs-lookup"><span data-stu-id="cda9b-139">**Win32\_TSGatewayServerSettings**</span></span>](win32-tsgatewayserversettings.md)
</dt> </dl>

 

