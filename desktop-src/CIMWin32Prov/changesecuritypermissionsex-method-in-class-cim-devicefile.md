---
description: Ändert die Sicherheits Berechtigungen für die im Objekt Pfad angegebene Gerätedatei (diese Methode ist eine erweiterte Version der changesecurrityberechtigungs-Methode).
ms.assetid: 5ad54470-6961-4c0d-9d2a-d3eaf81d75f4
ms.tgt_platform: multiple
title: Changesecurritypermissionsex-Methode der CIM_DeviceFile-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DeviceFile.ChangeSecurityPermissionsEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 5f2c7261844542f6414052517432c2e8ff3f1194
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127089"
---
# <a name="changesecuritypermissionsex-method-of-the-cim_devicefile-class"></a><span data-ttu-id="cf091-103">Changesecurritypermissionsex-Methode der CIM \_ Devicefile-Klasse</span><span class="sxs-lookup"><span data-stu-id="cf091-103">ChangeSecurityPermissionsEx method of the CIM\_DeviceFile class</span></span>

<span data-ttu-id="cf091-104">Die **changesecurritypermissionsex** -Methode ändert die Sicherheits Berechtigungen für die im Objekt Pfad angegebene Gerätedatei (diese Methode ist eine erweiterte Version der [**changesecurrityberechtigungs**](changesecuritypermissions-method-in-class-cim-devicefile.md) -Methode).</span><span class="sxs-lookup"><span data-stu-id="cf091-104">The **ChangeSecurityPermissionsEx** method changes the security permissions for the device file specified in the object path (this method is an extended version of the [**ChangeSecurityPermissions**](changesecuritypermissions-method-in-class-cim-devicefile.md) method).</span></span> <span data-ttu-id="cf091-105">Wenn die logische Datei ein Verzeichnis ist, wird diese Methode rekursiv durchlaufen, und die Sicherheits Berechtigungen für alle Dateien und Unterverzeichnisse, die im Verzeichnis enthalten sind, werden geändert.</span><span class="sxs-lookup"><span data-stu-id="cf091-105">If the logical file is a directory, then this method acts recursively, changing the security permissions for all of the files and sub-directories that the directory contains.</span></span> <span data-ttu-id="cf091-106">Diese Methode wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="cf091-106">This method is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="cf091-107">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="cf091-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="cf091-108">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="cf091-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="cf091-109">In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet.</span><span class="sxs-lookup"><span data-stu-id="cf091-109">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="cf091-110">Weitere Informationen zum Verwenden dieser Methode finden Sie unter [Aufrufen einer Methode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="cf091-110">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="cf091-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="cf091-111">Syntax</span></span>


```mof
uint32 ChangeSecurityPermissionsEx(
  [in]           Win32_SecurityDescriptor SecurityDescriptor,
  [in]           uint32                   Option,
  [out]          string                   StopFileName,
  [in, optional] string                   StartFileName,
  [in, optional] boolean                  Recursive
);
```



## <a name="parameters"></a><span data-ttu-id="cf091-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="cf091-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cf091-113">*SecurityDescriptor* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="cf091-113">*SecurityDescriptor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cf091-114">Gibt die Sicherheitsinformationen an.</span><span class="sxs-lookup"><span data-stu-id="cf091-114">Specifies the security information.</span></span>

> [!Caution]  
> <span data-ttu-id="cf091-115">Eine **null** -ACL in der [**Sicherheits \_ deskriptorstruktur**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) gewährt uneingeschränkten Zugriff.</span><span class="sxs-lookup"><span data-stu-id="cf091-115">A **NULL** ACL in the [**SECURITY\_DESCRIPTOR**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) structure grants unlimited access.</span></span>

 

</dd> <dt>

<span data-ttu-id="cf091-116">*Option* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="cf091-116">*Option* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cf091-117">Zu ändernde Sicherheits Berechtigung.</span><span class="sxs-lookup"><span data-stu-id="cf091-117">Security privilege to modify.</span></span> <span data-ttu-id="cf091-118">Wenn Sie z. b. den Besitzer und die DACL-Sicherheit ändern möchten, verwenden Sie</span><span class="sxs-lookup"><span data-stu-id="cf091-118">For example, to change the owner and DACL security, use</span></span>

`Option = 1 + 4`

<span data-ttu-id="cf091-119">oder</span><span class="sxs-lookup"><span data-stu-id="cf091-119">or</span></span>

`Option = CHANGE_OWNER_SECURITY_INFORMATION | CHANGE_DACL_SECURITY_INFORMATION`

<dt>

<span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>

<span data-ttu-id="cf091-120"><span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>**Ändern \_ \_Sicherheits \_ Informationen** für den Besitzer (1)</span><span class="sxs-lookup"><span data-stu-id="cf091-120"><span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>**CHANGE\_OWNER\_SECURITY\_INFORMATION** (1)</span></span>


</dt> <dd>

<span data-ttu-id="cf091-121">Ändern Sie den Besitzer der logischen Datei.</span><span class="sxs-lookup"><span data-stu-id="cf091-121">Change the owner of the logical file.</span></span>

</dd> <dt>

<span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>

<span data-ttu-id="cf091-122"><span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>**Ändern \_ Gruppen \_ Sicherheits \_ Informationen** (2)</span><span class="sxs-lookup"><span data-stu-id="cf091-122"><span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>**CHANGE\_GROUP\_SECURITY\_INFORMATION** (2)</span></span>


</dt> <dd>

<span data-ttu-id="cf091-123">Ändern Sie die Gruppe der logischen Datei.</span><span class="sxs-lookup"><span data-stu-id="cf091-123">Change the group of the logical file.</span></span>

</dd> <dt>

<span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>

<span data-ttu-id="cf091-124"><span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>**Ändern \_ DACL- \_ Sicherheits \_ Informationen** (4)</span><span class="sxs-lookup"><span data-stu-id="cf091-124"><span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>**CHANGE\_DACL\_SECURITY\_INFORMATION** (4)</span></span>


</dt> <dd>

<span data-ttu-id="cf091-125">Ändern Sie die ACL der logischen Datei.</span><span class="sxs-lookup"><span data-stu-id="cf091-125">Change the ACL of the logical file.</span></span>

</dd> <dt>

<span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>

<span data-ttu-id="cf091-126"><span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>**Ändern \_ SACL- \_ Sicherheits \_ Informationen** (8)</span><span class="sxs-lookup"><span data-stu-id="cf091-126"><span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>**CHANGE\_SACL\_SECURITY\_INFORMATION** (8)</span></span>


</dt> <dd>

<span data-ttu-id="cf091-127">Ändern Sie die System-ACL der logischen Datei.</span><span class="sxs-lookup"><span data-stu-id="cf091-127">Change the system ACL of the logical file.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="cf091-128">*Stop filename* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="cf091-128">*StopFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cf091-129">Eine Zeichenfolge, die den Namen der Datei (oder des Verzeichnisses) darstellt, in der die Methode fehlgeschlagen ist.</span><span class="sxs-lookup"><span data-stu-id="cf091-129">String that represents the name of the file (or directory) where the method failed.</span></span> <span data-ttu-id="cf091-130">Dieser Parameter ist **null** , wenn die Methode erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="cf091-130">This parameter is **null** if the method succeeds.</span></span>

</dd> <dt>

<span data-ttu-id="cf091-131">*Startdateiname* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="cf091-131">*StartFileName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="cf091-132">Die untergeordnete Datei (oder das Verzeichnis), die als Ausgangspunkt für diese Methode verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="cf091-132">Child file (or directory) to use as a starting point for this method.</span></span> <span data-ttu-id="cf091-133">In der Regel ist der Parameter " *StartFileName* " der Parameter " *StopFileName* ", der die Datei oder das Verzeichnis angibt, in dem ein Fehler im vorherigen Methoden aufrufstyp aufgetreten</span><span class="sxs-lookup"><span data-stu-id="cf091-133">Typically, the *StartFileName* parameter is the *StopFileName* parameter specifying the file or directory at which an error occurred from the previous method call.</span></span> <span data-ttu-id="cf091-134">Wenn dieser Parameter **null** ist, wird der Vorgang für die Datei (oder das Verzeichnis) ausgeführt, die im [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) -Befehl angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="cf091-134">If this parameter is **null**, the operation is performed on the file (or directory) specified in the [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) call.</span></span>

</dd> <dt>

<span data-ttu-id="cf091-135">*Rekursiv* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="cf091-135">*Recursive* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="cf091-136">**True** gibt an, dass die Methode auch rekursiv auf Dateien und Verzeichnisse innerhalb des Verzeichnisses angewendet wird, das von der [**CIM \_ Devicefile**](cim-devicefile.md) -Instanz angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="cf091-136">If **TRUE**, the method is also applied recursively to files and directories within the directory specified by the [**CIM\_DeviceFile**](cim-devicefile.md) instance.</span></span> <span data-ttu-id="cf091-137">Bei Datei Instanzen wird dieser Parameter ignoriert.</span><span class="sxs-lookup"><span data-stu-id="cf091-137">For file instances, this parameter is ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cf091-138">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="cf091-138">Return value</span></span>

<span data-ttu-id="cf091-139">Gibt bei Erfolg den Wert 0 (null) zurück, und jede andere Zahl gibt einen Fehler an.</span><span class="sxs-lookup"><span data-stu-id="cf091-139">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span>

<dl> <dt>


</dt> <dd>

<span data-ttu-id="cf091-140">0</span><span class="sxs-lookup"><span data-stu-id="cf091-140">0</span></span>

<span data-ttu-id="cf091-141">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="cf091-141">Success.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="cf091-142">2</span><span class="sxs-lookup"><span data-stu-id="cf091-142">2</span></span>

<span data-ttu-id="cf091-143">Zugriff verweigert.</span><span class="sxs-lookup"><span data-stu-id="cf091-143">Access denied.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="cf091-144">8</span><span class="sxs-lookup"><span data-stu-id="cf091-144">8</span></span>

<span data-ttu-id="cf091-145">Nicht spezifizierter Fehler.</span><span class="sxs-lookup"><span data-stu-id="cf091-145">Unspecified failure.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="cf091-146">9</span><span class="sxs-lookup"><span data-stu-id="cf091-146">9</span></span>

<span data-ttu-id="cf091-147">Ungültiges Objekt.</span><span class="sxs-lookup"><span data-stu-id="cf091-147">Invalid object.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="cf091-148">10</span><span class="sxs-lookup"><span data-stu-id="cf091-148">10</span></span>

<span data-ttu-id="cf091-149">Das Objekt ist bereits vorhanden.</span><span class="sxs-lookup"><span data-stu-id="cf091-149">Object already exists.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="cf091-150">11</span><span class="sxs-lookup"><span data-stu-id="cf091-150">11</span></span>

<span data-ttu-id="cf091-151">Das Dateisystem ist nicht NTFS.</span><span class="sxs-lookup"><span data-stu-id="cf091-151">File system not NTFS.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="cf091-152">12</span><span class="sxs-lookup"><span data-stu-id="cf091-152">12</span></span>

<span data-ttu-id="cf091-153">Plattform nicht Windows.</span><span class="sxs-lookup"><span data-stu-id="cf091-153">Platform not Windows.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="cf091-154">13</span><span class="sxs-lookup"><span data-stu-id="cf091-154">13</span></span>

<span data-ttu-id="cf091-155">Das Laufwerk ist nicht identisch.</span><span class="sxs-lookup"><span data-stu-id="cf091-155">Drive not the same.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="cf091-156">14</span><span class="sxs-lookup"><span data-stu-id="cf091-156">14</span></span>

<span data-ttu-id="cf091-157">„Verzeichnis ist nicht leer.“</span><span class="sxs-lookup"><span data-stu-id="cf091-157">Directory not empty.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="cf091-158">15</span><span class="sxs-lookup"><span data-stu-id="cf091-158">15</span></span>

<span data-ttu-id="cf091-159">Freigabeverletzung.</span><span class="sxs-lookup"><span data-stu-id="cf091-159">Sharing violation.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="cf091-160">16</span><span class="sxs-lookup"><span data-stu-id="cf091-160">16</span></span>

<span data-ttu-id="cf091-161">Ungültige Startdatei.</span><span class="sxs-lookup"><span data-stu-id="cf091-161">Invalid start file.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="cf091-162">17</span><span class="sxs-lookup"><span data-stu-id="cf091-162">17</span></span>

<span data-ttu-id="cf091-163">Die Berechtigung wurde nicht aufrechterhalten.</span><span class="sxs-lookup"><span data-stu-id="cf091-163">Privilege not held.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="cf091-164">21</span><span class="sxs-lookup"><span data-stu-id="cf091-164">21</span></span>

<span data-ttu-id="cf091-165">Ungültiger Parameter.</span><span class="sxs-lookup"><span data-stu-id="cf091-165">Invalid parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="cf091-166">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="cf091-166">Remarks</span></span>

<span data-ttu-id="cf091-167">Diese Methode wird zurzeit nicht von WMI implementiert.</span><span class="sxs-lookup"><span data-stu-id="cf091-167">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="cf091-168">Um diese Methode verwenden zu können, müssen Sie Sie in Ihrem eigenen Anbieter implementieren.</span><span class="sxs-lookup"><span data-stu-id="cf091-168">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="cf091-169">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="cf091-169">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="cf091-170">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="cf091-170">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="cf091-171">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cf091-171">Requirements</span></span>



| <span data-ttu-id="cf091-172">Anforderung</span><span class="sxs-lookup"><span data-stu-id="cf091-172">Requirement</span></span> | <span data-ttu-id="cf091-173">Wert</span><span class="sxs-lookup"><span data-stu-id="cf091-173">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="cf091-174">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="cf091-174">Minimum supported client</span></span><br/> | <span data-ttu-id="cf091-175">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="cf091-175">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="cf091-176">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="cf091-176">Minimum supported server</span></span><br/> | <span data-ttu-id="cf091-177">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="cf091-177">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="cf091-178">Namespace</span><span class="sxs-lookup"><span data-stu-id="cf091-178">Namespace</span></span><br/>                | <span data-ttu-id="cf091-179">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="cf091-179">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="cf091-180">MOF</span><span class="sxs-lookup"><span data-stu-id="cf091-180">MOF</span></span><br/>                      | <dl> <span data-ttu-id="cf091-181"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="cf091-181"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="cf091-182">DLL</span><span class="sxs-lookup"><span data-stu-id="cf091-182">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cf091-183"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cf091-183"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cf091-184">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cf091-184">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cf091-185">CIM- \_ Devicefile</span><span class="sxs-lookup"><span data-stu-id="cf091-185">CIM\_DeviceFile</span></span>](changesecuritypermissionsex-method-in-class-cim-devicefile.md)
</dt> <dt>

[<span data-ttu-id="cf091-186">**CIM- \_ Devicefile**</span><span class="sxs-lookup"><span data-stu-id="cf091-186">**CIM\_DeviceFile**</span></span>](cim-devicefile.md)
</dt> </dl>

 

