---
description: Wenn die Trusted Platform Module (TPM) verfügbar ist, sichert diese Methode den Verschlüsselungsschlüssel des Volumes, der durch eine benutzerspezifische Identifikationsnummer erweitert wurde.
ms.assetid: 8c4c434a-dd60-491a-a983-b3fa78c91c0d
title: Protectkeywithtpmandpin-Methode der Win32_EncryptableVolume-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.ProtectKeyWithTPMAndPIN
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: e5a0a7a253723bec84df7a86fa94ab182bd192dc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862279"
---
# <a name="protectkeywithtpmandpin-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="2e9c0-103">Protectkeywithtpmandpin-Methode der Win32- \_ Klasse "verschlüsseltablevolume"</span><span class="sxs-lookup"><span data-stu-id="2e9c0-103">ProtectKeyWithTPMAndPIN method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="2e9c0-104">Die **protectkeywithtpmandpin** -Methode der Win32-Klasse " [**\_ verschlüsseltablevolume**](win32-encryptablevolume.md) " sichert den Verschlüsselungsschlüssel des Volumes mithilfe der TPM-Sicherheits Hardware (Trusted Platform Module) auf dem Computer, sofern verfügbar, erweitert durch eine benutzerdefinierte ID (Personal Identification Number, PIN), die dem Computer beim startbereit gestellt werden muss.</span><span class="sxs-lookup"><span data-stu-id="2e9c0-104">The **ProtectKeyWithTPMAndPIN** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class secures the volume's encryption key by using the Trusted Platform Module (TPM) Security Hardware on the computer, if available, enhanced by a user-specified personal identification number (PIN) that must be provided to the computer at startup.</span></span>

<span data-ttu-id="2e9c0-105">Sowohl die Validierung durch das TPM als auch die Eingabe der persönlichen Identifikations Zeichenfolge sind erforderlich, um auf den Verschlüsselungsschlüssel des Volumes zuzugreifen und den volumeinhalt zu entsperren.</span><span class="sxs-lookup"><span data-stu-id="2e9c0-105">Both validation by the TPM and input of the personal identification string are necessary to access the volume's encryption key and unlock volume contents.</span></span>

<span data-ttu-id="2e9c0-106">Diese Methode ist nur für das Volume anwendbar, das das aktuell laufende Betriebssystem enthält.</span><span class="sxs-lookup"><span data-stu-id="2e9c0-106">This method is only applicable for the volume that contains the currently running operating system.</span></span>

<span data-ttu-id="2e9c0-107">Eine Schlüssel Schutzvorrichtung vom Typ "TPM und PIN" wird für das Volume erstellt, sofern nicht bereits vorhanden.</span><span class="sxs-lookup"><span data-stu-id="2e9c0-107">A key protector of type "TPM And PIN" is created for the volume, if one does not already exist.</span></span>

## <a name="syntax"></a><span data-ttu-id="2e9c0-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="2e9c0-108">Syntax</span></span>


```mof
uint32 ProtectKeyWithTPMAndPIN(
  [in, optional] string FriendlyName,
  [in, optional] uint8  PlatformValidationProfile[],
  [in]           string PIN,
  [out]          string VolumeKeyProtectorID
);
```



## <a name="parameters"></a><span data-ttu-id="2e9c0-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="2e9c0-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2e9c0-110">*FriendlyName* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="2e9c0-110">*FriendlyName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="2e9c0-111">Typ: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="2e9c0-111">Type: **string**</span></span>

<span data-ttu-id="2e9c0-112">Ein vom Benutzer zugewiesener Zeichen folgen Bezeichner für diese Schlüssel Schutzvorrichtung.</span><span class="sxs-lookup"><span data-stu-id="2e9c0-112">A user-assigned string identifier for this key protector.</span></span> <span data-ttu-id="2e9c0-113">Wenn dieser Parameter nicht angegeben wird, wird ein leerer Wert verwendet.</span><span class="sxs-lookup"><span data-stu-id="2e9c0-113">If this parameter is not specified, a blank value is used.</span></span>

</dd> <dt>

<span data-ttu-id="2e9c0-114">*Platformvalidationprofile* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="2e9c0-114">*PlatformValidationProfile* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="2e9c0-115">Typ: **Uint8 \[ \]**</span><span class="sxs-lookup"><span data-stu-id="2e9c0-115">Type: **uint8\[\]**</span></span>

<span data-ttu-id="2e9c0-116">Ein Array von ganzen Zahlen, das angibt, wie die Sicherheits Hardware des Computers Trusted Platform Module (TPM) den Verschlüsselungsschlüssel des festplattenvolumens sichert.</span><span class="sxs-lookup"><span data-stu-id="2e9c0-116">An array of integers that specifies how the computer's Trusted Platform Module (TPM) Security Hardware secures the disk volume's encryption key.</span></span>

<span data-ttu-id="2e9c0-117">Ein Platt Form Validierungs Profil besteht aus einem Satz von Platt Form Konfigurations Register Indizes (PCR), der zwischen 0 und 23 (einschließlich) liegt.</span><span class="sxs-lookup"><span data-stu-id="2e9c0-117">A platform validation profile consists of a set of Platform Configuration Register (PCR) indices ranging from 0 to 23, inclusive.</span></span> <span data-ttu-id="2e9c0-118">Wiederholungswerte im-Parameter werden ignoriert.</span><span class="sxs-lookup"><span data-stu-id="2e9c0-118">Repeat values in the parameter are ignored.</span></span> <span data-ttu-id="2e9c0-119">Jeder PCR-Index ist mit Diensten verknüpft, die beim Starten des Betriebssystems ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="2e9c0-119">Each PCR index is associated with services that run when the operating system starts.</span></span> <span data-ttu-id="2e9c0-120">Jedes Mal, wenn der Computer gestartet wird, prüft das TPM, ob die Dienste, die Sie im Platt Form Validierungs Profil angegeben haben, nicht geändert wurden.</span><span class="sxs-lookup"><span data-stu-id="2e9c0-120">Each time the computer starts, the TPM will check that the services you specified in the platform validation profile have not changed.</span></span> <span data-ttu-id="2e9c0-121">Wenn sich einer dieser Dienste ändert, während BitLocker-Laufwerkverschlüsselung (BDE)-Schutz beibehalten wird, gibt das TPM den Verschlüsselungsschlüssel nicht frei, um das Datenträger Volume zu entsperren, und der Computer wechselt in den Wiederherstellungs Modus.</span><span class="sxs-lookup"><span data-stu-id="2e9c0-121">If any of these services change while BitLocker Drive Encryption (BDE) protection remains on, the TPM will not release the encryption key to unlock the disk volume, and the computer will enter into recovery mode.</span></span>

<span data-ttu-id="2e9c0-122">Wenn dieser Parameter angegeben wird, während die entsprechende Gruppenrichtlinie Einstellung aktiviert ist, muss er mit der Gruppenrichtlinie Einstellung übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="2e9c0-122">If this parameter is specified while the corresponding Group Policy setting has been enabled, it must match the Group Policy setting.</span></span>

<span data-ttu-id="2e9c0-123">Wenn dieser Parameter nicht angegeben wird, wird der Standardwert 0, 2, 4, 5, 8, 9, 10 und 11 verwendet.</span><span class="sxs-lookup"><span data-stu-id="2e9c0-123">If this parameter is not specified, the default of 0, 2, 4, 5, 8, 9, 10, and 11 is used.</span></span> <span data-ttu-id="2e9c0-124">Das standardmäßige Platt Form Validierungs Profil sichert den Verschlüsselungsschlüssel vor Änderungen an den folgenden Elementen:</span><span class="sxs-lookup"><span data-stu-id="2e9c0-124">The default platform validation profile secures the encryption key against changes to the following elements:</span></span>

-   <span data-ttu-id="2e9c0-125">Kern Stamm der Messgeräte Vertrauensstellung (CRTM)</span><span class="sxs-lookup"><span data-stu-id="2e9c0-125">Core Root of Trust of Measurement (CRTM)</span></span>
-   <span data-ttu-id="2e9c0-126">BIOS</span><span class="sxs-lookup"><span data-stu-id="2e9c0-126">BIOS</span></span>
-   <span data-ttu-id="2e9c0-127">Platt Form Erweiterungen (PCR 0)</span><span class="sxs-lookup"><span data-stu-id="2e9c0-127">Platform Extensions (PCR 0)</span></span>
-   <span data-ttu-id="2e9c0-128">Options-ROM-Code (PCR 2)</span><span class="sxs-lookup"><span data-stu-id="2e9c0-128">Option ROM Code (PCR 2)</span></span>
-   <span data-ttu-id="2e9c0-129">Master Boot Record (MBR)-Code (PCR 4)</span><span class="sxs-lookup"><span data-stu-id="2e9c0-129">Master Boot Record (MBR) Code (PCR 4)</span></span>
-   <span data-ttu-id="2e9c0-130">MBR-Partitionstabelle (Master Boot Record) (PCR 5)</span><span class="sxs-lookup"><span data-stu-id="2e9c0-130">Master Boot Record (MBR) Partition Table (PCR 5)</span></span>
-   <span data-ttu-id="2e9c0-131">NTFS-Startsektor (PCR 8)</span><span class="sxs-lookup"><span data-stu-id="2e9c0-131">NTFS Boot Sector (PCR 8)</span></span>
-   <span data-ttu-id="2e9c0-132">NTFS-Startblock (PCR 9)</span><span class="sxs-lookup"><span data-stu-id="2e9c0-132">NTFS Boot Block (PCR 9)</span></span>
-   <span data-ttu-id="2e9c0-133">Start-Manager (PCR 10)</span><span class="sxs-lookup"><span data-stu-id="2e9c0-133">Boot Manager (PCR 10)</span></span>
-   <span data-ttu-id="2e9c0-134">BitLocker-Zugriffssteuerung (PCR 11)</span><span class="sxs-lookup"><span data-stu-id="2e9c0-134">BitLocker Access Control (PCR 11)</span></span>

<span data-ttu-id="2e9c0-135">Für die Sicherheit Ihres Computers wird das Standardprofil empfohlen.</span><span class="sxs-lookup"><span data-stu-id="2e9c0-135">For the security of your computer, we recommend the default profile.</span></span> <span data-ttu-id="2e9c0-136">Um zusätzlichen Schutz vor Änderungen der frühen Startkonfiguration zu erhalten, verwenden Sie ein Profil von PCRs 0, 1, 2, 3, 4, 5, 8, 9, 10, 11.</span><span class="sxs-lookup"><span data-stu-id="2e9c0-136">For additional protection against early startup configuration changes, use a profile of PCRs 0, 1, 2, 3, 4, 5, 8, 9, 10, 11.</span></span> <span data-ttu-id="2e9c0-137">Unified Extensible Firmware Interface (UEFI) – Computer verwenden standardmäßig nicht PCR 5.</span><span class="sxs-lookup"><span data-stu-id="2e9c0-137">Unified Extensible Firmware Interface (UEFI)–based computers do not use PCR 5 by default.</span></span>

<span data-ttu-id="2e9c0-138">Das Ändern des Standard Profils wirkt sich auf die Sicherheit und Verwaltbarkeit Ihres Computers aus.</span><span class="sxs-lookup"><span data-stu-id="2e9c0-138">Changing from the default profile affects the security and manageability of your computer.</span></span> <span data-ttu-id="2e9c0-139">Die Vertraulichkeit von BitLocker zu Platt Formänderungen (bösartig oder autorisiert) wird abhängig vom Inklusions-oder Ausschluss Wert des PCRs angehoben oder verringert.</span><span class="sxs-lookup"><span data-stu-id="2e9c0-139">The sensitivity of BitLocker to platform modifications (malicious or authorized) is increased or decreased depending upon the inclusion or exclusion, respectively, of the PCRs.</span></span> <span data-ttu-id="2e9c0-140">Damit der BitLocker-Schutz aktiviert werden kann, muss das Platt Form Validierungs Profil PCR 11 enthalten.</span><span class="sxs-lookup"><span data-stu-id="2e9c0-140">For BitLocker protection to be enabled, the platform validation profile must include PCR 11.</span></span>



| <span data-ttu-id="2e9c0-141">Wert</span><span class="sxs-lookup"><span data-stu-id="2e9c0-141">Value</span></span>                                                                         | <span data-ttu-id="2e9c0-142">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="2e9c0-142">Meaning</span></span>                                                                            |
|-------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="2e9c0-143"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="2e9c0-143"><dt>0</dt></span></span> </dl>  | <span data-ttu-id="2e9c0-144">Kern Stamm der Vertrauens Stellungen von Messgeräten (CRTM), BIOS und Plattformen</span><span class="sxs-lookup"><span data-stu-id="2e9c0-144">Core Root of Trust of Measurement (CRTM), BIOS, and Platform Extensions</span></span><br/> |
| <dl> <span data-ttu-id="2e9c0-145"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="2e9c0-145"><dt>1</dt></span></span> </dl>  | <span data-ttu-id="2e9c0-146">Konfiguration und Daten von Plattform und Motherboard</span><span class="sxs-lookup"><span data-stu-id="2e9c0-146">Platform and Motherboard Configuration and Data</span></span><br/>                         |
| <dl> <span data-ttu-id="2e9c0-147"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="2e9c0-147"><dt>2</dt></span></span> </dl>  | <span data-ttu-id="2e9c0-148">Option-ROM-Code</span><span class="sxs-lookup"><span data-stu-id="2e9c0-148">Option ROM Code</span></span><br/>                                                         |
| <dl> <span data-ttu-id="2e9c0-149"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="2e9c0-149"><dt>3</dt></span></span> </dl>  | <span data-ttu-id="2e9c0-150">Option ROM-Konfiguration und-Daten</span><span class="sxs-lookup"><span data-stu-id="2e9c0-150">Option ROM Configuration and Data</span></span><br/>                                       |
| <dl> <span data-ttu-id="2e9c0-151"><dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="2e9c0-151"><dt>4</dt></span></span> </dl>  | <span data-ttu-id="2e9c0-152">MBR-Code (Master Boot Record)</span><span class="sxs-lookup"><span data-stu-id="2e9c0-152">Master Boot Record (MBR) Code</span></span><br/>                                           |
| <dl> <span data-ttu-id="2e9c0-153"><dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="2e9c0-153"><dt>5</dt></span></span> </dl>  | <span data-ttu-id="2e9c0-154">MBR-Partitionstabelle (Master Boot Record)</span><span class="sxs-lookup"><span data-stu-id="2e9c0-154">Master Boot Record (MBR) Partition Table</span></span><br/>                                |
| <dl> <span data-ttu-id="2e9c0-155"><dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="2e9c0-155"><dt>6</dt></span></span> </dl>  | <span data-ttu-id="2e9c0-156">Zustandsübergänge und Aktivierungs Ereignisse</span><span class="sxs-lookup"><span data-stu-id="2e9c0-156">State Transition and Wake Events</span></span><br/>                                        |
| <dl> <span data-ttu-id="2e9c0-157"><dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="2e9c0-157"><dt>7</dt></span></span> </dl>  | <span data-ttu-id="2e9c0-158">Computer Manufacturer-Specific</span><span class="sxs-lookup"><span data-stu-id="2e9c0-158">Computer Manufacturer-Specific</span></span><br/>                                          |
| <dl> <span data-ttu-id="2e9c0-159"><dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="2e9c0-159"><dt>8</dt></span></span> </dl>  | <span data-ttu-id="2e9c0-160">NTFS-Startsektor</span><span class="sxs-lookup"><span data-stu-id="2e9c0-160">NTFS Boot Sector</span></span><br/>                                                        |
| <dl> <span data-ttu-id="2e9c0-161"><dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="2e9c0-161"><dt>9</dt></span></span> </dl>  | <span data-ttu-id="2e9c0-162">NTFS-Start Block</span><span class="sxs-lookup"><span data-stu-id="2e9c0-162">NTFS Boot Block</span></span><br/>                                                         |
| <dl> <span data-ttu-id="2e9c0-163"><dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="2e9c0-163"><dt>10</dt></span></span> </dl> | <span data-ttu-id="2e9c0-164">Start-Manager</span><span class="sxs-lookup"><span data-stu-id="2e9c0-164">Boot Manager</span></span><br/>                                                            |
| <dl> <span data-ttu-id="2e9c0-165"><dt>11</dt></span><span class="sxs-lookup"><span data-stu-id="2e9c0-165"><dt>11</dt></span></span> </dl> | <span data-ttu-id="2e9c0-166">BitLocker-Access Control</span><span class="sxs-lookup"><span data-stu-id="2e9c0-166">BitLocker Access Control</span></span><br/>                                                |
| <dl> <span data-ttu-id="2e9c0-167"><dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="2e9c0-167"><dt>12</dt></span></span> </dl> | <span data-ttu-id="2e9c0-168">Definiert für die Verwendung durch das statische Betriebssystem</span><span class="sxs-lookup"><span data-stu-id="2e9c0-168">Defined for use by the static operating system</span></span><br/>                          |
| <dl> <span data-ttu-id="2e9c0-169"><dt>13</dt></span><span class="sxs-lookup"><span data-stu-id="2e9c0-169"><dt>13</dt></span></span> </dl> | <span data-ttu-id="2e9c0-170">Definiert für die Verwendung durch das statische Betriebssystem</span><span class="sxs-lookup"><span data-stu-id="2e9c0-170">Defined for use by the static operating system</span></span><br/>                          |
| <dl> <span data-ttu-id="2e9c0-171"><dt>14</dt></span><span class="sxs-lookup"><span data-stu-id="2e9c0-171"><dt>14</dt></span></span> </dl> | <span data-ttu-id="2e9c0-172">Definiert für die Verwendung durch das statische Betriebssystem</span><span class="sxs-lookup"><span data-stu-id="2e9c0-172">Defined for use by the static operating system</span></span><br/>                          |
| <dl> <span data-ttu-id="2e9c0-173"><dt>15</dt></span><span class="sxs-lookup"><span data-stu-id="2e9c0-173"><dt>15</dt></span></span> </dl> | <span data-ttu-id="2e9c0-174">Definiert für die Verwendung durch das statische Betriebssystem</span><span class="sxs-lookup"><span data-stu-id="2e9c0-174">Defined for use by the static operating system</span></span><br/>                          |
| <dl> <span data-ttu-id="2e9c0-175"><dt>16</dt></span><span class="sxs-lookup"><span data-stu-id="2e9c0-175"><dt>16</dt></span></span> </dl> | <span data-ttu-id="2e9c0-176">Zum Debuggen verwendet</span><span class="sxs-lookup"><span data-stu-id="2e9c0-176">Used for debugging</span></span><br/>                                                      |
| <dl> <span data-ttu-id="2e9c0-177"><dt>17</dt></span><span class="sxs-lookup"><span data-stu-id="2e9c0-177"><dt>17</dt></span></span> </dl> | <span data-ttu-id="2e9c0-178">Dynamische CRTM</span><span class="sxs-lookup"><span data-stu-id="2e9c0-178">Dynamic CRTM</span></span><br/>                                                            |
| <dl> <span data-ttu-id="2e9c0-179"><dt>Jahren</dt></span><span class="sxs-lookup"><span data-stu-id="2e9c0-179"><dt>18</dt></span></span> </dl> | <span data-ttu-id="2e9c0-180">Plattform definiert</span><span class="sxs-lookup"><span data-stu-id="2e9c0-180">Platform defined</span></span><br/>                                                        |
| <dl> <span data-ttu-id="2e9c0-181"><dt>19</dt></span><span class="sxs-lookup"><span data-stu-id="2e9c0-181"><dt>19</dt></span></span> </dl> | <span data-ttu-id="2e9c0-182">Wird von einem vertrauenswürdigen Betriebssystem verwendet</span><span class="sxs-lookup"><span data-stu-id="2e9c0-182">Used by a trusted operating system</span></span><br/>                                      |
| <dl> <span data-ttu-id="2e9c0-183"><dt>20</dt></span><span class="sxs-lookup"><span data-stu-id="2e9c0-183"><dt>20</dt></span></span> </dl> | <span data-ttu-id="2e9c0-184">Wird von einem vertrauenswürdigen Betriebssystem verwendet</span><span class="sxs-lookup"><span data-stu-id="2e9c0-184">Used by a trusted operating system</span></span><br/>                                      |
| <dl> <span data-ttu-id="2e9c0-185"><dt>21</dt></span><span class="sxs-lookup"><span data-stu-id="2e9c0-185"><dt>21</dt></span></span> </dl> | <span data-ttu-id="2e9c0-186">Wird von einem vertrauenswürdigen Betriebssystem verwendet</span><span class="sxs-lookup"><span data-stu-id="2e9c0-186">Used by a trusted operating system</span></span><br/>                                      |
| <dl> <span data-ttu-id="2e9c0-187"><dt>22</dt></span><span class="sxs-lookup"><span data-stu-id="2e9c0-187"><dt>22</dt></span></span> </dl> | <span data-ttu-id="2e9c0-188">Wird von einem vertrauenswürdigen Betriebssystem verwendet</span><span class="sxs-lookup"><span data-stu-id="2e9c0-188">Used by a trusted operating system</span></span><br/>                                      |
| <dl> <span data-ttu-id="2e9c0-189"><dt>23</dt></span><span class="sxs-lookup"><span data-stu-id="2e9c0-189"><dt>23</dt></span></span> </dl> | <span data-ttu-id="2e9c0-190">Anwendungsunterstützung</span><span class="sxs-lookup"><span data-stu-id="2e9c0-190">Application support</span></span><br/>                                                     |



 

</dd> <dt>

<span data-ttu-id="2e9c0-191">*Pin* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2e9c0-191">*PIN* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2e9c0-192">Typ: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="2e9c0-192">Type: **string**</span></span>

<span data-ttu-id="2e9c0-193">Eine vom Benutzer angegebene persönliche Identifikations Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="2e9c0-193">A user-specified personal identification string.</span></span> <span data-ttu-id="2e9c0-194">Diese Zeichenfolge muss aus einer Sequenz von 6 bis 20 Ziffern bestehen, oder, wenn die Gruppenrichtlinie "Erweiterte Pins für den Start zulassen" aktiviert ist, 6 bis 20 Buchstaben, Symbole, Leerzeichen oder Ziffern.</span><span class="sxs-lookup"><span data-stu-id="2e9c0-194">This string must consist of a sequence of 6 to 20 digits or, if the "Allow enhanced PINs for startup" group policy is enabled, 6 to 20 letters, symbols, spaces, or numbers.</span></span>

</dd> <dt>

<span data-ttu-id="2e9c0-195">*Volumekeyprotectorid* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="2e9c0-195">*VolumeKeyProtectorID* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2e9c0-196">Typ: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="2e9c0-196">Type: **string**</span></span>

<span data-ttu-id="2e9c0-197">Der aktualisierte eindeutige Zeichen folgen Bezeichner zum Verwalten einer verschlüsselten volumeschlüsselschutzvorrichtung.</span><span class="sxs-lookup"><span data-stu-id="2e9c0-197">The updated unique string identifier used to manage an encrypted volume key protector.</span></span>

<span data-ttu-id="2e9c0-198">Wenn das Laufwerk die Hardware Verschlüsselung unterstützt und BitLocker keinen bandbesitz hat, wird die ID-Zeichenfolge auf "BitLocker" festgelegt, und die Schlüssel Schutzvorrichtung wird in die pro-Band-Metadaten geschrieben.</span><span class="sxs-lookup"><span data-stu-id="2e9c0-198">If the drive supports hardware encryption and BitLocker has not taken band ownership, the ID string is set to "BitLocker" and the key protector is written to per band metadata.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2e9c0-199">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2e9c0-199">Return value</span></span>

<span data-ttu-id="2e9c0-200">Typ: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2e9c0-200">Type: **uint32**</span></span>

<span data-ttu-id="2e9c0-201">Diese Methode gibt einen der folgenden Codes oder einen anderen Fehlercode zurück, wenn ein Fehler auftritt.</span><span class="sxs-lookup"><span data-stu-id="2e9c0-201">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="2e9c0-202">Rückgabecode/-wert</span><span class="sxs-lookup"><span data-stu-id="2e9c0-202">Return code/value</span></span>                                                                                                                                                                                | <span data-ttu-id="2e9c0-203">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2e9c0-203">Description</span></span>                                                                                                                                                                         |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="2e9c0-204"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="2e9c0-204"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                                | <span data-ttu-id="2e9c0-205">Die Methode war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="2e9c0-205">The method was successful.</span></span><br/>                                                                                                                                               |
| <dl> <span data-ttu-id="2e9c0-206"><dt>**E \_ InvalidArg**</dt> <dt>2147942487 (0x80070057)</dt></span><span class="sxs-lookup"><span data-stu-id="2e9c0-206"><dt>**E\_INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt></span></span> </dl>                        | <span data-ttu-id="2e9c0-207">Der *platformvalidationprofile* -Parameter wird bereitgestellt, seine Werte befinden sich jedoch nicht innerhalb des bekannten Bereichs oder stimmen nicht mit der derzeit gültigen Gruppenrichtlinie Einstellung identisch.</span><span class="sxs-lookup"><span data-stu-id="2e9c0-207">The *PlatformValidationProfile* parameter is provided, but its values are not within the known range, or it does not match the Group Policy setting currently in effect.</span></span><br/> |
| <dl> <span data-ttu-id="2e9c0-208"><dt>**F \_ E \_ Bootable \_ CDDVD**</dt> <dt>2150694960 (0x80310030)</dt></span><span class="sxs-lookup"><span data-stu-id="2e9c0-208"><dt>**FVE\_E\_BOOTABLE\_CDDVD**</dt> <dt>2150694960 (0x80310030)</dt></span></span> </dl>              | <span data-ttu-id="2e9c0-209">Auf diesem Computer wurde eine Start fähige CD/DVD gefunden.</span><span class="sxs-lookup"><span data-stu-id="2e9c0-209">A bootable CD/DVD is found in this computer.</span></span> <span data-ttu-id="2e9c0-210">Entfernen Sie die CD/DVD, und starten Sie den Computer neu.</span><span class="sxs-lookup"><span data-stu-id="2e9c0-210">Remove the CD/DVD and restart the computer.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="2e9c0-211"><dt>**F \_ E- \_ Fremd \_ Volume**</dt> <dt>2150694947 (0x80310023)</dt></span><span class="sxs-lookup"><span data-stu-id="2e9c0-211"><dt>**FVE\_E\_FOREIGN\_VOLUME**</dt> <dt>2150694947 (0x80310023)</dt></span></span> </dl>              | <span data-ttu-id="2e9c0-212">Das TPM kann den Verschlüsselungsschlüssel des Volumes nicht sichern, da das Volume nicht das aktuell Betriebssystem enthält.</span><span class="sxs-lookup"><span data-stu-id="2e9c0-212">The TPM cannot secure the volume's encryption key because the volume does not contain the currently running operating system.</span></span><br/>                                            |
| <dl> <span data-ttu-id="2e9c0-213"><dt>**F \_ E \_ ungültige \_ Pin \_**</dt> -Zeichen <dt>2150695066 (0x8031009a)</dt></span><span class="sxs-lookup"><span data-stu-id="2e9c0-213"><dt>**FVE\_E\_INVALID\_PIN\_CHARS**</dt> <dt>2150695066 (0x8031009A)</dt></span></span> </dl>          | <span data-ttu-id="2e9c0-214">Der *newpin* -Parameter enthält ungültige Zeichen.</span><span class="sxs-lookup"><span data-stu-id="2e9c0-214">The *NewPIN* parameter contains characters that are not valid.</span></span> <span data-ttu-id="2e9c0-215">Wenn der Gruppenrichtlinie "Erweiterte Pins für den Start zulassen" deaktiviert ist, werden nur Ziffern unterstützt.</span><span class="sxs-lookup"><span data-stu-id="2e9c0-215">When the "Allow enhanced PINs for startup" Group Policy is disabled, only numbers are supported.</span></span><br/>          |
| <dl> <span data-ttu-id="2e9c0-216"><dt>**F \_ E \_ gesperrt \_ Volume**</dt> <dt>2150694912 (0x80310000)</dt></span><span class="sxs-lookup"><span data-stu-id="2e9c0-216"><dt>**FVE\_E\_LOCKED\_VOLUME**</dt> <dt>2150694912 (0x80310000)</dt></span></span> </dl>               | <span data-ttu-id="2e9c0-217">Das Volume ist gesperrt.</span><span class="sxs-lookup"><span data-stu-id="2e9c0-217">The volume is locked.</span></span><br/>                                                                                                                                                    |
| <dl> <span data-ttu-id="2e9c0-218"><dt>**F \_ E \_ Richtlinie \_ ungültige \_ Pin- \_ Länge**</dt> <dt>2150695016 (0x80310068)</dt></span><span class="sxs-lookup"><span data-stu-id="2e9c0-218"><dt>**FVE\_E\_POLICY\_INVALID\_PIN\_LENGTH**</dt> <dt>2150695016 (0x80310068)</dt></span></span> </dl> | <span data-ttu-id="2e9c0-219">Der angegebene *newpin* -Parameter ist entweder länger als 20 Zeichen, kürzer als 6 Zeichen oder kürzer als die durch Gruppenrichtlinie angegebene Mindestlänge.</span><span class="sxs-lookup"><span data-stu-id="2e9c0-219">The *NewPIN* parameter supplied is either longer than 20 characters, shorter than 6 characters, or shorter than the minimum length specified by Group Policy.</span></span><br/>            |
| <dl> <span data-ttu-id="2e9c0-220"><dt>**F \_ E \_ Protector \_ vorhanden**</dt> <dt>2150694961 (0x80310031)</dt></span><span class="sxs-lookup"><span data-stu-id="2e9c0-220"><dt>**FVE\_E\_PROTECTOR\_EXISTS**</dt> <dt>2150694961 (0x80310031)</dt></span></span> </dl>            | <span data-ttu-id="2e9c0-221">Eine Schlüssel Schutzvorrichtung dieses Typs ist bereits vorhanden.</span><span class="sxs-lookup"><span data-stu-id="2e9c0-221">A key protector of this type already exists.</span></span><br/>                                                                                                                             |
| <dl> <span data-ttu-id="2e9c0-222"><dt>**TSB \_ E- \_ Dienst wird \_ nicht \_ ausgeführt**</dt> <dt>2150121480 (0x80284008)</dt></span><span class="sxs-lookup"><span data-stu-id="2e9c0-222"><dt>**TBS\_E\_SERVICE\_NOT\_RUNNING**</dt> <dt>2150121480 (0x80284008)</dt></span></span> </dl>        | <span data-ttu-id="2e9c0-223">Auf diesem Computer wurde kein kompatibles TPM gefunden.</span><span class="sxs-lookup"><span data-stu-id="2e9c0-223">No compatible TPM is found on this computer.</span></span><br/>                                                                                                                             |



 

## <a name="security-considerations"></a><span data-ttu-id="2e9c0-224">Überlegungen zur Sicherheit</span><span class="sxs-lookup"><span data-stu-id="2e9c0-224">Security Considerations</span></span>

<span data-ttu-id="2e9c0-225">Für die Sicherheit Ihres Computers wird das Standardprofil empfohlen.</span><span class="sxs-lookup"><span data-stu-id="2e9c0-225">For the security of your computer, we recommend the default profile.</span></span> <span data-ttu-id="2e9c0-226">Verwenden Sie ein Profil von PCRs 0, 2, 4, 5, 8, 9, 10 und 11, um zusätzlichen Schutz vor den Änderungen am Anfang des Start Codes zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="2e9c0-226">For additional protection against early startup code changes, use a profile of PCRs 0, 2, 4, 5, 8, 9, 10, and 11.</span></span> <span data-ttu-id="2e9c0-227">Um zusätzlichen Schutz vor Änderungen der frühen Startkonfiguration zu erhalten, verwenden Sie ein Profil von PCRs 0, 1, 2, 3, 4, 5, 8, 9, 10, 11.</span><span class="sxs-lookup"><span data-stu-id="2e9c0-227">For additional protection against early startup configuration changes, use a profile of PCRs 0, 1, 2, 3, 4, 5, 8, 9, 10, 11.</span></span>

<span data-ttu-id="2e9c0-228">Das Ändern des Standard Profils wirkt sich auf die Sicherheit oder Nutzbarkeit Ihres Computers aus.</span><span class="sxs-lookup"><span data-stu-id="2e9c0-228">Changing from the default profile affects the security or usability of your computer.</span></span>

## <a name="remarks"></a><span data-ttu-id="2e9c0-229">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2e9c0-229">Remarks</span></span>

<span data-ttu-id="2e9c0-230">Es kann höchstens eine Schlüssel Schutzvorrichtung vom Typ "TPM und PIN" für ein Volume vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="2e9c0-230">At most one key protector of type "TPM And PIN" can exist for a volume at any time.</span></span> <span data-ttu-id="2e9c0-231">Wenn Sie den anzeigen Amen oder das Platt Form Validierungs Profil ändern möchten, das von einer vorhandenen TPM-und PIN-Schlüssel Schutzvorrichtung verwendet wird, müssen Sie zuerst die vorhandene Schlüssel Schutzvorrichtung entfernen und dann **protectkeywithtpmandpin** aufrufen, um eine neue zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="2e9c0-231">If you want to change the display name or the platform validation profile used by an existing "TPM And PIN" key protector, you must first remove the existing key protector and then call **ProtectKeyWithTPMAndPIN** to create a new one.</span></span>

<span data-ttu-id="2e9c0-232">Zum Entsperren des Volumes in Wiederherstellungs Szenarien, in denen der Zugriff auf den Verschlüsselungsschlüssel des Volumes nicht abgerufen werden kann, müssen zusätzliche Schlüssel Schutzvorrichtungen angegeben werden. Dies ist z. b. der Fall, wenn das TPM nicht mit dem Platt Form Validierungs Profil überprüft werden kann oder wenn die PIN verloren geht.</span><span class="sxs-lookup"><span data-stu-id="2e9c0-232">Additional key protectors should be specified to unlock the volume in recovery scenarios where access to the volume's encryption key cannot be obtained; for example, when the TPM cannot successfully validate against the platform validation profile or when the PIN is lost.</span></span>

<span data-ttu-id="2e9c0-233">Verwenden Sie [**protectkeywithexternalkey**](protectkeywithexternalkey-win32-encryptablevolume.md) oder [**protectkeywithnumericalpassword**](protectkeywithnumericalpassword-win32-encryptablevolume.md) , um eine oder mehrere Schlüssel Schutzvorrichtungen für die Wiederherstellung eines anderweitig gesperrten Volumes zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="2e9c0-233">Use [**ProtectKeyWithExternalKey**](protectkeywithexternalkey-win32-encryptablevolume.md) or [**ProtectKeyWithNumericalPassword**](protectkeywithnumericalpassword-win32-encryptablevolume.md) to create one or more key protectors for recovering an otherwise locked volume.</span></span>

<span data-ttu-id="2e9c0-234">Obwohl es möglich ist, sowohl eine Schlüssel Schutzvorrichtung vom Typ "TPM" als auch eine andere vom Typ "TPM und PIN" zu haben, negiert das vorhanden sein des schlüsselschutzschutztyps "TPM" die Auswirkungen anderer TPM-basierter Schlüssel Schutzvorrichtungen.</span><span class="sxs-lookup"><span data-stu-id="2e9c0-234">While it is possible to have both a key protector of the type "TPM" and another of the type "TPM And PIN", the presence of the "TPM" key protector type negates the effects of other TPM-based key protectors.</span></span>

<span data-ttu-id="2e9c0-235">Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen.</span><span class="sxs-lookup"><span data-stu-id="2e9c0-235">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="2e9c0-236">MOF-Dateien werden nicht als Teil des Windows SDK installiert.</span><span class="sxs-lookup"><span data-stu-id="2e9c0-236">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="2e9c0-237">Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="2e9c0-237">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="2e9c0-238">Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="2e9c0-238">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="2e9c0-239">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2e9c0-239">Requirements</span></span>



| <span data-ttu-id="2e9c0-240">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2e9c0-240">Requirement</span></span> | <span data-ttu-id="2e9c0-241">Wert</span><span class="sxs-lookup"><span data-stu-id="2e9c0-241">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2e9c0-242">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2e9c0-242">Minimum supported client</span></span><br/> | <span data-ttu-id="2e9c0-243">Nur Windows Vista Enterprise, Windows Vista Ultimate \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2e9c0-243">Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="2e9c0-244">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2e9c0-244">Minimum supported server</span></span><br/> | <span data-ttu-id="2e9c0-245">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2e9c0-245">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="2e9c0-246">Namespace</span><span class="sxs-lookup"><span data-stu-id="2e9c0-246">Namespace</span></span><br/>                | <span data-ttu-id="2e9c0-247">Root \\ CIMV2 \\ Sicherheit ( \\ microsoftvolumeencryption)</span><span class="sxs-lookup"><span data-stu-id="2e9c0-247">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="2e9c0-248">MOF</span><span class="sxs-lookup"><span data-stu-id="2e9c0-248">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2e9c0-249"><dt>Win32 \_ verschlüsseltablevolume. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="2e9c0-249"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2e9c0-250">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2e9c0-250">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2e9c0-251">**Win32- \_ verschlüsseltablevolume**</span><span class="sxs-lookup"><span data-stu-id="2e9c0-251">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> <dt>

[<span data-ttu-id="2e9c0-252">**Win32- \_ TPM**</span><span class="sxs-lookup"><span data-stu-id="2e9c0-252">**Win32\_Tpm**</span></span>](win32-tpm.md)
</dt> </dl>

 

 
