---
description: Ändert die Sicherheits Berechtigungen für die im Objekt Pfad angegebene Datei für den logischen Verzeichniseintrag (diese Methode ist eine erweiterte Version der changesecurrityberechtigungs Methode und wird von CIM \_ LogicalFile geerbt).
ms.assetid: 5c1f66ba-9aa1-47ca-8fcf-7663782544cd
ms.tgt_platform: multiple
title: Changesecurritypermissionsex-Methode der CIM_Directory-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Directory.ChangeSecurityPermissionsEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: f2d8ddf4c6ffdbd016db1e8c08d89f2dd6476ccf
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106338904"
---
# <a name="changesecuritypermissionsex-method-of-the-cim_directory-class"></a><span data-ttu-id="3bfee-103">Changesecurritypermissionsex-Methode der CIM- \_ Verzeichnis Klasse</span><span class="sxs-lookup"><span data-stu-id="3bfee-103">ChangeSecurityPermissionsEx method of the CIM\_Directory class</span></span>

<span data-ttu-id="3bfee-104">Mit der **changesecurritypermissionsex** -Methode werden die Sicherheits Berechtigungen für die im Objekt Pfad angegebene Datei mit dem logischen Verzeichnis geändert (diese Methode ist eine erweiterte Version der [**changesecurrityberechtigungs**](changesecuritypermissions-method-in-class-cim-directory.md) Methode und wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt).</span><span class="sxs-lookup"><span data-stu-id="3bfee-104">The **ChangeSecurityPermissionsEx** method changes the security permissions for the logical directory entry file specified in the object path (this method is an extended version of the [**ChangeSecurityPermissions**](changesecuritypermissions-method-in-class-cim-directory.md) method and is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md)).</span></span> <span data-ttu-id="3bfee-105">Wenn die logische Datei ein Verzeichnis ist, wird diese Methode rekursiv ausgeführt, und die Sicherheits Berechtigungen für alle Dateien und Unterverzeichnisse, die im Verzeichnis enthalten sind, werden geändert.</span><span class="sxs-lookup"><span data-stu-id="3bfee-105">If the logical file is a directory, then this method will act recursively, changing the security permissions for all of the files and sub-directories that the directory contains.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="3bfee-106">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="3bfee-106">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="3bfee-107">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="3bfee-107">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="3bfee-108">In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet.</span><span class="sxs-lookup"><span data-stu-id="3bfee-108">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="3bfee-109">Weitere Informationen zum Verwenden dieser Methode finden Sie unter [Aufrufen einer Methode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="3bfee-109">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="3bfee-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="3bfee-110">Syntax</span></span>


```mof
uint32 ChangeSecurityPermissionsEx(
  [in]           Win32_SecurityDescriptor SecurityDescriptor,
  [in]           uint32                   Option,
  [out]          string                   StopFileName,
  [in, optional] string                   StartFileName,
  [in, optional] boolean                  Recursive
);
```



## <a name="parameters"></a><span data-ttu-id="3bfee-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="3bfee-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3bfee-112">*SecurityDescriptor* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3bfee-112">*SecurityDescriptor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3bfee-113">Gibt Sicherheitsinformationen an.</span><span class="sxs-lookup"><span data-stu-id="3bfee-113">Specifies security information.</span></span>

> [!Note]  
> <span data-ttu-id="3bfee-114">Eine **null** -ACL in der [**Sicherheits \_ deskriptorstruktur**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) gewährt uneingeschränkten Zugriff.</span><span class="sxs-lookup"><span data-stu-id="3bfee-114">A **NULL** ACL in the [**SECURITY\_DESCRIPTOR**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) structure grants unlimited access.</span></span>

 

</dd> <dt>

<span data-ttu-id="3bfee-115">*Option* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3bfee-115">*Option* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3bfee-116">Zu ändernde Sicherheits Berechtigung.</span><span class="sxs-lookup"><span data-stu-id="3bfee-116">Security privilege to modify.</span></span> <span data-ttu-id="3bfee-117">Wenn Sie z. b. den Besitzer und die DACL-Sicherheit ändern möchten, verwenden Sie</span><span class="sxs-lookup"><span data-stu-id="3bfee-117">For example, to change the owner and DACL security, use</span></span>

`Option = 1 + 4`

<span data-ttu-id="3bfee-118">oder</span><span class="sxs-lookup"><span data-stu-id="3bfee-118">or</span></span>

`Option = CHANGE_OWNER_SECURITY_INFORMATION | CHANGE_DACL_SECURITY_INFORMATION`

<dt>

<span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>

<span data-ttu-id="3bfee-119"><span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>**Ändern \_ \_Sicherheits \_ Informationen** für den Besitzer (1)</span><span class="sxs-lookup"><span data-stu-id="3bfee-119"><span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>**CHANGE\_OWNER\_SECURITY\_INFORMATION** (1)</span></span>


</dt> <dd>

<span data-ttu-id="3bfee-120">Ändern Sie den Besitzer der logischen Datei.</span><span class="sxs-lookup"><span data-stu-id="3bfee-120">Change the owner of the logical file.</span></span>

</dd> <dt>

<span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>

<span data-ttu-id="3bfee-121"><span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>**Ändern \_ Gruppen \_ Sicherheits \_ Informationen** (2)</span><span class="sxs-lookup"><span data-stu-id="3bfee-121"><span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>**CHANGE\_GROUP\_SECURITY\_INFORMATION** (2)</span></span>


</dt> <dd>

<span data-ttu-id="3bfee-122">Ändern Sie die Gruppe der logischen Datei.</span><span class="sxs-lookup"><span data-stu-id="3bfee-122">Change the group of the logical file.</span></span>

</dd> <dt>

<span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>

<span data-ttu-id="3bfee-123"><span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>**Ändern \_ DACL- \_ Sicherheits \_ Informationen** (4)</span><span class="sxs-lookup"><span data-stu-id="3bfee-123"><span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>**CHANGE\_DACL\_SECURITY\_INFORMATION** (4)</span></span>


</dt> <dd>

<span data-ttu-id="3bfee-124">Ändern Sie die ACL der logischen Datei.</span><span class="sxs-lookup"><span data-stu-id="3bfee-124">Change the ACL of the logical file.</span></span>

</dd> <dt>

<span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>

<span data-ttu-id="3bfee-125"><span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>**Ändern \_ SACL- \_ Sicherheits \_ Informationen** (8)</span><span class="sxs-lookup"><span data-stu-id="3bfee-125"><span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>**CHANGE\_SACL\_SECURITY\_INFORMATION** (8)</span></span>


</dt> <dd>

<span data-ttu-id="3bfee-126">Ändern Sie die System-ACL der logischen Datei.</span><span class="sxs-lookup"><span data-stu-id="3bfee-126">Change the system ACL of the logical file.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="3bfee-127">*Stop filename* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="3bfee-127">*StopFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3bfee-128">Eine Zeichenfolge, die den Namen der Datei (oder des Verzeichnisses) darstellt, in der die Methode fehlgeschlagen ist.</span><span class="sxs-lookup"><span data-stu-id="3bfee-128">String that represents the name of the file (or directory) where the method failed.</span></span> <span data-ttu-id="3bfee-129">Dieser Parameter hat den Wert **null** , wenn die Methode erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="3bfee-129">This parameter has a value of **null** if the method succeeds.</span></span>

</dd> <dt>

<span data-ttu-id="3bfee-130">*Startdateiname* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="3bfee-130">*StartFileName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="3bfee-131">Eine Zeichenfolge, die die untergeordnete Datei (oder das Verzeichnis) darstellt, die als Ausgangspunkt für diese Methode verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="3bfee-131">String that represents the child file (or directory) to use as a starting point for this method.</span></span> <span data-ttu-id="3bfee-132">In der Regel ist der Parameter " *StartFileName* " der Parameter " *StopFileName* ", der die Datei (oder das Verzeichnis) angibt, in der ein Fehler des vorherigen Methoden Aufrufes aufgetreten ist</span><span class="sxs-lookup"><span data-stu-id="3bfee-132">Typically, the *StartFileName* parameter is the *StopFileName* parameter specifying the file (or directory) at which an error occurred from the previous method call.</span></span> <span data-ttu-id="3bfee-133">Wenn der Parameterwert **null** ist, wird der Vorgang für die im [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) -Befehl angegebene Datei oder das Verzeichnis ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="3bfee-133">If the parameter value is **null**, the operation is performed on the file or directory specified in the [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) call.</span></span>

</dd> <dt>

<span data-ttu-id="3bfee-134">*Rekursiv* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="3bfee-134">*Recursive* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="3bfee-135">**True** gibt an, dass die Methode auch rekursiv auf Dateien und Verzeichnisse innerhalb des Verzeichnisses angewendet wird, das von der [**CIM- \_ Verzeichnis**](cim-directory.md) Instanz angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="3bfee-135">If **TRUE**, the method is also applied recursively to files and directories within the directory specified by the [**CIM\_Directory**](cim-directory.md) instance.</span></span> <span data-ttu-id="3bfee-136">Bei Datei Instanzen wird dieser Parameter ignoriert.</span><span class="sxs-lookup"><span data-stu-id="3bfee-136">For file instances, this parameter is ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3bfee-137">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3bfee-137">Return value</span></span>

<span data-ttu-id="3bfee-138">Gibt bei Erfolg den Wert 0 (null) zurück, und jede andere Zahl gibt einen Fehler an.</span><span class="sxs-lookup"><span data-stu-id="3bfee-138">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span>

<dl> <dt>


</dt> <dd>

<span data-ttu-id="3bfee-139">0</span><span class="sxs-lookup"><span data-stu-id="3bfee-139">0</span></span>

<span data-ttu-id="3bfee-140">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="3bfee-140">Success.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="3bfee-141">2</span><span class="sxs-lookup"><span data-stu-id="3bfee-141">2</span></span>

<span data-ttu-id="3bfee-142">Zugriff verweigert.</span><span class="sxs-lookup"><span data-stu-id="3bfee-142">Access denied.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="3bfee-143">8</span><span class="sxs-lookup"><span data-stu-id="3bfee-143">8</span></span>

<span data-ttu-id="3bfee-144">Nicht spezifizierter Fehler.</span><span class="sxs-lookup"><span data-stu-id="3bfee-144">Unspecified failure.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="3bfee-145">9</span><span class="sxs-lookup"><span data-stu-id="3bfee-145">9</span></span>

<span data-ttu-id="3bfee-146">Ungültiges Objekt.</span><span class="sxs-lookup"><span data-stu-id="3bfee-146">Invalid object.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="3bfee-147">10</span><span class="sxs-lookup"><span data-stu-id="3bfee-147">10</span></span>

<span data-ttu-id="3bfee-148">Das Objekt ist bereits vorhanden.</span><span class="sxs-lookup"><span data-stu-id="3bfee-148">Object already exists.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="3bfee-149">11</span><span class="sxs-lookup"><span data-stu-id="3bfee-149">11</span></span>

<span data-ttu-id="3bfee-150">Das Dateisystem ist nicht NTFS.</span><span class="sxs-lookup"><span data-stu-id="3bfee-150">File system not NTFS.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="3bfee-151">12</span><span class="sxs-lookup"><span data-stu-id="3bfee-151">12</span></span>

<span data-ttu-id="3bfee-152">Plattform nicht Windows.</span><span class="sxs-lookup"><span data-stu-id="3bfee-152">Platform not Windows.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="3bfee-153">13</span><span class="sxs-lookup"><span data-stu-id="3bfee-153">13</span></span>

<span data-ttu-id="3bfee-154">Das Laufwerk ist nicht identisch.</span><span class="sxs-lookup"><span data-stu-id="3bfee-154">Drive not the same.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="3bfee-155">14</span><span class="sxs-lookup"><span data-stu-id="3bfee-155">14</span></span>

<span data-ttu-id="3bfee-156">„Verzeichnis ist nicht leer.“</span><span class="sxs-lookup"><span data-stu-id="3bfee-156">Directory not empty.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="3bfee-157">15</span><span class="sxs-lookup"><span data-stu-id="3bfee-157">15</span></span>

<span data-ttu-id="3bfee-158">Freigabeverletzung.</span><span class="sxs-lookup"><span data-stu-id="3bfee-158">Sharing violation.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="3bfee-159">16</span><span class="sxs-lookup"><span data-stu-id="3bfee-159">16</span></span>

<span data-ttu-id="3bfee-160">Ungültige Startdatei.</span><span class="sxs-lookup"><span data-stu-id="3bfee-160">Invalid start file.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="3bfee-161">17</span><span class="sxs-lookup"><span data-stu-id="3bfee-161">17</span></span>

<span data-ttu-id="3bfee-162">Die Berechtigung wurde nicht aufrechterhalten.</span><span class="sxs-lookup"><span data-stu-id="3bfee-162">Privilege not held.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="3bfee-163">21</span><span class="sxs-lookup"><span data-stu-id="3bfee-163">21</span></span>

<span data-ttu-id="3bfee-164">Ungültiger Parameter.</span><span class="sxs-lookup"><span data-stu-id="3bfee-164">Invalid parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3bfee-165">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3bfee-165">Remarks</span></span>

<span data-ttu-id="3bfee-166">Diese Methode wird zurzeit nicht von WMI implementiert.</span><span class="sxs-lookup"><span data-stu-id="3bfee-166">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="3bfee-167">Um diese Methode verwenden zu können, müssen Sie Sie in Ihrem eigenen Anbieter implementieren.</span><span class="sxs-lookup"><span data-stu-id="3bfee-167">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="3bfee-168">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="3bfee-168">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="3bfee-169">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="3bfee-169">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="3bfee-170">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3bfee-170">Requirements</span></span>



| <span data-ttu-id="3bfee-171">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3bfee-171">Requirement</span></span> | <span data-ttu-id="3bfee-172">Wert</span><span class="sxs-lookup"><span data-stu-id="3bfee-172">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3bfee-173">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="3bfee-173">Minimum supported client</span></span><br/> | <span data-ttu-id="3bfee-174">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3bfee-174">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="3bfee-175">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="3bfee-175">Minimum supported server</span></span><br/> | <span data-ttu-id="3bfee-176">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3bfee-176">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="3bfee-177">Namespace</span><span class="sxs-lookup"><span data-stu-id="3bfee-177">Namespace</span></span><br/>                | <span data-ttu-id="3bfee-178">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="3bfee-178">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="3bfee-179">MOF</span><span class="sxs-lookup"><span data-stu-id="3bfee-179">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3bfee-180"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="3bfee-180"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="3bfee-181">DLL</span><span class="sxs-lookup"><span data-stu-id="3bfee-181">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3bfee-182"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3bfee-182"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3bfee-183">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3bfee-183">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3bfee-184">CIM- \_ Verzeichnis</span><span class="sxs-lookup"><span data-stu-id="3bfee-184">CIM\_Directory</span></span>](changesecuritypermissionsex-method-in-class-cim-directory.md)
</dt> <dt>

[<span data-ttu-id="3bfee-185">**CIM- \_ Verzeichnis**</span><span class="sxs-lookup"><span data-stu-id="3bfee-185">**CIM\_Directory**</span></span>](cim-directory.md)
</dt> </dl>

 

