---
description: Bestimmt, ob der Aufrufer die aggregierten Berechtigungen für das CIM \_ -Verzeichnis Objekt und die Freigabe, auf der sich die Datei oder das Verzeichnis befindet, gemäß der Angabe durch das Berechtigungs Argument besitzt. Diese Methode wird von CIM \_ LogicalFile geerbt.
ms.assetid: b3dc1e3c-5c99-46ba-93c4-15fbf18e98e8
ms.tgt_platform: multiple
title: Geteffectiveberechtigungs Methode der CIM_Directory-Klasse (aclui. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Directory.GetEffectivePermission
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 436a30517b7f3306ef8be2426385fe385947296e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103860951"
---
# <a name="geteffectivepermission-method-of-the-cim_directory-class"></a><span data-ttu-id="1b4a2-104">Geteffectiveberechtigungs Methode der CIM- \_ Verzeichnis Klasse</span><span class="sxs-lookup"><span data-stu-id="1b4a2-104">GetEffectivePermission method of the CIM\_Directory class</span></span>

<span data-ttu-id="1b4a2-105">Mit der **geteffectiveberechtigungs** Methode wird festgelegt, ob der Aufrufer über die aggregierten Berechtigungen für das [**CIM- \_ Verzeichnis**](cim-directory.md) Objekt und die Freigabe, auf der sich die Datei oder das Verzeichnis befindet, gemäß der Angabe durch das **Berechtigungs** Argument verfügt.</span><span class="sxs-lookup"><span data-stu-id="1b4a2-105">The **GetEffectivePermission** method determines whether the caller has the aggregated permissions on the [**CIM\_Directory**](cim-directory.md) object, and the share on which the file or directory resides, as specified by the **Permission** argument.</span></span> <span data-ttu-id="1b4a2-106">Diese Methode wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="1b4a2-106">This method is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="1b4a2-107">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="1b4a2-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="1b4a2-108">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="1b4a2-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="1b4a2-109">In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet.</span><span class="sxs-lookup"><span data-stu-id="1b4a2-109">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="1b4a2-110">Weitere Informationen zum Verwenden dieser Methode finden Sie unter [Aufrufen einer Methode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="1b4a2-110">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="1b4a2-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="1b4a2-111">Syntax</span></span>


```mof
boolean GetEffectivePermission(
  [in] uint32 Permissions
);
```



## <a name="parameters"></a><span data-ttu-id="1b4a2-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="1b4a2-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1b4a2-113">*Berechtigungen* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1b4a2-113">*Permissions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1b4a2-114">Liste der Berechtigungen, über die der Benutzer Nachfragen können.</span><span class="sxs-lookup"><span data-stu-id="1b4a2-114">List of permissions that the user can inquire about.</span></span>

<dt>

<span id="FILE_READ_DATA__file__FILE_LIST_DIRECTORY__directory_"></span><span id="file_read_data__file__file_list_directory__directory_"></span><span id="FILE_READ_DATA__FILE__FILE_LIST_DIRECTORY__DIRECTORY_"></span>

<span data-ttu-id="1b4a2-115"><span id="FILE_READ_DATA__file__FILE_LIST_DIRECTORY__directory_"></span><span id="file_read_data__file__file_list_directory__directory_"></span><span id="FILE_READ_DATA__FILE__FILE_LIST_DIRECTORY__DIRECTORY_"></span>**Datei \_ \_Datei \_ Listen \_ Verzeichnis (Verzeichnis) lesen** (1 (0x1))</span><span class="sxs-lookup"><span data-stu-id="1b4a2-115"><span id="FILE_READ_DATA__file__FILE_LIST_DIRECTORY__directory_"></span><span id="file_read_data__file__file_list_directory__directory_"></span><span id="FILE_READ_DATA__FILE__FILE_LIST_DIRECTORY__DIRECTORY_"></span>**FILE\_READ\_DATA (file) FILE\_LIST\_DIRECTORY (directory)** (1 (0x1))</span></span>


</dt> <dd>

<span data-ttu-id="1b4a2-116">Gewährt das Recht, Daten aus der Datei zu lesen.</span><span class="sxs-lookup"><span data-stu-id="1b4a2-116">Grants the right to read data from the file.</span></span> <span data-ttu-id="1b4a2-117">Bei einem Verzeichnis gewährt dieser Wert das Recht, den Inhalt des Verzeichnisses aufzulisten.</span><span class="sxs-lookup"><span data-stu-id="1b4a2-117">For a directory, this value grants the right to list the contents of the directory.</span></span>

</dd> <dt>

<span id="FILE_WRITE_DATA__file__FILE_ADD_FILE__directory_"></span><span id="file_write_data__file__file_add_file__directory_"></span><span id="FILE_WRITE_DATA__FILE__FILE_ADD_FILE__DIRECTORY_"></span>

<span data-ttu-id="1b4a2-118"><span id="FILE_WRITE_DATA__file__FILE_ADD_FILE__directory_"></span><span id="file_write_data__file__file_add_file__directory_"></span><span id="FILE_WRITE_DATA__FILE__FILE_ADD_FILE__DIRECTORY_"></span>**Datei \_ Datei zum \_ Hinzufügen von Daten schreiben (Datei) Datei \_ Hinzufügen \_ (Verzeichnis)** (2 (0x2))</span><span class="sxs-lookup"><span data-stu-id="1b4a2-118"><span id="FILE_WRITE_DATA__file__FILE_ADD_FILE__directory_"></span><span id="file_write_data__file__file_add_file__directory_"></span><span id="FILE_WRITE_DATA__FILE__FILE_ADD_FILE__DIRECTORY_"></span>**FILE\_WRITE\_DATA (file) FILE\_ADD\_FILE (directory)** (2 (0x2))</span></span>


</dt> <dd>

<span data-ttu-id="1b4a2-119">Gewährt das Recht, Daten in die Datei zu schreiben.</span><span class="sxs-lookup"><span data-stu-id="1b4a2-119">Grants the right to write data to the file.</span></span> <span data-ttu-id="1b4a2-120">Bei einem Verzeichnis gewährt dieser Wert das Recht, eine Datei im Verzeichnis zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="1b4a2-120">For a directory, this value grants the right to create a file in the directory.</span></span>

</dd> <dt>

<span id="FILE_APPEND_DATA__file__FILE_ADD_SUBDIRECTORY__directory_"></span><span id="file_append_data__file__file_add_subdirectory__directory_"></span><span id="FILE_APPEND_DATA__FILE__FILE_ADD_SUBDIRECTORY__DIRECTORY_"></span>

<span data-ttu-id="1b4a2-121"><span id="FILE_APPEND_DATA__file__FILE_ADD_SUBDIRECTORY__directory_"></span><span id="file_append_data__file__file_add_subdirectory__directory_"></span><span id="FILE_APPEND_DATA__FILE__FILE_ADD_SUBDIRECTORY__DIRECTORY_"></span>**Datei \_ Anfügen von \_ Daten (Datei) \_ \_ Unterverzeichnis (Verzeichnis) hinzufügen** (4 (0x4))</span><span class="sxs-lookup"><span data-stu-id="1b4a2-121"><span id="FILE_APPEND_DATA__file__FILE_ADD_SUBDIRECTORY__directory_"></span><span id="file_append_data__file__file_add_subdirectory__directory_"></span><span id="FILE_APPEND_DATA__FILE__FILE_ADD_SUBDIRECTORY__DIRECTORY_"></span>**FILE\_APPEND\_DATA (file) FILE\_ADD\_SUBDIRECTORY (directory)** (4 (0x4))</span></span>


</dt> <dd>

<span data-ttu-id="1b4a2-122">Gewährt das Recht zum Anfügen von Daten an die Datei.</span><span class="sxs-lookup"><span data-stu-id="1b4a2-122">Grants the right to append data to the file.</span></span> <span data-ttu-id="1b4a2-123">Bei einem Verzeichnis gewährt dieser Wert das Recht, ein Unterverzeichnis zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="1b4a2-123">For a directory, this value grants the right to create a subdirectory.</span></span>

</dd> <dt>

<span id="FILE_READ_EA"></span><span id="file_read_ea"></span>

<span data-ttu-id="1b4a2-124"><span id="FILE_READ_EA"></span><span id="file_read_ea"></span>**Datei \_ Lesen von \_ EA** (8 (0x8))</span><span class="sxs-lookup"><span data-stu-id="1b4a2-124"><span id="FILE_READ_EA"></span><span id="file_read_ea"></span>**FILE\_READ\_EA** (8 (0x8))</span></span>


</dt> <dd>

<span data-ttu-id="1b4a2-125">Gewährt das Recht zum Lesen erweiterter Attribute.</span><span class="sxs-lookup"><span data-stu-id="1b4a2-125">Grants the right to read extended attributes.</span></span>

</dd> <dt>

<span id="FILE_WRITE_EA"></span><span id="file_write_ea"></span>

<span data-ttu-id="1b4a2-126"><span id="FILE_WRITE_EA"></span><span id="file_write_ea"></span>**Datei \_ Schreiben von \_ EA** (16 (0x10))</span><span class="sxs-lookup"><span data-stu-id="1b4a2-126"><span id="FILE_WRITE_EA"></span><span id="file_write_ea"></span>**FILE\_WRITE\_EA** (16 (0x10))</span></span>


</dt> <dd>

<span data-ttu-id="1b4a2-127">Gewährt das Recht, erweiterte Attribute zu schreiben.</span><span class="sxs-lookup"><span data-stu-id="1b4a2-127">Grants the right to write extended attributes.</span></span>

</dd> <dt>

<span id="FILE_EXECUTE__file__FILE_TRAVERSE__directory_"></span><span id="file_execute__file__file_traverse__directory_"></span><span id="FILE_EXECUTE__FILE__FILE_TRAVERSE__DIRECTORY_"></span>

<span data-ttu-id="1b4a2-128"><span id="FILE_EXECUTE__file__FILE_TRAVERSE__directory_"></span><span id="file_execute__file__file_traverse__directory_"></span><span id="FILE_EXECUTE__FILE__FILE_TRAVERSE__DIRECTORY_"></span>**Datei \_ Execute (File) file \_ Traversieren (Verzeichnis)** (32 (0x20))</span><span class="sxs-lookup"><span data-stu-id="1b4a2-128"><span id="FILE_EXECUTE__file__FILE_TRAVERSE__directory_"></span><span id="file_execute__file__file_traverse__directory_"></span><span id="FILE_EXECUTE__FILE__FILE_TRAVERSE__DIRECTORY_"></span>**FILE\_EXECUTE (file) FILE\_TRAVERSE (directory)** (32 (0x20))</span></span>


</dt> <dd>

<span data-ttu-id="1b4a2-129">Gewährt das Recht, eine Datei auszuführen.</span><span class="sxs-lookup"><span data-stu-id="1b4a2-129">Grants the right to execute a file.</span></span> <span data-ttu-id="1b4a2-130">Für ein Verzeichnis kann das Verzeichnis durchsucht werden.</span><span class="sxs-lookup"><span data-stu-id="1b4a2-130">For a directory, the directory can be traversed.</span></span>

</dd> <dt>

<span id="FILE_DELETE_CHILD__directory_"></span><span id="file_delete_child__directory_"></span><span id="FILE_DELETE_CHILD__DIRECTORY_"></span>

<span data-ttu-id="1b4a2-131"><span id="FILE_DELETE_CHILD__directory_"></span><span id="file_delete_child__directory_"></span><span id="FILE_DELETE_CHILD__DIRECTORY_"></span>**Datei \_ \_Child (Verzeichnis) löschen** (64 (0x40))</span><span class="sxs-lookup"><span data-stu-id="1b4a2-131"><span id="FILE_DELETE_CHILD__directory_"></span><span id="file_delete_child__directory_"></span><span id="FILE_DELETE_CHILD__DIRECTORY_"></span>**FILE\_DELETE\_CHILD (directory)** (64 (0x40))</span></span>


</dt> <dd>

<span data-ttu-id="1b4a2-132">Gewährt das Recht, ein Verzeichnis und alle darin enthaltenen Dateien zu löschen, selbst wenn die Dateien schreibgeschützt sind.</span><span class="sxs-lookup"><span data-stu-id="1b4a2-132">Grants the right to delete a directory and all the files it contains, even if the files are read-only.</span></span>

</dd> <dt>

<span id="FILE_READ_ATTRIBUTES"></span><span id="file_read_attributes"></span>

<span data-ttu-id="1b4a2-133"><span id="FILE_READ_ATTRIBUTES"></span><span id="file_read_attributes"></span>**Datei \_ Lese \_ Attribute** (128 (0x80))</span><span class="sxs-lookup"><span data-stu-id="1b4a2-133"><span id="FILE_READ_ATTRIBUTES"></span><span id="file_read_attributes"></span>**FILE\_READ\_ATTRIBUTES** (128 (0x80))</span></span>


</dt> <dd>

<span data-ttu-id="1b4a2-134">Gewährt das Recht zum Lesen von Dateiattributen.</span><span class="sxs-lookup"><span data-stu-id="1b4a2-134">Grants the right to read file attributes.</span></span>

</dd> <dt>

<span id="FILE_WRITE_ATTRIBUTES"></span><span id="file_write_attributes"></span>

<span data-ttu-id="1b4a2-135"><span id="FILE_WRITE_ATTRIBUTES"></span><span id="file_write_attributes"></span>**Datei \_ \_Attribute schreiben** (256 (0x100))</span><span class="sxs-lookup"><span data-stu-id="1b4a2-135"><span id="FILE_WRITE_ATTRIBUTES"></span><span id="file_write_attributes"></span>**FILE\_WRITE\_ATTRIBUTES** (256 (0x100))</span></span>


</dt> <dd>

<span data-ttu-id="1b4a2-136">Erteilt das Recht, Dateiattribute zu ändern.</span><span class="sxs-lookup"><span data-stu-id="1b4a2-136">Grants the right to change file attributes.</span></span>

</dd> <dt>

<span id="DELETE"></span><span id="delete"></span>

<span data-ttu-id="1b4a2-137"><span id="DELETE"></span><span id="delete"></span>**Löschen** (65536 (0x10000))</span><span class="sxs-lookup"><span data-stu-id="1b4a2-137"><span id="DELETE"></span><span id="delete"></span>**DELETE** (65536 (0x10000))</span></span>


</dt> <dd>

<span data-ttu-id="1b4a2-138">Gewährt Lösch Zugriff.</span><span class="sxs-lookup"><span data-stu-id="1b4a2-138">Grants delete access.</span></span>

</dd> <dt>

<span id="READ_CONTROL"></span><span id="read_control"></span>

<span data-ttu-id="1b4a2-139"><span id="READ_CONTROL"></span><span id="read_control"></span>**Lesen Sie \_ Steuer** Element (131072 (0x20000))</span><span class="sxs-lookup"><span data-stu-id="1b4a2-139"><span id="READ_CONTROL"></span><span id="read_control"></span>**READ\_CONTROL** (131072 (0x20000))</span></span>


</dt> <dd>

<span data-ttu-id="1b4a2-140">Gewährt Lesezugriff auf die Sicherheits Beschreibung und den Besitzer.</span><span class="sxs-lookup"><span data-stu-id="1b4a2-140">Grants read access to the security descriptor and owner.</span></span>

</dd> <dt>

<span id="WRITE_DAC"></span><span id="write_dac"></span>

<span data-ttu-id="1b4a2-141"><span id="WRITE_DAC"></span><span id="write_dac"></span>**Schreiben \_ DAC** (262144 (0x40000))</span><span class="sxs-lookup"><span data-stu-id="1b4a2-141"><span id="WRITE_DAC"></span><span id="write_dac"></span>**WRITE\_DAC** (262144 (0x40000))</span></span>


</dt> <dd>

<span data-ttu-id="1b4a2-142">Gewährt Schreibzugriff auf die freigegebene ACL.</span><span class="sxs-lookup"><span data-stu-id="1b4a2-142">Grants write access to the discretionary ACL.</span></span>

</dd> <dt>

<span id="WRITE_OWNER"></span><span id="write_owner"></span>

<span data-ttu-id="1b4a2-143"><span id="WRITE_OWNER"></span><span id="write_owner"></span>**Schreiben \_ Besitzer** (524288 (0x80000))</span><span class="sxs-lookup"><span data-stu-id="1b4a2-143"><span id="WRITE_OWNER"></span><span id="write_owner"></span>**WRITE\_OWNER** (524288 (0x80000))</span></span>


</dt> <dd>

<span data-ttu-id="1b4a2-144">Weist den Schreib Besitzer zu.</span><span class="sxs-lookup"><span data-stu-id="1b4a2-144">Assigns the write owner.</span></span>

</dd> <dt>

<span id="SYNCHRONIZE"></span><span id="synchronize"></span>

<span data-ttu-id="1b4a2-145"><span id="SYNCHRONIZE"></span><span id="synchronize"></span>**Synchronisieren** (1048576 (0x100000))</span><span class="sxs-lookup"><span data-stu-id="1b4a2-145"><span id="SYNCHRONIZE"></span><span id="synchronize"></span>**SYNCHRONIZE** (1048576 (0x100000))</span></span>


</dt> <dd>

<span data-ttu-id="1b4a2-146">Synchronisiert den Zugriff und ermöglicht es einem Prozess zu warten, bis ein Objekt in den signalisierten Zustand wechselt.</span><span class="sxs-lookup"><span data-stu-id="1b4a2-146">Synchronizes access and allows a process to wait for an object to enter the signaled state.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1b4a2-147">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1b4a2-147">Return value</span></span>

<span data-ttu-id="1b4a2-148">Gibt **true** zurück, wenn der-Befehl über die erforderliche Berechtigung verfügt. Andernfalls wird **false** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="1b4a2-148">Returns **True** if the call has the necessary permission; otherwise, it returns **false**.</span></span>

## <a name="remarks"></a><span data-ttu-id="1b4a2-149">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1b4a2-149">Remarks</span></span>

<span data-ttu-id="1b4a2-150">Diese Methode wird zurzeit nicht von WMI implementiert.</span><span class="sxs-lookup"><span data-stu-id="1b4a2-150">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="1b4a2-151">Um diese Methode verwenden zu können, müssen Sie Sie in Ihrem eigenen Anbieter implementieren.</span><span class="sxs-lookup"><span data-stu-id="1b4a2-151">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="1b4a2-152">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="1b4a2-152">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="1b4a2-153">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="1b4a2-153">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="1b4a2-154">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1b4a2-154">Requirements</span></span>



| <span data-ttu-id="1b4a2-155">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1b4a2-155">Requirement</span></span> | <span data-ttu-id="1b4a2-156">Wert</span><span class="sxs-lookup"><span data-stu-id="1b4a2-156">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1b4a2-157">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1b4a2-157">Minimum supported client</span></span><br/> | <span data-ttu-id="1b4a2-158">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1b4a2-158">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="1b4a2-159">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1b4a2-159">Minimum supported server</span></span><br/> | <span data-ttu-id="1b4a2-160">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1b4a2-160">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="1b4a2-161">Namespace</span><span class="sxs-lookup"><span data-stu-id="1b4a2-161">Namespace</span></span><br/>                | <span data-ttu-id="1b4a2-162">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="1b4a2-162">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="1b4a2-163">Header</span><span class="sxs-lookup"><span data-stu-id="1b4a2-163">Header</span></span><br/>                   | <dl> <span data-ttu-id="1b4a2-164"><dt>Aclui. h</dt></span><span class="sxs-lookup"><span data-stu-id="1b4a2-164"><dt>Aclui.h</dt></span></span> </dl>      |
| <span data-ttu-id="1b4a2-165">MOF</span><span class="sxs-lookup"><span data-stu-id="1b4a2-165">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1b4a2-166"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="1b4a2-166"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="1b4a2-167">DLL</span><span class="sxs-lookup"><span data-stu-id="1b4a2-167">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1b4a2-168"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1b4a2-168"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1b4a2-169">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1b4a2-169">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1b4a2-170">**CIM- \_ Verzeichnis**</span><span class="sxs-lookup"><span data-stu-id="1b4a2-170">**CIM\_Directory**</span></span>](geteffectivepermission-method-in-class-cim-directory.md)
</dt> <dt>

[<span data-ttu-id="1b4a2-171">**CIM- \_ Verzeichnis**</span><span class="sxs-lookup"><span data-stu-id="1b4a2-171">**CIM\_Directory**</span></span>](cim-directory.md)
</dt> </dl>

 

