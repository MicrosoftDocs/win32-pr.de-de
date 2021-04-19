---
description: Ruft das Platt Form Validierungs Profil für eine angegebene Schlüssel Schutzvorrichtung des entsprechenden Typs ab.
ms.assetid: 45fa6ba7-169c-4753-8586-0029a7650acc
title: Getkeyprotectorplatformvalidationprofile-Methode der Win32_EncryptableVolume-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.GetKeyProtectorPlatformValidationProfile
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: b9b951d3ce9eab52687730831f7052942fcbec93
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106373223"
---
# <a name="getkeyprotectorplatformvalidationprofile-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="3120b-103">Getkeyprotectorplatformvalidationprofile-Methode der Win32- \_ Klasse "verschlüsseltablevolume"</span><span class="sxs-lookup"><span data-stu-id="3120b-103">GetKeyProtectorPlatformValidationProfile method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="3120b-104">Die **getkeyprotectorplatformvalidationprofile** -Methode ruft das Platt Form Validierungs Profil für eine bestimmte Schlüssel Schutzvorrichtung des entsprechenden Typs ab.</span><span class="sxs-lookup"><span data-stu-id="3120b-104">The **GetKeyProtectorPlatformValidationProfile** method retrieves the platform validation profile for a given key protector of the appropriate type.</span></span>

<span data-ttu-id="3120b-105">Die schlüsselschutzschutzkennung muss auf eine Schlüssel Schutzvorrichtung vom Typ "TPM", "TPM und PIN", "TPM und PIN und Systemstart Schlüssel" oder "TPM und Systemstart Schlüssel" verweisen.</span><span class="sxs-lookup"><span data-stu-id="3120b-105">The key protector identifier must refer to a key protector of type "TPM", "TPM And PIN", "TPM And PIN And Startup Key", or "TPM And Startup Key".</span></span>

## <a name="syntax"></a><span data-ttu-id="3120b-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="3120b-106">Syntax</span></span>


```mof
uint32 GetKeyProtectorPlatformValidationProfile(
  [in]  string VolumeKeyProtectorID,
  [out] uint8  PlatformValidationProfile[]
);
```



## <a name="parameters"></a><span data-ttu-id="3120b-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="3120b-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3120b-108">*Volumekeyprotectorid* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3120b-108">*VolumeKeyProtectorID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3120b-109">Typ: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="3120b-109">Type: **string**</span></span>

<span data-ttu-id="3120b-110">Ein eindeutiger Zeichen folgen Bezeichner zum Verwalten einer verschlüsselten volumeschlüsselschutzvorrichtung.</span><span class="sxs-lookup"><span data-stu-id="3120b-110">A unique string identifier used to manage an encrypted volume key protector.</span></span>

</dd> <dt>

<span data-ttu-id="3120b-111">*Platformvalidationprofile* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="3120b-111">*PlatformValidationProfile* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3120b-112">Typ: **Uint8 \[ \]**</span><span class="sxs-lookup"><span data-stu-id="3120b-112">Type: **uint8\[\]**</span></span>

<span data-ttu-id="3120b-113">Ein Array von ganzen Zahlen, das angibt, wie die Trusted Platform Module (TPM)-Sicherheits Hardware des Computers den Verschlüsselungsschlüssel des Datenträgervolumes sichert.</span><span class="sxs-lookup"><span data-stu-id="3120b-113">An array of integers that specifies how the Trusted Platform Module (TPM) Security Hardware of the computer secures the encryption key of the disk volume.</span></span>



| <span data-ttu-id="3120b-114">Wert</span><span class="sxs-lookup"><span data-stu-id="3120b-114">Value</span></span>                                                                         | <span data-ttu-id="3120b-115">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="3120b-115">Meaning</span></span>                                                                            |
|-------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="3120b-116"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="3120b-116"><dt>0</dt></span></span> </dl>  | <span data-ttu-id="3120b-117">Kern Stamm der Vertrauens Stellungen von Messgeräten (CRTM), BIOS und Plattformen</span><span class="sxs-lookup"><span data-stu-id="3120b-117">Core Root of Trust of Measurement (CRTM), BIOS, and Platform Extensions</span></span><br/> |
| <dl> <span data-ttu-id="3120b-118"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="3120b-118"><dt>1</dt></span></span> </dl>  | <span data-ttu-id="3120b-119">Konfiguration und Daten von Plattform und Motherboard</span><span class="sxs-lookup"><span data-stu-id="3120b-119">Platform and Motherboard Configuration and Data</span></span><br/>                         |
| <dl> <span data-ttu-id="3120b-120"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="3120b-120"><dt>2</dt></span></span> </dl>  | <span data-ttu-id="3120b-121">Option-ROM-Code</span><span class="sxs-lookup"><span data-stu-id="3120b-121">Option ROM Code</span></span><br/>                                                         |
| <dl> <span data-ttu-id="3120b-122"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="3120b-122"><dt>3</dt></span></span> </dl>  | <span data-ttu-id="3120b-123">Option ROM-Konfiguration und-Daten</span><span class="sxs-lookup"><span data-stu-id="3120b-123">Option ROM Configuration and Data</span></span><br/>                                       |
| <dl> <span data-ttu-id="3120b-124"><dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="3120b-124"><dt>4</dt></span></span> </dl>  | <span data-ttu-id="3120b-125">MBR-Code (Master Boot Record)</span><span class="sxs-lookup"><span data-stu-id="3120b-125">Master Boot Record (MBR) Code</span></span><br/>                                           |
| <dl> <span data-ttu-id="3120b-126"><dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="3120b-126"><dt>5</dt></span></span> </dl>  | <span data-ttu-id="3120b-127">MBR-Partitionstabelle (Master Boot Record)</span><span class="sxs-lookup"><span data-stu-id="3120b-127">Master Boot Record (MBR) Partition Table</span></span><br/>                                |
| <dl> <span data-ttu-id="3120b-128"><dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="3120b-128"><dt>6</dt></span></span> </dl>  | <span data-ttu-id="3120b-129">Zustandsübergänge und Aktivierungs Ereignisse</span><span class="sxs-lookup"><span data-stu-id="3120b-129">State Transition and Wake Events</span></span><br/>                                        |
| <dl> <span data-ttu-id="3120b-130"><dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="3120b-130"><dt>7</dt></span></span> </dl>  | <span data-ttu-id="3120b-131">Computer Manufacturer-Specific</span><span class="sxs-lookup"><span data-stu-id="3120b-131">Computer Manufacturer-Specific</span></span><br/>                                          |
| <dl> <span data-ttu-id="3120b-132"><dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="3120b-132"><dt>8</dt></span></span> </dl>  | <span data-ttu-id="3120b-133">NTFS-Startsektor</span><span class="sxs-lookup"><span data-stu-id="3120b-133">NTFS Boot Sector</span></span><br/>                                                        |
| <dl> <span data-ttu-id="3120b-134"><dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="3120b-134"><dt>9</dt></span></span> </dl>  | <span data-ttu-id="3120b-135">NTFS-Start Block</span><span class="sxs-lookup"><span data-stu-id="3120b-135">NTFS Boot Block</span></span><br/>                                                         |
| <dl> <span data-ttu-id="3120b-136"><dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="3120b-136"><dt>10</dt></span></span> </dl> | <span data-ttu-id="3120b-137">Start-Manager</span><span class="sxs-lookup"><span data-stu-id="3120b-137">Boot Manager</span></span><br/>                                                            |
| <dl> <span data-ttu-id="3120b-138"><dt>11</dt></span><span class="sxs-lookup"><span data-stu-id="3120b-138"><dt>11</dt></span></span> </dl> | <span data-ttu-id="3120b-139">BitLocker-Access Control</span><span class="sxs-lookup"><span data-stu-id="3120b-139">BitLocker Access Control</span></span><br/>                                                |
| <dl> <span data-ttu-id="3120b-140"><dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="3120b-140"><dt>12</dt></span></span> </dl> | <span data-ttu-id="3120b-141">Definiert für die Verwendung durch das statische Betriebssystem</span><span class="sxs-lookup"><span data-stu-id="3120b-141">Defined for use by the static operating system</span></span><br/>                          |
| <dl> <span data-ttu-id="3120b-142"><dt>13</dt></span><span class="sxs-lookup"><span data-stu-id="3120b-142"><dt>13</dt></span></span> </dl> | <span data-ttu-id="3120b-143">Definiert für die Verwendung durch das statische Betriebssystem</span><span class="sxs-lookup"><span data-stu-id="3120b-143">Defined for use by the static operating system</span></span><br/>                          |
| <dl> <span data-ttu-id="3120b-144"><dt>14</dt></span><span class="sxs-lookup"><span data-stu-id="3120b-144"><dt>14</dt></span></span> </dl> | <span data-ttu-id="3120b-145">Definiert für die Verwendung durch das statische Betriebssystem</span><span class="sxs-lookup"><span data-stu-id="3120b-145">Defined for use by the static operating system</span></span><br/>                          |
| <dl> <span data-ttu-id="3120b-146"><dt>15</dt></span><span class="sxs-lookup"><span data-stu-id="3120b-146"><dt>15</dt></span></span> </dl> | <span data-ttu-id="3120b-147">Definiert für die Verwendung durch das statische Betriebssystem</span><span class="sxs-lookup"><span data-stu-id="3120b-147">Defined for use by the static operating system</span></span><br/>                          |
| <dl> <span data-ttu-id="3120b-148"><dt>16</dt></span><span class="sxs-lookup"><span data-stu-id="3120b-148"><dt>16</dt></span></span> </dl> | <span data-ttu-id="3120b-149">Zum Debuggen verwendet</span><span class="sxs-lookup"><span data-stu-id="3120b-149">Used for debugging</span></span><br/>                                                      |
| <dl> <span data-ttu-id="3120b-150"><dt>17</dt></span><span class="sxs-lookup"><span data-stu-id="3120b-150"><dt>17</dt></span></span> </dl> | <span data-ttu-id="3120b-151">Dynamische CRTM</span><span class="sxs-lookup"><span data-stu-id="3120b-151">Dynamic CRTM</span></span><br/>                                                            |
| <dl> <span data-ttu-id="3120b-152"><dt>Jahren</dt></span><span class="sxs-lookup"><span data-stu-id="3120b-152"><dt>18</dt></span></span> </dl> | <span data-ttu-id="3120b-153">Plattform definiert</span><span class="sxs-lookup"><span data-stu-id="3120b-153">Platform defined</span></span><br/>                                                        |
| <dl> <span data-ttu-id="3120b-154"><dt>19</dt></span><span class="sxs-lookup"><span data-stu-id="3120b-154"><dt>19</dt></span></span> </dl> | <span data-ttu-id="3120b-155">Wird von einem vertrauenswürdigen Betriebssystem verwendet</span><span class="sxs-lookup"><span data-stu-id="3120b-155">Used by a trusted operating system</span></span><br/>                                      |
| <dl> <span data-ttu-id="3120b-156"><dt>20</dt></span><span class="sxs-lookup"><span data-stu-id="3120b-156"><dt>20</dt></span></span> </dl> | <span data-ttu-id="3120b-157">Wird von einem vertrauenswürdigen Betriebssystem verwendet</span><span class="sxs-lookup"><span data-stu-id="3120b-157">Used by a trusted operating system</span></span><br/>                                      |
| <dl> <span data-ttu-id="3120b-158"><dt>21</dt></span><span class="sxs-lookup"><span data-stu-id="3120b-158"><dt>21</dt></span></span> </dl> | <span data-ttu-id="3120b-159">Wird von einem vertrauenswürdigen Betriebssystem verwendet</span><span class="sxs-lookup"><span data-stu-id="3120b-159">Used by a trusted operating system</span></span><br/>                                      |
| <dl> <span data-ttu-id="3120b-160"><dt>22</dt></span><span class="sxs-lookup"><span data-stu-id="3120b-160"><dt>22</dt></span></span> </dl> | <span data-ttu-id="3120b-161">Wird von einem vertrauenswürdigen Betriebssystem verwendet</span><span class="sxs-lookup"><span data-stu-id="3120b-161">Used by a trusted operating system</span></span><br/>                                      |
| <dl> <span data-ttu-id="3120b-162"><dt>23</dt></span><span class="sxs-lookup"><span data-stu-id="3120b-162"><dt>23</dt></span></span> </dl> | <span data-ttu-id="3120b-163">Anwendungsunterstützung</span><span class="sxs-lookup"><span data-stu-id="3120b-163">Application support</span></span><br/>                                                     |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3120b-164">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3120b-164">Return value</span></span>

<span data-ttu-id="3120b-165">Typ: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3120b-165">Type: **uint32**</span></span>

<span data-ttu-id="3120b-166">Diese Methode gibt einen der folgenden Codes oder einen anderen Fehlercode zurück, wenn ein Fehler auftritt.</span><span class="sxs-lookup"><span data-stu-id="3120b-166">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="3120b-167">Rückgabecode/-wert</span><span class="sxs-lookup"><span data-stu-id="3120b-167">Return code/value</span></span>                                                                                                                                                                  | <span data-ttu-id="3120b-168">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3120b-168">Description</span></span>                                                                                                                                                                  |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="3120b-169"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="3120b-169"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                  | <span data-ttu-id="3120b-170">Die Methode war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="3120b-170">The method was successful.</span></span><br/>                                                                                                                                        |
| <dl> <span data-ttu-id="3120b-171"><dt>**E \_ InvalidArg**</dt> <dt>2147942487 (0x80070057)</dt></span><span class="sxs-lookup"><span data-stu-id="3120b-171"><dt>**E\_INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt></span></span> </dl>          | <span data-ttu-id="3120b-172">Der *volumekeyprotectorid-* Parameter verweist nicht auf eine Schlüssel Schutzvorrichtung vom Typ "TPM", "TPM und PIN", "TPM und PIN und Systemstart Schlüssel" oder "TPM und Systemstart Schlüssel".</span><span class="sxs-lookup"><span data-stu-id="3120b-172">The *VolumeKeyProtectorID* parameter does not refer to a key protector of the type "TPM", "TPM And PIN", "TPM And PIN And Startup Key", or "TPM And Startup Key".</span></span><br/> |
| <dl> <span data-ttu-id="3120b-173"><dt>**F \_ E \_ nicht \_ aktiviert**</dt> <dt>2150694920 (0x80310008)</dt></span><span class="sxs-lookup"><span data-stu-id="3120b-173"><dt>**FVE\_E\_NOT\_ACTIVATED**</dt> <dt>2150694920 (0x80310008)</dt></span></span> </dl> | <span data-ttu-id="3120b-174">BitLocker ist auf dem Volume nicht aktiviert.</span><span class="sxs-lookup"><span data-stu-id="3120b-174">BitLocker is not enabled on the volume.</span></span> <span data-ttu-id="3120b-175">Fügen Sie eine Schlüssel Schutzvorrichtung zum Aktivieren von BitLocker hinzu.</span><span class="sxs-lookup"><span data-stu-id="3120b-175">Add a key protector to enable BitLocker.</span></span><br/>                                                                                  |



 

## <a name="remarks"></a><span data-ttu-id="3120b-176">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3120b-176">Remarks</span></span>

<span data-ttu-id="3120b-177">Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen.</span><span class="sxs-lookup"><span data-stu-id="3120b-177">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="3120b-178">MOF-Dateien werden nicht als Teil des Windows SDK installiert.</span><span class="sxs-lookup"><span data-stu-id="3120b-178">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="3120b-179">Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="3120b-179">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="3120b-180">Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="3120b-180">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="3120b-181">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3120b-181">Requirements</span></span>



| <span data-ttu-id="3120b-182">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3120b-182">Requirement</span></span> | <span data-ttu-id="3120b-183">Wert</span><span class="sxs-lookup"><span data-stu-id="3120b-183">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3120b-184">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="3120b-184">Minimum supported client</span></span><br/> | <span data-ttu-id="3120b-185">Nur Windows Vista Enterprise, Windows Vista Ultimate \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3120b-185">Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="3120b-186">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="3120b-186">Minimum supported server</span></span><br/> | <span data-ttu-id="3120b-187">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3120b-187">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="3120b-188">Namespace</span><span class="sxs-lookup"><span data-stu-id="3120b-188">Namespace</span></span><br/>                | <span data-ttu-id="3120b-189">Root \\ CIMV2 \\ Sicherheit ( \\ microsoftvolumeencryption)</span><span class="sxs-lookup"><span data-stu-id="3120b-189">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="3120b-190">MOF</span><span class="sxs-lookup"><span data-stu-id="3120b-190">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3120b-191"><dt>Win32 \_ verschlüsseltablevolume. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="3120b-191"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3120b-192">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3120b-192">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3120b-193">**Win32- \_ verschlüsseltablevolume**</span><span class="sxs-lookup"><span data-stu-id="3120b-193">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 
