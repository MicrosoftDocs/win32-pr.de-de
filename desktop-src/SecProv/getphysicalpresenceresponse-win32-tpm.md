---
description: Gibt die Ergebnisse aus einem physischen TPM-Anwesenheits Vorgang zurück, der ausgeführt wurde.
ms.assetid: 28d76149-3905-45db-a41e-32fac1603582
title: Getphysicalpresenceresponse-Methode der Win32_Tpm-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.GetPhysicalPresenceResponse
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: 47dfad1491b398b035e40867d10d2d3e46327dd9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345032"
---
# <a name="getphysicalpresenceresponse-method-of-the-win32_tpm-class"></a><span data-ttu-id="98200-103">Getphysicalpresenceresponse-Methode der Win32 \_ TPM-Klasse</span><span class="sxs-lookup"><span data-stu-id="98200-103">GetPhysicalPresenceResponse method of the Win32\_Tpm class</span></span>

<span data-ttu-id="98200-104">Die **getphysicalpresenceresponse** -Methode der [**Win32- \_ TPM**](win32-tpm.md) -Klasse gibt die Ergebnisse aus einem physischen TPM-Anwesenheits Vorgang zurück, der ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="98200-104">The **GetPhysicalPresenceResponse** method of the [**Win32\_Tpm**](win32-tpm.md) class returns the results from a TPM physical presence operation that was performed.</span></span> <span data-ttu-id="98200-105">Verwenden Sie die [**setphysicalpresencerequest**](setphysicalpresencerequest-win32-tpm.md) -Methode, um einen Vorgang anzufordern.</span><span class="sxs-lookup"><span data-stu-id="98200-105">Use the [**SetPhysicalPresenceRequest**](setphysicalpresencerequest-win32-tpm.md) method to request an operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="98200-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="98200-106">Syntax</span></span>


```mof
uint32 GetPhysicalPresenceResponse(
  [out] uint32 Request,
  [out] uint32 Response
);
```



## <a name="parameters"></a><span data-ttu-id="98200-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="98200-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="98200-108">*Anforderung* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="98200-108">*Request* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="98200-109">Typ: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="98200-109">Type: **uint32**</span></span>

<span data-ttu-id="98200-110">Ein ganzzahliger Wert, der den durchgeführten TPM-Anwesenheits Vorgang angibt.</span><span class="sxs-lookup"><span data-stu-id="98200-110">An integer value that specifies the TPM physical presence operation that was performed.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="98200-111">Wert</span><span class="sxs-lookup"><span data-stu-id="98200-111">Value</span></span></th>
<th><span data-ttu-id="98200-112">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="98200-112">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><dl> <span data-ttu-id="98200-113"><dt>1,0</dt> </span><span class="sxs-lookup"><span data-stu-id="98200-113"><dt>0</dt> </span></span></dl></td>
<td><span data-ttu-id="98200-114">Keine Anforderung.</span><span class="sxs-lookup"><span data-stu-id="98200-114">No request.</span></span><br/> <span data-ttu-id="98200-115">Es wurde kein physischer Anwesenheits Vorgang ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="98200-115">No physical presence operation was performed.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="98200-116"><dt>1</dt> </span><span class="sxs-lookup"><span data-stu-id="98200-116"><dt>1</dt> </span></span></dl></td>
<td><span data-ttu-id="98200-117">Aktivieren Sie das TPM.</span><span class="sxs-lookup"><span data-stu-id="98200-117">Enable the TPM.</span></span><br/> <span data-ttu-id="98200-118">Dieser Vorgang wird von Vorgang 2 rückgängig gemacht.</span><span class="sxs-lookup"><span data-stu-id="98200-118">This operation is reversed by operation 2.</span></span> <br/> <span data-ttu-id="98200-119">Weitere Informationen finden Sie in den folgenden verwandten Methoden, die keine physische Präsenz beinhalten:</span><span class="sxs-lookup"><span data-stu-id="98200-119">For more information, see these related methods that do not involve physical presence:</span></span>
<ul>
<li><span data-ttu-id="98200-120"><a href="enable-win32-tpm.md"><strong>Aktivieren</strong></a></span><span class="sxs-lookup"><span data-stu-id="98200-120"><a href="enable-win32-tpm.md"><strong>Enable</strong></a></span></span></li>
<li><span data-ttu-id="98200-121"><a href="isenabled-win32-tpm.md"><strong>isEnabled</strong></a></span><span class="sxs-lookup"><span data-stu-id="98200-121"><a href="isenabled-win32-tpm.md"><strong>IsEnabled</strong></a></span></span></li>
</ul>
<br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="98200-122"><dt>2</dt> </span><span class="sxs-lookup"><span data-stu-id="98200-122"><dt>2</dt> </span></span></dl></td>
<td><span data-ttu-id="98200-123">Deaktivieren Sie das TPM.</span><span class="sxs-lookup"><span data-stu-id="98200-123">Disable the TPM.</span></span><br/> <span data-ttu-id="98200-124">Dieser Vorgang wird durch Vorgang 1 rückgängig gemacht.</span><span class="sxs-lookup"><span data-stu-id="98200-124">This operation is reversed by operation 1.</span></span> <br/> <span data-ttu-id="98200-125">Weitere Informationen finden Sie in dieser verwandten Methode, die keine physische Präsenz umfasst: <a href="disable-win32-tpm.md"><strong>Deaktivieren</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="98200-125">For more information, see this related method that does not involve physical presence: <a href="disable-win32-tpm.md"><strong>Disable</strong></a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="98200-126"><dt>€</dt> </span><span class="sxs-lookup"><span data-stu-id="98200-126"><dt>3</dt> </span></span></dl></td>
<td><span data-ttu-id="98200-127">Aktivieren Sie das TPM.</span><span class="sxs-lookup"><span data-stu-id="98200-127">Activate the TPM.</span></span><br/> <span data-ttu-id="98200-128">Dieser Vorgang wird von Vorgang 4 rückgängig gemacht.</span><span class="sxs-lookup"><span data-stu-id="98200-128">This operation is reversed by operation 4.</span></span><br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="98200-129"><dt>0:</dt> </span><span class="sxs-lookup"><span data-stu-id="98200-129"><dt>4</dt> </span></span></dl></td>
<td><span data-ttu-id="98200-130">Deaktivieren Sie das TPM.</span><span class="sxs-lookup"><span data-stu-id="98200-130">Deactivate the TPM.</span></span><br/> <span data-ttu-id="98200-131">Dieser Vorgang wird von Vorgang 3 rückgängig gemacht.</span><span class="sxs-lookup"><span data-stu-id="98200-131">This operation is reversed by operation 3.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="98200-132"><dt>5@@</dt> </span><span class="sxs-lookup"><span data-stu-id="98200-132"><dt>5</dt> </span></span></dl></td>
<td><span data-ttu-id="98200-133">Löschen Sie das TPM.</span><span class="sxs-lookup"><span data-stu-id="98200-133">Clear the TPM.</span></span><br/> <span data-ttu-id="98200-134">Dieser Vorgang kann nicht rückgängig gemacht werden.</span><span class="sxs-lookup"><span data-stu-id="98200-134">This operation cannot be reversed.</span></span> <br/> <span data-ttu-id="98200-135">Weitere Informationen finden Sie in der zugehörigen Methode, die keine physische Präsenz umfasst: <a href="clear-win32-tpm.md"><strong>Clear</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="98200-135">For more information, see this related method that does not involve physical presence: <a href="clear-win32-tpm.md"><strong>Clear</strong></a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="98200-136"><dt>6</dt> </span><span class="sxs-lookup"><span data-stu-id="98200-136"><dt>6</dt> </span></span></dl></td>
<td><span data-ttu-id="98200-137">Aktivieren und aktivieren Sie das TPM.</span><span class="sxs-lookup"><span data-stu-id="98200-137">Enable and activate the TPM.</span></span><br/> <span data-ttu-id="98200-138">Dieser Vorgang wird von Vorgang 7 rückgängig gemacht.</span><span class="sxs-lookup"><span data-stu-id="98200-138">This operation is reversed by operation 7.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="98200-139"><dt>19.00</dt> </span><span class="sxs-lookup"><span data-stu-id="98200-139"><dt>7</dt> </span></span></dl></td>
<td><span data-ttu-id="98200-140">Deaktivieren und deaktivieren Sie das TPM.</span><span class="sxs-lookup"><span data-stu-id="98200-140">Deactivate and disable the TPM.</span></span><br/> <span data-ttu-id="98200-141">Dieser Vorgang wird von Vorgang 6 rückgängig gemacht.</span><span class="sxs-lookup"><span data-stu-id="98200-141">This operation is reversed by operation 6.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="98200-142"><dt>88</dt> </span><span class="sxs-lookup"><span data-stu-id="98200-142"><dt>8</dt> </span></span></dl></td>
<td><span data-ttu-id="98200-143">Ermöglicht die Installation eines TPM-Besitzers.</span><span class="sxs-lookup"><span data-stu-id="98200-143">Allow the installation of a TPM owner.</span></span><br/> <span data-ttu-id="98200-144">Dieser Vorgang wird von Vorgang 9 rückgängig gemacht.</span><span class="sxs-lookup"><span data-stu-id="98200-144">This operation is reversed by operation 9.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="98200-145"><dt>21.00</dt> </span><span class="sxs-lookup"><span data-stu-id="98200-145"><dt>9</dt> </span></span></dl></td>
<td><span data-ttu-id="98200-146">Verhindern Sie die Installation eines TPM-Besitzers.</span><span class="sxs-lookup"><span data-stu-id="98200-146">Prevent the installation of a TPM owner.</span></span><br/> <span data-ttu-id="98200-147">Dieser Vorgang wird von Vorgang 8 rückgängig gemacht.</span><span class="sxs-lookup"><span data-stu-id="98200-147">This operation is reversed by operation 8.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="98200-148"><dt>€</dt> </span><span class="sxs-lookup"><span data-stu-id="98200-148"><dt>10</dt> </span></span></dl></td>
<td><span data-ttu-id="98200-149">Aktivieren, aktivieren und zulassen der Installation eines TPM-Besitzers.</span><span class="sxs-lookup"><span data-stu-id="98200-149">Enable, activate, and allow the installation of a TPM owner.</span></span><br/> <span data-ttu-id="98200-150">Dieser Vorgang wird von Vorgang 11 rückgängig gemacht.</span><span class="sxs-lookup"><span data-stu-id="98200-150">This operation is reversed by operation 11.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="98200-151"><dt>11:</dt> </span><span class="sxs-lookup"><span data-stu-id="98200-151"><dt>11</dt> </span></span></dl></td>
<td><span data-ttu-id="98200-152">Deaktivieren, deaktivieren und verhindern der Installation eines TPM-Besitzers.</span><span class="sxs-lookup"><span data-stu-id="98200-152">Deactivate, disable, and prevent the installation of a TPM owner.</span></span><br/> <span data-ttu-id="98200-153">Dieser Vorgang wird von Vorgang 10 rückgängig gemacht.</span><span class="sxs-lookup"><span data-stu-id="98200-153">This operation is reversed by operation 10.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span></span><dl> <span data-ttu-id="98200-154"><dt><strong></strong></dt><dt>12</dt> </span><span class="sxs-lookup"><span data-stu-id="98200-154"><dt><strong></strong></dt> <dt>12</dt> </span></span></dl></td>
<td><span data-ttu-id="98200-155">Verzögerte physische presenceunownedfieldupgrade</span><span class="sxs-lookup"><span data-stu-id="98200-155">Deferred Physical PresenceunownedFieldUpgrade</span></span><br/> <span data-ttu-id="98200-156">Die Einstellung für die physische Anwesenheit wurde aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="98200-156">Physical presence setting has been updated.</span></span><br/> <span data-ttu-id="98200-157"><strong>Windows 7, Windows Server 2008 R2, Windows Vista und Windows Server 2008:</strong> Dieser Wert wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="98200-157"><strong>Windows 7, Windows Server 2008 R2, Windows Vista and Windows Server 2008:</strong> This value is not supported.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="98200-158"><dt>14</dt> </span><span class="sxs-lookup"><span data-stu-id="98200-158"><dt>14</dt> </span></span></dl></td>
<td><span data-ttu-id="98200-159">Löschen, aktivieren und aktivieren Sie das TPM.</span><span class="sxs-lookup"><span data-stu-id="98200-159">Clear, enable, and activate the TPM.</span></span><br/> <span data-ttu-id="98200-160">Dieser Vorgang kann nicht rückgängig gemacht werden.</span><span class="sxs-lookup"><span data-stu-id="98200-160">This operation cannot be reversed.</span></span><br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="98200-161"><dt>17.15</dt> </span><span class="sxs-lookup"><span data-stu-id="98200-161"><dt>15</dt> </span></span></dl></td>
<td><span data-ttu-id="98200-162">SetNoPPIProvision_False</span><span class="sxs-lookup"><span data-stu-id="98200-162">SetNoPPIProvision_False</span></span><br/> <span data-ttu-id="98200-163">Legt die Bereitstellung fest, die physisch vorhanden sein muss, um das TPM festzulegen.</span><span class="sxs-lookup"><span data-stu-id="98200-163">Sets the provision that you must be physically presence to set the TPM.</span></span><br/> <span data-ttu-id="98200-164">Dieser Vorgang wird von Vorgang 16 rückgängig gemacht.</span><span class="sxs-lookup"><span data-stu-id="98200-164">This operation is reversed by operation 16.</span></span><br/> <span data-ttu-id="98200-165"><strong>Windows 7, Windows Server 2008 R2, Windows Vista und Windows Server 2008:</strong> Dieser Wert wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="98200-165"><strong>Windows 7, Windows Server 2008 R2, Windows Vista and Windows Server 2008:</strong> This value is not supported.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="98200-166"><dt>Uhr</dt> </span><span class="sxs-lookup"><span data-stu-id="98200-166"><dt>16</dt> </span></span></dl></td>
<td><span data-ttu-id="98200-167">SetNoPPIProvision_True</span><span class="sxs-lookup"><span data-stu-id="98200-167">SetNoPPIProvision_True</span></span><br/> <span data-ttu-id="98200-168">Legt fest, dass die Bereitstellung nicht physisch vorhanden sein muss, um das TPM festzulegen.</span><span class="sxs-lookup"><span data-stu-id="98200-168">Sets the provision that you don't need to be physically presence to set the TPM.</span></span><br/> <span data-ttu-id="98200-169">Dieser Vorgang wird von Vorgang 15 rückgängig gemacht.</span><span class="sxs-lookup"><span data-stu-id="98200-169">This operation is reversed by operation 15.</span></span><br/> <span data-ttu-id="98200-170"><strong>Windows 7, Windows Server 2008 R2, Windows Vista und Windows Server 2008:</strong> Dieser Wert wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="98200-170"><strong>Windows 7, Windows Server 2008 R2, Windows Vista and Windows Server 2008:</strong> This value is not supported.</span></span><br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="98200-171"><dt>Uhr</dt> </span><span class="sxs-lookup"><span data-stu-id="98200-171"><dt>17</dt> </span></span></dl></td>
<td><span data-ttu-id="98200-172">SetNoPPIClear_False</span><span class="sxs-lookup"><span data-stu-id="98200-172">SetNoPPIClear_False</span></span><br/> <span data-ttu-id="98200-173">Hiermit wird die Bereitstellung festgelegt, die physisch vorhanden sein muss, um das TPM zu löschen.</span><span class="sxs-lookup"><span data-stu-id="98200-173">Sets the provision that you must be physically presence to clear the TPM.</span></span><br/> <span data-ttu-id="98200-174">Dieser Vorgang wird durch den Vorgang 18 rückgängig gemacht.</span><span class="sxs-lookup"><span data-stu-id="98200-174">This operation is reversed by operation 18.</span></span><br/> <span data-ttu-id="98200-175"><strong>Windows 7, Windows Server 2008 R2, Windows Vista und Windows Server 2008:</strong> Dieser Wert wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="98200-175"><strong>Windows 7, Windows Server 2008 R2, Windows Vista and Windows Server 2008:</strong> This value is not supported.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="98200-176"><dt>Jahren</dt> </span><span class="sxs-lookup"><span data-stu-id="98200-176"><dt>18</dt> </span></span></dl></td>
<td><span data-ttu-id="98200-177">SetNoPPIClear_True</span><span class="sxs-lookup"><span data-stu-id="98200-177">SetNoPPIClear_True</span></span><br/> <span data-ttu-id="98200-178">Hiermit wird die Bereitstellung festgelegt, die nicht physisch vorhanden sein muss, um das TPM zu löschen.</span><span class="sxs-lookup"><span data-stu-id="98200-178">Sets the provision that you don't need to be physically presence to clear the TPM.</span></span><br/> <span data-ttu-id="98200-179">Dieser Vorgang wird von Vorgang 17 rückgängig gemacht.</span><span class="sxs-lookup"><span data-stu-id="98200-179">This operation is reversed by operation 17.</span></span><br/> <span data-ttu-id="98200-180"><strong>Windows 7, Windows Server 2008 R2, Windows Vista und Windows Server 2008:</strong> Dieser Wert wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="98200-180"><strong>Windows 7, Windows Server 2008 R2, Windows Vista and Windows Server 2008:</strong> This value is not supported.</span></span><br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="98200-181"><dt>19.07.2016</dt> </span><span class="sxs-lookup"><span data-stu-id="98200-181"><dt>19</dt> </span></span></dl></td>
<td><span data-ttu-id="98200-182">SetNoPPIMaintenance_False</span><span class="sxs-lookup"><span data-stu-id="98200-182">SetNoPPIMaintenance_False</span></span><br/> <span data-ttu-id="98200-183">Legt fest, dass Sie physisch vorhanden sein müssen, um das TPM beizubehalten.</span><span class="sxs-lookup"><span data-stu-id="98200-183">Sets the provision that you must be physically presence to maintain the TPM.</span></span><br/> <span data-ttu-id="98200-184">Dieser Vorgang wird durch den Vorgang 20 rückgängig gemacht.</span><span class="sxs-lookup"><span data-stu-id="98200-184">This operation is reversed by operation 20.</span></span><br/> <span data-ttu-id="98200-185"><strong>Windows 7, Windows Server 2008 R2, Windows Vista und Windows Server 2008:</strong> Dieser Wert wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="98200-185"><strong>Windows 7, Windows Server 2008 R2, Windows Vista and Windows Server 2008:</strong> This value is not supported.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="98200-186"><dt>20</dt> </span><span class="sxs-lookup"><span data-stu-id="98200-186"><dt>20</dt> </span></span></dl></td>
<td><span data-ttu-id="98200-187">SetNoPPIMaintenance_True</span><span class="sxs-lookup"><span data-stu-id="98200-187">SetNoPPIMaintenance_True</span></span><br/> <span data-ttu-id="98200-188">Legt fest, dass Sie physisch vorhanden sein müssen, um das TPM beizubehalten.</span><span class="sxs-lookup"><span data-stu-id="98200-188">Sets the provision that you must be physically presence to maintain the TPM.</span></span><br/> <span data-ttu-id="98200-189">Dieser Vorgang wird durch den Vorgang 19 rückgängig gemacht.</span><span class="sxs-lookup"><span data-stu-id="98200-189">This operation is reversed by operation 19.</span></span><br/> <span data-ttu-id="98200-190"><strong>Windows 7, Windows Server 2008 R2, Windows Vista und Windows Server 2008:</strong> Dieser Wert wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="98200-190"><strong>Windows 7, Windows Server 2008 R2, Windows Vista and Windows Server 2008:</strong> This value is not supported.</span></span><br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="98200-191"><dt>21</dt> </span><span class="sxs-lookup"><span data-stu-id="98200-191"><dt>21</dt> </span></span></dl></td>
<td><span data-ttu-id="98200-192">Aktivieren + aktivieren + löschen</span><span class="sxs-lookup"><span data-stu-id="98200-192">Enable + Activate + Clear</span></span><br/> <span data-ttu-id="98200-193">Aktivieren, aktivieren und Löschen des TPM.</span><span class="sxs-lookup"><span data-stu-id="98200-193">Enable, activate, and clear the TPM.</span></span><br/> <span data-ttu-id="98200-194"><strong>Windows 7, Windows Server 2008 R2, Windows Vista und Windows Server 2008:</strong> Dieser Wert wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="98200-194"><strong>Windows 7, Windows Server 2008 R2, Windows Vista and Windows Server 2008:</strong> This value is not supported.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="98200-195"><dt>22.11.2016</dt> </span><span class="sxs-lookup"><span data-stu-id="98200-195"><dt>22</dt> </span></span></dl></td>
<td><span data-ttu-id="98200-196">Aktivieren + aktivieren + deaktivieren + aktivieren + aktivieren</span><span class="sxs-lookup"><span data-stu-id="98200-196">Enable + Activate + Clear + Enable + Activate</span></span><br/> <span data-ttu-id="98200-197">Aktivieren, aktivieren und löschen Sie das TPM, und aktivieren und aktivieren Sie dann das TPM.</span><span class="sxs-lookup"><span data-stu-id="98200-197">Enable, activate, and clear the TPM, and then enable and reactivate the TPM.</span></span><br/> <span data-ttu-id="98200-198"><strong>Windows 7, Windows Server 2008 R2, Windows Vista und Windows Server 2008:</strong> Dieser Wert wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="98200-198"><strong>Windows 7, Windows Server 2008 R2, Windows Vista and Windows Server 2008:</strong> This value is not supported.</span></span><br/></td>
</tr>
</tbody>
</table>



 

</dd> <dt>

<span data-ttu-id="98200-199">*Antwort* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="98200-199">*Response* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="98200-200">Typ: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="98200-200">Type: **uint32**</span></span>

<span data-ttu-id="98200-201">Ein ganzzahliger Wert, der die Ergebnisse der Ausführung des physischen TPM-Anwesenheits Vorgangs angibt.</span><span class="sxs-lookup"><span data-stu-id="98200-201">An integer value that specifies the results of performing the TPM physical presence operation.</span></span>

<span data-ttu-id="98200-202">Ein physischer Anwesenheits Vorgang ist erfolgreich, wenn ein physisch vorhandener Benutzer den Vorgang bestätigt und der Vorgang fehlerfrei ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="98200-202">A physical presence operation is successful if a physically present user confirms the operation and if the operation runs without errors.</span></span>

<span data-ttu-id="98200-203">Dieser Wert kann jeden TPM-Fehler enthalten.</span><span class="sxs-lookup"><span data-stu-id="98200-203">This value may contain any TPM error.</span></span> <span data-ttu-id="98200-204">In der folgenden Tabelle werden einige der häufigen Fehler Antworten aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="98200-204">The following table lists some of the common error responses.</span></span>



| <span data-ttu-id="98200-205">Wert</span><span class="sxs-lookup"><span data-stu-id="98200-205">Value</span></span>                                                                                                                                                                                                                                                                    | <span data-ttu-id="98200-206">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="98200-206">Meaning</span></span>                                                             |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| <dl> <span data-ttu-id="98200-207"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="98200-207"><dt>0</dt></span></span> </dl>                                                                                                                                                                                             | <span data-ttu-id="98200-208">Der angeforderte TPM-Vorgang war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="98200-208">The requested TPM operation was successful.</span></span><br/>              |
| <span id="TPM_E_PPI_USER_ABORT"></span><span id="tpm_e_ppi_user_abort"></span><dl> <span data-ttu-id="98200-209"><dt>**TPM \_ E \_ ppi \_ Benutzer \_ Abbruch**</dt> <dt>2150171393 (0x80290301)</dt></span><span class="sxs-lookup"><span data-stu-id="98200-209"><dt>**TPM\_E\_PPI\_USER\_ABORT**</dt> <dt>2150171393 (0x80290301)</dt></span></span> </dl>       | <span data-ttu-id="98200-210">Der Benutzer hat den angeforderten TPM-Vorgang abgelehnt.</span><span class="sxs-lookup"><span data-stu-id="98200-210">The user rejected the requested TPM operation.</span></span><br/>           |
| <span id="TPM_E_PPI_BIOS_FAILURE"></span><span id="tpm_e_ppi_bios_failure"></span><dl> <span data-ttu-id="98200-211"><dt>**TPM \_ E \_ ppi \_ BIOS- \_ Fehler**</dt> <dt>2150171394 (0x80290302)</dt></span><span class="sxs-lookup"><span data-stu-id="98200-211"><dt>**TPM\_E\_PPI\_BIOS\_FAILURE**</dt> <dt>2150171394 (0x80290302)</dt></span></span> </dl> | <span data-ttu-id="98200-212">BIOS-Fehler beim Ausführen des TPM-Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="98200-212">A BIOS failure occurred while running the TPM operation.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="98200-213">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="98200-213">Return value</span></span>

<span data-ttu-id="98200-214">Typ: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="98200-214">Type: **uint32**</span></span>

<span data-ttu-id="98200-215">Alle TPM-Fehler sowie Fehler, die für die TPM-Basisdienste spezifisch sind, können zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="98200-215">All TPM errors as well as errors specific to TPM Base Services can be returned.</span></span>

<span data-ttu-id="98200-216">In der folgenden Tabelle sind einige der allgemeinen Rückgabecodes aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="98200-216">The following table lists some of the common return codes.</span></span>



| <span data-ttu-id="98200-217">Rückgabecode/-wert</span><span class="sxs-lookup"><span data-stu-id="98200-217">Return code/value</span></span>                                                                                                                                                                      | <span data-ttu-id="98200-218">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="98200-218">Description</span></span>                                                                                      |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="98200-219"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="98200-219"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                      | <span data-ttu-id="98200-220">Die Methode war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="98200-220">The method was successful.</span></span><br/>                                                            |
| <dl> <span data-ttu-id="98200-221"><dt>**TPM \_ E- \_ ppi- \_ ACPI- \_ Fehler**</dt> <dt>2150171392 (0x80290300)</dt></span><span class="sxs-lookup"><span data-stu-id="98200-221"><dt>**TPM\_E\_PPI\_ACPI\_FAILURE**</dt> <dt>2150171392 (0x80290300)</dt></span></span> </dl> | <span data-ttu-id="98200-222">Ein Hardwarefehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="98200-222">A hardware failure occurred.</span></span> <span data-ttu-id="98200-223">Weitere Informationen hierzu erhalten Sie von Ihrem Computerhersteller.</span><span class="sxs-lookup"><span data-stu-id="98200-223">Consult your computer manufacturer for more information.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="98200-224">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="98200-224">Remarks</span></span>

<span data-ttu-id="98200-225">Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen.</span><span class="sxs-lookup"><span data-stu-id="98200-225">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="98200-226">MOF-Dateien werden nicht als Teil des Windows SDK installiert.</span><span class="sxs-lookup"><span data-stu-id="98200-226">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="98200-227">Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="98200-227">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="98200-228">Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="98200-228">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="98200-229">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="98200-229">Requirements</span></span>



| <span data-ttu-id="98200-230">Anforderung</span><span class="sxs-lookup"><span data-stu-id="98200-230">Requirement</span></span> | <span data-ttu-id="98200-231">Wert</span><span class="sxs-lookup"><span data-stu-id="98200-231">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="98200-232">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="98200-232">Minimum supported client</span></span><br/> | <span data-ttu-id="98200-233">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="98200-233">Windows Vista \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="98200-234">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="98200-234">Minimum supported server</span></span><br/> | <span data-ttu-id="98200-235">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="98200-235">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="98200-236">Namespace</span><span class="sxs-lookup"><span data-stu-id="98200-236">Namespace</span></span><br/>                | <span data-ttu-id="98200-237">Root \\ CIMV2 \\ Security- \\ mikrosofttpm</span><span class="sxs-lookup"><span data-stu-id="98200-237">Root\\CIMV2\\Security\\MicrosoftTpm</span></span><br/>                                            |
| <span data-ttu-id="98200-238">MOF</span><span class="sxs-lookup"><span data-stu-id="98200-238">MOF</span></span><br/>                      | <dl> <span data-ttu-id="98200-239"><dt>Win32- \_ TPM. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="98200-239"><dt>Win32\_tpm.mof</dt></span></span> </dl> |
| <span data-ttu-id="98200-240">DLL</span><span class="sxs-lookup"><span data-stu-id="98200-240">DLL</span></span><br/>                      | <dl> <span data-ttu-id="98200-241"><dt>Win32- \_tpm.dll</dt></span><span class="sxs-lookup"><span data-stu-id="98200-241"><dt>Win32\_tpm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="98200-242">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="98200-242">See also</span></span>

<dl> <dt>

[<span data-ttu-id="98200-243">**Win32- \_ TPM**</span><span class="sxs-lookup"><span data-stu-id="98200-243">**Win32\_Tpm**</span></span>](win32-tpm.md)
</dt> <dt>

[<span data-ttu-id="98200-244">**Klartext**</span><span class="sxs-lookup"><span data-stu-id="98200-244">**Clear**</span></span>](clear-win32-tpm.md)
</dt> <dt>

[<span data-ttu-id="98200-245">**Deaktivieren**</span><span class="sxs-lookup"><span data-stu-id="98200-245">**Disable**</span></span>](disable-win32-tpm.md)
</dt> <dt>

[<span data-ttu-id="98200-246">**Aktivieren**</span><span class="sxs-lookup"><span data-stu-id="98200-246">**Enable**</span></span>](enable-win32-tpm.md)
</dt> <dt>

[<span data-ttu-id="98200-247">**isEnabled**</span><span class="sxs-lookup"><span data-stu-id="98200-247">**IsEnabled**</span></span>](isenabled-win32-tpm.md)
</dt> </dl>

 

 
