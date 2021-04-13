---
title: Changerole-Methode der Win32_TSLicenseServer-Klasse
description: Ändert den Ermittlungs Bereich des Remotedesktop Lizenzservers. Der Ermittlungs Bereich bestimmt, welche Remotedesktop-Sitzungshost (RD-Sitzungshost)-Server im Netzwerk den Lizenzserver automatisch ermitteln können.
ms.assetid: 3d98fd8a-4ade-489f-8edd-5df1227f15cd
ms.tgt_platform: multiple
keywords:
- Changerole-Methode Remotedesktopdienste
- Changerole-Methode Remotedesktopdienste, Win32_TSLicenseServer-Klasse
- Win32_TSLicenseServer-Klasse Remotedesktopdienste, changerole-Methode
topic_type:
- apiref
api_name:
- Win32_TSLicenseServer.ChangeRole
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e9746b856c74e9603751fe85bb861e2b6869f03a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475795"
---
# <a name="changerole-method-of-the-win32_tslicenseserver-class"></a><span data-ttu-id="044ed-107">Changerole-Methode der Win32- \_ Klasse "zlicenseserver"</span><span class="sxs-lookup"><span data-stu-id="044ed-107">ChangeRole method of the Win32\_TSLicenseServer class</span></span>

<span data-ttu-id="044ed-108">Ändert den Ermittlungs Bereich des Remotedesktop Lizenzservers.</span><span class="sxs-lookup"><span data-stu-id="044ed-108">Changes the discovery scope of the Remote Desktop license server.</span></span> <span data-ttu-id="044ed-109">Der Ermittlungs Bereich bestimmt, welche Remotedesktop-Sitzungshost (RD-Sitzungshost)-Server im Netzwerk den Lizenzserver automatisch ermitteln können.</span><span class="sxs-lookup"><span data-stu-id="044ed-109">The discovery scope determines which Remote Desktop Session Host (RD Session Host) servers on the network can automatically discover the license server.</span></span>

## <a name="syntax"></a><span data-ttu-id="044ed-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="044ed-110">Syntax</span></span>


```mof
uint32 ChangeRole(
  [in] uint32 ServerRole
);
```



## <a name="parameters"></a><span data-ttu-id="044ed-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="044ed-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="044ed-112">*ServerRole* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="044ed-112">*ServerRole* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="044ed-113">Ermittlungs Bereich für den Remotedesktop-Lizenzserver.</span><span class="sxs-lookup"><span data-stu-id="044ed-113">Discovery scope for the Remote Desktop license server.</span></span> <span data-ttu-id="044ed-114">Sie können einen der folgenden Werte festlegen:</span><span class="sxs-lookup"><span data-stu-id="044ed-114">You can set one of the following values.</span></span>

<dt>

<span data-ttu-id="044ed-115">0</span><span class="sxs-lookup"><span data-stu-id="044ed-115">0</span></span>
</dt> <dd>

<span data-ttu-id="044ed-116">RD-Sitzungshost Server in derselben Arbeitsgruppe können den Lizenzserver ermitteln.</span><span class="sxs-lookup"><span data-stu-id="044ed-116">RD Session Host servers in the same workgroup can discover the license server.</span></span>

</dd> <dt>

<span data-ttu-id="044ed-117">1</span><span class="sxs-lookup"><span data-stu-id="044ed-117">1</span></span>
</dt> <dd>

<span data-ttu-id="044ed-118">RD-Sitzungshost Server in derselben Domäne können den Lizenzserver ermitteln.</span><span class="sxs-lookup"><span data-stu-id="044ed-118">RD Session Host servers in the same domain can discover the license server.</span></span> <span data-ttu-id="044ed-119">Sie müssen als Domänen Administrator angemeldet sein, um diesen Wert festzulegen.</span><span class="sxs-lookup"><span data-stu-id="044ed-119">You must be logged on as a domain administrator to set this value.</span></span>

</dd> <dt>

<span data-ttu-id="044ed-120">2</span><span class="sxs-lookup"><span data-stu-id="044ed-120">2</span></span>
</dt> <dd>

<span data-ttu-id="044ed-121">RD-Sitzungshost Server aus mehreren Domänen in derselben Gesamtstruktur können den Lizenzserver ermitteln.</span><span class="sxs-lookup"><span data-stu-id="044ed-121">RD Session Host servers from multiple domains in the same forest can discover the license server.</span></span> <span data-ttu-id="044ed-122">Sie müssen als Unternehmens Administrator angemeldet sein, um diesen Wert festzulegen.</span><span class="sxs-lookup"><span data-stu-id="044ed-122">You must be logged on as an enterprise administrator to set this value.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="044ed-123">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="044ed-123">Return value</span></span>

<span data-ttu-id="044ed-124">Wenn die Methode erfolgreich ist, gibt Sie 0 (null) zurück.</span><span class="sxs-lookup"><span data-stu-id="044ed-124">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="044ed-125">Wenn die Methode nicht erfolgreich ist, wird ein Wert ungleich 0 (null) zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="044ed-125">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="044ed-126">Eine Liste der Fehlercodes finden Sie unter [Remotedesktopdienste Fehlercodes des WMI-Anbieters](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="044ed-126">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="044ed-127">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="044ed-127">Remarks</span></span>

<span data-ttu-id="044ed-128">Sie müssen Mitglied der Gruppe "Administratoren" sein, um diese Methode aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="044ed-128">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="044ed-129">Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen.</span><span class="sxs-lookup"><span data-stu-id="044ed-129">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="044ed-130">MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert.</span><span class="sxs-lookup"><span data-stu-id="044ed-130">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="044ed-131">Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="044ed-131">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="044ed-132">Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="044ed-132">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="044ed-133">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="044ed-133">Requirements</span></span>



| <span data-ttu-id="044ed-134">Anforderung</span><span class="sxs-lookup"><span data-stu-id="044ed-134">Requirement</span></span> | <span data-ttu-id="044ed-135">Wert</span><span class="sxs-lookup"><span data-stu-id="044ed-135">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="044ed-136">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="044ed-136">Minimum supported client</span></span><br/> | <span data-ttu-id="044ed-137">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="044ed-137">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="044ed-138">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="044ed-138">Minimum supported server</span></span><br/> | <span data-ttu-id="044ed-139">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="044ed-139">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="044ed-140">Namespace</span><span class="sxs-lookup"><span data-stu-id="044ed-140">Namespace</span></span><br/>                | <span data-ttu-id="044ed-141">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="044ed-141">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="044ed-142">MOF</span><span class="sxs-lookup"><span data-stu-id="044ed-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="044ed-143"><dt>Tltaumiprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="044ed-143"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="044ed-144">DLL</span><span class="sxs-lookup"><span data-stu-id="044ed-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="044ed-145"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="044ed-145"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="044ed-146">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="044ed-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="044ed-147">**Win32- \_ Lizenznehmer**</span><span class="sxs-lookup"><span data-stu-id="044ed-147">**Win32\_TSLicenseServer**</span></span>](win32-tslicenseserver.md)
</dt> </dl>

 

