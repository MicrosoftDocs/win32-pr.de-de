---
description: Gibt die physische Anwesenheits Operation für das TPM zurück. Verwenden Sie die setphysicalpresencerequest-Methode, um einen Vorgang anzufordern.
ms.assetid: c50378ae-b465-4c82-beb9-8ecb7939dae2
title: Getphysicalpresencerequest-Methode der Win32_Tpm-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.GetPhysicalPresenceRequest
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: 8d631aabfc1e2df15aa4182b8332091fe503f539
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106353861"
---
# <a name="getphysicalpresencerequest-method-of-the-win32_tpm-class"></a><span data-ttu-id="acd9d-104">Getphysicalpresencerequest-Methode der Win32 \_ TPM-Klasse</span><span class="sxs-lookup"><span data-stu-id="acd9d-104">GetPhysicalPresenceRequest method of the Win32\_Tpm class</span></span>

<span data-ttu-id="acd9d-105">Die **getphysicalpresencerequest** -Methode der [**Win32 \_ TPM**](win32-tpm.md) -Klasse gibt den ausstehenden TPM-Anwesenheits Vorgang zurück.</span><span class="sxs-lookup"><span data-stu-id="acd9d-105">The **GetPhysicalPresenceRequest** method of the [**Win32\_Tpm**](win32-tpm.md) class returns the pending TPM physical presence operation.</span></span> <span data-ttu-id="acd9d-106">Verwenden Sie die [**setphysicalpresencerequest**](setphysicalpresencerequest-win32-tpm.md) -Methode, um einen Vorgang anzufordern.</span><span class="sxs-lookup"><span data-stu-id="acd9d-106">Use the [**SetPhysicalPresenceRequest**](setphysicalpresencerequest-win32-tpm.md) method to request an operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="acd9d-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="acd9d-107">Syntax</span></span>


```mof
uint32 GetPhysicalPresenceRequest(
  [out] uint32 Request
);
```



## <a name="parameters"></a><span data-ttu-id="acd9d-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="acd9d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="acd9d-109">*Anforderung* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="acd9d-109">*Request* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="acd9d-110">Typ: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="acd9d-110">Type: **uint32**</span></span>

<span data-ttu-id="acd9d-111">Ein-Wert, der den ausstehenden TPM-Anwesenheits Vorgang angibt.</span><span class="sxs-lookup"><span data-stu-id="acd9d-111">A value that specifies the pending TPM physical presence operation.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="acd9d-112">Wert</span><span class="sxs-lookup"><span data-stu-id="acd9d-112">Value</span></span></th>
<th><span data-ttu-id="acd9d-113">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="acd9d-113">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><dl> <span data-ttu-id="acd9d-114"><dt>1,0</dt> </span><span class="sxs-lookup"><span data-stu-id="acd9d-114"><dt>0</dt> </span></span></dl></td>
<td><span data-ttu-id="acd9d-115">Keine Anforderung.</span><span class="sxs-lookup"><span data-stu-id="acd9d-115">No request.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="acd9d-116"><dt>1</dt> </span><span class="sxs-lookup"><span data-stu-id="acd9d-116"><dt>1</dt> </span></span></dl></td>
<td><span data-ttu-id="acd9d-117">Aktivieren Sie das TPM.</span><span class="sxs-lookup"><span data-stu-id="acd9d-117">Enable the TPM.</span></span><br/> <span data-ttu-id="acd9d-118">Dieser Vorgang wird von Vorgang 2 rückgängig gemacht.</span><span class="sxs-lookup"><span data-stu-id="acd9d-118">This operation is reversed by operation 2.</span></span> <br/> <span data-ttu-id="acd9d-119">Weitere Informationen finden Sie in den folgenden verwandten Methoden, die keine physische Präsenz beinhalten:</span><span class="sxs-lookup"><span data-stu-id="acd9d-119">For more information, see these related methods that do not involve physical presence:</span></span>
<ul>
<li><span data-ttu-id="acd9d-120"><a href="enable-win32-tpm.md"><strong>Aktivieren</strong></a></span><span class="sxs-lookup"><span data-stu-id="acd9d-120"><a href="enable-win32-tpm.md"><strong>Enable</strong></a></span></span></li>
<li><span data-ttu-id="acd9d-121"><a href="isenabled-win32-tpm.md"><strong>isEnabled</strong></a></span><span class="sxs-lookup"><span data-stu-id="acd9d-121"><a href="isenabled-win32-tpm.md"><strong>IsEnabled</strong></a></span></span></li>
</ul>
<br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="acd9d-122"><dt>2</dt> </span><span class="sxs-lookup"><span data-stu-id="acd9d-122"><dt>2</dt> </span></span></dl></td>
<td><span data-ttu-id="acd9d-123">Deaktivieren Sie das TPM.</span><span class="sxs-lookup"><span data-stu-id="acd9d-123">Disable the TPM.</span></span><br/> <span data-ttu-id="acd9d-124">Dieser Vorgang wird durch Vorgang 1 rückgängig gemacht.</span><span class="sxs-lookup"><span data-stu-id="acd9d-124">This operation is reversed by operation 1.</span></span> <br/> <span data-ttu-id="acd9d-125">Weitere Informationen finden Sie in dieser verwandten Methode, die keine physische Präsenz umfasst: <a href="disable-win32-tpm.md"><strong>Deaktivieren</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="acd9d-125">For more information, see this related method that does not involve physical presence: <a href="disable-win32-tpm.md"><strong>Disable</strong></a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="acd9d-126"><dt>€</dt> </span><span class="sxs-lookup"><span data-stu-id="acd9d-126"><dt>3</dt> </span></span></dl></td>
<td><span data-ttu-id="acd9d-127">Aktivieren Sie das TPM.</span><span class="sxs-lookup"><span data-stu-id="acd9d-127">Activate the TPM.</span></span><br/> <span data-ttu-id="acd9d-128">Dieser Vorgang wird von Vorgang 4 rückgängig gemacht.</span><span class="sxs-lookup"><span data-stu-id="acd9d-128">This operation is reversed by operation 4.</span></span><br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="acd9d-129"><dt>0:</dt> </span><span class="sxs-lookup"><span data-stu-id="acd9d-129"><dt>4</dt> </span></span></dl></td>
<td><span data-ttu-id="acd9d-130">Deaktivieren Sie das TPM.</span><span class="sxs-lookup"><span data-stu-id="acd9d-130">Deactivate the TPM.</span></span><br/> <span data-ttu-id="acd9d-131">Dieser Vorgang wird von Vorgang 3 rückgängig gemacht.</span><span class="sxs-lookup"><span data-stu-id="acd9d-131">This operation is reversed by operation 3.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="acd9d-132"><dt>5@@</dt> </span><span class="sxs-lookup"><span data-stu-id="acd9d-132"><dt>5</dt> </span></span></dl></td>
<td><span data-ttu-id="acd9d-133">Löschen Sie das TPM.</span><span class="sxs-lookup"><span data-stu-id="acd9d-133">Clear the TPM.</span></span><br/> <span data-ttu-id="acd9d-134">Dieser Vorgang kann nicht rückgängig gemacht werden.</span><span class="sxs-lookup"><span data-stu-id="acd9d-134">This operation cannot be reversed.</span></span><br/> <span data-ttu-id="acd9d-135">Weitere Informationen finden Sie in der zugehörigen Methode, die keine physische Präsenz umfasst: <a href="clear-win32-tpm.md"><strong>Clear</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="acd9d-135">For more information, see this related method that does not involve physical presence: <a href="clear-win32-tpm.md"><strong>Clear</strong></a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="acd9d-136"><dt>6</dt> </span><span class="sxs-lookup"><span data-stu-id="acd9d-136"><dt>6</dt> </span></span></dl></td>
<td><span data-ttu-id="acd9d-137">Aktivieren und aktivieren Sie das TPM.</span><span class="sxs-lookup"><span data-stu-id="acd9d-137">Enable and activate the TPM.</span></span> <br/> <span data-ttu-id="acd9d-138">Dieser Vorgang wird von Vorgang 7 rückgängig gemacht.</span><span class="sxs-lookup"><span data-stu-id="acd9d-138">This operation is reversed by operation 7.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="acd9d-139"><dt>19.00</dt> </span><span class="sxs-lookup"><span data-stu-id="acd9d-139"><dt>7</dt> </span></span></dl></td>
<td><span data-ttu-id="acd9d-140">Deaktivieren und deaktivieren Sie das TPM.</span><span class="sxs-lookup"><span data-stu-id="acd9d-140">Deactivate and disable the TPM.</span></span><br/> <span data-ttu-id="acd9d-141">Dieser Vorgang wird von Vorgang 6 rückgängig gemacht.</span><span class="sxs-lookup"><span data-stu-id="acd9d-141">This operation is reversed by operation 6.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="acd9d-142"><dt>88</dt> </span><span class="sxs-lookup"><span data-stu-id="acd9d-142"><dt>8</dt> </span></span></dl></td>
<td><span data-ttu-id="acd9d-143">Ermöglicht die Installation eines TPM-Besitzers.</span><span class="sxs-lookup"><span data-stu-id="acd9d-143">Allow the installation of a TPM owner.</span></span> <br/> <span data-ttu-id="acd9d-144">Dieser Vorgang wird von Vorgang 9 rückgängig gemacht.</span><span class="sxs-lookup"><span data-stu-id="acd9d-144">This operation is reversed by operation 9.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="acd9d-145"><dt>21.00</dt> </span><span class="sxs-lookup"><span data-stu-id="acd9d-145"><dt>9</dt> </span></span></dl></td>
<td><span data-ttu-id="acd9d-146">Verhindern Sie die Installation eines TPM-Besitzers.</span><span class="sxs-lookup"><span data-stu-id="acd9d-146">Prevent the installation of a TPM owner.</span></span><br/> <span data-ttu-id="acd9d-147">Dieser Vorgang wird von Vorgang 8 rückgängig gemacht.</span><span class="sxs-lookup"><span data-stu-id="acd9d-147">This operation is reversed by operation 8.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="acd9d-148"><dt>€</dt> </span><span class="sxs-lookup"><span data-stu-id="acd9d-148"><dt>10</dt> </span></span></dl></td>
<td><span data-ttu-id="acd9d-149">Aktivieren, aktivieren und zulassen der Installation eines TPM-Besitzers.</span><span class="sxs-lookup"><span data-stu-id="acd9d-149">Enable, activate, and allow the installation of a TPM owner.</span></span><br/> <span data-ttu-id="acd9d-150">Dieser Vorgang wird von Vorgang 11 rückgängig gemacht.</span><span class="sxs-lookup"><span data-stu-id="acd9d-150">This operation is reversed by operation 11.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="acd9d-151"><dt>11:</dt> </span><span class="sxs-lookup"><span data-stu-id="acd9d-151"><dt>11</dt> </span></span></dl></td>
<td><span data-ttu-id="acd9d-152">Deaktivieren, deaktivieren und verhindern der Installation eines TPM-Besitzers.</span><span class="sxs-lookup"><span data-stu-id="acd9d-152">Deactivate, disable, and prevent the installation of a TPM owner.</span></span><br/> <span data-ttu-id="acd9d-153">Dieser Vorgang wird von Vorgang 10 rückgängig gemacht.</span><span class="sxs-lookup"><span data-stu-id="acd9d-153">This operation is reversed by operation 10.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span></span><dl> <span data-ttu-id="acd9d-154"><dt><strong></strong></dt><dt>12</dt> </span><span class="sxs-lookup"><span data-stu-id="acd9d-154"><dt><strong></strong></dt> <dt>12</dt> </span></span></dl></td>
<td><span data-ttu-id="acd9d-155">Verzögerte physische presenceunownedfieldupgrade</span><span class="sxs-lookup"><span data-stu-id="acd9d-155">Deferred Physical PresenceunownedFieldUpgrade</span></span><br/> <span data-ttu-id="acd9d-156">Die Einstellung für die physische Anwesenheit wurde aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="acd9d-156">Physical presence setting has been updated.</span></span><br/> <span data-ttu-id="acd9d-157"><strong>Windows 7, Windows Server 2008 R2, Windows Vista und Windows Server 2008:</strong> Dieser Wert wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="acd9d-157"><strong>Windows 7, Windows Server 2008 R2, Windows Vista and Windows Server 2008:</strong> This value is not supported.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="acd9d-158"><dt>14</dt> </span><span class="sxs-lookup"><span data-stu-id="acd9d-158"><dt>14</dt> </span></span></dl></td>
<td><span data-ttu-id="acd9d-159">Löschen, aktivieren und aktivieren Sie das TPM.</span><span class="sxs-lookup"><span data-stu-id="acd9d-159">Clear, enable, and activate the TPM.</span></span><br/> <span data-ttu-id="acd9d-160">Dieser Vorgang kann nicht rückgängig gemacht werden.</span><span class="sxs-lookup"><span data-stu-id="acd9d-160">This operation cannot be reversed.</span></span><br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="acd9d-161"><dt>17.15</dt> </span><span class="sxs-lookup"><span data-stu-id="acd9d-161"><dt>15</dt> </span></span></dl></td>
<td><span data-ttu-id="acd9d-162">SetNoPPIProvision_False</span><span class="sxs-lookup"><span data-stu-id="acd9d-162">SetNoPPIProvision_False</span></span><br/> <span data-ttu-id="acd9d-163">Legt die Bereitstellung fest, die physisch vorhanden sein muss, um das TPM festzulegen.</span><span class="sxs-lookup"><span data-stu-id="acd9d-163">Sets the provision that you must be physically presence to set the TPM.</span></span><br/> <span data-ttu-id="acd9d-164">Dieser Vorgang wird von Vorgang 16 rückgängig gemacht.</span><span class="sxs-lookup"><span data-stu-id="acd9d-164">This operation is reversed by operation 16.</span></span><br/> <span data-ttu-id="acd9d-165"><strong>Windows 7, Windows Server 2008 R2, Windows Vista und Windows Server 2008:</strong> Dieser Wert wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="acd9d-165"><strong>Windows 7, Windows Server 2008 R2, Windows Vista and Windows Server 2008:</strong> This value is not supported.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="acd9d-166"><dt>Uhr</dt> </span><span class="sxs-lookup"><span data-stu-id="acd9d-166"><dt>16</dt> </span></span></dl></td>
<td><span data-ttu-id="acd9d-167">SetNoPPIProvision_True</span><span class="sxs-lookup"><span data-stu-id="acd9d-167">SetNoPPIProvision_True</span></span><br/> <span data-ttu-id="acd9d-168">Legt fest, dass die Bereitstellung nicht physisch vorhanden sein muss, um das TPM festzulegen.</span><span class="sxs-lookup"><span data-stu-id="acd9d-168">Sets the provision that you don't need to be physically presence to set the TPM.</span></span><br/> <span data-ttu-id="acd9d-169">Dieser Vorgang wird von Vorgang 15 rückgängig gemacht.</span><span class="sxs-lookup"><span data-stu-id="acd9d-169">This operation is reversed by operation 15.</span></span><br/> <span data-ttu-id="acd9d-170"><strong>Windows 7, Windows Server 2008 R2, Windows Vista und Windows Server 2008:</strong> Dieser Wert wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="acd9d-170"><strong>Windows 7, Windows Server 2008 R2, Windows Vista and Windows Server 2008:</strong> This value is not supported.</span></span><br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="acd9d-171"><dt>Uhr</dt> </span><span class="sxs-lookup"><span data-stu-id="acd9d-171"><dt>17</dt> </span></span></dl></td>
<td><span data-ttu-id="acd9d-172">SetNoPPIClear_False</span><span class="sxs-lookup"><span data-stu-id="acd9d-172">SetNoPPIClear_False</span></span><br/> <span data-ttu-id="acd9d-173">Hiermit wird die Bereitstellung festgelegt, die physisch vorhanden sein muss, um das TPM zu löschen.</span><span class="sxs-lookup"><span data-stu-id="acd9d-173">Sets the provision that you must be physically presence to clear the TPM.</span></span><br/> <span data-ttu-id="acd9d-174">Dieser Vorgang wird durch den Vorgang 18 rückgängig gemacht.</span><span class="sxs-lookup"><span data-stu-id="acd9d-174">This operation is reversed by operation 18.</span></span><br/> <span data-ttu-id="acd9d-175"><strong>Windows 7, Windows Server 2008 R2, Windows Vista und Windows Server 2008:</strong> Dieser Wert wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="acd9d-175"><strong>Windows 7, Windows Server 2008 R2, Windows Vista and Windows Server 2008:</strong> This value is not supported.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="acd9d-176"><dt>Jahren</dt> </span><span class="sxs-lookup"><span data-stu-id="acd9d-176"><dt>18</dt> </span></span></dl></td>
<td><span data-ttu-id="acd9d-177">SetNoPPIClear_True</span><span class="sxs-lookup"><span data-stu-id="acd9d-177">SetNoPPIClear_True</span></span><br/> <span data-ttu-id="acd9d-178">Hiermit wird die Bereitstellung festgelegt, die nicht physisch vorhanden sein muss, um das TPM zu löschen.</span><span class="sxs-lookup"><span data-stu-id="acd9d-178">Sets the provision that you don't need to be physically presence to clear the TPM.</span></span><br/> <span data-ttu-id="acd9d-179">Dieser Vorgang wird von Vorgang 17 rückgängig gemacht.</span><span class="sxs-lookup"><span data-stu-id="acd9d-179">This operation is reversed by operation 17.</span></span><br/> <span data-ttu-id="acd9d-180"><strong>Windows 7, Windows Server 2008 R2, Windows Vista und Windows Server 2008:</strong> Dieser Wert wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="acd9d-180"><strong>Windows 7, Windows Server 2008 R2, Windows Vista and Windows Server 2008:</strong> This value is not supported.</span></span><br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="acd9d-181"><dt>19.07.2016</dt> </span><span class="sxs-lookup"><span data-stu-id="acd9d-181"><dt>19</dt> </span></span></dl></td>
<td><span data-ttu-id="acd9d-182">SetNoPPIMaintenance_False</span><span class="sxs-lookup"><span data-stu-id="acd9d-182">SetNoPPIMaintenance_False</span></span><br/> <span data-ttu-id="acd9d-183">Legt fest, dass Sie physisch vorhanden sein müssen, um das TPM beizubehalten.</span><span class="sxs-lookup"><span data-stu-id="acd9d-183">Sets the provision that you must be physically presence to maintain the TPM.</span></span><br/> <span data-ttu-id="acd9d-184">Dieser Vorgang wird durch den Vorgang 20 rückgängig gemacht.</span><span class="sxs-lookup"><span data-stu-id="acd9d-184">This operation is reversed by operation 20.</span></span><br/> <span data-ttu-id="acd9d-185"><strong>Windows 7, Windows Server 2008 R2, Windows Vista und Windows Server 2008:</strong> Dieser Wert wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="acd9d-185"><strong>Windows 7, Windows Server 2008 R2, Windows Vista and Windows Server 2008:</strong> This value is not supported.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="acd9d-186"><dt>20</dt> </span><span class="sxs-lookup"><span data-stu-id="acd9d-186"><dt>20</dt> </span></span></dl></td>
<td><span data-ttu-id="acd9d-187">SetNoPPIMaintenance_True</span><span class="sxs-lookup"><span data-stu-id="acd9d-187">SetNoPPIMaintenance_True</span></span><br/> <span data-ttu-id="acd9d-188">Legt fest, dass Sie physisch vorhanden sein müssen, um das TPM beizubehalten.</span><span class="sxs-lookup"><span data-stu-id="acd9d-188">Sets the provision that you must be physically presence to maintain the TPM.</span></span><br/> <span data-ttu-id="acd9d-189">Dieser Vorgang wird durch den Vorgang 19 rückgängig gemacht.</span><span class="sxs-lookup"><span data-stu-id="acd9d-189">This operation is reversed by operation 19.</span></span><br/> <span data-ttu-id="acd9d-190"><strong>Windows 7, Windows Server 2008 R2, Windows Vista und Windows Server 2008:</strong> Dieser Wert wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="acd9d-190"><strong>Windows 7, Windows Server 2008 R2, Windows Vista and Windows Server 2008:</strong> This value is not supported.</span></span><br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="acd9d-191"><dt>21</dt> </span><span class="sxs-lookup"><span data-stu-id="acd9d-191"><dt>21</dt> </span></span></dl></td>
<td><span data-ttu-id="acd9d-192">Aktivieren + aktivieren + löschen</span><span class="sxs-lookup"><span data-stu-id="acd9d-192">Enable + Activate + Clear</span></span><br/> <span data-ttu-id="acd9d-193">Aktivieren, aktivieren und Löschen des TPM.</span><span class="sxs-lookup"><span data-stu-id="acd9d-193">Enable, activate, and clear the TPM.</span></span><br/> <span data-ttu-id="acd9d-194"><strong>Windows 7, Windows Server 2008 R2, Windows Vista und Windows Server 2008:</strong> Dieser Wert wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="acd9d-194"><strong>Windows 7, Windows Server 2008 R2, Windows Vista and Windows Server 2008:</strong> This value is not supported.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="acd9d-195"><dt>22.11.2016</dt> </span><span class="sxs-lookup"><span data-stu-id="acd9d-195"><dt>22</dt> </span></span></dl></td>
<td><span data-ttu-id="acd9d-196">Aktivieren + aktivieren + deaktivieren + aktivieren + aktivieren</span><span class="sxs-lookup"><span data-stu-id="acd9d-196">Enable + Activate + Clear + Enable + Activate</span></span><br/> <span data-ttu-id="acd9d-197">Aktivieren, aktivieren und löschen Sie das TPM, und aktivieren und aktivieren Sie dann das TPM.</span><span class="sxs-lookup"><span data-stu-id="acd9d-197">Enable, activate, and clear the TPM, and then enable and reactivate the TPM.</span></span><br/> <span data-ttu-id="acd9d-198"><strong>Windows 7, Windows Server 2008 R2, Windows Vista und Windows Server 2008:</strong> Dieser Wert wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="acd9d-198"><strong>Windows 7, Windows Server 2008 R2, Windows Vista and Windows Server 2008:</strong> This value is not supported.</span></span><br/></td>
</tr>
</tbody>
</table>



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="acd9d-199">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="acd9d-199">Return value</span></span>

<span data-ttu-id="acd9d-200">Typ: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="acd9d-200">Type: **uint32**</span></span>

<span data-ttu-id="acd9d-201">Alle TPM-Fehler sowie Fehler, die für die TPM-Basisdienste spezifisch sind, können zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="acd9d-201">All TPM errors as well as errors specific to TPM Base Services can be returned.</span></span>

<span data-ttu-id="acd9d-202">In der folgenden Tabelle sind die gemeinsamen Rückgabecodes aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="acd9d-202">The following table lists the common return codes.</span></span>



| <span data-ttu-id="acd9d-203">Rückgabecode/-wert</span><span class="sxs-lookup"><span data-stu-id="acd9d-203">Return code/value</span></span>                                                                                                                                                                      | <span data-ttu-id="acd9d-204">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="acd9d-204">Description</span></span>                                                                                      |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="acd9d-205"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="acd9d-205"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                      | <span data-ttu-id="acd9d-206">Die Methode war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="acd9d-206">The method was successful.</span></span><br/>                                                            |
| <dl> <span data-ttu-id="acd9d-207"><dt>**TPM \_ E- \_ ppi- \_ ACPI- \_ Fehler**</dt> <dt>2150171392 (0x80290300)</dt></span><span class="sxs-lookup"><span data-stu-id="acd9d-207"><dt>**TPM\_E\_PPI\_ACPI\_FAILURE**</dt> <dt>2150171392 (0x80290300)</dt></span></span> </dl> | <span data-ttu-id="acd9d-208">Ein Hardwarefehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="acd9d-208">A hardware failure occurred.</span></span> <span data-ttu-id="acd9d-209">Weitere Informationen hierzu erhalten Sie von Ihrem Computerhersteller.</span><span class="sxs-lookup"><span data-stu-id="acd9d-209">Consult your computer manufacturer for more information.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="acd9d-210">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="acd9d-210">Remarks</span></span>

<span data-ttu-id="acd9d-211">Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen.</span><span class="sxs-lookup"><span data-stu-id="acd9d-211">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="acd9d-212">MOF-Dateien werden nicht als Teil des Windows SDK installiert.</span><span class="sxs-lookup"><span data-stu-id="acd9d-212">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="acd9d-213">Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="acd9d-213">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="acd9d-214">Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="acd9d-214">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="acd9d-215">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="acd9d-215">Requirements</span></span>



| <span data-ttu-id="acd9d-216">Anforderung</span><span class="sxs-lookup"><span data-stu-id="acd9d-216">Requirement</span></span> | <span data-ttu-id="acd9d-217">Wert</span><span class="sxs-lookup"><span data-stu-id="acd9d-217">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="acd9d-218">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="acd9d-218">Minimum supported client</span></span><br/> | <span data-ttu-id="acd9d-219">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="acd9d-219">Windows Vista \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="acd9d-220">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="acd9d-220">Minimum supported server</span></span><br/> | <span data-ttu-id="acd9d-221">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="acd9d-221">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="acd9d-222">Namespace</span><span class="sxs-lookup"><span data-stu-id="acd9d-222">Namespace</span></span><br/>                | <span data-ttu-id="acd9d-223">Root \\ CIMV2 \\ Security- \\ mikrosofttpm</span><span class="sxs-lookup"><span data-stu-id="acd9d-223">Root\\CIMV2\\Security\\MicrosoftTpm</span></span><br/>                                            |
| <span data-ttu-id="acd9d-224">MOF</span><span class="sxs-lookup"><span data-stu-id="acd9d-224">MOF</span></span><br/>                      | <dl> <span data-ttu-id="acd9d-225"><dt>Win32- \_ TPM. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="acd9d-225"><dt>Win32\_tpm.mof</dt></span></span> </dl> |
| <span data-ttu-id="acd9d-226">DLL</span><span class="sxs-lookup"><span data-stu-id="acd9d-226">DLL</span></span><br/>                      | <dl> <span data-ttu-id="acd9d-227"><dt>Win32- \_tpm.dll</dt></span><span class="sxs-lookup"><span data-stu-id="acd9d-227"><dt>Win32\_tpm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="acd9d-228">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="acd9d-228">See also</span></span>

<dl> <dt>

[<span data-ttu-id="acd9d-229">**Win32- \_ TPM**</span><span class="sxs-lookup"><span data-stu-id="acd9d-229">**Win32\_Tpm**</span></span>](win32-tpm.md)
</dt> <dt>

[<span data-ttu-id="acd9d-230">**Klartext**</span><span class="sxs-lookup"><span data-stu-id="acd9d-230">**Clear**</span></span>](clear-win32-tpm.md)
</dt> <dt>

[<span data-ttu-id="acd9d-231">**Deaktivieren**</span><span class="sxs-lookup"><span data-stu-id="acd9d-231">**Disable**</span></span>](disable-win32-tpm.md)
</dt> <dt>

[<span data-ttu-id="acd9d-232">**Aktivieren**</span><span class="sxs-lookup"><span data-stu-id="acd9d-232">**Enable**</span></span>](enable-win32-tpm.md)
</dt> <dt>

[<span data-ttu-id="acd9d-233">**isEnabled**</span><span class="sxs-lookup"><span data-stu-id="acd9d-233">**IsEnabled**</span></span>](isenabled-win32-tpm.md)
</dt> <dt>

[<span data-ttu-id="acd9d-234">**Setphysicalpresencerequest**</span><span class="sxs-lookup"><span data-stu-id="acd9d-234">**SetPhysicalPresenceRequest**</span></span>](setphysicalpresencerequest-win32-tpm.md)
</dt> </dl>

 

 
