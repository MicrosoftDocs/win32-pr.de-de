---
description: Stellt die Einstellungen für die Terminaldienste des virtuellen Computers auf einem Host dar.
ms.assetid: 1f8d0718-09da-4231-95eb-cc63b6f324dd
title: Msvm_TerminalServiceSettingData-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_TerminalServiceSettingData
- Msvm_TerminalServiceSettingData.InstanceID
- Msvm_TerminalServiceSettingData.Caption
- Msvm_TerminalServiceSettingData.Description
- Msvm_TerminalServiceSettingData.ElementName
- Msvm_TerminalServiceSettingData.ListenerPort
- Msvm_TerminalServiceSettingData.DisableSelfSignedCertificateGeneration
- Msvm_TerminalServiceSettingData.AuthCertificateHash
- Msvm_TerminalServiceSettingData.TrustedIssuerCertificateHashes
- Msvm_TerminalServiceSettingData.AllowedHashAlgorithms
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 27d98971c847eab5042823e8a1524051a15fd679
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103753560"
---
# <a name="msvm_terminalservicesettingdata-class"></a><span data-ttu-id="8d455-103">MSVM \_ terminalservicesettingdata-Klasse</span><span class="sxs-lookup"><span data-stu-id="8d455-103">Msvm\_TerminalServiceSettingData class</span></span>

<span data-ttu-id="8d455-104">Stellt die Einstellungen für die Terminaldienste des virtuellen Computers auf einem Host dar.</span><span class="sxs-lookup"><span data-stu-id="8d455-104">Represents the settings for the virtual computer terminal services on a host.</span></span> <span data-ttu-id="8d455-105">Die Eigenschaften für diese Klasse können nicht direkt geändert werden.</span><span class="sxs-lookup"><span data-stu-id="8d455-105">The properties for this class cannot be modified directly.</span></span> <span data-ttu-id="8d455-106">Der Client muss die [**MSVM \_ Terminalservice. modifyservicesettings**](modifyservicesettings-msvm-terminalservice.md) -Methode abrufen, um diese Eigenschaften zu ändern.</span><span class="sxs-lookup"><span data-stu-id="8d455-106">The client must call the [**Msvm\_TerminalService.ModifyServiceSettings**](modifyservicesettings-msvm-terminalservice.md) method to modify any of these properties.</span></span>

<span data-ttu-id="8d455-107">Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="8d455-107">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="8d455-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="8d455-108">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_TerminalServiceSettingData : CIM_SettingData
{
  string  InstanceID;
  string  Caption = "Hyper-V Terminal Service Settings";
  string  Description = "Settings for the Hyper-V Terminal Service";
  string  ElementName = "Hyper-V Terminal Service Settings";
  uint32  ListenerPort;
  boolean DisableSelfSignedCertificateGeneration;
  uint8   AuthCertificateHash[];
  string  TrustedIssuerCertificateHashes[];
  string  AllowedHashAlgorithms[];
};
```

## <a name="members"></a><span data-ttu-id="8d455-109">Member</span><span class="sxs-lookup"><span data-stu-id="8d455-109">Members</span></span>

<span data-ttu-id="8d455-110">Die **MSVM \_ terminalservicesettingdata** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="8d455-110">The **Msvm\_TerminalServiceSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="8d455-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="8d455-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="8d455-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="8d455-112">Properties</span></span>

<span data-ttu-id="8d455-113">Die **MSVM \_ terminalservicesettingdata** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="8d455-113">The **Msvm\_TerminalServiceSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="8d455-114">**AllowedHashAlgorithms**</span><span class="sxs-lookup"><span data-stu-id="8d455-114">**AllowedHashAlgorithms**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8d455-115">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="8d455-115">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="8d455-116">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8d455-116">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8d455-117">Die Liste der Hash Algorithmen, die zum Überprüfen der Signatur von Verbund Authentifizierungs Token akzeptiert werden.</span><span class="sxs-lookup"><span data-stu-id="8d455-117">The list of hash algorithms accepted for verifying the signature of federated authentication tokens.</span></span>

<span data-ttu-id="8d455-118">**Windows 8.1:** Dieser Wert wird bis Windows 8.1 und Windows Server 2012 R2 nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="8d455-118">**Windows 8.1:** This value is not supported until Windows 8.1 and Windows Server 2012 R2.</span></span>

</dd> <dt>

<span data-ttu-id="8d455-119">**Authcertifialisiehash**</span><span class="sxs-lookup"><span data-stu-id="8d455-119">**AuthCertificateHash**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8d455-120">Datentyp: **Uint8** Array</span><span class="sxs-lookup"><span data-stu-id="8d455-120">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="8d455-121">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8d455-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8d455-122">Der Hash des Zertifikats, das für die Remote Authentifizierung verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="8d455-122">The hash of the certificate to use for remote authentication.</span></span>

</dd> <dt>

<span data-ttu-id="8d455-123">**Caption**</span><span class="sxs-lookup"><span data-stu-id="8d455-123">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8d455-124">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="8d455-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8d455-125">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8d455-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8d455-126">Eine kurze Beschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="8d455-126">A short description of the object.</span></span> <span data-ttu-id="8d455-127">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="8d455-127">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="8d455-128">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="8d455-128">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8d455-129">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="8d455-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8d455-130">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8d455-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8d455-131">Eine Beschreibung des -Objekts.</span><span class="sxs-lookup"><span data-stu-id="8d455-131">A description of the object.</span></span> <span data-ttu-id="8d455-132">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="8d455-132">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="8d455-133">**Disableselfsignedcertificategeneration**</span><span class="sxs-lookup"><span data-stu-id="8d455-133">**DisableSelfSignedCertificateGeneration**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8d455-134">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="8d455-134">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="8d455-135">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8d455-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8d455-136">Deaktiviert die Generierung eines selbst signierten Zertifikats.</span><span class="sxs-lookup"><span data-stu-id="8d455-136">Disables self-signed certificate generation.</span></span>

</dd> <dt>

<span data-ttu-id="8d455-137">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="8d455-137">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8d455-138">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="8d455-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8d455-139">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8d455-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8d455-140">Ein Anzeige Name für das-Objekt.</span><span class="sxs-lookup"><span data-stu-id="8d455-140">A display name for the object.</span></span> <span data-ttu-id="8d455-141">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="8d455-141">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="8d455-142">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="8d455-142">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8d455-143">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="8d455-143">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8d455-144">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8d455-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8d455-145">Qualifizierer: **Schlüssel**</span><span class="sxs-lookup"><span data-stu-id="8d455-145">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="8d455-146">Identifiziert eine Instanz dieser Klasse eindeutig.</span><span class="sxs-lookup"><span data-stu-id="8d455-146">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="8d455-147">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="8d455-147">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="8d455-148">**Eigenschaften**</span><span class="sxs-lookup"><span data-stu-id="8d455-148">**ListenerPort**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8d455-149">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8d455-149">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8d455-150">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8d455-150">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8d455-151">Der Netzwerkport, auf dem die anfängliche Remote Sitzungs Verbindung hergestellt wird.</span><span class="sxs-lookup"><span data-stu-id="8d455-151">The network port on which the initial remote session connection will be made.</span></span>

</dd> <dt>

<span data-ttu-id="8d455-152">**TrustedIssuerCertificateHashes**</span><span class="sxs-lookup"><span data-stu-id="8d455-152">**TrustedIssuerCertificateHashes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8d455-153">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="8d455-153">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="8d455-154">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8d455-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8d455-155">Die Liste der vertrauenswürdigen Aussteller-zertifikathashes zum Überprüfen der Signatur von Verbund Authentifizierungs Token.</span><span class="sxs-lookup"><span data-stu-id="8d455-155">The list of trusted issuer certificate hashes for verifying the signature of federated authentication tokens.</span></span>

<span data-ttu-id="8d455-156">**Windows 8.1:** Dieser Wert wird bis Windows 8.1 und Windows Server 2012 R2 nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="8d455-156">**Windows 8.1:** This value is not supported until Windows 8.1 and Windows Server 2012 R2.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8d455-157">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8d455-157">Requirements</span></span>



| <span data-ttu-id="8d455-158">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8d455-158">Requirement</span></span> | <span data-ttu-id="8d455-159">Wert</span><span class="sxs-lookup"><span data-stu-id="8d455-159">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8d455-160">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="8d455-160">Minimum supported client</span></span><br/> | <span data-ttu-id="8d455-161">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8d455-161">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="8d455-162">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="8d455-162">Minimum supported server</span></span><br/> | <span data-ttu-id="8d455-163">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8d455-163">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="8d455-164">Namespace</span><span class="sxs-lookup"><span data-stu-id="8d455-164">Namespace</span></span><br/>                | <span data-ttu-id="8d455-165">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="8d455-165">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="8d455-166">MOF</span><span class="sxs-lookup"><span data-stu-id="8d455-166">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8d455-167"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="8d455-167"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="8d455-168">DLL</span><span class="sxs-lookup"><span data-stu-id="8d455-168">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8d455-169"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="8d455-169"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

