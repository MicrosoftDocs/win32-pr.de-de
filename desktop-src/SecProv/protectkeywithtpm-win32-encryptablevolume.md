---
description: Wenn die Trusted Platform Module (TPM) verfügbar ist, wird mit dieser Methode der Verschlüsselungsschlüssel des Volumes gesichert.
ms.assetid: 79bee9ca-c86a-482b-a06f-1cfb887e7fae
title: Protectkeywithtpm-Methode der Win32_EncryptableVolume-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.ProtectKeyWithTPM
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 0369e44d96a4f1dcacf33dbf1b1da6ad6d37eed2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362367"
---
# <a name="protectkeywithtpm-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="3d6c7-103">Protectkeywithtpm-Methode der Win32- \_ Klasse "verschlüsseltablevolume"</span><span class="sxs-lookup"><span data-stu-id="3d6c7-103">ProtectKeyWithTPM method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="3d6c7-104">Die **protectkeywithtpm** -Methode der Win32-Klasse " [**\_ verschlüsseltablevolume**](win32-encryptablevolume.md) " sichert den Verschlüsselungsschlüssel des Volumes mithilfe der Trusted Platform Module (TPM)-Sicherheits Hardware auf dem Computer, falls verfügbar.</span><span class="sxs-lookup"><span data-stu-id="3d6c7-104">The **ProtectKeyWithTPM** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class secures the volume's encryption key by using the Trusted Platform Module (TPM) Security Hardware on the computer, if available.</span></span>

<span data-ttu-id="3d6c7-105">Für das Volume wird eine Schlüssel Schutzvorrichtung vom Typ "TPM" erstellt, sofern noch keine vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="3d6c7-105">A key protector of type "TPM" is created for the volume, if one does not already exist.</span></span>

<span data-ttu-id="3d6c7-106">Diese Methode ist nur für das Volume anwendbar, das das aktuell laufende Betriebssystem enthält, und, wenn nicht bereits eine Schlüssel Schutzvorrichtung auf dem Volume vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="3d6c7-106">This method is only applicable for the volume that contains the currently running operating system, and if a key protector does not already exist on the volume.</span></span>

## <a name="syntax"></a><span data-ttu-id="3d6c7-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="3d6c7-107">Syntax</span></span>


```mof
uint32 ProtectKeyWithTPM(
  [in, optional] string FriendlyName,
  [in, optional] uint8  PlatformValidationProfile[],
  [out]          string VolumeKeyProtectorID
);
```



## <a name="parameters"></a><span data-ttu-id="3d6c7-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="3d6c7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3d6c7-109">*FriendlyName* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="3d6c7-109">*FriendlyName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="3d6c7-110">Typ: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="3d6c7-110">Type: **string**</span></span>

<span data-ttu-id="3d6c7-111">Eine Zeichenfolge, die einen vom Benutzer zugewiesenen Zeichen folgen Bezeichner für diese Schlüssel Schutzvorrichtung angibt.</span><span class="sxs-lookup"><span data-stu-id="3d6c7-111">A string that specifies a user-assigned string identifier for this key protector.</span></span> <span data-ttu-id="3d6c7-112">Wenn dieser Parameter nicht angegeben wird, wird ein leerer Wert verwendet.</span><span class="sxs-lookup"><span data-stu-id="3d6c7-112">If this parameter is not specified, a blank value is used.</span></span>

</dd> <dt>

<span data-ttu-id="3d6c7-113">*Platformvalidationprofile* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="3d6c7-113">*PlatformValidationProfile* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="3d6c7-114">Typ: **Uint8 \[ \]**</span><span class="sxs-lookup"><span data-stu-id="3d6c7-114">Type: **uint8\[\]**</span></span>

<span data-ttu-id="3d6c7-115">Ein Array von ganzen Zahlen, das angibt, wie die Sicherheits Hardware des Computers Trusted Platform Module (TPM) den Verschlüsselungsschlüssel des festplattenvolumens sichert.</span><span class="sxs-lookup"><span data-stu-id="3d6c7-115">An array of integers that specifies how the computer's Trusted Platform Module (TPM) Security Hardware secures the disk volume's encryption key.</span></span>

<span data-ttu-id="3d6c7-116">Ein Platt Form Validierungs Profil besteht aus einem Satz von Platt Form Konfigurations Register Indizes (PCR), der zwischen 0 und 23 (einschließlich) liegt.</span><span class="sxs-lookup"><span data-stu-id="3d6c7-116">A platform validation profile consists of a set of Platform Configuration Register (PCR) indices ranging from 0 to 23, inclusive.</span></span> <span data-ttu-id="3d6c7-117">Wiederholungswerte im-Parameter werden ignoriert.</span><span class="sxs-lookup"><span data-stu-id="3d6c7-117">Repeat values in the parameter are ignored.</span></span> <span data-ttu-id="3d6c7-118">Jeder PCR-Index ist mit Diensten verknüpft, die beim Starten des Betriebssystems ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="3d6c7-118">Each PCR index is associated with services that run when the operating system starts.</span></span> <span data-ttu-id="3d6c7-119">Jedes Mal, wenn der Computer gestartet wird, prüft das TPM, ob die Dienste, die Sie im Platt Form Validierungs Profil angegeben haben, nicht geändert wurden.</span><span class="sxs-lookup"><span data-stu-id="3d6c7-119">Each time the computer starts, the TPM will check that the services you specified in the platform validation profile have not changed.</span></span> <span data-ttu-id="3d6c7-120">Wenn sich einer dieser Dienste ändert, während BitLocker-Laufwerkverschlüsselung (BDE)-Schutz beibehalten wird, gibt das TPM den Verschlüsselungsschlüssel nicht frei, um das Datenträger Volume zu entsperren, und der Computer wechselt in den Wiederherstellungs Modus.</span><span class="sxs-lookup"><span data-stu-id="3d6c7-120">If any of these services change while BitLocker Drive Encryption (BDE) protection remains on, the TPM will not release the encryption key to unlock the disk volume and the computer will enter into recovery mode.</span></span>

<span data-ttu-id="3d6c7-121">Wenn dieser Parameter angegeben wird, während die entsprechende Gruppenrichtlinie Einstellung aktiviert ist, muss er mit der Gruppenrichtlinie Einstellung übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="3d6c7-121">If this parameter is specified while the corresponding Group Policy setting has been enabled, it must match the Group Policy setting.</span></span>

<span data-ttu-id="3d6c7-122">Wenn dieser Parameter nicht angegeben wird, wird der Standardwert 0, 2, 4, 5, 8, 9, 10 und 11 verwendet.</span><span class="sxs-lookup"><span data-stu-id="3d6c7-122">If this parameter is not specified, the default of 0, 2, 4, 5, 8, 9, 10, and 11 is used.</span></span> <span data-ttu-id="3d6c7-123">Das standardmäßige Platt Form Validierungs Profil sichert den Verschlüsselungsschlüssel vor Änderungen am Kern Stamm der Trust of measurement (CRTM), BIOS-und Platt Form Erweiterungen (PCR 0), Option ROM-Code (PCR 2), der MBR (Master Boot Record)-Code (PCR), die MBR-Partitionstabelle (Master Boot Record) (PCR), der NTFS-Startsektor (PCR 8), der NTFS-Start Code (PCR 9), der Start-Manager (PCR 10) und die BitLocker-Laufwerkverschlüsselung Access Control (PCR 11).</span><span class="sxs-lookup"><span data-stu-id="3d6c7-123">The default platform validation profile secures the encryption key against changes to the Core Root of Trust of Measurement (CRTM), BIOS, and Platform Extensions (PCR 0), Option ROM Code (PCR 2), the Master Boot Record (MBR) Code (PCR 4), the Master Boot Record (MBR) Partition Table (PCR 5), the NTFS Boot Sector (PCR 8), the NTFS Boot Code (PCR 9), the Boot Manager (PCR 10), and the BitLocker Drive Encryption Access Control (PCR 11).</span></span> <span data-ttu-id="3d6c7-124">Für die Sicherheit Ihres Computers wird das Standardprofil empfohlen.</span><span class="sxs-lookup"><span data-stu-id="3d6c7-124">For the security of your computer, we recommend the default profile.</span></span> <span data-ttu-id="3d6c7-125">Unified Extensible Firmware Interface (UEFI) – Computer verwenden standardmäßig nicht PCR 5.</span><span class="sxs-lookup"><span data-stu-id="3d6c7-125">Unified Extensible Firmware Interface (UEFI)–based computers do not use PCR 5 by default.</span></span> <span data-ttu-id="3d6c7-126">Um zusätzlichen Schutz vor Änderungen der frühen Startkonfiguration zu erhalten, verwenden Sie ein Profil von PCRs 0, 1, 2, 3, 4, 5, 8, 9, 10, 11.</span><span class="sxs-lookup"><span data-stu-id="3d6c7-126">For additional protection against early startup configuration changes, use a profile of PCRs 0, 1, 2, 3, 4, 5, 8, 9, 10, 11.</span></span>

<span data-ttu-id="3d6c7-127">Das Ändern des Standard Profils wirkt sich auf die Sicherheit und Verwaltbarkeit Ihres Computers aus.</span><span class="sxs-lookup"><span data-stu-id="3d6c7-127">Changing from the default profile affects the security and manageability of your computer.</span></span> <span data-ttu-id="3d6c7-128">Die Vertraulichkeit von BitLocker zu Platt Formänderungen (bösartig oder autorisiert) wird abhängig vom Inklusions-oder Ausschluss Wert des PCRs angehoben oder verringert.</span><span class="sxs-lookup"><span data-stu-id="3d6c7-128">The sensitivity of BitLocker to platform modifications (malicious or authorized) is increased or decreased depending upon the inclusion or exclusion, respectively, of the PCRs.</span></span> <span data-ttu-id="3d6c7-129">Damit der BitLocker-Schutz aktiviert werden kann, muss das Platt Form Validierungs Profil PCR 11 enthalten.</span><span class="sxs-lookup"><span data-stu-id="3d6c7-129">For BitLocker protection to be enabled, the platform validation profile must include PCR 11.</span></span>



| <span data-ttu-id="3d6c7-130">Wert</span><span class="sxs-lookup"><span data-stu-id="3d6c7-130">Value</span></span>                                                                         | <span data-ttu-id="3d6c7-131">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="3d6c7-131">Meaning</span></span>                                                                             |
|-------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="3d6c7-132"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="3d6c7-132"><dt>0</dt></span></span> </dl>  | <span data-ttu-id="3d6c7-133">Kern Stamm der Vertrauens Stellungen von Messgeräten (CRTM), BIOS und Plattformen.</span><span class="sxs-lookup"><span data-stu-id="3d6c7-133">Core Root of Trust of Measurement (CRTM), BIOS, and Platform Extensions.</span></span><br/> |
| <dl> <span data-ttu-id="3d6c7-134"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="3d6c7-134"><dt>1</dt></span></span> </dl>  | <span data-ttu-id="3d6c7-135">Konfiguration und Daten von Plattform und Motherboard</span><span class="sxs-lookup"><span data-stu-id="3d6c7-135">Platform and Motherboard Configuration and Data</span></span><br/>                          |
| <dl> <span data-ttu-id="3d6c7-136"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="3d6c7-136"><dt>2</dt></span></span> </dl>  | <span data-ttu-id="3d6c7-137">Option-ROM-Code</span><span class="sxs-lookup"><span data-stu-id="3d6c7-137">Option ROM Code</span></span><br/>                                                          |
| <dl> <span data-ttu-id="3d6c7-138"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="3d6c7-138"><dt>3</dt></span></span> </dl>  | <span data-ttu-id="3d6c7-139">Option ROM-Konfiguration und-Daten</span><span class="sxs-lookup"><span data-stu-id="3d6c7-139">Option ROM Configuration and Data</span></span><br/>                                        |
| <dl> <span data-ttu-id="3d6c7-140"><dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="3d6c7-140"><dt>4</dt></span></span> </dl>  | <span data-ttu-id="3d6c7-141">MBR-Code (Master Boot Record)</span><span class="sxs-lookup"><span data-stu-id="3d6c7-141">Master Boot Record (MBR) Code</span></span><br/>                                            |
| <dl> <span data-ttu-id="3d6c7-142"><dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="3d6c7-142"><dt>5</dt></span></span> </dl>  | <span data-ttu-id="3d6c7-143">MBR-Partitionstabelle (Master Boot Record)</span><span class="sxs-lookup"><span data-stu-id="3d6c7-143">Master Boot Record (MBR) Partition Table</span></span><br/>                                 |
| <dl> <span data-ttu-id="3d6c7-144"><dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="3d6c7-144"><dt>6</dt></span></span> </dl>  | <span data-ttu-id="3d6c7-145">Zustandsübergänge und Aktivierungs Ereignisse</span><span class="sxs-lookup"><span data-stu-id="3d6c7-145">State Transition and Wake Events</span></span><br/>                                         |
| <dl> <span data-ttu-id="3d6c7-146"><dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="3d6c7-146"><dt>7</dt></span></span> </dl>  | <span data-ttu-id="3d6c7-147">Computer Manufacturer-Specific</span><span class="sxs-lookup"><span data-stu-id="3d6c7-147">Computer Manufacturer-Specific</span></span><br/>                                           |
| <dl> <span data-ttu-id="3d6c7-148"><dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="3d6c7-148"><dt>8</dt></span></span> </dl>  | <span data-ttu-id="3d6c7-149">NTFS-Startsektor</span><span class="sxs-lookup"><span data-stu-id="3d6c7-149">NTFS Boot Sector</span></span><br/>                                                         |
| <dl> <span data-ttu-id="3d6c7-150"><dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="3d6c7-150"><dt>9</dt></span></span> </dl>  | <span data-ttu-id="3d6c7-151">NTFS-Start Code</span><span class="sxs-lookup"><span data-stu-id="3d6c7-151">NTFS Boot Code</span></span><br/>                                                           |
| <dl> <span data-ttu-id="3d6c7-152"><dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="3d6c7-152"><dt>10</dt></span></span> </dl> | <span data-ttu-id="3d6c7-153">Start-Manager</span><span class="sxs-lookup"><span data-stu-id="3d6c7-153">Boot Manager</span></span><br/>                                                             |
| <dl> <span data-ttu-id="3d6c7-154"><dt>11</dt></span><span class="sxs-lookup"><span data-stu-id="3d6c7-154"><dt>11</dt></span></span> </dl> | <span data-ttu-id="3d6c7-155">BitLocker-Laufwerkverschlüsselung Access Control</span><span class="sxs-lookup"><span data-stu-id="3d6c7-155">BitLocker Drive Encryption Access Control</span></span><br/>                                |
| <dl> <span data-ttu-id="3d6c7-156"><dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="3d6c7-156"><dt>12</dt></span></span> </dl> | <span data-ttu-id="3d6c7-157">Definiert für die Verwendung durch das statische Betriebssystem</span><span class="sxs-lookup"><span data-stu-id="3d6c7-157">Defined for use by the static operating system</span></span><br/>                           |
| <dl> <span data-ttu-id="3d6c7-158"><dt>13</dt></span><span class="sxs-lookup"><span data-stu-id="3d6c7-158"><dt>13</dt></span></span> </dl> | <span data-ttu-id="3d6c7-159">Definiert für die Verwendung durch das statische Betriebssystem</span><span class="sxs-lookup"><span data-stu-id="3d6c7-159">Defined for use by the static operating system</span></span><br/>                           |
| <dl> <span data-ttu-id="3d6c7-160"><dt>14</dt></span><span class="sxs-lookup"><span data-stu-id="3d6c7-160"><dt>14</dt></span></span> </dl> | <span data-ttu-id="3d6c7-161">Definiert für die Verwendung durch das statische Betriebssystem</span><span class="sxs-lookup"><span data-stu-id="3d6c7-161">Defined for use by the static operating system</span></span><br/>                           |
| <dl> <span data-ttu-id="3d6c7-162"><dt>15</dt></span><span class="sxs-lookup"><span data-stu-id="3d6c7-162"><dt>15</dt></span></span> </dl> | <span data-ttu-id="3d6c7-163">Definiert für die Verwendung durch das statische Betriebssystem</span><span class="sxs-lookup"><span data-stu-id="3d6c7-163">Defined for use by the static operating system</span></span><br/>                           |
| <dl> <span data-ttu-id="3d6c7-164"><dt>16</dt></span><span class="sxs-lookup"><span data-stu-id="3d6c7-164"><dt>16</dt></span></span> </dl> | <span data-ttu-id="3d6c7-165">Zum Debuggen verwendet</span><span class="sxs-lookup"><span data-stu-id="3d6c7-165">Used for debugging</span></span><br/>                                                       |
| <dl> <span data-ttu-id="3d6c7-166"><dt>17</dt></span><span class="sxs-lookup"><span data-stu-id="3d6c7-166"><dt>17</dt></span></span> </dl> | <span data-ttu-id="3d6c7-167">Dynamische CRTM</span><span class="sxs-lookup"><span data-stu-id="3d6c7-167">Dynamic CRTM</span></span><br/>                                                             |
| <dl> <span data-ttu-id="3d6c7-168"><dt>Jahren</dt></span><span class="sxs-lookup"><span data-stu-id="3d6c7-168"><dt>18</dt></span></span> </dl> | <span data-ttu-id="3d6c7-169">Plattform definiert</span><span class="sxs-lookup"><span data-stu-id="3d6c7-169">Platform defined</span></span><br/>                                                         |
| <dl> <span data-ttu-id="3d6c7-170"><dt>19</dt></span><span class="sxs-lookup"><span data-stu-id="3d6c7-170"><dt>19</dt></span></span> </dl> | <span data-ttu-id="3d6c7-171">Wird von einem vertrauenswürdigen Betriebssystem verwendet</span><span class="sxs-lookup"><span data-stu-id="3d6c7-171">Used by trusted operating system</span></span><br/>                                         |
| <dl> <span data-ttu-id="3d6c7-172"><dt>20</dt></span><span class="sxs-lookup"><span data-stu-id="3d6c7-172"><dt>20</dt></span></span> </dl> | <span data-ttu-id="3d6c7-173">Wird von einem vertrauenswürdigen Betriebssystem verwendet</span><span class="sxs-lookup"><span data-stu-id="3d6c7-173">Used by trusted operating system</span></span><br/>                                         |
| <dl> <span data-ttu-id="3d6c7-174"><dt>21</dt></span><span class="sxs-lookup"><span data-stu-id="3d6c7-174"><dt>21</dt></span></span> </dl> | <span data-ttu-id="3d6c7-175">Wird von einem vertrauenswürdigen Betriebssystem verwendet</span><span class="sxs-lookup"><span data-stu-id="3d6c7-175">Used by trusted operating system</span></span><br/>                                         |
| <dl> <span data-ttu-id="3d6c7-176"><dt>22</dt></span><span class="sxs-lookup"><span data-stu-id="3d6c7-176"><dt>22</dt></span></span> </dl> | <span data-ttu-id="3d6c7-177">Wird von einem vertrauenswürdigen Betriebssystem verwendet</span><span class="sxs-lookup"><span data-stu-id="3d6c7-177">Used by trusted operating system</span></span><br/>                                         |
| <dl> <span data-ttu-id="3d6c7-178"><dt>23</dt></span><span class="sxs-lookup"><span data-stu-id="3d6c7-178"><dt>23</dt></span></span> </dl> | <span data-ttu-id="3d6c7-179">Anwendungsunterstützung</span><span class="sxs-lookup"><span data-stu-id="3d6c7-179">Application support</span></span><br/>                                                      |



 

</dd> <dt>

<span data-ttu-id="3d6c7-180">*Volumekeyprotectorid* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="3d6c7-180">*VolumeKeyProtectorID* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3d6c7-181">Typ: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="3d6c7-181">Type: **string**</span></span>

<span data-ttu-id="3d6c7-182">Eine Zeichenfolge, die die erstellte Schutzvorrichtung eindeutig identifiziert und zum Verwalten der Schlüssel Schutzvorrichtung verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="3d6c7-182">A string that uniquely identifies the created protector and which can be used to manage the key protector.</span></span>

<span data-ttu-id="3d6c7-183">Wenn das Laufwerk die Hardware Verschlüsselung unterstützt und BitLocker keinen bandbesitz hat, wird die ID-Zeichenfolge auf "BitLocker" festgelegt, und die Schlüssel Schutzvorrichtung wird in die pro-Band-Metadaten geschrieben.</span><span class="sxs-lookup"><span data-stu-id="3d6c7-183">If the drive supports hardware encryption and BitLocker has not taken band ownership, the ID string is set to "BitLocker" and the key protector is written to per band metadata.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3d6c7-184">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3d6c7-184">Return value</span></span>

<span data-ttu-id="3d6c7-185">Typ: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3d6c7-185">Type: **uint32**</span></span>

<span data-ttu-id="3d6c7-186">Diese Methode gibt einen der folgenden Codes oder einen anderen Fehlercode zurück, wenn ein Fehler auftritt.</span><span class="sxs-lookup"><span data-stu-id="3d6c7-186">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="3d6c7-187">Rückgabecode/-wert</span><span class="sxs-lookup"><span data-stu-id="3d6c7-187">Return code/value</span></span>                                                                                                                                                                         | <span data-ttu-id="3d6c7-188">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3d6c7-188">Description</span></span>                                                                                                                                                                        |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="3d6c7-189"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="3d6c7-189"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                         | <span data-ttu-id="3d6c7-190">Die Methode war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="3d6c7-190">The method was successful.</span></span><br/>                                                                                                                                              |
| <dl> <span data-ttu-id="3d6c7-191"><dt>**F \_ E \_ gesperrt \_ Volume**</dt> <dt>2150694912 (0x80310000)</dt></span><span class="sxs-lookup"><span data-stu-id="3d6c7-191"><dt>**FVE\_E\_LOCKED\_VOLUME**</dt> <dt>2150694912 (0x80310000)</dt></span></span> </dl>        | <span data-ttu-id="3d6c7-192">Das Volume ist gesperrt.</span><span class="sxs-lookup"><span data-stu-id="3d6c7-192">The volume is locked.</span></span><br/>                                                                                                                                                   |
| <dl> <span data-ttu-id="3d6c7-193"><dt>**TSB \_ E- \_ Dienst wird \_ nicht \_ ausgeführt**</dt> <dt>2150121480 (0x80284008)</dt></span><span class="sxs-lookup"><span data-stu-id="3d6c7-193"><dt>**TBS\_E\_SERVICE\_NOT\_RUNNING**</dt> <dt>2150121480 (0x80284008)</dt></span></span> </dl> | <span data-ttu-id="3d6c7-194">Auf diesem Computer wurde kein kompatibles TPM gefunden.</span><span class="sxs-lookup"><span data-stu-id="3d6c7-194">No compatible TPM is found on this computer.</span></span><br/>                                                                                                                            |
| <dl> <span data-ttu-id="3d6c7-195"><dt>**F \_ E- \_ Fremd \_ Volume**</dt> <dt>2150694947 (0x80310023)</dt></span><span class="sxs-lookup"><span data-stu-id="3d6c7-195"><dt>**FVE\_E\_FOREIGN\_VOLUME**</dt> <dt>2150694947 (0x80310023)</dt></span></span> </dl>       | <span data-ttu-id="3d6c7-196">Das TPM kann den Verschlüsselungsschlüssel des Volumes nicht sichern, da das Volume nicht das aktuell Betriebssystem enthält.</span><span class="sxs-lookup"><span data-stu-id="3d6c7-196">The TPM cannot secure the volume's encryption key because the volume does not contain the currently running operating system.</span></span><br/>                                           |
| <dl> <span data-ttu-id="3d6c7-197"><dt>**E \_ InvalidArg**</dt> <dt>2147942487 (0x80070057)</dt></span><span class="sxs-lookup"><span data-stu-id="3d6c7-197"><dt>**E\_INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt></span></span> </dl>                 | <span data-ttu-id="3d6c7-198">Der *platformvalidationprofile* -Parameter wird bereitgestellt, seine Werte befinden sich jedoch nicht im bekannten Bereich, oder er entspricht nicht der aktuell geltenden Gruppenrichtlinie Einstellung.</span><span class="sxs-lookup"><span data-stu-id="3d6c7-198">The *PlatformValidationProfile* parameter is provided but its values are not within the known range, or it does not match the Group Policy setting currently in effect.</span></span><br/> |
| <dl> <span data-ttu-id="3d6c7-199"><dt>**F \_ E \_ Protector \_ vorhanden**</dt> <dt>2150694961 (0x80310031)</dt></span><span class="sxs-lookup"><span data-stu-id="3d6c7-199"><dt>**FVE\_E\_PROTECTOR\_EXISTS**</dt> <dt>2150694961 (0x80310031)</dt></span></span> </dl>            | <span data-ttu-id="3d6c7-200">Eine Schlüssel Schutzvorrichtung dieses Typs ist bereits vorhanden.</span><span class="sxs-lookup"><span data-stu-id="3d6c7-200">A key protector of this type already exists.</span></span><br/>                                                                                                                             |



 

## <a name="security-considerations"></a><span data-ttu-id="3d6c7-201">Überlegungen zur Sicherheit</span><span class="sxs-lookup"><span data-stu-id="3d6c7-201">Security Considerations</span></span>

<span data-ttu-id="3d6c7-202">Für die Sicherheit Ihres Computers wird das Standardprofil empfohlen.</span><span class="sxs-lookup"><span data-stu-id="3d6c7-202">For the security of your computer, we recommend the default profile.</span></span> <span data-ttu-id="3d6c7-203">Um zusätzlichen Schutz vor Änderungen der frühen Startkonfiguration zu erhalten, verwenden Sie ein Profil von PCRs 0, 1, 2, 3, 4, 5, 8, 9, 10, 11.</span><span class="sxs-lookup"><span data-stu-id="3d6c7-203">For additional protection against early startup configuration changes, use a profile of PCRs 0, 1, 2, 3, 4, 5, 8, 9, 10, 11.</span></span>

<span data-ttu-id="3d6c7-204">Das Ändern des Standard Profils wirkt sich auf die Sicherheit oder Nutzbarkeit Ihres Computers aus.</span><span class="sxs-lookup"><span data-stu-id="3d6c7-204">Changing from the default profile affects the security or usability of your computer.</span></span>

## <a name="remarks"></a><span data-ttu-id="3d6c7-205">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3d6c7-205">Remarks</span></span>

<span data-ttu-id="3d6c7-206">Es kann höchstens eine Schlüssel Schutzvorrichtung vom Typ "TPM" für ein Volume vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="3d6c7-206">At most one key protector of type "TPM" can exist for a volume at any time.</span></span> <span data-ttu-id="3d6c7-207">Wenn Sie den anzeigen Amen oder das Platt Form Validierungs Profil ändern möchten, das von einer vorhandenen TPM-Schlüssel Schutzvorrichtung verwendet wird, müssen Sie zuerst die vorhandene Schlüssel Schutzvorrichtung entfernen und dann **protectkeywithtpm** aufrufen, um eine neue zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="3d6c7-207">If you want to change the display name or the platform validation profile used by an existing "TPM" key protector, you must first remove the existing key protector and then call **ProtectKeyWithTPM** to create a new one.</span></span>

<span data-ttu-id="3d6c7-208">Bei den PCR-Indizes 0 bis 5 werden die aktuellen Messungen in den Registern verwendet, um den Verschlüsselungsschlüssel zu schützen.</span><span class="sxs-lookup"><span data-stu-id="3d6c7-208">For PCR indices 0 through 5, the current measurements in the registers are used to protect the encryption key.</span></span> <span data-ttu-id="3d6c7-209">Bei den PCR-Werten 8 bis 11 werden die verwendeten Messwerte beim nächsten Start Durchlauf erwartet.</span><span class="sxs-lookup"><span data-stu-id="3d6c7-209">For PCR values 8 through 11, the measurements used are the ones expected to exist on the next start cycle.</span></span>

<span data-ttu-id="3d6c7-210">Zum Entsperren des Volumes in Wiederherstellungs Szenarien, in denen der Zugriff auf den Verschlüsselungsschlüssel des Volumes nicht abgerufen werden kann, müssen zusätzliche Schlüssel Schutzvorrichtungen angegeben werden. Dies kann beispielsweise der Fall sein, wenn das TPM nicht mit dem Platt Form Validierungs Profil überprüft werden kann.</span><span class="sxs-lookup"><span data-stu-id="3d6c7-210">Additional key protectors should be specified to unlock the volume in recovery scenarios where access to the volume's encryption key cannot be obtained; for example, when the TPM cannot successfully validate against the platform validation profile.</span></span> <span data-ttu-id="3d6c7-211">Verwenden Sie [**protectkeywithexternalkey**](protectkeywithexternalkey-win32-encryptablevolume.md) oder [**protectkeywithnumericalpassword**](protectkeywithnumericalpassword-win32-encryptablevolume.md) , um eine oder mehrere Schlüssel Schutzvorrichtungen für die Wiederherstellung eines anderweitig gesperrten Volumes zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="3d6c7-211">Use [**ProtectKeyWithExternalKey**](protectkeywithexternalkey-win32-encryptablevolume.md) or [**ProtectKeyWithNumericalPassword**](protectkeywithnumericalpassword-win32-encryptablevolume.md) to create one or more key protectors for recovering an otherwise locked volume.</span></span>

<span data-ttu-id="3d6c7-212">Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen.</span><span class="sxs-lookup"><span data-stu-id="3d6c7-212">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="3d6c7-213">MOF-Dateien werden nicht als Teil des Windows SDK installiert.</span><span class="sxs-lookup"><span data-stu-id="3d6c7-213">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="3d6c7-214">Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="3d6c7-214">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="3d6c7-215">Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="3d6c7-215">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="3d6c7-216">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3d6c7-216">Requirements</span></span>



| <span data-ttu-id="3d6c7-217">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3d6c7-217">Requirement</span></span> | <span data-ttu-id="3d6c7-218">Wert</span><span class="sxs-lookup"><span data-stu-id="3d6c7-218">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3d6c7-219">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="3d6c7-219">Minimum supported client</span></span><br/> | <span data-ttu-id="3d6c7-220">Nur Windows Vista Enterprise, Windows Vista Ultimate \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3d6c7-220">Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="3d6c7-221">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="3d6c7-221">Minimum supported server</span></span><br/> | <span data-ttu-id="3d6c7-222">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3d6c7-222">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="3d6c7-223">Namespace</span><span class="sxs-lookup"><span data-stu-id="3d6c7-223">Namespace</span></span><br/>                | <span data-ttu-id="3d6c7-224">Root \\ CIMV2 \\ Sicherheit ( \\ microsoftvolumeencryption)</span><span class="sxs-lookup"><span data-stu-id="3d6c7-224">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="3d6c7-225">MOF</span><span class="sxs-lookup"><span data-stu-id="3d6c7-225">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3d6c7-226"><dt>Win32 \_ verschlüsseltablevolume. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="3d6c7-226"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3d6c7-227">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3d6c7-227">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3d6c7-228">**Win32- \_ verschlüsseltablevolume**</span><span class="sxs-lookup"><span data-stu-id="3d6c7-228">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> <dt>

[<span data-ttu-id="3d6c7-229">**Win32- \_ TPM**</span><span class="sxs-lookup"><span data-stu-id="3d6c7-229">**Win32\_Tpm**</span></span>](win32-tpm.md)
</dt> </dl>

 

 
