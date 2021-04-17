---
title: Win32_TSLicenseKeyPack-Klasse
description: Stellt Methoden und Eigenschaften zum Anzeigen und installieren Remotedesktopdienste Lizenzschlüssel Packs bereit.
ms.assetid: 27450646-c51f-4911-bb42-410794e32003
ms.tgt_platform: multiple
keywords:
- Win32_TSLicenseKeyPack-Klasse Remotedesktopdienste
- Win32_TSLicenseKeyPack Klasse Remotedesktopdienste, beschrieben
topic_type:
- apiref
api_name:
- Win32_TSLicenseKeyPack
- Win32_TSLicenseKeyPack.KeyPackId
- Win32_TSLicenseKeyPack.Description
- Win32_TSLicenseKeyPack.KeyPackType
- Win32_TSLicenseKeyPack.ProductType
- Win32_TSLicenseKeyPack.ProductVersion
- Win32_TSLicenseKeyPack.ProductVersionID
- Win32_TSLicenseKeyPack.TotalLicenses
- Win32_TSLicenseKeyPack.IssuedLicenses
- Win32_TSLicenseKeyPack.AvailableLicenses
- Win32_TSLicenseKeyPack.ExpirationDate
- Win32_TSLicenseKeyPack.AccessRights
- Win32_TSLicenseKeyPack.TypeAndModel
api_location:
- TlsWmiProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9d78af398ebf7c137be5b31c9db427691a66a7a2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517402"
---
# <a name="win32_tslicensekeypack-class"></a><span data-ttu-id="5c9e3-105">Win32- \_ Klasse "slicenabkeypack"</span><span class="sxs-lookup"><span data-stu-id="5c9e3-105">Win32\_TSLicenseKeyPack class</span></span>

<span data-ttu-id="5c9e3-106">Stellt Methoden und Eigenschaften zum Anzeigen und installieren Remotedesktopdienste Lizenzschlüssel Packs bereit.</span><span class="sxs-lookup"><span data-stu-id="5c9e3-106">Provides methods and properties for viewing and installing Remote Desktop Services license key packs.</span></span>

## <a name="syntax"></a><span data-ttu-id="5c9e3-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="5c9e3-107">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_WIN32_TERMSERVLICENSING_Prov"), AMENDMENT]
class Win32_TSLicenseKeyPack
{
  uint32   KeyPackId;
  string   Description;
  uint32   KeyPackType;
  uint32   ProductType;
  string   ProductVersion;
  uint32   ProductVersionID;
  uint32   TotalLicenses;
  uint32   IssuedLicenses;
  uint32   AvailableLicenses;
  DATETIME ExpirationDate;
  uint32   AccessRights;
  string   TypeAndModel;
};
```

## <a name="members"></a><span data-ttu-id="5c9e3-108">Member</span><span class="sxs-lookup"><span data-stu-id="5c9e3-108">Members</span></span>

<span data-ttu-id="5c9e3-109">Die Win32-Klasse " **\_ zlicentarkeypack** " verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="5c9e3-109">The **Win32\_TSLicenseKeyPack** class has these types of members:</span></span>

-   [<span data-ttu-id="5c9e3-110">Methoden</span><span class="sxs-lookup"><span data-stu-id="5c9e3-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="5c9e3-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="5c9e3-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="5c9e3-112">Methoden</span><span class="sxs-lookup"><span data-stu-id="5c9e3-112">Methods</span></span>

<span data-ttu-id="5c9e3-113">Die Win32-Klasse " **\_ zlicenabkeypack** " verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="5c9e3-113">The **Win32\_TSLicenseKeyPack** class has these methods.</span></span>



| <span data-ttu-id="5c9e3-114">Methode</span><span class="sxs-lookup"><span data-stu-id="5c9e3-114">Method</span></span>                                                                                                        | <span data-ttu-id="5c9e3-115">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5c9e3-115">Description</span></span>                                                                                                                                                                                                                               |
|:--------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5c9e3-116">**Convertlicenses**</span><span class="sxs-lookup"><span data-stu-id="5c9e3-116">**ConvertLicenses**</span></span>](convertlicenses-win32-tslicensekeypack.md)                                             | <span data-ttu-id="5c9e3-117">Konvertiert die Lizenzen im aktuellen Schlüssel Paket.</span><span class="sxs-lookup"><span data-stu-id="5c9e3-117">Converts the licenses in the current key pack.</span></span><br/>                                                                                                                                                                                 |
| [<span data-ttu-id="5c9e3-118">**Importagreementlicenskeypack**</span><span class="sxs-lookup"><span data-stu-id="5c9e3-118">**ImportAgreementLicenseKeyPack**</span></span>](win32-tslicensekeypack-importagreementlicensekeypack.md)                 | <span data-ttu-id="5c9e3-119">Importe von einem anderen Remotedesktop Lizenzserver, ein Remotedesktopdienste Lizenzschlüssel Paket, das über einen Lizenzvertrag gekauft wurde, und die automatische Verbindung über das Internet, um die Key Pack-Lizenz zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="5c9e3-119">Imports, from another Remote Desktop license server, a Remote Desktop Services license key pack that was purchased through a license agreement, and automatically connects over the Internet to validate the key pack license.</span></span><br/> |
| [<span data-ttu-id="5c9e3-120">**Importlicenabkeypackoffline**</span><span class="sxs-lookup"><span data-stu-id="5c9e3-120">**ImportLicenseKeyPackOffline**</span></span>](win32-tslicensekeypack-importlicensekeypackoffline.md)                     | <span data-ttu-id="5c9e3-121">Importe von einem anderen Remotedesktop Lizenzserver, ein Remotedesktopdienste License Key Pack, das eine Lizenz-ID verwendet, die über das Internet oder das Telefon empfangen wurde.</span><span class="sxs-lookup"><span data-stu-id="5c9e3-121">Imports, from another Remote Desktop license server, a Remote Desktop Services license key pack that uses a license identifier that was received over the Internet or the phone.</span></span><br/>                                               |
| [<span data-ttu-id="5c9e3-122">**Importopenpurchaselicenabkeypack**</span><span class="sxs-lookup"><span data-stu-id="5c9e3-122">**ImportOpenPurchaseLicenseKeyPack**</span></span>](win32-tslicensekeypack-importopenpurchaselicensekeypack.md)           | <span data-ttu-id="5c9e3-123">Importe von einem anderen Remotedesktop Lizenzserver, einem Open License Remotedesktopdienste License Key Pack.</span><span class="sxs-lookup"><span data-stu-id="5c9e3-123">Imports, from another Remote Desktop license server, an Open License Remote Desktop Services license key pack.</span></span><br/>                                                                                                                 |
| [<span data-ttu-id="5c9e3-124">**Importretailpurchaselicenzkeypack**</span><span class="sxs-lookup"><span data-stu-id="5c9e3-124">**ImportRetailPurchaseLicenseKeyPack**</span></span>](win32-tslicensekeypack-importretailpurchaselicensekeypack.md)       | <span data-ttu-id="5c9e3-125">Importe von einem anderen Remotedesktop Lizenzserver, ein Remotedesktopdienste Lizenzschlüssel Paket, das über einen einzelhandelskanal gekauft wurde.</span><span class="sxs-lookup"><span data-stu-id="5c9e3-125">Imports, from another Remote Desktop license server, a Remote Desktop Services license key pack that was purchased through a retail channel.</span></span><br/>                                                                                   |
| [<span data-ttu-id="5c9e3-126">**Installagreementlicenskeypack**</span><span class="sxs-lookup"><span data-stu-id="5c9e3-126">**InstallAgreementLicenseKeyPack**</span></span>](installagreementlicensekeypack-win32-tslicensekeypack.md)               | <span data-ttu-id="5c9e3-127">Installiert ein Remotedesktopdienste Lizenzschlüssel Paket, das über eine Vertrags Lizenz erworben wurde.</span><span class="sxs-lookup"><span data-stu-id="5c9e3-127">Installs a Remote Desktop Services license key pack that was purchased through an agreement license.</span></span><br/>                                                                                                                           |
| [<span data-ttu-id="5c9e3-128">**Installlicenskeypack**</span><span class="sxs-lookup"><span data-stu-id="5c9e3-128">**InstallLicenseKeyPack**</span></span>](installlicensekeypack-win32-tslicensekeypack.md)                                 | <span data-ttu-id="5c9e3-129">Installiert ein Remotedesktopdienste Lizenzschlüssel Paket, das eine Lizenzschlüssel Paket-ID verwendet, die über das Internet oder das Telefon empfangen wurde.</span><span class="sxs-lookup"><span data-stu-id="5c9e3-129">Installs a Remote Desktop Services license key pack that uses a license key pack ID that was received over the Internet or the phone.</span></span><br/>                                                                                          |
| [<span data-ttu-id="5c9e3-130">**Installopenlicenskeypack**</span><span class="sxs-lookup"><span data-stu-id="5c9e3-130">**InstallOpenLicenseKeyPack**</span></span>](installopenlicensekeypack-win32-tslicensekeypack.md)                         | <span data-ttu-id="5c9e3-131">Installiert ein Remotedesktopdienste Lizenzschlüssel Paket, das über einen offenen Lizenzvertrag gekauft wurde.</span><span class="sxs-lookup"><span data-stu-id="5c9e3-131">Installs a Remote Desktop Services license key pack that was purchased through an open license agreement.</span></span><br/>                                                                                                                      |
| [<span data-ttu-id="5c9e3-132">**Installretailpurchaselicen\keypack**</span><span class="sxs-lookup"><span data-stu-id="5c9e3-132">**InstallRetailPurchaseLicenseKeyPack**</span></span>](installretailpurchaselicensekeypack-win32-tslicensekeypack.md)     | <span data-ttu-id="5c9e3-133">Installiert ein Remotedesktopdienste Lizenzschlüssel Paket, das über einen Einzelhandels Speicher gekauft wurde.</span><span class="sxs-lookup"><span data-stu-id="5c9e3-133">Installs a Remote Desktop Services license key pack that was purchased through a retail store.</span></span><br/>                                                                                                                                 |
| [<span data-ttu-id="5c9e3-134">**Reinstallagreementlicenskeypack**</span><span class="sxs-lookup"><span data-stu-id="5c9e3-134">**ReinstallAgreementLicenseKeyPack**</span></span>](win32-tslicensekeypack-reinstallagreementlicensekeypack.md)           | <span data-ttu-id="5c9e3-135">Installiert ein Remotedesktopdienste Lizenzschlüssel Paket neu, das über einen Lizenzvertrag gekauft wurde, und stellt automatisch eine Verbindung über das Internet her, um die Key Pack-Lizenz zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="5c9e3-135">Reinstalls a Remote Desktop Services license key pack that was purchased through a license agreement, and automatically connects over the Internet to validate the key pack license.</span></span><br/>                                           |
| [<span data-ttu-id="5c9e3-136">**Reinstalllicenumkeypackoffline**</span><span class="sxs-lookup"><span data-stu-id="5c9e3-136">**ReinstallLicenseKeyPackOffline**</span></span>](win32-tslicensekeypack-reinstalllicensekeypackoffline.md)               | <span data-ttu-id="5c9e3-137">Installiert ein Remotedesktopdienste Lizenzschlüssel Paket, das die über das Internet oder das Telefon empfangene Lizenz-ID verwendet.</span><span class="sxs-lookup"><span data-stu-id="5c9e3-137">Reinstalls a Remote Desktop Services license key pack that uses the license identifier that was received over the Internet or the phone.</span></span><br/>                                                                                       |
| [<span data-ttu-id="5c9e3-138">**Reinstallopenpurchaselicenskeypack**</span><span class="sxs-lookup"><span data-stu-id="5c9e3-138">**ReinstallOpenPurchaseLicenseKeyPack**</span></span>](win32-tslicensekeypack-reinstallopenpurchaselicensekeypack.md)     | <span data-ttu-id="5c9e3-139">Installiert ein Open License Remotedesktopdienste License Key Pack neu.</span><span class="sxs-lookup"><span data-stu-id="5c9e3-139">Reinstalls an Open License Remote Desktop Services license key pack.</span></span><br/>                                                                                                                                                           |
| [<span data-ttu-id="5c9e3-140">**Reinstallretailpurchaselicen\keypack**</span><span class="sxs-lookup"><span data-stu-id="5c9e3-140">**ReinstallRetailPurchaseLicenseKeyPack**</span></span>](win32-tslicensekeypack-reinstallretailpurchaselicensekeypack.md) | <span data-ttu-id="5c9e3-141">Neuinstallation eines Remotedesktopdienste Lizenzschlüssel Pakets, das über einen einzelhandelskanal gekauft wurde.</span><span class="sxs-lookup"><span data-stu-id="5c9e3-141">Reinstalls a Remote Desktop Services license key pack that was purchased through a retail channel.</span></span><br/>                                                                                                                             |
| [<span data-ttu-id="5c9e3-142">**Removelicenseswithidcount**</span><span class="sxs-lookup"><span data-stu-id="5c9e3-142">**RemoveLicensesWithIdCount**</span></span>](win32-tslicensekeypack-removelicenseswithidcount.md)                         | <span data-ttu-id="5c9e3-143">Entfernt die angegebene Anzahl von Remotedesktopdienste Lizenzen aus dem angegebenen Schlüssel Paket.</span><span class="sxs-lookup"><span data-stu-id="5c9e3-143">Removes the specified number of Remote Desktop Services licenses from the specified key pack.</span></span><br/>                                                                                                                                  |
| [<span data-ttu-id="5c9e3-144">**Uninstalllicenabkeypack**</span><span class="sxs-lookup"><span data-stu-id="5c9e3-144">**UninstallLicenseKeyPack**</span></span>](win32-tslicensekeypack-uninstalllicensekeypack.md)                             | <span data-ttu-id="5c9e3-145">Deinstalliert ein Remotedesktopdienste License Key Pack.</span><span class="sxs-lookup"><span data-stu-id="5c9e3-145">Uninstalls a Remote Desktop Services license key pack.</span></span><br/>                                                                                                                                                                         |
| [<span data-ttu-id="5c9e3-146">**Uninstalllicenabkeypackwithid**</span><span class="sxs-lookup"><span data-stu-id="5c9e3-146">**UninstallLicenseKeyPackWithId**</span></span>](win32-tslicensekeypack-uninstalllicensekeypackwithid.md)                 | <span data-ttu-id="5c9e3-147">Deinstalliert das Remotedesktopdienste License Key Pack mit der angegebenen Key Pack-Kennung.</span><span class="sxs-lookup"><span data-stu-id="5c9e3-147">Uninstalls the Remote Desktop Services license key pack with the specified key pack identifier.</span></span><br/>                                                                                                                                |



 

### <a name="properties"></a><span data-ttu-id="5c9e3-148">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="5c9e3-148">Properties</span></span>

<span data-ttu-id="5c9e3-149">Die Win32-Klasse " **\_ slicenabkeypack** " verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="5c9e3-149">The **Win32\_TSLicenseKeyPack** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="5c9e3-150">**AccessRights**</span><span class="sxs-lookup"><span data-stu-id="5c9e3-150">**AccessRights**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c9e3-151">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5c9e3-151">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5c9e3-152">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="5c9e3-152">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5c9e3-153">Qualifizierer: [**Bitmap**](/windows/desktop/WmiSdk/standard-qualifiers) ("0", "1", "2", "3"), [**BitValues**](/windows/desktop/WmiSdk/standard-qualifiers) ("RD-Sitzung", "VDI-Sitzung", "Calista", "VDI-Partner")</span><span class="sxs-lookup"><span data-stu-id="5c9e3-153">Qualifiers: [**BitMap**](/windows/desktop/WmiSdk/standard-qualifiers) ("0", "1", "2", "3"), [**BitValues**](/windows/desktop/WmiSdk/standard-qualifiers) ("RD Session", "VDI Session", "Calista", "VDI Partners")</span></span>
</dt> </dl>

<span data-ttu-id="5c9e3-154">Qualifizierer für Terminaldienstelizenzierungs-Schlüssel Paket</span><span class="sxs-lookup"><span data-stu-id="5c9e3-154">Qualifier for TS Licensing key pack access rights</span></span>

</dd> <dt>

<span data-ttu-id="5c9e3-155">**Availablelicenses**</span><span class="sxs-lookup"><span data-stu-id="5c9e3-155">**AvailableLicenses**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c9e3-156">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5c9e3-156">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5c9e3-157">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="5c9e3-157">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5c9e3-158">Die Gesamtanzahl der verfügbaren Lizenzen im Remotedesktopdienste License Key Pack.</span><span class="sxs-lookup"><span data-stu-id="5c9e3-158">Total number of available licenses in the Remote Desktop Services license key pack.</span></span>

</dd> <dt>

<span data-ttu-id="5c9e3-159">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="5c9e3-159">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c9e3-160">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="5c9e3-160">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5c9e3-161">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="5c9e3-161">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5c9e3-162">Die Beschreibung des Remotedesktopdienste License Key Pack.</span><span class="sxs-lookup"><span data-stu-id="5c9e3-162">Description of the Remote Desktop Services license key pack.</span></span>

</dd> <dt>

<span data-ttu-id="5c9e3-163">**ExpirationDate**</span><span class="sxs-lookup"><span data-stu-id="5c9e3-163">**ExpirationDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c9e3-164">**[Datentyp: DateTime](/windows/desktop/WmiSdk/datetime)**</span><span class="sxs-lookup"><span data-stu-id="5c9e3-164">Data type: **[DATETIME](/windows/desktop/WmiSdk/datetime)**</span></span>
</dt> <dt>

<span data-ttu-id="5c9e3-165">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="5c9e3-165">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5c9e3-166">Das Ablaufdatum des Remotedesktopdienste License Key Pack.</span><span class="sxs-lookup"><span data-stu-id="5c9e3-166">The expiration date of the Remote Desktop Services license key pack.</span></span>

</dd> <dt>

<span data-ttu-id="5c9e3-167">**Issuedlicenses**</span><span class="sxs-lookup"><span data-stu-id="5c9e3-167">**IssuedLicenses**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c9e3-168">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5c9e3-168">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5c9e3-169">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="5c9e3-169">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5c9e3-170">Die Gesamtanzahl der ausgestellten Lizenzen im Remotedesktopdienste License Key Pack.</span><span class="sxs-lookup"><span data-stu-id="5c9e3-170">Total number of issued licenses in the Remote Desktop Services license key pack.</span></span>

</dd> <dt>

<span data-ttu-id="5c9e3-171">**Keypackid**</span><span class="sxs-lookup"><span data-stu-id="5c9e3-171">**KeyPackId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c9e3-172">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5c9e3-172">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5c9e3-173">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="5c9e3-173">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5c9e3-174">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="5c9e3-174">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="5c9e3-175">Bezeichner für das Remotedesktopdienste License Key Pack.</span><span class="sxs-lookup"><span data-stu-id="5c9e3-175">Identifier for the Remote Desktop Services license key pack.</span></span>

</dd> <dt>

<span data-ttu-id="5c9e3-176">**Keypacktype**</span><span class="sxs-lookup"><span data-stu-id="5c9e3-176">**KeyPackType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c9e3-177">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5c9e3-177">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5c9e3-178">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="5c9e3-178">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5c9e3-179">Der Typ des Schlüssel Pakets für den Remotedesktop-Lizenzserver.</span><span class="sxs-lookup"><span data-stu-id="5c9e3-179">Type of key pack for the Remote Desktop license server.</span></span>

| <span data-ttu-id="5c9e3-180">Wert</span><span class="sxs-lookup"><span data-stu-id="5c9e3-180">Value</span></span> | <span data-ttu-id="5c9e3-181">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5c9e3-181">Description</span></span> |
|-------|-------------|
| <span data-ttu-id="5c9e3-182">0</span><span class="sxs-lookup"><span data-stu-id="5c9e3-182">0</span></span> | <span data-ttu-id="5c9e3-183">Der Typ Remotedesktopdienste License Key Pack ist unbekannt.</span><span class="sxs-lookup"><span data-stu-id="5c9e3-183">The Remote Desktop Services license key pack type is unknown.</span></span> |
| <span data-ttu-id="5c9e3-184">1</span><span class="sxs-lookup"><span data-stu-id="5c9e3-184">1</span></span> | <span data-ttu-id="5c9e3-185">Der Typ der Remotedesktopdienste License Key Pack ist ein Einzelhandels Einkauf.</span><span class="sxs-lookup"><span data-stu-id="5c9e3-185">The Remote Desktop Services license key pack type is a retail purchase.</span></span> |
| <span data-ttu-id="5c9e3-186">2</span><span class="sxs-lookup"><span data-stu-id="5c9e3-186">2</span></span> | <span data-ttu-id="5c9e3-187">Der Typ Remotedesktopdienste License Key Pack ist ein Volume Purchase.</span><span class="sxs-lookup"><span data-stu-id="5c9e3-187">The Remote Desktop Services license key pack type is a volume purchase.</span></span> |
| <span data-ttu-id="5c9e3-188">3</span><span class="sxs-lookup"><span data-stu-id="5c9e3-188">3</span></span> | <span data-ttu-id="5c9e3-189">Der Remotedesktopdienste License Key Pack-Typ ist eine gleichzeitige Lizenz.</span><span class="sxs-lookup"><span data-stu-id="5c9e3-189">The Remote Desktop Services license key pack type is a concurrent license.</span></span> |
| <span data-ttu-id="5c9e3-190">4</span><span class="sxs-lookup"><span data-stu-id="5c9e3-190">4</span></span> | <span data-ttu-id="5c9e3-191">Der Typ Remotedesktopdienste License Key Pack ist temporär.</span><span class="sxs-lookup"><span data-stu-id="5c9e3-191">The Remote Desktop Services license key pack type is temporary.</span></span> |
| <span data-ttu-id="5c9e3-192">5</span><span class="sxs-lookup"><span data-stu-id="5c9e3-192">5</span></span> | <span data-ttu-id="5c9e3-193">Der Remotedesktopdienste License Key Pack-Typ ist eine offene Lizenz.</span><span class="sxs-lookup"><span data-stu-id="5c9e3-193">The Remote Desktop Services license key pack type is an open license.</span></span> |
| <span data-ttu-id="5c9e3-194">6</span><span class="sxs-lookup"><span data-stu-id="5c9e3-194">6</span></span> | <span data-ttu-id="5c9e3-195">Wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="5c9e3-195">Not supported.</span></span> |

<span data-ttu-id="5c9e3-196">**ProductType**</span><span class="sxs-lookup"><span data-stu-id="5c9e3-196">**ProductType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c9e3-197">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5c9e3-197">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5c9e3-198">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="5c9e3-198">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5c9e3-199">Der Produkttyp des Remotedesktopdienste License Key Pack.</span><span class="sxs-lookup"><span data-stu-id="5c9e3-199">Product type of the Remote Desktop Services license key pack.</span></span>

| <span data-ttu-id="5c9e3-200">Wert</span><span class="sxs-lookup"><span data-stu-id="5c9e3-200">Value</span></span> | <span data-ttu-id="5c9e3-201">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5c9e3-201">Description</span></span> |
|-------|-------------|
| <span data-ttu-id="5c9e3-202">0</span><span class="sxs-lookup"><span data-stu-id="5c9e3-202">0</span></span> | <span data-ttu-id="5c9e3-203">Der Produkttyp Remotedesktopdienste License Key Pack ist pro Gerät.</span><span class="sxs-lookup"><span data-stu-id="5c9e3-203">The Remote Desktop Services license key pack product type is per device.</span></span> <span data-ttu-id="5c9e3-204">Daher muss jedes Gerät, das eine Verbindung mit dem RD-Sitzungshost Server herstellt, über eine Lizenz verfügen.</span><span class="sxs-lookup"><span data-stu-id="5c9e3-204">Therefore, each device that connects to the RD Session Host server must have a license.</span></span> |
| <span data-ttu-id="5c9e3-205">1</span><span class="sxs-lookup"><span data-stu-id="5c9e3-205">1</span></span> | <span data-ttu-id="5c9e3-206">Der Product Type für Remotedesktopdienste License Key Pack ist pro Benutzer.</span><span class="sxs-lookup"><span data-stu-id="5c9e3-206">The Remote Desktop Services license key pack product type is per user.</span></span> <span data-ttu-id="5c9e3-207">Daher muss jeder Benutzer, der eine Verbindung mit dem RD-Sitzungshost Server herstellt, über eine Lizenz verfügen.</span><span class="sxs-lookup"><span data-stu-id="5c9e3-207">Therefore, each user who connects to the RD Session Host server must have a license.</span></span> |
| <span data-ttu-id="5c9e3-208">2</span><span class="sxs-lookup"><span data-stu-id="5c9e3-208">2</span></span> | <span data-ttu-id="5c9e3-209">Der Produkttyp ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="5c9e3-209">This product type is not valid.</span></span> |

<span data-ttu-id="5c9e3-210">**ProductVersion**</span><span class="sxs-lookup"><span data-stu-id="5c9e3-210">**ProductVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c9e3-211">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="5c9e3-211">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5c9e3-212">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="5c9e3-212">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5c9e3-213">Produktversion für das Remotedesktopdienste License Key Pack.</span><span class="sxs-lookup"><span data-stu-id="5c9e3-213">Product version for the Remote Desktop Services license key pack.</span></span>

| <span data-ttu-id="5c9e3-214">Wert</span><span class="sxs-lookup"><span data-stu-id="5c9e3-214">Value</span></span> | <span data-ttu-id="5c9e3-215">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5c9e3-215">Description</span></span> |
|-------|-------------|
| <span data-ttu-id="5c9e3-216">"Windows Server 2012"</span><span class="sxs-lookup"><span data-stu-id="5c9e3-216">"Windows Server 2012"</span></span> | <span data-ttu-id="5c9e3-217">Nur Server, auf denen Windows Server 2012, Windows Server 2008 R2 oder Windows Server 2008 ausgeführt wird, werden mit dieser Lizenz unterstützt.</span><span class="sxs-lookup"><span data-stu-id="5c9e3-217">Only servers running Windows Server 2012, Windows Server 2008 R2, or Windows Server 2008 are supported with this license.</span></span> |
| <span data-ttu-id="5c9e3-218">"Windows Server 7"</span><span class="sxs-lookup"><span data-stu-id="5c9e3-218">"Windows Server 7"</span></span> | <span data-ttu-id="5c9e3-219">Nur Server, auf denen Windows Server 2008 R2 oder Windows Server 2008 ausgeführt wird, werden mit dieser Lizenz unterstützt.</span><span class="sxs-lookup"><span data-stu-id="5c9e3-219">Only servers running Windows Server 2008 R2, or Windows Server 2008 are supported with this license.</span></span> |
| <span data-ttu-id="5c9e3-220">"Windows Server 2008"</span><span class="sxs-lookup"><span data-stu-id="5c9e3-220">"Windows Server 2008"</span></span> | <span data-ttu-id="5c9e3-221">Nur Server, auf denen Windows Server 2008 ausgeführt wird, werden von diesem Schlüssel Paket unterstützt.</span><span class="sxs-lookup"><span data-stu-id="5c9e3-221">Only servers running Windows Server 2008 are supported by this key pack.</span></span> |

<span data-ttu-id="5c9e3-222">**Productversionid**</span><span class="sxs-lookup"><span data-stu-id="5c9e3-222">**ProductVersionID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c9e3-223">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5c9e3-223">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5c9e3-224">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="5c9e3-224">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5c9e3-225">Die Produkt Versions Kennung für das Remotedesktopdienste License Key Pack.</span><span class="sxs-lookup"><span data-stu-id="5c9e3-225">Product version identifier for the Remote Desktop Services license key pack.</span></span>

| <span data-ttu-id="5c9e3-226">Wert</span><span class="sxs-lookup"><span data-stu-id="5c9e3-226">Value</span></span> | <span data-ttu-id="5c9e3-227">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5c9e3-227">Description</span></span> |
|-------|-------------|
| <span data-ttu-id="5c9e3-228">0</span><span class="sxs-lookup"><span data-stu-id="5c9e3-228">0</span></span> | <span data-ttu-id="5c9e3-229">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="5c9e3-229">Not supported</span></span> |
| <span data-ttu-id="5c9e3-230">1</span><span class="sxs-lookup"><span data-stu-id="5c9e3-230">1</span></span> | <span data-ttu-id="5c9e3-231">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="5c9e3-231">Not supported</span></span> |
| <span data-ttu-id="5c9e3-232">2</span><span class="sxs-lookup"><span data-stu-id="5c9e3-232">2</span></span> | <span data-ttu-id="5c9e3-233">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5c9e3-233">Windows Server 2008</span></span> |
| <span data-ttu-id="5c9e3-234">3</span><span class="sxs-lookup"><span data-stu-id="5c9e3-234">3</span></span> | <span data-ttu-id="5c9e3-235">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="5c9e3-235">Windows Server 2008 R2</span></span> |
| <span data-ttu-id="5c9e3-236">4</span><span class="sxs-lookup"><span data-stu-id="5c9e3-236">4</span></span> | <span data-ttu-id="5c9e3-237">Windows Server 2012/Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="5c9e3-237">Windows Server 2012/Windows Server 2012 R2</span></span> |
| <span data-ttu-id="5c9e3-238">5</span><span class="sxs-lookup"><span data-stu-id="5c9e3-238">5</span></span> | <span data-ttu-id="5c9e3-239">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="5c9e3-239">Windows Server 2016</span></span> |
| <span data-ttu-id="5c9e3-240">6</span><span class="sxs-lookup"><span data-stu-id="5c9e3-240">6</span></span> | <span data-ttu-id="5c9e3-241">Windows Server 2019</span><span class="sxs-lookup"><span data-stu-id="5c9e3-241">Windows Server 2019</span></span> |

<span data-ttu-id="5c9e3-242">**Totallicenses**</span><span class="sxs-lookup"><span data-stu-id="5c9e3-242">**TotalLicenses**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c9e3-243">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5c9e3-243">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5c9e3-244">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="5c9e3-244">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5c9e3-245">Die Gesamtanzahl der Lizenzen im Remotedesktopdienste License Key Pack.</span><span class="sxs-lookup"><span data-stu-id="5c9e3-245">Total number of licenses in the Remote Desktop Services license key pack.</span></span>

</dd> <dt>

<span data-ttu-id="5c9e3-246">**Typeandmodel**</span><span class="sxs-lookup"><span data-stu-id="5c9e3-246">**TypeAndModel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c9e3-247">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="5c9e3-247">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5c9e3-248">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="5c9e3-248">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5c9e3-249">Qualifizierer für Terminaldienstelizenzierungs-Key Pack-Typ</span><span class="sxs-lookup"><span data-stu-id="5c9e3-249">Qualifier for TS Licensing key pack type and model.</span></span> <span data-ttu-id="5c9e3-250">Beispiele: VDI pro Geräte Abonnementlizenz, TS pro Benutzer-CAL</span><span class="sxs-lookup"><span data-stu-id="5c9e3-250">Examples: VDI Per Device subscription license, TS Per User CAL</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5c9e3-251">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5c9e3-251">Remarks</span></span>

<span data-ttu-id="5c9e3-252">Sie müssen Mitglied der Gruppe "Administratoren" sein, um diese Klasse verwenden zu können.</span><span class="sxs-lookup"><span data-stu-id="5c9e3-252">You must be a member of the Administrators group to use this class.</span></span>

<span data-ttu-id="5c9e3-253">Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen.</span><span class="sxs-lookup"><span data-stu-id="5c9e3-253">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="5c9e3-254">MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert.</span><span class="sxs-lookup"><span data-stu-id="5c9e3-254">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="5c9e3-255">Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="5c9e3-255">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="5c9e3-256">Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="5c9e3-256">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="5c9e3-257">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5c9e3-257">Requirements</span></span>



| <span data-ttu-id="5c9e3-258">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5c9e3-258">Requirement</span></span> | <span data-ttu-id="5c9e3-259">Wert</span><span class="sxs-lookup"><span data-stu-id="5c9e3-259">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="5c9e3-260">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5c9e3-260">Minimum supported client</span></span><br/> | <span data-ttu-id="5c9e3-261">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="5c9e3-261">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="5c9e3-262">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5c9e3-262">Minimum supported server</span></span><br/> | <span data-ttu-id="5c9e3-263">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5c9e3-263">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="5c9e3-264">Namespace</span><span class="sxs-lookup"><span data-stu-id="5c9e3-264">Namespace</span></span><br/>                | <span data-ttu-id="5c9e3-265">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="5c9e3-265">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="5c9e3-266">MOF</span><span class="sxs-lookup"><span data-stu-id="5c9e3-266">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5c9e3-267"><dt>Tltaumiprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="5c9e3-267"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="5c9e3-268">DLL</span><span class="sxs-lookup"><span data-stu-id="5c9e3-268">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5c9e3-269"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5c9e3-269"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5c9e3-270">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5c9e3-270">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5c9e3-271">**Win32-" \_ tsissuedlicense"**</span><span class="sxs-lookup"><span data-stu-id="5c9e3-271">**Win32\_TSIssuedLicense**</span></span>](win32-tsissuedlicense.md)
</dt> <dt>

[<span data-ttu-id="5c9e3-272">**Win32-Datei- \_ /licensereport**</span><span class="sxs-lookup"><span data-stu-id="5c9e3-272">**Win32\_TSLicenseReport**</span></span>](win32-tslicensereport.md)
</dt> <dt>

[<span data-ttu-id="5c9e3-273">**Win32-Wert für "- \_ Lizenzserver"**</span><span class="sxs-lookup"><span data-stu-id="5c9e3-273">**Win32\_TSLicenseReportEntry**</span></span>](win32-tslicensereportentry.md)
</dt> <dt>

[<span data-ttu-id="5c9e3-274">**Win32- \_ Lizenznehmer**</span><span class="sxs-lookup"><span data-stu-id="5c9e3-274">**Win32\_TSLicenseServer**</span></span>](win32-tslicenseserver.md)
</dt> </dl>

 

