---
description: Wenn die Trusted Platform Module (TPM) verfügbar ist, sichert diese Methode den Verschlüsselungsschlüssel des Volumes, der durch einen externen Schlüssel erweitert wurde.
ms.assetid: 58bc2de7-645f-4049-949c-975062f8c8ce
title: Protectkeywithtpmandstartupkey-Methode der Win32_EncryptableVolume-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.ProtectKeyWithTPMAndStartupKey
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 06ab2b9474b3564a567374490d9aeb70448338be
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346087"
---
# <a name="protectkeywithtpmandstartupkey-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="5eef2-103">Protectkeywithtpmandstartupkey-Methode der Win32- \_ Klasse "verschlüsseltablevolume"</span><span class="sxs-lookup"><span data-stu-id="5eef2-103">ProtectKeyWithTPMAndStartupKey method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="5eef2-104">Die **protectkeywithtpmandstartupkey** -Methode der Win32-Klasse " [**\_ verschlüsseltablevolume**](win32-encryptablevolume.md) " sichert den Verschlüsselungsschlüssel des Volumes mithilfe der TPM-Sicherheits Hardware (Trusted Platform Module) auf dem Computer, sofern verfügbar, erweitert durch einen externen Schlüssel, der dem Computer beim Start angezeigt werden muss.</span><span class="sxs-lookup"><span data-stu-id="5eef2-104">The **ProtectKeyWithTPMAndStartupKey** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class secures the volume's encryption key by using the Trusted Platform Module (TPM) Security Hardware on the computer, if available, enhanced by an external key that must be presented to the computer at startup.</span></span>

<span data-ttu-id="5eef2-105">Sowohl die Überprüfung durch das TPM als auch die Eingabe eines USB-Speichergeräts, das den externen Schlüssel enthält, sind erforderlich, um auf den Verschlüsselungsschlüssel des Volumes zuzugreifen und den volumeinhalt freizugeben.</span><span class="sxs-lookup"><span data-stu-id="5eef2-105">Both validation by the TPM and input of a USB memory device that contains the external key are necessary to access the volume's encryption key and unlock the volume contents.</span></span> <span data-ttu-id="5eef2-106">Verwenden Sie die [**saveexternalkeytofile**](saveexternalkeytofile-win32-encryptablevolume.md) -Methode, um diesen externen Schlüssel in einer Datei auf einem USB-Speichergerät für die Verwendung als Systemstart Schlüssel zu speichern.</span><span class="sxs-lookup"><span data-stu-id="5eef2-106">Use the [**SaveExternalKeyToFile**](saveexternalkeytofile-win32-encryptablevolume.md) method to save this external key to a file on a USB memory device for usage as a startup key.</span></span>

<span data-ttu-id="5eef2-107">Diese Methode ist nur für das Volume anwendbar, das das aktuell laufende Betriebssystem enthält.</span><span class="sxs-lookup"><span data-stu-id="5eef2-107">This method is only applicable for the volume that contains the currently running operating system.</span></span>

<span data-ttu-id="5eef2-108">Eine Schlüssel Schutzvorrichtung vom Typ "TPM und Systemstart Schlüssel" wird für das Volume erstellt, sofern nicht bereits vorhanden.</span><span class="sxs-lookup"><span data-stu-id="5eef2-108">A key protector of type "TPM And Startup Key" is created for the volume, if one does not already exist.</span></span>

## <a name="syntax"></a><span data-ttu-id="5eef2-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="5eef2-109">Syntax</span></span>


```mof
uint32 ProtectKeyWithTPMAndStartupKey(
  [in, optional] string FriendlyName,
  [in, optional] uint8  PlatformValidationProfile[],
  [in, optional] uint8  ExternalKey[],
  [out]          string VolumeKeyProtectorID
);
```



## <a name="parameters"></a><span data-ttu-id="5eef2-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="5eef2-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5eef2-111">*FriendlyName* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="5eef2-111">*FriendlyName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="5eef2-112">Typ: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="5eef2-112">Type: **string**</span></span>

<span data-ttu-id="5eef2-113">Ein vom Benutzer zugewiesener Zeichen folgen Bezeichner für diese Schlüssel Schutzvorrichtung.</span><span class="sxs-lookup"><span data-stu-id="5eef2-113">A user-assigned string identifier for this key protector.</span></span> <span data-ttu-id="5eef2-114">Wenn dieser Parameter nicht angegeben wird, wird ein leerer Wert verwendet.</span><span class="sxs-lookup"><span data-stu-id="5eef2-114">If this parameter is not specified, a blank value is used.</span></span>

</dd> <dt>

<span data-ttu-id="5eef2-115">*Platformvalidationprofile* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="5eef2-115">*PlatformValidationProfile* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="5eef2-116">Typ: **Uint8 \[ \]**</span><span class="sxs-lookup"><span data-stu-id="5eef2-116">Type: **uint8\[\]**</span></span>

<span data-ttu-id="5eef2-117">Ein Array von ganzen Zahlen, das angibt, wie die Sicherheits Hardware des Computers Trusted Platform Module (TPM) den Verschlüsselungsschlüssel des Datenträgervolumes sichert.</span><span class="sxs-lookup"><span data-stu-id="5eef2-117">An array of integers that specifies how the computer's Trusted Platform Module (TPM) Security Hardware secures the encryption key of the disk volume.</span></span>

<span data-ttu-id="5eef2-118">Ein Platt Form Validierungs Profil besteht aus einem Satz von Platt Form Konfigurations Register Indizes (PCR), der zwischen 0 und 23 (einschließlich) liegt.</span><span class="sxs-lookup"><span data-stu-id="5eef2-118">A platform validation profile consists of a set of Platform Configuration Register (PCR) indices ranging from 0 to 23, inclusive.</span></span> <span data-ttu-id="5eef2-119">Wiederholungswerte im-Parameter werden ignoriert.</span><span class="sxs-lookup"><span data-stu-id="5eef2-119">Repeat values in the parameter are ignored.</span></span> <span data-ttu-id="5eef2-120">Jeder PCR-Index ist mit Diensten verknüpft, die beim Starten des Betriebssystems ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="5eef2-120">Each PCR index is associated with services that run when the operating system starts.</span></span> <span data-ttu-id="5eef2-121">Jedes Mal, wenn der Computer gestartet wird, prüft das TPM, ob die Dienste, die Sie im Platt Form Validierungs Profil angegeben haben, nicht geändert wurden.</span><span class="sxs-lookup"><span data-stu-id="5eef2-121">Each time the computer starts, the TPM will check that the services you specified in the platform validation profile have not changed.</span></span> <span data-ttu-id="5eef2-122">Wenn sich einer dieser Dienste ändert, während BitLocker-Laufwerkverschlüsselung (BDE)-Schutz beibehalten wird, gibt das TPM den Verschlüsselungsschlüssel nicht frei, um das Datenträger Volume zu entsperren, und der Computer wechselt in den Wiederherstellungs Modus.</span><span class="sxs-lookup"><span data-stu-id="5eef2-122">If any of these services change while BitLocker Drive Encryption (BDE) protection remains on, the TPM will not release the encryption key to unlock the disk volume, and the computer will enter into recovery mode.</span></span>

<span data-ttu-id="5eef2-123">Wenn dieser Parameter angegeben wird, während die entsprechende Gruppenrichtlinie Einstellung aktiviert ist, muss er mit der Gruppenrichtlinie Einstellung übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="5eef2-123">If this parameter is specified while the corresponding Group Policy setting has been enabled, it must match the Group Policy setting.</span></span>

<span data-ttu-id="5eef2-124">Wenn dieser Parameter nicht angegeben wird, wird der Standardwert 0, 2, 4, 5, 8, 9, 10 und 11 verwendet.</span><span class="sxs-lookup"><span data-stu-id="5eef2-124">If this parameter is not specified, the default of 0, 2, 4, 5, 8, 9, 10, and 11 is used.</span></span> <span data-ttu-id="5eef2-125">Das standardmäßige Platt Form Validierungs Profil sichert den Verschlüsselungsschlüssel vor Änderungen an den folgenden Elementen:</span><span class="sxs-lookup"><span data-stu-id="5eef2-125">The default platform validation profile secures the encryption key against changes to the following elements:</span></span>

-   <span data-ttu-id="5eef2-126">Kern Stamm der Messgeräte Vertrauensstellung (CRTM)</span><span class="sxs-lookup"><span data-stu-id="5eef2-126">Core Root of Trust of Measurement (CRTM)</span></span>
-   <span data-ttu-id="5eef2-127">BIOS</span><span class="sxs-lookup"><span data-stu-id="5eef2-127">BIOS</span></span>
-   <span data-ttu-id="5eef2-128">Platt Form Erweiterungen (PCR 0)</span><span class="sxs-lookup"><span data-stu-id="5eef2-128">Platform Extensions (PCR 0)</span></span>
-   <span data-ttu-id="5eef2-129">Options-ROM-Code (PCR 2)</span><span class="sxs-lookup"><span data-stu-id="5eef2-129">Option ROM Code (PCR 2)</span></span>
-   <span data-ttu-id="5eef2-130">Master Boot Record (MBR)-Code (PCR 4)</span><span class="sxs-lookup"><span data-stu-id="5eef2-130">Master Boot Record (MBR) Code (PCR 4)</span></span>
-   <span data-ttu-id="5eef2-131">MBR-Partitionstabelle (Master Boot Record) (PCR 5)</span><span class="sxs-lookup"><span data-stu-id="5eef2-131">Master Boot Record (MBR) Partition Table (PCR 5)</span></span>
-   <span data-ttu-id="5eef2-132">NTFS-Startsektor (PCR 8)</span><span class="sxs-lookup"><span data-stu-id="5eef2-132">NTFS Boot Sector (PCR 8)</span></span>
-   <span data-ttu-id="5eef2-133">NTFS-Startblock (PCR 9)</span><span class="sxs-lookup"><span data-stu-id="5eef2-133">NTFS Boot Block (PCR 9)</span></span>
-   <span data-ttu-id="5eef2-134">Start-Manager (PCR 10)</span><span class="sxs-lookup"><span data-stu-id="5eef2-134">Boot Manager (PCR 10)</span></span>
-   <span data-ttu-id="5eef2-135">BitLocker-Zugriffssteuerung (PCR 11)</span><span class="sxs-lookup"><span data-stu-id="5eef2-135">BitLocker Access Control (PCR 11)</span></span>

<span data-ttu-id="5eef2-136">Für die Sicherheit Ihres Computers wird das Standardprofil empfohlen.</span><span class="sxs-lookup"><span data-stu-id="5eef2-136">For the security of your computer, we recommend the default profile.</span></span> <span data-ttu-id="5eef2-137">Um zusätzlichen Schutz vor Änderungen der frühen Startkonfiguration zu erhalten, verwenden Sie ein Profil von PCRs 0, 1, 2, 3, 4, 5, 8, 9, 10, 11.</span><span class="sxs-lookup"><span data-stu-id="5eef2-137">For additional protection against early startup configuration changes, use a profile of PCRs 0, 1, 2, 3, 4, 5, 8, 9, 10, 11.</span></span> <span data-ttu-id="5eef2-138">Unified Extensible Firmware Interface (UEFI) – Computer verwenden standardmäßig nicht PCR 5.</span><span class="sxs-lookup"><span data-stu-id="5eef2-138">Unified Extensible Firmware Interface (UEFI)–based computers do not use PCR 5 by default.</span></span>

<span data-ttu-id="5eef2-139">Das Ändern des Standard Profils wirkt sich auf die Sicherheit und Verwaltbarkeit Ihres Computers aus.</span><span class="sxs-lookup"><span data-stu-id="5eef2-139">Changing from the default profile affects the security and manageability of your computer.</span></span> <span data-ttu-id="5eef2-140">Die Vertraulichkeit von BitLocker zu Platt Formänderungen (bösartig oder autorisiert) wird abhängig vom Inklusions-oder Ausschluss Wert des PCRs angehoben oder verringert.</span><span class="sxs-lookup"><span data-stu-id="5eef2-140">The sensitivity of BitLocker to platform modifications (malicious or authorized) is increased or decreased depending upon the inclusion or exclusion, respectively, of the PCRs.</span></span> <span data-ttu-id="5eef2-141">Damit der BitLocker-Schutz aktiviert werden kann, muss das Platt Form Validierungs Profil PCR 11 enthalten.</span><span class="sxs-lookup"><span data-stu-id="5eef2-141">For BitLocker protection to be enabled, the platform validation profile must include PCR 11.</span></span>



| <span data-ttu-id="5eef2-142">Wert</span><span class="sxs-lookup"><span data-stu-id="5eef2-142">Value</span></span>                                                                         | <span data-ttu-id="5eef2-143">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="5eef2-143">Meaning</span></span>                                                                            |
|-------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="5eef2-144"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="5eef2-144"><dt>0</dt></span></span> </dl>  | <span data-ttu-id="5eef2-145">Kern Stamm der Vertrauens Stellungen von Messgeräten (CRTM), BIOS und Plattformen</span><span class="sxs-lookup"><span data-stu-id="5eef2-145">Core Root of Trust of Measurement (CRTM), BIOS, and Platform Extensions</span></span><br/> |
| <dl> <span data-ttu-id="5eef2-146"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="5eef2-146"><dt>1</dt></span></span> </dl>  | <span data-ttu-id="5eef2-147">Konfiguration und Daten von Plattform und Motherboard</span><span class="sxs-lookup"><span data-stu-id="5eef2-147">Platform and Motherboard Configuration and Data</span></span><br/>                         |
| <dl> <span data-ttu-id="5eef2-148"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="5eef2-148"><dt>2</dt></span></span> </dl>  | <span data-ttu-id="5eef2-149">Option-ROM-Code</span><span class="sxs-lookup"><span data-stu-id="5eef2-149">Option ROM Code</span></span><br/>                                                         |
| <dl> <span data-ttu-id="5eef2-150"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="5eef2-150"><dt>3</dt></span></span> </dl>  | <span data-ttu-id="5eef2-151">Option ROM-Konfiguration und-Daten</span><span class="sxs-lookup"><span data-stu-id="5eef2-151">Option ROM Configuration and Data</span></span><br/>                                       |
| <dl> <span data-ttu-id="5eef2-152"><dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="5eef2-152"><dt>4</dt></span></span> </dl>  | <span data-ttu-id="5eef2-153">MBR-Code (Master Boot Record)</span><span class="sxs-lookup"><span data-stu-id="5eef2-153">Master Boot Record (MBR) Code</span></span><br/>                                           |
| <dl> <span data-ttu-id="5eef2-154"><dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="5eef2-154"><dt>5</dt></span></span> </dl>  | <span data-ttu-id="5eef2-155">MBR-Partitionstabelle (Master Boot Record)</span><span class="sxs-lookup"><span data-stu-id="5eef2-155">Master Boot Record (MBR) Partition Table</span></span><br/>                                |
| <dl> <span data-ttu-id="5eef2-156"><dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="5eef2-156"><dt>6</dt></span></span> </dl>  | <span data-ttu-id="5eef2-157">Zustandsübergänge und Aktivierungs Ereignisse</span><span class="sxs-lookup"><span data-stu-id="5eef2-157">State Transition and Wake Events</span></span><br/>                                        |
| <dl> <span data-ttu-id="5eef2-158"><dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="5eef2-158"><dt>7</dt></span></span> </dl>  | <span data-ttu-id="5eef2-159">Computer Manufacturer-Specific</span><span class="sxs-lookup"><span data-stu-id="5eef2-159">Computer Manufacturer-Specific</span></span><br/>                                          |
| <dl> <span data-ttu-id="5eef2-160"><dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="5eef2-160"><dt>8</dt></span></span> </dl>  | <span data-ttu-id="5eef2-161">NTFS-Startsektor</span><span class="sxs-lookup"><span data-stu-id="5eef2-161">NTFS Boot Sector</span></span><br/>                                                        |
| <dl> <span data-ttu-id="5eef2-162"><dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="5eef2-162"><dt>9</dt></span></span> </dl>  | <span data-ttu-id="5eef2-163">NTFS-Start Block</span><span class="sxs-lookup"><span data-stu-id="5eef2-163">NTFS Boot Block</span></span><br/>                                                         |
| <dl> <span data-ttu-id="5eef2-164"><dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="5eef2-164"><dt>10</dt></span></span> </dl> | <span data-ttu-id="5eef2-165">Start-Manager</span><span class="sxs-lookup"><span data-stu-id="5eef2-165">Boot Manager</span></span><br/>                                                            |
| <dl> <span data-ttu-id="5eef2-166"><dt>11</dt></span><span class="sxs-lookup"><span data-stu-id="5eef2-166"><dt>11</dt></span></span> </dl> | <span data-ttu-id="5eef2-167">BitLocker-Access Control</span><span class="sxs-lookup"><span data-stu-id="5eef2-167">BitLocker Access Control</span></span><br/>                                                |
| <dl> <span data-ttu-id="5eef2-168"><dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="5eef2-168"><dt>12</dt></span></span> </dl> | <span data-ttu-id="5eef2-169">Definiert für die Verwendung durch das statische Betriebssystem</span><span class="sxs-lookup"><span data-stu-id="5eef2-169">Defined for use by the static operating system</span></span><br/>                          |
| <dl> <span data-ttu-id="5eef2-170"><dt>13</dt></span><span class="sxs-lookup"><span data-stu-id="5eef2-170"><dt>13</dt></span></span> </dl> | <span data-ttu-id="5eef2-171">Definiert für die Verwendung durch das statische Betriebssystem</span><span class="sxs-lookup"><span data-stu-id="5eef2-171">Defined for use by the static operating system</span></span><br/>                          |
| <dl> <span data-ttu-id="5eef2-172"><dt>14</dt></span><span class="sxs-lookup"><span data-stu-id="5eef2-172"><dt>14</dt></span></span> </dl> | <span data-ttu-id="5eef2-173">Definiert für die Verwendung durch das statische Betriebssystem</span><span class="sxs-lookup"><span data-stu-id="5eef2-173">Defined for use by the static operating system</span></span><br/>                          |
| <dl> <span data-ttu-id="5eef2-174"><dt>15</dt></span><span class="sxs-lookup"><span data-stu-id="5eef2-174"><dt>15</dt></span></span> </dl> | <span data-ttu-id="5eef2-175">Definiert für die Verwendung durch das statische Betriebssystem</span><span class="sxs-lookup"><span data-stu-id="5eef2-175">Defined for use by the static operating system</span></span><br/>                          |
| <dl> <span data-ttu-id="5eef2-176"><dt>16</dt></span><span class="sxs-lookup"><span data-stu-id="5eef2-176"><dt>16</dt></span></span> </dl> | <span data-ttu-id="5eef2-177">Zum Debuggen verwendet</span><span class="sxs-lookup"><span data-stu-id="5eef2-177">Used for debugging</span></span><br/>                                                      |
| <dl> <span data-ttu-id="5eef2-178"><dt>17</dt></span><span class="sxs-lookup"><span data-stu-id="5eef2-178"><dt>17</dt></span></span> </dl> | <span data-ttu-id="5eef2-179">Dynamische CRTM</span><span class="sxs-lookup"><span data-stu-id="5eef2-179">Dynamic CRTM</span></span><br/>                                                            |
| <dl> <span data-ttu-id="5eef2-180"><dt>Jahren</dt></span><span class="sxs-lookup"><span data-stu-id="5eef2-180"><dt>18</dt></span></span> </dl> | <span data-ttu-id="5eef2-181">Plattform definiert</span><span class="sxs-lookup"><span data-stu-id="5eef2-181">Platform defined</span></span><br/>                                                        |
| <dl> <span data-ttu-id="5eef2-182"><dt>19</dt></span><span class="sxs-lookup"><span data-stu-id="5eef2-182"><dt>19</dt></span></span> </dl> | <span data-ttu-id="5eef2-183">Wird von einem vertrauenswürdigen Betriebssystem verwendet</span><span class="sxs-lookup"><span data-stu-id="5eef2-183">Used by a trusted operating system</span></span><br/>                                      |
| <dl> <span data-ttu-id="5eef2-184"><dt>20</dt></span><span class="sxs-lookup"><span data-stu-id="5eef2-184"><dt>20</dt></span></span> </dl> | <span data-ttu-id="5eef2-185">Wird von einem vertrauenswürdigen Betriebssystem verwendet</span><span class="sxs-lookup"><span data-stu-id="5eef2-185">Used by a trusted operating system</span></span><br/>                                      |
| <dl> <span data-ttu-id="5eef2-186"><dt>21</dt></span><span class="sxs-lookup"><span data-stu-id="5eef2-186"><dt>21</dt></span></span> </dl> | <span data-ttu-id="5eef2-187">Wird von einem vertrauenswürdigen Betriebssystem verwendet</span><span class="sxs-lookup"><span data-stu-id="5eef2-187">Used by a trusted operating system</span></span><br/>                                      |
| <dl> <span data-ttu-id="5eef2-188"><dt>22</dt></span><span class="sxs-lookup"><span data-stu-id="5eef2-188"><dt>22</dt></span></span> </dl> | <span data-ttu-id="5eef2-189">Wird von einem vertrauenswürdigen Betriebssystem verwendet</span><span class="sxs-lookup"><span data-stu-id="5eef2-189">Used by a trusted operating system</span></span><br/>                                      |
| <dl> <span data-ttu-id="5eef2-190"><dt>23</dt></span><span class="sxs-lookup"><span data-stu-id="5eef2-190"><dt>23</dt></span></span> </dl> | <span data-ttu-id="5eef2-191">Anwendungsunterstützung</span><span class="sxs-lookup"><span data-stu-id="5eef2-191">Application support</span></span><br/>                                                     |



 

</dd> <dt>

<span data-ttu-id="5eef2-192">*ExternalKey* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="5eef2-192">*ExternalKey* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="5eef2-193">Typ: **Uint8 \[ \]**</span><span class="sxs-lookup"><span data-stu-id="5eef2-193">Type: **uint8\[\]**</span></span>

<span data-ttu-id="5eef2-194">Ein Bytearray, das den externen 256-Bit-Schlüssel angibt, der zum Entsperren des Volumes beim Starten des Computers verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="5eef2-194">An array of bytes that specifies the 256-bit external key used to unlock the volume when the computer starts.</span></span>

<span data-ttu-id="5eef2-195">Wenn kein externer Schlüssel angegeben ist, wird eine nach dem Zufallsprinzip generiert.</span><span class="sxs-lookup"><span data-stu-id="5eef2-195">If no external key is specified, one is randomly generated.</span></span> <span data-ttu-id="5eef2-196">Verwenden Sie die [**getkeyprotectorexternalkey**](getkeyprotectorexternalkey-win32-encryptablevolume.md) -Methode, um den zufällig generierten Schlüssel abzurufen.</span><span class="sxs-lookup"><span data-stu-id="5eef2-196">Use the [**GetKeyProtectorExternalKey**](getkeyprotectorexternalkey-win32-encryptablevolume.md) method to obtain the randomly generated key.</span></span>

</dd> <dt>

<span data-ttu-id="5eef2-197">*Volumekeyprotectorid* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="5eef2-197">*VolumeKeyProtectorID* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5eef2-198">Typ: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="5eef2-198">Type: **string**</span></span>

<span data-ttu-id="5eef2-199">Eine Zeichenfolge, die der eindeutige Bezeichner ist, der der erstellten Schlüssel Schutzvorrichtung zugeordnet ist und zum Verwalten der Schlüssel Schutzvorrichtung verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="5eef2-199">A string that is the unique identifier associated with the created key protector that can be used to manage the key protector.</span></span>

<span data-ttu-id="5eef2-200">Wenn das Laufwerk die Hardware Verschlüsselung unterstützt und BitLocker keinen bandbesitz hat, wird die ID-Zeichenfolge auf "BitLocker" festgelegt, und die Schlüssel Schutzvorrichtung wird in die pro-Band-Metadaten geschrieben.</span><span class="sxs-lookup"><span data-stu-id="5eef2-200">If the drive supports hardware encryption and BitLocker has not taken band ownership, the ID string is set to "BitLocker" and the key protector is written to per band metadata.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5eef2-201">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5eef2-201">Return value</span></span>

<span data-ttu-id="5eef2-202">Typ: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5eef2-202">Type: **uint32**</span></span>

<span data-ttu-id="5eef2-203">Diese Methode gibt einen der folgenden Codes oder einen anderen Fehlercode zurück, wenn ein Fehler auftritt.</span><span class="sxs-lookup"><span data-stu-id="5eef2-203">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="5eef2-204">Rückgabecode/-wert</span><span class="sxs-lookup"><span data-stu-id="5eef2-204">Return code/value</span></span>                                                                                                                                                                         | <span data-ttu-id="5eef2-205">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5eef2-205">Description</span></span>                                                                                                                                                                                                                                                            |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="5eef2-206"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="5eef2-206"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                         | <span data-ttu-id="5eef2-207">Die Methode war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="5eef2-207">The method was successful.</span></span><br/>                                                                                                                                                                                                                                  |
| <dl> <span data-ttu-id="5eef2-208"><dt>**F \_ E \_ gesperrt \_ Volume**</dt> <dt>2150694912 (0x80310000)</dt></span><span class="sxs-lookup"><span data-stu-id="5eef2-208"><dt>**FVE\_E\_LOCKED\_VOLUME**</dt> <dt>2150694912 (0x80310000)</dt></span></span> </dl>        | <span data-ttu-id="5eef2-209">Das Volume ist gesperrt.</span><span class="sxs-lookup"><span data-stu-id="5eef2-209">The volume is locked.</span></span><br/>                                                                                                                                                                                                                                       |
| <dl> <span data-ttu-id="5eef2-210"><dt>**TSB \_ E- \_ Dienst wird \_ nicht \_ ausgeführt**</dt> <dt>2150121480 (0x80284008)</dt></span><span class="sxs-lookup"><span data-stu-id="5eef2-210"><dt>**TBS\_E\_SERVICE\_NOT\_RUNNING**</dt> <dt>2150121480 (0x80284008)</dt></span></span> </dl> | <span data-ttu-id="5eef2-211">Auf diesem Computer wurde kein kompatibles TPM gefunden.</span><span class="sxs-lookup"><span data-stu-id="5eef2-211">No compatible TPM is found on this computer.</span></span><br/>                                                                                                                                                                                                                |
| <dl> <span data-ttu-id="5eef2-212"><dt>**F \_ E- \_ Fremd \_ Volume**</dt> <dt>2150694947 (0x80310023)</dt></span><span class="sxs-lookup"><span data-stu-id="5eef2-212"><dt>**FVE\_E\_FOREIGN\_VOLUME**</dt> <dt>2150694947 (0x80310023)</dt></span></span> </dl>       | <span data-ttu-id="5eef2-213">Das TPM kann den Verschlüsselungsschlüssel des Volumes nicht sichern, da das Volume nicht das aktuell Betriebssystem enthält.</span><span class="sxs-lookup"><span data-stu-id="5eef2-213">The TPM cannot secure the volume's encryption key because the volume does not contain the currently running operating system.</span></span><br/>                                                                                                                               |
| <dl> <span data-ttu-id="5eef2-214"><dt>**E \_ InvalidArg**</dt> <dt>2147942487 (0x80070057)</dt></span><span class="sxs-lookup"><span data-stu-id="5eef2-214"><dt>**E\_INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt></span></span> </dl>                 | <span data-ttu-id="5eef2-215">Der *platformvalidationprofile* -Parameter wird bereitgestellt, seine Werte befinden sich jedoch nicht innerhalb des bekannten Bereichs oder stimmen nicht mit der derzeit gültigen Gruppenrichtlinie Einstellung identisch.</span><span class="sxs-lookup"><span data-stu-id="5eef2-215">The *PlatformValidationProfile* parameter is provided, but its values are not within the known range, or it does not match the Group Policy setting currently in effect.</span></span><br/> <span data-ttu-id="5eef2-216">Der *ExternalKey* -Parameter wird bereitgestellt, ist aber kein Array der Größe 32.</span><span class="sxs-lookup"><span data-stu-id="5eef2-216">The *ExternalKey* parameter is provided but is not an array of size 32.</span></span><br/> |
| <dl> <span data-ttu-id="5eef2-217"><dt>**F \_ E \_ Bootable \_ CDDVD**</dt> <dt>2150694960 (0x80310030)</dt></span><span class="sxs-lookup"><span data-stu-id="5eef2-217"><dt>**FVE\_E\_BOOTABLE\_CDDVD**</dt> <dt>2150694960 (0x80310030)</dt></span></span> </dl>       | <span data-ttu-id="5eef2-218">Auf diesem Computer wurde eine Start fähige CD/DVD gefunden.</span><span class="sxs-lookup"><span data-stu-id="5eef2-218">A bootable CD/DVD is found in this computer.</span></span> <span data-ttu-id="5eef2-219">Entfernen Sie die CD/DVD, und starten Sie den Computer neu.</span><span class="sxs-lookup"><span data-stu-id="5eef2-219">Remove the CD/DVD and restart the computer.</span></span><br/>                                                                                                                                                                    |
| <dl> <span data-ttu-id="5eef2-220"><dt>**F \_ E \_ Protector \_ vorhanden**</dt> <dt>2150694961 (0x80310031)</dt></span><span class="sxs-lookup"><span data-stu-id="5eef2-220"><dt>**FVE\_E\_PROTECTOR\_EXISTS**</dt> <dt>2150694961 (0x80310031)</dt></span></span> </dl>     | <span data-ttu-id="5eef2-221">Eine Schlüssel Schutzvorrichtung dieses Typs ist bereits vorhanden.</span><span class="sxs-lookup"><span data-stu-id="5eef2-221">A key protector of this type already exists.</span></span><br/>                                                                                                                                                                                                                |



 

## <a name="security-considerations"></a><span data-ttu-id="5eef2-222">Überlegungen zur Sicherheit</span><span class="sxs-lookup"><span data-stu-id="5eef2-222">Security Considerations</span></span>

<span data-ttu-id="5eef2-223">Für die Sicherheit Ihres Computers wird das Standardprofil empfohlen.</span><span class="sxs-lookup"><span data-stu-id="5eef2-223">For the security of your computer, we recommend the default profile.</span></span> <span data-ttu-id="5eef2-224">Verwenden Sie ein Profil von PCRs 0, 2, 4, 5, 8, 9, 10 und 11, um zusätzlichen Schutz vor den Änderungen am Anfang des Start Codes zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="5eef2-224">For additional protection against early startup code changes, use a profile of PCRs 0, 2, 4, 5, 8, 9, 10, and 11.</span></span> <span data-ttu-id="5eef2-225">Um zusätzlichen Schutz vor Änderungen der frühen Startkonfiguration zu erhalten, verwenden Sie ein Profil von PCRs 0, 1, 2, 3, 4, 5, 8, 9, 10, 11.</span><span class="sxs-lookup"><span data-stu-id="5eef2-225">For additional protection against early startup configuration changes, use a profile of PCRs 0, 1, 2, 3, 4, 5, 8, 9, 10, 11.</span></span>

<span data-ttu-id="5eef2-226">Das Ändern des Standard Profils wirkt sich auf die Sicherheit oder Nutzbarkeit Ihres Computers aus.</span><span class="sxs-lookup"><span data-stu-id="5eef2-226">Changing from the default profile affects the security or usability of your computer.</span></span>

## <a name="remarks"></a><span data-ttu-id="5eef2-227">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5eef2-227">Remarks</span></span>

<span data-ttu-id="5eef2-228">Es kann höchstens eine Schlüssel Schutzvorrichtung vom Typ "TPM und Systemstart Schlüssel" für ein Volume vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="5eef2-228">At most one key protector of type "TPM And Startup Key" can exist for a volume at any time.</span></span> <span data-ttu-id="5eef2-229">Wenn Sie den anzeigen Amen oder das Platt Form Validierungs Profil ändern möchten, das von einer vorhandenen Schlüssel Schutzvorrichtung vom Typ "TPM plus Startup Key" verwendet wird, müssen Sie zunächst die vorhandene Schlüssel Schutzvorrichtung entfernen und dann **protectkeywithtpmandstartupkey** aufrufen, um eine neue zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="5eef2-229">If you want to change the display name or the platform validation profile used by an existing "TPM plus Startup Key" key protector, you must first remove the existing key protector and then call **ProtectKeyWithTPMAndStartupKey** to create a new one.</span></span> <span data-ttu-id="5eef2-230">Zum Entsperren des Volumes in Wiederherstellungs Szenarien, in denen der Zugriff auf den Verschlüsselungsschlüssel des Volumes nicht abgerufen werden kann, müssen zusätzliche Schlüssel Schutzvorrichtungen angegeben werden. Dies ist beispielsweise der Fall, wenn das TPM nicht mit dem Platt Form Validierungs Profil überprüft werden kann oder wenn der USB-Speicher, der den externen Schlüssel enthält, verloren geht</span><span class="sxs-lookup"><span data-stu-id="5eef2-230">Additional key protectors should be specified to unlock the volume in recovery scenarios where access to the volume's encryption key cannot be obtained; for example, when the TPM cannot successfully validate against the platform validation profile or when USB memory that contains the external key is lost.</span></span>

<span data-ttu-id="5eef2-231">Verwenden Sie [**protectkeywithexternalkey**](protectkeywithexternalkey-win32-encryptablevolume.md) oder [**protectkeywithnumericalpassword**](protectkeywithnumericalpassword-win32-encryptablevolume.md) , um eine oder mehrere Schlüssel Schutzvorrichtungen für die Wiederherstellung eines anderweitig gesperrten Volumes zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="5eef2-231">Use [**ProtectKeyWithExternalKey**](protectkeywithexternalkey-win32-encryptablevolume.md) or [**ProtectKeyWithNumericalPassword**](protectkeywithnumericalpassword-win32-encryptablevolume.md) to create one or more key protectors for recovering an otherwise locked volume.</span></span>

<span data-ttu-id="5eef2-232">Obwohl es möglich ist, sowohl eine Schlüssel Schutzvorrichtung vom Typ "TPM" als auch einen anderen Typ "TPM und Systemstart Schlüssel" zu haben, negiert das vorhanden sein des TPM-schlüsselschutzschutztyps die Auswirkungen anderer TPM-basierter Schlüssel Schutzvorrichtungen.</span><span class="sxs-lookup"><span data-stu-id="5eef2-232">While it is possible to have both a key protector of the type "TPM" and another of the type "TPM And Startup Key", the presence of the "TPM" key protector type negates the effects of other TPM-based key protectors.</span></span>

<span data-ttu-id="5eef2-233">Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen.</span><span class="sxs-lookup"><span data-stu-id="5eef2-233">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="5eef2-234">MOF-Dateien werden nicht als Teil des Windows SDK installiert.</span><span class="sxs-lookup"><span data-stu-id="5eef2-234">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="5eef2-235">Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="5eef2-235">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="5eef2-236">Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="5eef2-236">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="5eef2-237">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5eef2-237">Requirements</span></span>



| <span data-ttu-id="5eef2-238">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5eef2-238">Requirement</span></span> | <span data-ttu-id="5eef2-239">Wert</span><span class="sxs-lookup"><span data-stu-id="5eef2-239">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5eef2-240">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5eef2-240">Minimum supported client</span></span><br/> | <span data-ttu-id="5eef2-241">Nur Windows Vista Enterprise, Windows Vista Ultimate \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5eef2-241">Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="5eef2-242">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5eef2-242">Minimum supported server</span></span><br/> | <span data-ttu-id="5eef2-243">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5eef2-243">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="5eef2-244">Namespace</span><span class="sxs-lookup"><span data-stu-id="5eef2-244">Namespace</span></span><br/>                | <span data-ttu-id="5eef2-245">Root \\ CIMV2 \\ Sicherheit ( \\ microsoftvolumeencryption)</span><span class="sxs-lookup"><span data-stu-id="5eef2-245">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="5eef2-246">MOF</span><span class="sxs-lookup"><span data-stu-id="5eef2-246">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5eef2-247"><dt>Win32 \_ verschlüsseltablevolume. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="5eef2-247"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5eef2-248">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5eef2-248">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5eef2-249">**Win32- \_ verschlüsseltablevolume**</span><span class="sxs-lookup"><span data-stu-id="5eef2-249">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> <dt>

[<span data-ttu-id="5eef2-250">**Win32- \_ TPM**</span><span class="sxs-lookup"><span data-stu-id="5eef2-250">**Win32\_Tpm**</span></span>](win32-tpm.md)
</dt> </dl>

 

 
