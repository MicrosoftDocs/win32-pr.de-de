---
title: Istsintscgroup-Methode der Win32_TSLicenseServer-Klasse
description: Ruft ab, ob ein Remotedesktop-Sitzungshost (RD-Sitzungshost)-Server Mitglied der lokalen Gruppe "Terminal Server Computer" auf dem Remotedesktop-Lizenzserver ist.
ms.assetid: 61c39928-3a2b-4a36-ae4e-b9597a12d5e7
ms.tgt_platform: multiple
keywords:
- Istsintscgroup-Methode Remotedesktopdienste
- Istsintscgroup-Methode Remotedesktopdienste, Win32_TSLicenseServer-Klasse
- Win32_TSLicenseServer-Klasse Remotedesktopdienste, istsintscgroup-Methode
topic_type:
- apiref
api_name:
- Win32_TSLicenseServer.IsTSinTSCGroup
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d666457f053c8fd48abd904d099bfbfa93a0de6d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518830"
---
# <a name="istsintscgroup-method-of-the-win32_tslicenseserver-class"></a><span data-ttu-id="b3f0a-106">Istsintscgroup-Methode der Win32- \_ Klasse "zlicenseserver"</span><span class="sxs-lookup"><span data-stu-id="b3f0a-106">IsTSinTSCGroup method of the Win32\_TSLicenseServer class</span></span>

<span data-ttu-id="b3f0a-107">Ruft ab, ob ein Remotedesktop-Sitzungshost (RD-Sitzungshost)-Server Mitglied der lokalen Gruppe "Terminal Server Computer" auf dem Remotedesktop-Lizenzserver ist.</span><span class="sxs-lookup"><span data-stu-id="b3f0a-107">Retrieves whether a Remote Desktop Session Host (RD Session Host) server is a member of the Terminal Server Computers local group on the Remote Desktop license server.</span></span>

## <a name="syntax"></a><span data-ttu-id="b3f0a-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="b3f0a-108">Syntax</span></span>


```mof
uint32 IsTSinTSCGroup(
  [in]  string  tsname,
  [out] boolean IsMember
);
```



## <a name="parameters"></a><span data-ttu-id="b3f0a-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="b3f0a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b3f0a-110">*zname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b3f0a-110">*tsname* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b3f0a-111">Der Name des RD-Sitzungshost Servers.</span><span class="sxs-lookup"><span data-stu-id="b3f0a-111">Name of the RD Session Host server.</span></span>

</dd> <dt>

<span data-ttu-id="b3f0a-112">*IsMember* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="b3f0a-112">*IsMember* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b3f0a-113">Boolescher Wert, der angibt, ob der RD-Sitzungshost Server Mitglied der lokalen Gruppe "Terminal Server Computer" ist.</span><span class="sxs-lookup"><span data-stu-id="b3f0a-113">Boolean value that indicates whether the RD Session Host server is a member of the Terminal Server Computers local group.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b3f0a-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b3f0a-114">Return value</span></span>

<span data-ttu-id="b3f0a-115">Wenn die Methode erfolgreich ist, gibt Sie 0 (null) zurück.</span><span class="sxs-lookup"><span data-stu-id="b3f0a-115">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="b3f0a-116">Wenn die Methode nicht erfolgreich ist, wird ein Wert ungleich 0 (null) zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="b3f0a-116">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="b3f0a-117">Eine Liste der Fehlercodes finden Sie unter [Remotedesktopdienste Fehlercodes des WMI-Anbieters](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="b3f0a-117">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="b3f0a-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b3f0a-118">Remarks</span></span>

<span data-ttu-id="b3f0a-119">Sie müssen Mitglied der Gruppe "Administratoren" sein, um diese Methode aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="b3f0a-119">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="b3f0a-120">Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen.</span><span class="sxs-lookup"><span data-stu-id="b3f0a-120">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="b3f0a-121">MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert.</span><span class="sxs-lookup"><span data-stu-id="b3f0a-121">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="b3f0a-122">Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="b3f0a-122">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="b3f0a-123">Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="b3f0a-123">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="b3f0a-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b3f0a-124">Requirements</span></span>



| <span data-ttu-id="b3f0a-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b3f0a-125">Requirement</span></span> | <span data-ttu-id="b3f0a-126">Wert</span><span class="sxs-lookup"><span data-stu-id="b3f0a-126">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="b3f0a-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b3f0a-127">Minimum supported client</span></span><br/> | <span data-ttu-id="b3f0a-128">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="b3f0a-128">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="b3f0a-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b3f0a-129">Minimum supported server</span></span><br/> | <span data-ttu-id="b3f0a-130">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b3f0a-130">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="b3f0a-131">Namespace</span><span class="sxs-lookup"><span data-stu-id="b3f0a-131">Namespace</span></span><br/>                | <span data-ttu-id="b3f0a-132">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="b3f0a-132">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="b3f0a-133">MOF</span><span class="sxs-lookup"><span data-stu-id="b3f0a-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b3f0a-134"><dt>Tltaumiprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="b3f0a-134"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="b3f0a-135">DLL</span><span class="sxs-lookup"><span data-stu-id="b3f0a-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b3f0a-136"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b3f0a-136"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b3f0a-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b3f0a-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b3f0a-138">**Win32- \_ Lizenznehmer**</span><span class="sxs-lookup"><span data-stu-id="b3f0a-138">**Win32\_TSLicenseServer**</span></span>](win32-tslicenseserver.md)
</dt> </dl>

 

