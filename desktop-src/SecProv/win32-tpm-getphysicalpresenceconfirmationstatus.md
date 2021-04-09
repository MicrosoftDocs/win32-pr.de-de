---
description: Gibt an, ob für einen bestimmten physischen Anwesenheits Vorgang eine Bestätigung von einem physisch vorhandenen Benutzer erforderlich ist.
ms.assetid: 1CE558B7-EB6F-42CB-B52B-2A0101E90BD5
title: 'Win32_Tpm:: getphysicalpresenceconfirmationstatus-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.GetPhysicalPresenceConfirmationStatus
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: 61dc2798973a82cfc75c803f2bf8307c8a43b3c5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960122"
---
# <a name="win32_tpmgetphysicalpresenceconfirmationstatus-method"></a><span data-ttu-id="7fabb-103">Win32 \_ TPM:: getphysicalpresenceconfirmationstatus-Methode</span><span class="sxs-lookup"><span data-stu-id="7fabb-103">Win32\_Tpm::GetPhysicalPresenceConfirmationStatus method</span></span>

<span data-ttu-id="7fabb-104">Gibt an, ob für einen bestimmten physischen Anwesenheits Vorgang eine Bestätigung von einem physisch vorhandenen Benutzer erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="7fabb-104">Indicates if confirmation from a physically present user is required for a given physical presence operation.</span></span>

<span data-ttu-id="7fabb-105">Diese Methode ist nur für lokale Administratoren zugänglich.</span><span class="sxs-lookup"><span data-stu-id="7fabb-105">This method is only accessible by local administrators.</span></span>

## <a name="syntax"></a><span data-ttu-id="7fabb-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="7fabb-106">Syntax</span></span>


```C++
uint32 GetPhysicalPresenceConfirmationStatus(
  [in]  uint32 Operation,
  [out] uint32 ConfirmationStatus
);
```



## <a name="parameters"></a><span data-ttu-id="7fabb-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="7fabb-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7fabb-108">*Vorgang* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7fabb-108">*Operation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7fabb-109">Ein ganzzahliger Wert, der den angeforderten TPM-Vorgang angibt, der physisch vorhanden sein muss.</span><span class="sxs-lookup"><span data-stu-id="7fabb-109">An integer value that specifies the requested TPM operation that requires physical presence.</span></span> <span data-ttu-id="7fabb-110">Anbieterspezifische Befehle werden ebenfalls unterstützt.</span><span class="sxs-lookup"><span data-stu-id="7fabb-110">Vendor specific commands are supported as well.</span></span>

<span data-ttu-id="7fabb-111">Der *Vorgangs* Parameter kann aus den folgenden Werten bestehen.</span><span class="sxs-lookup"><span data-stu-id="7fabb-111">The *Operation* parameter may consist of the following values.</span></span>



| <span data-ttu-id="7fabb-112">Wert</span><span class="sxs-lookup"><span data-stu-id="7fabb-112">Value</span></span>                                                                                                                               | <span data-ttu-id="7fabb-113">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="7fabb-113">Meaning</span></span>                                                  |
|-------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <span data-ttu-id="7fabb-114"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="7fabb-114"><dt>1</dt></span></span> </dl>                                                        | <span data-ttu-id="7fabb-115">Aktivieren</span><span class="sxs-lookup"><span data-stu-id="7fabb-115">Enable</span></span><br/>                                        |
| <dl> <span data-ttu-id="7fabb-116"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="7fabb-116"><dt>2</dt></span></span> </dl>                                                        | <span data-ttu-id="7fabb-117">Deaktivieren</span><span class="sxs-lookup"><span data-stu-id="7fabb-117">Disable</span></span><br/>                                       |
| <dl> <span data-ttu-id="7fabb-118"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="7fabb-118"><dt>3</dt></span></span> </dl>                                                        | <span data-ttu-id="7fabb-119">Aktivieren</span><span class="sxs-lookup"><span data-stu-id="7fabb-119">Activate</span></span><br/>                                      |
| <dl> <span data-ttu-id="7fabb-120"><dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="7fabb-120"><dt>4</dt></span></span> </dl>                                                        | <span data-ttu-id="7fabb-121">Deaktivieren</span><span class="sxs-lookup"><span data-stu-id="7fabb-121">Deactivate</span></span><br/>                                    |
| <dl> <span data-ttu-id="7fabb-122"><dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="7fabb-122"><dt>5</dt></span></span> </dl>                                                        | <span data-ttu-id="7fabb-123">Clear</span><span class="sxs-lookup"><span data-stu-id="7fabb-123">Clear</span></span><br/>                                         |
| <dl> <span data-ttu-id="7fabb-124"><dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="7fabb-124"><dt>6</dt></span></span> </dl>                                                        | <span data-ttu-id="7fabb-125">Aktivieren und aktivieren</span><span class="sxs-lookup"><span data-stu-id="7fabb-125">Enable + Activate</span></span><br/>                             |
| <dl> <span data-ttu-id="7fabb-126"><dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="7fabb-126"><dt>7</dt></span></span> </dl>                                                        | <span data-ttu-id="7fabb-127">Deaktivieren und deaktivieren</span><span class="sxs-lookup"><span data-stu-id="7fabb-127">Deactivate + Disable</span></span><br/>                          |
| <dl> <span data-ttu-id="7fabb-128"><dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="7fabb-128"><dt>8</dt></span></span> </dl>                                                        | <span data-ttu-id="7fabb-129">"Seetownerinstall" \_ true</span><span class="sxs-lookup"><span data-stu-id="7fabb-129">SetOwnerInstall\_True</span></span><br/>                         |
| <dl> <span data-ttu-id="7fabb-130"><dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="7fabb-130"><dt>9</dt></span></span> </dl>                                                        | <span data-ttu-id="7fabb-131">"Seetownerinstall \_ false"</span><span class="sxs-lookup"><span data-stu-id="7fabb-131">SetOwnerInstall\_False</span></span><br/>                        |
| <dl> <span data-ttu-id="7fabb-132"><dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="7fabb-132"><dt>10</dt></span></span> </dl>                                                       | <span data-ttu-id="7fabb-133">Aktivieren + aktivieren + seetownerinstall \_ true</span><span class="sxs-lookup"><span data-stu-id="7fabb-133">Enable + Activate + SetOwnerInstall\_True</span></span><br/>     |
| <dl> <span data-ttu-id="7fabb-134"><dt>11</dt></span><span class="sxs-lookup"><span data-stu-id="7fabb-134"><dt>11</dt></span></span> </dl>                                                       | <span data-ttu-id="7fabb-135">"Seetownerinstall \_ false + deaktivieren + deaktivieren"</span><span class="sxs-lookup"><span data-stu-id="7fabb-135">SetOwnerInstall\_False + Deactivate + Disable</span></span><br/> |
| <dl> <span data-ttu-id="7fabb-136"><dt></dt><dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="7fabb-136"><dt></dt> <dt>12</dt></span></span> </dl> | <span data-ttu-id="7fabb-137">Verzögerte physische presenceunownedfieldupgrade</span><span class="sxs-lookup"><span data-stu-id="7fabb-137">Deferred Physical PresenceunownedFieldUpgrade</span></span><br/> |
| <dl> <span data-ttu-id="7fabb-138"><dt></dt><dt>14</dt></span><span class="sxs-lookup"><span data-stu-id="7fabb-138"><dt></dt> <dt>14</dt></span></span> </dl> | <span data-ttu-id="7fabb-139">Löschen + aktivieren + aktivieren</span><span class="sxs-lookup"><span data-stu-id="7fabb-139">Clear + Enable + Activate</span></span><br/>                     |
| <dl> <span data-ttu-id="7fabb-140"><dt>15</dt></span><span class="sxs-lookup"><span data-stu-id="7fabb-140"><dt>15</dt></span></span> </dl>                                                       | <span data-ttu-id="7fabb-141">Setnoppiprovision \_ false</span><span class="sxs-lookup"><span data-stu-id="7fabb-141">SetNoPPIProvision\_False</span></span><br/>                      |
| <dl> <span data-ttu-id="7fabb-142"><dt>16</dt></span><span class="sxs-lookup"><span data-stu-id="7fabb-142"><dt>16</dt></span></span> </dl>                                                       | <span data-ttu-id="7fabb-143">Setnoppiprovision \_ true</span><span class="sxs-lookup"><span data-stu-id="7fabb-143">SetNoPPIProvision\_True</span></span><br/>                       |
| <dl> <span data-ttu-id="7fabb-144"><dt>17</dt></span><span class="sxs-lookup"><span data-stu-id="7fabb-144"><dt>17</dt></span></span> </dl>                                                       | <span data-ttu-id="7fabb-145">Setnoppiclear \_ false</span><span class="sxs-lookup"><span data-stu-id="7fabb-145">SetNoPPIClear\_False</span></span><br/>                          |
| <dl> <span data-ttu-id="7fabb-146"><dt>Jahren</dt></span><span class="sxs-lookup"><span data-stu-id="7fabb-146"><dt>18</dt></span></span> </dl>                                                       | <span data-ttu-id="7fabb-147">Setnoppiclear \_ true</span><span class="sxs-lookup"><span data-stu-id="7fabb-147">SetNoPPIClear\_True</span></span><br/>                           |
| <dl> <span data-ttu-id="7fabb-148"><dt>19</dt></span><span class="sxs-lookup"><span data-stu-id="7fabb-148"><dt>19</dt></span></span> </dl>                                                       | <span data-ttu-id="7fabb-149">Setnoppimaintenance \_ false</span><span class="sxs-lookup"><span data-stu-id="7fabb-149">SetNoPPIMaintenance\_False</span></span><br/>                    |
| <dl> <span data-ttu-id="7fabb-150"><dt>20</dt></span><span class="sxs-lookup"><span data-stu-id="7fabb-150"><dt>20</dt></span></span> </dl>                                                       | <span data-ttu-id="7fabb-151">Setnoppimaintenance \_ true</span><span class="sxs-lookup"><span data-stu-id="7fabb-151">SetNoPPIMaintenance\_True</span></span><br/>                     |
| <dl> <span data-ttu-id="7fabb-152"><dt>21</dt></span><span class="sxs-lookup"><span data-stu-id="7fabb-152"><dt>21</dt></span></span> </dl>                                                       | <span data-ttu-id="7fabb-153">Aktivieren + aktivieren + löschen</span><span class="sxs-lookup"><span data-stu-id="7fabb-153">Enable + Activate + Clear</span></span><br/>                     |
| <dl> <span data-ttu-id="7fabb-154"><dt>22</dt></span><span class="sxs-lookup"><span data-stu-id="7fabb-154"><dt>22</dt></span></span> </dl>                                                       | <span data-ttu-id="7fabb-155">Aktivieren + aktivieren + deaktivieren + aktivieren + aktivieren</span><span class="sxs-lookup"><span data-stu-id="7fabb-155">Enable + Activate + Clear + Enable + Activate</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="7fabb-156">*Confirmationstatus* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="7fabb-156">*ConfirmationStatus* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7fabb-157">Gibt den Bestätigungs Status für den physischen Anwesenheits Befehl zurück.</span><span class="sxs-lookup"><span data-stu-id="7fabb-157">Returns the confirmation status for physical presence command.</span></span>

<span data-ttu-id="7fabb-158">Der *confirmationstatus* -Parameter kann aus den folgenden Werten bestehen.</span><span class="sxs-lookup"><span data-stu-id="7fabb-158">The *ConfirmationStatus* parameter may consist of the following values.</span></span>



| <span data-ttu-id="7fabb-159">Wert</span><span class="sxs-lookup"><span data-stu-id="7fabb-159">Value</span></span>                                                                        | <span data-ttu-id="7fabb-160">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="7fabb-160">Meaning</span></span>                                                                |
|------------------------------------------------------------------------------|------------------------------------------------------------------------|
| <dl> <span data-ttu-id="7fabb-161"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="7fabb-161"><dt>0</dt></span></span> </dl> | <span data-ttu-id="7fabb-162">Nicht implementiert</span><span class="sxs-lookup"><span data-stu-id="7fabb-162">Not implemented</span></span><br/>                                             |
| <dl> <span data-ttu-id="7fabb-163"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="7fabb-163"><dt>1</dt></span></span> </dl> | <span data-ttu-id="7fabb-164">Nur BIOS.</span><span class="sxs-lookup"><span data-stu-id="7fabb-164">BIOS only.</span></span><br/>                                                  |
| <dl> <span data-ttu-id="7fabb-165"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="7fabb-165"><dt>2</dt></span></span> </dl> | <span data-ttu-id="7fabb-166">Blockiert für das Betriebssystem durch die BIOS-Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="7fabb-166">Blocked for the operating system by the BIOS configuration.</span></span><br/> |
| <dl> <span data-ttu-id="7fabb-167"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="7fabb-167"><dt>3</dt></span></span> </dl> | <span data-ttu-id="7fabb-168">Der zulässige und physisch vorhandene Benutzer ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="7fabb-168">Allowed and physically present user required.</span></span><br/>               |
| <dl> <span data-ttu-id="7fabb-169"><dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="7fabb-169"><dt>4</dt></span></span> </dl> | <span data-ttu-id="7fabb-170">Zulässige und physisch vorhandene Benutzer nicht erforderlich</span><span class="sxs-lookup"><span data-stu-id="7fabb-170">Allowed and physically present user not required</span></span><br/>            |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7fabb-171">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7fabb-171">Return value</span></span>

<span data-ttu-id="7fabb-172">Alle TPM-Fehler sowie Fehler, die für die [TPM-Basisdienste](../tbs/tbs-return-codes.md) spezifisch sind, können zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="7fabb-172">All TPM errors as well as errors specific to [TPM Base Services](../tbs/tbs-return-codes.md) can be returned.</span></span>

<span data-ttu-id="7fabb-173">Allgemeine Rückgabecodes sind unten aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="7fabb-173">Common return codes are listed below.</span></span>



| <span data-ttu-id="7fabb-174">Rückgabecode/-wert</span><span class="sxs-lookup"><span data-stu-id="7fabb-174">Return code/value</span></span>                                                                                                                                 | <span data-ttu-id="7fabb-175">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7fabb-175">Description</span></span>                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="7fabb-176"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="7fabb-176"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="7fabb-177">Die Methode war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="7fabb-177">The method was successful.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="7fabb-178">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7fabb-178">Remarks</span></span>

<span data-ttu-id="7fabb-179">Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen.</span><span class="sxs-lookup"><span data-stu-id="7fabb-179">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="7fabb-180">MOF-Dateien werden nicht als Teil des Windows SDK installiert.</span><span class="sxs-lookup"><span data-stu-id="7fabb-180">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="7fabb-181">Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="7fabb-181">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="7fabb-182">Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="7fabb-182">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="7fabb-183">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7fabb-183">Requirements</span></span>



| <span data-ttu-id="7fabb-184">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7fabb-184">Requirement</span></span> | <span data-ttu-id="7fabb-185">Wert</span><span class="sxs-lookup"><span data-stu-id="7fabb-185">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="7fabb-186">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7fabb-186">Minimum supported client</span></span><br/> | <span data-ttu-id="7fabb-187">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7fabb-187">Windows 8 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="7fabb-188">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7fabb-188">Minimum supported server</span></span><br/> | <span data-ttu-id="7fabb-189">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7fabb-189">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="7fabb-190">Namespace</span><span class="sxs-lookup"><span data-stu-id="7fabb-190">Namespace</span></span><br/>                | <span data-ttu-id="7fabb-191">\\\\.\\ root \\ CIMV2 \\ Security- \\ mikrosofttpm</span><span class="sxs-lookup"><span data-stu-id="7fabb-191">\\\\.\\root\\CIMV2\\Security\\MicrosoftTpm</span></span><br/>                                     |
| <span data-ttu-id="7fabb-192">MOF</span><span class="sxs-lookup"><span data-stu-id="7fabb-192">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7fabb-193"><dt>Win32- \_ TPM. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="7fabb-193"><dt>Win32\_tpm.mof</dt></span></span> </dl> |
| <span data-ttu-id="7fabb-194">DLL</span><span class="sxs-lookup"><span data-stu-id="7fabb-194">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7fabb-195"><dt>Win32- \_tpm.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7fabb-195"><dt>Win32\_tpm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7fabb-196">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7fabb-196">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7fabb-197">**Win32- \_ TPM**</span><span class="sxs-lookup"><span data-stu-id="7fabb-197">**Win32\_Tpm**</span></span>](win32-tpm.md)
</dt> </dl>

 

 
