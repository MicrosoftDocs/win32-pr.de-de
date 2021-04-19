---
title: Islspublished-Methode der Win32_TSLicenseServer-Klasse
description: Ruft ab, ob der Remotedesktop Lizenzserver in Active Directory Domain Services (AD \ 160; DS) veröffentlicht wird.
ms.assetid: 0e97c9df-5cb0-4e28-8436-08093a8667d9
ms.tgt_platform: multiple
keywords:
- Islspublished-Methode Remotedesktopdienste
- Islspublished-Methode Remotedesktopdienste, Win32_TSLicenseServer-Klasse
- Win32_TSLicenseServer-Klasse Remotedesktopdienste, islspublished-Methode
topic_type:
- apiref
api_name:
- Win32_TSLicenseServer.IsLSPublished
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 69add751497ed52a107ea7183bb4b7cce4ea88c1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106339979"
---
# <a name="islspublished-method-of-the-win32_tslicenseserver-class"></a><span data-ttu-id="5082b-106">Islspublished-Methode der Win32- \_ Klasse "zlicenseserver"</span><span class="sxs-lookup"><span data-stu-id="5082b-106">IsLSPublished method of the Win32\_TSLicenseServer class</span></span>

<span data-ttu-id="5082b-107">Ruft ab, ob der Remotedesktop Lizenzserver in Active Directory Domain Services (AD DS) veröffentlicht wird.</span><span class="sxs-lookup"><span data-stu-id="5082b-107">Retrieves whether the Remote Desktop license server is published in Active Directory Domain Services (AD DS).</span></span>

## <a name="syntax"></a><span data-ttu-id="5082b-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="5082b-108">Syntax</span></span>


```mof
uint32 IsLSPublished(
  [out] boolean Published
);
```



## <a name="parameters"></a><span data-ttu-id="5082b-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="5082b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5082b-110">*Veröffentlicht* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="5082b-110">*Published* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5082b-111">Boolescher Wert, der angibt, ob der Lizenzserver in AD DS veröffentlicht wird.</span><span class="sxs-lookup"><span data-stu-id="5082b-111">Boolean value that indicates whether the license server is published in AD DS.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5082b-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5082b-112">Return value</span></span>

<span data-ttu-id="5082b-113">Wenn die Methode erfolgreich ist, gibt Sie 0 (null) zurück.</span><span class="sxs-lookup"><span data-stu-id="5082b-113">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="5082b-114">Wenn die Methode nicht erfolgreich ist, wird ein Wert ungleich 0 (null) zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="5082b-114">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="5082b-115">Eine Liste der Fehlercodes finden Sie unter [Remotedesktopdienste Fehlercodes des WMI-Anbieters](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="5082b-115">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="5082b-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5082b-116">Remarks</span></span>

<span data-ttu-id="5082b-117">Sie müssen Mitglied der Gruppe "Administratoren" sein, um diese Methode aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="5082b-117">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="5082b-118">Wenn der Lizenzserver in AD DS veröffentlicht wird, kann er automatisch durch Remotedesktop-Sitzungshost (RD-Sitzungshost)-Server in derselben Gesamtstruktur erkannt werden.</span><span class="sxs-lookup"><span data-stu-id="5082b-118">If the license server is published in AD DS, it will be automatically discoverable by Remote Desktop Session Host (RD Session Host) servers in the same forest.</span></span>

<span data-ttu-id="5082b-119">Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen.</span><span class="sxs-lookup"><span data-stu-id="5082b-119">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="5082b-120">MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert.</span><span class="sxs-lookup"><span data-stu-id="5082b-120">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="5082b-121">Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="5082b-121">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="5082b-122">Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="5082b-122">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="5082b-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5082b-123">Requirements</span></span>



| <span data-ttu-id="5082b-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5082b-124">Requirement</span></span> | <span data-ttu-id="5082b-125">Wert</span><span class="sxs-lookup"><span data-stu-id="5082b-125">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="5082b-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5082b-126">Minimum supported client</span></span><br/> | <span data-ttu-id="5082b-127">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="5082b-127">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="5082b-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5082b-128">Minimum supported server</span></span><br/> | <span data-ttu-id="5082b-129">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5082b-129">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="5082b-130">Namespace</span><span class="sxs-lookup"><span data-stu-id="5082b-130">Namespace</span></span><br/>                | <span data-ttu-id="5082b-131">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="5082b-131">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="5082b-132">MOF</span><span class="sxs-lookup"><span data-stu-id="5082b-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5082b-133"><dt>Tltaumiprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="5082b-133"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="5082b-134">DLL</span><span class="sxs-lookup"><span data-stu-id="5082b-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5082b-135"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5082b-135"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5082b-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5082b-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5082b-137">**Win32- \_ Lizenznehmer**</span><span class="sxs-lookup"><span data-stu-id="5082b-137">**Win32\_TSLicenseServer**</span></span>](win32-tslicenseserver.md)
</dt> </dl>

 

