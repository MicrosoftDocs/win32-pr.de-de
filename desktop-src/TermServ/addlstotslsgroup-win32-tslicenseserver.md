---
title: Addlstozlsgroup-Methode der Win32_TSLicenseServer-Klasse
description: Fügt den Remotedesktop-Lizenzserver der Gruppe Remotedesktopverbindung Broker (RD-Verbindungsbroker)-Lizenzserver auf einem Domänen Controller in derselben Domäne wie der Remotedesktop Lizenzserver hinzu.
ms.assetid: 65c6b7cf-324a-44f1-8dfc-40e35ed45d4f
ms.tgt_platform: multiple
keywords:
- Addlstozlsgroup-Methode Remotedesktopdienste
- Addlstozlsgroup-Methode Remotedesktopdienste, Win32_TSLicenseServer-Klasse
- Win32_TSLicenseServer-Klasse Remotedesktopdienste, addlstozlsgroup-Methode
topic_type:
- apiref
api_name:
- Win32_TSLicenseServer.AddLStoTSLSGroup
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 53934f6682d1a23f99916588aa4eac3b18526c06
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391752"
---
# <a name="addlstotslsgroup-method-of-the-win32_tslicenseserver-class"></a><span data-ttu-id="40903-106">Addlstozlsgroup-Methode der Win32- \_ Klasse "zlicenseserver"</span><span class="sxs-lookup"><span data-stu-id="40903-106">AddLStoTSLSGroup method of the Win32\_TSLicenseServer class</span></span>

<span data-ttu-id="40903-107">Fügt den Remotedesktop-Lizenzserver der Gruppe Remotedesktopverbindung Broker (RD-Verbindungsbroker)-Lizenzserver auf einem Domänen Controller in derselben Domäne wie der Remotedesktop Lizenzserver hinzu.</span><span class="sxs-lookup"><span data-stu-id="40903-107">Adds the Remote Desktop license server to the Remote Desktop Connection Broker (RD Connection Broker) License Servers group on a domain controller in the same domain as the Remote Desktop license server.</span></span>

## <a name="syntax"></a><span data-ttu-id="40903-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="40903-108">Syntax</span></span>


```mof
uint32 AddLStoTSLSGroup();
```



## <a name="parameters"></a><span data-ttu-id="40903-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="40903-109">Parameters</span></span>

<span data-ttu-id="40903-110">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="40903-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="40903-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="40903-111">Return value</span></span>

<span data-ttu-id="40903-112">Wenn die Methode erfolgreich ist, gibt Sie 0 (null) zurück.</span><span class="sxs-lookup"><span data-stu-id="40903-112">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="40903-113">Wenn die Methode nicht erfolgreich ist, wird ein Wert ungleich 0 (null) zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="40903-113">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="40903-114">Eine Liste der Fehlercodes finden Sie unter [Remotedesktopdienste Fehlercodes des WMI-Anbieters](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="40903-114">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="40903-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="40903-115">Remarks</span></span>

<span data-ttu-id="40903-116">Sie müssen Mitglied der Gruppe "Domänen-Admins" sein, um diese Methode aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="40903-116">You must be a member of the Domain Admins group to call this method.</span></span>

<span data-ttu-id="40903-117">Der Lizenzserver sollte Mitglied der Gruppe Remotedesktop-Lizenzserver sein, wenn der Server für die Verwendung des Domänen-oder Gesamtstruktur-Ermittlungs Bereichs konfiguriert ist.</span><span class="sxs-lookup"><span data-stu-id="40903-117">The license server should be a member of the Remote Desktop license servers group if the server is configured to use the domain or forest discovery scope.</span></span>

<span data-ttu-id="40903-118">Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen.</span><span class="sxs-lookup"><span data-stu-id="40903-118">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="40903-119">MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert.</span><span class="sxs-lookup"><span data-stu-id="40903-119">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="40903-120">Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="40903-120">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="40903-121">Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="40903-121">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="40903-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="40903-122">Requirements</span></span>



| <span data-ttu-id="40903-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="40903-123">Requirement</span></span> | <span data-ttu-id="40903-124">Wert</span><span class="sxs-lookup"><span data-stu-id="40903-124">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="40903-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="40903-125">Minimum supported client</span></span><br/> | <span data-ttu-id="40903-126">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="40903-126">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="40903-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="40903-127">Minimum supported server</span></span><br/> | <span data-ttu-id="40903-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="40903-128">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="40903-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="40903-129">Namespace</span></span><br/>                | <span data-ttu-id="40903-130">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="40903-130">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="40903-131">MOF</span><span class="sxs-lookup"><span data-stu-id="40903-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="40903-132"><dt>Tltaumiprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="40903-132"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="40903-133">DLL</span><span class="sxs-lookup"><span data-stu-id="40903-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="40903-134"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="40903-134"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="40903-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="40903-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="40903-136">**Win32- \_ Lizenznehmer**</span><span class="sxs-lookup"><span data-stu-id="40903-136">**Win32\_TSLicenseServer**</span></span>](win32-tslicenseserver.md)
</dt> <dt>

[<span data-ttu-id="40903-137">**Islsinzlsgroup**</span><span class="sxs-lookup"><span data-stu-id="40903-137">**IsLSinTSLSGroup**</span></span>](islsintslsgroup-win32-tslicenseserver.md)
</dt> </dl>

 

