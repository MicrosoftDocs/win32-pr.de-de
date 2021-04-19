---
description: Stellt den Trusted Platform Module (TPM) dar, einen Hardware Sicherheits Chip, der eine Vertrauensstellung für ein Computersystem bereitstellt.
ms.assetid: da4ba366-49af-420e-a2ad-80bba34b3b00
title: Win32_Tpm-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm
- Win32_Tpm.IsActivated_InitialValue
- Win32_Tpm.IsEnabled_InitialValue
- Win32_Tpm.IsOwned_InitialValue
- Win32_Tpm.SpecVersion
- Win32_Tpm.ManufacturerVersion
- Win32_Tpm.ManufacturerVersionInfo
- Win32_Tpm.ManufacturerId
- Win32_Tpm.PhysicalPresenceVersionInfo
api_type:
- DllExport
api_location:
- Win32_tpm.dll
ms.openlocfilehash: d8d6eac9fba875484ba2f08e149608c9994a1087
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106356972"
---
# <a name="win32_tpm-class"></a><span data-ttu-id="3cbe9-103">Win32- \_ TPM-Klasse</span><span class="sxs-lookup"><span data-stu-id="3cbe9-103">Win32\_Tpm class</span></span>

<span data-ttu-id="3cbe9-104">Die **Win32- \_ TPM** -Klasse stellt die Trusted Platform Module (TPM) dar, einen Hardware Sicherheits Chip, der eine Vertrauensstellung für ein Computersystem bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="3cbe9-104">The **Win32\_Tpm** class represents the Trusted Platform Module (TPM), a hardware security chip that provides a root of trust for a computer system.</span></span>

## <a name="syntax"></a><span data-ttu-id="3cbe9-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="3cbe9-105">Syntax</span></span>

``` syntax
class Win32_Tpm
{
  boolean IsActivated_InitialValue;
  boolean IsEnabled_InitialValue;
  boolean IsOwned_InitialValue;
  string  SpecVersion;
  string  ManufacturerVersion;
  string  ManufacturerVersionInfo;
  uint32  ManufacturerId;
  string  PhysicalPresenceVersionInfo;
};
```

## <a name="members"></a><span data-ttu-id="3cbe9-106">Member</span><span class="sxs-lookup"><span data-stu-id="3cbe9-106">Members</span></span>

<span data-ttu-id="3cbe9-107">Die **Win32- \_ TPM** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="3cbe9-107">The **Win32\_Tpm** class has these types of members:</span></span>

-   [<span data-ttu-id="3cbe9-108">Methoden</span><span class="sxs-lookup"><span data-stu-id="3cbe9-108">Methods</span></span>](#methods)
-   [<span data-ttu-id="3cbe9-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="3cbe9-109">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="3cbe9-110">Methoden</span><span class="sxs-lookup"><span data-stu-id="3cbe9-110">Methods</span></span>

<span data-ttu-id="3cbe9-111">Die **Win32- \_ TPM** -Klasse verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="3cbe9-111">The **Win32\_Tpm** class has these methods.</span></span>



| <span data-ttu-id="3cbe9-112">Methode</span><span class="sxs-lookup"><span data-stu-id="3cbe9-112">Method</span></span>                                                                                   | <span data-ttu-id="3cbe9-113">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3cbe9-113">Description</span></span>                                                                                                                                                                                 |
|:-----------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3cbe9-114">**Addblockedcommand**</span><span class="sxs-lookup"><span data-stu-id="3cbe9-114">**AddBlockedCommand**</span></span>](addblockedcommand-win32-tpm.md)                                 | <span data-ttu-id="3cbe9-115">Fügt der lokalen Liste von Befehlen, die unter Windows blockiert sind, einen TPM-Befehl hinzu.</span><span class="sxs-lookup"><span data-stu-id="3cbe9-115">Adds a TPM command to the local list of commands blocked on Windows.</span></span><br/>                                                                                                             |
| [<span data-ttu-id="3cbe9-116">**Changebesitzauth**</span><span class="sxs-lookup"><span data-stu-id="3cbe9-116">**ChangeOwnerAuth**</span></span>](changeownerauth-win32-tpm.md)                                     | <span data-ttu-id="3cbe9-117">Ändert den TPM-Besitzer Autorisierungs Wert.</span><span class="sxs-lookup"><span data-stu-id="3cbe9-117">Changes the TPM owner authorization value.</span></span><br/>                                                                                                                                       |
| [<span data-ttu-id="3cbe9-118">**Klartext**</span><span class="sxs-lookup"><span data-stu-id="3cbe9-118">**Clear**</span></span>](clear-win32-tpm.md)                                                         | <span data-ttu-id="3cbe9-119">Setzt das TPM auf seine Werkseinstellungen zurück.</span><span class="sxs-lookup"><span data-stu-id="3cbe9-119">Resets the TPM to its factory-default state.</span></span><br/>                                                                                                                                     |
| [<span data-ttu-id="3cbe9-120">**Converttbesitzauth**</span><span class="sxs-lookup"><span data-stu-id="3cbe9-120">**ConvertToOwnerAuth**</span></span>](converttoownerauth-win32-tpm.md)                               | <span data-ttu-id="3cbe9-121">Konvertiert eine vom Benutzer bereitgestellte Passphrase in einen 20-Byte-Besitzer Autorisierungs Wert, der für die Interaktion mit dem TPM verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="3cbe9-121">Converts a user-provided passphrase to a 20-byte owner authorization value that can be used to interact with the TPM.</span></span><br/>                                                            |
| [<span data-ttu-id="3cbe9-122">**"Kreateendorsegmentkeypair"**</span><span class="sxs-lookup"><span data-stu-id="3cbe9-122">**CreateEndorsementKeyPair**</span></span>](createendorsementkeypair-win32-tpm.md)                   | <span data-ttu-id="3cbe9-123">Erstellt ein 2048-Bit-Endorsement Key-paar auf dem TPM.</span><span class="sxs-lookup"><span data-stu-id="3cbe9-123">Creates a 2048-bit endorsement key pair on the TPM.</span></span><br/>                                                                                                                              |
| [<span data-ttu-id="3cbe9-124">**Deaktivieren**</span><span class="sxs-lookup"><span data-stu-id="3cbe9-124">**Disable**</span></span>](disable-win32-tpm.md)                                                     | <span data-ttu-id="3cbe9-125">Ermöglicht dem TPM-Besitzer, das TPM zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="3cbe9-125">Allows the TPM owner to disable the TPM.</span></span><br/>                                                                                                                                         |
| [<span data-ttu-id="3cbe9-126">**Aktivieren**</span><span class="sxs-lookup"><span data-stu-id="3cbe9-126">**Enable**</span></span>](enable-win32-tpm.md)                                                       | <span data-ttu-id="3cbe9-127">Ermöglicht dem TPM-Besitzer, das TPM zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="3cbe9-127">Allows the TPM owner to enable the TPM.</span></span><br/>                                                                                                                                          |
| [<span data-ttu-id="3cbe9-128">**Getphysicalpresencerequest**</span><span class="sxs-lookup"><span data-stu-id="3cbe9-128">**GetPhysicalPresenceRequest**</span></span>](getphysicalpresencerequest-win32-tpm.md)               | <span data-ttu-id="3cbe9-129">Ruft den ausstehenden TPM-Anwesenheits Vorgang ab und gibt ihn zurück.</span><span class="sxs-lookup"><span data-stu-id="3cbe9-129">Gets and returns the pending TPM physical presence operation.</span></span> <span data-ttu-id="3cbe9-130">Verwenden Sie die [**setphysicalpresencerequest**](setphysicalpresencerequest-win32-tpm.md) -Methode, um einen Vorgang anzufordern.</span><span class="sxs-lookup"><span data-stu-id="3cbe9-130">Use the [**SetPhysicalPresenceRequest**](setphysicalpresencerequest-win32-tpm.md) method to request an operation.</span></span><br/> |
| [<span data-ttu-id="3cbe9-131">**Getphysicalpresenceresponse**</span><span class="sxs-lookup"><span data-stu-id="3cbe9-131">**GetPhysicalPresenceResponse**</span></span>](getphysicalpresenceresponse-win32-tpm.md)             | <span data-ttu-id="3cbe9-132">Ruft die Ergebnisse eines ausgeführten TPM-Vorgangs für physische Anwesenheit ab und gibt Sie zurück.</span><span class="sxs-lookup"><span data-stu-id="3cbe9-132">Gets and returns the results from a TPM physical presence operation that was performed.</span></span><br/>                                                                                          |
| [<span data-ttu-id="3cbe9-133">**Getphysicalpresencetransition**</span><span class="sxs-lookup"><span data-stu-id="3cbe9-133">**GetPhysicalPresenceTransition**</span></span>](getphysicalpresencetransition-win32-tpm.md)         | <span data-ttu-id="3cbe9-134">Gibt die Benutzeraktion an, die erforderlich ist, um einen physischen TPM-Anwesenheits Vorgang auszuführen.</span><span class="sxs-lookup"><span data-stu-id="3cbe9-134">Indicates the user action that is needed to perform a TPM physical presence operation.</span></span><br/>                                                                                           |
| [<span data-ttu-id="3cbe9-135">**Isaktiviert**</span><span class="sxs-lookup"><span data-stu-id="3cbe9-135">**IsActivated**</span></span>](isactivated-win32-tpm.md)                                             | <span data-ttu-id="3cbe9-136">Gibt an, ob das TPM aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="3cbe9-136">Indicates whether the TPM is activated.</span></span><br/>                                                                                                                                          |
| [<span data-ttu-id="3cbe9-137">**Iscommandblockierte**</span><span class="sxs-lookup"><span data-stu-id="3cbe9-137">**IsCommandBlocked**</span></span>](iscommandblocked-win32-tpm.md)                                   | <span data-ttu-id="3cbe9-138">Gibt an, ob der TPM-Befehl unter diesem Betriebssystem ausgeführt werden kann.</span><span class="sxs-lookup"><span data-stu-id="3cbe9-138">Indicates whether the TPM command can run on this operating system.</span></span><br/>                                                                                                              |
| [<span data-ttu-id="3cbe9-139">**Iscommandpresent**</span><span class="sxs-lookup"><span data-stu-id="3cbe9-139">**IsCommandPresent**</span></span>](iscommandpresent-win32-tpm.md)                                   | <span data-ttu-id="3cbe9-140">Gibt an, ob ein TPM-Befehl von diesem Computer unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="3cbe9-140">Indicates whether a TPM command is supported by this computer.</span></span><br/>                                                                                                                   |
| [<span data-ttu-id="3cbe9-141">**isEnabled**</span><span class="sxs-lookup"><span data-stu-id="3cbe9-141">**IsEnabled**</span></span>](isenabled-win32-tpm.md)                                                 | <span data-ttu-id="3cbe9-142">Gibt an, ob das TPM aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="3cbe9-142">Indicates whether the TPM is enabled.</span></span><br/>                                                                                                                                            |
| [<span data-ttu-id="3cbe9-143">**Isendorsementkeypaarpresent**</span><span class="sxs-lookup"><span data-stu-id="3cbe9-143">**IsEndorsementKeyPairPresent**</span></span>](isendorsementkeypairpresent-win32-tpm.md)             | <span data-ttu-id="3cbe9-144">Gibt an, ob das TPM ein Endorsement Key-Paar hat.</span><span class="sxs-lookup"><span data-stu-id="3cbe9-144">Indicates whether the TPM has an endorsement key pair.</span></span><br/>                                                                                                                           |
| [<span data-ttu-id="3cbe9-145">**Isowned**</span><span class="sxs-lookup"><span data-stu-id="3cbe9-145">**IsOwned**</span></span>](isowned-win32-tpm.md)                                                     | <span data-ttu-id="3cbe9-146">Gibt an, ob das TPM über einen Besitzer verfügt.</span><span class="sxs-lookup"><span data-stu-id="3cbe9-146">Indicates whether the TPM has an owner.</span></span><br/>                                                                                                                                          |
| [<span data-ttu-id="3cbe9-147">**Isownercleardeaktiviert**</span><span class="sxs-lookup"><span data-stu-id="3cbe9-147">**IsOwnerClearDisabled**</span></span>](isownercleardisabled-win32-tpm.md)                           | <span data-ttu-id="3cbe9-148">Gibt an, ob der TPM-Besitzer das TPM löschen kann.</span><span class="sxs-lookup"><span data-stu-id="3cbe9-148">Indicates whether the TPM owner can clear the TPM.</span></span><br/>                                                                                                                               |
| [<span data-ttu-id="3cbe9-149">**Isownershipallowed**</span><span class="sxs-lookup"><span data-stu-id="3cbe9-149">**IsOwnershipAllowed**</span></span>](isownershipallowed-win32-tpm.md)                               | <span data-ttu-id="3cbe9-150">Gibt an, ob ein TPM-Besitzer installiert werden kann.</span><span class="sxs-lookup"><span data-stu-id="3cbe9-150">Indicates whether a TPM owner can be installed.</span></span><br/>                                                                                                                                  |
| [<span data-ttu-id="3cbe9-151">**Isphysicalcleardeaktiviert**</span><span class="sxs-lookup"><span data-stu-id="3cbe9-151">**IsPhysicalClearDisabled**</span></span>](isphysicalcleardisabled-win32-tpm.md)                     | <span data-ttu-id="3cbe9-152">Gibt an, ob das TPM durch einen physischen TPM-Anwesenheits Vorgang gelöscht werden kann.</span><span class="sxs-lookup"><span data-stu-id="3cbe9-152">Indicates whether a TPM physical presence operation can clear the TPM.</span></span><br/>                                                                                                           |
| [<span data-ttu-id="3cbe9-153">**Isphysicalpresencehardwareaktivierte**</span><span class="sxs-lookup"><span data-stu-id="3cbe9-153">**IsPhysicalPresenceHardwareEnabled**</span></span>](isphysicalpresencehardwareenabled-win32-tpm.md) | <span data-ttu-id="3cbe9-154">Gibt an, ob dieser Computer einen dedizierten Hardware Pfad zum signalisieren physischer Präsenz unterstützt.</span><span class="sxs-lookup"><span data-stu-id="3cbe9-154">Indicates whether this computer supports a dedicated hardware path to signal physical presence.</span></span><br/>                                                                                  |
| [<span data-ttu-id="3cbe9-155">**Issrkauthcompatible**</span><span class="sxs-lookup"><span data-stu-id="3cbe9-155">**IsSrkAuthCompatible**</span></span>](issrkauthcompatible-win32-tpm.md)                             | <span data-ttu-id="3cbe9-156">Gibt an, ob die SRK-Autorisierung (Storage Root Key) mit Windows kompatibel ist.</span><span class="sxs-lookup"><span data-stu-id="3cbe9-156">Indicates whether the Storage Root Key (SRK) authorization is compatible with Windows.</span></span><br/>                                                                                           |
| [<span data-ttu-id="3cbe9-157">**Removeblockedcommand**</span><span class="sxs-lookup"><span data-stu-id="3cbe9-157">**RemoveBlockedCommand**</span></span>](removeblockedcommand-win32-tpm.md)                           | <span data-ttu-id="3cbe9-158">Entfernt einen TPM-Befehl aus der lokalen Liste der Befehle, die von Windows blockiert werden.</span><span class="sxs-lookup"><span data-stu-id="3cbe9-158">Removes a TPM command from the local list of commands blocked by Windows.</span></span><br/>                                                                                                        |
| [<span data-ttu-id="3cbe9-159">**Resetauthlockout**</span><span class="sxs-lookup"><span data-stu-id="3cbe9-159">**ResetAuthLockOut**</span></span>](resetauthlockout-win32-tpm.md)                                   | <span data-ttu-id="3cbe9-160">Setzt den Timeout Zeitraum oder einen anderen Mechanismus zurück, den TPM-Hersteller implementiert, um Wörterbuchangriffe auf dem TPM zu schützen.</span><span class="sxs-lookup"><span data-stu-id="3cbe9-160">Resets the time-out period or other mechanism that TPM manufacturers implement to protect against dictionary attacks on the TPM.</span></span><br/>                                                 |
| [<span data-ttu-id="3cbe9-161">**Resegzrkauth**</span><span class="sxs-lookup"><span data-stu-id="3cbe9-161">**ResetSrkAuth**</span></span>](resetsrkauth-win32-tpm.md)                                           | <span data-ttu-id="3cbe9-162">Setzt den SRK-Autorisierungs Wert (Storage Root Key) so zurück, dass er mit Windows kompatibel ist.</span><span class="sxs-lookup"><span data-stu-id="3cbe9-162">Resets the Storage Root Key (SRK) authorization value to be compatible with Windows.</span></span><br/>                                                                                             |
| [<span data-ttu-id="3cbe9-163">**SelfTest**</span><span class="sxs-lookup"><span data-stu-id="3cbe9-163">**SelfTest**</span></span>](selftest-win32-tpm.md)                                                   | <span data-ttu-id="3cbe9-164">Führt einen Selbsttest des TPM aus und gibt das Ergebnis zurück.</span><span class="sxs-lookup"><span data-stu-id="3cbe9-164">Performs a self-test of the TPM and returns the result.</span></span><br/>                                                                                                                          |
| [<span data-ttu-id="3cbe9-165">**Setphysicalpresencerequest**</span><span class="sxs-lookup"><span data-stu-id="3cbe9-165">**SetPhysicalPresenceRequest**</span></span>](setphysicalpresencerequest-win32-tpm.md)               | <span data-ttu-id="3cbe9-166">Fordert die Ausführung eines physischen TPM-Anwesenheits Vorgangs an.</span><span class="sxs-lookup"><span data-stu-id="3cbe9-166">Requests a TPM physical presence operation to run.</span></span><br/>                                                                                                                               |
| [<span data-ttu-id="3cbe9-167">**TakeOwnership**</span><span class="sxs-lookup"><span data-stu-id="3cbe9-167">**TakeOwnership**</span></span>](takeownership-win32-tpm.md)                                         | <span data-ttu-id="3cbe9-168">Installiert einen Besitzer für das TPM.</span><span class="sxs-lookup"><span data-stu-id="3cbe9-168">Installs an owner for the TPM.</span></span><br/>                                                                                                                                                   |



 

### <a name="properties"></a><span data-ttu-id="3cbe9-169">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="3cbe9-169">Properties</span></span>

<span data-ttu-id="3cbe9-170">Die **Win32- \_ TPM** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="3cbe9-170">The **Win32\_Tpm** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="3cbe9-171">**Isaktivierter \_ InitialValue**</span><span class="sxs-lookup"><span data-stu-id="3cbe9-171">**IsActivated\_InitialValue**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3cbe9-172">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="3cbe9-172">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="3cbe9-173">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3cbe9-173">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3cbe9-174">Gibt an, ob das TPM aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="3cbe9-174">Indicates whether the TPM is activated.</span></span>

<span data-ttu-id="3cbe9-175">**true** , wenn das Gerät aktiviert ist (d. h., wenn **isaktivierter \_ InitialValue** true ist), andernfalls **false**.</span><span class="sxs-lookup"><span data-stu-id="3cbe9-175">**true** if the device is activated (that is, if **IsActivated\_InitialValue** is true); otherwise, **false**.</span></span>

<span data-ttu-id="3cbe9-176">Dieser Wert wird gespeichert, wenn die-Klasse instanziiert wird.</span><span class="sxs-lookup"><span data-stu-id="3cbe9-176">This value is stored when the class is instantiated.</span></span> <span data-ttu-id="3cbe9-177">Das TPM kann den Status zwischen der Instanziierung und dem Zeitpunkt, zu dem Sie diesen Wert überprüfen, ändern.</span><span class="sxs-lookup"><span data-stu-id="3cbe9-177">It is possible for the TPM to change state between the instantiation and when you check this value.</span></span> <span data-ttu-id="3cbe9-178">Verwenden Sie die [**isaktivierte**](isactivated-win32-tpm.md) Methode, um zu überprüfen, ob das TPM in Echtzeit aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="3cbe9-178">To check whether the TPM is activated in real time, use the [**IsActivated**](isactivated-win32-tpm.md) method.</span></span>

<span data-ttu-id="3cbe9-179">**Windows Server 2008 und Windows Vista:** Diese Eigenschaft ist nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="3cbe9-179">**Windows Server 2008 and Windows Vista:** This property is not available.</span></span>

</dd> <dt>

<span data-ttu-id="3cbe9-180">**Isaktivierter \_ InitialValue**</span><span class="sxs-lookup"><span data-stu-id="3cbe9-180">**IsEnabled\_InitialValue**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3cbe9-181">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="3cbe9-181">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="3cbe9-182">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3cbe9-182">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3cbe9-183">Gibt an, ob das TPM aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="3cbe9-183">Indicates whether the TPM is enabled.</span></span>

<span data-ttu-id="3cbe9-184">**true** , wenn das Gerät aktiviert ist (d. h., wenn **isaktivierter \_ InitialValue** true ist), andernfalls **false**.</span><span class="sxs-lookup"><span data-stu-id="3cbe9-184">**true** if the device is enabled (that is, if **IsEnabled\_InitialValue** is true); otherwise, **false**.</span></span>

<span data-ttu-id="3cbe9-185">Dieser Wert wird gespeichert, wenn die-Klasse instanziiert wird.</span><span class="sxs-lookup"><span data-stu-id="3cbe9-185">This value is stored when the class is instantiated.</span></span> <span data-ttu-id="3cbe9-186">Das TPM kann den Status zwischen der Instanziierung und dem Zeitpunkt, zu dem Sie diesen Wert überprüfen, ändern.</span><span class="sxs-lookup"><span data-stu-id="3cbe9-186">It is possible for the TPM to change state between the instantiation and when you check this value.</span></span> <span data-ttu-id="3cbe9-187">Verwenden Sie die [**isaktivierte**](isenabled-win32-tpm.md) Methode, um zu überprüfen, ob das TPM in Echtzeit aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="3cbe9-187">To check whether the TPM is enabled in real time, use the [**IsEnabled**](isenabled-win32-tpm.md) method.</span></span>

<span data-ttu-id="3cbe9-188">**Windows Server 2008 und Windows Vista:** Diese Eigenschaft ist nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="3cbe9-188">**Windows Server 2008 and Windows Vista:** This property is not available.</span></span>

</dd> <dt>

<span data-ttu-id="3cbe9-189">**Isowned \_ InitialValue**</span><span class="sxs-lookup"><span data-stu-id="3cbe9-189">**IsOwned\_InitialValue**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3cbe9-190">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="3cbe9-190">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="3cbe9-191">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3cbe9-191">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3cbe9-192">Gibt an, ob das TPM über einen Besitzer verfügt.</span><span class="sxs-lookup"><span data-stu-id="3cbe9-192">Indicates whether the TPM has an owner.</span></span>

<span data-ttu-id="3cbe9-193">**true** , wenn das Gerät über einen Besitzer verfügt (d. h., wenn der **isowned \_ InitialValue** true ist), andernfalls **false**.</span><span class="sxs-lookup"><span data-stu-id="3cbe9-193">**true** if the device has an owner (that is, if **IsOwned\_InitialValue** is true); otherwise, **false**.</span></span>

<span data-ttu-id="3cbe9-194">Dieser Wert wird gespeichert, wenn die-Klasse instanziiert wird.</span><span class="sxs-lookup"><span data-stu-id="3cbe9-194">This value is stored when the class is instantiated.</span></span> <span data-ttu-id="3cbe9-195">Das TPM kann den Status zwischen der Instanziierung und dem Zeitpunkt, zu dem Sie diesen Wert überprüfen, ändern.</span><span class="sxs-lookup"><span data-stu-id="3cbe9-195">It is possible for the TPM to change state between the instantiation and when you check this value.</span></span> <span data-ttu-id="3cbe9-196">Verwenden Sie die [**isowned**](isowned-win32-tpm.md) -Methode, um zu überprüfen, ob das TPM in Echtzeit gehört.</span><span class="sxs-lookup"><span data-stu-id="3cbe9-196">To check whether the TPM is owned in real time, use the [**IsOwned**](isowned-win32-tpm.md) method.</span></span>

<span data-ttu-id="3cbe9-197">**Windows Server 2008 und Windows Vista:** Diese Eigenschaft ist nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="3cbe9-197">**Windows Server 2008 and Windows Vista:** This property is not available.</span></span>

</dd> <dt>

<span data-ttu-id="3cbe9-198">**Manufacturerid**</span><span class="sxs-lookup"><span data-stu-id="3cbe9-198">**ManufacturerId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3cbe9-199">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3cbe9-199">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3cbe9-200">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3cbe9-200">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3cbe9-201">Die identifizierenden Informationen, die den TPM-Hersteller eindeutig benennen.</span><span class="sxs-lookup"><span data-stu-id="3cbe9-201">The identifying information that uniquely names the TPM manufacturer.</span></span>

<span data-ttu-id="3cbe9-202">Wenn die Daten nicht verfügbar sind, wird NULL zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="3cbe9-202">When the data is unavailable, zero is returned.</span></span>

<span data-ttu-id="3cbe9-203">Dieser ganzzahlige Wert kann in einen Zeichen folgen Wert übersetzt werden, indem die einzelnen Bytes als ASCII-Zeichen interpretiert werden.</span><span class="sxs-lookup"><span data-stu-id="3cbe9-203">This integer value can be translated to a string value by interpreting each byte as an ASCII character.</span></span> <span data-ttu-id="3cbe9-204">Beispielsweise kann ein ganzzahliger Wert von 1414548736 in diese 4 Bytes unterteilt werden: 0x54, 0x50, 0x4D und 0x00.</span><span class="sxs-lookup"><span data-stu-id="3cbe9-204">For example, an integer value of 1414548736 can be divided into these 4 bytes: 0x54, 0x50, 0x4D, and 0x00.</span></span> <span data-ttu-id="3cbe9-205">Wenn die Zeichenfolge von links nach rechts interpretiert wird, wird dieser ganzzahlige Wert in den Zeichen folgen Wert "TPM" übersetzt.</span><span class="sxs-lookup"><span data-stu-id="3cbe9-205">Assuming the string is interpreted from left to right, this integer value translated to a string value of "TPM".</span></span>

</dd> <dt>

<span data-ttu-id="3cbe9-206">**Manufacturerversion**</span><span class="sxs-lookup"><span data-stu-id="3cbe9-206">**ManufacturerVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3cbe9-207">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="3cbe9-207">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3cbe9-208">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3cbe9-208">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3cbe9-209">Die vom Hersteller angegebene TPM-Version.</span><span class="sxs-lookup"><span data-stu-id="3cbe9-209">The version of the TPM, as specified by the manufacturer.</span></span>

<span data-ttu-id="3cbe9-210">Wenn die Daten nicht verfügbar sind, wird "nicht unterstützt" zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="3cbe9-210">When the data is unavailable, "Not Supported" is returned.</span></span>

</dd> <dt>

<span data-ttu-id="3cbe9-211">**Manufacturerversioninfo**</span><span class="sxs-lookup"><span data-stu-id="3cbe9-211">**ManufacturerVersionInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3cbe9-212">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="3cbe9-212">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3cbe9-213">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3cbe9-213">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3cbe9-214">Weitere herstellerspezifische Versionsinformationen für das TPM.</span><span class="sxs-lookup"><span data-stu-id="3cbe9-214">Other manufacturer-specific version information for the TPM.</span></span>

<span data-ttu-id="3cbe9-215">Wenn die Daten nicht verfügbar sind, wird "nicht unterstützt" zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="3cbe9-215">When the data is unavailable, "Not Supported" is returned.</span></span>

</dd> <dt>

<span data-ttu-id="3cbe9-216">**Physicalpresenceversioninfo**</span><span class="sxs-lookup"><span data-stu-id="3cbe9-216">**PhysicalPresenceVersionInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3cbe9-217">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="3cbe9-217">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3cbe9-218">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3cbe9-218">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3cbe9-219">Die Version der physischen Anwesenheits Schnittstelle, ein Kommunikationsmechanismus, der zum Ausführen von Geräte Vorgängen verwendet wird, die vom Computer unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="3cbe9-219">The version of the Physical Presence Interface, a communication mechanism used to run device operations that require physical presence, that the computer supports.</span></span>

<span data-ttu-id="3cbe9-220">Diese Schnittstelle muss verfügbar sein, um TPM-Vorgänge zur physischen Anwesenheit auszuführen.</span><span class="sxs-lookup"><span data-stu-id="3cbe9-220">This interface must be available to run TPM physical presence operations.</span></span> <span data-ttu-id="3cbe9-221">Die **Win32 \_ TPM** -Methoden [**setphysicalpresencerequest**](setphysicalpresencerequest-win32-tpm.md), [**getphysicalpresencerequest**](getphysicalpresencerequest-win32-tpm.md), [**getphysicalpresencetransition**](getphysicalpresencetransition-win32-tpm.md)und [**getphysicalpresenceresponse**](getphysicalpresenceresponse-win32-tpm.md) machen die Funktionen der physischen Anwesenheits Schnittstelle verfügbar.</span><span class="sxs-lookup"><span data-stu-id="3cbe9-221">The **Win32\_Tpm** methods [**SetPhysicalPresenceRequest**](setphysicalpresencerequest-win32-tpm.md), [**GetPhysicalPresenceRequest**](getphysicalpresencerequest-win32-tpm.md), [**GetPhysicalPresenceTransition**](getphysicalpresencetransition-win32-tpm.md), and [**GetPhysicalPresenceResponse**](getphysicalpresenceresponse-win32-tpm.md) expose the capabilities of the Physical Presence Interface.</span></span>

<span data-ttu-id="3cbe9-222">Wenn die Daten nicht verfügbar sind, wird "nicht unterstützt" zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="3cbe9-222">When the data is unavailable, "Not Supported" is returned.</span></span>

</dd> <dt>

<span data-ttu-id="3cbe9-223">**SpecVersion**</span><span class="sxs-lookup"><span data-stu-id="3cbe9-223">**SpecVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3cbe9-224">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="3cbe9-224">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3cbe9-225">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3cbe9-225">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3cbe9-226">Die Version der Trusted Computing Group (TCG)-Spezifikation, die das TPM unterstützt.</span><span class="sxs-lookup"><span data-stu-id="3cbe9-226">The version of the Trusted Computing Group (TCG) specification that the TPM supports.</span></span> <span data-ttu-id="3cbe9-227">Dieser Wert umfasst die Spezifikation für die Haupt-und neben Version der TCG-Spezifikation, die Spezifikations Revisions Ebene und die Errata-Revisions Ebene.</span><span class="sxs-lookup"><span data-stu-id="3cbe9-227">This value includes the major and minor TCG specification version, the specification revision level, and the errata revision level.</span></span> <span data-ttu-id="3cbe9-228">Alle Werte sind hexadezimal.</span><span class="sxs-lookup"><span data-stu-id="3cbe9-228">All values are in hexadecimal.</span></span> <span data-ttu-id="3cbe9-229">Beispielsweise geben die Versionsinformationen "1,2, 2, 0" an, dass das Gerät in die TCG-Spezifikation Version 1,2, Revision Level 2 und ohne Errata implementiert wurde.</span><span class="sxs-lookup"><span data-stu-id="3cbe9-229">For example, a version information of "1.2, 2, 0" indicates that the device was implemented to TCG specification version 1.2, revision level 2, and with no errata.</span></span>

<span data-ttu-id="3cbe9-230">Wenn die Daten nicht verfügbar sind, wird "nicht unterstützt" zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="3cbe9-230">When the data is unavailable, "Not Supported" is returned.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3cbe9-231">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3cbe9-231">Remarks</span></span>

<span data-ttu-id="3cbe9-232">Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen.</span><span class="sxs-lookup"><span data-stu-id="3cbe9-232">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="3cbe9-233">MOF-Dateien werden nicht als Teil des Windows SDK installiert.</span><span class="sxs-lookup"><span data-stu-id="3cbe9-233">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="3cbe9-234">Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="3cbe9-234">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="3cbe9-235">Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="3cbe9-235">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="3cbe9-236">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3cbe9-236">Requirements</span></span>



| <span data-ttu-id="3cbe9-237">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3cbe9-237">Requirement</span></span> | <span data-ttu-id="3cbe9-238">Wert</span><span class="sxs-lookup"><span data-stu-id="3cbe9-238">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="3cbe9-239">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="3cbe9-239">Minimum supported client</span></span><br/> | <span data-ttu-id="3cbe9-240">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3cbe9-240">Windows Vista \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="3cbe9-241">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="3cbe9-241">Minimum supported server</span></span><br/> | <span data-ttu-id="3cbe9-242">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3cbe9-242">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="3cbe9-243">Namespace</span><span class="sxs-lookup"><span data-stu-id="3cbe9-243">Namespace</span></span><br/>                | <span data-ttu-id="3cbe9-244">Root \\ CIMV2 \\ Security- \\ mikrosofttpm</span><span class="sxs-lookup"><span data-stu-id="3cbe9-244">Root\\CIMV2\\Security\\MicrosoftTpm</span></span><br/>                                            |
| <span data-ttu-id="3cbe9-245">MOF</span><span class="sxs-lookup"><span data-stu-id="3cbe9-245">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3cbe9-246"><dt>Win32- \_ TPM. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="3cbe9-246"><dt>Win32\_tpm.mof</dt></span></span> </dl> |
| <span data-ttu-id="3cbe9-247">DLL</span><span class="sxs-lookup"><span data-stu-id="3cbe9-247">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3cbe9-248"><dt>Win32- \_tpm.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3cbe9-248"><dt>Win32\_tpm.dll</dt></span></span> </dl> |



 

 
