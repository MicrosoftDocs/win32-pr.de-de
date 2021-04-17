---
description: Ändert die Sicherheits Berechtigungen für die logische Datendatei, die im Objekt Pfad angegeben ist (diese Methode ist eine erweiterte Version der changesecurrityberechtigungs-Methode).
ms.assetid: baf50a6e-f624-464e-946d-975aeba88ac2
ms.tgt_platform: multiple
title: Changesecurritypermissionsex-Methode der CIM_DataFile-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DataFile.ChangeSecurityPermissionsEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 3c97f9b17fd148a0686a96fb46f77694a2b78b21
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523795"
---
# <a name="changesecuritypermissionsex-method-of-the-cim_datafile-class"></a><span data-ttu-id="6909c-103">Changesecurritypermissionsex-Methode der CIM \_ DataFile-Klasse</span><span class="sxs-lookup"><span data-stu-id="6909c-103">ChangeSecurityPermissionsEx method of the CIM\_DataFile class</span></span>

<span data-ttu-id="6909c-104">Die **changesecurritypermissionsex** -Methode ändert die Sicherheits Berechtigungen für die logische Datendatei, die im Objekt Pfad angegeben ist (diese Methode ist eine erweiterte Version der [**changesecurrityberechtigungs**](changesecuritypermissions-method-in-class-cim-datafile.md) -Methode).</span><span class="sxs-lookup"><span data-stu-id="6909c-104">The **ChangeSecurityPermissionsEx** method changes the security permissions for the logical data file specified in the object path (this method is an extended version of the [**ChangeSecurityPermissions**](changesecuritypermissions-method-in-class-cim-datafile.md) method).</span></span> <span data-ttu-id="6909c-105">Wenn die logische Datei tatsächlich ein Verzeichnis ist, wird diese Methode rekursiv ausgeführt, und die Sicherheits Berechtigungen für alle Dateien und Unterverzeichnisse, die im Verzeichnis enthalten sind, werden geändert.</span><span class="sxs-lookup"><span data-stu-id="6909c-105">If the logical file is actually a directory, then this method will act recursively, changing the security permissions for all of the files and sub-directories that the directory contains.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="6909c-106">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="6909c-106">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="6909c-107">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="6909c-107">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="6909c-108">In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet.</span><span class="sxs-lookup"><span data-stu-id="6909c-108">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="6909c-109">Weitere Informationen zum Verwenden dieser Methode finden Sie unter [Aufrufen einer Methode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="6909c-109">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="6909c-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="6909c-110">Syntax</span></span>


```mof
uint32 ChangeSecurityPermissionsEx(
  [in]           Win32_SecurityDescriptor SecurityDescriptor,
  [in]           uint32                   Option,
  [out]          string                   StopFileName,
  [in, optional] string                   StartFileName,
  [in, optional] boolean                  Recursive
);
```



## <a name="parameters"></a><span data-ttu-id="6909c-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="6909c-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6909c-112">*SecurityDescriptor* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6909c-112">*SecurityDescriptor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6909c-113">Gibt Sicherheitsinformationen an.</span><span class="sxs-lookup"><span data-stu-id="6909c-113">Specifies security information.</span></span>

> [!Note]  
> <span data-ttu-id="6909c-114">Eine **null** -ACL in der [**Sicherheits \_ deskriptorstruktur**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) gewährt uneingeschränkten Zugriff.</span><span class="sxs-lookup"><span data-stu-id="6909c-114">A **NULL** ACL in the [**SECURITY\_DESCRIPTOR**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) structure grants unlimited access.</span></span> <span data-ttu-id="6909c-115">Weitere Informationen zu den Auswirkungen des unbegrenzten Zugriffs finden Sie unter [Erstellen einer Sicherheits Beschreibung für ein neues Objekt](/windows/desktop/SecAuthZ/creating-a-security-descriptor-for-a-new-object-in-c--).</span><span class="sxs-lookup"><span data-stu-id="6909c-115">For more information about the implications of unlimited access, see [Creating a Security Descriptor for a New Object](/windows/desktop/SecAuthZ/creating-a-security-descriptor-for-a-new-object-in-c--).</span></span>

 

</dd> <dt>

<span data-ttu-id="6909c-116">*Option* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6909c-116">*Option* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6909c-117">Zu ändernde Sicherheits Berechtigung.</span><span class="sxs-lookup"><span data-stu-id="6909c-117">Security privilege to modify.</span></span> <span data-ttu-id="6909c-118">Um z. b. den Besitzer und die DACL-Sicherheit zu ändern, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="6909c-118">For example, to change the owner and DACL security, use:</span></span>

<span data-ttu-id="6909c-119">`Option = 1 + 4` oder `Option = CHANGE_OWNER_SECURITY_INFORMATION | CHANGE_DACL_SECURITY_INFORMATION`</span><span class="sxs-lookup"><span data-stu-id="6909c-119">`Option = 1 + 4` or `Option = CHANGE_OWNER_SECURITY_INFORMATION | CHANGE_DACL_SECURITY_INFORMATION`</span></span>

<dt>

<span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>

<span data-ttu-id="6909c-120"><span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>**Ändern \_ \_Sicherheits \_ Informationen** für den Besitzer (1)</span><span class="sxs-lookup"><span data-stu-id="6909c-120"><span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>**CHANGE\_OWNER\_SECURITY\_INFORMATION** (1)</span></span>


</dt> <dd>

<span data-ttu-id="6909c-121">Ändern Sie den Besitzer der logischen Datei.</span><span class="sxs-lookup"><span data-stu-id="6909c-121">Change the owner of the logical file.</span></span>

</dd> <dt>

<span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>

<span data-ttu-id="6909c-122"><span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>**Ändern \_ Gruppen \_ Sicherheits \_ Informationen** (2)</span><span class="sxs-lookup"><span data-stu-id="6909c-122"><span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>**CHANGE\_GROUP\_SECURITY\_INFORMATION** (2)</span></span>


</dt> <dd>

<span data-ttu-id="6909c-123">Ändern Sie die Gruppe der logischen Datei.</span><span class="sxs-lookup"><span data-stu-id="6909c-123">Change the group of the logical file.</span></span>

</dd> <dt>

<span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>

<span data-ttu-id="6909c-124"><span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>**Ändern \_ DACL- \_ Sicherheits \_ Informationen** (4)</span><span class="sxs-lookup"><span data-stu-id="6909c-124"><span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>**CHANGE\_DACL\_SECURITY\_INFORMATION** (4)</span></span>


</dt> <dd>

<span data-ttu-id="6909c-125">Ändern Sie die ACL der logischen Datei.</span><span class="sxs-lookup"><span data-stu-id="6909c-125">Change the ACL of the logical file.</span></span>

</dd> <dt>

<span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>

<span data-ttu-id="6909c-126"><span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>**Ändern \_ SACL- \_ Sicherheits \_ Informationen** (8)</span><span class="sxs-lookup"><span data-stu-id="6909c-126"><span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>**CHANGE\_SACL\_SECURITY\_INFORMATION** (8)</span></span>


</dt> <dd>

<span data-ttu-id="6909c-127">Ändern Sie die System-ACL der logischen Datei.</span><span class="sxs-lookup"><span data-stu-id="6909c-127">Change the system ACL of the logical file.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="6909c-128">*Stop filename* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="6909c-128">*StopFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6909c-129">Eine Zeichenfolge, die den Namen der Datei (oder des Verzeichnisses) darstellt, in der die Methode fehlgeschlagen ist.</span><span class="sxs-lookup"><span data-stu-id="6909c-129">String that represents the name of the file (or directory) where the method failed.</span></span> <span data-ttu-id="6909c-130">Dieser Parameter ist **null** , wenn die Methode erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="6909c-130">This parameter is **null** if the method succeeds.</span></span>

</dd> <dt>

<span data-ttu-id="6909c-131">*Startdateiname* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="6909c-131">*StartFileName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="6909c-132">Eine Zeichenfolge, die die untergeordnete Datei (oder das Verzeichnis) darstellt, die als Ausgangspunkt für diese Methode verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="6909c-132">String that represents the child file (or directory) to use as a starting point for this method.</span></span> <span data-ttu-id="6909c-133">In der Regel ist der Parameter " *StartFileName* " der Parameter " *StopFileName* ", der die Datei oder das Verzeichnis angibt, in dem ein Fehler im vorherigen Methoden aufrufstyp aufgetreten</span><span class="sxs-lookup"><span data-stu-id="6909c-133">Typically, the *StartFileName* parameter is the *StopFileName* parameter specifying the file or directory at which an error occurred from the previous method call.</span></span> <span data-ttu-id="6909c-134">Wenn dieser Parameter **null** ist, wird der Vorgang für die Datei (oder das Verzeichnis) ausgeführt, die im **ExecMethod** -Befehl angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="6909c-134">If this parameter is **null**, the operation is performed on the file (or directory) specified in the **ExecMethod** call.</span></span>

<span data-ttu-id="6909c-135">Wenn *StartFileName* verwendet wird, muss *rekursive* auch auf true festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="6909c-135">If *StartFileName* is used, *Recursive* must be set to true as well.</span></span>

</dd> <dt>

<span data-ttu-id="6909c-136">*Rekursiv* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="6909c-136">*Recursive* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="6909c-137">**True** gibt an, dass die Methode auch rekursiv auf Dateien und Verzeichnisse innerhalb des Verzeichnisses angewendet wird, das von der [**CIM \_ DataFile**](cim-datafile.md) -Instanz angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="6909c-137">If **True**, the method is also applied recursively to files and directories within the directory that is specified by the [**CIM\_DataFile**](cim-datafile.md) instance.</span></span> <span data-ttu-id="6909c-138">Bei Datei Instanzen wird dieser Parameter ignoriert.</span><span class="sxs-lookup"><span data-stu-id="6909c-138">For file instances, this parameter is ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6909c-139">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6909c-139">Return value</span></span>

<span data-ttu-id="6909c-140">Gibt bei Erfolg den Wert 0 (null) zurück, und jede andere Zahl gibt einen Fehler an.</span><span class="sxs-lookup"><span data-stu-id="6909c-140">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span> <span data-ttu-id="6909c-141">Weitere Fehlercodes finden Sie unter [**WMI-Fehler Konstanten**](/windows/desktop/WmiSdk/wmi-error-constants) oder [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="6909c-141">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="6909c-142">Allgemeine **HRESULT** -Werte finden Sie unter [System Fehler Codes](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="6909c-142">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="6909c-143">**Erfolgreich**</span><span class="sxs-lookup"><span data-stu-id="6909c-143">**Success**</span></span>
</dt> <dd>

<span data-ttu-id="6909c-144">0</span><span class="sxs-lookup"><span data-stu-id="6909c-144">0</span></span>

<span data-ttu-id="6909c-145">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="6909c-145">Success.</span></span>

</dd> <dt>

<span data-ttu-id="6909c-146">**Zugriff verweigert**</span><span class="sxs-lookup"><span data-stu-id="6909c-146">**Access Denied**</span></span>
</dt> <dd>

<span data-ttu-id="6909c-147">2</span><span class="sxs-lookup"><span data-stu-id="6909c-147">2</span></span>

<span data-ttu-id="6909c-148">Zugriff verweigert.</span><span class="sxs-lookup"><span data-stu-id="6909c-148">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="6909c-149">**Nicht spezifizierter Fehler**</span><span class="sxs-lookup"><span data-stu-id="6909c-149">**Unspecified failure**</span></span>
</dt> <dd>

<span data-ttu-id="6909c-150">8</span><span class="sxs-lookup"><span data-stu-id="6909c-150">8</span></span>

<span data-ttu-id="6909c-151">Nicht spezifizierter Fehler.</span><span class="sxs-lookup"><span data-stu-id="6909c-151">Unspecified failure.</span></span>

</dd> <dt>

<span data-ttu-id="6909c-152">**Ungültiges Objekt**</span><span class="sxs-lookup"><span data-stu-id="6909c-152">**Invalid object**</span></span>
</dt> <dd>

<span data-ttu-id="6909c-153">9</span><span class="sxs-lookup"><span data-stu-id="6909c-153">9</span></span>

<span data-ttu-id="6909c-154">Der angegebene Objektname ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="6909c-154">Object name specified is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="6909c-155">**Objekt ist bereits vorhanden.**</span><span class="sxs-lookup"><span data-stu-id="6909c-155">**Object already exists**</span></span>
</dt> <dd>

<span data-ttu-id="6909c-156">10</span><span class="sxs-lookup"><span data-stu-id="6909c-156">10</span></span>

<span data-ttu-id="6909c-157">Das Objekt ist bereits vorhanden.</span><span class="sxs-lookup"><span data-stu-id="6909c-157">Object already exists.</span></span>

</dd> <dt>

<span data-ttu-id="6909c-158">**Dateisystem nicht NTFS**</span><span class="sxs-lookup"><span data-stu-id="6909c-158">**File system not NTFS**</span></span>
</dt> <dd>

<span data-ttu-id="6909c-159">11</span><span class="sxs-lookup"><span data-stu-id="6909c-159">11</span></span>

<span data-ttu-id="6909c-160">Das Dateisystem ist nicht NTFS.</span><span class="sxs-lookup"><span data-stu-id="6909c-160">File system not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="6909c-161">**Plattform nicht NT/Windows 2000**</span><span class="sxs-lookup"><span data-stu-id="6909c-161">**Platform not NT/Windows 2000**</span></span>
</dt> <dd>

<span data-ttu-id="6909c-162">12</span><span class="sxs-lookup"><span data-stu-id="6909c-162">12</span></span>

<span data-ttu-id="6909c-163">Plattform nicht Windows.</span><span class="sxs-lookup"><span data-stu-id="6909c-163">Platform not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="6909c-164">**Laufwerk nicht identisch**</span><span class="sxs-lookup"><span data-stu-id="6909c-164">**Drive not the same**</span></span>
</dt> <dd>

<span data-ttu-id="6909c-165">13</span><span class="sxs-lookup"><span data-stu-id="6909c-165">13</span></span>

<span data-ttu-id="6909c-166">Das Laufwerk ist nicht identisch.</span><span class="sxs-lookup"><span data-stu-id="6909c-166">Drive not the same.</span></span>

</dd> <dt>

<span data-ttu-id="6909c-167">**Verzeichnis nicht leer**</span><span class="sxs-lookup"><span data-stu-id="6909c-167">**Directory not empty**</span></span>
</dt> <dd>

<span data-ttu-id="6909c-168">14</span><span class="sxs-lookup"><span data-stu-id="6909c-168">14</span></span>

<span data-ttu-id="6909c-169">„Verzeichnis ist nicht leer.“</span><span class="sxs-lookup"><span data-stu-id="6909c-169">Directory not empty.</span></span>

</dd> <dt>

<span data-ttu-id="6909c-170">**Freigabe Verletzung**</span><span class="sxs-lookup"><span data-stu-id="6909c-170">**Sharing violation**</span></span>
</dt> <dd>

<span data-ttu-id="6909c-171">15</span><span class="sxs-lookup"><span data-stu-id="6909c-171">15</span></span>

<span data-ttu-id="6909c-172">Freigabeverletzung.</span><span class="sxs-lookup"><span data-stu-id="6909c-172">Sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="6909c-173">**Ungültige Startdatei**</span><span class="sxs-lookup"><span data-stu-id="6909c-173">**Invalid start file**</span></span>
</dt> <dd>

<span data-ttu-id="6909c-174">16</span><span class="sxs-lookup"><span data-stu-id="6909c-174">16</span></span>

<span data-ttu-id="6909c-175">Die Startdatei ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="6909c-175">The start file is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="6909c-176">**Berechtigung nicht aufrechterhalten**</span><span class="sxs-lookup"><span data-stu-id="6909c-176">**Privilege not held**</span></span>
</dt> <dd>

<span data-ttu-id="6909c-177">17</span><span class="sxs-lookup"><span data-stu-id="6909c-177">17</span></span>

<span data-ttu-id="6909c-178">Die Berechtigung wurde nicht aufrechterhalten.</span><span class="sxs-lookup"><span data-stu-id="6909c-178">Privilege not held.</span></span>

</dd> <dt>

<span data-ttu-id="6909c-179">**Ungültiger Parameter**</span><span class="sxs-lookup"><span data-stu-id="6909c-179">**Invalid parameter**</span></span>
</dt> <dd>

<span data-ttu-id="6909c-180">21</span><span class="sxs-lookup"><span data-stu-id="6909c-180">21</span></span>

<span data-ttu-id="6909c-181">Ein Parameter ist nicht gültig.</span><span class="sxs-lookup"><span data-stu-id="6909c-181">A parameter is not valid.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6909c-182">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6909c-182">Remarks</span></span>

<span data-ttu-id="6909c-183">Die **changesecurritypermissionsex** -Methode in [**CIM \_ DataFile**](cim-datafile.md) wird von WMI implementiert.</span><span class="sxs-lookup"><span data-stu-id="6909c-183">The **ChangeSecurityPermissionsEx** method in [**CIM\_DataFile**](cim-datafile.md) is implemented by WMI.</span></span>

<span data-ttu-id="6909c-184">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="6909c-184">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="6909c-185">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="6909c-185">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="6909c-186">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6909c-186">Requirements</span></span>



| <span data-ttu-id="6909c-187">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6909c-187">Requirement</span></span> | <span data-ttu-id="6909c-188">Wert</span><span class="sxs-lookup"><span data-stu-id="6909c-188">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6909c-189">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6909c-189">Minimum supported client</span></span><br/> | <span data-ttu-id="6909c-190">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6909c-190">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="6909c-191">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6909c-191">Minimum supported server</span></span><br/> | <span data-ttu-id="6909c-192">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6909c-192">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="6909c-193">Namespace</span><span class="sxs-lookup"><span data-stu-id="6909c-193">Namespace</span></span><br/>                | <span data-ttu-id="6909c-194">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="6909c-194">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="6909c-195">MOF</span><span class="sxs-lookup"><span data-stu-id="6909c-195">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6909c-196"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="6909c-196"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="6909c-197">DLL</span><span class="sxs-lookup"><span data-stu-id="6909c-197">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6909c-198"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6909c-198"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6909c-199">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6909c-199">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6909c-200">**CIM- \_ Datendatei**</span><span class="sxs-lookup"><span data-stu-id="6909c-200">**CIM\_DataFile**</span></span>](changesecuritypermissionsex-method-in-class-cim-datafile.md)
</dt> <dt>

[<span data-ttu-id="6909c-201">**CIM- \_ Datendatei**</span><span class="sxs-lookup"><span data-stu-id="6909c-201">**CIM\_DataFile**</span></span>](cim-datafile.md)
</dt> <dt>

[<span data-ttu-id="6909c-202">WMI-Tasks: Dateien und Ordner</span><span class="sxs-lookup"><span data-stu-id="6909c-202">WMI Tasks: Files and Folders</span></span>](/windows/desktop/WmiSdk/wmi-tasks--files-and-folders)
</dt> <dt>

[<span data-ttu-id="6909c-203">**Datei-und Verzeichniszugriffs Rechte-Konstanten**</span><span class="sxs-lookup"><span data-stu-id="6909c-203">**File and Directory Access Rights Constants**</span></span>](/windows/desktop/WmiSdk/file-and-directory-access-rights-constants)
</dt> </dl>

 

