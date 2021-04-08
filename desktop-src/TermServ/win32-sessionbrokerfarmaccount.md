---
title: Win32_SessionBrokerFarmAccount-Klasse
description: Die Win32- \_ Klasse "sessionbrokerfarmaccount" ist nicht mehr für die Verwendung ab Windows Server 2012 verfügbar. | Win32_SessionBrokerFarmAccount-Klasse
ms.assetid: a76ade0f-cd94-438c-bc07-30dc4b4ee6c8
ms.tgt_platform: multiple
keywords:
- Win32_SessionBrokerFarmAccount-Klasse Remotedesktopdienste
- Win32_SessionBrokerFarmAccount Klasse Remotedesktopdienste, beschrieben
topic_type:
- apiref
api_name:
- Win32_SessionBrokerFarmAccount
- Win32_SessionBrokerFarmAccount.FarmName
- Win32_SessionBrokerFarmAccount.Manual
- Win32_SessionBrokerFarmAccount.AccountName
- Win32_SessionBrokerFarmAccount.AccountDomain
- Win32_SessionBrokerFarmAccount.AccountPassword
- Win32_SessionBrokerFarmAccount.AccountSPN1
- Win32_SessionBrokerFarmAccount.AccountSPN2
- Win32_SessionBrokerFarmAccount.ComputerDNSName
api_location:
- TssdWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a31f076ddc6f9361be12a57dc60ada24ed75e4bb
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "103761850"
---
# <a name="win32_sessionbrokerfarmaccount-class"></a><span data-ttu-id="58875-106">Win32 \_ sessionbrokerfarmaccount-Klasse</span><span class="sxs-lookup"><span data-stu-id="58875-106">Win32\_SessionBrokerFarmAccount class</span></span>

<span data-ttu-id="58875-107">\[Die Win32-Klasse " **\_ sessionbrokerfarmaccount** " ist nicht mehr für die Verwendung ab Windows Server 2012 verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="58875-107">\[The **Win32\_SessionBrokerFarmAccount** class is no longer available for use as of Windows Server 2012.\]</span></span>

<span data-ttu-id="58875-108">Definiert ein Sitzungs Broker-Farmkonto.</span><span class="sxs-lookup"><span data-stu-id="58875-108">Defines a session broker farm account.</span></span>

<span data-ttu-id="58875-109">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="58875-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="58875-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="58875-110">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_WIN32_SESSIONBROKERFARMACCOUNT_Prov"), AMENDMENT]
class Win32_SessionBrokerFarmAccount
{
  string  FarmName;
  boolean Manual;
  string  AccountName;
  string  AccountDomain;
  string  AccountPassword;
  string  AccountSPN1;
  string  AccountSPN2;
  string  ComputerDNSName;
};
```

## <a name="members"></a><span data-ttu-id="58875-111">Member</span><span class="sxs-lookup"><span data-stu-id="58875-111">Members</span></span>

<span data-ttu-id="58875-112">Die Win32-Klasse " **\_ sessionbrokerfarmaccount** " verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="58875-112">The **Win32\_SessionBrokerFarmAccount** class has these types of members:</span></span>

-   [<span data-ttu-id="58875-113">Methoden</span><span class="sxs-lookup"><span data-stu-id="58875-113">Methods</span></span>](#methods)
-   [<span data-ttu-id="58875-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="58875-114">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="58875-115">Methoden</span><span class="sxs-lookup"><span data-stu-id="58875-115">Methods</span></span>

<span data-ttu-id="58875-116">Die Win32-Klasse " **\_ sessionbrokerfarmaccount** " verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="58875-116">The **Win32\_SessionBrokerFarmAccount** class has these methods.</span></span>



| <span data-ttu-id="58875-117">Methode</span><span class="sxs-lookup"><span data-stu-id="58875-117">Method</span></span>                                                      | <span data-ttu-id="58875-118">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="58875-118">Description</span></span>                          |
|:------------------------------------------------------------|:-------------------------------------|
| [<span data-ttu-id="58875-119">**DeleteEx**</span><span class="sxs-lookup"><span data-stu-id="58875-119">**DeleteEx**</span></span>](deleteex-win32-sessionbrokerfarmaccount.md) | <span data-ttu-id="58875-120">Löscht das Farmkonto.</span><span class="sxs-lookup"><span data-stu-id="58875-120">Deletes the farm account.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="58875-121">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="58875-121">Properties</span></span>

<span data-ttu-id="58875-122">Die **Win32 \_ sessionbrokerfarmaccount** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="58875-122">The **Win32\_SessionBrokerFarmAccount** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="58875-123">**AccountDomain**</span><span class="sxs-lookup"><span data-stu-id="58875-123">**AccountDomain**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="58875-124">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="58875-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="58875-125">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="58875-125">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="58875-126">Der Name der Domäne, zu der das Farmkonto gehört.</span><span class="sxs-lookup"><span data-stu-id="58875-126">The name of the domain the farm account belongs to.</span></span>

</dd> <dt>

<span data-ttu-id="58875-127">**AccountName**</span><span class="sxs-lookup"><span data-stu-id="58875-127">**AccountName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="58875-128">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="58875-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="58875-129">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="58875-129">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="58875-130">Der Name des Farm Kontos.</span><span class="sxs-lookup"><span data-stu-id="58875-130">The name of the farm account.</span></span>

</dd> <dt>

<span data-ttu-id="58875-131">**Accountpassword**</span><span class="sxs-lookup"><span data-stu-id="58875-131">**AccountPassword**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="58875-132">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="58875-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="58875-133">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="58875-133">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="58875-134">Das Kennwort des Farm Kontos.</span><span class="sxs-lookup"><span data-stu-id="58875-134">The password of the farm account.</span></span>

</dd> <dt>

<span data-ttu-id="58875-135">**AccountSPN1**</span><span class="sxs-lookup"><span data-stu-id="58875-135">**AccountSPN1**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="58875-136">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="58875-136">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="58875-137">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="58875-137">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="58875-138">Der erste Dienst Prinzipal Name (Service Principal Name, SPN), der dem Farmkonto zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="58875-138">The first service principal name (SPN) associated with the farm account.</span></span>

</dd> <dt>

<span data-ttu-id="58875-139">**AccountSPN2**</span><span class="sxs-lookup"><span data-stu-id="58875-139">**AccountSPN2**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="58875-140">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="58875-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="58875-141">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="58875-141">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="58875-142">Der zweite SPN, der dem Farmkonto zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="58875-142">The second SPN associated with the farm account.</span></span>

</dd> <dt>

<span data-ttu-id="58875-143">**Computerdnsname**</span><span class="sxs-lookup"><span data-stu-id="58875-143">**ComputerDNSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="58875-144">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="58875-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="58875-145">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="58875-145">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="58875-146">Der DNS-Name des Computers, der dem Farmkonto zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="58875-146">The DNS name of the computer associated with the farm account.</span></span>

</dd> <dt>

<span data-ttu-id="58875-147">**Farmname**</span><span class="sxs-lookup"><span data-stu-id="58875-147">**FarmName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="58875-148">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="58875-148">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="58875-149">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="58875-149">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="58875-150">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="58875-150">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="58875-151">Der Name der Sitzungs Broker Farm.</span><span class="sxs-lookup"><span data-stu-id="58875-151">The name of the session broker farm.</span></span>

</dd> <dt>

<span data-ttu-id="58875-152">**Manuell**</span><span class="sxs-lookup"><span data-stu-id="58875-152">**Manual**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="58875-153">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="58875-153">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="58875-154">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="58875-154">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="58875-155">Gibt an, ob das Kennwort für das Konto manuell aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="58875-155">Indicates if the password for the account is updated manually.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="58875-156">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="58875-156">Requirements</span></span>



| <span data-ttu-id="58875-157">Anforderung</span><span class="sxs-lookup"><span data-stu-id="58875-157">Requirement</span></span> | <span data-ttu-id="58875-158">Wert</span><span class="sxs-lookup"><span data-stu-id="58875-158">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="58875-159">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="58875-159">Minimum supported client</span></span><br/> | <span data-ttu-id="58875-160">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="58875-160">None supported</span></span><br/>                                                              |
| <span data-ttu-id="58875-161">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="58875-161">Minimum supported server</span></span><br/> | <span data-ttu-id="58875-162">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="58875-162">Windows Server 2008 R2</span></span><br/>                                                      |
| <span data-ttu-id="58875-163">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="58875-163">End of client support</span></span><br/>    | <span data-ttu-id="58875-164">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="58875-164">None supported</span></span><br/>                                                              |
| <span data-ttu-id="58875-165">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="58875-165">End of server support</span></span><br/>    | <span data-ttu-id="58875-166">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="58875-166">Windows Server 2008 R2</span></span><br/>                                                      |
| <span data-ttu-id="58875-167">Namespace</span><span class="sxs-lookup"><span data-stu-id="58875-167">Namespace</span></span><br/>                | <span data-ttu-id="58875-168">Root \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="58875-168">Root\\CIMv2\\TerminalServices</span></span><br/>                                               |
| <span data-ttu-id="58875-169">MOF</span><span class="sxs-lookup"><span data-stu-id="58875-169">MOF</span></span><br/>                      | <dl> <span data-ttu-id="58875-170"><dt>"Tssdwmi. mof"</dt></span><span class="sxs-lookup"><span data-stu-id="58875-170"><dt>TssdWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="58875-171">DLL</span><span class="sxs-lookup"><span data-stu-id="58875-171">DLL</span></span><br/>                      | <dl> <span data-ttu-id="58875-172"><dt>TssdWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="58875-172"><dt>TssdWmi.dll</dt></span></span> </dl> |



 

