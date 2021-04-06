---
title: Widerruf-Methode der Win32_TSIssuedLicense-Klasse
description: Widerruft die Remotedesktopdienste pro Geräte-Client Zugriffs Lizenzen (RDS \ 160; Pro-Gerät-CALs), die durch das Win32- \_ Objekt "tsissuedlicense" dargestellt werden. Dabei handelt es sich nicht um eine statische Funktion.
ms.assetid: b1eb7448-5d8e-4c2d-ba52-9363e8e0297a
ms.tgt_platform: multiple
keywords:
- Methode widerrufen Remotedesktopdienste
- Methode Remotedesktopdienste widerrufen, Win32_TSIssuedLicense Klasse
- Win32_TSIssuedLicense Klasse Remotedesktopdienste, Methode widerrufen
topic_type:
- apiref
api_name:
- Win32_TSIssuedLicense.Revoke
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 63993ede5346f5b3cb56fcfa458d4cdce7dd58b8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743624"
---
# <a name="revoke-method-of-the-win32_tsissuedlicense-class"></a><span data-ttu-id="133eb-107">Widerruf-Methode der Win32- \_ Klasse "tsissuedlicense"</span><span class="sxs-lookup"><span data-stu-id="133eb-107">Revoke method of the Win32\_TSIssuedLicense class</span></span>

<span data-ttu-id="133eb-108">Widerruft die Remotedesktopdienste pro Geräte-Client Zugriffs Lizenzen (RDS pro Gerät CALs), die durch das Win32-Objekt " [**\_ tsissuedlicense**](win32-tsissuedlicense.md) " dargestellt werden.</span><span class="sxs-lookup"><span data-stu-id="133eb-108">Revokes the Remote Desktop Services Per Device client access licenses (RDS Per Device CALs) that are represented by the [**Win32\_TSIssuedLicense**](win32-tsissuedlicense.md) object.</span></span> <span data-ttu-id="133eb-109">Dabei handelt es sich nicht um eine statische Funktion.</span><span class="sxs-lookup"><span data-stu-id="133eb-109">This is not a static function.</span></span>

## <a name="syntax"></a><span data-ttu-id="133eb-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="133eb-110">Syntax</span></span>


```mof
uint32 Revoke(
  [out] uint32   RevokableCals,
  [out] DATETIME NextRevokeAllowedOn
);
```



## <a name="parameters"></a><span data-ttu-id="133eb-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="133eb-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="133eb-112">*Revokablecals* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="133eb-112">*RevokableCals* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="133eb-113">Anzahl der RDS-CALs desselben Typs wie das aktuelle Objekt, das widerrufen werden kann.</span><span class="sxs-lookup"><span data-stu-id="133eb-113">Number of RDS CALs of the same type as the current object that can be revoked.</span></span>

</dd> <dt>

<span data-ttu-id="133eb-114">*Nextrevokezuweisung* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="133eb-114">*NextRevokeAllowedOn* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="133eb-115">Datum, an dem der Administrator das nächste Mal versuchen kann, Lizenzen aufzuheben.</span><span class="sxs-lookup"><span data-stu-id="133eb-115">Date that the administrator can next try to revoke licenses.</span></span> <span data-ttu-id="133eb-116">Dieser Parameter enthält nur gültige Daten, wenn der **Widerruf** Methoden Aufrufwert fehlgeschlagen ist, da die maximale Anzahl von Sperren erreicht wurde.</span><span class="sxs-lookup"><span data-stu-id="133eb-116">This parameter only contains valid data when the **Revoke** method call has failed because the maximum revoke count has been reached.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="133eb-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="133eb-117">Remarks</span></span>

<span data-ttu-id="133eb-118">Sie müssen Mitglied der Gruppe "Administratoren" sein, um diese Methode aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="133eb-118">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="133eb-119">Nur RDS-CALs pro Gerät können widerrufen werden.</span><span class="sxs-lookup"><span data-stu-id="133eb-119">Only RDS Per Device CALs can be revoked.</span></span>

<span data-ttu-id="133eb-120">Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen.</span><span class="sxs-lookup"><span data-stu-id="133eb-120">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="133eb-121">MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert.</span><span class="sxs-lookup"><span data-stu-id="133eb-121">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="133eb-122">Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="133eb-122">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="133eb-123">Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="133eb-123">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="133eb-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="133eb-124">Requirements</span></span>



| <span data-ttu-id="133eb-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="133eb-125">Requirement</span></span> | <span data-ttu-id="133eb-126">Wert</span><span class="sxs-lookup"><span data-stu-id="133eb-126">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="133eb-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="133eb-127">Minimum supported client</span></span><br/> | <span data-ttu-id="133eb-128">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="133eb-128">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="133eb-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="133eb-129">Minimum supported server</span></span><br/> | <span data-ttu-id="133eb-130">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="133eb-130">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="133eb-131">Namespace</span><span class="sxs-lookup"><span data-stu-id="133eb-131">Namespace</span></span><br/>                | <span data-ttu-id="133eb-132">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="133eb-132">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="133eb-133">MOF</span><span class="sxs-lookup"><span data-stu-id="133eb-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="133eb-134"><dt>Tltaumiprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="133eb-134"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="133eb-135">DLL</span><span class="sxs-lookup"><span data-stu-id="133eb-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="133eb-136"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="133eb-136"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="133eb-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="133eb-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="133eb-138">**Win32-" \_ tsissuedlicense"**</span><span class="sxs-lookup"><span data-stu-id="133eb-138">**Win32\_TSIssuedLicense**</span></span>](win32-tsissuedlicense.md)
</dt> </dl>

 

