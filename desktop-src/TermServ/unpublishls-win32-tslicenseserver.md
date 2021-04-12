---
title: Unpublishls-Methode der Win32_TSLicenseServer-Klasse
description: Veröffentlichung eines Remotedesktop Lizenzservers aus Active Directory Domain Services.
ms.assetid: 275854e2-85f6-4142-8bce-8d633bfcff7d
ms.tgt_platform: multiple
keywords:
- Unpublishls-Methode Remotedesktopdienste
- Unpublishls-Methode Remotedesktopdienste, Win32_TSLicenseServer-Klasse
- Win32_TSLicenseServer-Klasse Remotedesktopdienste, unpublishls-Methode
topic_type:
- apiref
api_name:
- Win32_TSLicenseServer.UnpublishLS
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d1ec183b5be8055dc30add5bc00a7eb537cd20f8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518014"
---
# <a name="unpublishls-method-of-the-win32_tslicenseserver-class"></a><span data-ttu-id="a21d3-106">Unpublishls-Methode der Win32- \_ Klasse "zlicenseserver"</span><span class="sxs-lookup"><span data-stu-id="a21d3-106">UnpublishLS method of the Win32\_TSLicenseServer class</span></span>

<span data-ttu-id="a21d3-107">Veröffentlichung eines Remotedesktop Lizenzservers aus Active Directory Domain Services.</span><span class="sxs-lookup"><span data-stu-id="a21d3-107">Unpublishes a Remote Desktop license server from Active Directory Domain Services.</span></span>

## <a name="syntax"></a><span data-ttu-id="a21d3-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="a21d3-108">Syntax</span></span>


```mof
uint32 UnpublishLS();
```



## <a name="parameters"></a><span data-ttu-id="a21d3-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="a21d3-109">Parameters</span></span>

<span data-ttu-id="a21d3-110">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="a21d3-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="a21d3-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a21d3-111">Return value</span></span>

<span data-ttu-id="a21d3-112">Wenn die Methode erfolgreich ist, gibt Sie 0 (null) zurück.</span><span class="sxs-lookup"><span data-stu-id="a21d3-112">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="a21d3-113">Wenn die Methode nicht erfolgreich ist, wird ein Wert ungleich 0 (null) zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="a21d3-113">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="a21d3-114">Eine Liste der Fehlercodes finden Sie unter [Remotedesktopdienste Fehlercodes des WMI-Anbieters](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="a21d3-114">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="a21d3-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a21d3-115">Remarks</span></span>

<span data-ttu-id="a21d3-116">Um diese Methode aufzurufen, müssen Sie als Unternehmens Administrator an der Gesamtstruktur angemeldet sein, in der der Lizenzserver Mitglied ist.</span><span class="sxs-lookup"><span data-stu-id="a21d3-116">To call this method, you must be logged on as an enterprise administrator to the forest in which the license server is a member.</span></span>

<span data-ttu-id="a21d3-117">Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen.</span><span class="sxs-lookup"><span data-stu-id="a21d3-117">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="a21d3-118">MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert.</span><span class="sxs-lookup"><span data-stu-id="a21d3-118">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="a21d3-119">Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="a21d3-119">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="a21d3-120">Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="a21d3-120">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="a21d3-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a21d3-121">Requirements</span></span>



| <span data-ttu-id="a21d3-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a21d3-122">Requirement</span></span> | <span data-ttu-id="a21d3-123">Wert</span><span class="sxs-lookup"><span data-stu-id="a21d3-123">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="a21d3-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a21d3-124">Minimum supported client</span></span><br/> | <span data-ttu-id="a21d3-125">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="a21d3-125">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="a21d3-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a21d3-126">Minimum supported server</span></span><br/> | <span data-ttu-id="a21d3-127">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a21d3-127">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="a21d3-128">Namespace</span><span class="sxs-lookup"><span data-stu-id="a21d3-128">Namespace</span></span><br/>                | <span data-ttu-id="a21d3-129">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="a21d3-129">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="a21d3-130">MOF</span><span class="sxs-lookup"><span data-stu-id="a21d3-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a21d3-131"><dt>Tltaumiprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="a21d3-131"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="a21d3-132">DLL</span><span class="sxs-lookup"><span data-stu-id="a21d3-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a21d3-133"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a21d3-133"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a21d3-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a21d3-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a21d3-135">**Win32- \_ Lizenznehmer**</span><span class="sxs-lookup"><span data-stu-id="a21d3-135">**Win32\_TSLicenseServer**</span></span>](win32-tslicenseserver.md)
</dt> </dl>

 

