---
title: Getlicenseserverid-Methode der Win32_TSLicenseServer-Klasse
description: Ruft den Remotedesktop-Lizenzserver Bezeichner ab, wenn der Server zurzeit aktiviert ist.
ms.assetid: 0eb2cf82-3632-4693-97d2-0cfa814d8c94
ms.tgt_platform: multiple
keywords:
- Getlicenseserverid-Methode Remotedesktopdienste
- Getlicenseserverid-Methode Remotedesktopdienste, Win32_TSLicenseServer-Klasse
- Win32_TSLicenseServer-Klasse Remotedesktopdienste, getlicenseserverid-Methode
topic_type:
- apiref
api_name:
- Win32_TSLicenseServer.GetLicenseServerId
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 43a5883a5a52a0d111959e1f9fc1cbe9da5357d2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391747"
---
# <a name="getlicenseserverid-method-of-the-win32_tslicenseserver-class"></a><span data-ttu-id="5c2d6-106">Getlicenseserverid-Methode der Win32- \_ Klasse "zlicenseserver"</span><span class="sxs-lookup"><span data-stu-id="5c2d6-106">GetLicenseServerId method of the Win32\_TSLicenseServer class</span></span>

<span data-ttu-id="5c2d6-107">Ruft den Remotedesktop-Lizenzserver Bezeichner ab, wenn der Server zurzeit aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="5c2d6-107">Retrieves the Remote Desktop license server identifier if the server is currently activated.</span></span>

## <a name="syntax"></a><span data-ttu-id="5c2d6-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="5c2d6-108">Syntax</span></span>


```mof
uint32 GetLicenseServerId(
  [out] string sLicenseServerId
);
```



## <a name="parameters"></a><span data-ttu-id="5c2d6-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="5c2d6-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5c2d6-110">*slicenseserverid* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="5c2d6-110">*sLicenseServerId* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5c2d6-111">Remotedesktop-Lizenzserver Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="5c2d6-111">Remote Desktop license server identifier.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5c2d6-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5c2d6-112">Return value</span></span>

<span data-ttu-id="5c2d6-113">Wenn die Methode erfolgreich ist, gibt Sie 0 (null) zurück.</span><span class="sxs-lookup"><span data-stu-id="5c2d6-113">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="5c2d6-114">Wenn die Methode nicht erfolgreich ist, wird ein Wert ungleich 0 (null) zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="5c2d6-114">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="5c2d6-115">Eine Liste der Fehlercodes finden Sie unter [Remotedesktopdienste Fehlercodes des WMI-Anbieters](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="5c2d6-115">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="5c2d6-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5c2d6-116">Remarks</span></span>

<span data-ttu-id="5c2d6-117">Sie müssen Mitglied der Gruppe "Administratoren" sein, um diese Methode aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="5c2d6-117">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="5c2d6-118">Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen.</span><span class="sxs-lookup"><span data-stu-id="5c2d6-118">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="5c2d6-119">MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert.</span><span class="sxs-lookup"><span data-stu-id="5c2d6-119">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="5c2d6-120">Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="5c2d6-120">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="5c2d6-121">Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="5c2d6-121">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="5c2d6-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5c2d6-122">Requirements</span></span>



| <span data-ttu-id="5c2d6-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5c2d6-123">Requirement</span></span> | <span data-ttu-id="5c2d6-124">Wert</span><span class="sxs-lookup"><span data-stu-id="5c2d6-124">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="5c2d6-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5c2d6-125">Minimum supported client</span></span><br/> | <span data-ttu-id="5c2d6-126">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="5c2d6-126">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="5c2d6-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5c2d6-127">Minimum supported server</span></span><br/> | <span data-ttu-id="5c2d6-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5c2d6-128">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="5c2d6-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="5c2d6-129">Namespace</span></span><br/>                | <span data-ttu-id="5c2d6-130">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="5c2d6-130">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="5c2d6-131">MOF</span><span class="sxs-lookup"><span data-stu-id="5c2d6-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5c2d6-132"><dt>Tltaumiprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="5c2d6-132"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="5c2d6-133">DLL</span><span class="sxs-lookup"><span data-stu-id="5c2d6-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5c2d6-134"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5c2d6-134"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5c2d6-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5c2d6-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5c2d6-136">**Win32- \_ Lizenznehmer**</span><span class="sxs-lookup"><span data-stu-id="5c2d6-136">**Win32\_TSLicenseServer**</span></span>](win32-tslicenseserver.md)
</dt> </dl>

 

