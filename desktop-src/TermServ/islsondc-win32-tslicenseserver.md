---
title: Islsondc-Methode der Win32_TSLicenseServer-Klasse
description: Ruft ab, ob Remotedesktop Lizenzierung (RD-Lizenzierung) auf einem Domänen Controller installiert ist.
ms.assetid: 43345dc8-c8b6-4c41-b26d-781293d07516
ms.tgt_platform: multiple
keywords:
- Islsondc-Methode Remotedesktopdienste
- Islsondc-Methode Remotedesktopdienste, Win32_TSLicenseServer-Klasse
- Win32_TSLicenseServer-Klasse Remotedesktopdienste, islsondc-Methode
topic_type:
- apiref
api_name:
- Win32_TSLicenseServer.IsLSonDC
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 03ddbf01615903150ffa8f97fca88cfcf7fda937
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956666"
---
# <a name="islsondc-method-of-the-win32_tslicenseserver-class"></a><span data-ttu-id="c0d96-106">Islsondc-Methode der Win32- \_ Klasse "zlicenseserver"</span><span class="sxs-lookup"><span data-stu-id="c0d96-106">IsLSonDC method of the Win32\_TSLicenseServer class</span></span>

<span data-ttu-id="c0d96-107">Ruft ab, ob Remotedesktop Lizenzierung (RD-Lizenzierung) auf einem Domänen Controller installiert ist.</span><span class="sxs-lookup"><span data-stu-id="c0d96-107">Retrieves whether Remote Desktop Licensing (RD Licensing) is installed on a domain controller.</span></span>

## <a name="syntax"></a><span data-ttu-id="c0d96-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="c0d96-108">Syntax</span></span>


```mof
uint32 IsLSonDC(
  [out] boolean OnDC
);
```



## <a name="parameters"></a><span data-ttu-id="c0d96-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="c0d96-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c0d96-110">*Ondc* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="c0d96-110">*OnDC* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c0d96-111">Boolescher Wert, der angibt, ob RD-Lizenzierung auf einem Domänen Controller installiert ist.</span><span class="sxs-lookup"><span data-stu-id="c0d96-111">Boolean value that indicates whether RD Licensing is installed on a domain controller.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c0d96-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c0d96-112">Return value</span></span>

<span data-ttu-id="c0d96-113">Wenn die Methode erfolgreich ist, gibt Sie 0 (null) zurück.</span><span class="sxs-lookup"><span data-stu-id="c0d96-113">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="c0d96-114">Wenn die Methode nicht erfolgreich ist, wird ein Wert ungleich 0 (null) zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="c0d96-114">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="c0d96-115">Eine Liste der Fehlercodes finden Sie unter [Remotedesktopdienste Fehlercodes des WMI-Anbieters](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="c0d96-115">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="c0d96-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c0d96-116">Remarks</span></span>

<span data-ttu-id="c0d96-117">Sie müssen Mitglied der Gruppe "Administratoren" sein, um diese Methode aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="c0d96-117">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="c0d96-118">Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen.</span><span class="sxs-lookup"><span data-stu-id="c0d96-118">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="c0d96-119">MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert.</span><span class="sxs-lookup"><span data-stu-id="c0d96-119">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="c0d96-120">Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="c0d96-120">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="c0d96-121">Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="c0d96-121">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="c0d96-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c0d96-122">Requirements</span></span>



| <span data-ttu-id="c0d96-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c0d96-123">Requirement</span></span> | <span data-ttu-id="c0d96-124">Wert</span><span class="sxs-lookup"><span data-stu-id="c0d96-124">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="c0d96-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c0d96-125">Minimum supported client</span></span><br/> | <span data-ttu-id="c0d96-126">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="c0d96-126">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="c0d96-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c0d96-127">Minimum supported server</span></span><br/> | <span data-ttu-id="c0d96-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c0d96-128">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="c0d96-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="c0d96-129">Namespace</span></span><br/>                | <span data-ttu-id="c0d96-130">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="c0d96-130">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="c0d96-131">MOF</span><span class="sxs-lookup"><span data-stu-id="c0d96-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c0d96-132"><dt>Tltaumiprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="c0d96-132"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="c0d96-133">DLL</span><span class="sxs-lookup"><span data-stu-id="c0d96-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c0d96-134"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c0d96-134"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c0d96-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c0d96-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c0d96-136">**Win32- \_ Lizenznehmer**</span><span class="sxs-lookup"><span data-stu-id="c0d96-136">**Win32\_TSLicenseServer**</span></span>](win32-tslicenseserver.md)
</dt> </dl>

 

