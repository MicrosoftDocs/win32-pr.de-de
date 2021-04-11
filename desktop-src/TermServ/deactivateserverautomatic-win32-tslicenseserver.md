---
title: Deactivateserverautomatic-Methode der Win32_TSLicenseServer-Klasse
description: Deaktiviert den Remotedesktop Lizenzserver über das Internet.
ms.assetid: 6e049d7f-1753-484d-98b8-fde66d16b5ab
ms.tgt_platform: multiple
keywords:
- Deactivateserverautomatic-Methode Remotedesktopdienste
- Deactivateserverautomatic-Methode Remotedesktopdienste, Win32_TSLicenseServer-Klasse
- Win32_TSLicenseServer-Klasse Remotedesktopdienste, deactivateserverautomatic-Methode
topic_type:
- apiref
api_name:
- Win32_TSLicenseServer.DeactivateServerAutomatic
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d466b5f7814d6004bafdd01bce161a481eacf26a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040270"
---
# <a name="deactivateserverautomatic-method-of-the-win32_tslicenseserver-class"></a><span data-ttu-id="eda79-106">Deactivateserverautomatic-Methode der Win32- \_ Klasse "zlicenseserver"</span><span class="sxs-lookup"><span data-stu-id="eda79-106">DeactivateServerAutomatic method of the Win32\_TSLicenseServer class</span></span>

<span data-ttu-id="eda79-107">Deaktiviert den Remotedesktop Lizenzserver über das Internet.</span><span class="sxs-lookup"><span data-stu-id="eda79-107">Deactivates the Remote Desktop license server over the Internet.</span></span>

## <a name="syntax"></a><span data-ttu-id="eda79-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="eda79-108">Syntax</span></span>


```mof
uint32 DeactivateServerAutomatic(
  [out] uint32 ActivationStatus
);
```



## <a name="parameters"></a><span data-ttu-id="eda79-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="eda79-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eda79-110">*Activationstatus* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="eda79-110">*ActivationStatus* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="eda79-111">Der zurückgegebene Aktivierungs Status kann einer der folgenden sein.</span><span class="sxs-lookup"><span data-stu-id="eda79-111">The activation status returned can be one of the following.</span></span>

<dt>

<span data-ttu-id="eda79-112">0</span><span class="sxs-lookup"><span data-stu-id="eda79-112">0</span></span>
</dt> <dd>

<span data-ttu-id="eda79-113">Der Remotedesktop Lizenzserver wird aktiviert.</span><span class="sxs-lookup"><span data-stu-id="eda79-113">The Remote Desktop license server is activated.</span></span>

</dd> <dt>

<span data-ttu-id="eda79-114">1</span><span class="sxs-lookup"><span data-stu-id="eda79-114">1</span></span>
</dt> <dd>

<span data-ttu-id="eda79-115">Der Remotedesktop Lizenzserver ist nicht aktiviert.</span><span class="sxs-lookup"><span data-stu-id="eda79-115">The Remote Desktop license server is not activated.</span></span>

</dd> <dt>

<span data-ttu-id="eda79-116">2</span><span class="sxs-lookup"><span data-stu-id="eda79-116">2</span></span>
</dt> <dd>

<span data-ttu-id="eda79-117">Es ist ein unbekannter Fehler aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="eda79-117">An unknown error occurred.</span></span> <span data-ttu-id="eda79-118">Es ist nicht bekannt, ob der Remotedesktop Lizenzserver aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="eda79-118">It is not known whether the Remote Desktop license server is activated.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eda79-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="eda79-119">Return value</span></span>

<span data-ttu-id="eda79-120">Wenn die Methode erfolgreich ist, gibt Sie 0 (null) zurück.</span><span class="sxs-lookup"><span data-stu-id="eda79-120">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="eda79-121">Wenn die Methode nicht erfolgreich ist, wird ein Wert ungleich 0 (null) zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="eda79-121">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="eda79-122">Eine Liste der Fehlercodes finden Sie unter [Remotedesktopdienste Fehlercodes des WMI-Anbieters](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="eda79-122">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="eda79-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="eda79-123">Remarks</span></span>

<span data-ttu-id="eda79-124">Sie müssen Mitglied der Gruppe "Administratoren" sein, um diese Methode aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="eda79-124">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="eda79-125">Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen.</span><span class="sxs-lookup"><span data-stu-id="eda79-125">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="eda79-126">MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert.</span><span class="sxs-lookup"><span data-stu-id="eda79-126">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="eda79-127">Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="eda79-127">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="eda79-128">Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="eda79-128">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="eda79-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="eda79-129">Requirements</span></span>



| <span data-ttu-id="eda79-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="eda79-130">Requirement</span></span> | <span data-ttu-id="eda79-131">Wert</span><span class="sxs-lookup"><span data-stu-id="eda79-131">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="eda79-132">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="eda79-132">Minimum supported client</span></span><br/> | <span data-ttu-id="eda79-133">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="eda79-133">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="eda79-134">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="eda79-134">Minimum supported server</span></span><br/> | <span data-ttu-id="eda79-135">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="eda79-135">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="eda79-136">Namespace</span><span class="sxs-lookup"><span data-stu-id="eda79-136">Namespace</span></span><br/>                | <span data-ttu-id="eda79-137">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="eda79-137">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="eda79-138">MOF</span><span class="sxs-lookup"><span data-stu-id="eda79-138">MOF</span></span><br/>                      | <dl> <span data-ttu-id="eda79-139"><dt>Tltaumiprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="eda79-139"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="eda79-140">DLL</span><span class="sxs-lookup"><span data-stu-id="eda79-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="eda79-141"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="eda79-141"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eda79-142">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="eda79-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eda79-143">**Win32- \_ Lizenznehmer**</span><span class="sxs-lookup"><span data-stu-id="eda79-143">**Win32\_TSLicenseServer**</span></span>](win32-tslicenseserver.md)
</dt> </dl>

 

